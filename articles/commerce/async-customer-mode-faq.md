---
title: Asünkroonse kliendi loomise režiimi KKK
description: See artikkel annab vastused korduma kippuvatele küsimustele asünkroonse kliendi loomise režiimi kohta Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229972"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Asünkroonse kliendi loomise režiimi KKK

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See artikkel annab vastused korduma kippuvatele küsimustele asünkroonse (async) kliendi loomise režiimi kohta Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Miks ei saa lubada funktsiooni "Luba klientide redigeerimine asünkroonses režiimis"?

Enne kui lubate **klientide redigeerimise asünkroonses režiimis**, peate lubama järgmised funktsioonid:

- Klienditellimuste ja kliendikannete jõudluse parendused
- Luba täiustatud async Customeri loomine
- Kliendiaadresside asünkroonse loomise lubamine

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Miks ma siiski näha reaalajas teenuse kõnesid, mis on tehtud Commerce Headquartersisse pärast seda, kui funktsioon Luba klientide redigeerimine asünkroonrežiimis on lubatud?

See probleem ilmneb siis Commerce Data Exchange, kui (CDX) töid pole käitatud, et tagada funktsiooni olek ja teised kanali metaandmed sünkroonitakse kanaliga. Enne stsenaariumi kordamist veenduge, et järgmised CDX-tööd käitatakse Commerce Headquartersis:

- 1110 (globaalne konfiguratsioon)
- 1010 (kliendid)
- 1070 (kanali konfigureerimine)

Andmed, mis on vahemällu talletatud Commerce Scale Unitis (CSU) ei pruugi pärast CDX-tööde käivitamist Commerce Headquartersis kohe kajastuda.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Miks ei näita Commerce Headquarters kliendi loomist või värskendamist kassast või e-äri kanalist?

Kontrollige, et siin loetletud järjestuses oleks tehtud järgmised toimingud.

1. Käitage CDX P-tööd Commerce headquartersis **, et tagada tabelites RETAILASYNCCUSTOMERV2, RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT** **,** RETAILASYNCCUSTOMERAFFILIATION **ja** RETAILASYNCCUSTOMERATTRIBUTEV2 **talletatud** async Customeri andmed, on commerce headquartersis saadaval.
1. Käivitage klientide **ja kanali taotluste pakett-töö** sünkroonimine commerce headquartersis. Pärast pakett-töö edukat käivitamist on **kõigi varem mainitud tabelitest edukalt töödeldud kirjete välja OnlineOperationCompleted** **väärtuseks seatud 1**.
