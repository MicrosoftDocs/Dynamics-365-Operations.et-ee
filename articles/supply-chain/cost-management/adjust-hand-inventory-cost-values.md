---
title: Vaba kaubavaru kuluväärtuste korrigeerimine
description: Lehel Vaba kaubavaru korrigeerimine saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "335159"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Vaba kaubavaru kuluväärtuste korrigeerimine

[!include [banner](../includes/banner.md)]

Lehel Vaba kaubavaru korrigeerimine saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist.

Lehel **Vaba kaubavaru korrigeerimine** saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist. **Märkus.** Lehe **Vaba kaubavaru korrigeerimine** avamiseks valige lehel **Sulgemine ja korrigeerimine** lõpetatud lao sulgemisprotsessi kirje ja klõpsake siis valikuid **Korrigeerimine** &gt; **Laoseis**. **Näide.** Veebruaris on teil järgmised kanded.

-   1. veebruar: kaubavaru finantssissetulek, kogus 2, hind 10.00 USD
-   5. veebruar: kaubavaru finantssissetulek, kogus 1, hind 13.00 USD
-   19. veebruar: kaubavaru finantssissetulek, kogus 1, keskmine hind 11.00 USD

See kaup seadistati FIFO-laomudeliga (esimesena sisse, esimesena välja) ning lao sulgemine toimus 28. veebruaril. Finantsväliskanne summas 11,00 USD tasakaalustatakse finantssissetuleku suhtes 1. veebruaril ja tehakse parandus 1,00 USD ulatuses. Järgmistes lao sissetulekutes sisaldub avatud lao koguseid:

-   1. veebruar: kogus 1, hind 10.00 USD
-   5. veebruar: kogus 1, hind 13.00 USD

Et seadistada nende kahe kauba kulu 15,00 USD-le, kasutage vaba kaubavaru korrigeerimise valikut, et korrigeerida vabu kaubakoguseid alates viimasest lao sulgemise perioodist. **Märkus.** Vaba kaubavaru korrigeerimise kande kuupäeva sisestus on ka viimase lao sulgemise kuupäev. Seda kuupäeva ei saa muuta.
