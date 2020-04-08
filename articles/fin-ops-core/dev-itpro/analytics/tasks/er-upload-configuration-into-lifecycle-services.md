---
title: Elektroonilise aruande konfiguratsiooni üleslaadimine teenusesse Lifecycle Services
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni ja laadida selle teenusesse Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5def757de8fb9d347f5fd0f828039dad5c989c19
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143278"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="6eae4-103">Elektroonilise aruande konfiguratsiooni üleslaadimine teenusesse Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6eae4-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6eae4-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni ja laadida selle teenusesse Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6eae4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="6eae4-105">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. ja laadite selle üles LCS-i. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="6eae4-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="6eae4-106">Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.</span><span class="sxs-lookup"><span data-stu-id="6eae4-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="6eae4-107">Juurdepääs LCS-i on nõutav ka nende toimingute lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="6eae4-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="6eae4-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="6eae4-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6eae4-109">Valige „Litware, inc.”</span><span class="sxs-lookup"><span data-stu-id="6eae4-109">Select 'Litware, Inc.'</span></span> <span data-ttu-id="6eae4-110">ja määrake see aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="6eae4-110">and set it as active.</span></span>
3. <span data-ttu-id="6eae4-111">Klõpsake suvandit Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="6eae4-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="6eae4-112">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="6eae4-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="6eae4-113">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="6eae4-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="6eae4-114">Loote konfiguratsiooni, mis sisaldab elektrooniliste dokumentide andmemudeli näidist.</span><span class="sxs-lookup"><span data-stu-id="6eae4-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="6eae4-115">Selle andmemudeli konfiguratsioon laaditakse hiljem LCS-i.</span><span class="sxs-lookup"><span data-stu-id="6eae4-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="6eae4-116">Tippige väljale Nimi tekst Mudeli konfiguratsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="6eae4-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="6eae4-117">Mudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="6eae4-117">Sample model configuration</span></span>  
3. <span data-ttu-id="6eae4-118">Tippige väljale Kirjeldus tekst Mudeli konfiguratsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="6eae4-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="6eae4-119">Mudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="6eae4-119">Sample model configuration</span></span>  
4. <span data-ttu-id="6eae4-120">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="6eae4-120">Click Create configuration.</span></span>
5. <span data-ttu-id="6eae4-121">Klõpsake suvandit Mudeli koostaja.</span><span class="sxs-lookup"><span data-stu-id="6eae4-121">Click Model designer.</span></span>
6. <span data-ttu-id="6eae4-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6eae4-122">Click New.</span></span>
7. <span data-ttu-id="6eae4-123">Tippige väljale Nimi tekst Sisestuspunkt.</span><span class="sxs-lookup"><span data-stu-id="6eae4-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="6eae4-124">Sisestuspunkt</span><span class="sxs-lookup"><span data-stu-id="6eae4-124">Entry point</span></span>  
8. <span data-ttu-id="6eae4-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6eae4-125">Click Add.</span></span>
9. <span data-ttu-id="6eae4-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6eae4-126">Click Save.</span></span>
10. <span data-ttu-id="6eae4-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6eae4-127">Close the page.</span></span>
11. <span data-ttu-id="6eae4-128">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="6eae4-128">Click Change status.</span></span>
12. <span data-ttu-id="6eae4-129">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="6eae4-129">Click Complete.</span></span>
13. <span data-ttu-id="6eae4-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6eae4-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="6eae4-131">Uue hoidla registreerimine</span><span class="sxs-lookup"><span data-stu-id="6eae4-131">Register a new  repository</span></span>
1. <span data-ttu-id="6eae4-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6eae4-132">Close the page.</span></span>
2. <span data-ttu-id="6eae4-133">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="6eae4-133">Click Repositories.</span></span>
    * <span data-ttu-id="6eae4-134">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="6eae4-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="6eae4-135">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="6eae4-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="6eae4-136">See võimaldab lisada uue hoidla.</span><span class="sxs-lookup"><span data-stu-id="6eae4-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="6eae4-137">Tehke väljal Konfiguratsioonihoidla tüüp valik LCS.</span><span class="sxs-lookup"><span data-stu-id="6eae4-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="6eae4-138">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="6eae4-138">Click Create repository.</span></span>
