--- 
title: "Koosluse arvutamine ühetasandilise struktuuri abil (ainult veebruar 2016)"
description: "See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat üksiktaseme koosnemist."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e6829238b244cc01b070fde6acdf37bdaeb9670
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a>Koosluse arvutamine ühetasandilise struktuuri abil (ainult veebruar 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat üksiktaseme koosnemist. See on kuues ülesanne koosluse arvutamise seerias. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.

1. Avage Väljastatud tooted.
2. Otsige loendist ja valige soovitud kirje.
    * Valige toode BOM_1.  
3. Klõpsake toimingupaanil valikut Kulude haldamine.
4. Klõpsake nuppu Kauba hind.
5. Klõpsake nuppu Kauba kulu arvutamine.
    * Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.  
6. Klõpsake väljal Kuluversioon otsingu avamiseks ripploendi nuppu.
    * Selle demo puhul valige 10. See on sama kuluversioon, mida kasutatakse kuluhinna lisamiseks komponentidele.  
7. Klõpsake nuppu OK.
8. Klõpsake suvandit Kuva arvutamise üksikasjad.
    * Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.    Siin on kulu koosseis: • 10 tuletatakse üksusest ITEM_A, 10 üksusest ITEM_B, 10 üksusest BOM_2. Sellisel juhul pole BOM_2 jaoks üksikasju, kuna see sisestati 10 standardkuluna, kuid seda ei tehtud arvutuse kaudu.  • 7 tuletatakse häälestusajast, mis on püsikulu, ja täiendav 7 tuletatakse käitusaja toimingust (Protsess).  • Samuti on olemas teised summad, mis vastavad kaudsetele kuludele.  
9. @SysTaskRecorder:_RequestClose


