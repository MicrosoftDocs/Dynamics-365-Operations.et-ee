---
title: Tellimuse kinnituse moodul
description: See artikkel hõlmab tellimuse kinnitusmooduleid ja kirjeldab nende kasutamist moodulites Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6011c7e4713813a02fa8f812ea8981fd6fa0253f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269131"
---
# <a name="order-confirmation-module"></a>Tellimuse kinnituse moodul

[!include [banner](includes/banner.md)]

See artikkel hõlmab tellimuse kinnitusmooduleid ja kirjeldab nende kasutamist moodulites Microsoft Dynamics 365 Commerce.

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
1. Dialoogiaknas **Uus** mall malli nime **all** sisestage nime tellimuse **kinnitusmall ja** seejärel valige **OK**.
1. Kehapesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige vaikelehemoodul **ja** seejärel valige **OK**.
1. Vaikelehe mooduli põhipesas **valige** kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige tellimuse **kinnitusmoodul** ja seejärel valige **OK**.
1. Valige **Salvesta** ja seejärel malli eelvaate kuvamiseks **Eelvaade**. Tellimuse kinnituse moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Dialoogiaknas **Uue lehe loomine** sisestage jaotises **Lehe nimi** tellimuse **kinnitusleht ja** seejärel valige **järgmine**.
1. Valige **valiku Vali mall** all Tellimuse **kinnitusmall ja** seejärel **edasi**.
1. Valige **valiku Vali paigutus** all lehekülje paigutus (nt Paindlik **paigutus**) ja seejärel klõpsake nuppu **Edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui teil on vaja lehekülje teavet redigeerida, valige **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**. 
1. Vaikelehe mooduli põhipesas **valige** kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige tellimuse **kinnitusmoodul** ja seejärel valige **OK**.
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
