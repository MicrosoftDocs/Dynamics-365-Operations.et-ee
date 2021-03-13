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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36f908e02c996c0d0a636fd9295b84fcc16b6b63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011768"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="959b5-103">Koosluse arvutamine ühetasemelise struktuuri abil (veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="959b5-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="959b5-104">See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat üksiktaseme koosnemist.</span><span class="sxs-lookup"><span data-stu-id="959b5-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="959b5-105">See on kuues ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="959b5-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="959b5-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="959b5-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="959b5-107">Avage Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="959b5-107">Go to Released products.</span></span>
2. <span data-ttu-id="959b5-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="959b5-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="959b5-109">Valige toode BOM_1.</span><span class="sxs-lookup"><span data-stu-id="959b5-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="959b5-110">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="959b5-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="959b5-111">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="959b5-111">Click Item price.</span></span>
5. <span data-ttu-id="959b5-112">Klõpsake nuppu Kauba kulu arvutamine.</span><span class="sxs-lookup"><span data-stu-id="959b5-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="959b5-113">Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.</span><span class="sxs-lookup"><span data-stu-id="959b5-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="959b5-114">Klõpsake väljal Kuluversioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="959b5-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="959b5-115">Selle demo puhul valige 10.</span><span class="sxs-lookup"><span data-stu-id="959b5-115">For this demo, select 10.</span></span> <span data-ttu-id="959b5-116">See on sama kuluversioon, mida kasutatakse kuluhinna lisamiseks komponentidele.</span><span class="sxs-lookup"><span data-stu-id="959b5-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="959b5-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="959b5-117">Click OK.</span></span>
8. <span data-ttu-id="959b5-118">Klõpsake suvandit Kuva arvutamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="959b5-118">Click View calculation details.</span></span>
    * <span data-ttu-id="959b5-119">Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.</span><span class="sxs-lookup"><span data-stu-id="959b5-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="959b5-120">Siin on kulu koosseis:  \*    10 tuletatakse üksusest ITEM_A, 10 üksusest ITEM_B, 10 üksusest BOM_2.</span><span class="sxs-lookup"><span data-stu-id="959b5-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="959b5-121">Sellisel juhul pole BOM_2 jaoks üksikasju, kuna see sisestati 10 standardkuluna, kuid seda ei tehtud arvutuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="959b5-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="959b5-122">\*    7 tuletatakse häälestusajast, mis on püsikulu, ja täiendav 7 tuletatakse käitusaja toimingust (Protsess).</span><span class="sxs-lookup"><span data-stu-id="959b5-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="959b5-123">\*    Samuti on olemas teised summad, mis vastavad kaudsetele kuludele.</span><span class="sxs-lookup"><span data-stu-id="959b5-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="959b5-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="959b5-124">@SysTaskRecorder:_RequestClose</span></span>

