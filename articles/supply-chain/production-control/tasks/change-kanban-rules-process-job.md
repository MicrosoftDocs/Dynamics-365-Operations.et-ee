---
title: Kanban-reeglite muutmine protsessitöö jaoks
description: Protseduur keskendub konkreetse kanbani kasutatud kanban-reegli muutmisele.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c036f6aad79e33df6009913d1e21ff6176f22593
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843789"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Kanban-reeglite muutmine protsessitöö jaoks

[!include [task guide banner](../../includes/task-guide-banner.md)]

Protseduur keskendub konkreetse kanbani kasutatud kanban-reegli muutmisele. See on kasulik koormuse ressursside tasakaalustamiseks või katkestuse korral. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Protseduur on mõeldud plaanijale, kes töötab lean manufacturingil põhinevas ettevõttes ja vastutab väärtuse voo eest.


## <a name="copy-kanban-rule"></a>Kanban-reegli kopeerimine
1. Minge jaotisse Kanban-reeglid.
2. Otsige loendist ja valige soovitud kirje.
    * Valige sündmuse kanban-reegel 000022 üksusele L0001.  
3. Klõpsake suvandit Kanban-reegli dubleerimine.
4. Klõpsake nuppu OK.

## <a name="change-kanban-rule"></a>Kanban-reegli muutmine
1. Sulgege leht.
2. Avage kanban-töö plaanimine.
3. Märkige loendis valitud rida.
    * Valige rida, millel on Kanban 000177.  
4. Klõpsake suvandit Alternatiivse kanban-reegli kasutamine.
5. Klõpsake käsku Edasi.
6. Valige või sisestage väärtus väljal Kanban-reegel.
    * Valige varem loodud kanban-reegel. See on suurima numbriga kanban-reegel.  
7. Klõpsake Lõpeta.
    * Praegu kasutab kanban-töö muud kanban-reeglit. See võib olla kasulik töörakkude koormuse tasakaalustamiseks.  

