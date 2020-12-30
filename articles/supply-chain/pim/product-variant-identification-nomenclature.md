---
title: Tootevariandi numbrite ja nimede nomenklatuur
description: See teema kirjeldab, kuidas seadistada tootenumbri nomenklatuuri fikseeritud [Tooteetaloni number – Konfiguratsioon – Suurus – Värv – Laad] vormingu asendamiseks.
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 90c01e4281246d890ef888c56ca137f83e83741c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426028"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="d4805-103">Tootevariandi numbrite ja nimede nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="d4805-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4805-104">See teema kirjeldab, kuidas seadistada tootenumbri nomenklatuuri fikseeritud [Tooteetaloni number – Konfiguratsioon – Suurus – Värv – Laad] vormingu asendamiseks.</span><span class="sxs-lookup"><span data-stu-id="d4805-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="d4805-105">Uuel nomenklatuuril on sihipärane vorming, mis sisaldab tooteetaloni numbrit, aktiivseid tootedimensioone ja teie valitud teksti eraldajaid.</span><span class="sxs-lookup"><span data-stu-id="d4805-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="d4805-106">Nomenklatuuri saab luua ka tootenimede kohta.</span><span class="sxs-lookup"><span data-stu-id="d4805-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="d4805-107">Lõpuks saab koostada nomenklatuuri piirangupõhise tootekonfiguraatoriga loodud konfiguratsioonide tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="d4805-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="d4805-108">Need nomenklatuurid võivad sisaldada teie valitud atribuute.</span><span class="sxs-lookup"><span data-stu-id="d4805-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="d4805-109">Tootevariandi numbrite ja nimede uued nomenklatuurid võimaldavad kaasata identifikaatoritesse tootevariantide segmente.</span><span class="sxs-lookup"><span data-stu-id="d4805-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="d4805-110">Need segmendid võivad sisaldada tooteetaloni numbrit ja nime, tootedimensiooni ID-sid ja nimesid, numbriseeriaid, tekstikonstante ja atribuute.</span><span class="sxs-lookup"><span data-stu-id="d4805-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="d4805-111">See funktsionaalsus võimaldab teil müügitellimuse või ostutellimuse loomisel kiiresti leida konkreetse tootevariandi.</span><span class="sxs-lookup"><span data-stu-id="d4805-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="d4805-112">Nomenklatuure saab luua nii tootevariandi numbrite kui ka nimede kohta, kasutades lehte **Toote nomenklatuur**.</span><span class="sxs-lookup"><span data-stu-id="d4805-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="d4805-113">Selle lehe avamiseks klõpsake nuppe **Tooteteabe haldus** &gt; **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="d4805-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="d4805-114">Eelmääratletud tootevariantide nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="d4805-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="d4805-115">Tootevariandid luuakse tooteetalonidele vastavalt ühele kolmest konfiguratsioonitehnoloogiast.</span><span class="sxs-lookup"><span data-stu-id="d4805-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="d4805-116">Eelmääratletud variandid</span><span class="sxs-lookup"><span data-stu-id="d4805-116">Predefined variants</span></span>
-   <span data-ttu-id="d4805-117">Piirangupõhised</span><span class="sxs-lookup"><span data-stu-id="d4805-117">Constraint-based</span></span>
-   <span data-ttu-id="d4805-118">Dimensioonipõhised</span><span class="sxs-lookup"><span data-stu-id="d4805-118">Dimension-based</span></span>

