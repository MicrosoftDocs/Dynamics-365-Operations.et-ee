---
title: Koosluse arvutamine ühetasemelise struktuuri abil (veebruar 2016)
description: See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat üksiktaseme koosnemist.
author: AndersGirke
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5968631f5fed8a43cd63165a4ddff86e8cb4b4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572093"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Koosluse arvutamine ühetasemelise struktuuri abil (veebruar 2016)

[!include [banner](../../includes/banner.md)]

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
    * Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.    Siin on kulu koosseis:  *    10 tuletatakse üksusest ITEM_A, 10 üksusest ITEM_B, 10 üksusest BOM_2. Sellisel juhul pole BOM_2 jaoks üksikasju, kuna see sisestati 10 standardkuluna, kuid seda ei tehtud arvutuse kaudu.  *    7 tuletatakse häälestusajast, mis on püsikulu, ja täiendav 7 tuletatakse käitusaja toimingust (Protsess).  *    Samuti on olemas teised summad, mis vastavad kaudsetele kuludele.  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]