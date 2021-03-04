---
title: Asenduskanban-reegli loomine
description: See protseduur keskendub olemasoleva kanban-reegli kindlal kuupäeval uue kanban-reegliga asendamisele.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae589f81811c1586e0e24de94eaf5f467f19debb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425972"
---
# <a name="create-a-replacement-kanban-rule"></a>Asenduskanban-reegli loomine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]