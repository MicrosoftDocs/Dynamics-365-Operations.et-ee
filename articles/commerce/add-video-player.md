---
title: Videopleierimoodul
description: See artikkel katab video playeri moodulid ja kirjeldab, kuidas lisada neid saidile Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 919446981f7439d61b01deb57b206cd457eed919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269290"
---
# <a name="video-player-module"></a>Videopleierimoodul

[!include [banner](includes/banner.md)]

See artikkel katab video playeri moodulid ja kirjeldab, kuidas lisada neid saidile Microsoft Dynamics 365 Commerce.

Videopleieri moodulit kasutatakse video taasesituse toetamiseks. Seda saab lisada igale leheküljele, kui video sisu on üles laaditud ja sisuhaldussüsteemis (CMS) saadaval. Videopleieri moodul toetab .mp4 meediatüüpi.

## <a name="video-player-module"></a>Videopleierimoodul

Videopleieri moodulit saab kasutada videote esitamiseks e-kaubanduse saidil. See toetab kõiki taasesituse võimalusi, nagu esitamine, peatamine, täissuuruses režiim, helikirjeldused ja suletud pealdised. Videopleieri moodul toetab ka suletud pealdiste kohandamist, et see vastaks Microsofti juurdepääsu standarditele. Näiteks saate kohandada fondi suurust ja taustavärvi.

Video mängija moodul toetab ka sekundaarseid audio palasid. Kui video on CMS-i üles laaditud, saab ka teisese heliriba üles laadida. Kui kasutaja valib selle, saab video pleieri moodul esitada teise heliriba.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>E-kaubanduse videopleieri moodulite näited

- Juhiste videod toote üksikasjade lehtedel või turunduse lehtedel
- Kampaaniavideod või videod eeskirjade kohta mis tahes turunduse lehel
- Turundusvideod, mis tõstavad toote üksikasjade lehtedel või turunduse lehtedel esile toote omadused

Järgmisel pildil on näide videopleieri moodulist avalehel.

![Videopleieri mooduli näide.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Videopleieri mooduli atribuudid

| Atribuudi nimi         | Väärtus                               | Kirjeldus |
|-----------------------|-------------------------------------|-------------|
| Päis               | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Vaikimisi kasutatakse **H2** pealkirja silti päises, kuid pealkirja silti saab vajadusel muuta juurdepääsu nõuetele vastavaks. |
| Rikastekst             | Lõigu tekst | Moodul toetab RTF-vormingus lõigu teksti. Toetatud on mõned põhilised RTF-i võimalused, nagu hüperlingid ja paks, allajoonitud, ning kursiivis tekst. Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile. |
| Seos                  | Lingi tekst, lingi URL, Accessible Rich Internet Applications (ARIA) silt ja suvand **Ava link uuel vahekaardil** valija | Moodulid toetavad üht või mitut tegutsemiskutse linki. Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt. ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele. Linke saab konfigureerida nii, et need avatakse uuel vahekaardil. |
| Alamtekst              | Pealkiri, tekst ja lingid | Videopleierile saate lisada täiendavat sisu nagu nt autori või kujundaja nime või lingid isiklikele ajaveebidele. |
| Automaatesitus             | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, esitatakse video automaatselt. |
| Vaigista                  | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, on heli vaigistatud. Selle pleieri vaikeväärtus on **Väär**. Chrome’i brauseris on automaatselt esitatavad videod vaikimisi vaigistatud ja heli esitatakse ainult siis, kui kasutaja esitab videot käsitsi. |
| Silmus                  | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, korratakse videot tsüklis. |
| Värbamisvahend                 | Videofaili tee ja nimi | Videopleieris esitatav videofail. |
| Täisekraanil esitamine       | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, esitatakse video täisekraanil režiimis. |
| Lüliti Esita/Peata    | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, kuvatakse videol esitamise/peatamise nupp. |
| Videopleieri juhtelemendid | **Tõene** või **Väär**               | Kui väärtuseks on seatud **Tõene**, kuvatakse kõik vidopleieri juhtelemendid. Need juhtelemendid hõlmavad esitamise ja peatamise nuppe, edenemise näidikut ja suletud pealdise suvandeid. |
| Peida plakati pilt     | **Tõene** või **Väär**               | Videol võib olla plakati raam. Kui selle atribuudi väärtuseks on seatud **Tõene**, on plakati raam peidetud. |
| Maski tase            | Number vahemikus **0** kuni **100** | Video laadi jaoks rakendatav mask. |

> [!IMPORTANT]
> **Pealkirja**, **RTF-teksti**, **Lingi**, ja **Alamteksti** atribuudid on saadaval alates versiooni Dynamics 365 Commerce 10.0.20 väljalaskest.

## <a name="add-a-video-player-module-to-a-page"></a>Videopleieri mooduli lisamine lehele

> [!NOTE] 
> Enne kui loote videopleieri mooduli, peate esmalt video meediateeki üles laadima.

Uuele lehele videopleieri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Dialoogiboksis Uus **mall** sisestage malli nime **all** **Video Playeri mall** ja seejärel valige **OK**.
1. Kehapesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige vaikelehemoodul **ja** seejärel valige **OK**.
1. Vaikelehe mooduli põhipesas **valige** kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Valige konteineri pesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige **Video Player ja** seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. 
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Sisestage **dialoogiboksi Uue lehe loomine** jaotises Lehe nimi **, sisestage** Video **playeri leht** ja seejärel valige **edasi**.
1. Valige **valiku Vali mall** all **loodud Video Playeri** mall ja seejärel valige **edasi**.
1. Valige **valiku Vali paigutus** all lehekülje paigutus (nt Paindlik **paigutus**) ja seejärel klõpsake nuppu **Edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui teil on vaja lehekülje teavet redigeerida, valige **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**.
1. Uue lehekülje põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Valige konteineri pesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige **Video Player ja** seejärel valige **OK**.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
