---
title: Tootevariandi numbrite ja nimede nomenklatuur
description: "See teema kirjeldab, kuidas seadistada tootenumbri nomenklatuuri fikseeritud vormingu [Tooteetaloni number – Konfiguratsioon – Suurus – Värv – Laad] asendamiseks. Uuel nomenklatuuril on sihipärane vorming, mis sisaldab tooteetaloni numbrit, aktiivseid tootedimensioone ja teie valitud teksti eraldajaid. Nomenklatuuri saab luua ka tootenimede kohta. Lõpuks saab koostada nomenklatuuri piirangupõhise tootekonfiguraatoriga loodud konfiguratsioonide tuvastamiseks. Need nomenklatuurid võivad sisaldada teie valitud atribuute."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 4ebebc1d287908dbe8ac7557c34fc6693c88bfae
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="8e623-107">Tootevariandi numbrite ja nimede nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="8e623-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="8e623-108">See teema kirjeldab, kuidas seadistada tootenumbri nomenklatuuri fikseeritud vormingu [Tooteetaloni number – Konfiguratsioon – Suurus – Värv – Laad] asendamiseks.</span><span class="sxs-lookup"><span data-stu-id="8e623-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="8e623-109">Uuel nomenklatuuril on sihipärane vorming, mis sisaldab tooteetaloni numbrit, aktiivseid tootedimensioone ja teie valitud teksti eraldajaid.</span><span class="sxs-lookup"><span data-stu-id="8e623-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="8e623-110">Nomenklatuuri saab luua ka tootenimede kohta.</span><span class="sxs-lookup"><span data-stu-id="8e623-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="8e623-111">Lõpuks saab koostada nomenklatuuri piirangupõhise tootekonfiguraatoriga loodud konfiguratsioonide tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="8e623-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="8e623-112">Need nomenklatuurid võivad sisaldada teie valitud atribuute.</span><span class="sxs-lookup"><span data-stu-id="8e623-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="8e623-113">Tootevariandi numbrite ja nimede uued nomenklatuurid võimaldavad kaasata identifikaatoritesse tootevariantide segmente.</span><span class="sxs-lookup"><span data-stu-id="8e623-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="8e623-114">Need segmendid võivad sisaldada tooteetaloni numbrit ja nime, tootedimensiooni ID-sid ja nimesid, numbriseeriaid, tekstikonstante ja atribuute.</span><span class="sxs-lookup"><span data-stu-id="8e623-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="8e623-115">See funktsionaalsus võimaldab teil müügitellimuse või ostutellimuse loomisel kiiresti leida konkreetse tootevariandi.</span><span class="sxs-lookup"><span data-stu-id="8e623-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="8e623-116">Nomenklatuure saab luua nii tootevariandi numbrite kui ka nimede kohta, kasutades lehte **Toote nomenklatuur**.</span><span class="sxs-lookup"><span data-stu-id="8e623-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="8e623-117">Selle lehe avamiseks klõpsake nuppe **Tooteteabe haldus** &gt; **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="8e623-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="8e623-118">Eelmääratletud tootevariantide nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="8e623-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="8e623-119">Tootevariandid luuakse tooteetalonidele vastavalt ühele kolmest konfiguratsioonitehnoloogiast.</span><span class="sxs-lookup"><span data-stu-id="8e623-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="8e623-120">Eelmääratletud variandid</span><span class="sxs-lookup"><span data-stu-id="8e623-120">Predefined variants</span></span>
-   <span data-ttu-id="8e623-121">Piirangupõhised</span><span class="sxs-lookup"><span data-stu-id="8e623-121">Constraint-based</span></span>
-   <span data-ttu-id="8e623-122">Dimensioonipõhised</span><span class="sxs-lookup"><span data-stu-id="8e623-122">Dimension-based</span></span>