6. <span data-ttu-id="6eae4-139">Valige või sisestage väärtus väljal Projekt.</span><span class="sxs-lookup"><span data-stu-id="6eae4-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="6eae4-140">Valige soovitud LCS-i projekt.</span><span class="sxs-lookup"><span data-stu-id="6eae4-140">Select the desired LCS project.</span></span> <span data-ttu-id="6eae4-141">Teil peab olema juurdepääs projektile.</span><span class="sxs-lookup"><span data-stu-id="6eae4-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="6eae4-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6eae4-142">Click OK.</span></span>
    * <span data-ttu-id="6eae4-143">Täitke uus hoidla kirje.</span><span class="sxs-lookup"><span data-stu-id="6eae4-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="6eae4-144">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6eae4-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6eae4-145">Valige LCS-i hoidla kirje.</span><span class="sxs-lookup"><span data-stu-id="6eae4-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="6eae4-146">Pange tähele, et registreeritud hoidla on praeguse pakkuja tähistatud, mis tähendab, et sellesse hoidlasse saab paigutada ja valitud LCS-projekti üles laadida ainult need konfiguratsioonid, mille omanik see pakkuja on.</span><span class="sxs-lookup"><span data-stu-id="6eae4-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="6eae4-147">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="6eae4-147">Click Open.</span></span>
    * <span data-ttu-id="6eae4-148">Avage hoidla ER-i konfiguratsioonide loendi vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="6eae4-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="6eae4-149">See on tühi, kui seda projekti pole veel kasutatud ER-i konfiguratsioonide ühiskasutuseks.</span><span class="sxs-lookup"><span data-stu-id="6eae4-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="6eae4-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6eae4-150">Close the page.</span></span>
11. <span data-ttu-id="6eae4-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6eae4-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="6eae4-152">Konfiguratsiooni üleslaadimine LCS-i</span><span class="sxs-lookup"><span data-stu-id="6eae4-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="6eae4-153">Klõpsake suvandit Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="6eae4-153">Click Configurations.</span></span>
2. <span data-ttu-id="6eae4-154">Valige puul väärtus Mudeli konfiguratsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="6eae4-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="6eae4-155">Valige loodud konfiguratsioon, mis on juba lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="6eae4-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="6eae4-156">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6eae4-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6eae4-157">Valige valitud konfiguratsiooni versioon, mille olek on „Lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="6eae4-157">Select the version of the selected configuration with the status of 'Completed'.</span></span>  
4. <span data-ttu-id="6eae4-158">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="6eae4-158">Click Change status.</span></span>
5. <span data-ttu-id="6eae4-159">Klõpsake nuppu Jaga.</span><span class="sxs-lookup"><span data-stu-id="6eae4-159">Click Share.</span></span>
    * <span data-ttu-id="6eae4-160">Konfiguratsiooni olek muutub olekust „Lõpule viidud” olekuks „Ühiskasutuses”, kui see avaldatakse LCS-is.</span><span class="sxs-lookup"><span data-stu-id="6eae4-160">The configuration status will change from 'Completed' to 'Shared' when it is published in LCS.</span></span>  
6. <span data-ttu-id="6eae4-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6eae4-161">Click OK.</span></span>
7. <span data-ttu-id="6eae4-162">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6eae4-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6eae4-163">Valige konfiguratsiooni versioon olekuga Ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="6eae4-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="6eae4-164">Pange tähele, et valitud versiooni olek on muudetud olekus „Lõpule viidud” olekuks „Ühiskasutuses”.</span><span class="sxs-lookup"><span data-stu-id="6eae4-164">Note that the status of the selected version has changed from 'Completed' to 'Shared'.</span></span>  
8. <span data-ttu-id="6eae4-165">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6eae4-165">Close the page.</span></span>
9. <span data-ttu-id="6eae4-166">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="6eae4-166">Click Repositories.</span></span>
    * <span data-ttu-id="6eae4-167">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="6eae4-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="6eae4-168">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="6eae4-168">Click Open.</span></span>
    * <span data-ttu-id="6eae4-169">Valige LCS-hoidla ja avage see.</span><span class="sxs-lookup"><span data-stu-id="6eae4-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="6eae4-170">Pange tähele, et valitud konfiguratsiooni näidatakse valitud LCS-i projekti varana.</span><span class="sxs-lookup"><span data-stu-id="6eae4-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="6eae4-171">Avage LCS, kasutades linki https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="6eae4-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="6eae4-172">Avage projekt, mida kasutasite varem hoidla registreerimiseks, avage projekti varateek ja laiendage GER-i konfiguratsiooni vara tüübi sisu – üleslaaditud ER-i konfiguratsioon on saadaval.</span><span class="sxs-lookup"><span data-stu-id="6eae4-172">Open a project that was used earlier for repository registration, open the 'Asset library' of this project, and expand the content of the 'GER configuration' asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="6eae4-173">Pange tähele, et üleslaaditud LCS-i konfiguratsiooni saab importida teise eksemplari, kui teenuse pakkujatel on juurdepääs sellele LCS-i projektile.</span><span class="sxs-lookup"><span data-stu-id="6eae4-173">Note that the uploaded LCS configuration can be imported to another instance if providers have access to this LCS project.</span></span>  

