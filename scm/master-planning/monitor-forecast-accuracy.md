---
title: "Monitor prognoosi täpsust"
description: "Selles artiklis kirjeldatakse prognoosi täpsust, et Microsoft Dynamics 365 operatsioonide arvutab ja selgitab, kuidas kuvatakse väärtused täpsuse tüüpi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Monitor prognoosi täpsust

Selles artiklis kirjeldatakse prognoosi täpsust, et Microsoft Dynamics 365 operatsioonide arvutab ja selgitab, kuidas kuvatakse väärtused täpsuse tüüpi.

Dynamics 365 operatsioonide arvutab prognoosi täpsust järgmisi:

-   Ajalooline prognoosi täpsus, kus võrreldakse koondplaneerimises kasutatavat prognoosi ajaloolise nõudlusega. Ajaloolise prognoosi täpsuse väärtuste (nii absoluutsete väärtuste kui ka väärtuste protsendi) vaatamiseks klõpsake lehel **Nõudluse prognoosi üksikasjad** nuppu **Kuva täpsus**.
-   Prognooside loomisel kasutatud prognoosimudeli eeldatav täpsus. Saate vaadata täpsusprotsenti lehe **Nõudluse prognoosi üksikasjad** jaotisest **Mudeli üksikasjad – MAPE**. 

**Märkus:** Dynamics 365 toimingute nõudluse prognoosimise Microsoft Azure'i masinõppe teenuse kasutamisel sisemudeli täpsus arvutus põhineb testi andmete hulka. Määrata testi andmete hulka, määra ning **TEST\_seatud\_suurus\_%** parameeter on **nõudluse prognoosimise parameetrid** lehekülg. Näiteks kui seate väärtuseks **20**, kasutatakse sisemise mudeli täpsuse arvutamiseks viimast 20% ajaloolistest andmetest.


<a name="see-also"></a>Vt ka
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


