---
title: Karusellmoodul
description: See artikkel katab lehtmoodulid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 8bf9f7294dfbb4e16814dbdfb27bf646fcb5f4b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275823"
---
# <a name="carousel-module"></a>Karusellmoodul

[!include [banner](includes/banner.md)]

See artikkel katab lehtmoodulid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Karussellmoodulit kasutatakse mitme kampaaniakauba (sealhulgas rikastatud piltide) lisamiseks pöörlevale karussellibännerile, mida kliendid saavad sirvida. Näiteks saab jaemüüja kasutada avalehel karussellmoodulit, et tutvustada mitut uut toodet või kampaaniat.

Saate lisada karusellmooduli sisse sisuploki. Karussellmooduli atribuudid määratlevad seejärel, kuidas neid mooduleid renderdatakse.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>E-kaubanduse karusellmoodulite näited

- Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada kodulehel.
- Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada toote üksikasjade lehel.
- Karusselli saab kasutada mis tahes turunduse lehel, et reklaamida mitut kampaaniat või toodet.

Järgmisel pildil on näide karussellmoodulist, mida kasutatakse avalehel. Karussellmoodul sisaldab mitmeid sisu blokeerimise üksuseid.

![Karussellmooduli näide.](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Karusellmooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Automaatesitus                  | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, toimub karuselli sees üleminek kaupade vahel automaatselt. Kui väärtuseks on seatud **Väär**, siis üleminekut ei toimu, kui klient ei kasuta klaviatuuri või hiirt, et liikuda ühelt kaubalt järgmisele kaubale. |
| Slaidi ülemineku intervall | Väärtus sekundites    | Kaupade vahel üleminekute intervall. |
| Siirde tüüp           | **Libisemine** või **Hajumine** | Ülemineku efekt elementide vahel. |
| Peida karusselli pöördur     | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, on karusselli keeraja ja indikaator peidetud. |
| Luba karusselli hülgamine    | **Tõene** või **Väär** | Kui väärtuseks on seatud **Tõene**, saavad kliendid ise karusselli hüljata. |

## <a name="add-a-carousel-module-to-a-page"></a>Lehele karusellmooduli lisamine

Uuele lehele karusellmooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Karusselli mall** ja valige seejärel **OK**.
1. Lisage pesasse **Kehatekst** moodul **Vaikeleht**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.  
1. Kasutage äsja loodud karuselli malli, et luua leht, mille nimi on **Karuselli leht**.
1. Lisage uue lehe pessa **Peamine** konteinermoodul. 
1. Seadistage paremal paanil väärtus **Laius** olekusse **Täida ekraan**.
1. Lisage jaotises **Lehe liigendus** konteineri moodulile karusselli moodul.
1. Lisage karusselli moodulile sisuploki moodul. Seadistage sisuploki mooduli atribuudid, täites atribuudid **Pealkiri**, **Link**, **Paigutus** ja muud.
1. Lisage ja konfigureerige teine sisuploki moodul.
1. Seadistage vajadusel karusselli moodulile täiendavaid atribuute.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Lehekülg peaks näitama karusselli, mille sees on kaks moodulit (pannoomoodul ja funktsioonimoodul). Võite soovitud efekti saavutamiseks muuta karusell-, pannoo- ja funktsioonimoodulite täiendavaid atribuute.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Kampaania ribareklaami moodul](add-alert.md)

[Tekstiploki moodul](add-content-rich-block.md)

[Sisuploki moodul](add-hero-module.md)

[Videopleierimoodul](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
