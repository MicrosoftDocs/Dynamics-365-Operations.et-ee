---
title: Ettevõtte mõiste teenuses Common Data Service
description: Selles teemas kirjeldatakse ettevõtte andmete integreerimist rakenduse Finance and Operations ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 20a3f89821af56cb4c3969c89301d4a8a32ab848
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019745"
---
# <a name="company-concept-in-common-data-service"></a>Ettevõtte mõiste teenuses Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Rakenduses Finance and Operations on mõiste *ettevõte* nii juriidiline kui ka ka ärikonstruktsioon. See on ka andmete turvalisuse ja nähtavuse piir. Kasutajad töötavad alati ühe ettevõtte kontekstis ning ettevõte segmendib enamiku andmetest.

Teenuses Common Data Service pole ei ole samaväärset mõistet. Lähim mõiste on *äriüksus*, mis on peamiselt kasutajaandmete turvalisuse ja nähtavuse piir. Sellel mõistel pole sama juriidilist ega ärimõju nagu ettevõtte mõistel.

Kuna äriüksus ja ettevõte ei ole samaväärsed mõisted, ei ole võimalik jõustada üks-ühele (1:1) vastendust nende vahel teenuse Common Data Service integratsiooni eesmärgil. Kuid kuna kasutajad peavad vaikimisi nägema samu kirjeid rakenduses ja teenuses Common Data Service, on Microsoft kasutusele võtnud uue olemi teenuses Common Data Service nimega CDM\_Company. See olem on samaväärne rakenduse olemiga Ettevõte. Selleks, et kirjete nähtavus oleks valmislahendusena rakenduse ja teenuse Common Data Service vahel samaväärne, soovitame teenuse Common Data Service andmete järgmist seadistust.

+ Igale Finance and Operationsi ettevõtte kirjele, millele on topeltkirjutus lubatud, luuakse seotud kirje cdm\_Company.
+ Kui kirje CDM\_Company on loodud ja lubatud kahesuguse kirjutuse jaoks, luuakse samanimeline vaikeäriüksus. Kuigi selle äriüksuse jaoks luuakse automaatselt vaiketöörühm, ei kasutata äriüksust.
+ Luuakse eraldi omaniku töörühm, millel on sama nimi. See on samuti äriüksusega seostatud.
+ Mistahes kirje omanik, mis on loodud ja kahesuguselt kirjutatud teenusesse Common Data Service, on vaikimisi määratud väärtuseks „DW omanikust töörühm, mis on lingitud seostatud äriüksusega.

Järgmisel joonisel on näide seda tüüpi andmete seadistamise kohta teenuses Common Data Service.

![Andmete seadistus teenuses Common Data Service](media/dual-write-company-1.png)

Selle konfiguratsiooni tõttu kuulub kõigi USMF-i ettevõttega seotud kirje töörühmale, mis on seotud USMF-i äriüksusega teenuses Common Data Service. Seetõttu saab iga kasutaja, kellel on juurdepääs sellele äriüksusele turberolli kaudu, mis on määratud äriüksuse tasemel nähtavusele, nüüd näha neid kirjeid. Järgnev näide näitab, kuidas töörühmi saab kasutada neile kirjetele õige juurdepääsu pakkumiseks.

+ Roll "Müügihaldur" on määratud "USMF müük" töörühma liikmetele.
+ Kasutajad, kellel on roll „Müügihaldur", pääsevad juurde mistahes kontokirjetele, mis on sama äriüksuse liikmed.
+ Töörühm "USMF müük" on seotud varem mainitud USMF-i äriüksusega.
+ Seetõttu saavad töörühma "USMF Sales" liikmed vaadata mistahes kontot, mis kuulub "USMF DW" kasutajale, mis oleks tulnud olemist USMF ettevõtte rakenduses Finance and Operations.

![Töörühmade kasutamine](media/dual-write-company-2.png)

Vastavalt eespool toodud joonisele, on see 1:1 vastendamine äriüksuse, ettevõtte ja töörühma vahel vaid alguspunkt. Selles näites luuakse teenuses Common Data Service uus "Euroopa" äriüksus käsitsi ülataseme üksusena nii DEMF-i kui ka ESMF-i jaoks. See uus juuräriüksus pole kahesuguse kirjutamisega seotud. Siiski saab seda kasutada "EUR Sales" töörühmale juurdepääsu andmiseks kontoandmetele nii DEMF-is kui ka ESMF-is, määrates seostatud turberollis andmete nähtavuseks **Ülataseme/alataseme äriüksus**.

Viimaseks aruteluteemaks on, kuidas kahesugune kirjutamine määrab, millisele omanikust töörühmale tuleks kirjed määrata. Seda käitumist juhib väli **Omanikust vaiketöörühm** kirjes CDM\_Company. Kui cdm\_Company kirje on kahesuguseks kirjutamiseks lubatud, loob lisandmoodul automaatselt seostatud äriüksuse ja omaniktöörühma (kui seda veel pole) ja seadistab välja **Omanikust vaiketöörühm**. Administraator saab seda välja muuta muuks väärtuseks. Kuid administraator ei saa tühjendada välja seni, kuni olem on lubatud kahesuguseks kirjutamiseks.

> [!div class="mx-imgBorder"]
![Omanikust vaiketöörühma väli](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Ettevõtte segmentimine ja eellaadimine

Teenuse Common Data Service integreerimine toob kaasa ettevõtte paarsuse, kasutades ettevõtte identifikaatorit andmete segmentimiseks. Järgmine illustratsioon näitab, et kõik ettevõttekohased olemid laiendatakse nii, et neil on mitu-ühele (N:1) seos olemiga CDM\_Company.

> [!div class="mx-imgBorder"]
![N:1 seos ettevõttekohase olemi ja olemi cdm_Company vahel](media/dual-write-bootstrapping.png)

+ Kirjete puhul muutub väärtus pärast ettevõtte lisamist ja salvestamist kirjutuskaitstuks. Seetõttu peaksid kasutajad veenduma, et nad valivad õige ettevõtte.
+ Ainult kirjed, millel on ettevõtte andmed on kahesuguse kirjutamise õigused rakenduse ja teenuse Common Data Service vahel.
+ Teenuse Common Data Service olemasolevate andmete puhul on peagi saadaval administraatori juhitav eellaadimine.
