---
title: Võrgukanali aruannete loomine
description: See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 80d62b29fcc95a3153c604512e1ee6b3e55ba840
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019783"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="4f8ee-103">Võrgukanali aruannete loomine</span><span class="sxs-lookup"><span data-stu-id="4f8ee-103">Generate online channel reports</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f8ee-104">See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4f8ee-105">Rakenduses Commerce saadete luua ja vaadata mitut aruannet, et näha, kuidas võrgukanal toimib.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-105">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="4f8ee-106">Kanali koondaruanne</span><span class="sxs-lookup"><span data-stu-id="4f8ee-106">Channel summary report</span></span>

<span data-ttu-id="4f8ee-107">Aruanne **Kanali kokkuvõte** kuvab valitud kanali järgmiste kannete kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-107">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="4f8ee-108">Müügikanded</span><span class="sxs-lookup"><span data-stu-id="4f8ee-108">Sales transactions</span></span>
- <span data-ttu-id="4f8ee-109">Maksekanded</span><span class="sxs-lookup"><span data-stu-id="4f8ee-109">Payment transactions</span></span>
- <span data-ttu-id="4f8ee-110">Maksukanded</span><span class="sxs-lookup"><span data-stu-id="4f8ee-110">Tax transactions</span></span>
- <span data-ttu-id="4f8ee-111">Allahinnatud kanded</span><span class="sxs-lookup"><span data-stu-id="4f8ee-111">Discounted transactions</span></span>

<span data-ttu-id="4f8ee-112">Aruande **Kanali kokkuvõte** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-112">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="4f8ee-113">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali koondaruanne**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-113">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="4f8ee-114">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-114">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-115">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-115">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-116">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-116">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="4f8ee-117">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-117">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="4f8ee-118">Kanali müügiaruanne aastate alusel</span><span class="sxs-lookup"><span data-stu-id="4f8ee-118">Channel sales by year report</span></span> 

<span data-ttu-id="4f8ee-119">Aruanne **Kanali müük aastate alusel** näitab kindla poe müügi võrdlust aastate lõikes.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-119">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="4f8ee-120">Teie valite aasta, mille müüki võrrelda, ja aruanne võrdleb valitud aasta müüki eelmise aasta müügiga.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-120">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="4f8ee-121">Aruande **Kanali müük aastate alusel** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-121">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="4f8ee-122">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali aastapõhine müügiaruanne**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-122">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="4f8ee-123">Sisestage väljale **Kalendriaastast** aasta.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-123">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="4f8ee-124">Sisestage väljale **Kalendriaastani** aasta.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-124">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="4f8ee-125">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-125">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="4f8ee-126">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-126">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="4f8ee-127">Kanali müügiaruanne tundide alusel</span><span class="sxs-lookup"><span data-stu-id="4f8ee-127">Channel sales by hour report</span></span>

<span data-ttu-id="4f8ee-128">Aruanne **Kanali müük tundide alusel** näitab valitud kanali või tootmisüksuse müügimõõdikuid tunni alusel.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-128">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="4f8ee-129">Aruande **Kanali müük tundide alusel** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-129">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="4f8ee-130">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali tunnipõhine müügiaruanne**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-130">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="4f8ee-131">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-131">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-132">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-132">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-133">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-133">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="4f8ee-134">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-134">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="4f8ee-135">Parimate klientide aruanne</span><span class="sxs-lookup"><span data-stu-id="4f8ee-135">Top customers report</span></span>

<span data-ttu-id="4f8ee-136">Aruanne **Parimad kliendid** näitab valitud kanali või tootmisüksuse parima *N* kliendi müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-136">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="4f8ee-137">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-137">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="4f8ee-138">Aruande **Parimad kliendid** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-138">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="4f8ee-139">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste klientide aruanne**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-139">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="4f8ee-140">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-140">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-141">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-141">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-142">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-142">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="4f8ee-143">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-143">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="4f8ee-144">Peamiste allahindluste aruanne</span><span class="sxs-lookup"><span data-stu-id="4f8ee-144">Top discounts report</span></span>

<span data-ttu-id="4f8ee-145">Aruanne **Peamised allahindlused** näitab valitud kanali või tootmisüksuse peamise *N* allahindluse müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-145">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="4f8ee-146">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-146">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="4f8ee-147">Aruande **Peamised allahindlused** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-147">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="4f8ee-148">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste allahindluste aruanne**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-148">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="4f8ee-149">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-149">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-150">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-150">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-151">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-151">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="4f8ee-152">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-152">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="4f8ee-153">Peamiste toodete aruanne</span><span class="sxs-lookup"><span data-stu-id="4f8ee-153">Top products report</span></span>

<span data-ttu-id="4f8ee-154">Aruanne **Peamised tooted** näitab valitud kanali või tootmisüksuse peamise *N* toote müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-154">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="4f8ee-155">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-155">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="4f8ee-156">Aruande **Peamised tooted** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-156">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="4f8ee-157">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste toodete aruanne**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-157">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="4f8ee-158">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-158">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-159">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-159">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-160">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-160">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="4f8ee-161">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-161">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="4f8ee-162">Kategooria müügiaruanne</span><span class="sxs-lookup"><span data-stu-id="4f8ee-162">Category sales report</span></span>

<span data-ttu-id="4f8ee-163">Aruanne **Kategooria müük** näitab valitud kanali või tootmisüksuse kategooriahierarhia iga sõlme müügimõõdikuid valitud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-163">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="4f8ee-164">Aruande **Kategooria müük** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-164">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="4f8ee-165">Minge jaotisse **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kategooria müügiaruanded**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-165">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="4f8ee-166">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-166">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-167">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-167">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-168">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-168">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="4f8ee-169">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-169">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="4f8ee-170">Organisatsiooni müügiaruanne</span><span class="sxs-lookup"><span data-stu-id="4f8ee-170">Organization sales report</span></span>

<span data-ttu-id="4f8ee-171">Aruanne **Organisatsiooni müük** näitab teie kaupluste jõudlust organisatsiooni üksuse järgi.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-171">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="4f8ee-172">See aruanne sisaldab müügikogust ja -summat poe kaupa ning iga poe kasumimarginaali.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-172">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="4f8ee-173">Organisatsiooni üksus põhineb vaikearuandluse hierarhial.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-173">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="4f8ee-174">Aruande **Organisatsiooni müük** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-174">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="4f8ee-175">Minge jaotisse **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Organisatsiooni müügiaruanded**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-175">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="4f8ee-176">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-176">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-177">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-177">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="4f8ee-178">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f8ee-178">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f8ee-179">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4f8ee-179">Additional resources</span></span>

- [<span data-ttu-id="4f8ee-180">Commerce’i avaleht</span><span class="sxs-lookup"><span data-stu-id="4f8ee-180">Commerce home page</span></span>](./index.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]