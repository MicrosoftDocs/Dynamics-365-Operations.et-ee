---
title: Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega
description: See artikkel keskendub operatsioonide planeerimise ja tööde planeerimisega tootmistellimuse planeerimisele.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d82d5439e57c02ddc9db4222a946bd15f4ed67e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903923"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega

[!include [banner](../../includes/banner.md)]

See artikkel keskendub operatsioonide planeerimise ja tööde planeerimisega tootmistellimuse planeerimisele. Toimingute planeerimisega ei looda ühtegi tööd, samas kui töö planeerimisega luuakse tööd. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud diskreetses tootmiskeskkonnas töötavale tootmisjuhile, tootmise planeerijale või tööde järelevaatajale.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]