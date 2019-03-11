---
title: Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega
description: See protseduur keskendub tootmistellimuse planeerimisele koos toimingute ja töö planeerimisega.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2019
ms.locfileid: "352455"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur keskendub tootmistellimuse planeerimisele koos toimingute ja töö planeerimisega. Toimingute planeerimisega ei looda ühtegi tööd, samas kui töö planeerimisega luuakse tööd. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud diskreetses tootmiskeskkonnas töötavale tootmisjuhile, tootmise planeerijale või tööde järelevaatajale.


## <a name="create-a-production-order"></a>Tootmistellimuse loomine
1. Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.
2. Klõpsake valikut Uus tootmistellimus.
3. Sisestage või valige väärtus väljal Kaubakood.
    * Valige kaubakood D0001.  
4. Klõpsake käsku Loo.

## <a name="schedule-operations-for-the-production-order"></a>Tootmistellimuse toimingute plaanimine
1. Märkige loendis valitud rida.
    * Valige tootmistellimus, mille just lõite. See peaks olema loendi alguses.      
2. Klõpsake tegumiribal valikut Graafik.
3. Klõpsake valikut Planeeri toiminguid.
4. Valige väljal Planeerimissuund üksus Planeerimiskuupäevast edasi.
5. Sisestage kuupäev väljale Plaanimiskuupäev.
    * Valige kuupäev, näiteks täna pluss üks nädal. Kui planeerimissuund on valitud, planeeritakse tootmistellimus sellest kuupäevast edasi.  
6. Klõpsake nuppu OK.
7. Märkige loendis valitud rida.
    * Pange tähele, et olekuks määratakse Planeeritud.  
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake valikut Kõik tööd.
    * Pange tähele, et operatsioonide planeerimisega ei looda ühtegi tööd.  
10. Sulgege leht.

## <a name="schedule-jobs-for-the-production-order"></a>Tootmistellimuse tööde plaanimine
1. Klõpsake tegumiribal valikut Graafik.
2. Klõpsake valikut Tööde planeerimine.
3. Valige väljal Planeerimissuund üksus Planeerimiskuupäevast edasi.
4. Sisestage kuupäev väljale Plaanimiskuupäev.
    * Valige tuleviku kuupäev, näiteks täna pluss üks nädal. Kui planeerimissuund on valitud, planeeritakse tootmistellimus sellest kuupäevast edasi.  
5. Klõpsake nuppu OK.
6. Klõpsake toimingupaanil valikut Tootmistellimus.
7. Klõpsake valikut Kõik tööd.
    * Pange tähele, et aktiivses protsessis luuakse tööde planeerimisel 5 tööd.  

