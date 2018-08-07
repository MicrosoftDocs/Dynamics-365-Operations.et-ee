---
title: "Prognoosi täpsuse jälgimine"
description: "Selles artiklis kirjeldatakse, millist tüüpi prognoosi täpsust Microsoft Dynamics 365 for Finance and Operations arvutab ning selgitatakse, kuidas täpsuse väärtusi vaadata."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f54251b6f6937c59293bd44a0fc27272ffd3d55
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="monitor-forecast-accuracy"></a>Prognoosi täpsuse jälgimine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, millist tüüpi prognoosi täpsust Microsoft Dynamics 365 for Finance and Operations arvutab ning selgitatakse, kuidas täpsuse väärtusi vaadata.

Finance and Operations arvutab järgmised prognoosi täpsuse tüübid.

-   Ajalooline prognoosi täpsus, kus võrreldakse koondplaneerimises kasutatavat prognoosi ajaloolise nõudlusega. Ajaloolise prognoosi täpsuse väärtuste (nii absoluutsete väärtuste kui ka väärtuste protsendi) vaatamiseks klõpsake lehel **Nõudluse prognoosi üksikasjad** nuppu **Kuva täpsus**.
-   Prognooside loomisel kasutatud prognoosimudeli eeldatav täpsus. Saate vaadata täpsusprotsenti lehe **Nõudluse prognoosi üksikasjad** jaotisest **Mudeli üksikasjad – MAPE**. 

**Märkus.** Kui kasutate Finance and Operationsi nõudluse prognoosimise Microsoft Azure’i masinõppe teenust, põhineb sisemise mudeli täpsuse arvutus testandmete kogumil. Testandmete kogumi suuruse määramiseks seadke lehel **Nõudluse prognoosimise parameetrid** parameeter **TEST\_SET\_SIZE\_PERCENT**. Näiteks kui seate väärtuseks **20**, kasutatakse sisemise mudeli täpsuse arvutamiseks viimast 20% ajaloolistest andmetest.


<a name="additional-resources"></a>Lisaressursid
--------

[Korrigeeritud prognoosi autoriseerimine](authorize-adjusted-forecast.md)

[Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost](remove-historical-outliers-calculating-demand-forecast.md)




