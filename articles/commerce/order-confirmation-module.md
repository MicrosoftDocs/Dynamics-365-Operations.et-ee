---
title: Tellimuse kinnituse moodul
description: See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6914f8c968b03c05a2311a31a4f391c828db5b8b35bc864504dad78f43b3623f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733842"
---
# <a name="order-confirmation-module"></a>Tellimuse kinnituse moodul

[!include [banner](includes/banner.md)]

See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.

Tellimuse kinnitamise moodulit kasutatakse pärast tellimuse esitamist tellimuse kinnituse üksikasjade kuvamiseks. See kuvab tellimuse kinnituse ID, tellimuse kontaktandmeid ja muud tellimuse üksikasjad, nagu ostetud kaubad, makseteave, järeletulemisvõimalused ja tarneviis.

## <a name="order-confirmation-module-properties"></a>Tellimuse kinnituse mooduli atribuudid

| Atribuudi nimi  | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Pealkiri        | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Tellimuse kinnituse moodulil võib olla pealkiri. Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**. Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele. |
| Kontakti number | Tekst | Tellimusega seotud küsimuste jaoks saab kasutada kontaktnumbrit. |
| Järeletulemise ajavahemiku teabe kuvamine | Tõene või väär | See atribuut on saadaval Dynamics 365 Commerce'i versioonis 10.0.15 või uuemas versioonis. Kui see on tõene, kuvatakse järeletulemise ajavahemiku teave, kui see on kauba järeletulemise jaoks ette nähtud|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Moodulid, mida saab tellimuse kinnitamise lehel kasutada

Tellimuse kinnitamise lehe loomisel saate lisaks tellimuse kinnitamise moodulile lisada ka teisi asjakohaseid mooduleid. Järgmisena on toodud mõned näited.

- **Soovituste moodul** – soovituste mooduli saab lisada tellimuse kinnitamise lehele, et soovitada kliendile muid tooteid.
- **Turunduse moodulid** – mis tahes turunduse mooduli saab lisada tellimuse kinnitamise lehele, et kuvada turunduse sisu.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Lehele tellimuse kinnitamise mooduli lisamine

Uuele lehele tellimuse kinnitamise mooduli lisamiseks ja vajalike atribuutide häälestamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all nimi **Tellimuse kinnitamise mall** ja valige seejärel **OK**.
1. Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.
1. Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse kinnitamine** ja valige seejärel **OK**.
1. Valige **Salvesta** ja seejärel malli eelvaate kuvamiseks **Eelvaade**. Tellimuse kinnituse moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Malli valimine** suvand **Tellimuse kinnitamise mall**. Sisestage jaotises **Lehe nimi** väärtus **Tellimuse kinnitamise leht** ja seejärel valige **OK**.
1. Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse kinnitamine** ja valige seejärel **OK**.
1. Valige tellimuse kinnitamise mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.
1. Sisestage dialoogiboksi **Pealkiri** väljale **Pealkirja tekst** pealkirja tekst **Tellimuse kinnitamine** ja valige seejärel **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Maksmismoodul](add-checkout-module.md)

[Makse moodul](payment-module.md)

[Tarneaadressi moodul](ship-address-module.md)

[Tarnesuvandite moodul](delivery-options-module.md)

[Järeletulemise teabe moodul](pickup-info-module.md)

[Kinkekaardi moodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]