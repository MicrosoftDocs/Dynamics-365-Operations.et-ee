---
title: Tooteetaloni loomine
description: Tooteetaloni loomine eelmääratletud variantide puhul.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2290cf8da4387155de7790dd3db88b34eb6e96
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150075"
---
# <a name="create-a-product-master"></a><span data-ttu-id="04779-103">Tooteetaloni loomine</span><span class="sxs-lookup"><span data-stu-id="04779-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04779-104">Tooteetaloni loomine eelmääratletud variantide puhul.</span><span class="sxs-lookup"><span data-stu-id="04779-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="04779-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="04779-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="04779-106">See protseduur on mõeldud toote koostajale.</span><span class="sxs-lookup"><span data-stu-id="04779-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="04779-107">Uue tooteetaloni loomine</span><span class="sxs-lookup"><span data-stu-id="04779-107">Create a new product master</span></span>
1. <span data-ttu-id="04779-108">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Tootetalongid**.</span><span class="sxs-lookup"><span data-stu-id="04779-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="04779-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="04779-109">Click **New**.</span></span>
3. <span data-ttu-id="04779-110">Sisestage väärtus väljale **Toote number**.</span><span class="sxs-lookup"><span data-stu-id="04779-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="04779-111">Number peab olema kordumatu.</span><span class="sxs-lookup"><span data-stu-id="04779-111">The number must be unique.</span></span> <span data-ttu-id="04779-112">Numbrijada saab seadistada välja **Tootenumber** puhul.</span><span class="sxs-lookup"><span data-stu-id="04779-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="04779-113">Sellisel juhul ei pea kasutaja väärtust sisestama.</span><span class="sxs-lookup"><span data-stu-id="04779-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="04779-114">Sisestage väärtus väljale **Toote nimi**.</span><span class="sxs-lookup"><span data-stu-id="04779-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="04779-115">Sisestage kirjeldav toote nimi.</span><span class="sxs-lookup"><span data-stu-id="04779-115">Enter a descriptive product name.</span></span> <span data-ttu-id="04779-116">Väärtus on vaikimisi otsingunimi, kuid kasutaja saab seda muuta.</span><span class="sxs-lookup"><span data-stu-id="04779-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="04779-117">Klõpsake väljal **Tootedimensiooni grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="04779-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="04779-118">Tootedimensiooni grupp määrab, millist 4 tootedimensiooni saab kasutada tootevariantide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="04779-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="04779-119">Selles näites kasutatakse gruppi värvi ja suurusega.</span><span class="sxs-lookup"><span data-stu-id="04779-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="04779-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="04779-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="04779-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="04779-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="04779-122">Vaikimisi **Konfiguratsioonitehnoloogiaks** on „Eelmääratletud variant”.</span><span class="sxs-lookup"><span data-stu-id="04779-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="04779-123">Seda kasutatakse selle näite puhul.</span><span class="sxs-lookup"><span data-stu-id="04779-123">This will be used for this example.</span></span>
8. <span data-ttu-id="04779-124">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="04779-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="04779-125">Tootedimensiooni gruppide valimine</span><span class="sxs-lookup"><span data-stu-id="04779-125">Select product dimension groups</span></span>
1. <span data-ttu-id="04779-126">Klõpsake väljal **Värvigrupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="04779-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="04779-127">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="04779-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="04779-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="04779-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="04779-129">Klõpsake väljal **Suuruse grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="04779-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="04779-130">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="04779-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="04779-131">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="04779-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="04779-132">Dimensioonigruppide lisamine</span><span class="sxs-lookup"><span data-stu-id="04779-132">Add dimension groups</span></span>
1. <span data-ttu-id="04779-133">Klõpsake **toimingupaanil** suvandit **Toode**.</span><span class="sxs-lookup"><span data-stu-id="04779-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="04779-134">Klõpsake rippdialoogi avamiseks suvandit **Dimensioonigrupid**.</span><span class="sxs-lookup"><span data-stu-id="04779-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="04779-135">Klõpsake väljal **Laoala dimensiooni grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="04779-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="04779-136">Laoala dimensioonid aitavad reguleerida kaupade ladustamist ja laost väljastamist.</span><span class="sxs-lookup"><span data-stu-id="04779-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="04779-137">Näiteks saab laoala dimensioon hõlmata tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="04779-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="04779-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="04779-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="04779-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="04779-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="04779-140">Klõpsake väljal **Jälgimisdimensiooni grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="04779-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="04779-141">Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone saate tootele lisada.</span><span class="sxs-lookup"><span data-stu-id="04779-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="04779-142">Näiteks kasutatakse laokaupade jälgimiseks partiinumbrit ja seerianumbrit.</span><span class="sxs-lookup"><span data-stu-id="04779-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="04779-143">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="04779-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="04779-144">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="04779-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="04779-145">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="04779-145">Click **OK**.</span></span>
10. <span data-ttu-id="04779-146">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="04779-146">Click **Save**.</span></span>
11. <span data-ttu-id="04779-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="04779-147">Close the page.</span></span>

