---
title: Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (1. osa – andmemudeli ettevalmistamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 800df13e1654bc01304411bfa52f4bbd04e6589a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142059"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="ea2f0-103">Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (1. osa – andmemudeli ettevalmistamine)</span><span class="sxs-lookup"><span data-stu-id="ea2f0-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea2f0-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ea2f0-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ea2f0-106">Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="ea2f0-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="ea2f0-108">Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile</span><span class="sxs-lookup"><span data-stu-id="ea2f0-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="ea2f0-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="ea2f0-110">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="ea2f0-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="ea2f0-111">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-111">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="ea2f0-112">Valige ettevõtte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="ea2f0-113">pakkuja.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-113">provider.</span></span>
3. <span data-ttu-id="ea2f0-114">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-114">Click Repositories.</span></span>

    <span data-ttu-id="ea2f0-115">Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="ea2f0-116">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="ea2f0-117">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="ea2f0-118">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-118">Click Create repository.</span></span>
7. <span data-ttu-id="ea2f0-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="ea2f0-120">Microsofti antud kliendiarve mudeli konfiguratsioonide hankimine</span><span class="sxs-lookup"><span data-stu-id="ea2f0-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="ea2f0-121">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-121">Click Show filters.</span></span>
2. <span data-ttu-id="ea2f0-122">Rakendage järgmised filtrid: sisestage väljale Nimi filtriväärtus Operatsiooniressursid, kasutades filtri tehtemärki „algab järgmisega”; sisestage väljale Kirjeldus filtriväärtus "", kasutades filtri tehtemärki „algab järgmisega”</span><span class="sxs-lookup"><span data-stu-id="ea2f0-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="ea2f0-123">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-123">Click Show filters.</span></span>
4. <span data-ttu-id="ea2f0-124">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-124">Click Open.</span></span>
5. <span data-ttu-id="ea2f0-125">Valige puult Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-125">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="ea2f0-126">Valige selle importimiseks mudeli konfiguratsioon Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="ea2f0-127">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-127">Click Import.</span></span>

    <span data-ttu-id="ea2f0-128">Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-128">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="ea2f0-129">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-129">Click Yes.</span></span>
8. <span data-ttu-id="ea2f0-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-130">Close the page.</span></span>
9. <span data-ttu-id="ea2f0-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-131">Close the page.</span></span>
10. <span data-ttu-id="ea2f0-132">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="ea2f0-133">Valige puult Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="ea2f0-134">Looge tuletatud mudel, et toetada juurdepääsu dokumendihalduse failidele.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-134">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="ea2f0-135">Loote oma konfiguratsiooni kliendiarve mudelist, tuletades selle Microsofti antud konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="ea2f0-136">Kasutate seda konfiguratsiooni juurdepääsu juurutamiseks dokumendihalduse failidele ja nende kättesaadavaks tegemiseks elektroonilistele dokumentidele, mille selle mudeli põhjal loote.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="ea2f0-137">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="ea2f0-138">Sisestage väljale Uus tekst Tuleta väärtusest Nimi: kliendiarve mudel, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="ea2f0-139">Tippige väljale Nimi tekst Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="ea2f0-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ea2f0-140">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-140">Click Create configuration.</span></span>

