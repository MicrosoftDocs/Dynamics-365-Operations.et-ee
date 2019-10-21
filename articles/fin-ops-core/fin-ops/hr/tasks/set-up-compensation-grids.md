---
title: Hüvitisruudustike häälestamine
description: Tasuruudustikke kasutatakse põhipalgaplaanide palgastruktuuri määratlemiseks ja säilitamiseks.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0caebb2dfbff12545610aa6438dccbec84db3f9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190346"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="bbabf-103">Hüvitisruudustike häälestamine</span><span class="sxs-lookup"><span data-stu-id="bbabf-103">Set up compensation grids</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbabf-104">Tasuruudustikke kasutatakse põhipalgaplaanide palgastruktuuri määratlemiseks ja säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="bbabf-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="bbabf-105">Tasuruudustikke saab mitme plaani vahel jagada või uue tasuplaani loomisel kopeerida.</span><span class="sxs-lookup"><span data-stu-id="bbabf-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="bbabf-106">Enne tasuruudustiku koostamist tuleb seadistada tasemed ja viitepunktid.</span><span class="sxs-lookup"><span data-stu-id="bbabf-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="bbabf-107">Selles näites loome uue tasuruudustiku tüübi Tase, kasutades tasemete ja viitepunktide demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="bbabf-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="bbabf-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="bbabf-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="bbabf-109">Seadistage teave tasuruudustiku kohta.</span><span class="sxs-lookup"><span data-stu-id="bbabf-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="bbabf-110">Avage Personaliarvestus > Hüvitus > Põhipalk > Hüvituse ruudustikud.</span><span class="sxs-lookup"><span data-stu-id="bbabf-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="bbabf-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-111">Click New.</span></span>
3. <span data-ttu-id="bbabf-112">Sisestage väärtus väljale Ruudustik.</span><span class="sxs-lookup"><span data-stu-id="bbabf-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="bbabf-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bbabf-114">Valige suvand väljalt Tüüp.</span><span class="sxs-lookup"><span data-stu-id="bbabf-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="bbabf-115">Valige või sisestage väärtus väljal Viite seadistus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="bbabf-116">Valige või sisestage väärtus väljal Valuuta.</span><span class="sxs-lookup"><span data-stu-id="bbabf-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="bbabf-117">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="bbabf-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="bbabf-118">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="bbabf-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="bbabf-119">Tasustruktuurile tasemete lisamine</span><span class="sxs-lookup"><span data-stu-id="bbabf-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="bbabf-120">Klõpsake valikut Tasustruktuur.</span><span class="sxs-lookup"><span data-stu-id="bbabf-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="bbabf-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bbabf-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="bbabf-122">Valige või sisestage väärtus väljal Tase.</span><span class="sxs-lookup"><span data-stu-id="bbabf-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="bbabf-123">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-123">Click New.</span></span>
5. <span data-ttu-id="bbabf-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bbabf-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bbabf-125">Valige või sisestage väärtus väljal Tase.</span><span class="sxs-lookup"><span data-stu-id="bbabf-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="bbabf-126">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-126">Click New.</span></span>
8. <span data-ttu-id="bbabf-127">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bbabf-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="bbabf-128">Valige või sisestage väärtus väljal Tase.</span><span class="sxs-lookup"><span data-stu-id="bbabf-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="bbabf-129">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-129">Click New.</span></span>
11. <span data-ttu-id="bbabf-130">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bbabf-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="bbabf-131">Valige või sisestage väärtus väljal Tase.</span><span class="sxs-lookup"><span data-stu-id="bbabf-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="bbabf-132">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-132">Click New.</span></span>
14. <span data-ttu-id="bbabf-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bbabf-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="bbabf-134">Valige või sisestage väärtus väljal Tase.</span><span class="sxs-lookup"><span data-stu-id="bbabf-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="bbabf-135">Tasustruktuuri täitmine väärtustega</span><span class="sxs-lookup"><span data-stu-id="bbabf-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="bbabf-136">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bbabf-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bbabf-137">Sellel ajal saab tasuväärtused igale tabel väljale sisestada või kasutada hulgimuutmise funktsiooni, et täita hõlpsasti mitu välja ja teha põhiarvutusi.</span><span class="sxs-lookup"><span data-stu-id="bbabf-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="bbabf-138">Klõpsake valikut Massmuudatus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-138">Click Mass change.</span></span>
    * <span data-ttu-id="bbabf-139">Selle tabeli puhul rakendame kõigepealt esimese taseme keskpunkti väärtuse kõigile tabeli väljadele.</span><span class="sxs-lookup"><span data-stu-id="bbabf-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="bbabf-140">See on tasutabeli alus.</span><span class="sxs-lookup"><span data-stu-id="bbabf-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="bbabf-141">Valige suvand väljal Korrigeerimise tüüp.</span><span class="sxs-lookup"><span data-stu-id="bbabf-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="bbabf-142">Sisestage arv väljale Korrigeerimissumma.</span><span class="sxs-lookup"><span data-stu-id="bbabf-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="bbabf-143">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="bbabf-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="bbabf-144">Klõpsake käsku Rakenda ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="bbabf-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="bbabf-145">Nüüd kasutame hulgimuutmise funktsiooni, muutes iga järgmise taseme summasid teatud protsendi või summa võrra.</span><span class="sxs-lookup"><span data-stu-id="bbabf-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="bbabf-146">Selles näites on astmete keskpunktide vahe 12,5%.</span><span class="sxs-lookup"><span data-stu-id="bbabf-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="bbabf-147">Valige suvand väljal Korrigeerimise tüüp.</span><span class="sxs-lookup"><span data-stu-id="bbabf-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="bbabf-148">Sisestage arv väljale Korrigeerimissumma.</span><span class="sxs-lookup"><span data-stu-id="bbabf-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="bbabf-149">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="bbabf-150">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="bbabf-151">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="bbabf-152">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="bbabf-153">Klõpsake käsku Rakenda ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="bbabf-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="bbabf-154">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="bbabf-155">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="bbabf-156">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="bbabf-157">Klõpsake käsku Rakenda ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="bbabf-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="bbabf-158">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="bbabf-159">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="bbabf-160">Klõpsake käsku Rakenda ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="bbabf-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="bbabf-161">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bbabf-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="bbabf-162">Klõpsake käsku Rakenda ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="bbabf-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="bbabf-163">Nüüd kasutame hulgimuutmise funktsiooni, et kohandada iga taseme miinimum- ja maksimumpunkti.</span><span class="sxs-lookup"><span data-stu-id="bbabf-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="bbabf-164">Selles näites kasutatakse erinevust 50%, seega kohandatakse miinimumpunkti –20% ja maksimumpunkti +20% võrra.</span><span class="sxs-lookup"><span data-stu-id="bbabf-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="bbabf-165">Sisestage arv väljale Korrigeerimissumma.</span><span class="sxs-lookup"><span data-stu-id="bbabf-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="bbabf-166">Valige või sisestage väärtus väljal Viitepunkt.</span><span class="sxs-lookup"><span data-stu-id="bbabf-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="bbabf-167">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="bbabf-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="bbabf-168">Klõpsake käsku Rakenda ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="bbabf-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="bbabf-169">Sisestage arv väljale Korrigeerimissumma.</span><span class="sxs-lookup"><span data-stu-id="bbabf-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="bbabf-170">Valige või sisestage väärtus väljal Viitepunkt.</span><span class="sxs-lookup"><span data-stu-id="bbabf-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="bbabf-171">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="bbabf-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="bbabf-172">Klõpsake käsku Rakenda ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="bbabf-172">Click Apply to grid.</span></span>

