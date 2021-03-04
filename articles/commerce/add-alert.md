---
title: Reklaambänneri moodul
description: See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d9debd16b18300d090bde1862a16920d8e9185eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411589"
---
# <a name="promo-banner-module"></a>Reklaambänneri moodul

[!include [banner](includes/banner.md)]

See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Reklaambänneri mooduleid kasutatakse lehel sisemiste teabesõnumite kuvamiseks. Neid saab kasutada kõikidel e-kaubanduse saidi lehtedel ilmuvate saidiüleste kampaaniate kuvamiseks. 

Reklaambännerid toetavad tekstsõnumit ja linki. Kui reklaambänneri moodulile on lisatud mitu teadet, muutub see pöörlevaks karussell-bänneriks, mis võimaldab klientidel vaadata läbi kõik sõnumid. 

Reklaambänneri moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Reklaambännerite kasutamise näited e-kaubanduses

Reklaambännereid saab kasutada saidi päises, et näidata kogu saiti hõlmavaid kampaaniaid või teateid, nagu näiteks järgmistes näidetes.

„Iga-aastane allahindlus lõppeb 10 päeva pärast”

„Suured allahindlused tagasi kooli kampaania ajal. Ostke kohe.”

„Ostle ja naudi tänupühade KAMPAANIAT!“ 

Järgmisel pildil on toodud reklaambänneri näide.

![Reklaambänneri mooduli näide](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Reklaambänneri mooduli atribuudid

| Atribuudi nimi             | Väärtus                              | Kirjeldus |
|---------------------------|------------------------------------|-------------|
| Bänneri teated           | Tekst ja lingid                     | Valik tekste ja linke. |
| Automaatesitus                  | **Tõene** või **Väär**              | Väärtus, mis näitab, kas juhul kui konfigureeritud on mitu sõnumit, keritakse sõnumid automaatselt läbi. |
| Slaidi ülemineku intervall | Millisekundite arv (ms)      | Sõnumite läbimiseks kasutatav intervall. |
| Luba sulgemine             | **Tõene** või **Väär**              | Kui väärtuseks on seatud olekusse **Tõene**, saavad kliendid teatise hüljata. |
| Näita karusselli keerajat     | **Tõene** või **Väär**              | Väärtus, mis näitab, kas karusselli keerajaid tuleb kuvada, et kliendid saaksid käsitsi liikuda mitme bänneri vahel. |
| Teksti joondus            | **Paremal**, **Vasakul** või **Keskel** | Teksti joondamine reklaambänneri moodulis. |
| Seos                      | URL                              | Valikulise lingi URL. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Reklaambänneri mooduli lehele lisamine 

Lehele reklaambänneri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Reklaambänneri mall** ja valige seejärel **OK**.
1. Lisage jaotisse **Lehe liigendus** moodul **Vaikeleht** pesasse **Kehatekst**. 
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. 
1. Kasutage äsja loodud teatise malli, et luua leht, mille nimi on **Reklaambänneri leht**. 
1. Lisage uue lehe pessa **Peamine** konteinermoodul. 
1. Seadistage paremal paanil väärtus **Laius** olekusse **Täida konteiner**.
1. Lisage jaotises **Lehe liigendus** konteineri moodulile reklaambänneri moodul.
1. Lisage bänneri mooduli sätetes üks või mitu bänneri sõnumit. Igas sõnumis võib olla tekst koos lingiga. Et moodulit veelgi kohandada, võite redigeerida teisi atribuute.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Lehe ülaosas peaksite nägema teatist teie lisatud tekstiga.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

> [!NOTE]
> Reklaambännerit kasutatakse tavaliselt lehekülje päise pesas või alapealkirja pesas.


## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Karusellmoodul](add-carousel.md)

[Tekstiploki moodul](add-content-rich-block.md)

[Sisuploki moodul](add-hero-module.md)

[Videopleierimoodul](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]