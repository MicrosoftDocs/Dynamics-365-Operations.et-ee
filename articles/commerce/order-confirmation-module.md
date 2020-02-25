---
title: Tellimuse üksikasjade moodul
description: See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.
author: anupamar
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026013"
---
# <a name="order-details-module"></a>Tellimuse üksikasjade moodul


[!include [banner](includes/banner.md)]

See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.

## <a name="overview"></a>Ülevaade

Tellimuse üksikasjade moodulit kasutatakse pärast tellimuse esitamist tellimuse kinnituse üksikasjade kuvamiseks. See kuvab tellimuse kinnituse ID, tellimuse kontaktandmeid ja muud tellimuse üksikasjad, nagu ostetud kauvad makseteave ja tarneviis.

## <a name="order-confirmation-module-properties"></a>Tellimuse kinnituse mooduli atribuudid

| Atribuudi nimi  | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Pealkiri        | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Tellimuse kinnituse moodulil võib olla pealkiri. Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**. Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele. |
| Kontakti number | Tekst | Tellimusega seotud küsimuste jaoks saab kasutada kontaktnumbrit. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moodulid, mida saab tellimuse üksikasjade lehel kasutada

Tellimuse üksikasjade lehe loomisel saate lisaks tellimuse üksikasjade moodulile lisada ka teisi asjakohaseid mooduleid. Järgmisena on toodud mõned näited.

- **Soovituste moodul** – soovituste mooduli saab lisada tellimuse üksikasjade lehele, et soovitada kliendile muid tooteid.
- **Turunduse moodulid** – mis tahes turunduse mooduli saab lisada tellimuse üksikasjade lehele, et kuvada turunduse sisu.

## <a name="create-an-order-details-page-module"></a>Tellimuse üksikasjade lehe mooduli loomine

1. Looge lehe mall nimega **Tellimuse üksikasjade mall**.
1. Lisage vaikimisi lehe pesasse **Peamine** tellimuse üksikasjade moodul.
1. Lisage tellimuse üksikasjade moodulis soovituste moodul.
1. Malli salvestamine ja eelvaade. Tellimuse üksikasjade moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.
1. Viige lõpuni malli redigeerimine ja avaldage see.
1. Kasutage äsja loodud tellimuse üksikasjade malli, et luua leht, mille nimi on **Tellimuse üksikasjade leht**.
1. Lisage lehekülje liigendusele vaikimisi lehekülg.
1. Lisage päise fragment pesasse **Päis**.
1. Lisage jaluse fragment pesasse **Jalus**.
1. Lisage tellimuse üksikasjade moodul pesasse **Peamine**.
1. Tellimuse üksikasjade mooduli atribuutide paanil lisage pealkiri **Tellimuse üksikasjad**.
1. Lisage tellimuse üksikasjade mooduli alla soovituste moodul ja konfigureerige see nii, et see kasutaks sätteid **Uus** ja **Enimmüüdud**.
1. Salvestage ja kuvage lehe eelvaade.
1. Viige lõpuni lehe redigeerimine ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteineri moodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
