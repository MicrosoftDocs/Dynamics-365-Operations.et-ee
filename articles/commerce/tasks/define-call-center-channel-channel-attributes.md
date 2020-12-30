---
title: Kõnekeskuse kanalite loomine ja kanali atribuutide määratlemine
description: See protseduur selgitab uue kanali loomist ja kanali atribuutide määratlemist.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2f99029195a8b783f0d12990d4e8bab0bb348d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411720"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="d52df-103">Kõnekeskuse kanalite loomine ja kanali atribuutide määratlemine</span><span class="sxs-lookup"><span data-stu-id="d52df-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d52df-104">See protseduur selgitab uue ärikanali loomist ja kanali atribuutide konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="d52df-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="d52df-105">Selle tegevuse loomisel kasutati demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d52df-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="d52df-106">See protseduur on ette nähtud Kaubanduse IT-rollile.</span><span class="sxs-lookup"><span data-stu-id="d52df-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="d52df-107">Uue poe loomine</span><span class="sxs-lookup"><span data-stu-id="d52df-107">Create new store</span></span>
1. <span data-ttu-id="d52df-108">Avage Kõik tööruumid > Kanali juurutamine.</span><span class="sxs-lookup"><span data-stu-id="d52df-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="d52df-109">Klõpsake valikut Uus kanal.</span><span class="sxs-lookup"><span data-stu-id="d52df-109">Click New channel.</span></span>
3. <span data-ttu-id="d52df-110">Klõpsake nuppu Kauplus.</span><span class="sxs-lookup"><span data-stu-id="d52df-110">Click Store.</span></span>
4. <span data-ttu-id="d52df-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d52df-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d52df-112">Sisestage väljale Kaupluse number soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d52df-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="d52df-113">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d52df-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d52df-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d52df-116">Tehke valik väljal Salvesta ajavöönd.</span><span class="sxs-lookup"><span data-stu-id="d52df-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="d52df-117">Klõpsake väljal Kanali profiil otsingu avamiseks ripploendinuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d52df-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d52df-119">Klõpsake väljal Keel otsingu avamiseks ripploendinuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="d52df-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="d52df-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d52df-122">Klõpsake väljal Käibemaks otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="d52df-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="d52df-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d52df-125">Klõpsake väljal Kliendi aadressiraamat otsingu avamiseks ripploendinuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d52df-126">Valige aadressiraamat, mida kasutatakse klientide linkimiseks selle kauplusega.</span><span class="sxs-lookup"><span data-stu-id="d52df-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="d52df-127">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="d52df-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="d52df-129">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="d52df-129">Click Select.</span></span>
22. <span data-ttu-id="d52df-130">Klõpsake väljal Employee address book (Töötajate aadressiraamat) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d52df-131">Valige aadressiraamat, mida kasutatakse kassapidajate linkimiseks selle kanaliga.</span><span class="sxs-lookup"><span data-stu-id="d52df-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="d52df-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="d52df-133">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="d52df-134">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="d52df-134">Click Select.</span></span>
26. <span data-ttu-id="d52df-135">Klõpsake väljal Vaikeklient otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="d52df-136">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="d52df-137">Laiendage või ahendage jaotis Ekraani paigutus.</span><span class="sxs-lookup"><span data-stu-id="d52df-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="d52df-138">Klõpsake väljal Ekraani paigutuse ID otsingu avamiseks ripploendinuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d52df-139">Valige selle kaupluse jaoks POS-i ekraani vaikepaigutus.</span><span class="sxs-lookup"><span data-stu-id="d52df-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="d52df-140">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="d52df-141">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="d52df-142">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="d52df-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="d52df-143">Klõpsake valikut Kanali atribuudid.</span><span class="sxs-lookup"><span data-stu-id="d52df-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="d52df-144">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d52df-144">Click New.</span></span>
35. <span data-ttu-id="d52df-145">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="d52df-146">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="d52df-147">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="d52df-148">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d52df-148">Click Save.</span></span>
39. <span data-ttu-id="d52df-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d52df-149">Close the page.</span></span>
40. <span data-ttu-id="d52df-150">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="d52df-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="d52df-151">Klõpsake suvandit Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="d52df-151">Click Payment methods.</span></span>
42. <span data-ttu-id="d52df-152">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d52df-152">Click New.</span></span>
43. <span data-ttu-id="d52df-153">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="d52df-154">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="d52df-155">Laiendage või ahendage jaotist Sisestamine.</span><span class="sxs-lookup"><span data-stu-id="d52df-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="d52df-156">Määrake väljal Kontonumber soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="d52df-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="d52df-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d52df-157">Click Save.</span></span>
48. <span data-ttu-id="d52df-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d52df-158">Close the page.</span></span>
49. <span data-ttu-id="d52df-159">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="d52df-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="d52df-160">Klõpsake valikut Sularaha deklaratsioon.</span><span class="sxs-lookup"><span data-stu-id="d52df-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="d52df-161">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d52df-161">Click New.</span></span>
52. <span data-ttu-id="d52df-162">Sisestage arv väljale Summa kandevaluutas.</span><span class="sxs-lookup"><span data-stu-id="d52df-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="d52df-163">Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="d52df-164">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="d52df-165">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="d52df-166">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d52df-166">Click Save.</span></span>
57. <span data-ttu-id="d52df-167">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d52df-167">Close the page.</span></span>
58. <span data-ttu-id="d52df-168">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="d52df-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="d52df-169">Klõpsake valikut Kaupluselokaatori grupi määramine.</span><span class="sxs-lookup"><span data-stu-id="d52df-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="d52df-170">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d52df-170">Click New.</span></span>
61. <span data-ttu-id="d52df-171">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d52df-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="d52df-172">Klõpsake väljal Lokaatori grupp otsingu avamiseks ripploendinuppu.</span><span class="sxs-lookup"><span data-stu-id="d52df-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="d52df-173">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d52df-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="d52df-174">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d52df-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="d52df-175">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d52df-175">Click Save.</span></span>
66. <span data-ttu-id="d52df-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d52df-176">Close the page.</span></span>

