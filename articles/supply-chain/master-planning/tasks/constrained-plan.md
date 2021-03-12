---
title: Piirangutega plaani koostamine
description: Selles teemas selgitatakse, kuidas luua plaani, mis arvestab nii materiaalsete kui ka võimsuse piirangutega.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4af946a8dd4e5311bcb90386c88d5e7f205c4eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999852"
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

