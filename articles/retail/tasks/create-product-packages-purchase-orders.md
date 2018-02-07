--- 
title: " Tootepakendite loomine ostutellimuste jaoks"
description: See protseduur selgitab tootepaketi loomist ja ostutellimusel kasutamist.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: d89744a4dbe52d201dc370b5cde151cc579508ea
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="5ae8f-103"> Tootepakendite loomine ostutellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="5ae8f-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5ae8f-104">See protseduur selgitab tootepaketi loomist ja ostutellimusel kasutamist.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="5ae8f-105">Ostutellimust kasutatakse tellimuse loomiseks eelmääratletud tootekogumi kohta.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="5ae8f-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="5ae8f-107">Tootepaketi loomine</span><span class="sxs-lookup"><span data-stu-id="5ae8f-107">Create a product package</span></span>
1. <span data-ttu-id="5ae8f-108">Avage Jaemüük ja kaubandus > Varude haldus > Täiendamine > Tootepakendid.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="5ae8f-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-109">Click New.</span></span>
3. <span data-ttu-id="5ae8f-110">Sisestage väärtus väljale Paketi number.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="5ae8f-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5ae8f-112">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5ae8f-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5ae8f-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-114">Click Add.</span></span>
8. <span data-ttu-id="5ae8f-115">Sisestage väljale Kaubakood väärtus 0160.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="5ae8f-116">Klõpsake väljal Suurus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5ae8f-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="5ae8f-118">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="5ae8f-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-119">Click Add.</span></span>
13. <span data-ttu-id="5ae8f-120">Sisestage väljale Kaubakood väärtus 0160.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="5ae8f-121">Klõpsake väljal Variandi number otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5ae8f-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="5ae8f-123">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="5ae8f-124">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-124">Click Add.</span></span>
18. <span data-ttu-id="5ae8f-125">Sisestage väljale Kaubakood väärtus 0175.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="5ae8f-126">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="5ae8f-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-127">Click Save.</span></span>
21. <span data-ttu-id="5ae8f-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="5ae8f-129">Paketi lisamine ostutellimusele</span><span class="sxs-lookup"><span data-stu-id="5ae8f-129">Add package to purchase order</span></span>
1. <span data-ttu-id="5ae8f-130">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="5ae8f-131">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-131">Click New.</span></span>
3. <span data-ttu-id="5ae8f-132">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5ae8f-133">Valige loendist sama hankija, kelle jaoks tootepakett viimati hankija valimisel loodi.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="5ae8f-134">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="5ae8f-135">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5ae8f-136">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5ae8f-137">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="5ae8f-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="5ae8f-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-139">Click OK.</span></span>
11. <span data-ttu-id="5ae8f-140">Lülitage jaotise Rea üksikasjad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="5ae8f-141">Klõpsake vahekaarti Tootepaketid.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="5ae8f-142">Klõpsake suvandit Ostutellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="5ae8f-143">Klõpsake suvandit Loo paketist read.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="5ae8f-144">Leidke ja valige loendist eelmises etapis loodud tootepakett.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="5ae8f-145">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="5ae8f-146">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-146">Click Create.</span></span>
18. <span data-ttu-id="5ae8f-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5ae8f-147">Click Save.</span></span>


