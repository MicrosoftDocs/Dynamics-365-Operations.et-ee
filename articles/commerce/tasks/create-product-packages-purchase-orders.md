---
title: " Tootepakendite loomine ostutellimuste jaoks"
description: See protseduur selgitab tootepaketi loomist ja ostutellimusel kasutamist.
author: josaw1
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c84c829ca1344d70dee294da35b659299d6fa37
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802715"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="eb241-103"> Tootepakendite loomine ostutellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="eb241-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb241-104">See protseduur selgitab tootepaketi loomist ja ostutellimusel kasutamist.</span><span class="sxs-lookup"><span data-stu-id="eb241-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="eb241-105">Ostutellimust kasutatakse tellimuse loomiseks eelmääratletud tootekogumi kohta.</span><span class="sxs-lookup"><span data-stu-id="eb241-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="eb241-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="eb241-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="eb241-107">Tootepaketi loomine</span><span class="sxs-lookup"><span data-stu-id="eb241-107">Create a product package</span></span>
1. <span data-ttu-id="eb241-108">Avage Jaemüük ja kaubandus > Varude haldus > Täiendamine > Tootepakendid.</span><span class="sxs-lookup"><span data-stu-id="eb241-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="eb241-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="eb241-109">Click New.</span></span>
3. <span data-ttu-id="eb241-110">Sisestage väärtus väljale Paketi number.</span><span class="sxs-lookup"><span data-stu-id="eb241-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="eb241-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="eb241-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eb241-112">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="eb241-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="eb241-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="eb241-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="eb241-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="eb241-114">Click Add.</span></span>
8. <span data-ttu-id="eb241-115">Sisestage väljale Kaubakood väärtus 0160.</span><span class="sxs-lookup"><span data-stu-id="eb241-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="eb241-116">Klõpsake väljal Suurus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="eb241-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="eb241-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="eb241-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="eb241-118">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="eb241-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="eb241-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="eb241-119">Click Add.</span></span>
13. <span data-ttu-id="eb241-120">Sisestage väljale Kaubakood väärtus 0160.</span><span class="sxs-lookup"><span data-stu-id="eb241-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="eb241-121">Klõpsake väljal Variandi number otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="eb241-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="eb241-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="eb241-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="eb241-123">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="eb241-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="eb241-124">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="eb241-124">Click Add.</span></span>
18. <span data-ttu-id="eb241-125">Sisestage väljale Kaubakood väärtus 0175.</span><span class="sxs-lookup"><span data-stu-id="eb241-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="eb241-126">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="eb241-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="eb241-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="eb241-127">Click Save.</span></span>
21. <span data-ttu-id="eb241-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="eb241-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="eb241-129">Paketi lisamine ostutellimusele</span><span class="sxs-lookup"><span data-stu-id="eb241-129">Add package to purchase order</span></span>
1. <span data-ttu-id="eb241-130">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="eb241-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="eb241-131">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="eb241-131">Click New.</span></span>
3. <span data-ttu-id="eb241-132">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="eb241-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="eb241-133">Valige loendist sama hankija, kelle jaoks tootepakett viimati hankija valimisel loodi.</span><span class="sxs-lookup"><span data-stu-id="eb241-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="eb241-134">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="eb241-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="eb241-135">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="eb241-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="eb241-136">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="eb241-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="eb241-137">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="eb241-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="eb241-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="eb241-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="eb241-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="eb241-139">Click OK.</span></span>
11. <span data-ttu-id="eb241-140">Lülitage jaotise Rea üksikasjad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="eb241-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="eb241-141">Klõpsake vahekaarti Tootepaketid.</span><span class="sxs-lookup"><span data-stu-id="eb241-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="eb241-142">Klõpsake suvandit Ostutellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="eb241-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="eb241-143">Klõpsake suvandit Loo paketist read.</span><span class="sxs-lookup"><span data-stu-id="eb241-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="eb241-144">Leidke ja valige loendist eelmises etapis loodud tootepakett.</span><span class="sxs-lookup"><span data-stu-id="eb241-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="eb241-145">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="eb241-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="eb241-146">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="eb241-146">Click Create.</span></span>
18. <span data-ttu-id="eb241-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="eb241-147">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]