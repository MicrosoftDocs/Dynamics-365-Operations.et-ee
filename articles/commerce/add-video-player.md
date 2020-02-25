---
title: Videopleieri moodul
description: See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025640"
---
# <a name="video-player-module"></a>Videopleieri moodul


[!include [banner](includes/banner.md)]

See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Videopleieri moodulit kasutatakse video taasesituse toetamiseks. Seda saab lisada igale leheküljele, kui video sisu on üles laaditud ja sisuhaldussüsteemis (CMS) saadaval. Videopleieri moodul toetab .mp4 meediatüüpi.

## <a name="video-player-module"></a>Videopleierimoodul

Videopleieri moodulit saab kasutada videote esitamiseks e-kaubanduse saidil. See toetab kõiki taasesituse võimalusi, nagu esitamine, peatamine, täissuuruses režiim, helikirjeldused ja suletud pealdised. Videopleieri moodul toetab ka suletud pealdiste kohandamist, et see vastaks Microsofti juurdepääsu standarditele. Näiteks saate kohandada fondi suurust ja taustavärvi.

Video mängija moodul toetab ka sekundaarseid audio palasid. Kui video on CMS-i üles laaditud, saab ka teisese heliriba üles laadida. Kui kasutaja valib selle, saab video pleieri moodul esitada teise heliriba.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>E-kaubanduse videopleieri moodulite näited

- Juhiste videod toote üksikasjade lehtedel või turunduse lehtedel
- Kampaaniavideod või videod eeskirjade kohta mis tahes turunduse lehel
- Turundusvideod, mis tõstavad toote üksikasjade lehtedel või turunduse lehtedel esile toote omadused

### <a name="video-player-module-properties"></a>Videopleieri mooduli atribuudid

| Atribuudi nimi         | Väärtus                               | Kirjeldus |
|-----------------------|-------------------------------------|-------------|
| Automaatesitus             | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, esitatakse video automaatselt. |
| Vaigista                  | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, on heli vaigistatud. Selle pleieri vaikeväärtus on **Väär**. Chrome’i brauseris on automaatselt esitatavad videod vaikimisi vaigistatud ja heli esitatakse ainult siis, kui kasutaja esitab videot käsitsi. |
| Silmus                  | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, korratakse videot tsüklis. |
| Värbamisvahend                 | Videofaili tee ja nimi | Videopleieris esitatav videofail. |
| Täisekraanil esitamine       | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, esitatakse video täisekraanil režiimis. |
| Lüliti Esita/Peata    | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, kuvatakse videol esitamise/peatamise nupp. |
| Videopleieri juhtelemendid | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, kuvatakse kõik vidopleieri juhtelemendid. Need juhtelemendid hõlmavad esitamise ja peatamise nuppe, edenemise näidikut ja suletud pealdise suvandeid. |
| Peida plakati pilt     | **Tõene** või **Väär**               | Videol võib olla plakati raam. Kui selle atribuudi väärtuseks on seatud **Tõene**, on plakati raam peidetud. |
| Maski tase            | Number vahemikus **0** kuni **100** | Video laadi jaoks rakendatav mask. |

## <a name="add-a-video-player-module-to-a-page"></a>Videopleieri mooduli lisamine lehele

> [!NOTE] 
> Enne kui loote videopleieri mooduli, peate esmalt video meediateeki üles laadima.

Uuele lehele videopleieri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge lehe mall nimega **videopleieri mall**.
1. Lisage vaikelehe pessa **Peamine** konteinermoodul.
1. Lisage konteinermoodulis videopleieri ja ümbrise videopleieri moodulid.
1. Viige lõpuni malli redigeerimine ja avaldage see.
1. Kasutage äsja loodud videopleieri malli, et luua leht, mille nimi on **videopleieri leht**.
1. Lisage uue lehe pessa **Peamine** videopleieri moodul.
1. Valige videopleieri mooduli paanil atribuudid **Video lisamine**.
1. Valige dialoogiaknas **Meedia valija** video ja seejärel valige **Laadi üles uus meedium**.
1. Salvestage ja kuvage lehe eelvaade. Peaksite nägema lehel videomoodulit. Saate muuta täiendavaid sätteid mooduli käitumise kohandamiseks.
1. Viige lõpuni lehe redigeerimine ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Reklaambänneri moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Tekstiploki moodul](add-content-rich-block.md)

[Sisuploki moodul](add-hero-module.md)
