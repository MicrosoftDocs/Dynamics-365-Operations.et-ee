---
title: Juriidilise isiku ettevalmistamine konsolideerimisprotsessiks
description: Konsolideerimise ajal kogute kanded mitmetelt juriidiliste isikute kontokomplektidelt ühte juriidilise isiku kontokomplekti. Selles teemas kirjeldatakse, kuidas juriidilist isikut konsolideerimiseks ette valmistada.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990296"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Juriidilise isiku ettevalmistamine konsolideerimisprotsessiks

[!include [banner](../includes/banner.md)]

Konsolideerimise ajal kogute kanded mitmetelt juriidiliste isikute kontokomplektidelt ühte juriidilise isiku kontokomplekti. Selles teemas kirjeldatakse, kuidas juriidilist isikut konsolideerimiseks ette valmistada.

> [!NOTE]
> Soovitame teil kasutada rakenduse Microsoft Dynamics 365 Finance Management Reporterit, et kombineerida finantstulemused mitme juriidilise isiku jaoks konsolideeritud vormingus. Management Reporter võimaldab luua konsolideeritud finantsaruandeid juriidiliste isikute lõikes, kasutada Excelit konsolideerimise andmete importimiseks teistest allikatest ja teisendada summad mis tahes arvuks aruandlusvaluutadeks ilma, et konsolideerimisprotsessi oleks vaja rakenduses Dynamics 365 Finance käivitada.

Saate konsolideeritud juriidiliselt isikult aruandeid (nt finantsaruandeid) printida. Kuid te ei saa igapäevasteks kanneteks kasutada konsolideeritud juriidilist isikut.

Saate konsolideerida andmeid juriidilistelt isikutelt, mis kasutavad konsolideeritud juriidilise isiku andmebaasist erinevaid andmebaase. Sellele konsolideerimisprotsessile viidatakse kui *impordi konsolideerimisele*. Teise võimalusena saavad juriidilised isikud kasutada konsolideeritud juriidilise isikuga sama andmebaasi. Sellele konsolideerimisprotsessile viidatakse kui *võrgus konsolideerimisele*.

Konsolideeritud juriidiline isik kogub tütarettevõtete tulemusi ja saldosid. Konsolideeritud juriidilise isiku konsolideerimiseks ettevalmistamiseks toimige järgmiselt.

1. Avage **Pearaamat \> Seadistus \> Organisatsioon \> Juriidilised isikud**.
2. Valige **Uus**, et luua uus juriidiline isik, mis on konsolideeritud juriidiline isik.
3. Valige märkeruut **Kasuta finantskonsolideeritmise protsessi** ja seejärel sisestage teave konsolideeritud juriidilise isiku kohta. Sisestage kindlasti see teave täpselt nii, nagu soovite seda konsolideeritud juriidilise isiku finantsaruandes näha.
4. Sulgege leht.
5. Valige lehe ülemise parempoolse nurga väljal konsolideeritud juriidiline isik ja seejärel valige **OK**.
6. Avage **Pearaamat \> Seadistus \> Pearaamat**.
7. Valige konsolideeritud juriidilisele isikule kontoplaan, rahanduskalender, arvestusvaluuta, valikuline aruandlusvaluuta ja vahetuskursi vaiketüüp. 
8. Avage **Pearaamat \> Seadistus \> Valuuta \> Valuuta vahetuskursi määrad**.
9. Seadistage tütarettevõttena tegutsevate juriidiliste isikute valuutadele valuutavahetuskursid asjakohasteks perioodideks.
10. Sulgege leht.
11. Kui konsolideeritud juriidilisel isikul on tütarettevõtteid, mis kasutavad välisvaluutat, toimige järgmiselt.

    1. Avage **Pearaamat \> Seadistus \> Sisestamine \> Kontod automaatseteks kanneteks**.
    2. Valige väljal **Sisestamise tüüp** sobiv konto.

        - Kui juriidilisel isikul on välismaiseid tütarettevõtteid, mis on finantsiliselt või tegevusliselt emaettevõtte juriidilise isikuga vastastikku sõltuvad, valige sobiv konto sisestustüübile **Kasum ja kahjum erinevuste sisestamiseks konsolideeritud**.
        - Kui konsolideerite tütarettevõtte, mis on rahaliselt ja juhtimiselt emaüksuse juriidilisest isikust sõltumatu, või juriidilise isiku, mis hõlmab tulemusi mitmelt tütarettevõttelt, mis on rahaliselt ja juhtimiselt peamisest juriidilisest isikust sõltumatu, ja kui kasutate andmete konsolideerimiseks teisendamismeetodeid, valige sisestamise tüübile **Konsolideerimiserinevuste saldo konto** sobiv konto.

    3. Valige väljal **Põhikonto** need põhikontod mida kasutatakse välisvaluuta ümberarvutamise korrigeerimiseks.
    4. Sulgege leht.

    Kui loote konsolideeritud juriidilise isiku perioodi alguses, saate välisvaluuta summad ümber arvutada vastavalt sellele, kuidas vahetuskursid konsolideerimisperioodi jooksul muutuvad.

Konsolideeritud juriidiline isik on nüüd perioodilise töö **Konsolideerimise** jaoks seadistatud. Saate teha kas impordi konsolideerimist või võrgukonsolideerimisi.

- Konsolideerimise importimiseks avage **Pearaamat \> Perioodiline \> Konsolideeri \> Konsolideeri \[Impordi asukohast\]**.
- Veebipõhise konsolideerimise importimiseks avage **Pearaamat \> Perioodiline \> Konsolideeri \> Konsolideeri \[Veebis\]**.

> [!NOTE]
> Enne konsolideerimist valmistage tütarettevõtte juriidilised isikud konsolideerimiseks ette. Lisateavet vt jaotisest [Allettevõte juriidilise isiku konsolideerimiseks seadistamine](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]