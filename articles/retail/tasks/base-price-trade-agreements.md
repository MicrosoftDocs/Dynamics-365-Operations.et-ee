---
title: " Alushind ja kaubanduslepped"
description: See protseduur juhendab kanalispetsiifiliste müügihinna kaubanduslepete loomisel.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 4830ac553318cfbb3cb74395d1662e74dff75290
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "320416"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="b2d2f-103"> Alushind ja kaubanduslepped</span><span class="sxs-lookup"><span data-stu-id="b2d2f-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b2d2f-104">See protseduur juhendab kanalispetsiifiliste müügihinna kaubanduslepete loomisel.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="b2d2f-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="b2d2f-106">Avage Jaemüük ja kaubandus > Hinnad ja allahindlused > Hinnagrupid > Kõik hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-106">Go to Retail and commerce > Pricing and discounts > Price groups > All price groups.</span></span>
    * <span data-ttu-id="b2d2f-107">Kaubanduslepped määratakse konkreetsetesse kanalitesse hinnagruppide kaudu.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="b2d2f-108">Hinnagruppide kasutamine kaubanduslepete määramiseks kanalisse võimaldab kanalispetsiifilist hindade määramist.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="b2d2f-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-109">Click New.</span></span>
3. <span data-ttu-id="b2d2f-110">Sisestage väärtus väljale Hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-110">In the Price groups field, type a value.</span></span>
4. <span data-ttu-id="b2d2f-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b2d2f-112">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-112">Click Save.</span></span>
6. <span data-ttu-id="b2d2f-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-113">Close the page.</span></span>
7. <span data-ttu-id="b2d2f-114">Avage Jaemüük ja kaubandus > Kanalid > Jaemüügikauplused > Kõik jaemüügikauplused.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-114">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
8. <span data-ttu-id="b2d2f-115">Valige loendist New York.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="b2d2f-116">Klõpsake tegevuspaneelil valikut Store (Kauplus).</span><span class="sxs-lookup"><span data-stu-id="b2d2f-116">On the Action Pane, click Store.</span></span>
10. <span data-ttu-id="b2d2f-117">Klõpsake valikut Hinnagrupid.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-117">Click Price groups.</span></span>
11. <span data-ttu-id="b2d2f-118">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-118">Click New.</span></span>
12. <span data-ttu-id="b2d2f-119">Klõpsake väljal Price groups (Hinnagrupid) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-119">In the Price groups field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="b2d2f-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b2d2f-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-121">Click Save.</span></span>
15. <span data-ttu-id="b2d2f-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-122">Close the page.</span></span>
16. <span data-ttu-id="b2d2f-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-123">Close the page.</span></span>
17. <span data-ttu-id="b2d2f-124">Avage Jaemüük ja kaubandus > Tooted ja kategooriad > Väljastatud tooted kategooria järgi.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-124">Go to Retail and commerce > Products and categories > Released products by category.</span></span>
18. <span data-ttu-id="b2d2f-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="b2d2f-126">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-126">Click Edit.</span></span>
20. <span data-ttu-id="b2d2f-127">Vajutage jaotise Sell (Müük) väljaulatuvat osa.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-127">Toggle the expansion of the Sell section.</span></span>
21. <span data-ttu-id="b2d2f-128">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-128">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="b2d2f-129">Seda hinda kasutatakse, kui kohalduvaid kaubandusleppeid ei leita.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="b2d2f-130">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-130">Click Save.</span></span>
23. <span data-ttu-id="b2d2f-131">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-131">On the Action Pane, click Sell.</span></span>
24. <span data-ttu-id="b2d2f-132">Klõpsake Create trade agreements (Loo kaubanduslepped).</span><span class="sxs-lookup"><span data-stu-id="b2d2f-132">Click Create trade agreements.</span></span>
25. <span data-ttu-id="b2d2f-133">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-133">Click New.</span></span>
26. <span data-ttu-id="b2d2f-134">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-134">In the Name field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="b2d2f-135">Valige loendist Retail (Jaemüük).</span><span class="sxs-lookup"><span data-stu-id="b2d2f-135">In the list, select 'Retail'.</span></span>
    * <span data-ttu-id="b2d2f-136">Demoandmetes on Jaemüügi töölehe nimi vaikimisi seotud müügihinnaga.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="b2d2f-137">See tähendab, et kõik uued loodud read lülituvad vaikimisi kaubanduslepete kohastele müügihindadele.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="b2d2f-138">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-138">Click Lines.</span></span>
29. <span data-ttu-id="b2d2f-139">Valige väljal Account code (Konto kood) Group (Grupp).</span><span class="sxs-lookup"><span data-stu-id="b2d2f-139">In the Account code field, select 'Group'.</span></span>
30. <span data-ttu-id="b2d2f-140">Klõpsake väljal Konto valik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-140">In the Account selection field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="b2d2f-141">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b2d2f-142">See viib lõpule ühenduse valikute Kanal > Hinnagrupp > Kaubanduslepe vahel.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="b2d2f-143">Sisestage väärtus väljale Item relation (Kauba seos).</span><span class="sxs-lookup"><span data-stu-id="b2d2f-143">In the Item relation field, type a value.</span></span>
33. <span data-ttu-id="b2d2f-144">Sisestage arv väljale Summa valuutas.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-144">In the Amount in currency field, enter a number.</span></span>
34. <span data-ttu-id="b2d2f-145">Märkige ruut Find next (Leia järgmine) või eemaldage sellest märge.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-145">Check or uncheck the Find next checkbox.</span></span>
    * <span data-ttu-id="b2d2f-146">Kui valiku Leia järgmine väärtuseks on Jah, jätkab hinnamootor madalama müügihinnaga kohalduvate kaubanduselepete otsimist.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-146">When Find next is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="b2d2f-147">Kui valiku Leia järgmine väärtuseks on Ei, lõpetab hinnamootor otsimise ja kasutab kaubanduslepet.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-147">When Find next is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="b2d2f-148">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-148">Click Post.</span></span>
36. <span data-ttu-id="b2d2f-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-149">Click OK.</span></span>
37. <span data-ttu-id="b2d2f-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-150">Close the page.</span></span>
38. <span data-ttu-id="b2d2f-151">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="b2d2f-151">On the Action Pane, click Sell.</span></span>
39. <span data-ttu-id="b2d2f-152">Klõpsake Sales price (Müügihind).</span><span class="sxs-lookup"><span data-stu-id="b2d2f-152">Click Sales price.</span></span>

