---
title: Kulumiarvestus kordaja alusel
description: "Selles artiklis antakse ülevaade teguripõhisest kulumiarvestusmeetodist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d56386db5f1223dd03764d0f515aca6409f2c8a7
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="factor-depreciation"></a><span data-ttu-id="ec56d-103">Kulumiarvestus kordaja alusel</span><span class="sxs-lookup"><span data-stu-id="ec56d-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec56d-104">Selles artiklis antakse ülevaade teguripõhisest kulumiarvestusmeetodist.</span><span class="sxs-lookup"><span data-stu-id="ec56d-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="ec56d-105">Tegurid on põhivarade kulumiarvestuses kasutatavad protsendimäärad.</span><span class="sxs-lookup"><span data-stu-id="ec56d-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="ec56d-106">Kui valite põhivara kulumireegli seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **Tegur**, saate seadistada progresseeruva, degressiivse või lineaarse kulumi.</span><span class="sxs-lookup"><span data-stu-id="ec56d-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="ec56d-107">Progresseeruva kulumi puhul suureneb kulumi summa igal kulumiperioodil.</span><span class="sxs-lookup"><span data-stu-id="ec56d-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="ec56d-108">Degressiivse kulumi puhul väheneb perioodide kulumisumma aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="ec56d-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="ec56d-109">Lineaarse kulumi puhul on kulum igal perioodil ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="ec56d-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="ec56d-110">Järgmiste reeglite ja näidete varal näete, kuidas saate seadistada iga kulumiliigi tegureid.</span><span class="sxs-lookup"><span data-stu-id="ec56d-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="ec56d-111">Märkus. Kui valite väljal **Meetod** väärtuse **Tegur**, kuvatakse väljad **Tegur** ja **Intervall**.</span><span class="sxs-lookup"><span data-stu-id="ec56d-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="ec56d-112">Progresseeruv kulum</span><span class="sxs-lookup"><span data-stu-id="ec56d-112">Progressive depreciation</span></span>
<span data-ttu-id="ec56d-113">Välja **Tegur** väärtus on suurem kui **50**.</span><span class="sxs-lookup"><span data-stu-id="ec56d-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="ec56d-114">Näide</span><span class="sxs-lookup"><span data-stu-id="ec56d-114">Example</span></span>

<span data-ttu-id="ec56d-115">Soetusmaksumus on 100 000, tegur on 70, tööiga on 10 aastat ning kulumiarvestuse algus on 1. jaanuar.</span><span class="sxs-lookup"><span data-stu-id="ec56d-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="ec56d-116">Kulumisummad ja raamatupidamisliku jääkväärtuse summad kuvatakse ainult kasuliku eluea kuue esimese aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="ec56d-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="ec56d-117">Aasta</span><span class="sxs-lookup"><span data-stu-id="ec56d-117">Year</span></span> | <span data-ttu-id="ec56d-118">Periood</span><span class="sxs-lookup"><span data-stu-id="ec56d-118">Period</span></span>      | <span data-ttu-id="ec56d-119">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="ec56d-119">Depreciation amount</span></span> | <span data-ttu-id="ec56d-120">Raamatupidamisliku jääkväärtuse summa</span><span class="sxs-lookup"><span data-stu-id="ec56d-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="ec56d-121">1</span><span class="sxs-lookup"><span data-stu-id="ec56d-121">1</span></span>    | <span data-ttu-id="ec56d-122">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-122">December 31</span></span> | <span data-ttu-id="ec56d-123">307.69</span><span class="sxs-lookup"><span data-stu-id="ec56d-123">307.69</span></span>              | <span data-ttu-id="ec56d-124">99 692.31</span><span class="sxs-lookup"><span data-stu-id="ec56d-124">99,692.31</span></span>             |
| <span data-ttu-id="ec56d-125">2</span><span class="sxs-lookup"><span data-stu-id="ec56d-125">2</span></span>    | <span data-ttu-id="ec56d-126">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-126">December 31</span></span> | <span data-ttu-id="ec56d-127">1447.21</span><span class="sxs-lookup"><span data-stu-id="ec56d-127">1,447.21</span></span>            | <span data-ttu-id="ec56d-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="ec56d-128">98,245.10</span></span>             |
| <span data-ttu-id="ec56d-129">3</span><span class="sxs-lookup"><span data-stu-id="ec56d-129">3</span></span>    | <span data-ttu-id="ec56d-130">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-130">December 31</span></span> | <span data-ttu-id="ec56d-131">3104.50</span><span class="sxs-lookup"><span data-stu-id="ec56d-131">3,104.50</span></span>            | <span data-ttu-id="ec56d-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="ec56d-132">95,140.60</span></span>             |
| <span data-ttu-id="ec56d-133">4</span><span class="sxs-lookup"><span data-stu-id="ec56d-133">4</span></span>    | <span data-ttu-id="ec56d-134">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-134">December 31</span></span> | <span data-ttu-id="ec56d-135">5150.21</span><span class="sxs-lookup"><span data-stu-id="ec56d-135">5,150.21</span></span>            | <span data-ttu-id="ec56d-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="ec56d-136">89,990.39</span></span>             |
| <span data-ttu-id="ec56d-137">5</span><span class="sxs-lookup"><span data-stu-id="ec56d-137">5</span></span>    | <span data-ttu-id="ec56d-138">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-138">December 31</span></span> | <span data-ttu-id="ec56d-139">7522.95</span><span class="sxs-lookup"><span data-stu-id="ec56d-139">7,522.95</span></span>            | <span data-ttu-id="ec56d-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="ec56d-140">82,467.44</span></span>             |
| <span data-ttu-id="ec56d-141">6</span><span class="sxs-lookup"><span data-stu-id="ec56d-141">6</span></span>    | <span data-ttu-id="ec56d-142">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-142">December 31</span></span> | <span data-ttu-id="ec56d-143">10 184.06</span><span class="sxs-lookup"><span data-stu-id="ec56d-143">10,184.06</span></span>           | <span data-ttu-id="ec56d-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="ec56d-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="ec56d-145">Degressiivne kulum</span><span class="sxs-lookup"><span data-stu-id="ec56d-145">Digressive depreciation</span></span>
<span data-ttu-id="ec56d-146">Välja **Tegur** väärtus on väiksem kui **50**.</span><span class="sxs-lookup"><span data-stu-id="ec56d-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="ec56d-147">Näide</span><span class="sxs-lookup"><span data-stu-id="ec56d-147">Example</span></span>

