--- 
title: Kanban-koguse arvutuspoliitika lisamine kanban-reeglile
description: See protseduur keskendub kanban-koguse arvutamise poliitika loomisele ja selle lisamisele kanban-reeglisse kanbani suuruse ja koguste optimeerimiseks.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f9e0ccf25a346d54e48f51b0866f0c11e98bf0a0
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Kanban-koguse arvutuspoliitika lisamine kanban-reeglile

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur keskendub kanban-koguse arvutamise poliitika loomisele ja selle lisamisele kanban-reeglisse kanbani suuruse ja koguste optimeerimiseks. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud väärtuse voo haldurile. See protseduur on eeltingimus protseduuri Kanban koguse soovituste arvutamine loomiseks. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Kanban-koguse arvutamise poliitika loomine
1. Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-koguse arvutamine > Kanban-koguse arvutamise poliitikad.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
    * Näiteks sisestage Speaker2016.  
4. Klõpsake väljal Koondplaan otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje.
    * Valige nõudluse arvutamiseks suvand StaticPlan.  
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake nuppu Salvesta.
8. Sisestage väljale Minimaalne kanban-kogus väärtus 1.
    * See on kanban-koguse arvutamisesse kaasatud kanbanide lisaarv.  
9. Määrake Ohutustegur väärtusele 1.
    * See on tegur, mida kasutatakse puhvervaru täiendava koguse arvutamiseks.  
10. Sisestage väljale Päevi enne väärtus 30.
    * See on päevade arv enne kanban-koguse arvutamise kuupäeva, mis nõudluse arvutamisse kaasatakse.  
11. Sisestage väljale Päevi pärast väärtus 30.
    * See on päevade arv pärast kanban-koguse arvutamise kuupäeva, mis nõudluse arvutamisse kaasatakse.  Arvutamiseks kasutatud valemit näidatakse tegelike väärtustega. Näiteks Kanban-kogus = ((keskmine igapäevane nõudlus × täitmisaeg × 2,00) / toote kogus materjali käsitlemisühiku kohta) + 1  
12. Sulgege leht.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Kanban-koguse arvutamise poliitika lisamine kanban-reeglile
1. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
2. Otsige loendist ja valige soovitud kirje.
    * Valige selle protseduuri puhul kanban-reegel 000020.  
3. Klõpsake loendis valitud real olevat linki.
4. Laiendage jaotist Kanban-koguse arvutamise poliitikad.
5. Klõpsake vahekaarti Lisa.
    * Lisage kanban-koguse arvutamise poliitika, mille olete eelmises alamülesandes äsja loonud.  
6. Märkige loendis valitud rida.
7. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
8. Klõpsake loendis valitud real olevat linki.
    * Valige poliitika Speaker2016, mille olete eelmises alamülesandes äsja loonud.  


