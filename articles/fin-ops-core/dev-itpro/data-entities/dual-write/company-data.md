---
title: Ettevõtte kontseptsioon Dataverse'is
description: See artikkel kirjeldab ettevõtete andmete integreerimist finantside ja toimingute ning ettevõtete vahel Dataverse.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: ad0075e2b92ebeb9fba879bcae503100dc7adb47
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205932"
---
# <a name="company-concept-in-dataverse"></a>Ettevõtte kontseptsioon Dataverse'is

[!include [banner](../../includes/banner.md)]




Finantside ja operatsioonide puhul on ettevõtte mõiste *nii* juriidiline konstrukt kui ka ettevõtte konstrukt. See on ka andmete turvalisuse ja nähtavuse piir. Kasutajad töötavad alati ühe ettevõtte kontekstis ning ettevõte segmendib enamiku andmetest.

Teenuses Dataverse pole ei ole samaväärset mõistet. Lähim mõiste on *äriüksus*, mis on peamiselt kasutajaandmete turvalisuse ja nähtavuse piir. Sellel mõistel pole sama juriidilist ega ärimõju nagu ettevõtte mõistel.

Kuna äriüksus ja ettevõte ei ole samaväärsed mõisted, ei ole võimalik jõustada üks-ühele (1:1) vastendust nende vahel teenuse Dataverse integratsiooni eesmärgil. Kuid kuna kasutajad peavad vaikimisi nägema samu ridu rakenduses ja teenuses Dataverse, on Microsoft võtnud teenuses Dataverse kasutusele uue tabeli nimega CDM\_Company. See tabel on samaväärne rakenduse tabeliga Ettevõte. Selleks, et ridade nähtavus oleks valmislahendusena rakenduse ja teenuse Dataverse vahel samaväärne, soovitame teenuse Dataverse andmete järgmist seadistust.

+ Iga finantsi ja operatsioonide ettevõtterea jaoks, mis on lubatud topeltkirjutuse jaoks, luuakse seotud rida cdm\_ Company.

+ Kui rida CDM\_Company on loodud ja lubatud kahesuguse kirjutuse jaoks, luuakse samanimeline vaikeäriüksus. Kuigi selle äriüksuse jaoks luuakse automaatselt omaniku vaikemeeskond, äriüksust ei kasutata.
+ Luuakse eraldi omaniku meeskond, kellel on sama nimi topeltkirjutuse järelliidetega. See on samuti äriüksusega seostatud.

+ Mistahes rea omanik, mis on loodud ja kahesuguselt kirjutatud teenusesse Dataverse, on vaikimisi määratud väärtuseks „DW omanikust töörühm, mis on lingitud seostatud äriüksusega.

Järgmisel joonisel on näide seda tüüpi andmete seadistamise kohta teenuses Dataverse.

![Andmete seadistus teenuses Dataverse.](media/dual-write-company-1.png)

Selle konfiguratsiooni tõttu kuulub kõigi USMF-i ettevõttega seotud rea töörühmale, mis on seotud USMF-i äriüksusega teenuses Dataverse. Seetõttu saab iga kasutaja, kellel on juurdepääs sellele äriüksusele turberolli kaudu, mis on määratud äriüksuse tasemel nähtavusele, nüüd näha neid ridu. Järgnev näide näitab, kuidas töörühmi saab kasutada neile ridadele õige juurdepääsu pakkumiseks.

+ Roll "Müügihaldur" on määratud "USMF müük" töörühma liikmetele.
+ Kasutajad, kellel on roll „Müügihaldur", pääsevad juurde mistahes kontoridadele, mis on sama äriüksuse liikmed.
+ Töörühm "USMF müük" on seotud varem mainitud USMF-i äriüksusega.
+ Seetõttu saavad USMF-i müügimeeskonna liikmed näha mis tahes kontot, mis kuulub kasutajale "USMF DW", mis oleks pärit finantside ja toimingute tabelist USMF Company.

![Töörühmade kasutamine.](media/dual-write-company-2.png)

Vastavalt eespool toodud joonisele, on see 1:1 vastendamine äriüksuse, ettevõtte ja töörühma vahel vaid alguspunkt. Selles näites luuakse teenuses Dataverse uus "Euroopa" äriüksus käsitsi ülataseme üksusena nii DEMF-i kui ka ESMF-i jaoks. See uus juuräriüksus pole kahesuguse kirjutamisega seotud. Siiski saab seda kasutada "EUR Sales" töörühmale juurdepääsu andmiseks kontoandmetele nii DEMF-is kui ka ESMF-is, määrates seostatud turberollis andmete nähtavuseks **Ülataseme/alataseme äriüksus**.

