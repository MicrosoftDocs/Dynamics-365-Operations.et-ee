--- 
title: "Elektroonilise aruande konfiguratsiooni üleslaadimine teenusesse Lifecycle Services"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni ja laadida selle teenusesse Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="79ce3-103">Elektroonilise aruande konfiguratsiooni üleslaadimine teenusesse Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="79ce3-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79ce3-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni ja laadida selle teenusesse Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="79ce3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="79ce3-105">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. ja laadite selle üles LCS-i. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="79ce3-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="79ce3-106">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="79ce3-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="79ce3-107">Juurdepääs LCS-i on nõutav ka nende toimingute lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="79ce3-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="79ce3-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="79ce3-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="79ce3-109">Valige Litware, inc.</span><span class="sxs-lookup"><span data-stu-id="79ce3-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="79ce3-110">ja määrake see aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="79ce3-110">and set it as active.</span></span>
3. <span data-ttu-id="79ce3-111">Klõpsake suvandit Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="79ce3-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="79ce3-112">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="79ce3-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="79ce3-113">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="79ce3-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="79ce3-114">Loote konfiguratsiooni, mis sisaldab elektrooniliste dokumentide andmemudeli näidist.</span><span class="sxs-lookup"><span data-stu-id="79ce3-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="79ce3-115">Selle andmemudeli konfiguratsioon laaditakse hiljem LCS-i.</span><span class="sxs-lookup"><span data-stu-id="79ce3-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="79ce3-116">Tippige väljale Nimi tekst Mudeli konfiguratsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="79ce3-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="79ce3-117">Mudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="79ce3-117">Sample model configuration</span></span>  
3. <span data-ttu-id="79ce3-118">Tippige väljale Kirjeldus tekst Mudeli konfiguratsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="79ce3-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="79ce3-119">Mudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="79ce3-119">Sample model configuration</span></span>  
4. <span data-ttu-id="79ce3-120">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="79ce3-120">Click Create configuration.</span></span>
5. <span data-ttu-id="79ce3-121">Klõpsake suvandit Mudeli koostaja.</span><span class="sxs-lookup"><span data-stu-id="79ce3-121">Click Model designer.</span></span>
6. <span data-ttu-id="79ce3-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="79ce3-122">Click New.</span></span>
7. <span data-ttu-id="79ce3-123">Tippige väljale Nimi tekst Sisestuspunkt.</span><span class="sxs-lookup"><span data-stu-id="79ce3-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="79ce3-124">Sisestuspunkt</span><span class="sxs-lookup"><span data-stu-id="79ce3-124">Entry point</span></span>  
8. <span data-ttu-id="79ce3-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="79ce3-125">Click Add.</span></span>
9. <span data-ttu-id="79ce3-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="79ce3-126">Click Save.</span></span>
10. <span data-ttu-id="79ce3-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="79ce3-127">Close the page.</span></span>
11. <span data-ttu-id="79ce3-128">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="79ce3-128">Click Change status.</span></span>
12. <span data-ttu-id="79ce3-129">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="79ce3-129">Click Complete.</span></span>
13. <span data-ttu-id="79ce3-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79ce3-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="79ce3-131">Uue hoidla registreerimine</span><span class="sxs-lookup"><span data-stu-id="79ce3-131">Register a new  repository</span></span>
1. <span data-ttu-id="79ce3-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="79ce3-132">Close the page.</span></span>
2. <span data-ttu-id="79ce3-133">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="79ce3-133">Click Repositories.</span></span>
    * <span data-ttu-id="79ce3-134">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="79ce3-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="79ce3-135">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="79ce3-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="79ce3-136">See võimaldab lisada uue hoidla.</span><span class="sxs-lookup"><span data-stu-id="79ce3-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="79ce3-137">Tehke väljal Konfiguratsioonihoidla tüüp valik LCS.</span><span class="sxs-lookup"><span data-stu-id="79ce3-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="79ce3-138">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="79ce3-138">Click Create repository.</span></span>