<span data-ttu-id="d4805-119">Igal tootevariandil on number ja nimi ning tootevariandi ID nomenklatuurid võimaldavad valida segmendid, mida kaasatakse igas tootevariandi numbris või nimes.</span><span class="sxs-lookup"><span data-stu-id="d4805-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="d4805-120">Saate valida lehel **Toote nomenklatuur** järgmisi segmente.</span><span class="sxs-lookup"><span data-stu-id="d4805-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="d4805-121">Tooteetaloni number</span><span class="sxs-lookup"><span data-stu-id="d4805-121">Product master number</span></span>
-   <span data-ttu-id="d4805-122">Tooteetaloni nimi</span><span class="sxs-lookup"><span data-stu-id="d4805-122">Product master name</span></span>
-   <span data-ttu-id="d4805-123">Numbriseeria väärtus</span><span class="sxs-lookup"><span data-stu-id="d4805-123">Number sequence value</span></span>
-   <span data-ttu-id="d4805-124">Tekstikonstant</span><span class="sxs-lookup"><span data-stu-id="d4805-124">Text constant</span></span>
-   <span data-ttu-id="d4805-125">Tootedimensioonid</span><span class="sxs-lookup"><span data-stu-id="d4805-125">Product dimensions</span></span>
    -   <span data-ttu-id="d4805-126">Konfiguratsiooni ID või nimi</span><span class="sxs-lookup"><span data-stu-id="d4805-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="d4805-127">Värvi ID või nimi</span><span class="sxs-lookup"><span data-stu-id="d4805-127">Color ID or name</span></span>
    -   <span data-ttu-id="d4805-128">Suuruse ID või nimi</span><span class="sxs-lookup"><span data-stu-id="d4805-128">Size ID or name</span></span>
    -   <span data-ttu-id="d4805-129">Laadi ID või nimi</span><span class="sxs-lookup"><span data-stu-id="d4805-129">Style ID or name</span></span>

<span data-ttu-id="d4805-130">Pärast tootevariandi ID-numbri nomenklatuuri määratlemist saab selle seostada tootedimensioonigrupiga.</span><span class="sxs-lookup"><span data-stu-id="d4805-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="d4805-131">Kõigile sellele tootedimensioonigrupile viitavatele tooteetalonidele määratakse siis nomenklatuuri põhjal tootevariandi numbrid.</span><span class="sxs-lookup"><span data-stu-id="d4805-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="d4805-132">Kuid tootevariandi nime nomenklatuure ei saa tootedimensiooni gruppidega seostada.</span><span class="sxs-lookup"><span data-stu-id="d4805-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="d4805-133">Tootevariandi ID nomenklatuuri saab seostada ka otse tooteetaloniga.</span><span class="sxs-lookup"><span data-stu-id="d4805-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="d4805-134">Sel juhul määratakse tooteetaloni juurde kuuluvatele tootevariantidele nomenklatuuride alusel tootevariandi numbrid ja nimed.</span><span class="sxs-lookup"><span data-stu-id="d4805-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="d4805-135">Näide</span><span class="sxs-lookup"><span data-stu-id="d4805-135">Example</span></span>

<span data-ttu-id="d4805-136">T-särki (TS1234) toodetakse kolmes suuruses (S, M, L), nelja värvi (punane, roheline, sinine, kollane) ja kahes stiilis (polo, V).</span><span class="sxs-lookup"><span data-stu-id="d4805-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="d4805-137">Seetõttu on võimalikud 24 tootevarianti (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="d4805-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="d4805-138">Loote tootevariandi numbri nomenklatuuri, millel on järgmised segmendid.</span><span class="sxs-lookup"><span data-stu-id="d4805-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="d4805-139">Tooteetaloni number</span><span class="sxs-lookup"><span data-stu-id="d4805-139">Product master number</span></span>
2.  <span data-ttu-id="d4805-140">Tekstikonstant: „-”</span><span class="sxs-lookup"><span data-stu-id="d4805-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="d4805-141">Värv</span><span class="sxs-lookup"><span data-stu-id="d4805-141">Color</span></span>
4.  <span data-ttu-id="d4805-142">Tekstikonstant: „-”</span><span class="sxs-lookup"><span data-stu-id="d4805-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="d4805-143">Suurus</span><span class="sxs-lookup"><span data-stu-id="d4805-143">Size</span></span>
6.  <span data-ttu-id="d4805-144">Tekstikonstant: „-”</span><span class="sxs-lookup"><span data-stu-id="d4805-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="d4805-145">Laad</span><span class="sxs-lookup"><span data-stu-id="d4805-145">Style</span></span>

