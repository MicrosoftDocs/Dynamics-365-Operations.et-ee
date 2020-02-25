---
title: Võrgukanali aruannete loomine
description: See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd40aabdf40e0f2bb257b914326df5595a0e6945
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003000"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="159cf-103">Võrgukanali aruannete loomine</span><span class="sxs-lookup"><span data-stu-id="159cf-103">Generate online channel reports</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="159cf-104">See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="159cf-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="159cf-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="159cf-105">Overview</span></span>

<span data-ttu-id="159cf-106">Rakenduses Commerce saadete luua ja vaadata mitut aruannet, et näha, kuidas võrgukanal toimib.</span><span class="sxs-lookup"><span data-stu-id="159cf-106">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="159cf-107">Kanali koondaruanne</span><span class="sxs-lookup"><span data-stu-id="159cf-107">Channel summary report</span></span>

<span data-ttu-id="159cf-108">Aruanne **Kanali kokkuvõte** kuvab valitud kanali järgmiste kannete kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="159cf-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="159cf-109">Müügikanded</span><span class="sxs-lookup"><span data-stu-id="159cf-109">Sales transactions</span></span>
- <span data-ttu-id="159cf-110">Maksekanded</span><span class="sxs-lookup"><span data-stu-id="159cf-110">Payment transactions</span></span>
- <span data-ttu-id="159cf-111">Maksukanded</span><span class="sxs-lookup"><span data-stu-id="159cf-111">Tax transactions</span></span>
- <span data-ttu-id="159cf-112">Allahinnatud kanded</span><span class="sxs-lookup"><span data-stu-id="159cf-112">Discounted transactions</span></span>

<span data-ttu-id="159cf-113">Aruande **Kanali kokkuvõte** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="159cf-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="159cf-114">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali koondaruanne**.</span><span class="sxs-lookup"><span data-stu-id="159cf-114">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="159cf-115">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="159cf-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-116">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="159cf-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-117">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="159cf-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="159cf-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="159cf-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="159cf-119">Kanali müügiaruanne aastate alusel</span><span class="sxs-lookup"><span data-stu-id="159cf-119">Channel sales by year report</span></span> 

<span data-ttu-id="159cf-120">Aruanne **Kanali müük aastate alusel** näitab kindla poe müügi võrdlust aastate lõikes.</span><span class="sxs-lookup"><span data-stu-id="159cf-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="159cf-121">Teie valite aasta, mille müüki võrrelda, ja aruanne võrdleb valitud aasta müüki eelmise aasta müügiga.</span><span class="sxs-lookup"><span data-stu-id="159cf-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="159cf-122">Aruande **Kanali müük aastate alusel** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="159cf-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="159cf-123">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali aastapõhine müügiaruanne**.</span><span class="sxs-lookup"><span data-stu-id="159cf-123">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="159cf-124">Sisestage väljale **Kalendriaastast** aasta.</span><span class="sxs-lookup"><span data-stu-id="159cf-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="159cf-125">Sisestage väljale **Kalendriaastani** aasta.</span><span class="sxs-lookup"><span data-stu-id="159cf-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="159cf-126">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="159cf-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="159cf-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="159cf-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="159cf-128">Kanali müügiaruanne tundide alusel</span><span class="sxs-lookup"><span data-stu-id="159cf-128">Channel sales by hour report</span></span>

<span data-ttu-id="159cf-129">Aruanne **Kanali müük tundide alusel** näitab valitud kanali või tootmisüksuse müügimõõdikuid tunni alusel.</span><span class="sxs-lookup"><span data-stu-id="159cf-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="159cf-130">Aruande **Kanali müük tundide alusel** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="159cf-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="159cf-131">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali tunnipõhine müügiaruanne**.</span><span class="sxs-lookup"><span data-stu-id="159cf-131">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="159cf-132">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="159cf-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-133">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="159cf-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-134">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="159cf-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="159cf-135">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="159cf-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="159cf-136">Parimate klientide aruanne</span><span class="sxs-lookup"><span data-stu-id="159cf-136">Top customers report</span></span>

