---
title: Kulukomplekti poliitika loomine
description: See protseduur näitab, kuidas luua kulukomplekti poliitikat ja selle jaoks reegleid.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6505d658103a4c34dfe7c7eb86ad4ea41515ccfb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261280"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="6c4b4-103">Kulukomplekti poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="6c4b4-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c4b4-104">See protseduur näitab, kuidas luua kulukomplekti poliitikat ja selle jaoks reegleid.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="6c4b4-105">Selle protseduuri loomiseks kasutati demoandmeid USP2.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="6c4b4-106">Poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="6c4b4-106">Create a policy</span></span>
1. <span data-ttu-id="6c4b4-107">Valige Kuluarvestus > Poliitikad > Kulukomplekti poliitikad.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="6c4b4-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-108">Click New.</span></span>
3. <span data-ttu-id="6c4b4-109">Tippige väärtus väljale Poliitika nimi.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="6c4b4-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6c4b4-111">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-112">Valige suvand Kulukomplekt CC.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="6c4b4-113">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-114">Valige suvand Kulukomplekt CC.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="6c4b4-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="6c4b4-116">Poliitika jaoks reeglite loomine</span><span class="sxs-lookup"><span data-stu-id="6c4b4-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="6c4b4-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-117">Click New.</span></span>
2. <span data-ttu-id="6c4b4-118">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6c4b4-119">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-120">Valige 007.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-120">Select 007.</span></span>  
4. <span data-ttu-id="6c4b4-121">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-122">Valige suvand Kulukomplekt CE.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="6c4b4-123">Sisestage või valige väärtus väljal Teisene kuluelement.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-124">Näiteks vastendage teisene kuluelement CC-007 kulukeskusega.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="6c4b4-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-125">Click New.</span></span>
7. <span data-ttu-id="6c4b4-126">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="6c4b4-127">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-128">Valige 008.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-128">Select 008.</span></span>  
9. <span data-ttu-id="6c4b4-129">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-130">Valige suvand Kulukomplekt CE.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="6c4b4-131">Sisestage või valige väärtus väljal Teisene kuluelement.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-132">Näiteks vastendage teisene kuluelement CC-008 kulukeskusega.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="6c4b4-133">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-133">Click New.</span></span>
12. <span data-ttu-id="6c4b4-134">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="6c4b4-135">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-136">Valige 009.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-136">Select 009.</span></span>  
14. <span data-ttu-id="6c4b4-137">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-138">Valige suvand Kulukomplekt CE.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="6c4b4-139">Sisestage või valige väärtus väljal Teisene kuluelement.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="6c4b4-140">Näiteks vastendage teisene kuluelement CC-009 kulukeskusega.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="6c4b4-141">Jätkake, kuni kõik kulukeskused on vastendatud vastavate teiseste kuluelementidega.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="6c4b4-142">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6c4b4-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]