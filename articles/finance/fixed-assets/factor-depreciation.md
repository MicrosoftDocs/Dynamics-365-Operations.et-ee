---
title: Kulumiarvestus kordaja alusel
description: Selles artiklis antakse ülevaade teguripõhisest kulumiarvestusmeetodist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87cca8b3472f572cd1c4ba3d894269f7ba0f248a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241070"
---
# <a name="factor-depreciation"></a><span data-ttu-id="8499e-103">Kulumiarvestus kordaja alusel</span><span class="sxs-lookup"><span data-stu-id="8499e-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8499e-104">Selles artiklis antakse ülevaade teguripõhisest kulumiarvestusmeetodist.</span><span class="sxs-lookup"><span data-stu-id="8499e-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="8499e-105">Tegurid on põhivarade kulumiarvestuses kasutatavad protsendimäärad.</span><span class="sxs-lookup"><span data-stu-id="8499e-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="8499e-106">Kui valite põhivara kulumireegli seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **Tegur**, saate seadistada progresseeruva, degressiivse või lineaarse kulumi.</span><span class="sxs-lookup"><span data-stu-id="8499e-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="8499e-107">Progresseeruva kulumi puhul suureneb kulumi summa igal kulumiperioodil.</span><span class="sxs-lookup"><span data-stu-id="8499e-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="8499e-108">Degressiivse kulumi puhul väheneb perioodide kulumisumma aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="8499e-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="8499e-109">Lineaarse kulumi puhul on kulum igal perioodil ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="8499e-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="8499e-110">Järgmiste reeglite ja näidete varal näete, kuidas saate seadistada iga kulumiliigi tegureid.</span><span class="sxs-lookup"><span data-stu-id="8499e-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="8499e-111">Märkus. Kui valite väljal **Meetod** väärtuse **Tegur**, kuvatakse väljad **Tegur** ja **Intervall**.</span><span class="sxs-lookup"><span data-stu-id="8499e-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="8499e-112">Progresseeruv kulum</span><span class="sxs-lookup"><span data-stu-id="8499e-112">Progressive depreciation</span></span>
<span data-ttu-id="8499e-113">Välja **Tegur** väärtus on suurem kui **50**.</span><span class="sxs-lookup"><span data-stu-id="8499e-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="8499e-114">Näide</span><span class="sxs-lookup"><span data-stu-id="8499e-114">Example</span></span>

<span data-ttu-id="8499e-115">Soetusmaksumus on 100 000, tegur on 70, tööiga on 10 aastat ning kulumiarvestuse algus on 1. jaanuar.</span><span class="sxs-lookup"><span data-stu-id="8499e-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="8499e-116">Kulumisummad ja raamatupidamisliku jääkväärtuse summad kuvatakse ainult kasuliku eluea kuue esimese aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="8499e-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="8499e-117">Aasta</span><span class="sxs-lookup"><span data-stu-id="8499e-117">Year</span></span> | <span data-ttu-id="8499e-118">Periood</span><span class="sxs-lookup"><span data-stu-id="8499e-118">Period</span></span>      | <span data-ttu-id="8499e-119">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="8499e-119">Depreciation amount</span></span> | <span data-ttu-id="8499e-120">Raamatupidamisliku jääkväärtuse summa</span><span class="sxs-lookup"><span data-stu-id="8499e-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="8499e-121">1</span><span class="sxs-lookup"><span data-stu-id="8499e-121">1</span></span>    | <span data-ttu-id="8499e-122">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-122">December 31</span></span> | <span data-ttu-id="8499e-123">307.69</span><span class="sxs-lookup"><span data-stu-id="8499e-123">307.69</span></span>              | <span data-ttu-id="8499e-124">99 692.31</span><span class="sxs-lookup"><span data-stu-id="8499e-124">99,692.31</span></span>             |
| <span data-ttu-id="8499e-125">2</span><span class="sxs-lookup"><span data-stu-id="8499e-125">2</span></span>    | <span data-ttu-id="8499e-126">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-126">December 31</span></span> | <span data-ttu-id="8499e-127">1447.21</span><span class="sxs-lookup"><span data-stu-id="8499e-127">1,447.21</span></span>            | <span data-ttu-id="8499e-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="8499e-128">98,245.10</span></span>             |
| <span data-ttu-id="8499e-129">3</span><span class="sxs-lookup"><span data-stu-id="8499e-129">3</span></span>    | <span data-ttu-id="8499e-130">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-130">December 31</span></span> | <span data-ttu-id="8499e-131">3104.50</span><span class="sxs-lookup"><span data-stu-id="8499e-131">3,104.50</span></span>            | <span data-ttu-id="8499e-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="8499e-132">95,140.60</span></span>             |
| <span data-ttu-id="8499e-133">4</span><span class="sxs-lookup"><span data-stu-id="8499e-133">4</span></span>    | <span data-ttu-id="8499e-134">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-134">December 31</span></span> | <span data-ttu-id="8499e-135">5150.21</span><span class="sxs-lookup"><span data-stu-id="8499e-135">5,150.21</span></span>            | <span data-ttu-id="8499e-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="8499e-136">89,990.39</span></span>             |
| <span data-ttu-id="8499e-137">5</span><span class="sxs-lookup"><span data-stu-id="8499e-137">5</span></span>    | <span data-ttu-id="8499e-138">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-138">December 31</span></span> | <span data-ttu-id="8499e-139">7522.95</span><span class="sxs-lookup"><span data-stu-id="8499e-139">7,522.95</span></span>            | <span data-ttu-id="8499e-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="8499e-140">82,467.44</span></span>             |
| <span data-ttu-id="8499e-141">6</span><span class="sxs-lookup"><span data-stu-id="8499e-141">6</span></span>    | <span data-ttu-id="8499e-142">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-142">December 31</span></span> | <span data-ttu-id="8499e-143">10 184.06</span><span class="sxs-lookup"><span data-stu-id="8499e-143">10,184.06</span></span>           | <span data-ttu-id="8499e-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="8499e-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="8499e-145">Degressiivne kulum</span><span class="sxs-lookup"><span data-stu-id="8499e-145">Digressive depreciation</span></span>
<span data-ttu-id="8499e-146">Välja **Tegur** väärtus on väiksem kui **50**.</span><span class="sxs-lookup"><span data-stu-id="8499e-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="8499e-147">Näide</span><span class="sxs-lookup"><span data-stu-id="8499e-147">Example</span></span>