<span data-ttu-id="d4805-146">Sellisel juhul on tootevariandi number punase väikese polosärgi puhul TS1234-punane-väike-polo.</span><span class="sxs-lookup"><span data-stu-id="d4805-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="d4805-147">Piirangupõhiste konfiguratsioonide nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="d4805-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="d4805-148">Piirangupõhiste konfiguratsioonide puhul saab tootedimensiooni konfigureerimiseks luua spetsiaalse nomenklatuuri.</span><span class="sxs-lookup"><span data-stu-id="d4805-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="d4805-149">Saate valida lehel **Toote nomenklatuur** järgmisi segmente.</span><span class="sxs-lookup"><span data-stu-id="d4805-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="d4805-150">Numbriseeria väärtus</span><span class="sxs-lookup"><span data-stu-id="d4805-150">Number sequence value</span></span>
-   <span data-ttu-id="d4805-151">Tekstikonstant</span><span class="sxs-lookup"><span data-stu-id="d4805-151">Text constant</span></span>
-   <span data-ttu-id="d4805-152">Atribuudi väärtus</span><span class="sxs-lookup"><span data-stu-id="d4805-152">Attribute value</span></span>

<span data-ttu-id="d4805-153">Igal toote konfiguratsioonimudelis oleval komponendil võib olla oma konfiguratsiooninomenklatuur.</span><span class="sxs-lookup"><span data-stu-id="d4805-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="d4805-154">Kasutada saab ainult komponendile kuuluvaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="d4805-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="d4805-155">Alamkomponente või kasutajanõuete atribuute ei saa kasutada.</span><span class="sxs-lookup"><span data-stu-id="d4805-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="d4805-156">Näide</span><span class="sxs-lookup"><span data-stu-id="d4805-156">Example</span></span>

<span data-ttu-id="d4805-157">Toote konfiguratsioonimudelil on kahe atribuudiga juurkomponent.</span><span class="sxs-lookup"><span data-stu-id="d4805-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="d4805-158">Materjal (plast, puit, teras)</span><span class="sxs-lookup"><span data-stu-id="d4805-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="d4805-159">Pikkus (10...100)</span><span class="sxs-lookup"><span data-stu-id="d4805-159">Length (10...100)</span></span>

<span data-ttu-id="d4805-160">Loote konfiguratsiooni nomenklatuuri, millel on järgmised segmendid.</span><span class="sxs-lookup"><span data-stu-id="d4805-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="d4805-161">Atribuudi väärtus: materjal</span><span class="sxs-lookup"><span data-stu-id="d4805-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="d4805-162">Tekstikonstant: „AAA”</span><span class="sxs-lookup"><span data-stu-id="d4805-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="d4805-163">Atribuudi väärtus: pikkus</span><span class="sxs-lookup"><span data-stu-id="d4805-163">Attribute value: Length</span></span>

<span data-ttu-id="d4805-164">Sellisel juhul on konfiguratsiooni ID puitmaterjali puhul pikkusega 78 PuitAAA78.</span><span class="sxs-lookup"><span data-stu-id="d4805-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="d4805-165">Dimensioonipõhiste konfiguratsioonide nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="d4805-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="d4805-166">Dimensioonipõhiste konfiguratsioonide puhul saab tootedimensiooni konfigureerimiseks luua spetsiaalse nomenklatuuri.</span><span class="sxs-lookup"><span data-stu-id="d4805-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="d4805-167">Saate valida lehel **Toote nomenklatuur** järgmisi segmente.</span><span class="sxs-lookup"><span data-stu-id="d4805-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="d4805-168">Numbriseeria väärtus</span><span class="sxs-lookup"><span data-stu-id="d4805-168">Number sequence value</span></span>
-   <span data-ttu-id="d4805-169">Tekstikonstant</span><span class="sxs-lookup"><span data-stu-id="d4805-169">Text constant</span></span>
-   <span data-ttu-id="d4805-170">Konfiguratsioonigrupi kaup</span><span class="sxs-lookup"><span data-stu-id="d4805-170">Configuration group item</span></span>

