---
title: " Püsikliendiprogrammide määratlemine"
description: See protseduur selgitab kahe püsikliendijärguga püsikliendiprogrammi seadistamist.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b178f1c6a71b34b70db4dbcd1765117215a4d2a1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022251"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="f3dbe-103"> Püsikliendiprogrammide määratlemine</span><span class="sxs-lookup"><span data-stu-id="f3dbe-103">Define loyalty programs</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f3dbe-104">See protseduur selgitab kahe püsikliendijärguga püsikliendiprogrammi seadistamist.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="f3dbe-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="f3dbe-106">Avage Jaemüük ja kaubandus > ..</span><span class="sxs-lookup"><span data-stu-id="f3dbe-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="f3dbe-107">> Püsikliendiprogrammid.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="f3dbe-108">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-108">Click New.</span></span>
3. <span data-ttu-id="f3dbe-109">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f3dbe-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f3dbe-111">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-111">Click Add line.</span></span>
6. <span data-ttu-id="f3dbe-112">Sisestage arv väljale Tase.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="f3dbe-113">Sisestage püsikliendijärgu nimi väljale Järk.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="f3dbe-114">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="f3dbe-115">Klõpsake väljal Kuupäevaintervall otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f3dbe-116">See kuupäevaintervall peab ulatuma tulevikku.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-116">This date interval should extend into the future.</span></span> <span data-ttu-id="f3dbe-117">Näiteks kui kuldkliendi järgu jaoks valitud kuupäevaintervall on üheaastane periood, saavad kõik kuldkliendi järku kvalifitseerunud kliendid ühe aasta jooksul kuldkliendi järgule määratud preemiaid.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="f3dbe-118">Kui klient kvalifitseerub järgus olles uuesti kuldkliendi järgule, pikendatakse tema järgu oleku aegumise kuupäeva ühe aasta võrra, alates uuesti kvalifitseerumise kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="f3dbe-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f3dbe-120">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-120">Click Add line.</span></span>
12. <span data-ttu-id="f3dbe-121">Sisestage arv väljale Tase.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="f3dbe-122">Sisestage püsikliendijärgu nimi väljale Järk.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="f3dbe-123">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="f3dbe-124">Klõpsake väljal Kuupäevaintervall otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="f3dbe-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f3dbe-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-126">Click Save.</span></span>
18. <span data-ttu-id="f3dbe-127">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f3dbe-128">Järgureeglid määratlevad ajaperioodil teenitavate preemiapunktide vajaliku miinimumarvu järgule kvalifitseerumiseks.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="f3dbe-129">Laiendage jaotist Järgureeglid.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="f3dbe-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-130">Click New.</span></span>
    * <span data-ttu-id="f3dbe-131">Iga järgu kohta võib olla rohkem kui üks järgureegel.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="f3dbe-132">Näiteks võib teil olla järgule kvalifitseerumiseks kolm erinevat kriteeriumit: kuu jooksul kulutatud 500 dollarit, aasta jooksul kulutatud 1000 dollarit ja ühe aasta jooksul tehtud 20 kannet.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="f3dbe-133">Selleks peate looma kolm järgureeglit.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="f3dbe-134">Klõpsake väljal Preemiapunktid otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f3dbe-135">See peab olema mittelunastatav püsikliendi preemiapunkt.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="f3dbe-136">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="f3dbe-137">Sisestage number väljale Minimaalsed väljastatud punktid.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="f3dbe-138">Kui kliendid kvalifitseeruvad püsikliendijärgule üksnes programmis osaledes, sisestage madalaima järgu väljale väärtus 0.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="f3dbe-139">Klõpsake väljal Hindamise kuupäevaintervall otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f3dbe-140">See kuupäevaintervall peab ulatuma minevikku.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-140">This date interval should extend into the past.</span></span> <span data-ttu-id="f3dbe-141">Selle kuupäevaintervalli jooksul teenitud punkte arvestatakse edasisuunas, kuni on saavutatud väljastatud punktide miinimumväärtus.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="f3dbe-142">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="f3dbe-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-143">Click Save.</span></span>
27. <span data-ttu-id="f3dbe-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="f3dbe-145">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-145">Click New.</span></span>
29. <span data-ttu-id="f3dbe-146">Klõpsake väljal Preemiapunktid otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="f3dbe-147">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="f3dbe-148">Sisestage number väljale Minimaalsed väljastatud punktid.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="f3dbe-149">Klõpsake väljal Hindamise kuupäevaintervall otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f3dbe-150">See kuupäevaintervall peab ulatuma minevikku.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="f3dbe-151">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="f3dbe-152">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-152">Click Save.</span></span>
35. <span data-ttu-id="f3dbe-153">Klõpsake suvandit Hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-153">Click Price groups.</span></span>
    * <span data-ttu-id="f3dbe-154">Kui soovite anda püsiklientidele allahindlusi</span><span class="sxs-lookup"><span data-stu-id="f3dbe-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="f3dbe-155">peate püsikliendiprogrammile vähemalt ühe hinnagrupi ja allahindlustele hinnagrupid määrama.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="f3dbe-156">Erinevat tüüpi allahindlusüksustes pole soovitatav kasutada erinevaid hinnagruppe.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="f3dbe-157">Näiteks ärge kasutage sama hinnagruppi püsikliendi allahindluse ja kanali allahindluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="f3dbe-158">Klõpsake väljal Hinnagrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f3dbe-159">Link Hinnagrupid lehe ülaosas on mõeldud püsikliendiprogrammi jaoks.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="f3dbe-160">Hinnagruppide link kiirkaardil Programmijärgud on mõeldud ainult kindlale püsikliendijärgule.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="f3dbe-161">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="f3dbe-162">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-162">Click Save.</span></span>
39. <span data-ttu-id="f3dbe-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-163">Close the page.</span></span>
40. <span data-ttu-id="f3dbe-164">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f3dbe-164">Click Save.</span></span>
