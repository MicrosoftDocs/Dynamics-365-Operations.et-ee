---
title: Elektroonilise aruandluse (ER) mudelivastenduse konfiguratsioonide loomine
description: Selle protseduuriga saate kujundada uue elektroonilise aruandluse (ER) mudeli vastendamise konfiguratsiooni ja kasutada sisseehitatud ER-i funktsioone tõhusate koondarvutuste jaoks.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 614ef06fcf5761f1cf2afb6e7655558d2858d763
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544952"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="092c0-103">Elektroonilise aruandluse (ER) mudelivastenduse konfiguratsioonide loomine</span><span class="sxs-lookup"><span data-stu-id="092c0-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="092c0-104">Selle protseduuriga saate kujundada uue elektroonilise aruandluse (ER) mudeli vastendamise konfiguratsiooni ja kasutada sisseehitatud ER-i funktsioone tõhusate koondarvutuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="092c0-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="092c0-105">Selles protseduuris loote konfiguratsiooni näidisettevõttele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="092c0-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="092c0-106">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="092c0-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="092c0-107">Need etapid saab lõpule viia ükskõik millise andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="092c0-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="092c0-108">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” etapid.</span><span class="sxs-lookup"><span data-stu-id="092c0-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="092c0-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="092c0-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="092c0-110">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="092c0-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="092c0-111">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="092c0-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="092c0-112">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="092c0-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="092c0-113">Klõpsake valikut Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="092c0-113">Click Show filters.</span></span>
4. <span data-ttu-id="092c0-114">Sisestage väljale „Nimi” filtriväärtus „Intrastat” ja kasutage filtri tehtemärki „algab järgmisega”.</span><span class="sxs-lookup"><span data-stu-id="092c0-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="092c0-115">Rakendage see filter, et leida andmemudeli konfiguratsioon „Intrastat”.</span><span class="sxs-lookup"><span data-stu-id="092c0-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="092c0-116">See mudel on võib-olla juba konfiguratsioonide puus olemas.</span><span class="sxs-lookup"><span data-stu-id="092c0-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="092c0-117">Kui on, jätke järgmine alamülesanne vahele.</span><span class="sxs-lookup"><span data-stu-id="092c0-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="092c0-118">Microsofti pakutava Intrastati mudeli konfiguratsiooni hankimine</span><span class="sxs-lookup"><span data-stu-id="092c0-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="092c0-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="092c0-119">Close the page.</span></span>
2. <span data-ttu-id="092c0-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="092c0-120">Close the page.</span></span>
3. <span data-ttu-id="092c0-121">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="092c0-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="092c0-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="092c0-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="092c0-123">Valige Microsofti pakkuja paan.</span><span class="sxs-lookup"><span data-stu-id="092c0-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="092c0-124">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="092c0-124">Click Repositories.</span></span>
    * <span data-ttu-id="092c0-125">Klõpsake Microsofti pakkuja paanil valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="092c0-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="092c0-126">Klõpsake valikut Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="092c0-126">Click Show filters.</span></span>
7. <span data-ttu-id="092c0-127">Sisestage väljale „Tüübi nimi” filtriväärtus „ressursid” ja kasutage filtri tehtemärki „sisaldab”.</span><span class="sxs-lookup"><span data-stu-id="092c0-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="092c0-128">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="092c0-128">Click Open.</span></span>
9. <span data-ttu-id="092c0-129">Tehke puul valik „Intrastati mudel”.</span><span class="sxs-lookup"><span data-stu-id="092c0-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="092c0-130">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="092c0-130">Click Import.</span></span>
11. <span data-ttu-id="092c0-131">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="092c0-131">Click Yes.</span></span>
    * <span data-ttu-id="092c0-132">Importisite ER-i mudeli konfiguratsiooni, mis sisaldab andmemudelit, millega saate uurida, kuidas saab kasutada uut ER-i funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="092c0-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="092c0-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="092c0-133">Close the page.</span></span>
13. <span data-ttu-id="092c0-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="092c0-134">Close the page.</span></span>
14. <span data-ttu-id="092c0-135">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="092c0-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="092c0-136">Uue mudelivastenduse konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="092c0-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="092c0-137">Tehke puul valik „Intrastati mudel”.</span><span class="sxs-lookup"><span data-stu-id="092c0-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="092c0-138">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="092c0-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="092c0-139">Väljale Uus sisestage „Intrastati andmemudelil põhinev mudeli vastendamine”.</span><span class="sxs-lookup"><span data-stu-id="092c0-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="092c0-140">Sisestage nimeväljale tekst „Intrastati näidise vastendamine”.</span><span class="sxs-lookup"><span data-stu-id="092c0-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="092c0-141">Intrastati näidise vastendamine</span><span class="sxs-lookup"><span data-stu-id="092c0-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="092c0-142">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="092c0-142">Click Create configuration.</span></span>

