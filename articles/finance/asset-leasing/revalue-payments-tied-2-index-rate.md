---
title: Indeksimääraga seotud rendimaksete ümberhindamine
description: See artikkel kirjeldab korrektsiooni, mis tehakse kasutusva vara (RUB) kohustuse liisimiseks muutuvate rendimaksete muutmisel indeksi määra muutuse tõttu.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8dc2325e9f0651bea0d70d9f66e5d88b741009f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903243"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Indeksimääraga seotud rendimaksete ümberhindamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab korrektsiooni, mida tehakse kasutusse antud liisingukohustusele (RUB), kui muutuvad rendimaksed muutuvad indeksimäära muutuse tõttu. Rendikohustist ja kasutamisõiguse esemeks olevaid varasid korrigeeritakse uute maksesummade arvestamiseks. Raamatupidamise standardite kodeerimise teema 842 (ASC 842), mis on üldtunnustatud raamatupidamispõhimõtete standard USA-s (USA RAAMATUPIDAMISTAVA), kohaselt muutuvad ainult muutuvad maksed, kui makse indeksimäära muutumise tõttu suureneb või väheneb, välja arvatud juhul, kui rahavoogudes esinevad täiendavad muudatused. Need täiendavad muudatused võivad hõlmata intressimääradega seotud rendilepingu tingimuste muutmist. Lisateavet vt teemast ASC 842-10-55-225 ja rahvusvahelise finantsaruandluse standardi 16 (IFRS 16) § 42 punktist b.

## <a name="adjust-lease-payments"></a>Rendimaksete korrigeerimine

Indeksimääraga seotud rendimaksete ümberhindamiseks toimige järgmiselt.

1. Rendi indeksi ümberhindamise protsessi käivitamiseks avage jaotis **Vara rentimine \> Perioodiline \> Indeksimäära ümberhindamine**.

    Kuvatakse leht **Indeksimäära ümberhindamine** ja kuvatakse kõik varem käitatud rendi indeksi ümberhindamise protsessid. Sellel lehel olev teave sisaldab protsessi ID-d, mis loodi numbriseeria seadistusest, juriidilist isikust, korrigeeritud rendiraamatute arvu, IFRS 16 rendi kohustise summa korrigeerimist ja muutuvate maksete summat, mis ASC 842 rendilepingute jaoks korrigeeriti.

2. Ümberhindamise alustamiseks valige tegevuspaanil suvand **Rendi indeksi ümberhindamine**.

    Kuvatakse dialoogiboks **Indeksi ümberhindamise parameetrid**. Siin saate filtreerida ja valida, millised rendilepingud, rendilepingute grupid või muud kriteeriumid tuleks ümberhindamiseks rendilepingute valimisel arvesse võtta. Lisaks saate vahekaardil **Käivita taustal** seadistada indeksi ümberhindamise protsessi nii, et see töötaks partiina.

4. Valige filtrid, et valida rendilepingud, mis tuleks taustal töötlemisse kaasata, ja seejärel valige **OK**.

    Kuvatakse dialoogiboks **Indeksimäära ümberhindamise eelvaade** ja kuvatakse ümberarvutatavad rendilepingud. Kuvatakse ka vara ja kohustiste korrigeerimisi või muutuvate maksete korrigeerimisi.

5. Rendilepingute ümberarvutamise vältimiseks valige rendilepingud, mis **tuleks** ümberarvutada. Kui te ei vali ühtegi rendilepingut, hinnatakse kõik rendilepingud ümber. Kui olete lõpetanud, valige rendimaksete ümberhindamiseks **OK**.
6. Kindla indeksi ümberhindamise protsessi jaoks loodud kannete vaatamiseks valige protsessi ID ja seejärel valige **Kanded**.

    Kuvatakse dialoogiboks ja kuvatakse töötlemise käigus loodud kannete üksikasjad.

> [!NOTE]
> Ainult need rendilepingud, millel on ümberhindamise kuupäev kas süsteemi kuupäeval või enne seda, hinnatakse ümber. Süsteem eirab automaatselt kõiki rendilepinguid, mille ümberhindamise kuupäev on hilisem kui süsteemi kuupäev.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842 rendilepingud – indeksi ümberhindamine

ASC 842 rendilepingute ümberhindamise mõju vaatamiseks avage rendilepingu maksegraafik. Lehel kuvatakse ainult indeksi ümberarvutamise tõttu tehtud ümberhindamise kuupäeval või pärast seda tehtud muutuvad maksed. Amortisatsiooni ja kulumi graafikuid ei muudeta. Kui loote arve, millel on muutuv makse, siis debiteeritakse muutuv makse muutuva makse sisestuskontole. Samuti lisatakse muutuv maksesumma kreeditkandele, mis sisestatakse otse hankijale, või sisestatakse Märkuste ostureskontrole, sõltuvalt rendiraamatu seadistusest.

Rendilepingu üksikasjade lehe maksegraafiku ridu uuendatakse automaatselt, lisades uue rea, mis näitab uut indeksimäära. Lisaks näitab veerg, kas rida loodi käsitsi või indeksi ümberhindamise protsessi kaudu.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16 rendilepingud – indeksi ümberhindamine

IFRS 16 rendilepingute ümberhindamise mõju vaatamiseks avage korrigeeritud rendilepingu üksikasjad. Väljad **Rendiperiood** ja **Vara kasulik tööiga** värskendatakse, et kajastada aja möödumist alguskuupäevast või muutmiskuupäevast ümberhindamise kuupäevani. Lisaks on maksegraafiku read uuendatud, et kajastada uusi rendimakseid, uut indeksimäära ja seda, kuidas rida on loodud.

Saate vaadata värskeltloodud maksegraafikut, mis algab ümberhindamise kuupäevast ja näitab värskendatud makse kogusummat. Loodud on ka uus rendikohustise amortisatsioonigraafik ja vara kulumigraafik, mis peegeldavad korrigeeritud maksegraafikut.

Töölehe kirje sisestas korrigeerimise töölehe kirje automaatselt kontole indeksi ümberhindamisega seotud rendimaksete muutmiseks.

> [!NOTE]
> **Kui** liisingu üksikasjade lehe üldisel kiirkaardil on lubatud suvand Jaotuse maksesumma ja seotud raamatuks **on** **IFRS** 16, **lisab** indeksi ümberhindamise protsess automaatselt kirje makse summa katkestuse dialoogiboksis. Summa peegeldab makses tehtud muudatust indeksi ümberhindamise tõttu. Kirje märgitakse kui Kasutatud **IRFS 16 indeksi ümberhindamise jaoks**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