<span data-ttu-id="8499e-148">Soetusmaksumus on 100 000, tegur on 20, tööiga on 10 aastat ning kulumiarvestuse algus on 1. jaanuar.</span><span class="sxs-lookup"><span data-stu-id="8499e-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="8499e-149">Kulumisummad ja raamatupidamisliku jääkväärtuse summad kuvatakse ainult kasuliku eluea kuue esimese aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="8499e-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="8499e-150">Aasta</span><span class="sxs-lookup"><span data-stu-id="8499e-150">Year</span></span> | <span data-ttu-id="8499e-151">Periood</span><span class="sxs-lookup"><span data-stu-id="8499e-151">Period</span></span>      | <span data-ttu-id="8499e-152">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="8499e-152">Depreciation amount</span></span> | <span data-ttu-id="8499e-153">Raamatupidamisliku jääkväärtuse summa</span><span class="sxs-lookup"><span data-stu-id="8499e-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="8499e-154">1</span><span class="sxs-lookup"><span data-stu-id="8499e-154">1</span></span>    | <span data-ttu-id="8499e-155">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-155">December 31</span></span> | <span data-ttu-id="8499e-156">56 080.43</span><span class="sxs-lookup"><span data-stu-id="8499e-156">56,080.43</span></span>           | <span data-ttu-id="8499e-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="8499e-157">43,919.57</span></span>             |
| <span data-ttu-id="8499e-158">2</span><span class="sxs-lookup"><span data-stu-id="8499e-158">2</span></span>    | <span data-ttu-id="8499e-159">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-159">December 31</span></span> | <span data-ttu-id="8499e-160">10 665.70</span><span class="sxs-lookup"><span data-stu-id="8499e-160">10,665.70</span></span>           | <span data-ttu-id="8499e-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="8499e-161">33,253.87</span></span>             |
| <span data-ttu-id="8499e-162">3</span><span class="sxs-lookup"><span data-stu-id="8499e-162">3</span></span>    | <span data-ttu-id="8499e-163">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-163">December 31</span></span> | <span data-ttu-id="8499e-164">7156.22</span><span class="sxs-lookup"><span data-stu-id="8499e-164">7,156.22</span></span>            | <span data-ttu-id="8499e-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="8499e-165">26,097.65</span></span>             |
| <span data-ttu-id="8499e-166">4</span><span class="sxs-lookup"><span data-stu-id="8499e-166">4</span></span>    | <span data-ttu-id="8499e-167">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-167">December 31</span></span> | <span data-ttu-id="8499e-168">5538.06</span><span class="sxs-lookup"><span data-stu-id="8499e-168">5,538.06</span></span>            | <span data-ttu-id="8499e-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="8499e-169">20,559.59</span></span>             |
| <span data-ttu-id="8499e-170">5</span><span class="sxs-lookup"><span data-stu-id="8499e-170">5</span></span>    | <span data-ttu-id="8499e-171">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-171">December 31</span></span> | <span data-ttu-id="8499e-172">4579.89</span><span class="sxs-lookup"><span data-stu-id="8499e-172">4,579.89</span></span>            | <span data-ttu-id="8499e-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="8499e-173">15,979.70</span></span>             |
| <span data-ttu-id="8499e-174">6</span><span class="sxs-lookup"><span data-stu-id="8499e-174">6</span></span>    | <span data-ttu-id="8499e-175">31. detsember</span><span class="sxs-lookup"><span data-stu-id="8499e-175">December 31</span></span> | <span data-ttu-id="8499e-176">3937.36</span><span class="sxs-lookup"><span data-stu-id="8499e-176">3,937.36</span></span>            | <span data-ttu-id="8499e-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="8499e-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="8499e-178">Lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="8499e-178">Straight line depreciation</span></span>
<span data-ttu-id="8499e-179">Välja **Tegur** väärtus võrdub **50**.</span><span class="sxs-lookup"><span data-stu-id="8499e-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="8499e-180">Sellisel juhul on kulum igal perioodil sama ja teil tuleks kaaluda oma teistel väljadel määratud väärtuste mõju. Lugege selle kohta teemat [Lineaarne tööea kulumiarvestus](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="8499e-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]