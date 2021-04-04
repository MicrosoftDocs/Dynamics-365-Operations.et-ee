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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ec93bd8ef8dea6ca979dee1819a9c9abcc38a2e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251477"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="467e1-103">Võrgukanali aruannete loomine</span><span class="sxs-lookup"><span data-stu-id="467e1-103">Generate online channel reports</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="467e1-104">See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="467e1-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="467e1-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="467e1-105">Overview</span></span>

<span data-ttu-id="467e1-106">Rakenduses Commerce saadete luua ja vaadata mitut aruannet, et näha, kuidas võrgukanal toimib.</span><span class="sxs-lookup"><span data-stu-id="467e1-106">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="467e1-107">Kanali koondaruanne</span><span class="sxs-lookup"><span data-stu-id="467e1-107">Channel summary report</span></span>

<span data-ttu-id="467e1-108">Aruanne **Kanali kokkuvõte** kuvab valitud kanali järgmiste kannete kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="467e1-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="467e1-109">Müügikanded</span><span class="sxs-lookup"><span data-stu-id="467e1-109">Sales transactions</span></span>
- <span data-ttu-id="467e1-110">Maksekanded</span><span class="sxs-lookup"><span data-stu-id="467e1-110">Payment transactions</span></span>
- <span data-ttu-id="467e1-111">Maksukanded</span><span class="sxs-lookup"><span data-stu-id="467e1-111">Tax transactions</span></span>
- <span data-ttu-id="467e1-112">Allahinnatud kanded</span><span class="sxs-lookup"><span data-stu-id="467e1-112">Discounted transactions</span></span>

<span data-ttu-id="467e1-113">Aruande **Kanali kokkuvõte** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="467e1-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="467e1-114">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali koondaruanne**.</span><span class="sxs-lookup"><span data-stu-id="467e1-114">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="467e1-115">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="467e1-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-116">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="467e1-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-117">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="467e1-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="467e1-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="467e1-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="467e1-119">Kanali müügiaruanne aastate alusel</span><span class="sxs-lookup"><span data-stu-id="467e1-119">Channel sales by year report</span></span> 

<span data-ttu-id="467e1-120">Aruanne **Kanali müük aastate alusel** näitab kindla poe müügi võrdlust aastate lõikes.</span><span class="sxs-lookup"><span data-stu-id="467e1-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="467e1-121">Teie valite aasta, mille müüki võrrelda, ja aruanne võrdleb valitud aasta müüki eelmise aasta müügiga.</span><span class="sxs-lookup"><span data-stu-id="467e1-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="467e1-122">Aruande **Kanali müük aastate alusel** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="467e1-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="467e1-123">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali aastapõhine müügiaruanne**.</span><span class="sxs-lookup"><span data-stu-id="467e1-123">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="467e1-124">Sisestage väljale **Kalendriaastast** aasta.</span><span class="sxs-lookup"><span data-stu-id="467e1-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="467e1-125">Sisestage väljale **Kalendriaastani** aasta.</span><span class="sxs-lookup"><span data-stu-id="467e1-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="467e1-126">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="467e1-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="467e1-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="467e1-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="467e1-128">Kanali müügiaruanne tundide alusel</span><span class="sxs-lookup"><span data-stu-id="467e1-128">Channel sales by hour report</span></span>

<span data-ttu-id="467e1-129">Aruanne **Kanali müük tundide alusel** näitab valitud kanali või tootmisüksuse müügimõõdikuid tunni alusel.</span><span class="sxs-lookup"><span data-stu-id="467e1-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="467e1-130">Aruande **Kanali müük tundide alusel** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="467e1-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="467e1-131">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kanali tunnipõhine müügiaruanne**.</span><span class="sxs-lookup"><span data-stu-id="467e1-131">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="467e1-132">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="467e1-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-133">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="467e1-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-134">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="467e1-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="467e1-135">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="467e1-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="467e1-136">Parimate klientide aruanne</span><span class="sxs-lookup"><span data-stu-id="467e1-136">Top customers report</span></span>