<span data-ttu-id="8e623-123">Igal tootevariandil on number ja nimi ning tootevariandi ID nomenklatuurid võimaldavad valida segmendid, mida kaasatakse igas tootevariandi numbris või nimes.</span><span class="sxs-lookup"><span data-stu-id="8e623-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="8e623-124">Saate valida lehel **Toote nomenklatuur** järgmisi segmente.</span><span class="sxs-lookup"><span data-stu-id="8e623-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="8e623-125">Tooteetaloni number</span><span class="sxs-lookup"><span data-stu-id="8e623-125">Product master number</span></span>
-   <span data-ttu-id="8e623-126">Tooteetaloni nimi</span><span class="sxs-lookup"><span data-stu-id="8e623-126">Product master name</span></span>
-   <span data-ttu-id="8e623-127">Numbriseeria väärtus</span><span class="sxs-lookup"><span data-stu-id="8e623-127">Number sequence value</span></span>
-   <span data-ttu-id="8e623-128">Tekstikonstant</span><span class="sxs-lookup"><span data-stu-id="8e623-128">Text constant</span></span>
-   <span data-ttu-id="8e623-129">Tootedimensioonid</span><span class="sxs-lookup"><span data-stu-id="8e623-129">Product dimensions</span></span>
    -   <span data-ttu-id="8e623-130">Konfiguratsiooni ID või nimi</span><span class="sxs-lookup"><span data-stu-id="8e623-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="8e623-131">Värvi ID või nimi</span><span class="sxs-lookup"><span data-stu-id="8e623-131">Color ID or name</span></span>
    -   <span data-ttu-id="8e623-132">Suuruse ID või nimi</span><span class="sxs-lookup"><span data-stu-id="8e623-132">Size ID or name</span></span>
    -   <span data-ttu-id="8e623-133">Laadi ID või nimi</span><span class="sxs-lookup"><span data-stu-id="8e623-133">Style ID or name</span></span>

<span data-ttu-id="8e623-134">Pärast tootevariandi ID-numbri nomenklatuuri määratlemist saab selle seostada tootedimensioonigrupiga.</span><span class="sxs-lookup"><span data-stu-id="8e623-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="8e623-135">Kõigile sellele tootedimensioonigrupile viitavatele tooteetalonidele määratakse siis nomenklatuuri põhjal tootevariandi numbrid.</span><span class="sxs-lookup"><span data-stu-id="8e623-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="8e623-136">Kuid tootevariandi nime nomenklatuure ei saa tootedimensiooni gruppidega seostada.</span><span class="sxs-lookup"><span data-stu-id="8e623-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="8e623-137">Tootevariandi ID nomenklatuuri saab seostada ka otse tooteetaloniga.</span><span class="sxs-lookup"><span data-stu-id="8e623-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="8e623-138">Sel juhul määratakse tooteetaloni juurde kuuluvatele tootevariantidele nomenklatuuride alusel tootevariandi numbrid ja nimed.</span><span class="sxs-lookup"><span data-stu-id="8e623-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="8e623-139">Näide</span><span class="sxs-lookup"><span data-stu-id="8e623-139">Example</span></span>

<span data-ttu-id="8e623-140">T-särki (TS1234) toodetakse kolmes suuruses (S, M, L), nelja värvi (punane, roheline, sinine, kollane) ja kahes stiilis (polo, V).</span><span class="sxs-lookup"><span data-stu-id="8e623-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="8e623-141">Seetõttu on võimalikud 24 tootevarianti (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="8e623-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="8e623-142">Loote tootevariandi numbri nomenklatuuri, millel on järgmised segmendid.</span><span class="sxs-lookup"><span data-stu-id="8e623-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="8e623-143">Tooteetaloni number</span><span class="sxs-lookup"><span data-stu-id="8e623-143">Product master number</span></span>
2.  <span data-ttu-id="8e623-144">Tekstikonstant: „-”</span><span class="sxs-lookup"><span data-stu-id="8e623-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="8e623-145">Värv</span><span class="sxs-lookup"><span data-stu-id="8e623-145">Color</span></span>
4.  <span data-ttu-id="8e623-146">Tekstikonstant: „-”</span><span class="sxs-lookup"><span data-stu-id="8e623-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="8e623-147">Suurus</span><span class="sxs-lookup"><span data-stu-id="8e623-147">Size</span></span>
6.  <span data-ttu-id="8e623-148">Tekstikonstant: „-”</span><span class="sxs-lookup"><span data-stu-id="8e623-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="8e623-149">Laad</span><span class="sxs-lookup"><span data-stu-id="8e623-149">Style</span></span>

