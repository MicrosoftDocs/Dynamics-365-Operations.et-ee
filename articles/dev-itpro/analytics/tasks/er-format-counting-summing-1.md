--- 
title: Loendamis- ja liitmisvormingu loomine
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7613b78d4a9ab63f5be9773a8699fe3ed94636eb
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-format-for-counting-and-summing"></a><span data-ttu-id="010fc-103">Loendamis- ja liitmisvormingu loomine</span><span class="sxs-lookup"><span data-stu-id="010fc-103">Create format for counting and summing</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="010fc-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="010fc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="010fc-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="010fc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="010fc-106">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="010fc-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="010fc-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="010fc-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="010fc-108">Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile</span><span class="sxs-lookup"><span data-stu-id="010fc-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="010fc-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="010fc-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="010fc-110">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="010fc-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="010fc-111">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="010fc-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="010fc-112">Valige ettevõtte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="010fc-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="010fc-113">pakkuja.</span><span class="sxs-lookup"><span data-stu-id="010fc-113">provider.</span></span>
3. <span data-ttu-id="010fc-114">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="010fc-114">Click Repositories.</span></span>
    * <span data-ttu-id="010fc-115">Kui on juba olemas hoidla tüübiga Operatsiooniressursid, siis jätke praeguse alamtoimingu ülejäänud etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="010fc-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="010fc-116">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="010fc-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="010fc-117">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="010fc-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="010fc-118">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="010fc-118">Click Create repository.</span></span>
7. <span data-ttu-id="010fc-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="010fc-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="010fc-120">Microsofti pakutavate intrastati konfiguratsioonide saamine</span><span class="sxs-lookup"><span data-stu-id="010fc-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="010fc-121">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="010fc-121">Click Open.</span></span>
2. <span data-ttu-id="010fc-122">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="010fc-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="010fc-123">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="010fc-123">Click Import.</span></span>
    * <span data-ttu-id="010fc-124">Klõpsake valikut Impordi valitud konfiguratsiooni versioonile 1.1.</span><span class="sxs-lookup"><span data-stu-id="010fc-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="010fc-125">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="010fc-125">Click Yes.</span></span>
5. <span data-ttu-id="010fc-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="010fc-126">Close the page.</span></span>
6. <span data-ttu-id="010fc-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="010fc-127">Close the page.</span></span>
7. <span data-ttu-id="010fc-128">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="010fc-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="010fc-129">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="010fc-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="010fc-130">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="010fc-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


