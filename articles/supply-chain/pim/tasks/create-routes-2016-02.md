---
title: Protsesside loomine (veebruar 2016)
description: See ülesanne keskendub valmistoote ja pooltoote jaoks tootmisprotsesside loomisele.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "354088"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="ab17b-103">Protsesside loomine (veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="ab17b-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab17b-104">See ülesanne keskendub valmistoote ja pooltoote jaoks tootmisprotsesside loomisele.</span><span class="sxs-lookup"><span data-stu-id="ab17b-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="ab17b-105">See on viies ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="ab17b-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="ab17b-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ab17b-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="ab17b-107">Marsruudi loomine pooleldi lõpetatud tootele</span><span class="sxs-lookup"><span data-stu-id="ab17b-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="ab17b-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="ab17b-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ab17b-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ab17b-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ab17b-110">Valige kaubakood BOM_2.</span><span class="sxs-lookup"><span data-stu-id="ab17b-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="ab17b-111">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="ab17b-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="ab17b-112">Klõpsake valikut Protsess.</span><span class="sxs-lookup"><span data-stu-id="ab17b-112">Click Route.</span></span>
5. <span data-ttu-id="ab17b-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ab17b-113">Click New.</span></span>
6. <span data-ttu-id="ab17b-114">Klõpsake nuppu Protsess ja protsessi versioon.</span><span class="sxs-lookup"><span data-stu-id="ab17b-114">Click Route and route version.</span></span>
7. <span data-ttu-id="ab17b-115">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ab17b-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ab17b-116">Näiteks tippige ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="ab17b-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="ab17b-117">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="ab17b-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ab17b-118">Selles snäites sisestage või valige Sait 1.</span><span class="sxs-lookup"><span data-stu-id="ab17b-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="ab17b-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ab17b-119">Click OK.</span></span>
10. <span data-ttu-id="ab17b-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ab17b-120">Click New.</span></span>
11. <span data-ttu-id="ab17b-121">Sisestage või valige väärtus väljal Toiming.</span><span class="sxs-lookup"><span data-stu-id="ab17b-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="ab17b-122">Selles näites valige Assembler.</span><span class="sxs-lookup"><span data-stu-id="ab17b-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="ab17b-123">Sisestage number väljale Käitusaeg.</span><span class="sxs-lookup"><span data-stu-id="ab17b-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="ab17b-124">Tippige näiteks 1.</span><span class="sxs-lookup"><span data-stu-id="ab17b-124">For example, type 1.</span></span> <span data-ttu-id="ab17b-125">Käitusajad on sageli osa kauba puhul arvutatavast hinnast.</span><span class="sxs-lookup"><span data-stu-id="ab17b-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="ab17b-126">Sisestage või valige väärtus väljal Protsessigrupp.</span><span class="sxs-lookup"><span data-stu-id="ab17b-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="ab17b-127">Selles näites valige Std.</span><span class="sxs-lookup"><span data-stu-id="ab17b-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="ab17b-128">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="ab17b-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="ab17b-129">Sisestage või valige väärtus väljal Seadistuse kategooria.</span><span class="sxs-lookup"><span data-stu-id="ab17b-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="ab17b-130">Selles näites valige Assembler.</span><span class="sxs-lookup"><span data-stu-id="ab17b-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="ab17b-131">Klõpsake vahekaarti Ajad.</span><span class="sxs-lookup"><span data-stu-id="ab17b-131">Click the Times tab.</span></span>
17. <span data-ttu-id="ab17b-132">Väljale Häälestusaeg sisestage number.</span><span class="sxs-lookup"><span data-stu-id="ab17b-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="ab17b-133">Selles näites tippige 1.</span><span class="sxs-lookup"><span data-stu-id="ab17b-133">For this example, type 1.</span></span> <span data-ttu-id="ab17b-134">Häälestusajad on sageli osa hinnast, mis kauba puhul arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="ab17b-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="ab17b-135">Tegevuspaanil klõpsake nuppu Protsessi versioon.</span><span class="sxs-lookup"><span data-stu-id="ab17b-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="ab17b-136">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="ab17b-136">Click Approve.</span></span>
20. <span data-ttu-id="ab17b-137">Valikus Kas soovite ka protsessi kinnitada? tehke valik Jah. valik Jah.</span><span class="sxs-lookup"><span data-stu-id="ab17b-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="ab17b-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ab17b-138">Click OK.</span></span>
22. <span data-ttu-id="ab17b-139">Tegevuspaanil klõpsake nuppu Protsessi versioon.</span><span class="sxs-lookup"><span data-stu-id="ab17b-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="ab17b-140">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="ab17b-140">Click Activate.</span></span>
24. <span data-ttu-id="ab17b-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab17b-141">Close the page.</span></span>
25. <span data-ttu-id="ab17b-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab17b-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="ab17b-143">Marsruudi loomine lõpetatud tootele</span><span class="sxs-lookup"><span data-stu-id="ab17b-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="ab17b-144">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ab17b-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ab17b-145">Valige kaubakood BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ab17b-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="ab17b-146">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="ab17b-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="ab17b-147">Klõpsake valikut Protsess.</span><span class="sxs-lookup"><span data-stu-id="ab17b-147">Click Route.</span></span>
4. <span data-ttu-id="ab17b-148">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ab17b-148">Click New.</span></span>
5. <span data-ttu-id="ab17b-149">Klõpsake nuppu Protsess ja protsessi versioon.</span><span class="sxs-lookup"><span data-stu-id="ab17b-149">Click Route and route version.</span></span>
6. <span data-ttu-id="ab17b-150">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ab17b-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ab17b-151">Selles näites tippige ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="ab17b-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="ab17b-152">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="ab17b-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ab17b-153">Selles snäites sisestage või valige Sait 1.</span><span class="sxs-lookup"><span data-stu-id="ab17b-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="ab17b-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ab17b-154">Click OK.</span></span>
9. <span data-ttu-id="ab17b-155">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ab17b-155">Click New.</span></span>
10. <span data-ttu-id="ab17b-156">Sisestage või valige väärtus väljal Toiming.</span><span class="sxs-lookup"><span data-stu-id="ab17b-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="ab17b-157">Selles näites valige Pakkimine.</span><span class="sxs-lookup"><span data-stu-id="ab17b-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="ab17b-158">Sisestage number väljale Käitusaeg.</span><span class="sxs-lookup"><span data-stu-id="ab17b-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="ab17b-159">Selles näites tippige 1.</span><span class="sxs-lookup"><span data-stu-id="ab17b-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="ab17b-160">Sisestage või valige väärtus väljal Protsessigrupp.</span><span class="sxs-lookup"><span data-stu-id="ab17b-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="ab17b-161">Selles näites valige Std.</span><span class="sxs-lookup"><span data-stu-id="ab17b-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="ab17b-162">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="ab17b-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="ab17b-163">Sisestage või valige väärtus väljal Seadistuse kategooria.</span><span class="sxs-lookup"><span data-stu-id="ab17b-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="ab17b-164">Selles näites valige Pakkimine.</span><span class="sxs-lookup"><span data-stu-id="ab17b-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="ab17b-165">Klõpsake vahekaarti Ajad.</span><span class="sxs-lookup"><span data-stu-id="ab17b-165">Click the Times tab.</span></span>
16. <span data-ttu-id="ab17b-166">Väljale Häälestusaeg sisestage number.</span><span class="sxs-lookup"><span data-stu-id="ab17b-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="ab17b-167">Selles näites tippige 1.</span><span class="sxs-lookup"><span data-stu-id="ab17b-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="ab17b-168">Tegevuspaanil klõpsake nuppu Protsessi versioon.</span><span class="sxs-lookup"><span data-stu-id="ab17b-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="ab17b-169">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="ab17b-169">Click Approve.</span></span>
19. <span data-ttu-id="ab17b-170">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ab17b-170">Click OK.</span></span>
20. <span data-ttu-id="ab17b-171">Tegevuspaanil klõpsake nuppu Protsessi versioon.</span><span class="sxs-lookup"><span data-stu-id="ab17b-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="ab17b-172">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="ab17b-172">Click Activate.</span></span>
22. <span data-ttu-id="ab17b-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab17b-173">Close the page.</span></span>
23. <span data-ttu-id="ab17b-174">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab17b-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="ab17b-175">Häälestusaja automaatse tarbimise lubamine</span><span class="sxs-lookup"><span data-stu-id="ab17b-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="ab17b-176">Avage Tootmise juhtimine > Häälestamine > Marsruudid > Protsessigrupid.</span><span class="sxs-lookup"><span data-stu-id="ab17b-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="ab17b-177">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ab17b-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ab17b-178">Valige loendist Std.</span><span class="sxs-lookup"><span data-stu-id="ab17b-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="ab17b-179">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="ab17b-179">Click Edit.</span></span>
4. <span data-ttu-id="ab17b-180">Väljal Häälestusaeg valige Jah.</span><span class="sxs-lookup"><span data-stu-id="ab17b-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="ab17b-181">Häälestusajad on sageli osa hinnast, mis kauba puhul arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="ab17b-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="ab17b-182">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ab17b-182">Click Save.</span></span>
6. <span data-ttu-id="ab17b-183">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab17b-183">Close the page.</span></span>

