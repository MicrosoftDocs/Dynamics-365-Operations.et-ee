--- 
title: "Eelmääratletud tootevariantide loomine"
description: Selles protseduuris juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone.
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2b9202c24b2c1511da6344df6b54326b4d3106c5
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="1aa1b-103">Eelmääratletud tootevariantide loomine</span><span class="sxs-lookup"><span data-stu-id="1aa1b-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1aa1b-104">Selles protseduuris juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="1aa1b-105">Selle protseduuri jaoks kasutati demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="1aa1b-106">Tooteetaloni loomine</span><span class="sxs-lookup"><span data-stu-id="1aa1b-106">Create a product master</span></span>
1. <span data-ttu-id="1aa1b-107">Avage Tooteteabe haldus > Tooted > Tooteetalonid.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="1aa1b-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-108">Click New.</span></span>
3. <span data-ttu-id="1aa1b-109">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="1aa1b-110">Tootenumbri sisestamine käsitsi on kohustuslik ainult siis, kui tootenumbri välja jaoks pole numbriseeriat seadistatud.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="1aa1b-111">Teisisõnu, jätke see etapp vahele, kui väljale on numbriseeria määratud.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="1aa1b-112">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="1aa1b-113">Sisestage või valige väärtus väljal Tootedimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="1aa1b-114">Valige tootedimensioonigrupp SizeCol (suurus ja värv).</span><span class="sxs-lookup"><span data-stu-id="1aa1b-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="1aa1b-115">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="1aa1b-116">Tootedimensioonide lisamine</span><span class="sxs-lookup"><span data-stu-id="1aa1b-116">Add product dimensions</span></span>
1. <span data-ttu-id="1aa1b-117">Klõpsake suvandit Tootedimensioonid.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="1aa1b-118">Selles näites kirjeldatakse, kuidas sisestada käsitsi tootedimensioone.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="1aa1b-119">Samuti saate valida suuruse, värvi või laadi grupi, mis sisaldab tootedimensioon iväärtusi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="1aa1b-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-120">Click New.</span></span>
3. <span data-ttu-id="1aa1b-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1aa1b-122">Sisestage või valige väärtus väljal Suurus.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="1aa1b-123">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="1aa1b-124">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-124">Click New.</span></span>
7. <span data-ttu-id="1aa1b-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1aa1b-126">Sisestage või valige väärtus väljal Suurus.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="1aa1b-127">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="1aa1b-128">Klõpsake vahekaarti Värvid.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="1aa1b-129">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-129">Click New.</span></span>
12. <span data-ttu-id="1aa1b-130">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1aa1b-131">Sisestage või valige väärtus väljal Värv.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="1aa1b-132">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="1aa1b-133">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-133">Click New.</span></span>
16. <span data-ttu-id="1aa1b-134">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="1aa1b-135">Sisestage või valige väärtus väljal Värv.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="1aa1b-136">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="1aa1b-137">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-137">Click Save.</span></span>
20. <span data-ttu-id="1aa1b-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="1aa1b-139">Tootevariantide loomine</span><span class="sxs-lookup"><span data-stu-id="1aa1b-139">Generate product variants</span></span>
1. <span data-ttu-id="1aa1b-140">Klõpsake suvandit Tootevariandid.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-140">Click Product variants.</span></span>
2. <span data-ttu-id="1aa1b-141">Klõpsake suvandit Variandisoovitused.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="1aa1b-142">Klõpsake nuppu Vali kõik.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-142">Click Select all.</span></span>
    * <span data-ttu-id="1aa1b-143">Selles näites on valitud kõik võimalikud variandid.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="1aa1b-144">K variantide loomiseks kasutatakse ainult alamkogumit võimalikest tootedimensioonide kombinatsioonidest, saate valida üksikuid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="1aa1b-145">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-145">Click Create.</span></span>
    * <span data-ttu-id="1aa1b-146">Saate luua kirjeldused kõikidele oma variantidele tootedimensiooni väärtuste kombinatsiooni alusel.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="1aa1b-147">Kirjeldused on valikulised.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="1aa1b-148">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1aa1b-148">Click Save.</span></span>


