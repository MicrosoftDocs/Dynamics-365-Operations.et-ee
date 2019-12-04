---
title: Kulueraldamispoliitika loomine ja määramine kulujuhtimisüksusele
description: Selle protseduuri abil saate luua ja määrata kulude eraldamise poliitika ja vastavad reeglid kulu juhtseadmele.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f0422a9aaf95184b556293bf6ebcaf4dcfb5b59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177353"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="782b5-103">Kulueraldamispoliitika loomine ja määramine kulujuhtimisüksusele</span><span class="sxs-lookup"><span data-stu-id="782b5-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="782b5-104">Selle protseduuri abil saate luua ja määrata kulude eraldamise poliitika ja vastavad reeglid kulu juhtseadmele.</span><span class="sxs-lookup"><span data-stu-id="782b5-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="782b5-105">See salvestis kasutab USP2 demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="782b5-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="782b5-106">Poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="782b5-106">Create a policy</span></span>
1. <span data-ttu-id="782b5-107">Avage Kuluarvestus > Poliitikad > Kulude eraldamise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="782b5-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="782b5-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="782b5-108">Click New.</span></span>
3. <span data-ttu-id="782b5-109">Tippige väärtus väljale Poliitika nimi.</span><span class="sxs-lookup"><span data-stu-id="782b5-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="782b5-110">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="782b5-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="782b5-111">Valige suvand Organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="782b5-111">Select Organization.</span></span>  
5. <span data-ttu-id="782b5-112">Sisestage või valige väärtus väljal Statistiline dimensioon.</span><span class="sxs-lookup"><span data-stu-id="782b5-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="782b5-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="782b5-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="782b5-114">Eraldusreeglite loomine</span><span class="sxs-lookup"><span data-stu-id="782b5-114">Create allocation rules</span></span>
1. <span data-ttu-id="782b5-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="782b5-115">Click New.</span></span>
2. <span data-ttu-id="782b5-116">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="782b5-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="782b5-117">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="782b5-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="782b5-118">Valige väljal Kulukäitumine väärtus Kokku.</span><span class="sxs-lookup"><span data-stu-id="782b5-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="782b5-119">Sisestage või valige väärtus väljal Eraldamise alus.</span><span class="sxs-lookup"><span data-stu-id="782b5-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="782b5-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="782b5-120">Click New.</span></span>
7. <span data-ttu-id="782b5-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="782b5-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="782b5-122">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="782b5-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="782b5-123">Valige väljal Kulukäitumine väärtus Kokku.</span><span class="sxs-lookup"><span data-stu-id="782b5-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="782b5-124">Sisestage või valige väärtus väljal Eraldamise alus.</span><span class="sxs-lookup"><span data-stu-id="782b5-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="782b5-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="782b5-125">Click New.</span></span>
12. <span data-ttu-id="782b5-126">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="782b5-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="782b5-127">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="782b5-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="782b5-128">Valige väljal Kulukäitumine väärtus Kokku.</span><span class="sxs-lookup"><span data-stu-id="782b5-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="782b5-129">Sisestage või valige väärtus väljal Eraldamise alus.</span><span class="sxs-lookup"><span data-stu-id="782b5-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="782b5-130">Jätkake, kuni olete kõik reeglid loonud.</span><span class="sxs-lookup"><span data-stu-id="782b5-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="782b5-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="782b5-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="782b5-132">Poliitika määramine kulu juhtseadmele</span><span class="sxs-lookup"><span data-stu-id="782b5-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="782b5-133">Klõpskae kulu juhtseadme suvandit Poliitikamäärangud.</span><span class="sxs-lookup"><span data-stu-id="782b5-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="782b5-134">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="782b5-134">Click New.</span></span>
3. <span data-ttu-id="782b5-135">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="782b5-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="782b5-136">Sisestage kuupäev väljale Aruandluse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="782b5-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="782b5-137">Reeglite kehtivus sõltub kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="782b5-137">The rules are date-effective.</span></span> <span data-ttu-id="782b5-138">Kasutaja või süsteem saab muuta reeglid aegunuks, kui luuakse uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="782b5-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="782b5-139">Sisestage või valige väärtus väljal Kulu juhtseade.</span><span class="sxs-lookup"><span data-stu-id="782b5-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="782b5-140">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="782b5-140">Click Save.</span></span>
