---
title: Koosluse arvutamine ühetasemelise struktuuri abil (veebruar 2016)
description: See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat üksiktaseme koosnemist.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f74f8e4efc4474693f0a5b543c1300c3b64ecda0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "361586"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="88417-103">Koosluse arvutamine ühetasemelise struktuuri abil (veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="88417-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88417-104">See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat üksiktaseme koosnemist.</span><span class="sxs-lookup"><span data-stu-id="88417-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="88417-105">See on kuues ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="88417-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="88417-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="88417-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="88417-107">Avage Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="88417-107">Go to Released products.</span></span>
2. <span data-ttu-id="88417-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="88417-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="88417-109">Valige toode BOM_1.</span><span class="sxs-lookup"><span data-stu-id="88417-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="88417-110">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="88417-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="88417-111">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="88417-111">Click Item price.</span></span>
5. <span data-ttu-id="88417-112">Klõpsake nuppu Kauba kulu arvutamine.</span><span class="sxs-lookup"><span data-stu-id="88417-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="88417-113">Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.</span><span class="sxs-lookup"><span data-stu-id="88417-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="88417-114">Klõpsake väljal Kuluversioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="88417-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="88417-115">Selle demo puhul valige 10.</span><span class="sxs-lookup"><span data-stu-id="88417-115">For this demo, select 10.</span></span> <span data-ttu-id="88417-116">See on sama kuluversioon, mida kasutatakse kuluhinna lisamiseks komponentidele.</span><span class="sxs-lookup"><span data-stu-id="88417-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="88417-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="88417-117">Click OK.</span></span>
8. <span data-ttu-id="88417-118">Klõpsake suvandit Kuva arvutamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="88417-118">Click View calculation details.</span></span>
    * <span data-ttu-id="88417-119">Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.</span><span class="sxs-lookup"><span data-stu-id="88417-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="88417-120">Siin on kulu koosseis: • 10 tuletatakse üksusest ITEM_A, 10 üksusest ITEM_B, 10 üksusest BOM_2.</span><span class="sxs-lookup"><span data-stu-id="88417-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="88417-121">Sellisel juhul pole BOM_2 jaoks üksikasju, kuna see sisestati 10 standardkuluna, kuid seda ei tehtud arvutuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="88417-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="88417-122">• 7 tuletatakse häälestusajast, mis on püsikulu, ja täiendav 7 tuletatakse käitusaja toimingust (Protsess).</span><span class="sxs-lookup"><span data-stu-id="88417-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="88417-123">• Samuti on olemas teised summad, mis vastavad kaudsetele kuludele.</span><span class="sxs-lookup"><span data-stu-id="88417-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="88417-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="88417-124">@SysTaskRecorder:_RequestClose</span></span>

