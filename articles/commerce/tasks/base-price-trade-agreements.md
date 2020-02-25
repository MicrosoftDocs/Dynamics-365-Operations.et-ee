---
title: " Alushind ja kaubanduslepped"
description: See protseduur juhendab kanalispetsiifiliste müügihinna kaubanduslepete loomisel.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7576c4218118724562ff739ff9805a06b7ba22d5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022269"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="f7053-103"> Alushind ja kaubanduslepped</span><span class="sxs-lookup"><span data-stu-id="f7053-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f7053-104">See protseduur juhendab kanalispetsiifiliste müügihinna kaubanduslepete loomisel.</span><span class="sxs-lookup"><span data-stu-id="f7053-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="f7053-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="f7053-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="f7053-106">Avage **Navigeerimispaanil** jaotis **Moodulid > Jaemüük ja kaubandus > Hinnakujunduse ja allahindluse haldus > Hinnagrupid >Kõik hinnagrupid**.</span><span class="sxs-lookup"><span data-stu-id="f7053-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="f7053-107">Kaubanduslepped määratakse konkreetsetesse kanalitesse hinnagruppide kaudu.</span><span class="sxs-lookup"><span data-stu-id="f7053-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="f7053-108">Hinnagruppide kasutamine kaubanduslepete määramiseks kanalisse võimaldab kanalispetsiifilist hindade määramist.</span><span class="sxs-lookup"><span data-stu-id="f7053-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="f7053-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f7053-109">Click **New**.</span></span>
3. <span data-ttu-id="f7053-110">Väljale **Hinnagrupid** tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="f7053-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="f7053-111">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f7053-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="f7053-112">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f7053-112">Click **Save**.</span></span>
6. <span data-ttu-id="f7053-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7053-113">Close the page.</span></span>
7. <span data-ttu-id="f7053-114">Avage **Navigatsioonipaneelil** suvand **Moodulid > Jaemüük ja kaubandus > Kanalid > Kauplused > Kõik kauplused**.</span><span class="sxs-lookup"><span data-stu-id="f7053-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="f7053-115">Valige loendist New York.</span><span class="sxs-lookup"><span data-stu-id="f7053-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="f7053-116">Toimingupaanil klõpsake **Kauplus**.</span><span class="sxs-lookup"><span data-stu-id="f7053-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="f7053-117">Klõpsake **Hinnagrupid**.</span><span class="sxs-lookup"><span data-stu-id="f7053-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="f7053-118">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f7053-118">Click **New**.</span></span>
12. <span data-ttu-id="f7053-119">Väljal **Hinnagrupid** klõpsake rippmenüü nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="f7053-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f7053-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f7053-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f7053-121">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f7053-121">Click **Save**.</span></span>
15. <span data-ttu-id="f7053-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7053-122">Close the page.</span></span>
16. <span data-ttu-id="f7053-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7053-123">Close the page.</span></span>
17. <span data-ttu-id="f7053-124">Paanil **Navigeerimispaan** avage **Moodulid > Jaemüük ja kaubandus > Tooted ja kategooriad > Väljastatud tooted kategooria alusel**.</span><span class="sxs-lookup"><span data-stu-id="f7053-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="f7053-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f7053-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="f7053-126">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="f7053-126">Click **Edit**.</span></span>
20. <span data-ttu-id="f7053-127">Laiendage vahekaart **Müük**.</span><span class="sxs-lookup"><span data-stu-id="f7053-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="f7053-128">Väljale **Hind** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="f7053-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="f7053-129">Seda hinda kasutatakse, kui kohalduvaid kaubandusleppeid ei leita.</span><span class="sxs-lookup"><span data-stu-id="f7053-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="f7053-130">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f7053-130">Click **Save**.</span></span>
23. <span data-ttu-id="f7053-131">Klõpsake paanil **Tegevuspaan** nuppu **Müük**.</span><span class="sxs-lookup"><span data-stu-id="f7053-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="f7053-132">Klõpsake **Loo kaubanduslepe**.</span><span class="sxs-lookup"><span data-stu-id="f7053-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="f7053-133">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f7053-133">Click **New**.</span></span>
26. <span data-ttu-id="f7053-134">Klõpsake väljal **Nimi** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f7053-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="f7053-135">Valige loendist **Kaubandus**.</span><span class="sxs-lookup"><span data-stu-id="f7053-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="f7053-136">Demoandmetes on **Kaubanduse** töölehe nimi vaikimisi seotud **Müügihinnaga**.</span><span class="sxs-lookup"><span data-stu-id="f7053-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="f7053-137">See tähendab, et kõik uued loodud read lülituvad vaikimisi kaubanduslepete kohastele müügihindadele.</span><span class="sxs-lookup"><span data-stu-id="f7053-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="f7053-138">Klõpsake paanil **Tegevuspaan** valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="f7053-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="f7053-139">Väljal **Konto kood** valige 'Grupeeri'.</span><span class="sxs-lookup"><span data-stu-id="f7053-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="f7053-140">Klõpsake väljal **Konto valik** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f7053-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="f7053-141">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f7053-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="f7053-142">See viib lõpule ühenduse valikute Kanal > Hinnagrupp > Kaubanduslepe vahel.</span><span class="sxs-lookup"><span data-stu-id="f7053-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="f7053-143">Väljale **Kauba seos** tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="f7053-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="f7053-144">Väljale **Summa valuutas** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="f7053-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="f7053-145">Vahekaardil **Üksikasjad** märkige või eemaldage märge märkeruudust **Leia järgmine**.</span><span class="sxs-lookup"><span data-stu-id="f7053-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="f7053-146">Kui suvandi **Leia järgmine** väärtus on 'Jah', jätkab hinnakujunduse mootor kohaldatavate madalam müügihinnaga kaubanduslepete otsimist.</span><span class="sxs-lookup"><span data-stu-id="f7053-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="f7053-147">Kui suvandi **Leia järgmine** väärtus on 'Ei', lõpetab hinnakujunduse mootor otsingu ja kasutab seda kaubanduslepet.</span><span class="sxs-lookup"><span data-stu-id="f7053-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="f7053-148">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="f7053-148">Click **Post**.</span></span>
36. <span data-ttu-id="f7053-149">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7053-149">Click **OK**.</span></span>
37. <span data-ttu-id="f7053-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7053-150">Close the page.</span></span>
38. <span data-ttu-id="f7053-151">Klõpsake paanil **Toimingupaan** nuppu Müük.</span><span class="sxs-lookup"><span data-stu-id="f7053-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="f7053-152">Klõpsake valikut **Müügihinnad**.</span><span class="sxs-lookup"><span data-stu-id="f7053-152">Click **Sales price**.</span></span>

