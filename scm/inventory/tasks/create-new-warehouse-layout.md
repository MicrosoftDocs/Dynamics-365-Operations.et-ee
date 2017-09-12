---
title: Uue laopaigutuse loomine
description: "Selles protseduuris näitlikustatakse, kuidas seadistada lao asukohtade teavet."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: et-ee
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="815a9-103">Uue laopaigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="815a9-103">Create a new warehouse layout</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="815a9-104">Selles protseduuris näitlikustatakse, kuidas seadistada lao asukohtade teavet.</span><span class="sxs-lookup"><span data-stu-id="815a9-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="815a9-105">See rakendub ainult ladudele, mis on loodud, kasutades üldist ladustamist moodulis Varude haldus, mitte nendele ladudele, mis on loodud moodulis Laohaldus.</span><span class="sxs-lookup"><span data-stu-id="815a9-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="815a9-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="815a9-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="815a9-107">Määrake asukoha vaikemahutavus</span><span class="sxs-lookup"><span data-stu-id="815a9-107">Set the default location capacity</span></span>
1. <span data-ttu-id="815a9-108">Avage Varude haldus > Seadistus > Varude ja lao halduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="815a9-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="815a9-109">Klõpsake vahekaarti Asukohad.</span><span class="sxs-lookup"><span data-stu-id="815a9-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="815a9-110">Sisestage arv väljale Standardlaius.</span><span class="sxs-lookup"><span data-stu-id="815a9-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="815a9-111">Sisestage arv väljale Standardmaht.</span><span class="sxs-lookup"><span data-stu-id="815a9-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="815a9-112">Sisestage arv väljale Standardkõrgus.</span><span class="sxs-lookup"><span data-stu-id="815a9-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="815a9-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="815a9-113">Click Save.</span></span>
7. <span data-ttu-id="815a9-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="815a9-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="815a9-115">Asukoha nime vormingu määratlemine</span><span class="sxs-lookup"><span data-stu-id="815a9-115">Define the location name format</span></span>
1. <span data-ttu-id="815a9-116">Avage Varude haldus > Seadistus > Laovarude jaotamine > Laod.</span><span class="sxs-lookup"><span data-stu-id="815a9-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="815a9-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="815a9-117">Click New.</span></span>
3. <span data-ttu-id="815a9-118">Sisestage väärtus väljale Ladu.</span><span class="sxs-lookup"><span data-stu-id="815a9-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="815a9-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="815a9-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="815a9-120">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="815a9-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="815a9-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="815a9-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="815a9-122">Lülitage ümber jaotis Asukoha nimed.</span><span class="sxs-lookup"><span data-stu-id="815a9-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="815a9-123">Selle jaotise suvandites saate määratleda asukohanimede vaikevormingu.</span><span class="sxs-lookup"><span data-stu-id="815a9-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="815a9-124">Selles näites on kasutatud riiulirea, sektsiooni ja riiuli numbrit.</span><span class="sxs-lookup"><span data-stu-id="815a9-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="815a9-125">Seadistage suvand Kaasa riiulirida väärtusele Jah.</span><span class="sxs-lookup"><span data-stu-id="815a9-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="815a9-126">Seadistage suvand Kaasa sektsioon väärtusele Jah.</span><span class="sxs-lookup"><span data-stu-id="815a9-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="815a9-127">Sisestage sektsiooni jaoks väärtus väljale Vorming.</span><span class="sxs-lookup"><span data-stu-id="815a9-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="815a9-128">Näide: ‑##</span><span class="sxs-lookup"><span data-stu-id="815a9-128">For example: -##</span></span>  
11. <span data-ttu-id="815a9-129">Seadistage suvand Kaasa riiul väärtusele Jah.</span><span class="sxs-lookup"><span data-stu-id="815a9-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="815a9-130">Sisestage riiuli jaoks väärtus väljale Vorming.</span><span class="sxs-lookup"><span data-stu-id="815a9-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="815a9-131">Näide: ‑##</span><span class="sxs-lookup"><span data-stu-id="815a9-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="815a9-132">Lao asukohtade määratlemine</span><span class="sxs-lookup"><span data-stu-id="815a9-132">Define warehouse locations</span></span>
1. <span data-ttu-id="815a9-133">Klõpsake toimingupaanil valikut Ladu.</span><span class="sxs-lookup"><span data-stu-id="815a9-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="815a9-134">Klõpsake Asukohaviisardit.</span><span class="sxs-lookup"><span data-stu-id="815a9-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="815a9-135">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-135">Click Next.</span></span>
4. <span data-ttu-id="815a9-136">Tühistage suvand Lähetusalad</span><span class="sxs-lookup"><span data-stu-id="815a9-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="815a9-137">Tühistage suvand Hulgiasukohad</span><span class="sxs-lookup"><span data-stu-id="815a9-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="815a9-138">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-138">Click Next.</span></span>
7. <span data-ttu-id="815a9-139">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-139">Click Next.</span></span>
8. <span data-ttu-id="815a9-140">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-140">Click Next.</span></span>
9. <span data-ttu-id="815a9-141">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-141">Click Next.</span></span>
10. <span data-ttu-id="815a9-142">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-142">Click Next.</span></span>
11. <span data-ttu-id="815a9-143">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-143">Click Next.</span></span>
12. <span data-ttu-id="815a9-144">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-144">Click Next.</span></span>
    * <span data-ttu-id="815a9-145">Pange tähele, et sellel lehel kuvatavad füüsilised dimensioonid on need, mille te selle protseduuri alguses seadistasite.</span><span class="sxs-lookup"><span data-stu-id="815a9-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="815a9-146">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="815a9-146">Click Next.</span></span>
14. <span data-ttu-id="815a9-147">Klõpsake Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="815a9-147">Click Finish.</span></span>
15. <span data-ttu-id="815a9-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="815a9-148">Close the page.</span></span>
16. <span data-ttu-id="815a9-149">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="815a9-149">Refresh the page.</span></span>

