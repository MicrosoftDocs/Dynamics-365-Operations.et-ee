---
title: 'Protsessitegevuste loomine: lean manufacturing'
description: Protsessitegevuse loomine lean manufacturingi jaoks.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb8068012453fd4a8b06dea8cc8e5067d6968fe3
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826595"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="06b39-103">Protsessitegevuste loomine: lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="06b39-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06b39-104">Protsessitegevuse loomine lean manufacturingi jaoks.</span><span class="sxs-lookup"><span data-stu-id="06b39-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="06b39-105">Eeltingimused:</span><span class="sxs-lookup"><span data-stu-id="06b39-105">Prerequisites:</span></span> 

1. <span data-ttu-id="06b39-106">Tuleb luua tootmisvoog ja mitteaktiivne versioon.</span><span class="sxs-lookup"><span data-stu-id="06b39-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="06b39-107">Tuleb luua töörakk.</span><span class="sxs-lookup"><span data-stu-id="06b39-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="06b39-108">Tootmisvoo versiooni leidmine</span><span class="sxs-lookup"><span data-stu-id="06b39-108">Find the production flow version</span></span>
1. <span data-ttu-id="06b39-109">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="06b39-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="06b39-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="06b39-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="06b39-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="06b39-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="06b39-112">Uue tegevuse loomine</span><span class="sxs-lookup"><span data-stu-id="06b39-112">Create a new activity</span></span>
1. <span data-ttu-id="06b39-113">Klõpsake suvandit Tegevused.</span><span class="sxs-lookup"><span data-stu-id="06b39-113">Click Activities.</span></span>
    * <span data-ttu-id="06b39-114">Veenduge, et valitud tootmisvool oleks mustandversioon, ja valige see versioon.</span><span class="sxs-lookup"><span data-stu-id="06b39-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="06b39-115">Klõpsake suvandit Uue plaanitegevuse loomine.</span><span class="sxs-lookup"><span data-stu-id="06b39-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="06b39-116">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="06b39-116">Click Next.</span></span>
4. <span data-ttu-id="06b39-117">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="06b39-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="06b39-118">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="06b39-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="06b39-119">Pange tähele, et nimi peab kõnealuse tootmisvoo kõigi versioonide puhul olema kordumatu.</span><span class="sxs-lookup"><span data-stu-id="06b39-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="06b39-120">Sisestage number väljale Protsessikogus.</span><span class="sxs-lookup"><span data-stu-id="06b39-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="06b39-121">Pange tähele, et olenemata töödeldavast töökogusest on see tööjõukulu arvutamiseks minimaalne kogus iga töö kohta.</span><span class="sxs-lookup"><span data-stu-id="06b39-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="06b39-122">Kui töökogused sellest kogusest hälbivad, luuakse tööjõuhälve.</span><span class="sxs-lookup"><span data-stu-id="06b39-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="06b39-123">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="06b39-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="06b39-124">Tööraku valimine</span><span class="sxs-lookup"><span data-stu-id="06b39-124">Select the work cell</span></span>
1. <span data-ttu-id="06b39-125">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="06b39-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="06b39-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="06b39-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="06b39-127">Laovarude värskenduste määratlemine</span><span class="sxs-lookup"><span data-stu-id="06b39-127">Define the inventory updates</span></span>
1. <span data-ttu-id="06b39-128">Märkige või tühjendage ruut Värskenda laoseisu sissetulekut.</span><span class="sxs-lookup"><span data-stu-id="06b39-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="06b39-129">Kui suvandi Laoseisu värskendamine sätteks on valitud Ei, saate määratleda tegevuse vastu võtma pooltoodet (tegevus ei jõua järgmisele kooslusetasemele).</span><span class="sxs-lookup"><span data-stu-id="06b39-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="06b39-130">Saate valida ka pooltoodete tarbimise.</span><span class="sxs-lookup"><span data-stu-id="06b39-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="06b39-131">Komplekteerimistegevuste määratlemine</span><span class="sxs-lookup"><span data-stu-id="06b39-131">Define the picking activities</span></span>
1. <span data-ttu-id="06b39-132">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="06b39-132">Click Next.</span></span>
2. <span data-ttu-id="06b39-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="06b39-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="06b39-134">Valitud tööraku sisendasukoha kohta luuakse vaikekomplekteerimistegevus.</span><span class="sxs-lookup"><span data-stu-id="06b39-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="06b39-135">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="06b39-135">Click Add.</span></span>
    * <span data-ttu-id="06b39-136">Saate luua kindlate toodete puhul täiendavaid komplekteerimistegevusi, mis ei ole tööraku sisendtegevuses etapiviisilised.</span><span class="sxs-lookup"><span data-stu-id="06b39-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="06b39-137">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="06b39-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="06b39-138">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="06b39-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="06b39-139">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="06b39-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="06b39-140">Selle määratlusega komplekteeritakse kõik tegevuses tarbitavad materjalid vaikesisendlaost ja -asukohast, v.a kaup, mis määratletakse teises komplekteerimistegevuses.</span><span class="sxs-lookup"><span data-stu-id="06b39-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="06b39-141">See kaup komplekteeritakse teisest laost ja asukohast.</span><span class="sxs-lookup"><span data-stu-id="06b39-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="06b39-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="06b39-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="06b39-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="06b39-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="06b39-144">Märkige või tühjendage ruut Registreeri praak.</span><span class="sxs-lookup"><span data-stu-id="06b39-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="06b39-145">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="06b39-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="06b39-146">Tegevusaegade määratlemine</span><span class="sxs-lookup"><span data-stu-id="06b39-146">Define the activity times</span></span>
1. <span data-ttu-id="06b39-147">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="06b39-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="06b39-148">Vajalik on Käitusaja määratlus.</span><span class="sxs-lookup"><span data-stu-id="06b39-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="06b39-149">Käitusaega kasutatakse kanban-tööde maksumuse ja läbilaskeaegade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="06b39-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="06b39-150">Käitusaegu ei kasutata täiskoormuse ja tarbimise arvutamiseks; neid arvutatakse tsükliaja järgi, mis saadakse tootmisvoo versiooni ülesandest.</span><span class="sxs-lookup"><span data-stu-id="06b39-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="06b39-151">Sisestage number väljale Kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="06b39-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="06b39-152">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="06b39-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="06b39-153">Valige ajaühik.</span><span class="sxs-lookup"><span data-stu-id="06b39-153">Select the Time unit.</span></span>
5. <span data-ttu-id="06b39-154">Sisestage number väljale Koguse kohta.</span><span class="sxs-lookup"><span data-stu-id="06b39-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="06b39-155">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="06b39-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="06b39-156">Ooteajad on valikulised.</span><span class="sxs-lookup"><span data-stu-id="06b39-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="06b39-157">Sisestage number väljale Kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="06b39-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="06b39-158">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="06b39-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="06b39-159">Valige ajaühik.</span><span class="sxs-lookup"><span data-stu-id="06b39-159">Select the Time unit.</span></span>
10. <span data-ttu-id="06b39-160">Sisestage number väljale Koguse kohta.</span><span class="sxs-lookup"><span data-stu-id="06b39-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="06b39-161">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="06b39-161">Click Next.</span></span>
12. <span data-ttu-id="06b39-162">Klõpsake Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="06b39-162">Click Finish.</span></span>
13. <span data-ttu-id="06b39-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="06b39-163">Close the page.</span></span>