<span data-ttu-id="8e623-150">Sellisel juhul on tootevariandi number punase väikese polosärgi puhul TS1234-punane-väike-polo.</span><span class="sxs-lookup"><span data-stu-id="8e623-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="8e623-151">Piirangupõhiste konfiguratsioonide nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="8e623-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="8e623-152">Piirangupõhiste konfiguratsioonide puhul saab tootedimensiooni konfigureerimiseks luua spetsiaalse nomenklatuuri.</span><span class="sxs-lookup"><span data-stu-id="8e623-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="8e623-153">Saate valida lehel **Toote nomenklatuur** järgmisi segmente.</span><span class="sxs-lookup"><span data-stu-id="8e623-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="8e623-154">Numbriseeria väärtus</span><span class="sxs-lookup"><span data-stu-id="8e623-154">Number sequence value</span></span>
-   <span data-ttu-id="8e623-155">Tekstikonstant</span><span class="sxs-lookup"><span data-stu-id="8e623-155">Text constant</span></span>
-   <span data-ttu-id="8e623-156">Atribuudi väärtus</span><span class="sxs-lookup"><span data-stu-id="8e623-156">Attribute value</span></span>

<span data-ttu-id="8e623-157">Igal toote konfiguratsioonimudelis oleval komponendil võib olla oma konfiguratsiooninomenklatuur.</span><span class="sxs-lookup"><span data-stu-id="8e623-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="8e623-158">Kasutada saab ainult komponendile kuuluvaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="8e623-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="8e623-159">Alamkomponente või kasutajanõuete atribuute ei saa kasutada.</span><span class="sxs-lookup"><span data-stu-id="8e623-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="8e623-160">Näide</span><span class="sxs-lookup"><span data-stu-id="8e623-160">Example</span></span>

<span data-ttu-id="8e623-161">Toote konfiguratsioonimudelil on kahe atribuudiga juurkomponent.</span><span class="sxs-lookup"><span data-stu-id="8e623-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="8e623-162">Materjal (plast, puit, teras)</span><span class="sxs-lookup"><span data-stu-id="8e623-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="8e623-163">Pikkus (10...100)</span><span class="sxs-lookup"><span data-stu-id="8e623-163">Length (10...100)</span></span>

<span data-ttu-id="8e623-164">Loote konfiguratsiooni nomenklatuuri, millel on järgmised segmendid.</span><span class="sxs-lookup"><span data-stu-id="8e623-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="8e623-165">Atribuudi väärtus: materjal</span><span class="sxs-lookup"><span data-stu-id="8e623-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="8e623-166">Tekstikonstant: „AAA”</span><span class="sxs-lookup"><span data-stu-id="8e623-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="8e623-167">Atribuudi väärtus: pikkus</span><span class="sxs-lookup"><span data-stu-id="8e623-167">Attribute value: Length</span></span>

<span data-ttu-id="8e623-168">Sellisel juhul on konfiguratsiooni ID puitmaterjali puhul pikkusega 78 PuitAAA78.</span><span class="sxs-lookup"><span data-stu-id="8e623-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="8e623-169">Dimensioonipõhiste konfiguratsioonide nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="8e623-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="8e623-170">Dimensioonipõhiste konfiguratsioonide puhul saab tootedimensiooni konfigureerimiseks luua spetsiaalse nomenklatuuri.</span><span class="sxs-lookup"><span data-stu-id="8e623-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="8e623-171">Saate valida lehel **Toote nomenklatuur** järgmisi segmente.</span><span class="sxs-lookup"><span data-stu-id="8e623-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="8e623-172">Numbriseeria väärtus</span><span class="sxs-lookup"><span data-stu-id="8e623-172">Number sequence value</span></span>
-   <span data-ttu-id="8e623-173">Tekstikonstant</span><span class="sxs-lookup"><span data-stu-id="8e623-173">Text constant</span></span>
-   <span data-ttu-id="8e623-174">Konfiguratsioonigrupi kaup</span><span class="sxs-lookup"><span data-stu-id="8e623-174">Configuration group item</span></span>

