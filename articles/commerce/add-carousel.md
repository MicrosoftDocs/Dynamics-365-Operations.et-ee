---
title: Karusellmoodul
description: See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785233"
---
# <a name="carousel-module"></a>Karusellmoodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Karussellmoodulit kasutatakse mitme kampaaniakauba lisamiseks karuselli, mida kliendid saavad sirvida. See on spetsiaalne konteinermoodul, mis majutab teisi mooduleid. Näiteks saab jaemüüja kasutada avalehel karussellmoodulit, et tutvustada mitut uut toodet või kampaaniat.

Saate lisada karusellmooduli sisse pannoo- ja funktsioonimoodulid. Karussellmooduli atribuudid määratlevad seejärel, kuidas neid mooduleid renderdatakse.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>E-kaubanduse karusellmoodulite näited

- Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada kodulehel.
- Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada toote üksikasjade lehel.
- Karusselli saab kasutada mis tahes turunduse lehel, et reklaamida mitut kampaaniat või toodet.

## <a name="carousel-module-properties"></a>Karusellmooduli atribuudid

| Atribuudi nimi             | Väärtus                                | Kirjeldus |
|---------------------------|--------------------------------------|-------------|
| Automaatesitus                  | **Tõene** või **Väär**                | Kui väärtuseks on seatud **Tõene**, toimub karuselli sees üleminek kaupade vahel automaatselt. Kui väärtuseks on seatud **Väär**, siis üleminekut ei toimu, kui klient ei kasuta klaviatuuri või hiirt, et liikuda ühelt kaubalt järgmisele kaubale. |
| Slaidi ülemineku intervall | Väärtus sekundites                   | Kaupade vahel üleminekute intervall. |
| Ülemineku animatsioon      | **Libisemine** või **Hajumine**                | Ülemineku efekt. |
| Laius                     | **Mahuta konteinerisse** või **Täida ekraan** | Kui väärtuseks on seatud **Mahuta konteinerisse**, on karussellis olevad kaubad piiratud karusselli laiusega. Kui väärtuseks on seatud **Täida ekraan**, ei ole kaubad karusselli laiusega piiratud, vaid võivad minna täisekraani režiimi. Soovitud paigutuse saavutamiseks saate väärtust muuta. |

## <a name="add-a-carousel-module-to-a-page"></a>Lehele karusellmooduli lisamine

Uuele lehele karusellmooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge lehe mall nimega **karuselli mall**.
1. Lisage vaikelehe pessa **Peamine** karusellmoodul.
1. Lisage karusellmoodulile pannoomoodul.
1. Lisage karusellmoodulile funktsioonimoodul.
1. Registreerige mall ja avaldage see. 
1. Kasutage äsja loodud karuselli malli, et luua leht, mille nimi on **karuselli leht**.
1. Lisage uue lehe pessa **Peamine** karusellmoodul.
1. Määrake karusellmooduli atribuut **Laius** väärtusele **Täida ekraan**. 
1. Määrake atribuut **Ülemineku animatsioon** väärtusele **Libisemine**.
1. Lisage karusellmoodulile pannoomoodul.
1. Pannoomoodulis lisage pilt ja pealkiri ning valige seejärel **Salvesta**.
1. Lisage karusellmoodulile funktsioonimoodul.
1. Funktsioonimoodulis lisage pilt, pealkiri ja tekstilõik.
1. Salvestage ja kuvage lehe eelvaade. Lehekülg peaks näitama karusselli, mille sees on kaks moodulit (pannoomoodul ja funktsioonimoodul). Võite soovitud efekti saavutamiseks muuta karusell-, pannoo- ja funktsioonimoodulite täiendavaid atribuute.
1. Registreerige leht ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Teatise moodul](add-alert.md)

[Sisurikas plokimoodul](add-content-rich-block.md)

[Sisupaigutuse moodul](add-content-placement-modules.md)

[Funktsioonimoodul](add-feature-module.md)

[Pannoomoodul](add-hero-module.md)

[Videopleieri moodul](add-video-player.md)
