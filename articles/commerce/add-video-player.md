---
title: Videopleieri moodul
description: See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885897"
---
# <a name="video-player-module"></a>Videopleieri moodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Videopleieri mooduleid kasutatakse video taasesituse toetamiseks. Kaupluse alustuskomplektis on kaks videopleieri moodulit: ümbruse videopleieri moodul ja videopleieri moodul. Mõlemad pleierid toetavad meediumitüüpi MP4.

## <a name="ambient-video-player-module"></a>Ümbruse videopleieri moodul

Ümbruse videopleieri moodul toetab lühikesi teavitavaid videoid. Seda tuleks kasutada videote jaoks, mille pikkus on vähem kui viis sekundit. See pleier toetab piiratud video taasesituse võimalusi, nagu esitamine ja paus.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>E-kaubanduse ümbruse videopleieri moodulite näited

- Lühikesed teavitavad videod, mis tõstavad avalehel esile uusi tooteid
- Lühikesed teavitavad videod, mis tõstavad toote üksikasjade lehel esile toote omadused

### <a name="ambient-video-player-module-properties"></a>Ümbruse videopleieri mooduli atribuudid

| Atribuudi nimi     | Väärtus                 | Kirjeldus |
|-------------------|-----------------------|-------------|
| Automaatesitus          | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, esitatakse video automaatselt. |
| Vaigista              | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, on heli vaigistatud. Selle pleieri vaikeväärtus on **Tõene**. Google Chrome’i brauseris on automaatselt esitatavad videod vaikimisi vaigistatud ja heli esitatakse ainult siis, kui kasutaja esitab videot käsitsi. |
| Silmus              | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, korratakse videot tsüklis. |
| Värbamisvahend             |  Videofaili tee ja nimi | Videopleieri esitatav videofail. |
| Esituse juhtelemendid | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, kuvatakse videol esitamise/peatamise nupp. Kui väärtuseks on seatud **Väär**, siis esitamise/peatamise nuppu ei kuvata, kuid kasutajad saavad siiski klaviatuuri abil video peatada ja jätkata. |

## <a name="video-player-module"></a>Videopleieri moodul

Videopleieri moodulit saab kasutada videote esitamiseks e-kaubanduse saidil. See toetab kõiki taasesituse võimalusi, nagu esitamine, peatamine, täissuuruses režiim ja suletud pealdised. Videopleieri moodul toetab ka suletud pealdiste kohandamist, et see vastaks Microsofti juurdepääsu standarditele. Näiteks saate kohandada fondi suurust ja taustavärvi.

Video mängija moodul toetab ka sekundaarseid audio palasid. Kui video on üles laaditud, saab ka teisese heliriba üles laadida. Kui kasutaja valib selle, saab video pleieri moodul esitada teise heliriba.

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
| Esituse juhtelemendid     | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, kuvatakse videol esitamise/peatamise nupp. Kui väärtuseks on seatud **Väär**, siis esitamise/peatamise nuppu ei kuvata, kuid kasutajad saavad siiski klaviatuuri abil video peatada ja jätkata. |
| Täisekraanil esitamine       | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, esitatakse video täisekraanil režiimis. |
| Juhtelemendid              | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, kuvatakse kõik juhtelemendid. Need juhtelemendid hõlmavad esitamise ja peatamise nuppe, edenemise näidikut ja suletud pealdisi. |
| Plakati raami peitmine     | **Tõene** või **Väär**               | Videol võib olla plakati raam. Kui selle atribuudi väärtuseks on seatud **Tõene**, on plakati raam peidetud. |
| Maski tase            | Number vahemikus **0** kuni **100** | Video laadi jaoks rakendatav mask. |
| Täisekraani ikooni laad | **Kandiline** või **Nool**             | Täisekraani ikooni laad, mis kuvatakse videopleieris. |

## <a name="add-a-video-player-module-to-a-page"></a>Videopleieri mooduli lisamine lehele

Uuele lehele videopleieri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge lehe mall nimega **videopleieri mall**.
1. Lisage vaikelehe pessa **Peamine** konteinermoodul.
1. Lisage konteinermoodulis videopleieri ja ümbrise videopleieri moodulid.
1. Registreerige mall ja avaldage see.
1. Kasutage äsja loodud videopleieri malli, et luua leht, mille nimi on **videopleieri leht**.
1. Lisage uue lehe pessa **Peamine** ümbruse videopleieri moodul.
1. Avage ümbruse videopleieri mooduli sätetes suvand **Meedium**ja laadige videofail üles. Saate vastavalt vajadusele muuta suvandeid **Automaatesitus**, **Silmus** ja teisi atribuute.
1. Salvestage ja kuvage lehe eelvaade.
1. Lisage uue lehe pessa **Peamine** videopleieri moodul.
1. Avage videopleieri mooduli sätetes suvand **Meedium**ja laadige videofail üles.
1. Salvestage ja kuvage lehe eelvaade. Peaksite nägema lehel mõlemat videomoodulit. Saate muuta täiendavaid sätteid iga mooduli käitumise kohandamiseks.
1. Registreerige leht ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Teatise moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Sisurikas plokimoodul](add-content-rich-block.md)

[Sisupaigutuse moodul](add-content-placement-modules.md)

[Funktsioonimoodul](add-feature-module.md)

[Pannoomoodul](add-hero-module.md)
