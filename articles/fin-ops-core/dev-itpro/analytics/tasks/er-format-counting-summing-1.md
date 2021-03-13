---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa – vormingu loomine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse vormingut juba loodud tekstiväljundi andmete põhjal loendama ja liitma. (1. osa)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a3639b5ac28f8a571642e983906d658dabf05b1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093018"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="6de01-104">Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa – vormingu loomine)</span><span class="sxs-lookup"><span data-stu-id="6de01-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6de01-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="6de01-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="6de01-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="6de01-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="6de01-107">Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.</span><span class="sxs-lookup"><span data-stu-id="6de01-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="6de01-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="6de01-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="6de01-109">Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile</span><span class="sxs-lookup"><span data-stu-id="6de01-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6de01-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="6de01-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6de01-111">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="6de01-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="6de01-112">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="6de01-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="6de01-113">Valige ettevõte „Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="6de01-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="6de01-114">pakkuja.</span><span class="sxs-lookup"><span data-stu-id="6de01-114">provider.</span></span>
3. <span data-ttu-id="6de01-115">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="6de01-115">Click Repositories.</span></span>
    * <span data-ttu-id="6de01-116">Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="6de01-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="6de01-117">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="6de01-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="6de01-118">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="6de01-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="6de01-119">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="6de01-119">Click Create repository.</span></span>
7. <span data-ttu-id="6de01-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6de01-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="6de01-121">Microsofti pakutavate intrastati konfiguratsioonide saamine</span><span class="sxs-lookup"><span data-stu-id="6de01-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6de01-122">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="6de01-122">Click Open.</span></span>
2. <span data-ttu-id="6de01-123">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="6de01-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="6de01-124">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="6de01-124">Click Import.</span></span>
    * <span data-ttu-id="6de01-125">Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.1.</span><span class="sxs-lookup"><span data-stu-id="6de01-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="6de01-126">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="6de01-126">Click Yes.</span></span>
5. <span data-ttu-id="6de01-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6de01-127">Close the page.</span></span>
6. <span data-ttu-id="6de01-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6de01-128">Close the page.</span></span>
7. <span data-ttu-id="6de01-129">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="6de01-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="6de01-130">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="6de01-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="6de01-131">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="6de01-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