<span data-ttu-id="8e623-175">Konfiguratsiooninomenklatuuri saab määratleda kooslusele.</span><span class="sxs-lookup"><span data-stu-id="8e623-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="8e623-176">Näide</span><span class="sxs-lookup"><span data-stu-id="8e623-176">Example</span></span>

<span data-ttu-id="8e623-177">Kooslusel on neli koosluserida, mis on jagatud kaheks konfiguratsioonigrupiks.</span><span class="sxs-lookup"><span data-stu-id="8e623-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="8e623-178">Koosluserida: M0007, standardkorpus</span><span class="sxs-lookup"><span data-stu-id="8e623-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="8e623-179">Konfiguratsioonigrupp: korpus</span><span class="sxs-lookup"><span data-stu-id="8e623-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="8e623-180">Koosluserida: M0008, tipptasemel korpus</span><span class="sxs-lookup"><span data-stu-id="8e623-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="8e623-181">Konfiguratsioonigrupp: korpus</span><span class="sxs-lookup"><span data-stu-id="8e623-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="8e623-182">Koosluserida: M0021, kangast esivõre</span><span class="sxs-lookup"><span data-stu-id="8e623-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="8e623-183">Konfiguratsioonigrupp: esivõre</span><span class="sxs-lookup"><span data-stu-id="8e623-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="8e623-184">Koosluserida: M0022, metallist esivõre</span><span class="sxs-lookup"><span data-stu-id="8e623-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="8e623-185">Konfiguratsioonigrupp: esivõre</span><span class="sxs-lookup"><span data-stu-id="8e623-185">Configuration group: Front grill</span></span>

<span data-ttu-id="8e623-186">Loote konfiguratsiooni nomenklatuuri, millel on järgmised segmendid.</span><span class="sxs-lookup"><span data-stu-id="8e623-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="8e623-187">Konfiguratsioonigrupp: korpus</span><span class="sxs-lookup"><span data-stu-id="8e623-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="8e623-188">Tekstikonstant: „&”</span><span class="sxs-lookup"><span data-stu-id="8e623-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="8e623-189">Konfiguratsioonigrupp: esivõre</span><span class="sxs-lookup"><span data-stu-id="8e623-189">Configuration group: Front grill</span></span>

<span data-ttu-id="8e623-190">Sellisel juhul on kangast esivõrega standardse korpuse konfiguratsiooni-ID M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="8e623-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="8e623-191">Tootevariantide ja konfiguratsioonide kombinatsiooni nomenklatuur</span><span class="sxs-lookup"><span data-stu-id="8e623-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="8e623-192">Kui kasutate tooteetalonile tootevariantide konfigureerimiseks piirangupõhist või dimensioonipõhist konfiguratsioonitehnoloogiat, võivad tootevariantide tootevariandi numbrid hõlmata konfiguratsioonidimensioonist pärit nomenklatuuri.</span><span class="sxs-lookup"><span data-stu-id="8e623-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="8e623-193">Variantide konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="8e623-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="8e623-194">Määratlege lehel **Toote nomenklatuur** tootevariandi numbrite nomenklatuur, mis sisaldab konfiguratsioonidimensiooni.</span><span class="sxs-lookup"><span data-stu-id="8e623-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="8e623-195">Määrake see nomenklatuur konfiguratsioonidimensiooniga tootedimensioonigrupile.</span><span class="sxs-lookup"><span data-stu-id="8e623-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="8e623-196">Määratlege konfiguratsiooninomenklatuur komponentidele või kooslustele, mida kasutatakse tootevariantide konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8e623-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="8e623-197">Nomenklatuure saab luua ka tootevariantide nimedele.</span><span class="sxs-lookup"><span data-stu-id="8e623-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="8e623-198">Tootevariantide nimed saab konfigureerida nii, et need sisaldaksid konfiguratsiooni ID-d või nime.</span><span class="sxs-lookup"><span data-stu-id="8e623-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="8e623-199">Piirangupõhiste konfiguratsioonide näide</span><span class="sxs-lookup"><span data-stu-id="8e623-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="8e623-200">Selle näite puhul saate kasutada tootevariandi numbrite nomenklatuuri, mis koosneb järgmistest segmentidest.</span><span class="sxs-lookup"><span data-stu-id="8e623-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="8e623-201">Tooteetaloni number</span><span class="sxs-lookup"><span data-stu-id="8e623-201">Product master number</span></span>
2.  <span data-ttu-id="8e623-202">Tekstikonstant: „\_”</span><span class="sxs-lookup"><span data-stu-id="8e623-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="8e623-203">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="8e623-203">Configuration</span></span>

