---
title: Kuluobjekti kontrolleri pääsuõiguste konfigureerimine
description: Selle protseduuri abil saate konfigureerida kuluobjekti kontrollija pääsuõigusi.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b7018f9d4926321341af94efd13911e2c69f5f5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "351167"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="1c0af-103">Kuluobjekti kontrolleri pääsuõiguste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1c0af-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c0af-104">Selle protseduuri abil saate konfigureerida kuluobjekti kontrollija pääsuõigusi.</span><span class="sxs-lookup"><span data-stu-id="1c0af-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="1c0af-105">See salvestis kasutab USP2 demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="1c0af-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="1c0af-106">Kuluobjekti kontrollija rolli määramine</span><span class="sxs-lookup"><span data-stu-id="1c0af-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="1c0af-107">Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.</span><span class="sxs-lookup"><span data-stu-id="1c0af-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="1c0af-108">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="1c0af-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1c0af-109">Näiteks saate filtreerida välja Kasutajanimi väärtuse "alicia" järgi.</span><span class="sxs-lookup"><span data-stu-id="1c0af-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="1c0af-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1c0af-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1c0af-111">Klõpsake suvandit Määra rollid.</span><span class="sxs-lookup"><span data-stu-id="1c0af-111">Click Assign roles.</span></span>
5. <span data-ttu-id="1c0af-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1c0af-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="1c0af-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1c0af-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="1c0af-114">Juurdepääsuloendi turbe lubamine</span><span class="sxs-lookup"><span data-stu-id="1c0af-114">Enable access list security</span></span>
1. <span data-ttu-id="1c0af-115">Valige menüü Kuluarvestus jaotis Dimensioonid ja seejärel jaotis Dimensioonihierarhiad.</span><span class="sxs-lookup"><span data-stu-id="1c0af-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="1c0af-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1c0af-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1c0af-117">Valige suvand Organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="1c0af-117">Select Organization.</span></span>  
3. <span data-ttu-id="1c0af-118">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="1c0af-118">Click Edit.</span></span>
4. <span data-ttu-id="1c0af-119">Valige väljal Juurdepääsuloendi hierarhia väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="1c0af-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="1c0af-120">Klõpsake käsku Kuva hierarhia.</span><span class="sxs-lookup"><span data-stu-id="1c0af-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="1c0af-121">Kasutajale pääsuõiguste määramine</span><span class="sxs-lookup"><span data-stu-id="1c0af-121">Assign access rights to user</span></span>
1. <span data-ttu-id="1c0af-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1c0af-122">Click New.</span></span>
2. <span data-ttu-id="1c0af-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1c0af-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="1c0af-124">Sisestage või valige väärtus väljal Kasutaja ID.</span><span class="sxs-lookup"><span data-stu-id="1c0af-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="1c0af-125">Valige suvand Administraator.</span><span class="sxs-lookup"><span data-stu-id="1c0af-125">Select Admin.</span></span>  
4. <span data-ttu-id="1c0af-126">Valige puus väärtus "Organization\CEO\CFO\FIM".</span><span class="sxs-lookup"><span data-stu-id="1c0af-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="1c0af-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1c0af-127">Click New.</span></span>
6. <span data-ttu-id="1c0af-128">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1c0af-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="1c0af-129">Sisestage või valige väärtus väljal Kasutaja ID.</span><span class="sxs-lookup"><span data-stu-id="1c0af-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="1c0af-130">Valige Alicia.</span><span class="sxs-lookup"><span data-stu-id="1c0af-130">Select Alicia.</span></span>  
8. <span data-ttu-id="1c0af-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1c0af-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="1c0af-132">Pääsuõiguste lubamine kuluarvestuses</span><span class="sxs-lookup"><span data-stu-id="1c0af-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="1c0af-133">Valige menüü Kuluarvestus > Seadistus > Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="1c0af-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="1c0af-134">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="1c0af-134">Click the General tab.</span></span>
3. <span data-ttu-id="1c0af-135">Valige väljal Luba kuvamise juurdepääs kuluobjekti dimensiooniliikmete jaoks väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="1c0af-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="1c0af-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1c0af-136">Click Save.</span></span>
5. <span data-ttu-id="1c0af-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1c0af-137">Close the page.</span></span>
6. <span data-ttu-id="1c0af-138">Valige menüü Kuluarvestus > Seadistus > Kulujuhtimise tööruumi konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="1c0af-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="1c0af-139">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="1c0af-139">Click Edit.</span></span>
8. <span data-ttu-id="1c0af-140">Valige väljal Avaldatud väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="1c0af-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="1c0af-141">Kui klõpsate nuppu Jah, saab kasutaja, kellele on määratud üks järgmisest neljast rollist, vaadata aruandeid kulude juhtimise tööruumis: kuluarvestuse haldur, kuluarvestaja, kuluarvestuse spetsialist ja kuluobjekti kontrollija.</span><span class="sxs-lookup"><span data-stu-id="1c0af-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="1c0af-142">Kui klõpsate nuppu Ei, saab ainult kasutaja, kellele on määratud üks järgmistest rollidest, vaadata aruandeid: kuluarvestuse haldur, kuluarvestaja ja kuluarvestuse spetsialist.</span><span class="sxs-lookup"><span data-stu-id="1c0af-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="1c0af-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1c0af-143">Click Save.</span></span>

