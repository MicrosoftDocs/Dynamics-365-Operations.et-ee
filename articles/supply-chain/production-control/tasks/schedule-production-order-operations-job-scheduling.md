---
title: Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega
description: Selles teemas keskendutakse tootmistellimuse plaanimisele koos toimingute ja tööde plaanimisega.
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3023d6a6fe09c84b47839a2c4b78c37907754ded
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914880"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas keskendutakse tootmistellimuse plaanimisele koos toimingute ja tööde plaanimisega. Toimingute planeerimisega ei looda ühtegi tööd, samas kui töö planeerimisega luuakse tööd. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud diskreetses tootmiskeskkonnas töötavale tootmisjuhile, tootmise planeerijale või tööde järelevaatajale.


## <a name="create-a-production-order"></a>Tootmistellimuse loomine
1. Avage navigeerimispaanil **Moodulid > Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused**.
2. Valige **Uus tootmistellimus**.
3. Sisestage või valige väärtus väljale **Kauba kood**. Valige kaubakood **D0001**.  
4. Valige **Loo**.

## <a name="schedule-operations-for-the-production-order"></a>Tootmistellimuse toimingute plaanimine
1. Märkige äsja loodud rida.      
2. Toimingupaanil valige **Plaani**.
3. Valige **Plaani toiming**.
4. Väljal **Planeerimissuund** valige **Planeerimiskuupäevast edasi**.
5. Väljale **Planeerimiskuupäev** sisestage kuupäev. Valige kuupäev, näiteks täna pluss üks nädal. Kui planeerimissuund on valitud, planeeritakse tootmistellimus sellest kuupäevast edasi.  
6. Valige nupp **OK**.
7. Märkige loendis valitud rida. Pange tähele, et olek on muudetud **Plaanitud**. 
8. Valige **Kõik tööd**. Pange tähele, et operatsioonide planeerimisega ei looda ühtegi tööd.  
9. Sulgege leht.

## <a name="schedule-jobs-for-the-production-order"></a>Tootmistellimuse tööde plaanimine
1. Toimingupaanil valige **Plaani**.
2. Valige **Plaani töid**.
3. Väljal **Planeerimissuund** valige **Planeerimiskuupäevast edasi**.
4. Väljale **Planeerimiskuupäev** sisestage kuupäev. Valige tuleviku kuupäev, näiteks täna pluss üks nädal. Kui planeerimissuund on valitud, planeeritakse tootmistellimus sellest kuupäevast edasi.  
5. Valige nupp **OK**.
6. Toimingupaanil valige **Tootmistellimus**.
7. Valige **Kõik tööd**. Pange tähele, et aktiivses protsessis luuakse tööde planeerimisel 5 tööd.  

