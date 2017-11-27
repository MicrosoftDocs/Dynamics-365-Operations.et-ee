--- 
title: Elektroonilise aruandluse (ER) loendamis- ja liitmisvormingu loomine
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5d4f57ae2a309d9e15c1afe60c3e91d7d7eb3870
ms.openlocfilehash: 3c4ae958a03d4681a85f5b83d81fe64b9ac99cf5
ms.contentlocale: et-ee
ms.lasthandoff: 11/02/2017

---
# <a name="create-format-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="c9597-103">Elektroonilise aruandluse (ER) loendamis- ja liitmisvormingu loomine</span><span class="sxs-lookup"><span data-stu-id="c9597-103">Create format for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9597-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="c9597-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="c9597-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="c9597-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c9597-106">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="c9597-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="c9597-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="c9597-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="c9597-108">Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile</span><span class="sxs-lookup"><span data-stu-id="c9597-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="c9597-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="c9597-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c9597-110">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="c9597-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="c9597-111">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="c9597-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="c9597-112">Valige ettevõtte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c9597-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="c9597-113">pakkuja.</span><span class="sxs-lookup"><span data-stu-id="c9597-113">provider.</span></span>
3. <span data-ttu-id="c9597-114">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="c9597-114">Click Repositories.</span></span>
    * <span data-ttu-id="c9597-115">Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="c9597-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="c9597-116">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c9597-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="c9597-117">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="c9597-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="c9597-118">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="c9597-118">Click Create repository.</span></span>
7. <span data-ttu-id="c9597-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c9597-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="c9597-120">Microsofti pakutavate intrastati konfiguratsioonide saamine</span><span class="sxs-lookup"><span data-stu-id="c9597-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="c9597-121">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="c9597-121">Click Open.</span></span>
2. <span data-ttu-id="c9597-122">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="c9597-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="c9597-123">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="c9597-123">Click Import.</span></span>
    * <span data-ttu-id="c9597-124">Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.1.</span><span class="sxs-lookup"><span data-stu-id="c9597-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="c9597-125">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="c9597-125">Click Yes.</span></span>
5. <span data-ttu-id="c9597-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c9597-126">Close the page.</span></span>
6. <span data-ttu-id="c9597-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c9597-127">Close the page.</span></span>
7. <span data-ttu-id="c9597-128">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="c9597-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="c9597-129">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="c9597-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="c9597-130">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="c9597-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


