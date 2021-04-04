---
title: Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (1. osa – andmemudeli ettevalmistamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) vormingut kasutama ER-i väljundis dokumendihalduse faile (manused). (1. osa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35bffd6d3688a9887fcdaf4edbd89c344cb9b18d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559793"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="5d095-104">Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (1. osa – andmemudeli ettevalmistamine)</span><span class="sxs-lookup"><span data-stu-id="5d095-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d095-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="5d095-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="5d095-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="5d095-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="5d095-107">Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.</span><span class="sxs-lookup"><span data-stu-id="5d095-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="5d095-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="5d095-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="5d095-109">Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile</span><span class="sxs-lookup"><span data-stu-id="5d095-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="5d095-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="5d095-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="5d095-111">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="5d095-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="5d095-112">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="5d095-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="5d095-113">Valige ettevõtte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5d095-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="5d095-114">pakkuja.</span><span class="sxs-lookup"><span data-stu-id="5d095-114">provider.</span></span>
3. <span data-ttu-id="5d095-115">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="5d095-115">Click Repositories.</span></span>

    <span data-ttu-id="5d095-116">Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="5d095-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="5d095-117">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5d095-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="5d095-118">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="5d095-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="5d095-119">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="5d095-119">Click Create repository.</span></span>
7. <span data-ttu-id="5d095-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5d095-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="5d095-121">Microsofti antud kliendiarve mudeli konfiguratsioonide hankimine</span><span class="sxs-lookup"><span data-stu-id="5d095-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="5d095-122">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="5d095-122">Click Show filters.</span></span>
2. <span data-ttu-id="5d095-123">Rakendage järgmised filtrid: sisestage väljale Nimi filtriväärtus Operatsiooniressursid, kasutades filtri tehtemärki „algab järgmisega”; sisestage väljale Kirjeldus filtriväärtus "", kasutades filtri tehtemärki „algab järgmisega”</span><span class="sxs-lookup"><span data-stu-id="5d095-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="5d095-124">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="5d095-124">Click Show filters.</span></span>
4. <span data-ttu-id="5d095-125">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="5d095-125">Click Open.</span></span>
5. <span data-ttu-id="5d095-126">Valige puult Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="5d095-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="5d095-127">Valige selle importimiseks mudeli konfiguratsioon Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="5d095-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="5d095-128">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="5d095-128">Click Import.</span></span>

    <span data-ttu-id="5d095-129">Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.</span><span class="sxs-lookup"><span data-stu-id="5d095-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="5d095-130">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="5d095-130">Click Yes.</span></span>
8. <span data-ttu-id="5d095-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5d095-131">Close the page.</span></span>
9. <span data-ttu-id="5d095-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5d095-132">Close the page.</span></span>
10. <span data-ttu-id="5d095-133">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="5d095-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="5d095-134">Valige puult Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="5d095-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="5d095-135">Looge tuletatud mudel, et toetada juurdepääsu dokumendihalduse failidele.</span><span class="sxs-lookup"><span data-stu-id="5d095-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="5d095-136">Loote oma konfiguratsiooni kliendiarve mudelist, tuletades selle Microsofti antud konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="5d095-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="5d095-137">Kasutate seda konfiguratsiooni juurdepääsu juurutamiseks dokumendihalduse failidele ja nende kättesaadavaks tegemiseks elektroonilistele dokumentidele, mille selle mudeli põhjal loote.</span><span class="sxs-lookup"><span data-stu-id="5d095-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="5d095-138">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="5d095-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="5d095-139">Sisestage väljale Uus tekst Tuleta väärtusest Nimi: kliendiarve mudel, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5d095-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="5d095-140">Tippige väljale Nimi tekst Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="5d095-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="5d095-141">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="5d095-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]