6. <span data-ttu-id="79ce3-139">Valige või sisestage väärtus väljal Projekt.</span><span class="sxs-lookup"><span data-stu-id="79ce3-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="79ce3-140">Valige soovitud LCS-i projekt.</span><span class="sxs-lookup"><span data-stu-id="79ce3-140">Select the desired LCS project.</span></span> <span data-ttu-id="79ce3-141">Teil peab olema juurdepääs projektile.</span><span class="sxs-lookup"><span data-stu-id="79ce3-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="79ce3-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79ce3-142">Click OK.</span></span>
    * <span data-ttu-id="79ce3-143">Täitke uus hoidla kirje.</span><span class="sxs-lookup"><span data-stu-id="79ce3-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="79ce3-144">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="79ce3-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="79ce3-145">Valige LCS-i hoidla kirje.</span><span class="sxs-lookup"><span data-stu-id="79ce3-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="79ce3-146">Pange tähele, et registreeritud hoidla on praeguse pakkuja tähistatud, mis tähendab, et sellesse hoidlasse saab paigutada ja valitud LCS-projekti üles laadida ainult need konfiguratsioonid, mille omanik see pakkuja on.</span><span class="sxs-lookup"><span data-stu-id="79ce3-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="79ce3-147">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="79ce3-147">Click Open.</span></span>
    * <span data-ttu-id="79ce3-148">Avage hoidla ER-i konfiguratsioonide loendi vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="79ce3-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="79ce3-149">See on tühi, kui seda projekti pole veel kasutatud ER-i konfiguratsioonide ühiskasutuseks.</span><span class="sxs-lookup"><span data-stu-id="79ce3-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="79ce3-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="79ce3-150">Close the page.</span></span>
11. <span data-ttu-id="79ce3-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="79ce3-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="79ce3-152">Konfiguratsiooni üleslaadimine LCS-i</span><span class="sxs-lookup"><span data-stu-id="79ce3-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="79ce3-153">Klõpsake suvandit Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="79ce3-153">Click Configurations.</span></span>
2. <span data-ttu-id="79ce3-154">Valige puul väärtus Mudeli konfiguratsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="79ce3-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="79ce3-155">Valige loodud konfiguratsioon, mis on juba lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="79ce3-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="79ce3-156">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="79ce3-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="79ce3-157">Valige valitud konfiguratsiooni versioon, mille olek on Lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="79ce3-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="79ce3-158">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="79ce3-158">Click Change status.</span></span>
5. <span data-ttu-id="79ce3-159">Klõpsake nuppu Jaga.</span><span class="sxs-lookup"><span data-stu-id="79ce3-159">Click Share.</span></span>
    * <span data-ttu-id="79ce3-160">Konfiguratsiooni olek muutub olekust Lõpule viidud olekuks Ühiskasutuses, kui see avaldatakse LCS-is.</span><span class="sxs-lookup"><span data-stu-id="79ce3-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="79ce3-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79ce3-161">Click OK.</span></span>
7. <span data-ttu-id="79ce3-162">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="79ce3-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="79ce3-163">Valige konfiguratsiooni versioon olekuga Ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="79ce3-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="79ce3-164">Pange tähele, et valitud versiooni olek on muudetud olekus Lõpule viidud olekuks Ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="79ce3-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="79ce3-165">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="79ce3-165">Close the page.</span></span>
9. <span data-ttu-id="79ce3-166">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="79ce3-166">Click Repositories.</span></span>
    * <span data-ttu-id="79ce3-167">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="79ce3-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="79ce3-168">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="79ce3-168">Click Open.</span></span>
    * <span data-ttu-id="79ce3-169">Valige LCS-hoidla ja avage see.</span><span class="sxs-lookup"><span data-stu-id="79ce3-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="79ce3-170">Pange tähele, et valitud konfiguratsiooni näidatakse valitud LCS-i projekti varana.</span><span class="sxs-lookup"><span data-stu-id="79ce3-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="79ce3-171">Avage LCS, kasutades linki https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="79ce3-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="79ce3-172">Avage projekt, mida kasutasite varem hoidla registreerimiseks, avage projekti varateek ja laiendage GER-i konfiguratsiooni vara tüübi sisu – üleslaaditud ER-i konfiguratsioon on saadaval.</span><span class="sxs-lookup"><span data-stu-id="79ce3-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="79ce3-173">Pange tähele, et üleslaaditud LCS-i konfiguratsiooni saab importida teise Microsoft Dynamics 365 for Finance and Operations, Enterprise edition eksemplari, kui teenuse pakkujatel on juurdepääs sellele LCS-i projektile.</span><span class="sxs-lookup"><span data-stu-id="79ce3-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  


