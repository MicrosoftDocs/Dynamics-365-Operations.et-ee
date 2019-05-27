---
title: Piirangutega plaani koostamine
description: Selles protseduuris näitlikustatakse, kuidas luua plaani, mis võtab arvesse nii materjali kui ka võimsuse piiranguid.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556019"
---
# <a name="generate-a-constrained-plan"></a>Piirangutega plaani koostamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris näitlikustatakse, kuidas luua plaani, mis võtab arvesse nii materjali kui ka võimsuse piiranguid. Plaan tagab, et tootmine ei käivitu enne, kui materjalid on olemas ja ressursid pole üle broneeritud. 

Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud tootmisplaanijale.


## <a name="set-up-a-constrained-plan"></a>Piirangutega plaani seadistamine
1. Klõpsake valikul Koondplaneerimine.
2. Klõpsake valikul Koondplaneerimise plaanid.
3. Otsige loendist ja valige soovitud kirje.
    * Näide: StaticPlan  
4. Valige väljal Piiratud võimsus suvand Jah.
5. Sisestage väärtus „30” väljale Piiratud võimsus.
6. Laiendage jaotist Ajapiirid päevades.
7. Valige väljal Võimsus suvand Jah.
8. Sisestage arv väljale Võimsuse plaanimise ajapiir (päevades).
    * Näide: 60  
9. Valige väljal Arvutatud hilinemised suvand Jah.
10. Sisestage arv väljale Hilinemiste ajapiiri arvutamine (päevades).
    * Näide: 60  
11. Laiendage jaotist Arvutatud hilinemised.
12. Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.
13. Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.
14. Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.
15. Sulgege leht.

## <a name="create-a-constrained-plan"></a>Piirangutega plaani loomine
1. Klõpsake nuppu Käivita.
2. Sisestage või valige väärtus väljal Koondplaan.
    * Valige plaan, millele olete piirangud seadistanud.  
3. Klõpsake nuppu OK.
    * See võib veidi aega võtta.  
4. Klõpsake valikut Planeeritud tellimused.