<span data-ttu-id="159cf-137">Aruanne **Parimad kliendid** näitab valitud kanali või tootmisüksuse parima *N* kliendi müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="159cf-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="159cf-138">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="159cf-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="159cf-139">Aruande **Parimad kliendid** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="159cf-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="159cf-140">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste klientide aruanne**.</span><span class="sxs-lookup"><span data-stu-id="159cf-140">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="159cf-141">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="159cf-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-142">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="159cf-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-143">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="159cf-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="159cf-144">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="159cf-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="159cf-145">Peamiste allahindluste aruanne</span><span class="sxs-lookup"><span data-stu-id="159cf-145">Top discounts report</span></span>

<span data-ttu-id="159cf-146">Aruanne **Peamised allahindlused** näitab valitud kanali või tootmisüksuse peamise *N* allahindluse müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="159cf-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="159cf-147">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="159cf-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="159cf-148">Aruande **Peamised allahindlused** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="159cf-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="159cf-149">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste allahindluste aruanne**.</span><span class="sxs-lookup"><span data-stu-id="159cf-149">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="159cf-150">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="159cf-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-151">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="159cf-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-152">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="159cf-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="159cf-153">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="159cf-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="159cf-154">Peamiste toodete aruanne</span><span class="sxs-lookup"><span data-stu-id="159cf-154">Top products report</span></span>

<span data-ttu-id="159cf-155">Aruanne **Peamised tooted** näitab valitud kanali või tootmisüksuse peamise *N* toote müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="159cf-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="159cf-156">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="159cf-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="159cf-157">Aruande **Peamised tooted** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="159cf-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="159cf-158">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste toodete aruanne**.</span><span class="sxs-lookup"><span data-stu-id="159cf-158">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="159cf-159">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="159cf-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-160">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="159cf-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-161">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="159cf-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="159cf-162">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="159cf-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="159cf-163">Kategooria müügiaruanne</span><span class="sxs-lookup"><span data-stu-id="159cf-163">Category sales report</span></span>

<span data-ttu-id="159cf-164">Aruanne **Kategooria müük** näitab valitud kanali või tootmisüksuse kategooriahierarhia iga sõlme müügimõõdikuid valitud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="159cf-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="159cf-165">Aruande **Kategooria müük** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="159cf-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="159cf-166">Minge jaotisse **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kategooria müügiaruanded**.</span><span class="sxs-lookup"><span data-stu-id="159cf-166">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="159cf-167">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="159cf-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-168">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="159cf-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-169">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="159cf-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="159cf-170">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="159cf-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="159cf-171">Organisatsiooni müügiaruanne</span><span class="sxs-lookup"><span data-stu-id="159cf-171">Organization sales report</span></span>

<span data-ttu-id="159cf-172">Aruanne **Organisatsiooni müük** näitab teie kaupluste jõudlust organisatsiooni üksuse järgi.</span><span class="sxs-lookup"><span data-stu-id="159cf-172">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="159cf-173">See aruanne sisaldab müügikogust ja -summat poe kaupa ning iga poe kasumimarginaali.</span><span class="sxs-lookup"><span data-stu-id="159cf-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="159cf-174">Organisatsiooni üksus põhineb vaikearuandluse hierarhial.</span><span class="sxs-lookup"><span data-stu-id="159cf-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="159cf-175">Aruande **Organisatsiooni müük** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="159cf-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="159cf-176">Minge jaotisse **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Organisatsiooni müügiaruanded**.</span><span class="sxs-lookup"><span data-stu-id="159cf-176">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="159cf-177">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="159cf-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-178">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="159cf-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="159cf-179">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="159cf-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="159cf-180">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="159cf-180">Additional resources</span></span>

- [<span data-ttu-id="159cf-181">Abiressursid rakenduse Dynamics 365 Retail jaoks</span><span class="sxs-lookup"><span data-stu-id="159cf-181">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
