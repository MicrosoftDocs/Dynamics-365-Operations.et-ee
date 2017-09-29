---
title: Planeerimise koefitsiendid
description: "See artikkel sisaldab näiteid planeerimise koefitsiendi seadistamise kohta. Selles on teave mitmesuguste planeerimise koefitsiendi sätete ja nende tulemuste kohta. Planeerimise koefitsiendi abil saate määratleda, kuidas eelarvevajadusi vähendada."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 30634b0af343ad171c385a95c4ba0934180f70cf
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="reduction-keys"></a><span data-ttu-id="e5816-105">Planeerimise koefitsiendid</span><span class="sxs-lookup"><span data-stu-id="e5816-105">Reduction keys</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e5816-106">See artikkel sisaldab näiteid planeerimise koefitsiendi seadistamise kohta.</span><span class="sxs-lookup"><span data-stu-id="e5816-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="e5816-107">Selles on teave mitmesuguste planeerimise koefitsiendi sätete ja nende tulemuste kohta.</span><span class="sxs-lookup"><span data-stu-id="e5816-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="e5816-108">Planeerimise koefitsiendi abil saate määratleda, kuidas eelarvevajadusi vähendada.</span><span class="sxs-lookup"><span data-stu-id="e5816-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="e5816-109">1. näide. Prognoosi vähendamise põhimõte Protsent – planeerimise koefitsient</span><span class="sxs-lookup"><span data-stu-id="e5816-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="e5816-110">See näide selgitab, kuidas vähendab planeerimise koefitsient nõudluse prognoosi nõudeid planeerimise koefitsiendiga määratletud protsentide ja perioodide alusel.</span><span class="sxs-lookup"><span data-stu-id="e5816-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1.  <span data-ttu-id="e5816-111">Seadistage lehel **Planeerimise koefitsiendid** järgmised read.</span><span class="sxs-lookup"><span data-stu-id="e5816-111">On the **Reduction keys** page, set up the following lines.</span></span>
    | <span data-ttu-id="e5816-112">Muuda</span><span class="sxs-lookup"><span data-stu-id="e5816-112">Change</span></span> | <span data-ttu-id="e5816-113">Ühik</span><span class="sxs-lookup"><span data-stu-id="e5816-113">Unit</span></span>  | <span data-ttu-id="e5816-114">Protsent</span><span class="sxs-lookup"><span data-stu-id="e5816-114">Percent</span></span> |
    |--------|-------|---------|
    | <span data-ttu-id="e5816-115">1</span><span class="sxs-lookup"><span data-stu-id="e5816-115">1</span></span>      | <span data-ttu-id="e5816-116">Kuu</span><span class="sxs-lookup"><span data-stu-id="e5816-116">Month</span></span> | <span data-ttu-id="e5816-117">100</span><span class="sxs-lookup"><span data-stu-id="e5816-117">100</span></span>     |
    | <span data-ttu-id="e5816-118">2</span><span class="sxs-lookup"><span data-stu-id="e5816-118">2</span></span>      | <span data-ttu-id="e5816-119">Kuu</span><span class="sxs-lookup"><span data-stu-id="e5816-119">Month</span></span> | <span data-ttu-id="e5816-120">75</span><span class="sxs-lookup"><span data-stu-id="e5816-120">75</span></span>      |
    | <span data-ttu-id="e5816-121">3</span><span class="sxs-lookup"><span data-stu-id="e5816-121">3</span></span>      | <span data-ttu-id="e5816-122">Kuu</span><span class="sxs-lookup"><span data-stu-id="e5816-122">Month</span></span> | <span data-ttu-id="e5816-123">50</span><span class="sxs-lookup"><span data-stu-id="e5816-123">50</span></span>      |
    | <span data-ttu-id="e5816-124">4</span><span class="sxs-lookup"><span data-stu-id="e5816-124">4</span></span>      | <span data-ttu-id="e5816-125">Kuu</span><span class="sxs-lookup"><span data-stu-id="e5816-125">Month</span></span> | <span data-ttu-id="e5816-126">25</span><span class="sxs-lookup"><span data-stu-id="e5816-126">25</span></span>      |

