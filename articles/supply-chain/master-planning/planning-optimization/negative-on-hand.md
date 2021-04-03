---
title: Negatiivsete vabade kogustega plaanimine
description: Selles teemas selgitatakse, kuidas plaanimise optimeerimise kasutamisel käsitsetakse negatiivset kaubavaru.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ba36d87a991a3b0088800313da2cac3a769f2894
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232298"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="6bdd9-103">Negatiivsete vabade kogustega plaanimine</span><span class="sxs-lookup"><span data-stu-id="6bdd9-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6bdd9-104">Kui süsteem näitab negatiivset kaubavaru kogust, käsitleb planeerimise mootor kogust kui 0 (null), et aidata vältida ületarnet.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="6bdd9-105">See funktsioon töötab järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="6bdd9-106">Planeerimise optimeerimise funktsioon koondab vabad kogused laovarude dimensioonide madalaimal tasemel.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="6bdd9-107">(Näiteks kui *asukoht* ei ole laevarude dimensioon, koondab plaanimise optimeerimine vabad kogused *lao* tasemel.)</span><span class="sxs-lookup"><span data-stu-id="6bdd9-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="6bdd9-108">Kui laovarude dimensioonide kaubavaru kogus on negatiivne, eeldab süsteem, et vaba kogus on tegelikult 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6bdd9-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bdd9-109">Planeerimise süsteem võib olla ainult nii täpne kui sisendandmed.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="6bdd9-110">Kui sisendandmed on ebatäpsed, näitavad negatiivsed varude kirjed, et Microsoft Dynamics 365 Supply Chain Managementi varude teave on reaalse maailmaga sünkroonist väljas.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="6bdd9-111">Seetõttu on planeerimise tulemus vigane.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="6bdd9-112">Täpse planeerimise tulemuse saamiseks tuleb minimeerida kirjete arv, mis näitavad negatiivset vaba kogust.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="6bdd9-113">Näide 1</span><span class="sxs-lookup"><span data-stu-id="6bdd9-113">Example 1</span></span>

<span data-ttu-id="6bdd9-114">Ladu 13 on konfigureeritud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="6bdd9-115">**Katvuse kood:** min/max</span><span class="sxs-lookup"><span data-stu-id="6bdd9-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="6bdd9-116">**Miinimum:** 15 tükki (tk)</span><span class="sxs-lookup"><span data-stu-id="6bdd9-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="6bdd9-117">**Maksimum:** 25 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="6bdd9-118">Laovarude dimensioonide madalaim tase on *ladu* ja järgmised vabad kogused salvestatakse *asukoha* tasemel.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="6bdd9-119">**Tegevuskoht 1, ladu 13, asukoht 1:** 20 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="6bdd9-120">**Tegevuskoht 1, ladu 13, asukoht 2:** &minus;8 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="6bdd9-121">Seega on lao 13 kaubavaru kogus 12 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="6bdd9-122">(= 20 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-122">(= 20 pcs.</span></span> <span data-ttu-id="6bdd9-123">&minus; 8 tk).</span><span class="sxs-lookup"><span data-stu-id="6bdd9-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="6bdd9-124">Sellisel juhul kasutab planeerimise mootor kaubavaru kogust 12 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="6bdd9-125">lao 13 jaoks.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-125">for warehouse 13.</span></span>

<span data-ttu-id="6bdd9-126">Tulemuseks on plaanitud tellimus 13 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="6bdd9-127">(= 25 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-127">(= 25 pcs.</span></span> <span data-ttu-id="6bdd9-128">&minus;12 tk), et täita ladu 13 koguselt 12 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="6bdd9-129">kogusele 25 tk.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="6bdd9-130">Näide 2</span><span class="sxs-lookup"><span data-stu-id="6bdd9-130">Example 2</span></span>

<span data-ttu-id="6bdd9-131">Ladu 13 on konfigureeritud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="6bdd9-132">**Katvuse kood:** min/max</span><span class="sxs-lookup"><span data-stu-id="6bdd9-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="6bdd9-133">**Miinimum:** 15 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="6bdd9-134">**Maksimum:** 25 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="6bdd9-135">Laovarude dimensioonide madalaim tase on *ladu* ja järgmised vabad kogused salvestatakse *asukoha* tasemel.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="6bdd9-136">**Tegevuskoht 1, ladu 13, asukoht 1:** 4 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="6bdd9-137">**Tegevuskoht 1, ladu 13, asukoht 2:** &minus;8 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="6bdd9-138">Seega on lao 13 kaubavaru kogus &minus;4 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="6bdd9-139">(= 4 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-139">(= 4 pcs.</span></span> <span data-ttu-id="6bdd9-140">&minus; 8 tk).</span><span class="sxs-lookup"><span data-stu-id="6bdd9-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="6bdd9-141">Teisisõnu on see vähem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6bdd9-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="6bdd9-142">Sellisel juhul eeldab planeerimise mootor, et lao 13 vaba kogus on 0 tk,</span><span class="sxs-lookup"><span data-stu-id="6bdd9-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="6bdd9-143">mitte &minus;4 tk.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="6bdd9-144">Tulemuseks on plaanitud tellimus 25 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="6bdd9-145">(= 25 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-145">(= 25 pcs.</span></span> <span data-ttu-id="6bdd9-146">&minus; 0 tk), et täita ladu 13 koguselt 0 tk</span><span class="sxs-lookup"><span data-stu-id="6bdd9-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="6bdd9-147">kogusele 25 tk.</span><span class="sxs-lookup"><span data-stu-id="6bdd9-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="6bdd9-148">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="6bdd9-148">Related resources</span></span>

[<span data-ttu-id="6bdd9-149">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="6bdd9-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="6bdd9-150">Planeerimise optimeerimisega alustamine</span><span class="sxs-lookup"><span data-stu-id="6bdd9-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="6bdd9-151">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="6bdd9-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="6bdd9-152">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="6bdd9-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="6bdd9-153">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="6bdd9-153">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]