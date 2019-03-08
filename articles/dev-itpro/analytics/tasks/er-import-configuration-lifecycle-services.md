---
title: Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida uue elektroonilise aruandluse (ER) konfiguratsiooni teenusest Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "337252"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="868be-103">Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="868be-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="868be-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida uue elektroonilise aruandluse (ER) konfiguratsiooni teenusest Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="868be-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="868be-105">Selles näites valite soovitud ER-i konfiguratsiooni ja impordite selle näidisettevõttele Litware, Inc. Neid etappe saab läbida mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtete seas ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="868be-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="868be-106">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri ER-i konfiguratsiooni üleslaadimine teenusesse Lifecycle Services etapid.</span><span class="sxs-lookup"><span data-stu-id="868be-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="868be-107">Juurdepääs LCS-i on nõutav ka nende toimingute lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="868be-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="868be-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="868be-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="868be-109">Klõpsake suvandit Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="868be-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="868be-110">Andmemudeli konfiguratsiooni ühiskasutuses versiooni kustutamine</span><span class="sxs-lookup"><span data-stu-id="868be-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="868be-111">Valige puul väärtus Mudeli konfiguratsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="868be-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="868be-112">Andmemudeli konfiguratsiooni esimene versioon on loodud ja avaldatud LCS-is protseduuri ER-i konfiguratsiooni üleslaadimine teenusesse Lifecycle Services ajal.</span><span class="sxs-lookup"><span data-stu-id="868be-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="868be-113">Selle protseduuri käigus kustutate selle ER-i konfiguratsiooni versiooni.</span><span class="sxs-lookup"><span data-stu-id="868be-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="868be-114">See andmemudeli näidiskonfiguratsiooni versioon imporditakse hiljem LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="868be-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="868be-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="868be-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="868be-116">Valige selle konfiguratsiooni versioon, mis on olekus Ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="868be-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="868be-117">See olek näitab, et konfiguratsioon on avaldatud LCS-is.</span><span class="sxs-lookup"><span data-stu-id="868be-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="868be-118">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="868be-118">Click Change status.</span></span>
4. <span data-ttu-id="868be-119">Klõpsake nuppu Katkesta.</span><span class="sxs-lookup"><span data-stu-id="868be-119">Click Discontinue.</span></span>
    * <span data-ttu-id="868be-120">Muutke valitud versiooni olek Ühiskasutuses olekuks Katkestatud, et muuta see kustutamiseks kättesaadavaks</span><span class="sxs-lookup"><span data-stu-id="868be-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="868be-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="868be-121">Click OK.</span></span>
6. <span data-ttu-id="868be-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="868be-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="868be-123">Valige selle konfiguratsiooni versioon, mille olek on Katkestatud.</span><span class="sxs-lookup"><span data-stu-id="868be-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="868be-124">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="868be-124">Click Delete.</span></span>
8. <span data-ttu-id="868be-125">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="868be-125">Click Yes.</span></span>
    * <span data-ttu-id="868be-126">Pange tähele, et saadaval on ainult valitud andmemudeli konfiguratsiooni mustandversioon 2.</span><span class="sxs-lookup"><span data-stu-id="868be-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="868be-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="868be-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="868be-128">Andmemudeli konfiguratsiooni ühiskasutuses versiooni importimine LCS-ist</span><span class="sxs-lookup"><span data-stu-id="868be-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="868be-129">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="868be-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="868be-130">Avage ettevõtte Litware, Inc. hoidlate loend.</span><span class="sxs-lookup"><span data-stu-id="868be-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="868be-131">konfiguratsiooni pakkuja jaoks.</span><span class="sxs-lookup"><span data-stu-id="868be-131">configuration provider.</span></span>  
2. <span data-ttu-id="868be-132">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="868be-132">Click Repositories.</span></span>
3. <span data-ttu-id="868be-133">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="868be-133">Click Open.</span></span>
    * <span data-ttu-id="868be-134">Valige LCS-hoidla ja avage see.</span><span class="sxs-lookup"><span data-stu-id="868be-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="868be-135">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="868be-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="868be-136">Valige versiooni loendist suvandi Mudeli konfiguratsiooni näide esimene versioon.</span><span class="sxs-lookup"><span data-stu-id="868be-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="868be-137">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="868be-137">Click Import.</span></span>
6. <span data-ttu-id="868be-138">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="868be-138">Click Yes.</span></span>
    * <span data-ttu-id="868be-139">Kinnitage valitud versiooni import LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="868be-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="868be-140">Pange tähele, et tebeteade (vormi kohal) kinnitab valitud versiooni impordi lõpuleviimise.</span><span class="sxs-lookup"><span data-stu-id="868be-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="868be-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="868be-141">Close the page.</span></span>
8. <span data-ttu-id="868be-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="868be-142">Close the page.</span></span>
9. <span data-ttu-id="868be-143">Klõpsake suvandit Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="868be-143">Click Configurations.</span></span>
10. <span data-ttu-id="868be-144">Valige puul väärtus Mudeli konfiguratsiooni näide.</span><span class="sxs-lookup"><span data-stu-id="868be-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="868be-145">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="868be-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="868be-146">Valige selle konfiguratsiooni versiooni, mille olek on Ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="868be-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="868be-147">Pange tähele, et nüüd on saadaval ka valitud andmemudeli konfiguratsiooni ühiskasutatav versioon 1.</span><span class="sxs-lookup"><span data-stu-id="868be-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