<span data-ttu-id="d4805-171">Konfiguratsiooninomenklatuuri saab määratleda kooslusele.</span><span class="sxs-lookup"><span data-stu-id="d4805-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="d4805-172">Näide</span><span class="sxs-lookup"><span data-stu-id="d4805-172">Example</span></span>

<span data-ttu-id="d4805-173">Kooslusel on neli koosluserida, mis on jagatud kaheks konfiguratsioonigrupiks.</span><span class="sxs-lookup"><span data-stu-id="d4805-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="d4805-174">Koosluserida: M0007, standardkorpus</span><span class="sxs-lookup"><span data-stu-id="d4805-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="d4805-175">Konfiguratsioonigrupp: korpus</span><span class="sxs-lookup"><span data-stu-id="d4805-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="d4805-176">Koosluserida: M0008, tipptasemel korpus</span><span class="sxs-lookup"><span data-stu-id="d4805-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="d4805-177">Konfiguratsioonigrupp: korpus</span><span class="sxs-lookup"><span data-stu-id="d4805-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="d4805-178">Koosluserida: M0021, kangast esivõre</span><span class="sxs-lookup"><span data-stu-id="d4805-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="d4805-179">Konfiguratsioonigrupp: esivõre</span><span class="sxs-lookup"><span data-stu-id="d4805-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="d4805-180">Koosluserida: M0022, metallist esivõre</span><span class="sxs-lookup"><span data-stu-id="d4805-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="d4805-181">Konfiguratsioonigrupp: esivõre</span><span class="sxs-lookup"><span data-stu-id="d4805-181">Configuration group: Front grill</span></span>

<span data-ttu-id="d4805-182">Loote konfiguratsiooni nomenklatuuri, millel on järgmised segmendid.</span><span class="sxs-lookup"><span data-stu-id="d4805-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="d4805-183">Konfiguratsioonigrupp: korpus</span><span class="sxs-lookup"><span data-stu-id="d4805-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="d4805-184">Tekstikonstant: „&”</span><span class="sxs-lookup"><span data-stu-id="d4805-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="d4805-185">Konfiguratsioonigrupp: esivõre</span><span class="sxs-lookup"><span data-stu-id="d4805-185">Configuration group: Front grill</span></span>

<span data-ttu-id="d4805-186">Sellisel juhul on kangast esivõrega standardse korpuse konfiguratsiooni-ID M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="d4805-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="d4805-187">Tootevariantide ja konfiguratsioonide kombinatsiooni nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="d4805-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="d4805-188">Kui kasutate tooteetalonile tootevariantide konfigureerimiseks piirangupõhist või dimensioonipõhist konfiguratsioonitehnoloogiat, võivad tootevariantide tootevariandi numbrid hõlmata konfiguratsioonidimensioonist pärit nomenklatuuri.</span><span class="sxs-lookup"><span data-stu-id="d4805-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="d4805-189">Variantide konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d4805-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="d4805-190">Määratlege lehel **Toote nomenklatuur** tootevariandi numbrite nomenklatuur, mis sisaldab konfiguratsioonidimensiooni.</span><span class="sxs-lookup"><span data-stu-id="d4805-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="d4805-191">Määrake see nomenklatuur konfiguratsioonidimensiooniga tootedimensioonigrupile.</span><span class="sxs-lookup"><span data-stu-id="d4805-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="d4805-192">Määratlege konfiguratsiooninomenklatuur komponentidele või kooslustele, mida kasutatakse tootevariantide konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d4805-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="d4805-193">Nomenklatuure saab luua ka tootevariantide nimedele.</span><span class="sxs-lookup"><span data-stu-id="d4805-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="d4805-194">Tootevariantide nimed saab konfigureerida nii, et need sisaldaksid konfiguratsiooni ID-d või nime.</span><span class="sxs-lookup"><span data-stu-id="d4805-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="d4805-195">Piirangupõhiste konfiguratsioonide näide</span><span class="sxs-lookup"><span data-stu-id="d4805-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="d4805-196">Selle näite puhul saate kasutada tootevariandi numbrite nomenklatuuri, mis koosneb järgmistest segmentidest.</span><span class="sxs-lookup"><span data-stu-id="d4805-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="d4805-197">Tooteetaloni number</span><span class="sxs-lookup"><span data-stu-id="d4805-197">Product master number</span></span>
2.  <span data-ttu-id="d4805-198">Tekstikonstant: „\_”</span><span class="sxs-lookup"><span data-stu-id="d4805-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="d4805-199">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="d4805-199">Configuration</span></span>

