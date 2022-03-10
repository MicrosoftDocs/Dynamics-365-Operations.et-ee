---
title: Teatiste pakktöötlus
description: See teema annab teavet teatiste pakktöötluse kohta.
author: RichdiMSFT
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 0ec2a9bd925ccd7dc7c6a8251629bf565ece2268
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416425"
---
# <a name="batch-processing-of-alerts"></a>Teatiste pakktöötlus

[!include [banner](../includes/banner.md)]

Teatisi töödeldakse pakktöötluse funktsioonidega. Enne teatiste töötlemist ja edastamist peate häälestama pakett-töötluse.

Pakett-töötluse funktsioon toetab kaht tüüpi sündmusi.

- Sündmused, mille käivitavad muutuspõhised sündmused. Neile viidatakse ka kui sündmused Loo/Kustuta ja Värskenda.
- Sündmused, mille käivitavad tähtajad.

Pakktöötlust saab seadistada mõlemat tüüpi sündmuse jaoks.

## <a name="batch-processing-for-change-based-events"></a>Muutuspõhiste sündmuste pakktöötlus

Süsteem arvestab kõiki muutuspõhiseid sündmusi, mis on toimunud pärast pakktöötluse viimast käivitamist. Muutusel põhinevad sündmused hõlmavad väljade värskendusi, kirjete kustutamist ja kirjete loomist. Neid sündmusi võrreldakse teie poolt teatisereeglites seadistatud tingimustega. Kui sündmus kattub reegli tingimustega, loob pakktöötlus teatise.

### <a name="frequency-for-change-based-events"></a>Muutuspõhiste sündmuste sagedus

Muutusel põhinevate sündmuste jaoks saab seadistada pakett-töö, mis käivitab sündmuse töötlemise varsti pärast seda, kui süsteem sündmuse logib. Kui seadistate pakett-töö sagedasema kordumise, saavad kasutajad muudatuste toimumisest varem teatiseid. Kuid väga sage pakktöötlus võib ebasoodsalt mõjutada süsteemi jõudlust.

Teisest küljest võib harvemini korduv pakett-töö, mille plaanite ajale, mil süsteemi koormus on väike, aidata parandada süsteemi jõudlust. Kuid liiga harv pakktöötlus ei pruugi vastata kasutajate nõudmistele õigeaegsete teatiste osas.

Seetõttu tuleb muutuspõhiste sündmuste pakktöötluse sageduse seadistamisel arvestada teatiste õigeaegsuse ja kogu süsteemi jõudluse vahelist tasakaalu. Sellised kaalutlused on veelgi olulisemad, kui teatisereegleid loovate isikute arv suureneb. Sagedus ei mõjuta süsteemi töödeldavate sündmuste arvu. Ent mida rohkem on reegleid loovaid kasutajaid, seda rohkem kontrolle protsess teeb. Seda tüüpi andmevahetus võib mõjutada süsteemi jõudlust.

#### <a name="the-risks-of-low-batch-frequency"></a>Väikese sagedusega pakett-töö riskid

Muutuspõhiste sündmuste vähese sagedusega pakett-töötlus võib põhjustada olukorra, kus andmed, mis on olulised teatisereegli tingimuste suhtes, võivad muutuda enne töötlemist. Seetõttu võivad teatised kaotsi minna.

Näiteks on loote teatise käivitamise, kui sündmus on **Kliendi kontaktandmete muutumine** ja tingimuseks on **Klient = BB**. Teisisõnu, kui kliendi BB kliendikontakt muutub, logib protsess sündmuse. Siiski on pakktöötluse süsteem seadistatud selliselt, et pakktöötlus käivitatakse harvemini kui andmesisestus. Kui kliendi nimi muutub **BB-st** **AA-ks** enne sündmuse töötlust, ei ühti enam reegli tingimus **klient = BB** andmebaasis olevate andmetega. Seetõttu ei looda hilisemal sündmuse töötlusel teatist.

### <a name="set-up-processing-for-change-based-alerts"></a>Muutusepõhiste teatiste töötlemise seadistamine

1. Avage **Süsteemihaldus** &gt; **Perioodilised ülesanded** &gt; **Teatised** &gt; **Muutuspõhised teatised**.
2. Sisestage asjakohane teave dialoogiboksi **Muutuspõhised teatised**.

## <a name="batch-processing-for-due-date-events"></a>Tähtajaliste sündmuste pakktöötlus

Süsteem tuvastab kõik tähtaegadest tingitud sündmused ja neid sündmusi võrreldakse teatisereeglites seadistatud tingimustega. Kui sündmus kattub reegli tingimustega, loob pakktöötlus teatise.

### <a name="frequency-for-due-date-events"></a>Tähtajaliste sündmuste sagedus

Võimalik, et soovite seadistada tähtajaliste sündmuste jaoks pakett-tööd, mida käivitatakse süsteemi koormuse tasakaalustamiseks kas öösiti või kindlal päevasel kellaajal. Soovitatav on seadistada pakett-töö selliselt, et seda käivitataks vähemalt üks kord päevas. Kui teatisi tuleks väljastada võimalikult varakult, siis tuleks pakett-töötlus seadistada toimuma võimalikult vahetult pärast süsteemi kuupäeva muutumist. Tähtajaliste sündmuste teatiste loomiseks pärast seda, kui tähtajaliste sündmuste pakett-töö on juba toimunud, võib pakett-töö samal päeval uuesti käitada.

Näiteks on pakett-töö teatud päeval käivitatud. Seejärel loote ostutellimuse, millel on tähtaeg, mis peaks teatise samal päeval käivitama. Sel päeval teatise saamiseks peate pakett-töö pärast ostutellimuse loomist uuesti käivitama. Kui aga pakett-tööd samal päeval uuesti ei käivitata, siis tuvastab järgmise päeva pakett-töö kõik eelmisel päeval töötlemata jäänud tähtajalised sündmused.

> [!NOTE]
> Isegi kui pakktöötlus toimub rohkem kui korra päevas, ei dubleerita teatist sama tähtajalise sündmuse ja tingimuste jaoks. Kõigi saabunud tähtaegade puhul luuakse teatisi ainult juhul, kui muutused on süsteemis toimunud pärast pakett-töö viimast käivitamist.

### <a name="batch-processing-window"></a>Pakktöötluse aken

Ettevõtte teatisereeglite töötlemine võidakse peatada mitmel põhjusel. Nende põhjuste hulka kuuluvad puhkused, süsteemi tõrked või muud probleemid, mis takistavad mõneks ajaks pakett-tööde käitamise.

Vältimaks tähtajaliste teatiste muutumist aegunuks seetõttu, et pakett-tööd pole mitu päeva käivitatud, saate seadistada pakktöötluse akna. Pakktöötluse akent saab kasutada, et takistada pakett-töö käivitamist määratud päevade arvu jooksul.

Pakktöötluse akna seadistamisel saadetakse teatis teatisereegli töötlemise kohta ka juhul, kui teatis ületab tähtaja kriteeriumides määratud ajalimiidi. Teatise väljastamist jätkatakse seni, kuni pole ületatud ajalimiidis määratud perioodi ega pakktöötluse akent. Samas teatist ei saadeta, kui periood ületab ajalimiidi perioodi ja pakktöötluse akna määratud väärtuse.

### <a name="set-up-processing-for-due-date-alerts"></a>Tähtajapõhiste teatiste töötlemise seadistamine

1. Avage **Süsteemihaldus** &gt; **Perioodilised ülesanded** &gt; **Teatised** &gt; **Tähtajateatised**.
2. Sisestage asjakohane teave dialoogiboksi **Tähtajateatised**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