2.  <span data-ttu-id="e5816-127">Linkige planeerimise koefitsient kauba laovarude grupiga.</span><span class="sxs-lookup"><span data-stu-id="e5816-127">Link the reduction key to the item's coverage group.</span></span>
3.  <span data-ttu-id="e5816-128">Valige lehel **Koondplaanid** väljal **Vähenduspõhimõte** suvand **Protsent – planeerimise koefitsient**.</span><span class="sxs-lookup"><span data-stu-id="e5816-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4.  <span data-ttu-id="e5816-129">Looge nõudluse prognoos 1000 tk kuus.</span><span class="sxs-lookup"><span data-stu-id="e5816-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="e5816-130">Kui käivitate eelplaneerimise 1. jaanuaril, tabitakse nõudluse prognoosi nõudeid lehel **Planeerimise koefitsiendid** seadistatud protsentide järgi.</span><span class="sxs-lookup"><span data-stu-id="e5816-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="e5816-131">Koondplaani kantakse üle järgmised vajaduse kogused.</span><span class="sxs-lookup"><span data-stu-id="e5816-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="e5816-132">Kuu</span><span class="sxs-lookup"><span data-stu-id="e5816-132">Month</span></span>                | <span data-ttu-id="e5816-133">Vajalik tükkide arv</span><span class="sxs-lookup"><span data-stu-id="e5816-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="e5816-134">Jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-134">January</span></span>              | <span data-ttu-id="e5816-135">0</span><span class="sxs-lookup"><span data-stu-id="e5816-135">0</span></span>                         |
| <span data-ttu-id="e5816-136">Veebruar</span><span class="sxs-lookup"><span data-stu-id="e5816-136">February</span></span>             | <span data-ttu-id="e5816-137">250</span><span class="sxs-lookup"><span data-stu-id="e5816-137">250</span></span>                       |
| <span data-ttu-id="e5816-138">Märts</span><span class="sxs-lookup"><span data-stu-id="e5816-138">March</span></span>                | <span data-ttu-id="e5816-139">500</span><span class="sxs-lookup"><span data-stu-id="e5816-139">500</span></span>                       |
| <span data-ttu-id="e5816-140">aprill</span><span class="sxs-lookup"><span data-stu-id="e5816-140">April</span></span>                | <span data-ttu-id="e5816-141">750</span><span class="sxs-lookup"><span data-stu-id="e5816-141">750</span></span>                       |
| <span data-ttu-id="e5816-142">Mai kuni detsember</span><span class="sxs-lookup"><span data-stu-id="e5816-142">May through December</span></span> | <span data-ttu-id="e5816-143">1000</span><span class="sxs-lookup"><span data-stu-id="e5816-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="e5816-144">2. näide. Prognoosi vähendamise põhimõte Kanded – planeerimise koefitsient</span><span class="sxs-lookup"><span data-stu-id="e5816-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="e5816-145">See näide selgitab, kuidas vähendavad planeerimise koefitsiendiga määratletud perioodide ajal tehtavad tegelikud tellimused nõudluse prognoosi nõudeid.</span><span class="sxs-lookup"><span data-stu-id="e5816-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="e5816-146">Valige lehel **Koondplaanid** väljal **Vähenduspõhimõte** suvand **Kanded – planeerimise koefitsient**.</span><span class="sxs-lookup"><span data-stu-id="e5816-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="e5816-147">1. jaanuaril on olemas järgmised müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="e5816-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="e5816-148">Kuu</span><span class="sxs-lookup"><span data-stu-id="e5816-148">Month</span></span>    | <span data-ttu-id="e5816-149">Tellitud tükkide arv</span><span class="sxs-lookup"><span data-stu-id="e5816-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="e5816-150">Jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-150">January</span></span>  | <span data-ttu-id="e5816-151">956</span><span class="sxs-lookup"><span data-stu-id="e5816-151">956</span></span>                      |
| <span data-ttu-id="e5816-152">Veebruar</span><span class="sxs-lookup"><span data-stu-id="e5816-152">February</span></span> | <span data-ttu-id="e5816-153">1,176</span><span class="sxs-lookup"><span data-stu-id="e5816-153">1,176</span></span>                    |
| <span data-ttu-id="e5816-154">Märts</span><span class="sxs-lookup"><span data-stu-id="e5816-154">March</span></span>    | <span data-ttu-id="e5816-155">451</span><span class="sxs-lookup"><span data-stu-id="e5816-155">451</span></span>                      |
| <span data-ttu-id="e5816-156">Aprill</span><span class="sxs-lookup"><span data-stu-id="e5816-156">April</span></span>    | <span data-ttu-id="e5816-157">119</span><span class="sxs-lookup"><span data-stu-id="e5816-157">119</span></span>                      |

