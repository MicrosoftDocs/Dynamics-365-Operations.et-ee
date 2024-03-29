---
title: Väljastamise kanban-reegli loomine
description: See protseduur näitab seadistust, mida on vaja, et luua tühistamise kanban-reegel materjali ülekandmiseks säästlikus keskkonnas.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba30e9d09e9eeb0cd7428aafc1195d6b7e7caaa4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574469"
---
# <a name="create-a-withdrawal-kanban-rule"></a>Väljastamise kanban-reegli loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab seadistust, mida on vaja, et luua tühistamise kanban-reegel materjali ülekandmiseks säästlikus keskkonnas. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Protseduur on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud materjali täiendamist.


## <a name="create-new-kanban-rule"></a>Uue kanban-reegli loomine
1. Minge jaotisse Kanban-reeglid.
2. Klõpsake valikut Uus.
3. Tehke väljal Tüüp vali Tühistamine.
    * Kanban-reeglite puhul kasutatakse materjalide või kaupade edastamiseks tüüpi Tühistamine.  
4. Sisestage või valige väärtus väljal Esimene plaanitegevus.
    * Tehke valik ReplenishSpeakerComponents.   See tegevus on seadistatud teisaldama komponente laost 11, asukohast 11 lattu 12 ja asukohta 12.  
5. Sisestage või valige väärtus väljal Toode.
    * Valige suvand M0007.  
6. Sisestage number väljale Täitmisaeg.
    * Näiteks 60.  
7. Sisestage või valige väärtus väljal Mõõtühik.
    * Näiteks minutid.  

## <a name="set-quantities-for-kanban"></a>Kanbanile koguste määramine
1. Valige välja Vaikekogus väärtuseks 5.
    * See on iga kanbani kohta üle kantav kogus.  
2. Siseatage väljale Fikseeritud kanban-kogus väärtus 2.
    * See on kanbanide, mis peaksid olema aktiivsed, arv. Sellisel juhul edastavad iga 2 kanbani 5.  
3. Sisestage väljale Teatise miinimumpiir väärtus 1.
    * Kasutatakse täielike kanbanide, mis peaks olema sihtkohas, minimaalse summa jälgimiseks. Näiteks kasutatakse seda kanban-koguse ülevaates.  
4. Sisestage väljale Teatise maksimumpiir väärtus 2.
    * Kasutatakse täielike kanbanide, mis peaks olema sihtkohas, maksimaalse summa jälgimiseks. Näiteks kasutatakse seda kanban-koguse ülevaates.  

## <a name="create-kanbans"></a>Loo kanbane
1. Klõpsake nuppu Salvesta.
    * Enne, kui kanbane saab luua, tuleb kanban-reegel salvestada.  
2. Klõpsake vahekaarti Lisa.
    * Pange tähele, et aktiivseid kanbane pole, kuna soovituslik uute kanbanide arv on 2, mis võrdub fikseeritud kanban-kogusega.  
3. Klõpsake käsku Loo.
    * See loob kaks kanbani.  
    * Pange tähele, et selle tühistamise kanban-reegli puhul loodi 2 kanbani, igaühe kohta 5.  See on selle protseduuri viimane etapp.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]