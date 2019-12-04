---
title: Kulukäitumispoliitika loomine ja määramine kulujuhtimisüksusele
description: Kulukäitumine on kulude liigitamine fikseerituks või muutuvaks.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
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
ms.openlocfilehash: 16d9dceb4c2a22eab9a5ecb8501393444f20498b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187816"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="6ae3f-103">Kulukäitumispoliitika loomine ja määramine kulujuhtimisüksusele</span><span class="sxs-lookup"><span data-stu-id="6ae3f-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ae3f-104">Kulukäitumine on kulude liigitamine fikseerituks või muutuvaks.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="6ae3f-105">Poliitika ja vastavad reeglid tuleb poliitika jõustamiseks määrata kulu juhtseadmele.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="6ae3f-106">Selle protseduuri abil saate luua poliitika ja seejärel määrata selle kulu juhtseadmele.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="6ae3f-107">Kulukäitumise hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="6ae3f-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="6ae3f-108">Valige menüü Kuluarvestus jaotis Dimensioonid ja seejärel jaotis Dimensioonihierarhiad.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="6ae3f-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-109">Click New.</span></span>
3. <span data-ttu-id="6ae3f-110">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-110">Click Create.</span></span>
4. <span data-ttu-id="6ae3f-111">Tippige väljale Dimensioonihierarhia nimi väärtus Kulukäitumise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="6ae3f-112">Sisestage või valige väärtus väljal Dimensioon.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-113">Valige suvand Kuluelemendid.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="6ae3f-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-114">Click Save.</span></span>
7. <span data-ttu-id="6ae3f-115">Klõpsake käsku Kuva hierarhia.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="6ae3f-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-116">Click New.</span></span>
9. <span data-ttu-id="6ae3f-117">Tippige väärtus väljale Sõlme nimi.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="6ae3f-118">Sisestage fikseeritud omahind.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="6ae3f-119">Valige puus väärtus Kulukäitumise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="6ae3f-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-120">Click New.</span></span>
12. <span data-ttu-id="6ae3f-121">Tippige väärtus väljale Sõlme nimi.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="6ae3f-122">Sisestage muutuv kulu.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="6ae3f-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-123">Click Save.</span></span>
14. <span data-ttu-id="6ae3f-124">Valige puus väärtus Kulukäitumise hierarhia\Fikseeritud omahind.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="6ae3f-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-125">Click New.</span></span>
16. <span data-ttu-id="6ae3f-126">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="6ae3f-127">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-128">Dimensiooniliikmete vahemik võib sisaldada lünki, kuid liikmed ei tohi kattuda.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="6ae3f-129">Sisestage või valige väärtus väljal Sihtdimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-130">Dimensiooniliikmete vahemik võib sisaldada lünki, kuid liikmed ei tohi kattuda.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="6ae3f-131">Valige puus väärtus Kulukäitumise hierarhia\Muutuv kulu.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="6ae3f-132">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-132">Click New.</span></span>
21. <span data-ttu-id="6ae3f-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="6ae3f-134">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-135">Dimensiooniliikmete vahemik võib sisaldada lünki, kuid liikmed ei tohi kattuda.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="6ae3f-136">Sisestage või valige väärtus väljal Sihtdimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-137">Dimensiooniliikmete vahemik võib sisaldada lünki, kuid liikmed ei tohi kattuda.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="6ae3f-138">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="6ae3f-139">Poliitika ja reeglite loomine</span><span class="sxs-lookup"><span data-stu-id="6ae3f-139">Create the policy and rules</span></span>
1. <span data-ttu-id="6ae3f-140">Avage Kuluarvestus > Poliitikad > Kulukäitumise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="6ae3f-141">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-141">Click New.</span></span>
3. <span data-ttu-id="6ae3f-142">Tippige väärtus väljale Poliitika nimi.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="6ae3f-143">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-144">Valige äsja loodud poliitikahierarhia.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="6ae3f-145">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-146">Valige suvand Organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-146">Select Organization.</span></span>  
6. <span data-ttu-id="6ae3f-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-147">Click Save.</span></span>
7. <span data-ttu-id="6ae3f-148">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-148">Click New.</span></span>
8. <span data-ttu-id="6ae3f-149">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="6ae3f-150">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-151">Laiendage hierarhia, et valida väärtus Muutuv kulu.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="6ae3f-152">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="6ae3f-153">Vaikimisi on muutuja 100 protsenti.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="6ae3f-154">Klõpskae kulu juhtseadme suvandit Poliitikamäärangud.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="6ae3f-155">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-155">Click New.</span></span>
13. <span data-ttu-id="6ae3f-156">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="6ae3f-157">Sisestage kuupäev väljale Aruandluse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="6ae3f-158">Reeglite kehtivus sõltub kuupäevast ja kasutaja või süsteem saab muuta reegli aegunuks, kui luuakse uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="6ae3f-159">Sisestage või valige väärtus väljal Kulu juhtseade.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="6ae3f-160">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6ae3f-160">Click Save.</span></span>
