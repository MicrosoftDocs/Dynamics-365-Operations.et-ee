---
title: Teatise moodul
description: See teema hõlmab teatise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785348"
---
# <a name="alert-module"></a>Teatise moodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab teatise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Teatise moodulit kasutatakse lehel olevate sisemiste teabesõnumite kuvamiseks. Teatise moodulid toetavad tekstsõnumit ja linki. Neid saab kasutada kõikidel e-kaubanduse saidi lehtedel ilmuvate saidiüleste kampaaniate kuvamiseks. 

Teatise moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.

## <a name="examples-of-alert-modules-in-e-commerce"></a>E-kaubanduse teatise moodulite näited

Teatise mooduleid saab kasutada saidi päises, et näidata saidiüleseid kampaaniaid või sõnumeid. Järgmisena on toodud mõned näited.

„Iga-aastane allahindlus lõppeb 10 päeva pärast”

„Suured allahindlused tagasi kooli kampaania ajal. Ostke kohe.”

## <a name="alert-module-properties"></a>Teatise mooduli atribuudid

| Atribuudi nimi  | Väärtus                              | Kirjeldus |
|----------------|------------------------------------|-------------|
| Tekst           | Tekst                               | Teatise moodulis ilmuv tekstsõnum. |
| Teksti joondus | **Paremal**, **Vasakul** või **Keskel** | Väärtus, mis määratleb, kuidas tekst on teatise moodulis joondatud. |
| Unusta teatis  | **Tõene** või **Väär**              | Kui väärtuseks on seatud **Tõene**, Saab klient teatise lõpetada. |
| Seos           | URL                                | Valikulise lingi URL. |

## <a name="add-an-alert-module-to-a-page"></a>Lehele teatise mooduli lisamine 

Lehele teatise mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge lehe mall nimega **teatise mall**.
1. Lisage vaikelehe pessa **Peamine** teatise moodul.
1. Registreerige mall ja avaldage see. 
1. Kasutage äsja loodud teatise malli, et luua leht, mille nimi on **teatise leht**. 
1. Lisage uue lehe pessa **Peamine** teatise moodul.
1. Sisestage teatise mooduli sätetes teatise tekst. Kui soovite teatise moodulit veelgi kohandada, võite redigeerida teisi atribuute.
1. Salvestage ja kuvage lehe eelvaade. Lehe ülaosas peaksite nägema teatist teie lisatud tekstiga.
1. Registreerige leht ja avaldage see. 

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Karusellmoodul](add-carousel.md)

[Sisurikas plokimoodul](add-content-rich-block.md)

[Sisupaigutuse moodul](add-content-placement-modules.md)

[Funktsioonimoodul](add-feature-module.md)

[Pannoomoodul](add-hero-module.md)

[Videopleieri moodul](add-video-player.md)
