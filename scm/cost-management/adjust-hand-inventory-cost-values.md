---
title: "Vaba kaubavaru kuluväärtuste korrigeerimine"
description: "Lehel Vaba kaubavaru korrigeerimine saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Vaba kaubavaru kuluväärtuste korrigeerimine

[!include[banner](../includes/banner.md)]


Lehel Vaba kaubavaru korrigeerimine saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist.

Lehel **Vaba kaubavaru korrigeerimine** saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist. **Märkus.** Lehe **Vaba kaubavaru korrigeerimine** avamiseks valige lehel **Sulgemine ja korrigeerimine** lõpetatud lao sulgemisprotsessi kirje ja klõpsake siis valikuid **Korrigeerimine** &gt; **Laoseis**. **Näide.** Veebruaris on teil järgmised kanded.

-   1. veebruar: kaubavaru finantssissetulek, kogus 2, hind 10.00 USD
-   5. veebruar: kaubavaru finantssissetulek, kogus 1, hind 13.00 USD
-   19. veebruar: kaubavaru finantssissetulek, kogus 1, keskmine hind 11.00 USD

See kaup seadistati FIFO-laomudeliga (esimesena sisse, esimesena välja) ning lao sulgemine toimus 28. veebruaril. Finantsväliskanne summas 11,00 USD tasakaalustatakse finantssissetuleku suhtes 1. veebruaril ja tehakse parandus 1,00 USD ulatuses. Järgmistes lao sissetulekutes sisaldub avatud lao koguseid:

-   1. veebruar: kogus 1, hind 10.00 USD
-   5. veebruar: kogus 1, hind 13.00 USD

Et seadistada nende kahe kauba kulu 15,00 USD-le, kasutage vaba kaubavaru korrigeerimise valikut, et korrigeerida vabu kaubakoguseid alates viimasest lao sulgemise perioodist. **Märkus.** Vaba kaubavaru korrigeerimise kande kuupäeva sisestus on ka viimase lao sulgemise kuupäev. Seda kuupäeva ei saa muuta.