<span data-ttu-id="d4805-200">Konfiguratsiooninomenklatuur koosneb järgmistest segmentidest.</span><span class="sxs-lookup"><span data-stu-id="d4805-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="d4805-201">Atribuudi väärtus: materjal</span><span class="sxs-lookup"><span data-stu-id="d4805-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="d4805-202">Tekstikonstant: „AAA”</span><span class="sxs-lookup"><span data-stu-id="d4805-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="d4805-203">Atribuudi väärtus: pikkus</span><span class="sxs-lookup"><span data-stu-id="d4805-203">Attribute value: Length</span></span>

<span data-ttu-id="d4805-204">Saate sisestada segmentidele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d4805-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="d4805-205">Tooteetaloni number = **M0099**</span><span class="sxs-lookup"><span data-stu-id="d4805-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="d4805-206">Materjal = **plast**</span><span class="sxs-lookup"><span data-stu-id="d4805-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="d4805-207">Pikkus = **12**</span><span class="sxs-lookup"><span data-stu-id="d4805-207">Length = **12**</span></span>

<span data-ttu-id="d4805-208">Sellisel juhul saab tootevariandi numbriks M0099\_PlastAAA12.</span><span class="sxs-lookup"><span data-stu-id="d4805-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="d4805-209">Dimensioonipõhiste konfiguratsioonide näide</span><span class="sxs-lookup"><span data-stu-id="d4805-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="d4805-210">Selle näite puhul saate kasutada tootevariandi numbrite nomenklatuuri, mis koosneb järgmistest segmentidest.</span><span class="sxs-lookup"><span data-stu-id="d4805-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="d4805-211">Tooteetaloni number</span><span class="sxs-lookup"><span data-stu-id="d4805-211">Product master number</span></span>
2.  <span data-ttu-id="d4805-212">Tekstikonstant: „//”</span><span class="sxs-lookup"><span data-stu-id="d4805-212">Text constant "//"</span></span>
3.  <span data-ttu-id="d4805-213">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="d4805-213">Configuration</span></span>

<span data-ttu-id="d4805-214">Konfiguratsiooninomenklatuur koosneb järgmistest segmentidest.</span><span class="sxs-lookup"><span data-stu-id="d4805-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="d4805-215">Konfiguratsioonigrupp: korpus</span><span class="sxs-lookup"><span data-stu-id="d4805-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="d4805-216">Tekstikonstant: „&”</span><span class="sxs-lookup"><span data-stu-id="d4805-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="d4805-217">Konfiguratsioonigrupp: esivõre</span><span class="sxs-lookup"><span data-stu-id="d4805-217">Configuration group: Front grill</span></span>

<span data-ttu-id="d4805-218">Saate sisestada segmentidele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d4805-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="d4805-219">Tooteetaloni number = **D0123**</span><span class="sxs-lookup"><span data-stu-id="d4805-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="d4805-220">Korpus = **M0008**</span><span class="sxs-lookup"><span data-stu-id="d4805-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="d4805-221">Esivõre = **M0022**</span><span class="sxs-lookup"><span data-stu-id="d4805-221">Front grill = **M0022**</span></span>

