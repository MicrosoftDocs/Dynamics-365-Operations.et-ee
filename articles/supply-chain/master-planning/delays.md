---
title: Hilinemised
description: "Selles artiklis antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db5c507fbc68e637dbbc4ef3311d1fbd298f24f
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="delays"></a>Hilinemised

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.

Koondplaneerimine saab arvutada varaseima kande täitmise kuupäeva täitmisaegade, materjali saadavuse, võimsuse saadavuse ja erinevate plaanimisparameetrite põhjal. 

Kui koondplaneerimine arvutab praegusest kuupäevast varasema tellimuse kuupäeva, ei saa tellimust täita õigel ajal. Seetõttu lükatakse tellimus edasi. Sellisel juhul plaanib koondplaneerimine tellimust praegusest kuupäevast edasi ja hõlmab täitmisaegu. Need täitmisajad algavad mis tahes madalama taseme kaubakomponentidega. Tellimus saab seejärel edasilükatud kuupäeva. Edasilükatud kuupäev on praegustel andmetel põhinev realistlik tähtaeg. Koondplaneerimine arvutab ka hilinemispäevade arvu. 

Mõningatel juhtudel võite hilinemisi mitte arvutada, näiteks kui kasutajad teavad, et saavad täitmisaegu kiirendada, valides alternatiivsed tarneviisid. 

Saate konfigureerida laovarude grupi viivituste arvutamise viisi. Seejärel saate laovarude grupi hiljem kaubale lisada. 

Lehel **Koondplaneerimise parameetrid** saate seadistada viivituste arvutamise algusaja. Kui tellimus täidetakse pärast seda aega, lisatakse tellimuse viivituskuupäevale ühepäevane viivitus. 

**Märkus.** Varasemates versioonides kutsuti arvutatud viivitusi nimetusega *tähtajateated*, hilinenud kuupäeva nimetusega *tähtajakuupäev* ja hilinenud kandele viidati nimetusega *tulevane kanne*.

<a name="see-also"></a>Vt ka
--------

[Laovarude sätted](coverage-settings.md)




