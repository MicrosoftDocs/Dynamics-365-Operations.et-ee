---
title: Tootedimensioonid
description: 'On olemas neli tootedimensiooni: värv, konfiguratsioon, suurus ja stiil. Tootedimensioonid saab ühendada dimensioonigruppidesse ja dimensioonigrupid saab määrata tooteetalonidele. Tootevariantide määratlemise määravad tootedimensioonide kombinatsioonid.'
author: cvocph
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3391679696c0e1dd84840821480ccbfb544829a6
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863032"
---
# <a name="product-dimensions"></a><span data-ttu-id="3c10d-105">Tootedimensioonid</span><span class="sxs-lookup"><span data-stu-id="3c10d-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

<span data-ttu-id="3c10d-106">On olemas neli tootedimensiooni: värv, konfiguratsioon, suurus ja stiil.</span><span class="sxs-lookup"><span data-stu-id="3c10d-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="3c10d-107">Tootedimensioonid saab ühendada dimensioonigruppidesse ja dimensioonigrupid saab määrata tooteetalonidele.</span><span class="sxs-lookup"><span data-stu-id="3c10d-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="3c10d-108">Tootevariantide määratlemise määravad tootedimensioonide kombinatsioonid.</span><span class="sxs-lookup"><span data-stu-id="3c10d-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="3c10d-109">Tootedimensioonid on tootevarianti identifitseerivad omadused.</span><span class="sxs-lookup"><span data-stu-id="3c10d-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="3c10d-110">Tootevariantide määratlemiseks saate kasutada tootedimensioonide kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="3c10d-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="3c10d-111">Tootevariandi loomiseks peate määratlema tooteetaloni jaoks vähemalt ühe tootedimensiooni.</span><span class="sxs-lookup"><span data-stu-id="3c10d-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>

## <a name="product-variants"></a><span data-ttu-id="3c10d-112">Tootevariandid</span><span class="sxs-lookup"><span data-stu-id="3c10d-112">Product variants</span></span>