Lõpp-artikkel, mida arutleda, on see, kui topeltkirjutusega määrab, millisele omaniku töörühmale peaks ridu määrama. Seda käitumist juhib veerg **Omanikust vaiketöörühm** real CDM\_Company. Kui rida cdm\_Company on kahesuguseks kirjutamiseks lubatud, loob lisandmoodul automaatselt seostatud äriüksuse ja omaniktöörühma (kui seda veel pole) ja seadistab veeru **Omanikust vaiketöörühm**. Administraator saab selle veeru muuta muuks väärtuseks. Kuid administraator ei saa tühjendada veergu seni, kuni tabel on lubatud kahesuguseks kirjutamiseks.

> [!div class="mx-imgBorder"]
![Omanikust vaiketöörühma veerg.](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Ettevõtte segmentimine ja eellaadimine

Teenuse Dataverse integreerimine toob kaasa ettevõtte paarsuse, kasutades ettevõtte identifikaatorit andmete segmentimiseks. Järgmine illustratsioon näitab, et kõik ettevõttekohased tabelid laiendatakse nii, et neil onleks mitu-ühele (N : 1) seos tabeliga CDM\_Company.

> [!div class="mx-imgBorder"]
![Seos N:1 ettevõttekohase tabeli ja tabeli cdm_Company vahel.](media/dual-write-bootstrapping.png)

+ Ridade puhul muutub väärtus pärast ettevõtte lisamist ja salvestamist kirjutuskaitstuks. Seetõttu peaksid kasutajad veenduma, et nad valivad õige ettevõtte.
+ Ainult read, millel on ettevõtte andmed on kahesuguse kirjutamise õigused rakenduse ja teenuse Dataverse vahel.
+ Teenuse Dataverse olemasolevate andmete puhul on peagi saadaval administraatori juhitav eellaadimine.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Ettevõtte nime automaatne asustamine klientide kaasamise rakendustes

Ettevõtte nime automaatseks asustamiseks klientide kaasamise rakendustes on mitu võimalust.

+ Kui olete süsteemiadministraator, saate määrata vaikeettevõtte , kui valite **Täpsemad sätted > Süsteem > Turve > Kasutajad**. Avage vorm **Kasutaja** ja määrake jaotises **Organisatsiooni andmed** väärtus **Ettevõtte vaikesätteks vormidel**.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Vaikeettevõtte seadmine organisatsiooni andmete jaotises.":::

+ Kui teil on tasemel **Äriüksus** **Kirjutuspääs** tabelile **Süsteemikasutaja**, saate vaikeettevõtet muuta mistahes vormil, kui valite ettevõtte rippmenüüst **Ettevõte**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Ettevõtte nime muutmine uuel kontol.":::

+ Kui teil on **Kirjutuspääs** rohkem kui ühe ettevõtte andmetele, saate vaikeettevõtet muuta, kui valite rea, mis kuulub muule ettevõttele.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Rea valimine muudab vaikeettevõtet.":::

+ Kui olete süsteemikonfigureerija või -administraator, ja soovite kohandatud vormil automaatselt ettevõtte andmeid asustada, saate kasutada [vormisündmusi](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Lisage JavaScripti viide failile **msdyn_/DefaultCompany.js** ja kasutage järgmisi sündmusi. Saate kasutada valmisvormi, näiteks vormi **Konto**.

    + Vormi sündmus **OnLoad**: määrake veerg **defaultCompany**.
    + Veeru **Ettevõte** sündmus **OnChange**: määrake veerg **updateDefaultCompany**.

## <a name="apply-filtering-based-on-the-company-context"></a>Filtreerimise rakendamine ettevõtte konteksti põhjal

Filtreerimise rakendamiseks ettevõtte konteksti põhjal kohandatud vormidele või standardvormidele lisatud otsinguveergudele avage vorm ja kasutage ettevõtte filtri rakendamiseks jaotist **Seotud kirjete filtreerimine**. Selle peate määrama igale otsinguveerule, mis antud real nõuab filtreerimist aluseksoleva ettevõtte põhjal. Säte kuvatakse järgmisel joonisel suvandi **Konto** jaoks.

:::image type="content" source="media/apply-company-context.png" alt-text="Ettevõtte konteksti rakendamine.":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