<span data-ttu-id="e5816-158">Kui kasutate sama nõudluse prognoosi (1000 tk kuus), kantakse koondplaani üle järgmised vajaduse kogused.</span><span class="sxs-lookup"><span data-stu-id="e5816-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="e5816-159">Kuu</span><span class="sxs-lookup"><span data-stu-id="e5816-159">Month</span></span>                | <span data-ttu-id="e5816-160">Vajalik tükkide arv</span><span class="sxs-lookup"><span data-stu-id="e5816-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="e5816-161">Jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-161">January</span></span>              | <span data-ttu-id="e5816-162">44</span><span class="sxs-lookup"><span data-stu-id="e5816-162">44</span></span>                        |
| <span data-ttu-id="e5816-163">Veebruar</span><span class="sxs-lookup"><span data-stu-id="e5816-163">February</span></span>             | <span data-ttu-id="e5816-164">0</span><span class="sxs-lookup"><span data-stu-id="e5816-164">0</span></span>                         |
| <span data-ttu-id="e5816-165">Märts</span><span class="sxs-lookup"><span data-stu-id="e5816-165">March</span></span>                | <span data-ttu-id="e5816-166">549</span><span class="sxs-lookup"><span data-stu-id="e5816-166">549</span></span>                       |
| <span data-ttu-id="e5816-167">aprill</span><span class="sxs-lookup"><span data-stu-id="e5816-167">April</span></span>                | <span data-ttu-id="e5816-168">881</span><span class="sxs-lookup"><span data-stu-id="e5816-168">881</span></span>                       |
| <span data-ttu-id="e5816-169">Mai kuni detsember</span><span class="sxs-lookup"><span data-stu-id="e5816-169">May through December</span></span> | <span data-ttu-id="e5816-170">1000</span><span class="sxs-lookup"><span data-stu-id="e5816-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="e5816-171">3. näide. Prognoosi vähendamise põhimõte Kanded – dünaamiline periood</span><span class="sxs-lookup"><span data-stu-id="e5816-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="e5816-172">Enamasti on süsteemid seadistatud nii, et kanded vähendavad nõudluse prognoosi teatud prognoosiperioodide (nädalad, kuud jne) jooksul.</span><span class="sxs-lookup"><span data-stu-id="e5816-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="e5816-173">Need perioodid on määratletud planeerimise koefitsiendis.</span><span class="sxs-lookup"><span data-stu-id="e5816-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="e5816-174">Siiski võib ka kahe nõudluse perioodi rea vaheline aeg *tähendada* perioodi.</span><span class="sxs-lookup"><span data-stu-id="e5816-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1.  <span data-ttu-id="e5816-175">Looge nõudluse prognoos järgmiste kuupäevade ja koguste kohta.</span><span class="sxs-lookup"><span data-stu-id="e5816-175">Create a demand forecast for the following dates and quantities.</span></span>
    | <span data-ttu-id="e5816-176">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="e5816-176">Date</span></span>       | <span data-ttu-id="e5816-177">Nõudluse prognoos</span><span class="sxs-lookup"><span data-stu-id="e5816-177">Demand forecast</span></span> |
    |------------|-----------------|
    | <span data-ttu-id="e5816-178">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-178">January 1</span></span>  | <span data-ttu-id="e5816-179">1000</span><span class="sxs-lookup"><span data-stu-id="e5816-179">1,000</span></span>           |
    | <span data-ttu-id="e5816-180">5. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-180">January 5</span></span>  | <span data-ttu-id="e5816-181">500</span><span class="sxs-lookup"><span data-stu-id="e5816-181">500</span></span>             |
    | <span data-ttu-id="e5816-182">12. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-182">January 12</span></span> | <span data-ttu-id="e5816-183">1000</span><span class="sxs-lookup"><span data-stu-id="e5816-183">1,000</span></span>           |

    <span data-ttu-id="e5816-184">Selles prognoosis ei ole prognoosi kuupäevade vahel selget perioodi: esimese ja teise kuupäeva vahel on neljapäevane vahe ning teise ja kolmanda kuupäeva vahel on seitsmepäevane vahe.</span><span class="sxs-lookup"><span data-stu-id="e5816-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="e5816-185">Need erinevad vahed on dünaamilised perioodid.</span><span class="sxs-lookup"><span data-stu-id="e5816-185">These various spans are the dynamic periods.</span></span>