<span data-ttu-id="3c10d-113">Tootevariante nimetatakse ka kaupadeks.</span><span class="sxs-lookup"><span data-stu-id="3c10d-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="3c10d-114">Kaup on materiaalne toode, mis ei ole sama, mis teenus.</span><span class="sxs-lookup"><span data-stu-id="3c10d-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="3c10d-115">Samuti on võimalik määratleda tooteetalon, mille tüüp on Teenus.</span><span class="sxs-lookup"><span data-stu-id="3c10d-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="3c10d-116">Kasutades tüüpi Teenus, saate määrata teenuseid sisaldavad tootevariandid.</span><span class="sxs-lookup"><span data-stu-id="3c10d-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="3c10d-117">Näiteks saate määrata tooteetaloni nõustamistööle ja tootevariandid tööle, mida teevad vanem- ja nooremnõustajad.</span><span class="sxs-lookup"><span data-stu-id="3c10d-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="3c10d-118">Tootedimensioonid</span><span class="sxs-lookup"><span data-stu-id="3c10d-118">Product dimensions</span></span>
<span data-ttu-id="3c10d-119">Saadaval on järgmised tootedimensioonid: konfiguratsioon, värv, suurus ja stiil.</span><span class="sxs-lookup"><span data-stu-id="3c10d-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="3c10d-120">Tootevariandi saab luua tootedimensiooni väärtuste alusel.</span><span class="sxs-lookup"><span data-stu-id="3c10d-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="3c10d-121">Tootedimensioonide väärtused, nagu suurus, värv ja stiil, saab luua lehtedel **Suurus**, **Värv** ja **Stiil**, millele pääseb järgmistest asukohtadest: **Tooteteabe haldus** &gt; **Seadistus** &gt; **Dimensiooni- ja variandigrupid** &gt; **Suurused/Värvid/Stiilid**.</span><span class="sxs-lookup"><span data-stu-id="3c10d-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="3c10d-122">Tootedimensiooni väärtused konfiguratsioonidimensiooni puhul luuakse tavaliselt kas tootekonfiguraatoris või dimensioonipõhises konfiguraatoris.</span><span class="sxs-lookup"><span data-stu-id="3c10d-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="3c10d-123">Tootedimensioone saab luua ja hallata ka lehel **Tootedimensioonid**, millele pääseb juurde järgmistest asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="3c10d-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="3c10d-124">Klõpsake suvandeid **Tooteteabe haldus** &gt; **Tooted** &gt; **Tooteetalonid**.</span><span class="sxs-lookup"><span data-stu-id="3c10d-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="3c10d-125">Klõpsake **toimingupaanil** valikut **Tootedimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="3c10d-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="3c10d-126">Klõpsake suvandeid **Tooteteabe haldus** &gt; **Tooted** &gt; **Kõik tooted ja tooteetalonid**.</span><span class="sxs-lookup"><span data-stu-id="3c10d-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="3c10d-127">Valige tooteetalon.</span><span class="sxs-lookup"><span data-stu-id="3c10d-127">Select a product master.</span></span> <span data-ttu-id="3c10d-128">Klõpsake **toimingupaanil** valikut **Tootedimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="3c10d-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="3c10d-129">Klõpsake valikuid **Tooteteabe haldus** &gt; **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="3c10d-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="3c10d-130">Valige tooteetalon.</span><span class="sxs-lookup"><span data-stu-id="3c10d-130">Select a product master.</span></span> <span data-ttu-id="3c10d-131">Klõpsake **toimingupaanil** suvandit **Toode**.</span><span class="sxs-lookup"><span data-stu-id="3c10d-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="3c10d-132">Klõpsake grupis **Tooteetalon** suvandit **Tootedimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="3c10d-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="3c10d-133">Kaubale loodavate variantide arv on piiratud võimalike tootedimensiooni kombinatsioonide arvuga.</span><span class="sxs-lookup"><span data-stu-id="3c10d-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="3c10d-134">**Näpunäide**</span><span class="sxs-lookup"><span data-stu-id="3c10d-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c10d-135">Toote kasutamisel näiteks tellimusereal valige tootedimensioonid selleks, et määrata tootevariant, millega soovite töötada.</span><span class="sxs-lookup"><span data-stu-id="3c10d-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="3c10d-136">Näide</span><span class="sxs-lookup"><span data-stu-id="3c10d-136">Example</span></span>
<span data-ttu-id="3c10d-137">Ettevõte müüb teksasid.</span><span class="sxs-lookup"><span data-stu-id="3c10d-137">A company sells denim jeans.</span></span> <span data-ttu-id="3c10d-138">Kaup „teksad” kasutab dimensioone Värv ja Suurus.</span><span class="sxs-lookup"><span data-stu-id="3c10d-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="3c10d-139">Teksasid müüakse kolmes eri värvis ja kuues eri suuruses.</span><span class="sxs-lookup"><span data-stu-id="3c10d-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="3c10d-140">Värvid: sinine, must, pruun, suurused: XS, S, M, L, XL, XXL. Kõik suurused ei ole kõigis kolmes värvis saadaval.</span><span class="sxs-lookup"><span data-stu-id="3c10d-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="3c10d-141">Kui kõik kombinatsioonid oleksid olemas, oleks teksasid 18 tüüpi.</span><span class="sxs-lookup"><span data-stu-id="3c10d-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="3c10d-142">Selles näites on toodetud ainult järgmised üheksa tootevariandi kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="3c10d-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="3c10d-143">Värv</span><span class="sxs-lookup"><span data-stu-id="3c10d-143">Color</span></span> | <span data-ttu-id="3c10d-144">Suurus</span><span class="sxs-lookup"><span data-stu-id="3c10d-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="3c10d-145">Sinine</span><span class="sxs-lookup"><span data-stu-id="3c10d-145">Blue</span></span>  | <span data-ttu-id="3c10d-146">XS</span><span class="sxs-lookup"><span data-stu-id="3c10d-146">XS</span></span>   |
| <span data-ttu-id="3c10d-147">Sinine</span><span class="sxs-lookup"><span data-stu-id="3c10d-147">Blue</span></span>  | <span data-ttu-id="3c10d-148">L</span><span class="sxs-lookup"><span data-stu-id="3c10d-148">S</span></span>    |
| <span data-ttu-id="3c10d-149">Sinine</span><span class="sxs-lookup"><span data-stu-id="3c10d-149">Blue</span></span>  | <span data-ttu-id="3c10d-150">E</span><span class="sxs-lookup"><span data-stu-id="3c10d-150">M</span></span>    |
| <span data-ttu-id="3c10d-151">Must</span><span class="sxs-lookup"><span data-stu-id="3c10d-151">Black</span></span> | <span data-ttu-id="3c10d-152">E</span><span class="sxs-lookup"><span data-stu-id="3c10d-152">M</span></span>    |
| <span data-ttu-id="3c10d-153">Must</span><span class="sxs-lookup"><span data-stu-id="3c10d-153">Black</span></span> | <span data-ttu-id="3c10d-154">L</span><span class="sxs-lookup"><span data-stu-id="3c10d-154">L</span></span>    |
| <span data-ttu-id="3c10d-155">Must</span><span class="sxs-lookup"><span data-stu-id="3c10d-155">Black</span></span> | <span data-ttu-id="3c10d-156">XL</span><span class="sxs-lookup"><span data-stu-id="3c10d-156">XL</span></span>   |
| <span data-ttu-id="3c10d-157">Pruun</span><span class="sxs-lookup"><span data-stu-id="3c10d-157">Brown</span></span> | <span data-ttu-id="3c10d-158">L</span><span class="sxs-lookup"><span data-stu-id="3c10d-158">L</span></span>    |
| <span data-ttu-id="3c10d-159">Pruun</span><span class="sxs-lookup"><span data-stu-id="3c10d-159">Brown</span></span> | <span data-ttu-id="3c10d-160">XL</span><span class="sxs-lookup"><span data-stu-id="3c10d-160">XL</span></span>   |
| <span data-ttu-id="3c10d-161">Pruun</span><span class="sxs-lookup"><span data-stu-id="3c10d-161">Brown</span></span> | <span data-ttu-id="3c10d-162">XXL</span><span class="sxs-lookup"><span data-stu-id="3c10d-162">XXL</span></span>  |





