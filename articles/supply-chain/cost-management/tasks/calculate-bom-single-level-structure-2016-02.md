---
title: Koosluse arvutamine ühetasemelise struktuuri abil (veebruar 2016)
description: See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat üksiktaseme koosnemist.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7c2c34474cada787b7a7ba720ba177aa8dc125f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214341"
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