<span data-ttu-id="8e623-204">Konfiguratsiooninomenklatuur koosneb järgmistest segmentidest.</span><span class="sxs-lookup"><span data-stu-id="8e623-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="8e623-205">Atribuudi väärtus: materjal</span><span class="sxs-lookup"><span data-stu-id="8e623-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="8e623-206">Tekstikonstant: „AAA”</span><span class="sxs-lookup"><span data-stu-id="8e623-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="8e623-207">Atribuudi väärtus: pikkus</span><span class="sxs-lookup"><span data-stu-id="8e623-207">Attribute value: Length</span></span>

<span data-ttu-id="8e623-208">Saate sisestada segmentidele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="8e623-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="8e623-209">Tooteetaloni number = **M0099**</span><span class="sxs-lookup"><span data-stu-id="8e623-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="8e623-210">Materjal = **plast**</span><span class="sxs-lookup"><span data-stu-id="8e623-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="8e623-211">Pikkus = **12**</span><span class="sxs-lookup"><span data-stu-id="8e623-211">Length = **12**</span></span>

<span data-ttu-id="8e623-212">Sellisel juhul saab tootevariandi numbriks M0099\_PlastAAA12.</span><span class="sxs-lookup"><span data-stu-id="8e623-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="8e623-213">Dimensioonipõhiste konfiguratsioonide näide</span><span class="sxs-lookup"><span data-stu-id="8e623-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="8e623-214">Selle näite puhul saate kasutada tootevariandi numbrite nomenklatuuri, mis koosneb järgmistest segmentidest.</span><span class="sxs-lookup"><span data-stu-id="8e623-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="8e623-215">Tooteetaloni number</span><span class="sxs-lookup"><span data-stu-id="8e623-215">Product master number</span></span>
2.  <span data-ttu-id="8e623-216">Tekstikonstant: „//”</span><span class="sxs-lookup"><span data-stu-id="8e623-216">Text constant "//"</span></span>
3.  <span data-ttu-id="8e623-217">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="8e623-217">Configuration</span></span>

<span data-ttu-id="8e623-218">Konfiguratsiooninomenklatuur koosneb järgmistest segmentidest.</span><span class="sxs-lookup"><span data-stu-id="8e623-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="8e623-219">Konfiguratsioonigrupp: korpus</span><span class="sxs-lookup"><span data-stu-id="8e623-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="8e623-220">Tekstikonstant: „&”</span><span class="sxs-lookup"><span data-stu-id="8e623-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="8e623-221">Konfiguratsioonigrupp: esivõre</span><span class="sxs-lookup"><span data-stu-id="8e623-221">Configuration group: Front grill</span></span>

<span data-ttu-id="8e623-222">Saate sisestada segmentidele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="8e623-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="8e623-223">Tooteetaloni number = **D0123**</span><span class="sxs-lookup"><span data-stu-id="8e623-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="8e623-224">Korpus = **M0008**</span><span class="sxs-lookup"><span data-stu-id="8e623-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="8e623-225">Esivõre = **M0022**</span><span class="sxs-lookup"><span data-stu-id="8e623-225">Front grill = **M0022**</span></span>

