---
title: Mitme tegevuse kanban-reegli loomine
description: See protseduur näitab, kuidas luua kanban-reeglit, mis sisaldab tootmisvoost mitut tegevust.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f55034f4f0557023ce0c659c1e8258214cf8bfa3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569235"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Mitme tegevuse kanban-reegli loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua kanban-reeglit, mis sisaldab tootmisvoost mitut tegevust. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.


## <a name="create-a-new-kanban-rule"></a>Looge uus kanban-reegel.
1. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
2. Klõpsake valikut Uus.
3. Valige väljalt Täiendusstrateegia väärtus Plaanitud.
4. Sisestage või valige väärtus väljal Esimene plaanitegevus.
    * Valige SpeakerAssemblyAndPolish.  
5. Märkige ruut Mitu tegevust.
    * Eesmärk on kaasata kanban-reeglisse mitu tegevust. Tootmisvoos valitakse tee viimase plaani tegevuse valimisel.  
6. Sisestage või valige väärtus väljal Viimane plaanitegevus.
    * Valige SpeakerTestAndPackaging. Pärast selle väärtuse valimist avaneb leht automaatselt. Valige kanban-voog SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Klõpsake nuppu OK.  
7. Laiendage jaotist Üksikasjad.
8. Sisestage või valige väärtus väljal Toode.
    * Valige kaup L0006.  

## <a name="create-kanban-and-view-jobs"></a>Kanbani loomine ja tööde vaatamine
1. Laiendage jaotist Kanbanid.
2. Klõpsake vahekaarti Lisa.
3. Sisestage väljale Uute kanbanide arv väärtus 1.
    * See loob ühe kanbani.  
4. Määrake toote koguseks 3.
    * Kanban töötleb 3 toodet.  
5. Sisestage kuupäev ja kellaaeg väljale Tähtaja kuupäev/kellaaeg.
    * Võite sisestada väärtuse Täna.  
6. Klõpsake käsku Loo.
7. Klõpsake käsku Details (Üksikasjad).
    * Pange tähele, et kanbanil on tootmisvoost kaks protsessitööd. Esimene on SpeakerAssemblyAndPolish ja teine on SpeakerTestAndPackaging.  
    * See on viimane etapp!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]