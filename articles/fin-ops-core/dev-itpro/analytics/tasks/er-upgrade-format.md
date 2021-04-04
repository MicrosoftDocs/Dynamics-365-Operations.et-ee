---
title: Elektrooniline aruandlus. Vormingu täiendamine uue alusversiooni kasutuselevõtuga
description: Selles teemas kirjeldatakse, kuidas säilitada elektroonilise aruandluse (ER) vormingu konfiguratsioon.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 336551f4e9858269010ec7debd1750a8d8453163
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564238"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="e4c12-103">Elektrooniline aruandlus. Vormingu täiendamine uue alusversiooni kasutuselevõtuga</span><span class="sxs-lookup"><span data-stu-id="e4c12-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4c12-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad hallata elektroonilise aruandluse (ER) vormingu konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="e4c12-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="e4c12-105">Selles protseduuris selgitatakse, kuidas saab luua vormingu kohandatud versiooni konfiguratsiooni pakkujalt (CP) saadud vormingu alusel.</span><span class="sxs-lookup"><span data-stu-id="e4c12-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="e4c12-106">Selgitatakse ka seda, kuidas võtta kasutusele selle vormingu uus alusversioon.</span><span class="sxs-lookup"><span data-stu-id="e4c12-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="e4c12-107">Nende etappide lõpule viimiseks peate kõigepealt lõpetama etapid protseduurides „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” ja „Loodud vormingu kasutamine maksete jaoks elektrooniliste dokumentide loomiseks”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="e4c12-108">Neid toiminguid saab teha GBSI ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="e4c12-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="e4c12-109">Vormingu konfiguratsiooni valimine kohandamiseks</span><span class="sxs-lookup"><span data-stu-id="e4c12-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="e4c12-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="e4c12-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="e4c12-111">Selles näites on näidisettevõte Litware, Inc. (https://www.litware.com) konfiguratsiooni pakkuja, mis toetab kindla riigi elektrooniliste maksete vormingu konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="e4c12-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="e4c12-112">Näidisettevõte Proseware, Inc. (http://www.proseware.com) on selle vormingukonfiguratsiooni tarbija, mida pakub Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e4c12-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="e4c12-113">Proseware, Inc. kasutab vorminguid selle riigi teatud piirkondades.</span><span class="sxs-lookup"><span data-stu-id="e4c12-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="e4c12-114">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e4c12-115">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-115">Click Show filters.</span></span>
4. <span data-ttu-id="e4c12-116">Rakendage järgmised filtrid: sisestage filtri väärtus „BACS (UK fiktiivne)” väljale „Nimi”, kasutades filtri tehtemärki „algab üksusega”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="e4c12-117">Valitud vormingu konfiguratsiooni BACS (UK fiktiivne) omanik on pakkuja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e4c12-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="e4c12-118">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-118">Click Show filters.</span></span>
6. <span data-ttu-id="e4c12-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e4c12-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="e4c12-120">Proseware, Inc. kasutab isikupärastamiseks vormingu versiooni olekuga Lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e4c12-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="e4c12-121">Elektroonilise dokumendi kohandatud vormingule uue konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="e4c12-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="e4c12-122">Proseware, Inc. sai ettevõttelt Litware, Inc vastavalt nende teenusekirjeldusele BACS-i (UK fiktiivne) konfiguratsiooniversiooni 1.1, mis sisaldab algset vormingut elektrooniliste maksedokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="e4c12-123">Proseware, Inc. soovib hakata seda kasutama oma riigi standardina, kuid nõutavad on mõned kohandamised, et toetada teatud piirkondlikke nõudeid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="e4c12-124">Proseware, Inc. soovib säilitada ka võime täiendada kohandatud vormingut niipea kui selle uus versioon (koos muudatustega uute riigipõhiste nõuete toetamiseks) ettevõttelt Litware, Inc. välja antakse ja soovib täienduse läbi viia võimalikult väikeste kuludega.</span><span class="sxs-lookup"><span data-stu-id="e4c12-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="e4c12-125">Selleks peab Proseware, Inc. looma konfiguratsiooni, kasutades alusena Litware, Inc. konfiguratsiooni BACS (UK fiktiivne).</span><span class="sxs-lookup"><span data-stu-id="e4c12-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="e4c12-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4c12-126">Close the page.</span></span>
2. <span data-ttu-id="e4c12-127">Valige Proseware, Inc, et muuta see aktiivseks pakkujaks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="e4c12-128">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-128">Click Set active.</span></span>
4. <span data-ttu-id="e4c12-129">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="e4c12-130">Laiendage puustruktuuris suvandit Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="e4c12-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="e4c12-131">Tehke puustruktuuris valik 'Maksed (lihtsustatud mudel)\BACS (UK fiktiivne)'.</span><span class="sxs-lookup"><span data-stu-id="e4c12-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="e4c12-132">Valige ettevõtte Litware, Inc. pakutav BACS (UK fiktiivne). Proseware, Inc. kasutab väljaannet 1.1 kohandatud versiooni alusena.</span><span class="sxs-lookup"><span data-stu-id="e4c12-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="e4c12-133">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="e4c12-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="e4c12-134">See võimaldab teil luua uut konfiguratsiooni kohandatud maksevormingule.</span><span class="sxs-lookup"><span data-stu-id="e4c12-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="e4c12-135">Sisestage väljale Uus tekst 'Tuleta nimest: BACS (UK fiktiivne), Litware, Inc.'.</span><span class="sxs-lookup"><span data-stu-id="e4c12-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="e4c12-136">Valige suvand Tuleta, et kinnitada BACS-i (UK fiktiivne) kasutamine kohandatud versiooni loomise alusena.</span><span class="sxs-lookup"><span data-stu-id="e4c12-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="e4c12-137">Tippige väljale Nimi tekst 'BACS (UK fiktiivne kohandatud)'.</span><span class="sxs-lookup"><span data-stu-id="e4c12-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="e4c12-138">Väljale Kirjeldus tippige „BACS-i hankija makse (UK fiktiivne kohandatud)”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="e4c12-139">Aktiivse konfiguratsiooni pakkuja (Proseware, Inc.) sisestatakse siia automaatselt.</span><span class="sxs-lookup"><span data-stu-id="e4c12-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="e4c12-140">See pakkuja saab seda konfiguratsiooni hallata.</span><span class="sxs-lookup"><span data-stu-id="e4c12-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="e4c12-141">Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.</span><span class="sxs-lookup"><span data-stu-id="e4c12-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="e4c12-142">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="e4c12-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="e4c12-143">Elektroonilise dokumendi jaoks vormingu kohandamine</span><span class="sxs-lookup"><span data-stu-id="e4c12-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="e4c12-144">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="e4c12-144">Click Designer.</span></span>
2. <span data-ttu-id="e4c12-145">Klõpsake nuppu Laienda/ahenda.</span><span class="sxs-lookup"><span data-stu-id="e4c12-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="e4c12-146">Klõpsake nuppu Laienda/ahenda.</span><span class="sxs-lookup"><span data-stu-id="e4c12-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="e4c12-147">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="e4c12-148">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="e4c12-149">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="e4c12-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="e4c12-150">Sisestage väljale Nimi suvand IBAN.</span><span class="sxs-lookup"><span data-stu-id="e4c12-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="e4c12-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4c12-151">Click OK.</span></span>
9. <span data-ttu-id="e4c12-152">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\IBAN”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="e4c12-153">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="e4c12-154">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="e4c12-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="e4c12-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4c12-155">Click OK.</span></span>
13. <span data-ttu-id="e4c12-156">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi\String”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="e4c12-157">Sisestage väljale Maksimaalne pikkus väärtus '60'.</span><span class="sxs-lookup"><span data-stu-id="e4c12-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="e4c12-158">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="e4c12-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="e4c12-159">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="e4c12-160">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="e4c12-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="e4c12-161">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="e4c12-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="e4c12-162">Laiendage puus sõlme model\Payments\Creditor\Account.</span><span class="sxs-lookup"><span data-stu-id="e4c12-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="e4c12-163">Puuvaates valige „mudel\Maksed\Kreeditor\Konto\IBAN”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="e4c12-164">Puuvaates valige „Xml\Teade\Maksed\Kaup = model.Payments\Hankija\Pank\IBAN\String”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="e4c12-165">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="e4c12-165">Click Bind.</span></span>
23. <span data-ttu-id="e4c12-166">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e4c12-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="e4c12-167">Kohandatud vormingu kinnitamine</span><span class="sxs-lookup"><span data-stu-id="e4c12-167">Validate the customized format</span></span>
1. <span data-ttu-id="e4c12-168">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="e4c12-168">Click Validate.</span></span>

    <span data-ttu-id="e4c12-169">Kinnitage kohandatud vormingu paigutus ja andmete vastendamise muudatused veendumaks, et kõik seosed on korras.</span><span class="sxs-lookup"><span data-stu-id="e4c12-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="e4c12-170">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4c12-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="e4c12-171">Kohandatud vormingu konfiguratsiooni praeguse versiooni oleku muutmine</span><span class="sxs-lookup"><span data-stu-id="e4c12-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="e4c12-172">Muutke koostatud vormingu konfiguratsiooni olek suvandilt Mustand suvandile Lõpetatud, et muuta see maksedokumedi loomiseks kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="e4c12-173">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="e4c12-173">Click Change status.</span></span>

    <span data-ttu-id="e4c12-174">Pange tähele, et valitud konfiguratsiooni praegune versioon on olekus Mustand.</span><span class="sxs-lookup"><span data-stu-id="e4c12-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="e4c12-175">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="e4c12-175">Click Complete.</span></span>
3. <span data-ttu-id="e4c12-176">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e4c12-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e4c12-177">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4c12-177">Click OK.</span></span>
5. <span data-ttu-id="e4c12-178">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e4c12-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="e4c12-179">Pange tähele, et loodud konfiguratsioon salvestatakse kui lõpetatud versioon 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="e4c12-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="e4c12-180">See tähendab, et see on kohandatud BACS-i (UK fiktiivne kohandatud) vormingu 1. versioon, mis põhineb BACS-i (UK fiktiivne) vormingu 1. versioonil, mis põhineb andmemudeli Maksed (lihtsustatud mudel) 1. versioonil.</span><span class="sxs-lookup"><span data-stu-id="e4c12-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="e4c12-181">Kohandatud vormingu testimine maksefailide loomiseks</span><span class="sxs-lookup"><span data-stu-id="e4c12-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="e4c12-182">Viige rakenduse Finance and Operations paralleelseansis lõpule protseduur „Loodud vormingu kasutamine maksete jaoks elektrooniliste dokumentide loomiseks”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="e4c12-183">Valige BACS-i (UK fiktiivne kohandatud) vorming elektroonilise makseviisi parameetrites.</span><span class="sxs-lookup"><span data-stu-id="e4c12-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="e4c12-184">Veenduge, et loodud maksefail sisaldab hiljuti kasutusele võetud XML-sõlme IBAN-koodiga vastavalt piirkondlikele nõuetele.</span><span class="sxs-lookup"><span data-stu-id="e4c12-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="e4c12-185">Olemasoleva riigipõhise konfiguratsiooni värskendamine</span><span class="sxs-lookup"><span data-stu-id="e4c12-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="e4c12-186">Litware, Inc. peab värskendama BACS-i (UK fiktiivne) konfiguratsiooni ja kasutusele võtma uued riigipõhised nõuded, et hallata elektroonilise dokumendi vormingut.</span><span class="sxs-lookup"><span data-stu-id="e4c12-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="e4c12-187">Hiljem lisatakse see selle konfiguratsiooni uude versiooni, mida pakutakse teenuse tellijatele, sh ettevõttele Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e4c12-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="e4c12-188">Tegelikes teenuse osutamisega seotud protsessides saab Proseware, Inc. importida iga uue BACS-i (UK fiktiivne) väljaande ettevõtte Litware, Inc. konfiguratsioonide LCS-hoidlast.</span><span class="sxs-lookup"><span data-stu-id="e4c12-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="e4c12-189">Selles protseduuris simuleerime seda, värskendades BACS-i (UK fiktiivne) teenusepakkuja nimel.</span><span class="sxs-lookup"><span data-stu-id="e4c12-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="e4c12-190">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4c12-190">Close the page.</span></span>
2. <span data-ttu-id="e4c12-191">Valige pakkuja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e4c12-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="e4c12-192">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-192">Click Set active.</span></span>
4. <span data-ttu-id="e4c12-193">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="e4c12-194">Laiendage puustruktuuris suvandit Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="e4c12-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="e4c12-195">Tehke puustruktuuris valik 'Maksed (lihtsustatud mudel)\BACS (UK fiktiivne)'.</span><span class="sxs-lookup"><span data-stu-id="e4c12-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="e4c12-196">Ettevõtte Litware, Inc omandis mustandversioon pakkuja BACS (UK fiktiivne) on valitud toomaks kaasa muudatusi, et toetada uusi riigipõhiseid nõudeid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="e4c12-197">Elektroonilise dokumendi alusvormingu lokaliseerimine</span><span class="sxs-lookup"><span data-stu-id="e4c12-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="e4c12-198">Oletagem, et Litware, Inc. peab toetama järgmiseid uusi riigipõhiseid nõudeid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="e4c12-199">Kreeditori panga SWIFT-koodi väärtus igas maksekandes.</span><span class="sxs-lookup"><span data-stu-id="e4c12-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="e4c12-200">100 tähemärgi piirang hankija nime tekstipikkusele loomisfailis.</span><span class="sxs-lookup"><span data-stu-id="e4c12-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="e4c12-201">Uued riigipõhised nõuded</span><span class="sxs-lookup"><span data-stu-id="e4c12-201">New country-specific requirements</span></span>  
- <span data-ttu-id="e4c12-202">Valige soovitud konfiguratsiooni mustandiversioon, et nõutavad muudatused kasutusele võtta.</span><span class="sxs-lookup"><span data-stu-id="e4c12-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="e4c12-203">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="e4c12-203">Click Designer.</span></span>
2. <span data-ttu-id="e4c12-204">Klõpsake nuppu Laienda/ahenda.</span><span class="sxs-lookup"><span data-stu-id="e4c12-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="e4c12-205">Klõpsake nuppu Laienda/ahenda.</span><span class="sxs-lookup"><span data-stu-id="e4c12-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="e4c12-206">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="e4c12-207">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="e4c12-208">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="e4c12-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="e4c12-209">Sisestage väljale Nimi suvand SWIFT.</span><span class="sxs-lookup"><span data-stu-id="e4c12-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="e4c12-210">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4c12-210">Click OK.</span></span>
9. <span data-ttu-id="e4c12-211">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\SWIFT”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="e4c12-212">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="e4c12-213">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="e4c12-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="e4c12-214">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4c12-214">Click OK.</span></span>
13. <span data-ttu-id="e4c12-215">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi\String”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="e4c12-216">Sisestage väljale Maksimaalne pikkus väärtus '100'.</span><span class="sxs-lookup"><span data-stu-id="e4c12-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="e4c12-217">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="e4c12-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="e4c12-218">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="e4c12-219">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="e4c12-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="e4c12-220">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="e4c12-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="e4c12-221">Laiendage puus sõlme model\Payments\Creditor\Agent.</span><span class="sxs-lookup"><span data-stu-id="e4c12-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="e4c12-222">Puuvaates valige „mudel\Maksed\Kreeditor\Agent\SWIFT”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="e4c12-223">Puuvaates valige „Xml\Teade\Maksed\Kaup = model.Payments\Hankija\Pank\SWIFT\String”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="e4c12-224">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="e4c12-224">Click Bind.</span></span>
23. <span data-ttu-id="e4c12-225">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e4c12-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="e4c12-226">Lokaliseeritud vormingu kinnitamine</span><span class="sxs-lookup"><span data-stu-id="e4c12-226">Validate the localized format</span></span>
1. <span data-ttu-id="e4c12-227">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="e4c12-227">Click Validate.</span></span>
2. <span data-ttu-id="e4c12-228">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4c12-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="e4c12-229">Alusvormingu konfiguratsiooni praeguse versiooni oleku muutmine</span><span class="sxs-lookup"><span data-stu-id="e4c12-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="e4c12-230">Muutke värskendatud alusvormingu konfiguratsiooni olek suvandist Mustand suvandiks Lõpetatud, et teha see kättesaadavaks maksedokumentide loomiseks ja sellest tuletatud vormingu konfiguratsioonide värskendusteks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="e4c12-231">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="e4c12-231">Click Change status.</span></span>

    <span data-ttu-id="e4c12-232">Pange tähele, et valitud konfiguratsiooni praegune versioon on olekus Mustand.</span><span class="sxs-lookup"><span data-stu-id="e4c12-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="e4c12-233">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="e4c12-233">Click Complete.</span></span>
3. <span data-ttu-id="e4c12-234">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e4c12-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e4c12-235">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4c12-235">Click OK.</span></span>
5. <span data-ttu-id="e4c12-236">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e4c12-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="e4c12-237">Kohandatud vormingu konfiguratsiooni alusversiooni muutmine</span><span class="sxs-lookup"><span data-stu-id="e4c12-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="e4c12-238">Proseware, Inc. saab teada, et saadaval on BACS-i (UK fiktiivne) konfiguratsiooni uus versioon 1.2, et luua elektroonilisi maksedokumente vastavalt hiljuti teatatud riigipõhistele nõuetele.</span><span class="sxs-lookup"><span data-stu-id="e4c12-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="e4c12-239">Proseware, Inc. soovib hakata kasutama seda riigi standardina.</span><span class="sxs-lookup"><span data-stu-id="e4c12-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="e4c12-240">Selleks peab Proseware, Inc. muutma kohandatud konfiguratsiooni BACS-i (UK fiktiivne kohandatud) aluskonfiguratsiooni versiooni.</span><span class="sxs-lookup"><span data-stu-id="e4c12-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="e4c12-241">BACS-i (UK fiktiivne) versiooni 1.1 asemel kasutage uut versiooni 1.2.</span><span class="sxs-lookup"><span data-stu-id="e4c12-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="e4c12-242">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="e4c12-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e4c12-243">Valige pakkuja Proseware, Inc, et muuta see aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="e4c12-244">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-244">Click Set active.</span></span>
4. <span data-ttu-id="e4c12-245">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="e4c12-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="e4c12-246">Laiendage puustruktuuris suvandit Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="e4c12-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="e4c12-247">Laiendage puustruktuuris suvandit 'Payments (simplified model)\BACS (UK fictitious)'.</span><span class="sxs-lookup"><span data-stu-id="e4c12-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="e4c12-248">Tehke puustruktuuris valik 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span><span class="sxs-lookup"><span data-stu-id="e4c12-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="e4c12-249">Valige BACS-i (UK fiktiivne kohandatud) konfiguratsioon, mille omanik on Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e4c12-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="e4c12-250">Kasutage valitud konfiguratsiooni mustandiversiooni, et nõutavad muudatused kasutusele võtta.</span><span class="sxs-lookup"><span data-stu-id="e4c12-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="e4c12-251">Klõpsake nuppu Muuda alust.</span><span class="sxs-lookup"><span data-stu-id="e4c12-251">Click Rebase.</span></span>

    <span data-ttu-id="e4c12-252">Valige aluskonfiguratsiooni uus versioon 1.2 konfiguratsiooni värskendamise uueks aluseks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="e4c12-253">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4c12-253">Click OK.</span></span>

    <span data-ttu-id="e4c12-254">Pange tähele, et kohandatud versiooni ja uue alusversiooni liitmisel on avastatud mõned probleemid, mis esindavad mõnd vormingumuudatusi, mida ei saa automaatselt ühendada.</span><span class="sxs-lookup"><span data-stu-id="e4c12-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="e4c12-255">Aluse muutmise konfliktide lahendamine</span><span class="sxs-lookup"><span data-stu-id="e4c12-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="e4c12-256">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="e4c12-256">Click Designer.</span></span>
    
    <span data-ttu-id="e4c12-257">Pange tähele, et hankija nime pikkuse piirangu muudatusi ei saa automaatselt lahendada.</span><span class="sxs-lookup"><span data-stu-id="e4c12-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="e4c12-258">Seega on see esitatud konfliktide loendis.</span><span class="sxs-lookup"><span data-stu-id="e4c12-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="e4c12-259">Iga Värskendus-tüüpi konflikti puhul on saadaval järgmised võimalused: - rakendage eelnevat alusväärtust (ruudustiku ülaosas olev nupp), et tuua sisse eelmise alusversiooni väärtus (meie juhtumi puhul 0);</span><span class="sxs-lookup"><span data-stu-id="e4c12-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="e4c12-260">- rakendage alusväärtust (ruudustiku ülaosas olev nupp), et tuua sisse uue alusversiooni väärtus (meie juhtumi puhul 100);</span><span class="sxs-lookup"><span data-stu-id="e4c12-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="e4c12-261">- Säilitage enda (kohandatud) väärtus (60 meie juhtumis).</span><span class="sxs-lookup"><span data-stu-id="e4c12-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="e4c12-262">Klõpsake suvandit Alusväärtuse rakendamine, et rakendada riigipõhist 100 tähemärgi piirangut hankijate nimepikkuste puhul.</span><span class="sxs-lookup"><span data-stu-id="e4c12-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="e4c12-263">Pange tähele, et ettevõtetel Proseware, Inc. ja Litware Inc. on selle vormingu kohandatud ja kohalikud versioonid, mis kasutavad IBAN- ja SWIFT-koode koos seotud komponentidega, mis liidetakse automaatselt haldusvormingus.</span><span class="sxs-lookup"><span data-stu-id="e4c12-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="e4c12-264">Klõpsake suvandit Alusväärtuse rakendamine.</span><span class="sxs-lookup"><span data-stu-id="e4c12-264">Click Apply base value.</span></span>

    <span data-ttu-id="e4c12-265">Klõpsake suvandit Alusväärtuse rakendamine, et rakendada riigipõhist 100 tähemärgi piirangut hankijate nimede puhul.</span><span class="sxs-lookup"><span data-stu-id="e4c12-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="e4c12-266">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e4c12-266">Click Save.</span></span>

    <span data-ttu-id="e4c12-267">Vormingu salvestamine eemaldab lahendatud konfliktid konfliktide loendist.</span><span class="sxs-lookup"><span data-stu-id="e4c12-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="e4c12-268">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4c12-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="e4c12-269">Kohandatud vormingu konfiguratsiooni uue versiooni oleku muutmine</span><span class="sxs-lookup"><span data-stu-id="e4c12-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="e4c12-270">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="e4c12-270">Click Change status.</span></span>

    <span data-ttu-id="e4c12-271">Muutke värskendatud, kohandatud vormingu konfiguratsiooni olekust Mustand olekule Lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e4c12-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="e4c12-272">See muudab vormingu konfiguratsiooni maksedokumentide loomiseks kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="e4c12-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="e4c12-273">Pange tähele, et valitud konfiguratsiooni praegune versioon on olekus Mustand.</span><span class="sxs-lookup"><span data-stu-id="e4c12-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="e4c12-274">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="e4c12-274">Click Complete.</span></span>
3. <span data-ttu-id="e4c12-275">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e4c12-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e4c12-276">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4c12-276">Click OK.</span></span>

    <span data-ttu-id="e4c12-277">Pange tähele, et loodud konfiguratsioon salvestatakse lõpetatud versioonina 1.2.2: alus-BACS-i (UK fiktiivne kohandatud) vormingu versioon 2, mis põhineb alust-BACS-i (UK fiktiivne) vormingu versioonil 2, mis põhineb andmemudeli Maksed (lihtsustatud mudel) versioonil 1.</span><span class="sxs-lookup"><span data-stu-id="e4c12-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="e4c12-278">Kohandatud vormingu testimine maksefailide loomiseks</span><span class="sxs-lookup"><span data-stu-id="e4c12-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="e4c12-279">Viige rakenduse Finance and Operations paralleelseansis lõpule protseduur „Loodud vormingu kasutamine maksete jaoks elektrooniliste dokumentide loomiseks”.</span><span class="sxs-lookup"><span data-stu-id="e4c12-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="e4c12-280">Valige loodud vorming „BACS (UK fiktiivne kohandatud)” elektroonilise makseviisi parameetrites.</span><span class="sxs-lookup"><span data-stu-id="e4c12-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="e4c12-281">Veenduge, et loodud maksefail sisaldab ettevõttes Proseware, Inc. hiljuti kasutusele võetud XML-sõlme IBAN-koodiga vastavalt piirkondlikele nõuetele.</span><span class="sxs-lookup"><span data-stu-id="e4c12-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="e4c12-282">Fail peab sisaldama ka hiljuti ettevõtte Litware, Inc. poolt loodud XML-sõlme SWIFT-pangakoodiga vastavalt riigi nõuetele.</span><span class="sxs-lookup"><span data-stu-id="e4c12-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]