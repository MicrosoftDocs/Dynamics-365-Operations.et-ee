---
title: Laohalduse vabade kirjete puhastustöö
description: Selles teemas kirjeldatakse vabade kirjete puhastustööd, mis aitab parandada süsteemi jõudlust, tuvastades ja kustutades seotud, kuid mittevajalikud kirjed.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f045b9686bbdfcf3e82f5158f0fd28860354b7d7
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014479"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Laohalduse vabade kirjete puhastustöö

Vabade varude arvutamiseks kasutatavat päringute jõudlust mõjutab kaasatud tabelites sisalduvate kirjete arv. Üks viis jõudluse parandamiseks on vähendada kirjete arvu, mida andmebaas peab arvestama.

Selles teemas kirjeldatakse vabade kirjete puhastustööd, mille käigus kustutatakse tabelitest InventSum ja WHSInventReserve ebavajalikud kirjed. Antud tabelid talletavad laohalduse töötlemise jaoks lubatud kaupade vabade varude teavet. (Neid kaupu nimetatakse WHS kaupadeks.) Antud kirjete kustutamine võib parandada märkimisväärselt vabade varude arvutuste jõudlust.

## <a name="what-the-cleanup-job-does"></a>Puhastustöö otstarve

Vabade kirjete puhastustöö käigus kustutatakse kõik tabelis WHSInventReserve ja InventSum sisalduvad kirjed, kus kõik väljaväärtused on *0* (null). Need kirjed võib kustutada, kuna need ei anna vabade varude teabele midagi juurde. Töö käigus kustutatakse vaid kirjed, mille tase jääb alla taseme **Asukoht**.

Negatiivseete füüsiliste varude lubamise korral ei pruugita puhastustöö käigus kustutada kõiki asjakohaseid kandeid. Selle piirangu põhjuseks on tõsiasi, et töö peab võimaldama eristsenaariumit, kus litsentsiplaadil on mitu seerianumbrit ja üks neist seerianumbritest on muutunud negatiivseks. Näiteks on süsteemis litsentsiplaadi tasemel vabade varude väärtus null, kui litsentsiplaadil on +1 tk seerianumbrit 1 ja -1 tk seerianumbrit 2. Antud eristsenaariumi korral teostatakse töö raames esmalt ulatusepõhine kustutamine, kus üritatakse kustutada esmalt madalamatest tasemetest.

## <a name="schedule-and-configure-the-cleanup-job"></a>Puhastustöö kavandamine ja konfigureerimine

Vabade varude puhastustöö on saadaval asukohas **Varude haldus \> Perioodilised ülesanded \> Puhastus \> Laohalduse vabade kirjete puhastustöö**. Töö käitamise ulatuse ja graafiku kontrollimiseks kasutage tavapäraseid töösätteid. Lisaks pakutakse järgmisi sätteid.

- **Kustutada, kui pole värskendatud antud arv päevi** – sisestage minimaalne päevade arv, kui kaua töö peaks ootama enne nullkoguseni langenud vabade varude kirje kustutamist. Kasutage seda sätet, et vähendada kasutatavate vabade varude kirjete kustutamise ohtu. Kui soovite teostada puhastustöö esimesel võimalusel, siis sisestage väärtuseks *0* (null) või jätke väli tühjaks.
- **Maksimaalne teostamisaeg (tundides)** – sisestage puhastustöö maksimaalne teostamisaeg tundides. Kui töö ei ole enne selle aja möödumist lõpule viidud, siis salvestatakse seni tehtud töö ja suletakse toiming. See võimalus on eriti oluline rakenduste puhul, kus varude kasutamise tase on kõrge. Sellisel juhul tuleb planeerida töö käitamine ajale, mil süsteemi koormus on võimalikult väike. Kui soovite, et partiitöö jätkuks lõpule viimiseni, siis sisestage väärtuseks *0* (null) või jätke väli tühjaks. See säte on saadaval vaid juhul, kui seotud funktsioon on [teie süsteemis sisse lülitatud](#max-execution-time).

Kuigi te saate käitada tööd tavatöötundide ajal, siis soovitame seda käitada väljaspool tavatööaega. See aitab ära hoida võimalikke konflikte, mis võivad tekkida juhul, kui kasutaja töötab kirjega, mida samal ajal ka puhastatakse.

Kui töö proovib kustutada kauba kirjet samal ajal, kui teine kasutaja antud kirjet kasutab, siis esineb puhastutöö käigus või kasutaja jaoks tupiktõrge.

Töö käitamisel on selle kinnitustase 100. Teisisõnu püütakse iga 100 kustutamise järel teostada üks kinnitus. Kuna mõned kustutamised on kogumipõhised, siis võib esineda stsenaariume, kus ühe tehingu käigus võidakse kustutada enam kui 100 kirjet. Seega võivad aeg-ajalt esineda lukustuslaiendused.

## <a name="possible-user-impact"></a>Võimalik mõju kasutajale

Kui puhastustöö käigus kustutatakse kõik puhastustöö vabade kirjete andmed konkreetse taseme kohta (nt litsentsiplaadi tase), siis võib see mõjutada ka kasutajaid. Sellisel juhul ei pruugi antud varude nägemiseks varasemalt litsentsiplaadil saadaolev funktsioon õigesti töötada, kuna asjakohased vabad kirjed ei ole enam saadaval. See võib näiteks esineda järgmistes olukordades.

- **Vaba kaubavaru loendis**, kui kasutaja tühistab tingimuse **Kogus \<\> 0** või valib tingimus **Suletud kanded** sätetes **Dimensioonide kuva**.
- Möödunud perioodide aruandes **Füüsilised laovarud varude dimensiooni alusel**, kui kasutaja määrab parameetri **Kuupäeva järgi**.

Samas jõudluse parandamine, mida puhastustöö pakub, peaks need väikesed funktsionaalsuse kahjumid hüvitama.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Maksimaalse teostamisaja kättesaadavaks muutmine

**Maksimaalse teostamisaja** säte ei ole vaikesättena kättesaadav. Kui soovite seda kasutada, peate kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lülitada seotud funktsioon oma süsteemis sisse. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Laohalduse vabade kirjete puhastustöö maksimaalne teostamisaeg*
