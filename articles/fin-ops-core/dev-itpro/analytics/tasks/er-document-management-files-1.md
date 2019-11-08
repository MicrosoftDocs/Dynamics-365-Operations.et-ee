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
ms.openlocfilehash: 29c13e729223a98d7f45244c5a796bca6e3baaf3
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550829"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="6ecd3-103">Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (1. osa – andmemudeli ettevalmistamine)</span><span class="sxs-lookup"><span data-stu-id="6ecd3-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ecd3-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="6ecd3-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6ecd3-106">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="6ecd3-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="6ecd3-108">Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile</span><span class="sxs-lookup"><span data-stu-id="6ecd3-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6ecd3-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6ecd3-110">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="6ecd3-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="6ecd3-111">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="6ecd3-112">Valige ettevõtte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="6ecd3-113">pakkuja.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-113">provider.</span></span>
3. <span data-ttu-id="6ecd3-114">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-114">Click Repositories.</span></span>
    * <span data-ttu-id="6ecd3-115">Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="6ecd3-116">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="6ecd3-117">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="6ecd3-118">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-118">Click Create repository.</span></span>
7. <span data-ttu-id="6ecd3-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="6ecd3-120">Microsofti antud kliendiarve mudeli konfiguratsioonide hankimine</span><span class="sxs-lookup"><span data-stu-id="6ecd3-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6ecd3-121">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-121">Click Show filters.</span></span>
2. <span data-ttu-id="6ecd3-122">Rakendage järgmised filtrid: sisestage väljale Nimi filtriväärtus Operatsiooniressursid, kasutades filtri tehtemärki „algab järgmisega”; sisestage väljale Kirjeldus filtriväärtus "", kasutades filtri tehtemärki „algab järgmisega”</span><span class="sxs-lookup"><span data-stu-id="6ecd3-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="6ecd3-123">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-123">Click Show filters.</span></span>
4. <span data-ttu-id="6ecd3-124">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-124">Click Open.</span></span>
5. <span data-ttu-id="6ecd3-125">Valige puult Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="6ecd3-126">Valige selle importimiseks mudeli konfiguratsioon Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="6ecd3-127">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-127">Click Import.</span></span>
    * <span data-ttu-id="6ecd3-128">Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="6ecd3-129">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-129">Click Yes.</span></span>
8. <span data-ttu-id="6ecd3-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-130">Close the page.</span></span>
9. <span data-ttu-id="6ecd3-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-131">Close the page.</span></span>
10. <span data-ttu-id="6ecd3-132">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="6ecd3-133">Valige puult Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="6ecd3-134">Looge tuletatud mudel, et toetada juurdepääsu dokumendihalduse failidele.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="6ecd3-135">Loote oma konfiguratsiooni kliendiarve mudelist, tuletades selle Microsofti antud konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="6ecd3-136">Kasutate seda konfiguratsiooni juurdepääsu juurutamiseks dokumendihalduse failidele ja nende kättesaadavaks tegemiseks elektroonilistele dokumentidele, mille selle mudeli põhjal loote.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="6ecd3-137">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6ecd3-138">Sisestage väljale Uus tekst Tuleta väärtusest Nimi: kliendiarve mudel, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="6ecd3-139">Tippige väljale Nimi tekst Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="6ecd3-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="6ecd3-140">Kliendiarve mudel (kohandatud)</span><span class="sxs-lookup"><span data-stu-id="6ecd3-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="6ecd3-141">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="6ecd3-141">Click Create configuration.</span></span>