<span data-ttu-id="d4805-222">Sellisel juhul saab tootevariandi numbriks D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="d4805-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="d4805-223">Numbrikonfliktid</span><span class="sxs-lookup"><span data-stu-id="d4805-223">Numbering conflicts</span></span>
<span data-ttu-id="d4805-224">Mõnikord ei pruugi seadistatav tootevariandi numbrite nomenklatuur anda kordumatuid tootevariandi numbreid.</span><span class="sxs-lookup"><span data-stu-id="d4805-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="d4805-225">Tootevariantide numbrid pole kordumatud näiteks juhul, kui üks aktiivne tootedimensioon ei sisaldu eelmääratud variandi konfiguratsioonitehnoloogiat kasutava tooteetaloni nomenklatuuris.</span><span class="sxs-lookup"><span data-stu-id="d4805-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="d4805-226">Konfliktide lahendamise viis võib olla erinev, olenevalt konfiguratsiooni tehnoloogiast.</span><span class="sxs-lookup"><span data-stu-id="d4805-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="d4805-227">Eelmääratletud variandid</span><span class="sxs-lookup"><span data-stu-id="d4805-227">Predefined variants</span></span>

<span data-ttu-id="d4805-228">Kui proovite luua tootevariante käsitsi või automaatselt, nii et mitmel tootevariandil on sama tootevariandi number, tekib tõrge.</span><span class="sxs-lookup"><span data-stu-id="d4805-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="d4805-229">Selle stsenaariumi vältimiseks tuleks kasutada tootedimensiooni grupis kõiki aktiivseid tootedimensioone.</span><span class="sxs-lookup"><span data-stu-id="d4805-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="d4805-230">Teine võimalus on lisada numbriseeria, mis aitab tagada kordumatud tootevariantide numbrid.</span><span class="sxs-lookup"><span data-stu-id="d4805-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="d4805-231">Piirangupõhised konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="d4805-231">Constraint-based configurations</span></span>

<span data-ttu-id="d4805-232">Olenevalt nomenklatuurist võib süsteem püüda määrata konfiguratsioonile mittekordumatu tootevariandi numbri.</span><span class="sxs-lookup"><span data-stu-id="d4805-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="d4805-233">Sellisel juhul kasutab süsteem tootevariandi numbrina konfiguratsioonidimensiooni numbriseeriat ja kuvatakse hoiatus.</span><span class="sxs-lookup"><span data-stu-id="d4805-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="d4805-234">Selle stsenaariumi vältimiseks tuleks lisada nomenklatuuri piisavalt atribuute, mis aitaksid tagada kordumatud tootevariantide numbrid.</span><span class="sxs-lookup"><span data-stu-id="d4805-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="d4805-235">Samuti peaksite veenduma, et valik **Taaskasuta** oleks komponendi puhul sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="d4805-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="d4805-236">Dimensioonipõhised konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="d4805-236">Dimension-based configurations</span></span>

<span data-ttu-id="d4805-237">Ühe konfiguratsiooniprotsessi etapi ajal soovitab süsteem nomenklatuurile vastavat konfiguratsiooniväärtust.</span><span class="sxs-lookup"><span data-stu-id="d4805-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="d4805-238">Selles etapis saate konfiguratsiooniväärtust käsitsi muuta.</span><span class="sxs-lookup"><span data-stu-id="d4805-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="d4805-239">Konfiguratsiooni salvestamisel kontrollib süsteem, kas konfiguratsiooniväärtus on kordumatu.</span><span class="sxs-lookup"><span data-stu-id="d4805-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="d4805-240">Kui sisestatud väärtus ei ole kordumatu, saate tõrketeate.</span><span class="sxs-lookup"><span data-stu-id="d4805-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="d4805-241">Konfiguratsiooni salvestamiseks peate sisestama kordumatu konfiguratsiooniväärtuse.</span><span class="sxs-lookup"><span data-stu-id="d4805-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="d4805-242">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d4805-242">Additional resources</span></span>
--------

[<span data-ttu-id="d4805-243">Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks</span><span class="sxs-lookup"><span data-stu-id="d4805-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="d4805-244">Kaubakoodi nomenklatuuri loomine konfigureeritud tootevariantidele</span><span class="sxs-lookup"><span data-stu-id="d4805-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

