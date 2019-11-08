---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa – vormingu loomine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e85109cd0448383ba231cbec1bdeeb9dcd2db805
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550782"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="3aeff-103">Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa – vormingu loomine)</span><span class="sxs-lookup"><span data-stu-id="3aeff-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3aeff-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="3aeff-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="3aeff-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="3aeff-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="3aeff-106">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="3aeff-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="3aeff-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="3aeff-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="3aeff-108">Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile</span><span class="sxs-lookup"><span data-stu-id="3aeff-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="3aeff-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="3aeff-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="3aeff-110">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="3aeff-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="3aeff-111">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="3aeff-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="3aeff-112">Valige ettevõtte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3aeff-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="3aeff-113">pakkuja.</span><span class="sxs-lookup"><span data-stu-id="3aeff-113">provider.</span></span>
3. <span data-ttu-id="3aeff-114">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="3aeff-114">Click Repositories.</span></span>
    * <span data-ttu-id="3aeff-115">Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="3aeff-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="3aeff-116">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="3aeff-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="3aeff-117">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="3aeff-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="3aeff-118">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="3aeff-118">Click Create repository.</span></span>
7. <span data-ttu-id="3aeff-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3aeff-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="3aeff-120">Microsofti pakutavate intrastati konfiguratsioonide saamine</span><span class="sxs-lookup"><span data-stu-id="3aeff-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="3aeff-121">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="3aeff-121">Click Open.</span></span>
2. <span data-ttu-id="3aeff-122">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="3aeff-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="3aeff-123">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="3aeff-123">Click Import.</span></span>
    * <span data-ttu-id="3aeff-124">Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.1.</span><span class="sxs-lookup"><span data-stu-id="3aeff-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="3aeff-125">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="3aeff-125">Click Yes.</span></span>
5. <span data-ttu-id="3aeff-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3aeff-126">Close the page.</span></span>
6. <span data-ttu-id="3aeff-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3aeff-127">Close the page.</span></span>
7. <span data-ttu-id="3aeff-128">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="3aeff-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="3aeff-129">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="3aeff-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="3aeff-130">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="3aeff-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

