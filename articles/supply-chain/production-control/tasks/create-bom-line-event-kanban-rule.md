---
title: Koosluserea sündmuse kanban-reegli loomine
description: See toiming keskendub seadistusele, mida on vaja sündmuse kanban-reegli loomiseks, et tagada tootmise koosluseridade varud segatud kulusäästlikus ja klassikalises tootmiskeskkonnas.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14cef6279b756ff71872747dfb1ca9e5c8cd8fcc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575047"
---
# <a name="create-a-bom-line-event-kanban-rule"></a>Koosluserea sündmuse kanban-reegli loomine

[!include [banner](../../includes/banner.md)]

See toiming keskendub seadistusele, mida on vaja sündmuse kanban-reegli loomiseks, et tagada tootmise koosluseridade varud segatud kulusäästlikus ja klassikalises tootmiskeskkonnas. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See ülesanne on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist.


## <a name="create-a-new-kanban-rule"></a>Looge uus kanban-reegel.
1. Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-koguse arvutamine > Kanban-reeglid.
2. Klõpsake valikut Uus.
3. Tehke väljal Tüüp vali Tühistamine.
    * Tühistamise tüüpi kasutatakse ülekande-kanbanide loomiseks.  
4. Valige väljal Täiendusstrateegia suvand Sündmus.
    * Sündmuse alusel kanbanide ülekandmise loomiseks valitakse sündmuse strateegia. Hiljem käivitame selle ülesande juhendis, hinnates tootmistellimust.  
5. Sisestage või valige väärtus väljal Esimene plaanitegevus.
    * Sisestage või valige väärtus ReplenishSpeakerComponents. Sellel ülekandmistegevusel on sissetulev (väljund) ladu ja asukoht 12, mis tähendab, et materjal teisaldatakse asukohta 12 laos 12.  
6. Laiendage jaotist Üksikasjad.
7. Sisestage või valige väljal Toode väärtus M0001.
8. Laiendage jaotist Sündmused.
9. Valige väljal Koosluse rea sündmus väärtus Automaatne.
    * Kui välja Koosluse rea sündmus väärtuseks on Automaatne, luuakse kanban, et täita tootmistellimuse koosluse ridade materjalivajadused.  
10. Sulgege leht.

## <a name="create-and-modify-a-new-production-order"></a>Uue tootmistellimuse loomine ja muutmine
1. Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.
2. Klõpsake valikut Uus tootmistellimus.
3. Sisestage või valige väärtus väljal Kaubakood.
    * Sisestage või valige väärtus L0001. Kasutame kaupa L0001, sest kaup M0001 on lisatud kooslusse kauba L0001 puhul.  
4. Klõpsake käsku Loo.
5. Klõpsake loendis linki väärtuse L0001 real
6. Klõpsake valikut Kooslus.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake nuppu Redigeeri.
9. Valige väljal Rea tüüp väärtus Kinnistatud tarne.
    * Kinnistatud tarne on valitud, et käivitada kanbani pakkumise loomine.  
10. Tehke väljal Ressursi tarbimine valik Ei.
    * Märkeruudu Ressursi tarbimine tühjendamist võimaldab meil ladu muuta.  
11. Laiendage jaotist Varude dimensioonid.
12. Sisestage väljale Ladu väärtus 12.
    * Ladu on seadistatud režiimile 12, sest see on tühistamistegevuse väljundi ladu.  
13. Tippige väljale Asukoht väärtus 12.
    * Asukohaks on seatud 12, sest see on tühistamistegevuse väljundi asukoht.  
14. Sulgege leht.
15. Sulgege leht.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Tootmistellimuse hindamine ja loodud kanbani kuvamine
1. Klõpsake suvandit Hinnang.
    * Tootmistellimuse hindamine käivitab seostatud kanbani loomise tarnekaubale M0001.  
2. Klõpsake nuppu OK.
3. Sulgege leht.
4. Sulgege leht.
5. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
6. Klõpsake loendis valitud real olevat linki.
    * Valige sündmuse kanban-reegel, mis on loodud kaubale M0001.  
7. Laiendage jaotist Kanbanid.
8. Märkige loendis valitud rida.
    * Pange tähele kanbani, mis on loodud M0001 tarneks hinnangulise tootmistellimuse jaoks.  
    * See on viimane etapp!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]