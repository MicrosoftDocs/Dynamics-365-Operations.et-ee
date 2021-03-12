---
title: " Tootepakendite loomine ostutellimuste jaoks"
description: See protseduur selgitab tootepaketi loomist ja ostutellimusel kasutamist.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 296b3fb03b20dee5b6024c182df7feb3ce280913
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964666"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="74e45-103"> Tootepakendite loomine ostutellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="74e45-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74e45-104">See protseduur selgitab tootepaketi loomist ja ostutellimusel kasutamist.</span><span class="sxs-lookup"><span data-stu-id="74e45-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="74e45-105">Ostutellimust kasutatakse tellimuse loomiseks eelmääratletud tootekogumi kohta.</span><span class="sxs-lookup"><span data-stu-id="74e45-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="74e45-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="74e45-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="74e45-107">Tootepaketi loomine</span><span class="sxs-lookup"><span data-stu-id="74e45-107">Create a product package</span></span>
1. <span data-ttu-id="74e45-108">Avage Jaemüük ja kaubandus > Varude haldus > Täiendamine > Tootepakendid.</span><span class="sxs-lookup"><span data-stu-id="74e45-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="74e45-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="74e45-109">Click New.</span></span>
3. <span data-ttu-id="74e45-110">Sisestage väärtus väljale Paketi number.</span><span class="sxs-lookup"><span data-stu-id="74e45-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="74e45-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="74e45-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="74e45-112">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="74e45-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="74e45-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="74e45-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="74e45-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="74e45-114">Click Add.</span></span>
8. <span data-ttu-id="74e45-115">Sisestage väljale Kaubakood väärtus 0160.</span><span class="sxs-lookup"><span data-stu-id="74e45-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="74e45-116">Klõpsake väljal Suurus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="74e45-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="74e45-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="74e45-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="74e45-118">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="74e45-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="74e45-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="74e45-119">Click Add.</span></span>
13. <span data-ttu-id="74e45-120">Sisestage väljale Kaubakood väärtus 0160.</span><span class="sxs-lookup"><span data-stu-id="74e45-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="74e45-121">Klõpsake väljal Variandi number otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="74e45-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="74e45-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="74e45-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="74e45-123">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="74e45-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="74e45-124">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="74e45-124">Click Add.</span></span>
18. <span data-ttu-id="74e45-125">Sisestage väljale Kaubakood väärtus 0175.</span><span class="sxs-lookup"><span data-stu-id="74e45-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="74e45-126">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="74e45-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="74e45-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="74e45-127">Click Save.</span></span>
21. <span data-ttu-id="74e45-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="74e45-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="74e45-129">Paketi lisamine ostutellimusele</span><span class="sxs-lookup"><span data-stu-id="74e45-129">Add package to purchase order</span></span>
1. <span data-ttu-id="74e45-130">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="74e45-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="74e45-131">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="74e45-131">Click New.</span></span>
3. <span data-ttu-id="74e45-132">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="74e45-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="74e45-133">Valige loendist sama hankija, kelle jaoks tootepakett viimati hankija valimisel loodi.</span><span class="sxs-lookup"><span data-stu-id="74e45-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="74e45-134">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="74e45-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="74e45-135">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="74e45-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="74e45-136">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="74e45-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="74e45-137">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="74e45-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="74e45-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="74e45-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="74e45-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="74e45-139">Click OK.</span></span>
11. <span data-ttu-id="74e45-140">Lülitage jaotise Rea üksikasjad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="74e45-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="74e45-141">Klõpsake vahekaarti Tootepaketid.</span><span class="sxs-lookup"><span data-stu-id="74e45-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="74e45-142">Klõpsake suvandit Ostutellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="74e45-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="74e45-143">Klõpsake suvandit Loo paketist read.</span><span class="sxs-lookup"><span data-stu-id="74e45-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="74e45-144">Leidke ja valige loendist eelmises etapis loodud tootepakett.</span><span class="sxs-lookup"><span data-stu-id="74e45-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="74e45-145">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="74e45-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="74e45-146">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="74e45-146">Click Create.</span></span>
18. <span data-ttu-id="74e45-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="74e45-147">Click Save.</span></span>

