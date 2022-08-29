---
title: Kampaania ribareklaami moodul
description: See artikkel katab kampaania mooduleid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: fbde146923d1448e382cbf2458880f7e300f605c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279731"
---
# <a name="promo-banner-module"></a>Kampaania ribareklaami moodul

[!include [banner](includes/banner.md)]

See artikkel katab kampaania mooduleid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce

Reklaambänneri mooduleid kasutatakse lehel sisemiste teabesõnumite kuvamiseks. Neid saab kasutada kõikidel e-kaubanduse saidi lehtedel ilmuvate saidiüleste kampaaniate kuvamiseks. 

Reklaambännerid toetavad tekstsõnumit ja linki. Kui reklaambänneri moodulile on lisatud mitu teadet, muutub see pöörlevaks karussell-bänneriks, mis võimaldab klientidel vaadata läbi kõik sõnumid. 

Reklaambänneri moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Reklaambännerite kasutamise näited e-kaubanduses

Reklaambännereid saab kasutada saidi päises, et näidata kogu saiti hõlmavaid kampaaniaid või teateid, nagu näiteks järgmistes näidetes.

„Iga-aastane allahindlus lõppeb 10 päeva pärast”

„Suured allahindlused tagasi kooli kampaania ajal. Ostke kohe.”

„Ostle ja naudi tänupühade KAMPAANIAT!“ 

Järgmisel pildil on toodud reklaambänneri näide.

![Reklaambänneri mooduli näide.](./media/ecommerce-Promobanner.PNG)

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
|Teksti joondamine             | **Paremal**, **Vasakul** või **Keskel** | See atribuut on saadaval teema laiendina Adventure Worksi teemas. See võimaldab kasutajal määrata teksti joonduse reklaamibänneris. |

> [!IMPORTANT]
> Adventure Works teema on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20.

## <a name="add-a-promo-banner-module-to-a-page"></a>Reklaambänneri mooduli lehele lisamine 

Lehele reklaambänneri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Dialoogiaknas **Uus** mall jaotises Malli nimi **sisestage** **Kampaania malli ja** seejärel valige **OK**.
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
