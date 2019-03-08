---
title: Alltöövõtu tööraku loomine - lean manufacturing
description: Lean manufacturing tööde alltööde mudeli loomiseks peate looma tööraku, mis on seostatud tööd pakkuva hankijaga.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58b725af456f1a5c7f158f01ffe48a2d8cdf056b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "319151"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="46a91-103">Alltöövõtu tööraku loomine - lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="46a91-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46a91-104">Lean manufacturing tööde alltööde mudeli loomiseks peate looma tööraku, mis on seostatud tööd pakkuva hankijaga.</span><span class="sxs-lookup"><span data-stu-id="46a91-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="46a91-105">Alltöövõtu töörakk on lingitud hankijaga läbi ressursi seostamise hankija tüübiga.</span><span class="sxs-lookup"><span data-stu-id="46a91-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="46a91-106">Kui esitate selle salvestise USMF-i demoettevõttes, saate valida hankija konto ID 1002 ja saidi 1.</span><span class="sxs-lookup"><span data-stu-id="46a91-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="46a91-107">Looge hankija ressurss</span><span class="sxs-lookup"><span data-stu-id="46a91-107">Create a vendor resource</span></span>
1. <span data-ttu-id="46a91-108">Avage Ressursid.</span><span class="sxs-lookup"><span data-stu-id="46a91-108">Go to Resources.</span></span>
2. <span data-ttu-id="46a91-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="46a91-109">Click New.</span></span>
3. <span data-ttu-id="46a91-110">Sisestage väärtus väljale Ressurss.</span><span class="sxs-lookup"><span data-stu-id="46a91-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="46a91-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="46a91-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="46a91-112">Valige väljal Tüüp valik Hankija.</span><span class="sxs-lookup"><span data-stu-id="46a91-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="46a91-113">Klõpsake väljal Hankija otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="46a91-114">Looge ressursigrupp</span><span class="sxs-lookup"><span data-stu-id="46a91-114">Create the resource group</span></span>
1. <span data-ttu-id="46a91-115">Avage Ressursigrupid.</span><span class="sxs-lookup"><span data-stu-id="46a91-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="46a91-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="46a91-116">Click New.</span></span>
3. <span data-ttu-id="46a91-117">Sisestage väärtus väljale Ressursigrupp.</span><span class="sxs-lookup"><span data-stu-id="46a91-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="46a91-118">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="46a91-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="46a91-119">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46a91-120">Valige sait, mille jaoks tuleb eraldada töörakk.</span><span class="sxs-lookup"><span data-stu-id="46a91-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="46a91-121">Teoreetiliselt võib said esindada ühte saiti, mida haldab hankija.</span><span class="sxs-lookup"><span data-stu-id="46a91-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="46a91-122">Siiski enamasti eraldatakse alltöövõturessursid ainult alltöövõtulepinguga tööd tellivale saidile.</span><span class="sxs-lookup"><span data-stu-id="46a91-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="46a91-123">Pange tähele, et alltöövõtu töörakkude sisend- ja väljundlaod peavad olema samal saidil.</span><span class="sxs-lookup"><span data-stu-id="46a91-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="46a91-124">Sisestage väärtus väljale Koht.</span><span class="sxs-lookup"><span data-stu-id="46a91-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="46a91-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="46a91-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="46a91-126">Valige või tühjendage märkeruut Töörakk.</span><span class="sxs-lookup"><span data-stu-id="46a91-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="46a91-127">Klõpsake väljal Sisestusladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46a91-128">Valige ladu ja asukoht, mida kasutatakse hankija hallatud tööraku materjalide jaoks.</span><span class="sxs-lookup"><span data-stu-id="46a91-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="46a91-129">Paljudel juhtudel esitatakse ladu ja asukoht nii, et iga hankija jaoks kasutatakse erinevat ladu ja iga tööraku jaoks kasutatakse ühte asukohta.</span><span class="sxs-lookup"><span data-stu-id="46a91-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="46a91-130">Klõpsake väljal Sisestuskoht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="46a91-131">Klõpsake väljal Väljastusladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46a91-132">Määrake ladu ja asukoht, kuhu materjal sisestatakse, kui sisestatakse tööraku alltöövõtu tegevused.</span><span class="sxs-lookup"><span data-stu-id="46a91-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="46a91-133">Ladu ja asukoht võivad olla hankija saidil, kui hankija raporteerib kanban-tööd.</span><span class="sxs-lookup"><span data-stu-id="46a91-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="46a91-134">Alternatiivina võivad ladu ja asukoht olla vastuvõtvas asukohas, mis on seostatud tootmisvoo järgmise etapiga.</span><span class="sxs-lookup"><span data-stu-id="46a91-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="46a91-135">Klõpsake väljal Väljastuskoht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="46a91-136">Laiendage või ahendage jaotist Kalendrid.</span><span class="sxs-lookup"><span data-stu-id="46a91-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="46a91-137">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="46a91-137">Click Add.</span></span>
15. <span data-ttu-id="46a91-138">Klõpsake väljal Kalender otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46a91-139">Seostage tööraku tööaja kalender ressursigrupiga.</span><span class="sxs-lookup"><span data-stu-id="46a91-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="46a91-140">Kriitiliste ressursside puhul soovitame teil määrata konkreetsed kalendrid, mis kujutavad tööraku või hankija saidi täpseid tööaegasid ja seotud võimekusi.</span><span class="sxs-lookup"><span data-stu-id="46a91-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="46a91-141">Laiendage või ahendage jaotist Ressursid.</span><span class="sxs-lookup"><span data-stu-id="46a91-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="46a91-142">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="46a91-142">Click Add.</span></span>
    * <span data-ttu-id="46a91-143">Alltöövõtu ressursigrupil peab olema vastava hankijatüübi seostatud ressurss, mis lingib ressursigrupi hankija kontoga.</span><span class="sxs-lookup"><span data-stu-id="46a91-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="46a91-144">Klõpsake väljal Ressurss otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46a91-145">Valige või sisestage hankijaressurss, mille olete loonud eelmises alamülesandes.</span><span class="sxs-lookup"><span data-stu-id="46a91-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="46a91-146">Laiendage või ahendage jaotist Tööraku võimsus.</span><span class="sxs-lookup"><span data-stu-id="46a91-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="46a91-147">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="46a91-147">Click Add.</span></span>
    * <span data-ttu-id="46a91-148">Töörakul peab olema määratletud võimsus.</span><span class="sxs-lookup"><span data-stu-id="46a91-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="46a91-149">Selles näites loome läbilaskevõime 100 ühikut standardse tööpäeva kohta.</span><span class="sxs-lookup"><span data-stu-id="46a91-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="46a91-150">Klõpsake väljal Tootmisvoo mudel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="46a91-151">Valige suvand väljalt Võimsuse periood.</span><span class="sxs-lookup"><span data-stu-id="46a91-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="46a91-152">Sisestage number väljale Keskmine läbilaskekogus.</span><span class="sxs-lookup"><span data-stu-id="46a91-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="46a91-153">Klõpsake väljal Ühik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="46a91-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="46a91-154">Ühiku toiming ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="46a91-154">ResolveChanges the Unit.</span></span>

