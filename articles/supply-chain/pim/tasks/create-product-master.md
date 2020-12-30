---
title: Tooteetaloni loomine
description: Tooteetaloni loomine eelmääratletud variantide puhul.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdb30b46a0e5a6d4fac997588dd47148f2664c03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426256"
---
# <a name="create-a-product-master"></a><span data-ttu-id="f3bc0-103">Tooteetaloni loomine</span><span class="sxs-lookup"><span data-stu-id="f3bc0-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3bc0-104">Tooteetaloni loomine eelmääratletud variantide puhul.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="f3bc0-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f3bc0-106">See protseduur on mõeldud toote koostajale.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="f3bc0-107">Uue tooteetaloni loomine</span><span class="sxs-lookup"><span data-stu-id="f3bc0-107">Create a new product master</span></span>
1. <span data-ttu-id="f3bc0-108">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Tootetalongid**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="f3bc0-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-109">Click **New**.</span></span>
3. <span data-ttu-id="f3bc0-110">Sisestage väärtus väljale **Toote number**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="f3bc0-111">Number peab olema kordumatu.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-111">The number must be unique.</span></span> <span data-ttu-id="f3bc0-112">Numbrijada saab seadistada välja **Tootenumber** puhul.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="f3bc0-113">Sellisel juhul ei pea kasutaja väärtust sisestama.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="f3bc0-114">Sisestage väärtus väljale **Toote nimi**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="f3bc0-115">Sisestage kirjeldav toote nimi.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-115">Enter a descriptive product name.</span></span> <span data-ttu-id="f3bc0-116">Väärtus on vaikimisi otsingunimi, kuid kasutaja saab seda muuta.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="f3bc0-117">Klõpsake väljal **Tootedimensiooni grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f3bc0-118">Tootedimensiooni grupp määrab, millist 4 tootedimensiooni saab kasutada tootevariantide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="f3bc0-119">Selles näites kasutatakse gruppi värvi ja suurusega.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="f3bc0-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f3bc0-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="f3bc0-122">Vaikimisi **Konfiguratsioonitehnoloogiaks** on „Eelmääratletud variant”.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="f3bc0-123">Seda kasutatakse selle näite puhul.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-123">This will be used for this example.</span></span>
8. <span data-ttu-id="f3bc0-124">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="f3bc0-125">Tootedimensiooni gruppide valimine</span><span class="sxs-lookup"><span data-stu-id="f3bc0-125">Select product dimension groups</span></span>
1. <span data-ttu-id="f3bc0-126">Klõpsake väljal **Värvigrupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="f3bc0-127">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f3bc0-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f3bc0-129">Klõpsake väljal **Suuruse grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f3bc0-130">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f3bc0-131">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="f3bc0-132">Dimensioonigruppide lisamine</span><span class="sxs-lookup"><span data-stu-id="f3bc0-132">Add dimension groups</span></span>
1. <span data-ttu-id="f3bc0-133">Klõpsake **toimingupaanil** suvandit **Toode**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="f3bc0-134">Klõpsake rippdialoogi avamiseks suvandit **Dimensioonigrupid**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="f3bc0-135">Klõpsake väljal **Laoala dimensiooni grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f3bc0-136">Laoala dimensioonid aitavad reguleerida kaupade ladustamist ja laost väljastamist.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="f3bc0-137">Näiteks saab laoala dimensioon hõlmata tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="f3bc0-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f3bc0-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f3bc0-140">Klõpsake väljal **Jälgimisdimensiooni grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f3bc0-141">Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone saate tootele lisada.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="f3bc0-142">Näiteks kasutatakse laokaupade jälgimiseks partiinumbrit ja seerianumbrit.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="f3bc0-143">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f3bc0-144">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f3bc0-145">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-145">Click **OK**.</span></span>
10. <span data-ttu-id="f3bc0-146">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-146">Click **Save**.</span></span>
11. <span data-ttu-id="f3bc0-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3bc0-147">Close the page.</span></span>

