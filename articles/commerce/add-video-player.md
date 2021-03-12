---
title: Videopleieri moodul
description: See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 712e9359e31be96c426d6f16c878f18f05cc1bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980103"
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

Järgmisel pildil on näide videopleieri moodulist avalehel.

![Videopleieri mooduli näide](./media/ecommerce-videoplayer.PNG)

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

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Videopleieri mall** ja valige seejärel **OK**.
1. Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.
1. Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Videopleier** ja klõpsake seejärel **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. 
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Vali mall** teie loodud videopleieri mall. Sisestage jaotises **Lehe nimi** väärtus **Videopleieri leht** ja seejärel **OK**.
1. Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Videopleier** ja klõpsake seejärel **OK**.
1. Valige videopleieri mooduli atribuutide paanil **Video lisamine**.
1. Valige dialoogiaknas **Meedia valija** video ja seejärel valige **Laadi üles uus meedium**.
1. Valige File Exploreris videofail ja seejärel **Ava**.
1. Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** pealkiri ja muu vajalik teave ja seejärel valige **OK**.
1. Valige dialoogiboksis **Meedia valija** käsk **Sule**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Peaksite nägema lehel videomoodulit. Saate muuta täiendavaid sätteid mooduli käitumise kohandamiseks.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. 

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Kampaania ribareklaami moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Tekstiploki moodul](add-content-rich-block.md)

[Sisuploki moodul](add-hero-module.md)