<span data-ttu-id="8e623-226">Sellisel juhul saab tootevariandi numbriks D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="8e623-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="8e623-227">Numbrikonfliktid</span><span class="sxs-lookup"><span data-stu-id="8e623-227">Numbering conflicts</span></span>
<span data-ttu-id="8e623-228">Mõnikord ei pruugi seadistatav tootevariandi numbrite nomenklatuur anda kordumatuid tootevariandi numbreid.</span><span class="sxs-lookup"><span data-stu-id="8e623-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="8e623-229">Tootevariantide numbrid pole kordumatud näiteks juhul, kui üks aktiivne tootedimensioon ei sisaldu eelmääratud variandi konfiguratsioonitehnoloogiat kasutava tooteetaloni nomenklatuuris.</span><span class="sxs-lookup"><span data-stu-id="8e623-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="8e623-230">Konfliktide lahendamise viis võib olla erinev, olenevalt konfiguratsiooni tehnoloogiast.</span><span class="sxs-lookup"><span data-stu-id="8e623-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="8e623-231">Eelmääratletud variandid</span><span class="sxs-lookup"><span data-stu-id="8e623-231">Predefined variants</span></span>

<span data-ttu-id="8e623-232">Kui proovite luua tootevariante käsitsi või automaatselt, nii et mitmel tootevariandil on sama tootevariandi number, tekib tõrge.</span><span class="sxs-lookup"><span data-stu-id="8e623-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="8e623-233">Selle stsenaariumi vältimiseks tuleks kasutada tootedimensiooni grupis kõiki aktiivseid tootedimensioone.</span><span class="sxs-lookup"><span data-stu-id="8e623-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="8e623-234">Teine võimalus on lisada numbriseeria, mis aitab tagada kordumatud tootevariantide numbrid.</span><span class="sxs-lookup"><span data-stu-id="8e623-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="8e623-235">Piirangupõhised konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="8e623-235">Constraint-based configurations</span></span>

<span data-ttu-id="8e623-236">Olenevalt nomenklatuurist võib süsteem püüda määrata konfiguratsioonile mittekordumatu tootevariandi numbri.</span><span class="sxs-lookup"><span data-stu-id="8e623-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="8e623-237">Sellisel juhul kasutab süsteem tootevariandi numbrina konfiguratsioonidimensiooni numbriseeriat ja kuvatakse hoiatus.</span><span class="sxs-lookup"><span data-stu-id="8e623-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="8e623-238">Selle stsenaariumi vältimiseks tuleks lisada nomenklatuuri piisavalt atribuute, mis aitaksid tagada kordumatud tootevariantide numbrid.</span><span class="sxs-lookup"><span data-stu-id="8e623-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="8e623-239">Samuti peaksite veenduma, et valik **Taaskasuta** oleks komponendi puhul sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="8e623-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="8e623-240">Dimensioonipõhised konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="8e623-240">Dimension-based configurations</span></span>

<span data-ttu-id="8e623-241">Ühe konfiguratsiooniprotsessi etapi ajal soovitab süsteem nomenklatuurile vastavat konfiguratsiooniväärtust.</span><span class="sxs-lookup"><span data-stu-id="8e623-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="8e623-242">Selles etapis saate konfiguratsiooniväärtust käsitsi muuta.</span><span class="sxs-lookup"><span data-stu-id="8e623-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="8e623-243">Konfiguratsiooni salvestamisel kontrollib süsteem, kas konfiguratsiooniväärtus on kordumatu.</span><span class="sxs-lookup"><span data-stu-id="8e623-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="8e623-244">Kui sisestatud väärtus ei ole kordumatu, saate tõrketeate.</span><span class="sxs-lookup"><span data-stu-id="8e623-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="8e623-245">Konfiguratsiooni salvestamiseks peate sisestama kordumatu konfiguratsiooniväärtuse.</span><span class="sxs-lookup"><span data-stu-id="8e623-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="8e623-246">Vt ka</span><span class="sxs-lookup"><span data-stu-id="8e623-246">See also</span></span>
--------

[<span data-ttu-id="8e623-247">Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantidele</span><span class="sxs-lookup"><span data-stu-id="8e623-247">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="8e623-248">Kaubakoodi nomenklatuuri loomine konfigureeritud tootevariantidele</span><span class="sxs-lookup"><span data-stu-id="8e623-248">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