<span data-ttu-id="467e1-137">Aruanne **Parimad kliendid** näitab valitud kanali või tootmisüksuse parima *N* kliendi müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="467e1-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="467e1-138">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="467e1-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="467e1-139">Aruande **Parimad kliendid** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="467e1-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="467e1-140">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste klientide aruanne**.</span><span class="sxs-lookup"><span data-stu-id="467e1-140">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="467e1-141">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="467e1-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-142">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="467e1-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-143">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="467e1-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="467e1-144">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="467e1-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="467e1-145">Peamiste allahindluste aruanne</span><span class="sxs-lookup"><span data-stu-id="467e1-145">Top discounts report</span></span>

<span data-ttu-id="467e1-146">Aruanne **Peamised allahindlused** näitab valitud kanali või tootmisüksuse peamise *N* allahindluse müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="467e1-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="467e1-147">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="467e1-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="467e1-148">Aruande **Peamised allahindlused** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="467e1-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="467e1-149">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste allahindluste aruanne**.</span><span class="sxs-lookup"><span data-stu-id="467e1-149">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="467e1-150">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="467e1-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-151">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="467e1-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-152">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="467e1-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="467e1-153">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="467e1-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="467e1-154">Peamiste toodete aruanne</span><span class="sxs-lookup"><span data-stu-id="467e1-154">Top products report</span></span>

<span data-ttu-id="467e1-155">Aruanne **Peamised tooted** näitab valitud kanali või tootmisüksuse peamise *N* toote müügimõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="467e1-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="467e1-156">Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.</span><span class="sxs-lookup"><span data-stu-id="467e1-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="467e1-157">Aruande **Peamised tooted** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="467e1-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="467e1-158">Avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Peamiste toodete aruanne**.</span><span class="sxs-lookup"><span data-stu-id="467e1-158">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="467e1-159">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="467e1-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-160">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="467e1-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-161">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="467e1-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="467e1-162">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="467e1-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="467e1-163">Kategooria müügiaruanne</span><span class="sxs-lookup"><span data-stu-id="467e1-163">Category sales report</span></span>

<span data-ttu-id="467e1-164">Aruanne **Kategooria müük** näitab valitud kanali või tootmisüksuse kategooriahierarhia iga sõlme müügimõõdikuid valitud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="467e1-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="467e1-165">Aruande **Kategooria müük** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="467e1-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="467e1-166">Minge jaotisse **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Kategooria müügiaruanded**.</span><span class="sxs-lookup"><span data-stu-id="467e1-166">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="467e1-167">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="467e1-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-168">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="467e1-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-169">Valige väljal **Kanal** võrgukanal.</span><span class="sxs-lookup"><span data-stu-id="467e1-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="467e1-170">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="467e1-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="467e1-171">Organisatsiooni müügiaruanne</span><span class="sxs-lookup"><span data-stu-id="467e1-171">Organization sales report</span></span>

<span data-ttu-id="467e1-172">Aruanne **Organisatsiooni müük** näitab teie kaupluste jõudlust organisatsiooni üksuse järgi.</span><span class="sxs-lookup"><span data-stu-id="467e1-172">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="467e1-173">See aruanne sisaldab müügikogust ja -summat poe kaupa ning iga poe kasumimarginaali.</span><span class="sxs-lookup"><span data-stu-id="467e1-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="467e1-174">Organisatsiooni üksus põhineb vaikearuandluse hierarhial.</span><span class="sxs-lookup"><span data-stu-id="467e1-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="467e1-175">Aruande **Organisatsiooni müük** loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="467e1-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="467e1-176">Minge jaotisse **Jaemüük ja kaubandus \> Päringud ja aruanded \> Müügiaruanded \> Organisatsiooni müügiaruanded**.</span><span class="sxs-lookup"><span data-stu-id="467e1-176">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="467e1-177">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="467e1-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-178">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="467e1-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="467e1-179">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="467e1-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="467e1-180">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="467e1-180">Additional resources</span></span>

- [<span data-ttu-id="467e1-181">Commerce’i avaleht</span><span class="sxs-lookup"><span data-stu-id="467e1-181">Commerce home page</span></span>](../retail/index.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]