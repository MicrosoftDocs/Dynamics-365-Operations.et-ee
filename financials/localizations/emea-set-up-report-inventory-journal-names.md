---
title: "Lao töölehe aruanded"
description: "Seadistatav lao aruanded vastavalt elektroonilisel kasutamisel peate luua seos kindla aruande ja tüüp."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalName
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265144
ms.assetid: 0f07f62f-1053-46e9-b235-a7b38cbda409
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: eed3398651612743958722814ec5594ec34e4e5e
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-journal-reports"></a>Lao töölehe aruanded

Seadistatav lao aruanded vastavalt elektroonilisel kasutamisel peate luua seos kindla aruande ja tüüp.

Luua kindla aruande seos tüüp, edasi on **varude töölehenimede** lehele (**varud**&gt;**Setup**&gt;**nimed**&gt;**varude**), sisestage aruande nimi. **Märkus:** toetatud konfiguratsioonid seadistamiseks lae nõutav elektrooniliste andmete esitamise koosseisud. Lisateabe saamiseks vaadake [lae elektrooniline aruandlus koosseisud elutsükli teenuste](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Lao aruanded koos toetatud konfiguratsioonid Euroopas on loetletud järgmises tabelis.
|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| **Country**        | **Aruande kirjeldus**              | **Journal type** | **Kujul vastenduse nimi**                 |
| Leedu, Ungari | Inventuuri aruande aruande          | Inventuur         | Inventuuriaruanne (HU, LT)            |
| Läti, Poola     | Varude ümberklassifitseerimise dokument | Ülekanne         | InventoryReclassificationDocument\_PLLV |
| Eesti            | Varude ümberklassifitseerimise dokument | Ülekanne         | InventoryReclassificationDocument\_EE   |
| Poola             | Sisemine PW/RW                      | Liikumine         | InventJournalLinesDocPL                 |
| Läti             |  Varude liikumise dokument         | Liikumine         | Liikumine\_LV                            |
| Läti             | Varude allahindluse dokumendi       | Korrigeerimine       | InventJournalLines\_LV                  |
| Läti             | Ülekande tarneteade              | Ülekanne         | InternalTransferDeliveryNote\_LV        |
| Läti             | Lugedes dokumenti aruanne            | Inventuur         | CountedDocument\_LV                     |
| Läti             | Inventuuri aruanne                | Inventuur         | Inventuuri loend                           |




