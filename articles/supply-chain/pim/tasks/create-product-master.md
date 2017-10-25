--- 
title: Tooteetaloni loomine
description: "Tooteetaloni loomine eelmääratletud variantide puhul."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f944258e7efdd5c9eba7daf9a80c67058a6cc055
ms.openlocfilehash: 6e5cf92f7736523faf25ac97278a8a273e14ff88
ms.contentlocale: et-ee
ms.lasthandoff: 10/25/2017

---
# <a name="create-a-product-master"></a><span data-ttu-id="874e6-103">Tooteetaloni loomine</span><span class="sxs-lookup"><span data-stu-id="874e6-103">Create a product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="874e6-104">Tooteetaloni loomine eelmääratletud variantide puhul.</span><span class="sxs-lookup"><span data-stu-id="874e6-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="874e6-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="874e6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="874e6-106">See protseduur on mõeldud toote koostajale.</span><span class="sxs-lookup"><span data-stu-id="874e6-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="874e6-107">Uue tooteetaloni loomine</span><span class="sxs-lookup"><span data-stu-id="874e6-107">Create a new product master</span></span>
1. <span data-ttu-id="874e6-108">Avage Tooteteabe haldus > Tooted > Tooteetalonid.</span><span class="sxs-lookup"><span data-stu-id="874e6-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="874e6-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="874e6-109">Click New.</span></span>
3. <span data-ttu-id="874e6-110">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="874e6-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="874e6-111">Number peab olema kordumatu.</span><span class="sxs-lookup"><span data-stu-id="874e6-111">The number must be unique.</span></span> <span data-ttu-id="874e6-112">Numbrijada saab seadistada välja Tootenumber puhul.</span><span class="sxs-lookup"><span data-stu-id="874e6-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="874e6-113">Sellisel juhul ei pea kasutaja väärtust sisestama.</span><span class="sxs-lookup"><span data-stu-id="874e6-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="874e6-114">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="874e6-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="874e6-115">Sisestage kirjeldav toote nimi.</span><span class="sxs-lookup"><span data-stu-id="874e6-115">Enter a descriptive product name.</span></span> <span data-ttu-id="874e6-116">Väärtus on vaikimisi otsingunimi, kuid kasutaja saab seda muuta.</span><span class="sxs-lookup"><span data-stu-id="874e6-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="874e6-117">Klõpsake väljal Tootedimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="874e6-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="874e6-118">Tootedimensiooni grupp määrab, millist 4 tootedimensiooni saab kasutada tootevariantide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="874e6-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="874e6-119">Selles näites kasutatakse gruppi värvi ja suurusega.</span><span class="sxs-lookup"><span data-stu-id="874e6-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="874e6-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="874e6-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="874e6-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="874e6-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="874e6-122">Vaikimisi konfiguratsioonitehnoloogiaks on Eelmääratletud variant.</span><span class="sxs-lookup"><span data-stu-id="874e6-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="874e6-123">Seda kasutatakse selle näite puhul.</span><span class="sxs-lookup"><span data-stu-id="874e6-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="874e6-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="874e6-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="874e6-125">Tootedimensiooni gruppide valimine</span><span class="sxs-lookup"><span data-stu-id="874e6-125">Select product dimension groups</span></span>
1. <span data-ttu-id="874e6-126">Klõpsake väljal Värvigrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="874e6-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="874e6-127">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="874e6-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="874e6-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="874e6-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="874e6-129">Klõpsake väljal Suuruse grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="874e6-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="874e6-130">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="874e6-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="874e6-131">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="874e6-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="874e6-132">Dimensioonigruppide lisamine</span><span class="sxs-lookup"><span data-stu-id="874e6-132">Add dimension groups</span></span>
1. <span data-ttu-id="874e6-133">Klõpsake toimingupaanil suvandit Toode.</span><span class="sxs-lookup"><span data-stu-id="874e6-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="874e6-134">Klõpsake rippdialoogi avamiseks suvandit Dimensioonigrupid.</span><span class="sxs-lookup"><span data-stu-id="874e6-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="874e6-135">Klõpsake väljal Laoala dimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="874e6-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="874e6-136">Laoala dimensioonid aitavad reguleerida kaupade ladustamist ja laost väljastamist.</span><span class="sxs-lookup"><span data-stu-id="874e6-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="874e6-137">Näiteks saab laoala dimensioon hõlmata tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="874e6-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="874e6-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="874e6-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="874e6-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="874e6-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="874e6-140">Klõpsake väljal Jälgimisdimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="874e6-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="874e6-141">Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone saate tootele lisada.</span><span class="sxs-lookup"><span data-stu-id="874e6-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="874e6-142">Näiteks kasutatakse laokaupade jälgimiseks partiinumbrit ja seerianumbrit.</span><span class="sxs-lookup"><span data-stu-id="874e6-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="874e6-143">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="874e6-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="874e6-144">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="874e6-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="874e6-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="874e6-145">Click OK.</span></span>
10. <span data-ttu-id="874e6-146">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="874e6-146">Click Save.</span></span>
11. <span data-ttu-id="874e6-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="874e6-147">Close the page.</span></span>


