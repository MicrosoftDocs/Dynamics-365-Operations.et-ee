---
title: Hilinemised
description: Selles teemas antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/20/2019
ms.locfileid: "878306"
---
# <a name="delays"></a>Hilinemised

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.

Koondplaneerimine saab arvutada varaseima kande täitmise kuupäeva täitmisaegade, materjali saadavuse, võimsuse saadavuse ja erinevate plaanimisparameetrite põhjal. 

Kui koondplaneerimine arvutab praegusest kuupäevast varasema tellimuse kuupäeva, ei saa tellimust täita õigel ajal. Seetõttu lükatakse tellimus edasi. Sellisel juhul plaanib koondplaneerimine tellimust praegusest kuupäevast edasi ja hõlmab täitmisaegu. Need täitmisajad algavad mis tahes madalama taseme kaubakomponentidega. Tellimus saab seejärel edasilükatud kuupäeva. Edasilükatud kuupäev on praegustel andmetel põhinev realistlik tähtaeg. Koondplaneerimine arvutab ka hilinemispäevade arvu. 

Mõningatel juhtudel võite hilinemisi mitte arvutada, näiteks kui kasutajad teavad, et saavad täitmisaegu kiirendada, valides alternatiivsed tarneviisid. 

Saate konfigureerida laovarude grupi viivituste arvutamise viisi. Seejärel saate laovarude grupi hiljem kaubale lisada. 

Lehel **Koondplaneerimise parameetrid** saate seadistada viivituste arvutamise algusaja. Kui tellimus täidetakse pärast seda aega, lisatakse tellimuse viivituskuupäevale ühepäevane viivitus. 

> [!MÄRKUS} Varasemates versioonides nimetati arvutatud viivitusi *tähtajateadeteks*, hilinenud kuupäeva *tähtajakuupäevaks* ja hilinenud kannet *tulevaseks kandeks*.

## <a name="desired-date"></a>Soovitud kuupäev

Lehe **Plaanitud tellimus** vahekaardil **Viivitused** on planeeritud kuupäeva parameeter **Soovitud kuupäev**. Plaanitud tellimuse soovitud kuupäev on viivituste aluskuupäev, mis on arvutatud kuupäev, mis võrdub parameetrist **Netonõue** arvutatud parameetriga **Nõutav kuupäev**. Kui plaanitud tellimus on koosluse rida, tootmisrida või kanban-rida, on soovitud kuupäeva aluseks **Vajaduse kuupäev** ja soovitud kuupäeva ei kuvata lehel **Plaanitud tellimus**.

<a name="additional-resources"></a>Lisaressursid
--------

[Laovarude sätted](coverage-settings.md)
