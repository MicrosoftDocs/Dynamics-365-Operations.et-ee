---
title: Võrgukanali aruannete loomine
description: See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Retail.
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
ms.openlocfilehash: 77737c134df8f3ba598fe9026fa7c01ca9976733
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698046"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="a6a77-103">Võrgukanali aruannete loomine</span><span class="sxs-lookup"><span data-stu-id="a6a77-103">Generate online channel reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a6a77-104">See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="a6a77-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="a6a77-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a6a77-105">Overview</span></span>

<span data-ttu-id="a6a77-106">Saate luua ja vaadata Retailis mitu aruannet, et näha, kuidas võrgukanal toimib.</span><span class="sxs-lookup"><span data-stu-id="a6a77-106">You can generate and view several reports in Retail to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="a6a77-107">Kanali koondaruanne</span><span class="sxs-lookup"><span data-stu-id="a6a77-107">Channel summary report</span></span>

<span data-ttu-id="a6a77-108">Aruanne **Kanali kokkuvõte** kuvab valitud kanali järgmiste kannete kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="a6a77-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="a6a77-109">Müügikanded</span><span class="sxs-lookup"><span data-stu-id="a6a77-109">Sales transactions</span></span>
- <span data-ttu-id="a6a77-110">Maksekanded</span><span class="sxs-lookup"><span data-stu-id="a6a77-110">Payment transactions</span></span>
- <span data-ttu-id="a6a77-111">Maksukanded</span><span class="sxs-lookup"><span data-stu-id="a6a77-111">Tax transactions</span></span>
- <span data-ttu-id="a6a77-112">Allahinnatud kanded</span><span class="sxs-lookup"><span data-stu-id="a6a77-112">Discounted transactions</span></span>

<span data-ttu-id="a6a77-113">Aruande **Kanali kokkuvõte** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6a77-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="a6a77-114">Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Kanali koondaruanne**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-114">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="a6a77-115">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-116">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-117">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="a6a77-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="a6a77-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="a6a77-119">Kanali müügiaruanne aastate alusel</span><span class="sxs-lookup"><span data-stu-id="a6a77-119">Channel sales by year report</span></span> 

<span data-ttu-id="a6a77-120">Aruanne **Kanali müük aastate alusel** näitab kindla poe müügi võrdlust aastate lõikes.</span><span class="sxs-lookup"><span data-stu-id="a6a77-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="a6a77-121">Teie valite aasta, mille müüki võrrelda, ja aruanne võrdleb valitud aasta müüki eelmise aasta müügiga.</span><span class="sxs-lookup"><span data-stu-id="a6a77-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="a6a77-122">Aruande **Kanali müük aastate alusel** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6a77-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="a6a77-123">Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Kanali müügiaruanne aastate alusel**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-123">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="a6a77-124">Sisestage väljale **Kalendriaastast** aasta.</span><span class="sxs-lookup"><span data-stu-id="a6a77-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="a6a77-125">Sisestage väljale **Kalendriaastani** aasta.</span><span class="sxs-lookup"><span data-stu-id="a6a77-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="a6a77-126">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="a6a77-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="a6a77-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="a6a77-128">Kanali müügiaruanne tundide alusel</span><span class="sxs-lookup"><span data-stu-id="a6a77-128">Channel sales by hour report</span></span>

<span data-ttu-id="a6a77-129">Aruanne **Kanali müük tundide alusel** näitab valitud kanali või tootmisüksuse müügimõõdikuid tunni alusel.</span><span class="sxs-lookup"><span data-stu-id="a6a77-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="a6a77-130">Aruande **Kanali müük tundide alusel** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6a77-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="a6a77-131">Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Kanali müügiaruanne tundide alusel**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-131">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="a6a77-132">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-133">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-134">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="a6a77-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="a6a77-135">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="a6a77-136">Parimate klientide aruanne</span><span class="sxs-lookup"><span data-stu-id="a6a77-136">Top customers report</span></span>

<span data-ttu-id="a6a77-137">Aruanne **Parimad kliendid** näitab valitud kanali või tootmisüksuse parima *N* kliendi müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="a6a77-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="a6a77-138">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="a6a77-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="a6a77-139">Aruande **Parimad kliendid** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6a77-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="a6a77-140">Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Parimate klientide aruanne**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-140">Go to **Retail \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="a6a77-141">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-142">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-143">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="a6a77-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="a6a77-144">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="a6a77-145">Peamiste allahindluste aruanne</span><span class="sxs-lookup"><span data-stu-id="a6a77-145">Top discounts report</span></span>

<span data-ttu-id="a6a77-146">Aruanne **Peamised allahindlused** näitab valitud kanali või tootmisüksuse peamise *N* allahindluse müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="a6a77-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="a6a77-147">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="a6a77-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="a6a77-148">Aruande **Peamised allahindlused** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6a77-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="a6a77-149">Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Peamiste allahindluste aruanne**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-149">Go to **Retail \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="a6a77-150">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-151">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-152">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="a6a77-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="a6a77-153">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="a6a77-154">Peamiste toodete aruanne</span><span class="sxs-lookup"><span data-stu-id="a6a77-154">Top products report</span></span>

<span data-ttu-id="a6a77-155">Aruanne **Peamised tooted** näitab valitud kanali või tootmisüksuse peamise *N* toote müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="a6a77-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="a6a77-156">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="a6a77-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="a6a77-157">Aruande **Peamised tooted** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6a77-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="a6a77-158">Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Peamiste toodete aruanne**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-158">Go to **Retail \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="a6a77-159">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-160">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-161">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="a6a77-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="a6a77-162">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="a6a77-163">Kategooria müügiaruanne</span><span class="sxs-lookup"><span data-stu-id="a6a77-163">Category sales report</span></span>

<span data-ttu-id="a6a77-164">Aruanne **Kategooria müük** näitab valitud kanali või tootmisüksuse kategooriahierarhia iga sõlme müügimõõdikuid valitud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="a6a77-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="a6a77-165">Aruande **Kategooria müük** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6a77-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="a6a77-166">Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Kategooria müügiaruanded**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-166">Go to **Retail \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="a6a77-167">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-168">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-169">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="a6a77-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="a6a77-170">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="a6a77-171">Organisatsiooni müügiaruanne</span><span class="sxs-lookup"><span data-stu-id="a6a77-171">Organization sales report</span></span>

<span data-ttu-id="a6a77-172">Aruanne **Organisatsiooni müük** näitab teie jaekaupluste jõudlust organisatsiooni üksuse järgi.</span><span class="sxs-lookup"><span data-stu-id="a6a77-172">The **Organization sales** report shows the performance of your retail stores by organization unit.</span></span> <span data-ttu-id="a6a77-173">See aruanne sisaldab müügikogust ja -summat poe kaupa ning iga poe kasumimarginaali.</span><span class="sxs-lookup"><span data-stu-id="a6a77-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="a6a77-174">Organisatsiooni üksus põhineb vaikearuandluse hierarhial.</span><span class="sxs-lookup"><span data-stu-id="a6a77-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="a6a77-175">Aruande **Organisatsiooni müük** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6a77-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="a6a77-176">Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Organisatsiooni müügiaruanded**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-176">Go to **Retail \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="a6a77-177">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-178">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="a6a77-179">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6a77-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6a77-180">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a6a77-180">Additional resources</span></span>

- [<span data-ttu-id="a6a77-181">Abiressursid rakenduse Dynamics 365 Retail jaoks</span><span class="sxs-lookup"><span data-stu-id="a6a77-181">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
