---
title: Varude töölehe aruanded
description: Kui kasutate elektroonilisel aruandlusel põhinevaid konfigureeritavaid varude aruandeid, siis peate seadistama seose konkreetse aruande ja töölehe tüübi vahel.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalName
audience: Application User
ms.reviewer: kfend
ms.custom: 265144
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5b1ee2f7d75897da4cc884e11d2a499ce4016a00
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818282"
---
# <a name="inventory-journal-reports"></a>Varude töölehe aruanded

[!include [banner](../includes/banner.md)]

Kui kasutate elektroonilisel aruandlusel põhinevaid konfigureeritavaid varude aruandeid, siis peate seadistama seose konkreetse aruande ja töölehe tüübi vahel.

Konkreetse aruande ja töölehe tüübi vahelise seose seadistamiseks sisestage lehel **Varude töölehe nimed** (**Varude haldus** &gt; **Seadistus** &gt; **Töölehtede nimed** &gt; **Varud**) aruandele nimi. **Märkus:** toetatud konfiguratsioonide seadistamiseks laadige alla vajalikud elektroonilise aruandluse konfiguratsioonid. Lisateavet leiate jaotisest [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md). Näited Euroopas toetatud konfiguratsioonidega laoaruannete kohta on loetletud järgmises tabelis.

| Riik            |    Aruande kirjeldus               | Töölehe tüüp     |    Vormingu vastenduse nimi                  |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| Leedu, Ungari | Inventuuriväljavõtte aruanne          | Inventuur         | Inventuuriväljavõte (HU, LT)            |
| Läti, Poola     | Varude ümberklassifitseerimise dokument | Ülekanne         | InventoryReclassificationDocument\_PLLV |
| Eesti            | Varude ümberklassifitseerimise dokument | Ülekanne         | InventoryReclassificationDocument\_EE   |
| Poola             | Sisemine PW/RW                      | Liikumine         | InventJournalLinesDocPL                 |
| Läti             |  Varude liikumise dokument         | Liikumine         | Liikumine\_LV                            |
| Läti             | Varude allahindluse dokument       | Korrigeerimine       | InventJournalLines\_LV                  |
| Läti             | Ülekande tarneteade              | Ülekanne         | InternalTransferDeliveryNote\_LV        |
| Läti             | Inventuuridokumendi aruanne            | Inventuur         | CountedDocument\_LV                     |
| Läti             | Inventuuri loendi aruanne                | Inventuur         | Inventuuri loend                           |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]