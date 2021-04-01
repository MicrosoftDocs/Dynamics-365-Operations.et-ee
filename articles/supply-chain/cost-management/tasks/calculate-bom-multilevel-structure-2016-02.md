---
title: Koosluse arvutamine mitmetasandilise struktuuri abil (veebruar 2016)
description: See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat mitmetasandilist koosnevust.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbbc1e3c7941fd12991f1f6eaec4e9daf35fde9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239498"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="9779f-103">Koosluse arvutamine mitmetasandilise struktuuri abil (veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="9779f-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9779f-104">See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat mitmetasandilist koosnevust.</span><span class="sxs-lookup"><span data-stu-id="9779f-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="9779f-105">See on seitsmes ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="9779f-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="9779f-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="9779f-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="9779f-107">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="9779f-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="9779f-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9779f-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9779f-109">Valige toode BOM_1.</span><span class="sxs-lookup"><span data-stu-id="9779f-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="9779f-110">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="9779f-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="9779f-111">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="9779f-111">Click Item price.</span></span>
5. <span data-ttu-id="9779f-112">Klõpsake nuppu Kauba kulu arvutamine.</span><span class="sxs-lookup"><span data-stu-id="9779f-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="9779f-113">Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.</span><span class="sxs-lookup"><span data-stu-id="9779f-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="9779f-114">Väljal Kuluversioon sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="9779f-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="9779f-115">Valige kuluversioon 20, kuna see on kulutüüp Plaanitud ja režiim Koosnemine on Mitmetasemeline.</span><span class="sxs-lookup"><span data-stu-id="9779f-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="9779f-116">Mitmetasandilise koosnevuse režiim on mõeldud plaanitud kuludele ja simulatsioonidele.</span><span class="sxs-lookup"><span data-stu-id="9779f-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="9779f-117">Seda ei kasutata standardkulu jaoks.</span><span class="sxs-lookup"><span data-stu-id="9779f-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="9779f-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9779f-118">Click OK.</span></span>
8. <span data-ttu-id="9779f-119">Klõpsake suvandit Kuva arvutamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="9779f-119">Click View calculation details.</span></span>
    * <span data-ttu-id="9779f-120">Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.</span><span class="sxs-lookup"><span data-stu-id="9779f-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="9779f-121">Sellisel juhul pange tähele, kuidas BOM_2 on arvutatud, arvestades seeria algses tegevusejuhises aktiveeritud standardkulu 10 asemel toormaterjali, protsessi ja üldkulusid kogusummas 29,40.</span><span class="sxs-lookup"><span data-stu-id="9779f-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="9779f-122">Klõpsake vahekaarti Kuluarvutustabel.</span><span class="sxs-lookup"><span data-stu-id="9779f-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="9779f-123">Liikudes vahekaardile Kuluarvutustabel, on kogusummad kulugrupi kohta eelmises tegevusejuhises tehtud arvutusega võrreldes erinevad.</span><span class="sxs-lookup"><span data-stu-id="9779f-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="9779f-124">Väljal Tase valige Mitu.</span><span class="sxs-lookup"><span data-stu-id="9779f-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="9779f-125">Valides suvandi Mitu, klassifitseeritakse kulud BOM_2 koosnevuse järgi, kus 10 tuletatakse M1 kulugrupist (ITEM_C) ja 15,60 tuletatakse selle tootmisest, kus kulugrupp on L2.</span><span class="sxs-lookup"><span data-stu-id="9779f-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="9779f-126">Kaudsed kulud varieeruvad samuti.</span><span class="sxs-lookup"><span data-stu-id="9779f-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="9779f-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9779f-127">Close the page.</span></span>
12. <span data-ttu-id="9779f-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9779f-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]