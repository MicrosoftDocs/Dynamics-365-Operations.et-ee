---
title: 'Ülekandmistegevuste loomine: lean manufacturing'
description: Ülekandetegevuse loomine lean manufacturingi jaoks.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae31cca96825665f9482b4523b66586415504b65
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210797"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="6481e-103">Ülekandmistegevuste loomine: lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="6481e-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6481e-104">Ülekandetegevuse loomine lean manufacturingi jaoks.</span><span class="sxs-lookup"><span data-stu-id="6481e-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="6481e-105">Eeltingimused:</span><span class="sxs-lookup"><span data-stu-id="6481e-105">Prerequisites:</span></span> 

1. <span data-ttu-id="6481e-106">Tuleb luua tootmisvoog ja mitteaktiivne versioon.</span><span class="sxs-lookup"><span data-stu-id="6481e-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="6481e-107">Tuleb luua saate- ja vastuvõtulaod ja asukohad.</span><span class="sxs-lookup"><span data-stu-id="6481e-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="6481e-108">Soovi korral saate luua täiendava või täiendatud tööraku.</span><span class="sxs-lookup"><span data-stu-id="6481e-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="6481e-109">Tootmisvoo versiooni leidmine</span><span class="sxs-lookup"><span data-stu-id="6481e-109">Find the production flow version</span></span>
1. <span data-ttu-id="6481e-110">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="6481e-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="6481e-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6481e-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6481e-112">Pange tähele, et tootmisvool peab olema mustandolekus versioon.</span><span class="sxs-lookup"><span data-stu-id="6481e-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="6481e-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6481e-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="6481e-114">Uue tegevuse loomine</span><span class="sxs-lookup"><span data-stu-id="6481e-114">Create a new activity</span></span>
1. <span data-ttu-id="6481e-115">Klõpsake suvandit Tegevused.</span><span class="sxs-lookup"><span data-stu-id="6481e-115">Click Activities.</span></span>
    * <span data-ttu-id="6481e-116">Veenduge, et valitud tootmisvool oleks mustandversioon, ja valige see versioon.</span><span class="sxs-lookup"><span data-stu-id="6481e-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="6481e-117">Klõpsake suvandit Uue plaanitegevuse loomine.</span><span class="sxs-lookup"><span data-stu-id="6481e-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="6481e-118">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="6481e-118">Click Next.</span></span>
4. <span data-ttu-id="6481e-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="6481e-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6481e-120">Valige väljal Tegevuse tüüp suvand Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="6481e-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="6481e-121">Sisestage number väljale Protsessikogus.</span><span class="sxs-lookup"><span data-stu-id="6481e-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="6481e-122">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="6481e-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="6481e-123">Töörakkude valimine</span><span class="sxs-lookup"><span data-stu-id="6481e-123">Select the Work cells</span></span>
1. <span data-ttu-id="6481e-124">Klõpsake väljal Täiendamine otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6481e-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6481e-125">Tööraku väljundasukoha kasutamiseks ülekandetegevuse lähteasukohana valige töörakk.</span><span class="sxs-lookup"><span data-stu-id="6481e-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="6481e-126">Sama saab teha täiendatud töörakuga, mis määrab ülekandetegevuse sihtasukoha.</span><span class="sxs-lookup"><span data-stu-id="6481e-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="6481e-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6481e-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="6481e-128">Laovarude värskenduste määratlemine</span><span class="sxs-lookup"><span data-stu-id="6481e-128">Define the inventory updates</span></span>
1. <span data-ttu-id="6481e-129">Valige suvand väljal Toote tüüp.</span><span class="sxs-lookup"><span data-stu-id="6481e-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="6481e-130">Pange tähele, et ülekanne ei muuda toote tüüpi.</span><span class="sxs-lookup"><span data-stu-id="6481e-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="6481e-131">Saate valmistooted või pooltooted üle kanda (ülekanne tootmisvoo ja võib-olla ka kanban-voo kahe tegevuse vahel).</span><span class="sxs-lookup"><span data-stu-id="6481e-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="6481e-132">Valmistoodete ülekandmisel saate valida varude ülekandes komplekteerimise või vastuvõtmise tulemused.</span><span class="sxs-lookup"><span data-stu-id="6481e-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="6481e-133">Ülekande asukohtade määratlemine</span><span class="sxs-lookup"><span data-stu-id="6481e-133">Define the transfer locations</span></span>
1. <span data-ttu-id="6481e-134">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="6481e-134">Click Next.</span></span>
2. <span data-ttu-id="6481e-135">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6481e-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6481e-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6481e-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6481e-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6481e-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6481e-138">Klõpsake väljal Asukoht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6481e-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6481e-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6481e-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6481e-140">Valige väljal Lastija suvand Saatja.</span><span class="sxs-lookup"><span data-stu-id="6481e-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="6481e-141">Suvandid hõlmavad järgmist: saatja – tarneladu juhtiv organisatsioon, saaja – vastuvõtvat ladu juhtiv organisatsioon, vedaja – muu osapoole hankija.</span><span class="sxs-lookup"><span data-stu-id="6481e-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="6481e-142">Kui juhtiv organisatsioon on hankija, nõuab ülekandetegevus allhankelepingut.</span><span class="sxs-lookup"><span data-stu-id="6481e-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="6481e-143">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="6481e-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="6481e-144">Tegevusaegade määratlemine</span><span class="sxs-lookup"><span data-stu-id="6481e-144">Define the activity times</span></span>
1. <span data-ttu-id="6481e-145">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6481e-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6481e-146">Vajalik on Käitusaja määratlus.</span><span class="sxs-lookup"><span data-stu-id="6481e-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="6481e-147">Käitusaega kasutatakse kanban-tööde maksumuse ja läbilaskeaegade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="6481e-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="6481e-148">Käitusaegu ei kasutata täiskoormuse ja tarbimise arvutamiseks; neid arvutatakse tsükliaja järgi, mis saadakse tootmisvoo versiooni ülesandest.</span><span class="sxs-lookup"><span data-stu-id="6481e-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="6481e-149">Sisestage number väljale Kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="6481e-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="6481e-150">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="6481e-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="6481e-151">Valige ajaühik.</span><span class="sxs-lookup"><span data-stu-id="6481e-151">Select the Time unit.</span></span>
5. <span data-ttu-id="6481e-152">Sisestage number väljale Koguse kohta.</span><span class="sxs-lookup"><span data-stu-id="6481e-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="6481e-153">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6481e-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6481e-154">Ooteajad on valikulised.</span><span class="sxs-lookup"><span data-stu-id="6481e-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="6481e-155">Sisestage number väljale Kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="6481e-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="6481e-156">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="6481e-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="6481e-157">Valige ajaühik.</span><span class="sxs-lookup"><span data-stu-id="6481e-157">Select the Time unit.</span></span>
10. <span data-ttu-id="6481e-158">Sisestage number väljale Koguse kohta.</span><span class="sxs-lookup"><span data-stu-id="6481e-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="6481e-159">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="6481e-159">Click Next.</span></span>
12. <span data-ttu-id="6481e-160">Klõpsake Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="6481e-160">Click Finish.</span></span>
13. <span data-ttu-id="6481e-161">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6481e-161">Close the page.</span></span>

