--- 
title: Asenduskanban-reegli loomine
description: "See protseduur keskendub olemasoleva kanban-reegli kindlal kuupäeval uue kanban-reegliga asendamisele."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5b27200a8d56192d473887f01076eced0f92e4c
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-replacement-kanban-rule"></a>Asenduskanban-reegli loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur keskendub olemasoleva kanban-reegli kindlal kuupäeval uue kanban-reegliga asendamisele. See on kasulik juhul, kui muudatused tootmisvoos või täiendamise reeglites peavad olema koordineeritud ja ajastatud. Protseduuri loomiseks kasutati demoettevõtte USMF andmeid Protseduur on mõeldud protsessiinsenerile või väärtuse voo haldurile, kui ta valmistab ette tootmist muudetud tootmisvoo või uue täiendusreegli puhul. See toiming asendab kanban-reegli 000022 uue reegliga ja suurendab uue reegli puhul maksimaalset kogust 48-t 100-le.


## <a name="select-a-kanban-rule-to-replace"></a>Asendatava kanban-reegli valimine
1. Minge jaotisse Kanban-reeglid.
2. Otsige loendist ja valige soovitud kirje.
    * Valige kanban-reegel 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Asenduskanban-reegli loomine
1. Klõpsake suvandit Kanban-reegli asendamine.
2. Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.
    * Valige kuupäev tulevikus, näiteks üks nädal alates tänasest. See on kuupäev ja kellaaeg, millal uus kanban-reegel muutub aktiivseks ja asendab vana kanban-reegli.  
    * Kui kanban-reegel muudab tootmisvoo teed, saab valida muu tegevuse.  Selles protseduuris jätame tegevuse samaks.  
3. Klõpsake nuppu OK.
    * Pange tähele, et luuakse uus kanban-reegel, mis asendab kanban-reeglit 000022.  
    * Jõustumise kuupäev määratakse vastavalt kuupäevale, mille valisite kanban-reegli asendamisel.  
4. Otsige loendist ja valige soovitud kirje.
    * Valige asendatud kanban-reegel 000022.  
    * Pange tähele, et asendatud kanban-reeglil on sama kuupäev mis aegumiskuupäev, sest see on kuupäev, millal see aegub.  
5. Valige loendist rida 1.
    * Valige loendi ülaosas uus kanban-reegel. See on suurima kanban-reegli numbriga kanban-reegel.  
6. Klõpsake loendis valitud real olevat linki.
    * Klõpsake kanban-reegli numbrit, et avada kanban-reegel.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Asendus-kanban-reegli maksimaalse koguse muutmine
1. Määrake maksimaalse koguse väärtuseks 100.
    * Laiendage kiirkaarti Kogused, et näha välja Maksimaalne kogus. Maksimaalse koguse muutmine väärtusele 100 võimaldab töödelda kuni 100 kanbani.    See on selle ülesande viimane etapp.  


