---
title: Hilinemised
description: "Selles artiklis antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9113c7728c5d23b70e3809bab31136aff63c6acf
ms.lasthandoff: 03/31/2017


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



