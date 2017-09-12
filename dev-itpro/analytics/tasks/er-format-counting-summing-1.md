--- 
title: Elektroonilise aruandluse (ER) loendamis- ja liitmisvormingu loomine
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: cac3748182ba27735264acc947403d7b857f1b6e
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="f9889-103">Elektroonilise aruandluse (ER) loendamis- ja liitmisvormingu loomine</span><span class="sxs-lookup"><span data-stu-id="f9889-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9889-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="f9889-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="f9889-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="f9889-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f9889-106">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="f9889-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="f9889-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="f9889-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="f9889-108">Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile</span><span class="sxs-lookup"><span data-stu-id="f9889-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f9889-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="f9889-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f9889-110">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="f9889-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="f9889-111">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="f9889-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="f9889-112">Valige ettevõtte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f9889-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="f9889-113">pakkuja.</span><span class="sxs-lookup"><span data-stu-id="f9889-113">provider.</span></span>
3. <span data-ttu-id="f9889-114">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="f9889-114">Click Repositories.</span></span>
    * <span data-ttu-id="f9889-115">Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="f9889-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="f9889-116">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="f9889-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="f9889-117">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="f9889-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="f9889-118">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="f9889-118">Click Create repository.</span></span>
7. <span data-ttu-id="f9889-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f9889-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="f9889-120">Microsofti pakutavate intrastati konfiguratsioonide saamine</span><span class="sxs-lookup"><span data-stu-id="f9889-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f9889-121">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="f9889-121">Click Open.</span></span>
2. <span data-ttu-id="f9889-122">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="f9889-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="f9889-123">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="f9889-123">Click Import.</span></span>
    * <span data-ttu-id="f9889-124">Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.1.</span><span class="sxs-lookup"><span data-stu-id="f9889-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="f9889-125">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="f9889-125">Click Yes.</span></span>
5. <span data-ttu-id="f9889-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9889-126">Close the page.</span></span>
6. <span data-ttu-id="f9889-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9889-127">Close the page.</span></span>
7. <span data-ttu-id="f9889-128">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="f9889-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="f9889-129">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="f9889-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="f9889-130">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="f9889-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