<span data-ttu-id="ec56d-148">Soetusmaksumus on 100 000, tegur on 20, tööiga on 10 aastat ning kulumiarvestuse algus on 1. jaanuar.</span><span class="sxs-lookup"><span data-stu-id="ec56d-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="ec56d-149">Kulumisummad ja raamatupidamisliku jääkväärtuse summad kuvatakse ainult kasuliku eluea kuue esimese aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="ec56d-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="ec56d-150">Aasta</span><span class="sxs-lookup"><span data-stu-id="ec56d-150">Year</span></span> | <span data-ttu-id="ec56d-151">Periood</span><span class="sxs-lookup"><span data-stu-id="ec56d-151">Period</span></span>      | <span data-ttu-id="ec56d-152">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="ec56d-152">Depreciation amount</span></span> | <span data-ttu-id="ec56d-153">Raamatupidamisliku jääkväärtuse summa</span><span class="sxs-lookup"><span data-stu-id="ec56d-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="ec56d-154">1</span><span class="sxs-lookup"><span data-stu-id="ec56d-154">1</span></span>    | <span data-ttu-id="ec56d-155">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-155">December 31</span></span> | <span data-ttu-id="ec56d-156">56 080.43</span><span class="sxs-lookup"><span data-stu-id="ec56d-156">56,080.43</span></span>           | <span data-ttu-id="ec56d-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="ec56d-157">43,919.57</span></span>             |
| <span data-ttu-id="ec56d-158">2</span><span class="sxs-lookup"><span data-stu-id="ec56d-158">2</span></span>    | <span data-ttu-id="ec56d-159">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-159">December 31</span></span> | <span data-ttu-id="ec56d-160">10 665.70</span><span class="sxs-lookup"><span data-stu-id="ec56d-160">10,665.70</span></span>           | <span data-ttu-id="ec56d-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="ec56d-161">33,253.87</span></span>             |
| <span data-ttu-id="ec56d-162">3</span><span class="sxs-lookup"><span data-stu-id="ec56d-162">3</span></span>    | <span data-ttu-id="ec56d-163">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-163">December 31</span></span> | <span data-ttu-id="ec56d-164">7156.22</span><span class="sxs-lookup"><span data-stu-id="ec56d-164">7,156.22</span></span>            | <span data-ttu-id="ec56d-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="ec56d-165">26,097.65</span></span>             |
| <span data-ttu-id="ec56d-166">4</span><span class="sxs-lookup"><span data-stu-id="ec56d-166">4</span></span>    | <span data-ttu-id="ec56d-167">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-167">December 31</span></span> | <span data-ttu-id="ec56d-168">5538.06</span><span class="sxs-lookup"><span data-stu-id="ec56d-168">5,538.06</span></span>            | <span data-ttu-id="ec56d-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="ec56d-169">20,559.59</span></span>             |
| <span data-ttu-id="ec56d-170">5</span><span class="sxs-lookup"><span data-stu-id="ec56d-170">5</span></span>    | <span data-ttu-id="ec56d-171">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-171">December 31</span></span> | <span data-ttu-id="ec56d-172">4579.89</span><span class="sxs-lookup"><span data-stu-id="ec56d-172">4,579.89</span></span>            | <span data-ttu-id="ec56d-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="ec56d-173">15,979.70</span></span>             |
| <span data-ttu-id="ec56d-174">6</span><span class="sxs-lookup"><span data-stu-id="ec56d-174">6</span></span>    | <span data-ttu-id="ec56d-175">31. detsember</span><span class="sxs-lookup"><span data-stu-id="ec56d-175">December 31</span></span> | <span data-ttu-id="ec56d-176">3937.36</span><span class="sxs-lookup"><span data-stu-id="ec56d-176">3,937.36</span></span>            | <span data-ttu-id="ec56d-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="ec56d-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="ec56d-178">Lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="ec56d-178">Straight line depreciation</span></span>
<span data-ttu-id="ec56d-179">Välja **Tegur** väärtus võrdub **50**.</span><span class="sxs-lookup"><span data-stu-id="ec56d-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="ec56d-180">Sellisel juhul on kulum igal perioodil sama ja teil tuleks kaaluda oma teistel väljadel määratud väärtuste mõju. Lugege selle kohta teemat [Lineaarne tööea kulumiarvestus](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="ec56d-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




