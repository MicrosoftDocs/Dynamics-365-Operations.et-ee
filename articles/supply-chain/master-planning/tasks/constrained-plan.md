---
title: Piirangutega plaani koostamine
description: See artikkel selgitab, kuidas luua plaani, mis arvestab nii materjali- kui võimsusepiiranguid.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65884d556724cd6132fe328e95a5bec78885c174
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904010"
---
# <a name="generate-a-constrained-plan"></a>Piirangutega plaani koostamine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas luua plaani, mis arvestab nii materjali- kui võimsusepiiranguid. Plaan tagab, et tootmine ei käivitu enne, kui materjalid on olemas ja ressursid pole üle broneeritud. 

Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud tootmisplaanijale.


## <a name="set-up-a-constrained-plan"></a>Piirangutega plaani seadistamine
1. Avalehel valige tööruum **Koondplaneerimine**.
2. Valige tööruumi kõige parempoolsemalt küljelt linkide loendist **Koondplaan**.
3. Otsige loendist ja valige soovitud kirje. Näide: **StaticPlan**  
4. Valige väärtus **Jah** väljal **Piiratud võimsus**.
5. Väljale **Piiratud võimsuse ajapiir** sisestage `30`.
6. Laiendage jaotist **Ajapiir päevades**.
7. Valige väärtus **Jah** väljal **Võimsus**.
8. Väljale **Võimsuse plaanimise ajapiir (päevad)** sisestage arv. Näide: `60`  
9. Valige väärtus **Jah** väljal **Arvutatud hilinemised**.
10. Väljale **Arvuta hilinemiste ajapiir (päevad)** sisestage arv. Näide: `60` 
11. Laiendage jaotist **Arvutatud hilinemised**.
12. Valige väärtus **Jah** kõigile suvandi **Lisa arvutatud hilinemine vajaduse kuupäevale** väljadele.
13. Sulgege leht.

## <a name="create-a-constrained-plan"></a>Piirangutega plaani loomine
1. Valige käsk **Käitus**.
2. Väljale **Koondplaan** sisestage või valige plaan, millele soovite seadistada piiranguid.  
3. Valige nupp **OK**.
4. Valige **Plaanitud tellimused**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]