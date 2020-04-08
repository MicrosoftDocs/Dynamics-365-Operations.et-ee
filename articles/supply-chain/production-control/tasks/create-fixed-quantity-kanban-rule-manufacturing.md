---
title: Fikseeritud kogusega kanban-reegli loomine tootmise jaoks
description: See protseduur keskendub teisendustegevuste käivitamise eesmärgil fikseeritud tootmise kanban-reegli loomiseks vajalikele etappidele kulusäästliku keskkonna töörakus.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff38ba2ed1d513d6b64cf5a64e021cbb08d69b21
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161750"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Fikseeritud kogusega kanban-reegli loomine tootmise jaoks

[!include [banner](../../includes/banner.md)]

See protseduur keskendub teisendustegevuste käivitamise eesmärgil fikseeritud tootmise kanban-reegli loomiseks vajalikele etappidele kulusäästliku keskkonna töörakus. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Protseduur on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist.


## <a name="create-new-kanban-rule"></a>Uue kanban-reegli loomine
1. Minge jaotisse Kanban-reeglid.
2. Klõpsake valikut Uus.
    * Pange tähele, et suvandi Tüüp vaikesäte on Tootmine ja suvandi Täiendusstrateegia vaikesäte on Fikseeritud. Te ei pea neid parameetreid muutma.  
3. Sisestage või valige väärtus väljal Esimene plaanitegevus.
    * See on tegevus, mis teostatakse selle kanban-reegli põhjal loodud kanbanide puhul.  Valige suvand SpeakerTestAndPackaging.  
4. Laiendage jaotist Üksikasjad.
5. Sisestage või valige väärtus väljal Toode.
    * Valige suvand L0050.  
6. Sisestage või valige väärtus väljal Mõõtühik.
    * Valige minutid.  
7. Sisestage number väljale Täitmisaeg.
    * Sisestage väärtus 5.  

## <a name="set-quantities"></a>Koguste määramine
1. Laiendage jaotist Kogused.
2. Valige välja Vaikekogus väärtuseks 10.
    * See on iga kanbani kohta üle kantav kogus.  
3. Märkige ruut Toote koguse hälve.
    * Sellega saab valitud kanbanid lõpule viia hälbega vaikekogusest.  Selleks ei võimaldada kanbanid lõpule viia kogusega 8 kuni 12, määrake mõlema hälbe väärtuseks 2.  
4. Valige välja Hälve alla väärtuseks 2.
    * See võimaldab allapoole lõpuleviimist 10 – 2 = 8  
5. Valige välja Hälve üle väärtuseks 2.
    * See võimaldab ülespoole lõpule viimist 10 + 2 = 12  
6. Sisestage number väljale Fikseeritud kanban-kogus.
    * See on kanbanide, mis peaksid olema aktiivsed, arv. Sel juhul töötlevad viiest kanbanist igaüks kümmet.  
7. Sisestage väljale Teatise miinimumpiir väärtus 2.
    * Kasutatakse täielike kanbanide, mis peaks olema sihtkohas, minimaalse summa jälgimiseks. Näiteks kasutatakse seda kanban-koguse ülevaates.  
8. Sisestage väljale Teatise maksimumpiir väärtus 4.
    * Kasutatakse täielike kanbanide, mis peaks olema sihtkohas, maksimaalse summa jälgimiseks. Näiteks kasutatakse seda kanban-koguse ülevaates.  
9. Sisestage väljale Automaatse plaanimise kogus väärtus 1.
    * Kui valite selle väärtuseks 1, plaanitakse iga kanban automaatselt.   Kui valite väärtuseks 3, ei plaanita kanbane enne, kui 3 tühja kanbani on plaanimiseks valmis. See on kasulik töö grupeerimiseks ja liiga paljude etappide vältimiseks.  

## <a name="create-kanbans"></a>Kanbanide loomine
1. Laiendage jaotist Kanbanid.
2. Klõpsake nuppu Salvesta.
    * Enne, kui kanbane saab luua, tuleb kanban-reegel salvestada.  
3. Klõpsake vahekaarti Lisa.
    * Pange tähele, et aktiivseid kanbane ei ole, seetõttu on välja "Uute kanbanide arv" soovitatav väärtus 5. See on võrdne väärtusega "Fikseeritud kanban-kogus".  
4. Klõpsake käsku Loo.
    * See loob 5 kanbani.  
    * Pange tähele, et selle tootmise kanban-reegli puhul loodi 5 kanbani, igaühe kohta 10. See on selle protseduuri viimane etapp.  

