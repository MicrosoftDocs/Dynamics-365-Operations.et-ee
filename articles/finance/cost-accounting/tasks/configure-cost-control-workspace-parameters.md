---
title: Kulujuhtimise tööruumi parameetrite konfigureerimine
description: Selle protseduuri abil saate konfigureerida kulude juhtimise tööruumi nii, et organisatsiooni erinevate tasemete haldurid saavad ülevaate oma kuluobjektidest, nt kulukeskustest ja tootegruppidest.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11e1edc435cac100bfef15299251c1863103b568
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759204"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="efce3-103">Kulujuhtimise tööruumi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="efce3-103">Configure cost control workspace parameters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efce3-104">Selle protseduuri abil saate konfigureerida kulude juhtimise tööruumi nii, et organisatsiooni erinevate tasemete haldurid saavad ülevaate oma kuluobjektidest, nt kulukeskustest ja tootegruppidest.</span><span class="sxs-lookup"><span data-stu-id="efce3-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="efce3-105">Selle salvestise loomisel kasutati demoettevõtet USP2.</span><span class="sxs-lookup"><span data-stu-id="efce3-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="efce3-106">Valige menüü Kuluarvestus > Seadistus > Kulujuhtimise tööruumi konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="efce3-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="efce3-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="efce3-107">Click New.</span></span>
3. <span data-ttu-id="efce3-108">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="efce3-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="efce3-109">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="efce3-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="efce3-110">Valige väljal Avaldatud väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="efce3-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="efce3-111">Kui klõpsate nuppu Jah, saab kasutaja, kellele on määratud üks nendest rollidest, vaadata aruannet kulude juhtimise tööruumis: kuluarvestuse haldur, kuluarvestaja, kuluarvestuse spetsialist või kuluobjekti kontrollija.</span><span class="sxs-lookup"><span data-stu-id="efce3-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="efce3-112">Kui klõpsate nuppu Ei, saavad ainult kasutajad, kellele on määratud üks nendest rollidest, vaadata aruannet kulude juhtimise tööruumis: kuluarvestuse haldur, kuluarvestaja või kuluarvestuse spetsialist.</span><span class="sxs-lookup"><span data-stu-id="efce3-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="efce3-113">Laiendage jaotis Andmete filtreerimine.</span><span class="sxs-lookup"><span data-stu-id="efce3-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="efce3-114">Sisestage või valige väärtus väljal Kulu juhtseade.</span><span class="sxs-lookup"><span data-stu-id="efce3-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="efce3-115">Sisestage või valige väärtus väljal Eelarve algne versioon.</span><span class="sxs-lookup"><span data-stu-id="efce3-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="efce3-116">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="efce3-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="efce3-117">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="efce3-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="efce3-118">Laiendage jaotis Arvutuskirje määramine.</span><span class="sxs-lookup"><span data-stu-id="efce3-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="efce3-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="efce3-119">Click New.</span></span>
13. <span data-ttu-id="efce3-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="efce3-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="efce3-121">Sisestage või valige väärtus väljal Rahanduskalendri periood.</span><span class="sxs-lookup"><span data-stu-id="efce3-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="efce3-122">Sisestage või valige väärtus väljal Tegelik versioon.</span><span class="sxs-lookup"><span data-stu-id="efce3-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="efce3-123">Laiendage rahandusperioode veerujaotises.</span><span class="sxs-lookup"><span data-stu-id="efce3-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="efce3-124">Valige väljal Praegune periood väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="efce3-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="efce3-125">Laiendage kulude kuvatavate veergude jaotis.</span><span class="sxs-lookup"><span data-stu-id="efce3-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="efce3-126">Valige väljal Fikseeritud omahind väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="efce3-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="efce3-127">Valige väljal Muutuv kulu väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="efce3-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="efce3-128">Valige väljal Kogumaksumus väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="efce3-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="efce3-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="efce3-129">Click Save.</span></span>
23. <span data-ttu-id="efce3-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="efce3-130">Close the page.</span></span>
24. <span data-ttu-id="efce3-131">Valige Kuluarvestus > Tööruumid > Kulude juhtimine.</span><span class="sxs-lookup"><span data-stu-id="efce3-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="efce3-132">Valige aruanne valitud rahandusperioodide fikseeritud, muutuvate, kogu- ja liigitamata kulude vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="efce3-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="efce3-133">Sisestage või valige väärtus väljal Rahanduskalendri periood.</span><span class="sxs-lookup"><span data-stu-id="efce3-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="efce3-134">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="efce3-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="efce3-135">Pärast kuluobjekti dimensiooni hierarhia valimist laiendage kuluelemendi dimensioon, et vaadata soovitud kuluväärtusi.</span><span class="sxs-lookup"><span data-stu-id="efce3-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="efce3-136">Näiteks saate väärtuse kuvamiseks laiendada hierarhiat tootmise üldkuluni.</span><span class="sxs-lookup"><span data-stu-id="efce3-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  

