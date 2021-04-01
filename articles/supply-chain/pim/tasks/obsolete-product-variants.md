---
title: Aegunud tootevariantide leidmine
description: Protseduur näitab, kuidas leida aegunud väljastatud tooteid või tootevariante ja kuidas seostada toote elutsükli olek aegunud toodetega.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33f16cf8c731dc1a954ed94229b2a833510dac4f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245175"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="fceb1-103">Aegunud tootevariantide leidmine</span><span class="sxs-lookup"><span data-stu-id="fceb1-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fceb1-104">Protseduur näitab, kuidas leida aegunud väljastatud tooteid või tootevariante ja kuidas seostada toote elutsükli olek aegunud toodetega.</span><span class="sxs-lookup"><span data-stu-id="fceb1-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="fceb1-105">Eelnõue: peate määratlema vähemalt ühe toote elutsükli oleku, mis on planeerimise jaoks passiivne, enne kui saate selle ülesande juhendit esitada.</span><span class="sxs-lookup"><span data-stu-id="fceb1-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="fceb1-106">Simulatsiooni käivitamine</span><span class="sxs-lookup"><span data-stu-id="fceb1-106">Run a simulation</span></span>
1. <span data-ttu-id="fceb1-107">Avage jaotis Tooteteabe haldus > Perioodilised ülesanded > Aegunud toodete elutsükli oleku muutmine.</span><span class="sxs-lookup"><span data-stu-id="fceb1-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="fceb1-108">Väljal Uue toote elutsükli olek sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="fceb1-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="fceb1-109">Valige Jah väljal Simulatsiooni käivitamine toote andmeid värskendamata.</span><span class="sxs-lookup"><span data-stu-id="fceb1-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="fceb1-110">Sisestage arv väljale Selle arvu päevade jooksul loodud toodete välistamine.</span><span class="sxs-lookup"><span data-stu-id="fceb1-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="fceb1-111">Sisestage arv väljale Kannetes kasutatud toodete välistamine (päevade arv).</span><span class="sxs-lookup"><span data-stu-id="fceb1-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="fceb1-112">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="fceb1-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="fceb1-113">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="fceb1-113">Click Filter.</span></span>
8. <span data-ttu-id="fceb1-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="fceb1-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fceb1-115">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="fceb1-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="fceb1-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fceb1-116">Click OK.</span></span>
11. <span data-ttu-id="fceb1-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fceb1-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="fceb1-118">Soovitatav on käitada simulatsiooni partiina, kui plaanite otsida suurt hulka tooteid.</span><span class="sxs-lookup"><span data-stu-id="fceb1-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="fceb1-119">Veenduge ka, et simulatsiooni ei käitataks ettevõtte kõige aktiivsemal tööajal.</span><span class="sxs-lookup"><span data-stu-id="fceb1-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="fceb1-120">Simulatsiooni tulemuste ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="fceb1-120">Review the simulation results</span></span>
1. <span data-ttu-id="fceb1-121">Avage jaotis Tooteteabe haldus > Päringud ja aruanded > Toote elutsükli oleku haldamise ajalugu.</span><span class="sxs-lookup"><span data-stu-id="fceb1-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="fceb1-122">Sellel lehel saate üle vaadata simulatsiooni tulemused ja hinnata, kui palju tooteid ning tootevariante uue toote elutsükli olekuga seostatakse, kui värskendus käivitatakse ilma simulatsioonita.</span><span class="sxs-lookup"><span data-stu-id="fceb1-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="fceb1-123">Aegunud toodete elutsükli oleku värskenduse käitamine</span><span class="sxs-lookup"><span data-stu-id="fceb1-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="fceb1-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fceb1-124">Close the page.</span></span>
2. <span data-ttu-id="fceb1-125">Avage jaotis Tooteteabe haldus > Perioodilised ülesanded > Aegunud toodete elutsükli oleku muutmine.</span><span class="sxs-lookup"><span data-stu-id="fceb1-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="fceb1-126">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="fceb1-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="fceb1-127">Pange tähele, et viimane valik on salvestatud.</span><span class="sxs-lookup"><span data-stu-id="fceb1-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="fceb1-128">Valige Ei väljal Simulatsiooni käivitamine toote andmeid värskendamata.</span><span class="sxs-lookup"><span data-stu-id="fceb1-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="fceb1-129">Laiendage jaotist Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="fceb1-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="fceb1-130">Olenevalt mõjutatud toodete ja tootevariantide arvust kaaluge toimingu käitamist pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="fceb1-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="fceb1-131">Veenduge, et te ei käitaks suurt värskendustööd ettevõtte kõige aktiivsemal tööajal.</span><span class="sxs-lookup"><span data-stu-id="fceb1-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="fceb1-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fceb1-132">Click OK.</span></span>
7. <span data-ttu-id="fceb1-133">Avage jaotis Tooteteabe haldus > Päringud ja aruanded > Toote elutsükli oleku haldamise ajalugu.</span><span class="sxs-lookup"><span data-stu-id="fceb1-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="fceb1-134">Vaadake üle muudetud väljastatud tooted ja tootevariandid.</span><span class="sxs-lookup"><span data-stu-id="fceb1-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="fceb1-135">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="fceb1-135">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]