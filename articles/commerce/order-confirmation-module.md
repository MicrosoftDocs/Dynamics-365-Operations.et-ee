---
title: Tellimuse kinnituse moodul
description: See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698322"
---
# <a name="order-confirmation-module"></a>Tellimuse kinnituse moodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.

## <a name="overview"></a>Ülevaade

Tellimuse kinnituse moodulit kasutatakse kinnitusteate kuvamiseks tellimuse kinnitamise lehel pärast tellimuse esitamist. Tellimuse kinnituse moodul näitab tellimuse kinnituse numbrit ja kliendi meiliaadressi, mis esitati maksmise ajal.

Kui tellimus esitatakse maksmise ajal, edastatakse tellimuse kinnituse number ja kliendi meiliaadress tellimuse kinnitamise lehe URL-i päringu stringina. Tellimuse kinnituse moodul võtab selle teabe vastu ja muudab tellimuse oleku tellimuse kinnitamise lehele. Tellimuse kinnituse moodul nõuab tellimuse oleku esitamiseks lehe konteksti.

## <a name="order-confirmation-module-properties"></a>Tellimuse kinnituse mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pealkiri       | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Tellimuse kinnituse moodulil võib olla pealkiri. Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**. Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Moodulid, mida saab kasutada tellimuse kinnitamise lehe moodulis 

- **Soovitused** – soovituste mooduli saab panna tellimuse kinnitamise lehele, et soovitada kliendile muid tooteid.
- **Turundus** – turunduse moodul saab lisada turunduse sisu tellimuse kinnitamise lehele.

## <a name="create-an-order-confirmation-page-module"></a>Tellimuse kinnitamise lehe mooduli loomine

1. Looge lehe mall nimega **tellimuse kinnituse mall**.
1. Lisage vaikimisi lehe pesasse **Peamine** tellimuse kinnituse moodul.
1. Tellimuse kinnituse moodulis lisage soovituste moodul.
1. Malli salvestamine ja eelvaade. Tellimuse kinnituse moodulit ei tohi renderdada, kuna see nõuab tellimuse kinnituse numbri konteksti.
1. Registreerige mall ja avaldage see.
1. Kasutage äsja loodud tellimuse kinnituse malli, et luua leht, mille nimi on **tellimuse kinnituse leht**.
1. Lisage lehekülje liigendusele vaikimisi lehekülg.
1. Lisage päise fragment pesasse **Päis**.
1. Lisage jaluse fragment pesasse **Jalus**.
1. Lisage tellimuse kinnituse moodul pesasse **Peamine**.
1. Tellimuse kinnituse mooduli atribuutide paanil lisage pealkiri **Tellimuse kinnitus**.
1. Tellimuse kinnituse mooduli alla lisage soovituste moodul ja konfigureerige see nii, et see kasutaks sätteid **Uus** ja **Enimmüüdud**.
1. Salvestage ja eelvaadake lehte, registreerige ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteineri moodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
