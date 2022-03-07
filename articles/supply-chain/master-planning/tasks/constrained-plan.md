---
title: Piirangutega plaani koostamine
description: Selles teemas selgitatakse, kuidas luua plaani, mis arvestab nii materiaalsete kui ka võimsuse piirangutega.
author: ChristianRytt
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fea315d41d01cb578d7d60c9eb7006e4b6c3362
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578340"
---
# <a name="generate-a-constrained-plan"></a>Piirangutega plaani koostamine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas luua plaani, mis arvestab nii materiaalsete kui ka võimsuse piirangutega. Plaan tagab, et tootmine ei käivitu enne, kui materjalid on olemas ja ressursid pole üle broneeritud. 

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