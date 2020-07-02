---
title: Tellimuse üksikasjade moodul
description: See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464926"
---
# <a name="order-details-module"></a>Tellimuse üksikasjade moodul


[!include [banner](includes/banner.md)]

See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.

## <a name="overview"></a>Ülevaade

Tellimuse üksikasjade moodulit kasutatakse pärast tellimuse esitamist tellimuse kinnituse üksikasjade kuvamiseks. See kuvab tellimuse kinnituse ID, tellimuse kontaktandmeid ja muud tellimuse üksikasjad, nagu ostetud kauvad makseteave ja tarneviis.

## <a name="order-details-module-properties"></a>Tellimuse üksikasjade mooduli atribuudid

| Atribuudi nimi  | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Pealkiri        | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Tellimuse üksikasjade moodulil võib olla pealkiri. Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**. Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele. |
| Kontakti number | Tekst | Tellimusega seotud küsimuste jaoks saab kasutada kontaktnumbrit. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moodulid, mida saab tellimuse üksikasjade lehel kasutada

Tellimuse üksikasjade lehe loomisel saate lisaks tellimuse üksikasjade moodulile lisada ka teisi asjakohaseid mooduleid. Järgmisena on toodud mõned näited.

- **Soovituste moodul** – soovituste mooduli saab lisada tellimuse üksikasjade lehele, et soovitada kliendile muid tooteid.
- **Turunduse moodulid** – mis tahes turunduse mooduli saab lisada tellimuse üksikasjade lehele, et kuvada turunduse sisu.

## <a name="add-an-order-details-module-to-a-page"></a>Lehele tellimuse üksikasjade mooduli lisamine

Uuele lehele tellimuse üksikasjade mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all nimi **Tellimuse üksikasjade mall** ja valige seejärel **OK**.
1. Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.
1. Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.
1. Valige **Salvesta** ja seejärel malli eelvaate kuvamiseks **Eelvaade**. Tellimuse üksikasjade moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Vali mall** suvand **Tellimuse üksikasjade mall**. Sisestage jaotises **Lehe nimi** väärtus **Tellimuse üksikasjade leht** ja seejärel klõpsake **OK**.
1. Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.
1. Valige tellimuse üksikasjade mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.
1. Sisestage dialoogiboksi **Pealkiri** väljale **Pealkirja tekst** pealkirja tekst **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteineri moodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