2.  <span data-ttu-id="e5816-186">Looge müügitellimuse read järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e5816-186">Create sales order lines as follows.</span></span>
    | <span data-ttu-id="e5816-187">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="e5816-187">Date</span></span>                             | <span data-ttu-id="e5816-188">Müügitellimuse kogus</span><span class="sxs-lookup"><span data-stu-id="e5816-188">Sales order quantity</span></span> |
    |----------------------------------|----------------------|
    | <span data-ttu-id="e5816-189">Eelmise aasta 15. detsember</span><span class="sxs-lookup"><span data-stu-id="e5816-189">December 15 in the previous year</span></span> | <span data-ttu-id="e5816-190">500</span><span class="sxs-lookup"><span data-stu-id="e5816-190">500</span></span>                  |
    | <span data-ttu-id="e5816-191">3. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-191">January 3</span></span>                        | <span data-ttu-id="e5816-192">100</span><span class="sxs-lookup"><span data-stu-id="e5816-192">100</span></span>                  |
    | <span data-ttu-id="e5816-193">10. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-193">January 10</span></span>                       | <span data-ttu-id="e5816-194">200</span><span class="sxs-lookup"><span data-stu-id="e5816-194">200</span></span>                  |

<span data-ttu-id="e5816-195">Prognoosi vähendatakse järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e5816-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="e5816-196">Esimene müügitellimus ei jää ühegi perioodi piiresse ega vähenda seega ühtki prognoosi.</span><span class="sxs-lookup"><span data-stu-id="e5816-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="e5816-197">Teine müügitellimus jääb 1. jaanuari ja 5. jaanuari vahele ning vähendab seega prognoosi 1. jaanuariks 100 võrra.</span><span class="sxs-lookup"><span data-stu-id="e5816-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="e5816-198">Kolmas müügitellimus jääb 5. jaanuari ja 12. jaanuari vahele ning vähendab seega prognoosi 5. jaanuariks 200 võrra.</span><span class="sxs-lookup"><span data-stu-id="e5816-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="e5816-199">Järgmine plaanitud tellimus luuakse prognoosi täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="e5816-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="e5816-200">Nõudluse prognoosi kuupäev</span><span class="sxs-lookup"><span data-stu-id="e5816-200">Demand forecast date</span></span> | <span data-ttu-id="e5816-201">Vähendatud kogus</span><span class="sxs-lookup"><span data-stu-id="e5816-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="e5816-202">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-202">January 1</span></span>            | <span data-ttu-id="e5816-203">900</span><span class="sxs-lookup"><span data-stu-id="e5816-203">900</span></span>              |
| <span data-ttu-id="e5816-204">5. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-204">January 5</span></span>            | <span data-ttu-id="e5816-205">300</span><span class="sxs-lookup"><span data-stu-id="e5816-205">300</span></span>              |
| <span data-ttu-id="e5816-206">12. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e5816-206">January 12</span></span>           | <span data-ttu-id="e5816-207">1000</span><span class="sxs-lookup"><span data-stu-id="e5816-207">1,000</span></span>            |

<span data-ttu-id="e5816-208">Siin on toodud vähenduse **Kanded – dünaamiline periood** kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="e5816-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="e5816-209">Eelarvevajadusi vähendatakse tegelike tellimusekannete võrra, mis tehakse dünaamilise perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="e5816-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="e5816-210">Dünaamiline periood katab praeguse eelarve kuupäevad ja lõpeb järgmise prognoosi algusega.</span><span class="sxs-lookup"><span data-stu-id="e5816-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="e5816-211">See meetod ei kasuta ega nõua planeerimise koefitsienti.</span><span class="sxs-lookup"><span data-stu-id="e5816-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="e5816-212">Selle suvandi kasutamisel ilmneb järgmine käitumine.</span><span class="sxs-lookup"><span data-stu-id="e5816-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="e5816-213">Prognoosi täielikul vähendamisel muutub praeguse prognoosi eelarvevajaduseks 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e5816-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="e5816-214">Kui tulevasi prognoose pole, vähendatakse eelarvevajadusi viimati sisestatud prognoosist.</span><span class="sxs-lookup"><span data-stu-id="e5816-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="e5816-215">Prognoosi vähenduse arvutamisse kaasatakse ajapiirid.</span><span class="sxs-lookup"><span data-stu-id="e5816-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="e5816-216">Prognoosi vähenduse arvutamisse kaasatakse positiivne päevade arv.</span><span class="sxs-lookup"><span data-stu-id="e5816-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="e5816-217">Kui tellimuse tegelikud kanded ületavad eelarvevajadusi, ei edastata järelejäänud kandeid järgmisse prognoosiperioodi.</span><span class="sxs-lookup"><span data-stu-id="e5816-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="e5816-218">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e5816-218">See also</span></span>
--------

[<span data-ttu-id="e5816-219">Koondplaanid</span><span class="sxs-lookup"><span data-stu-id="e5816-219">Master plans</span></span>](master-plans.md)




