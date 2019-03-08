---
title: Puhkuste ja puudumiste põhimõtted
description: Selles teemas kirjeldatakse puhkuste ja puudumiste mõisteid ja kuidas vaba aja saldosid määratletakse.
author: jcart
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 563593d6c93b0488c681f5b43004f5c0d22cc004
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304119"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="62567-103">Puhkuste ja puudumiste põhimõtted</span><span class="sxs-lookup"><span data-stu-id="62567-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="62567-104">Mõistete ja tingimuste abil, mida selles teemas kirjeldatakse, saate määrata, kuidas antakse töötajale töölt vaba aega ja kuidas selle töötaja ajasaldosid arvutada.</span><span class="sxs-lookup"><span data-stu-id="62567-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="62567-105">Puhkuste ja puudumiste halduse kohta lisateabe saamiseks vt [Puhkuste ja puudumiste haldus](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="62567-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="62567-106">Puhkuseplaani üksikasjad</span><span class="sxs-lookup"><span data-stu-id="62567-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="62567-107">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-107">Start date</span></span>

<span data-ttu-id="62567-108">Alguskuupäev on see kuupäev, mil viitvõlgade töötlus algab.</span><span class="sxs-lookup"><span data-stu-id="62567-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="62567-109">Alguskuupäev on samas ka edasikantavate summade arvutamiseks kasutatav tähtpäeva kuupäev.</span><span class="sxs-lookup"><span data-stu-id="62567-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="62567-110">Viitvõlad</span><span class="sxs-lookup"><span data-stu-id="62567-110">Accruals</span></span>

<span data-ttu-id="62567-111">Viitvõlad määravad, millal ja kui sageli määratakse töötajale vaba aega.</span><span class="sxs-lookup"><span data-stu-id="62567-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="62567-112">Poliitika selle kohta, millal viitvõlgu määrata, ja poliitika proportsionaalse arvestuse kohta on määratletud jaotises **Viitvõlad** puhkuste ja puudumiste plaani loomisel.</span><span class="sxs-lookup"><span data-stu-id="62567-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="62567-113">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-113">Accrual frequency</span></span>

<span data-ttu-id="62567-114">Puhkuse andmise sagedus määratleb, kui tihti on puhkus kogunenud või määratud.</span><span class="sxs-lookup"><span data-stu-id="62567-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="62567-115">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="62567-115">The following options are available:</span></span>

- <span data-ttu-id="62567-116">Kord päevas</span><span class="sxs-lookup"><span data-stu-id="62567-116">Daily</span></span>
- <span data-ttu-id="62567-117">Iganädalane</span><span class="sxs-lookup"><span data-stu-id="62567-117">Weekly</span></span>
- <span data-ttu-id="62567-118">Kaks korda nädalas</span><span class="sxs-lookup"><span data-stu-id="62567-118">Biweekly</span></span>
- <span data-ttu-id="62567-119">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="62567-119">Semimonthly</span></span>
- <span data-ttu-id="62567-120">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="62567-120">Monthly</span></span>
- <span data-ttu-id="62567-121">Kord kvartalis</span><span class="sxs-lookup"><span data-stu-id="62567-121">Quarterly</span></span>
- <span data-ttu-id="62567-122">Poolaasta kohta</span><span class="sxs-lookup"><span data-stu-id="62567-122">Semiannually</span></span>
- <span data-ttu-id="62567-123">Kord aastas</span><span class="sxs-lookup"><span data-stu-id="62567-123">Annually</span></span>
- <span data-ttu-id="62567-124">Pole</span><span class="sxs-lookup"><span data-stu-id="62567-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="62567-125">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-125">Accrual period basis</span></span>

<span data-ttu-id="62567-126">Puhkuseperioodi baas määratleb kuupäeva, mida kasutatakse puhkuseperioodi arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="62567-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="62567-127">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="62567-127">The following options are available:</span></span>

- <span data-ttu-id="62567-128">**Plaanitav alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="62567-128">**Plan start date**</span></span>
- <span data-ttu-id="62567-129">**Töötajale kindlal kuupäeval** - selle suvandi valimisel määratleb selle väärtus puhkuseperioodide alguskuupäeva allikat.</span><span class="sxs-lookup"><span data-stu-id="62567-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="62567-130">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="62567-130">The following options are available:</span></span>

    - <span data-ttu-id="62567-131">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="62567-131">Custom</span></span>
    - <span data-ttu-id="62567-132">Tähtpäeva kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-132">Anniversary date</span></span>
    - <span data-ttu-id="62567-133">Värbamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-133">Original hire date</span></span>
    - <span data-ttu-id="62567-134">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="62567-134">Seniority date</span></span>
    - <span data-ttu-id="62567-135">Töötaja töösuhte korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="62567-136">Töötaja töösuhte alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="62567-137">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-137">Accrual award date</span></span>

<span data-ttu-id="62567-138">Puhkuse andmise kuupäev määrab, millal antakse töötajale vaba aega.</span><span class="sxs-lookup"><span data-stu-id="62567-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="62567-139">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="62567-139">The following options are available:</span></span>

- <span data-ttu-id="62567-140">**Viitvõlgade lõppkuupäev** – töötajale määratakse puhkus puhkuseperioodi viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="62567-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="62567-141">Õige koguse lisandumisel peab viitvõlgade protsess sisaldama kogu perioodi.</span><span class="sxs-lookup"><span data-stu-id="62567-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="62567-142">Näiteks puhkuseperiood on 1. jaanuarist 2018 kuni 31. jaanuarini 2018.</span><span class="sxs-lookup"><span data-stu-id="62567-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="62567-143">Sel juhul, et kaasata jaanuari, käivitatakse viitvõlg 1. veebruaril 2018.</span><span class="sxs-lookup"><span data-stu-id="62567-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="62567-144">**Viitvõlgade alguskuupäev** – töötajale määratakse puhkus puhkuseperioodi esimesel päeval.</span><span class="sxs-lookup"><span data-stu-id="62567-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="62567-145">Viitvõlgade poliitika registreerimine</span><span class="sxs-lookup"><span data-stu-id="62567-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="62567-146">Viitvõlgade poliitika registreerimise määratleb viitvõlgade arvutamise, kui töötaja on liitunud keset puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="62567-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="62567-147">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="62567-147">The following options are available:</span></span>

- <span data-ttu-id="62567-148">**Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani.</span><span class="sxs-lookup"><span data-stu-id="62567-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="62567-149">Viitvõlgade töötlemisel rakendatakse seda erinevust.</span><span class="sxs-lookup"><span data-stu-id="62567-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="62567-150">**Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="62567-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="62567-151">**Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="62567-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="62567-152">Viitvõlgade poliitika registreerimise tühistamise kohta</span><span class="sxs-lookup"><span data-stu-id="62567-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="62567-153">Viitvõlgade poliitika registreerimise tühistamise kohta määratleb viitvõlgade arvutamise, kui töötaja on lahkunud keset puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="62567-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="62567-154">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="62567-154">The following options are available:</span></span>

- <span data-ttu-id="62567-155">**Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani.</span><span class="sxs-lookup"><span data-stu-id="62567-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="62567-156">Viitvõlgade töötlemisel rakendatakse seda erinevust.</span><span class="sxs-lookup"><span data-stu-id="62567-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="62567-157">**Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="62567-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="62567-158">**Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="62567-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="62567-159">Viitvõlgade skeemid</span><span class="sxs-lookup"><span data-stu-id="62567-159">Accrual schedule</span></span>

<span data-ttu-id="62567-160">Viitvõlgade graafik määrab, kuidas töötaja puhkuse aeg koguneb ja millised summad antud töötajal kogunevad ja edasi kanduvad.</span><span class="sxs-lookup"><span data-stu-id="62567-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="62567-161">Järkusid saab luua nii, et vaba aega premeeritakse erinevate tasemete alusel.</span><span class="sxs-lookup"><span data-stu-id="62567-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="62567-162">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="62567-162">Months of service</span></span>

<span data-ttu-id="62567-163">Jaotise **Töötatud kuud** väärtus määratleb kuude miinimumarvu, kui palju töötaja peab töötama, et tal oleks õigus viitvõlgadele.</span><span class="sxs-lookup"><span data-stu-id="62567-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="62567-164">Kui miinimuumarv töötajate kohta puudub, määrake väärtuseks **0**.</span><span class="sxs-lookup"><span data-stu-id="62567-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="62567-165">Töötunnid</span><span class="sxs-lookup"><span data-stu-id="62567-165">Hours worked</span></span>

<span data-ttu-id="62567-166">Jaotise **Töötunnid** väärtus määratleb tundide miinimumarvu, kui palju töötaja peab puhkuseperioodi kohta töötama, et tal oleks õigus viitvõlgadele.</span><span class="sxs-lookup"><span data-stu-id="62567-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="62567-167">Kui miinimuumarv töötajate kohta puudub, määrake väärtuseks **0**.</span><span class="sxs-lookup"><span data-stu-id="62567-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="62567-168">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-168">Accrual amount</span></span>

<span data-ttu-id="62567-169">Viitvõla summat arvestatakse tundides või päevades, mis kogunevad töötajale perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="62567-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="62567-170">Periood põhineb puhkuse andmise sageduse põhjal.</span><span class="sxs-lookup"><span data-stu-id="62567-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="62567-171">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="62567-171">Minimum balance</span></span>

<span data-ttu-id="62567-172">Kui töötajad võtavad rohkem puhkust välja, kui neile on ette nähtud, võib miinimumsaldole anda negatiivse väärtuse.</span><span class="sxs-lookup"><span data-stu-id="62567-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="62567-173">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="62567-173">Maximum carry-forward</span></span>

<span data-ttu-id="62567-174">Viitvõlgade protsess kohandab puhkusesaldod, mis ületab alguskuupäeva aastapäeva ülekandmise maksimumsaldot.</span><span class="sxs-lookup"><span data-stu-id="62567-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="62567-175">Hüvitise summa</span><span class="sxs-lookup"><span data-stu-id="62567-175">Grant amount</span></span>

<span data-ttu-id="62567-176">Hüvitise summa on tundide või päevade esmane arv, mis töötajale antakse, kui nad esmakordselt registreeruvad puhkuseplaani.</span><span class="sxs-lookup"><span data-stu-id="62567-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="62567-177">See summa ei kogune iga viitvõlaperioodiga.</span><span class="sxs-lookup"><span data-stu-id="62567-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="62567-178">Registreerimised ja saldod</span><span class="sxs-lookup"><span data-stu-id="62567-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="62567-179">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-179">Enrollment date</span></span>

<span data-ttu-id="62567-180">Registreerimise kuupäev määratleb, millal töötaja saaks alustada vaba aja kogumist.</span><span class="sxs-lookup"><span data-stu-id="62567-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="62567-181">Näiteks kui töötaja on liitunud 15. juunil 2018 puhkusekavasse, ei saa tal vaba aega koguneda enne 15. juunit 2018.</span><span class="sxs-lookup"><span data-stu-id="62567-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="62567-182">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="62567-182">Current balance</span></span>

<span data-ttu-id="62567-183">Praegune saldo on puhkuse aja taotluste jaoks saadaolev summa.</span><span class="sxs-lookup"><span data-stu-id="62567-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="62567-184">See summa sisaldab viitvõlgu, kinnitatud taotlusi ja korrigeerimisi kuni praeguse kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="62567-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="62567-185">Praeguse saldo näited</span><span class="sxs-lookup"><span data-stu-id="62567-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="62567-186">Aastaplaan</span><span class="sxs-lookup"><span data-stu-id="62567-186">Annual plan</span></span>

<span data-ttu-id="62567-187">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-187">**Plan setup**</span></span>

| <span data-ttu-id="62567-188">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-188">Plan start date</span></span> | <span data-ttu-id="62567-189">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-189">Enrollment date</span></span> | <span data-ttu-id="62567-190">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-190">Accrual frequency</span></span> | <span data-ttu-id="62567-191">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-191">Accrual period basis</span></span> | <span data-ttu-id="62567-192">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="62567-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-193">1/1/2018</span></span>        | <span data-ttu-id="62567-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-194">1/1/2018</span></span>        | <span data-ttu-id="62567-195">Aastane</span><span class="sxs-lookup"><span data-stu-id="62567-195">Annual</span></span>            | <span data-ttu-id="62567-196">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-196">Plan start date</span></span>      | <span data-ttu-id="62567-197">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="62567-197">End of accrual period</span></span> |

<span data-ttu-id="62567-198">Viitvõlad töödeldakse 01. jaanuaril 2019 (01/01/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="62567-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="62567-199">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-199">**Results**</span></span>

| <span data-ttu-id="62567-200">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-200">Accrual amount</span></span> | <span data-ttu-id="62567-201">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="62567-201">Minimum balance</span></span> | <span data-ttu-id="62567-202">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="62567-202">Maximum carry-forward</span></span> | <span data-ttu-id="62567-203">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="62567-203">Request amount</span></span> | <span data-ttu-id="62567-204">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="62567-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="62567-205">200</span><span class="sxs-lookup"><span data-stu-id="62567-205">200</span></span>            | <span data-ttu-id="62567-206">0</span><span class="sxs-lookup"><span data-stu-id="62567-206">0</span></span>               | <span data-ttu-id="62567-207">120</span><span class="sxs-lookup"><span data-stu-id="62567-207">120</span></span>                   | <span data-ttu-id="62567-208">40</span><span class="sxs-lookup"><span data-stu-id="62567-208">40</span></span>             | <span data-ttu-id="62567-209">160</span><span class="sxs-lookup"><span data-stu-id="62567-209">160</span></span>                              |

<span data-ttu-id="62567-210">Praegune saldo (160) = viitvõla summa (200) – taotluse summa (40)</span><span class="sxs-lookup"><span data-stu-id="62567-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="62567-211">Poole kuu plaan</span><span class="sxs-lookup"><span data-stu-id="62567-211">Semimonthly plan</span></span>

<span data-ttu-id="62567-212">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-212">**Plan setup**</span></span>

| <span data-ttu-id="62567-213">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-213">Plan start date</span></span> | <span data-ttu-id="62567-214">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-214">Enrollment date</span></span> | <span data-ttu-id="62567-215">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-215">Accrual frequency</span></span> | <span data-ttu-id="62567-216">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-216">Accrual period basis</span></span> | <span data-ttu-id="62567-217">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="62567-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-218">1/1/2018</span></span>        | <span data-ttu-id="62567-219">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-219">2/1/2018</span></span>        | <span data-ttu-id="62567-220">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="62567-220">Semimonthly</span></span>       | <span data-ttu-id="62567-221">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-221">Plan start date</span></span>      | <span data-ttu-id="62567-222">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="62567-222">End of accrual period</span></span> |

<span data-ttu-id="62567-223">Viitvõlad töödeldakse 01. mail 2018 (01/05/2018), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="62567-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="62567-224">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-224">**Results**</span></span>

| <span data-ttu-id="62567-225">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-225">Accrual amount</span></span> | <span data-ttu-id="62567-226">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="62567-226">Minimum balance</span></span> | <span data-ttu-id="62567-227">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="62567-227">Maximum carry-forward</span></span> | <span data-ttu-id="62567-228">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="62567-228">Request amount</span></span> | <span data-ttu-id="62567-229">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="62567-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="62567-230">5</span><span class="sxs-lookup"><span data-stu-id="62567-230">5</span></span>              | <span data-ttu-id="62567-231">0</span><span class="sxs-lookup"><span data-stu-id="62567-231">0</span></span>               | <span data-ttu-id="62567-232">120</span><span class="sxs-lookup"><span data-stu-id="62567-232">120</span></span>                   | <span data-ttu-id="62567-233">8</span><span class="sxs-lookup"><span data-stu-id="62567-233">8</span></span>              | <span data-ttu-id="62567-234">22</span><span class="sxs-lookup"><span data-stu-id="62567-234">22</span></span>                               |

<span data-ttu-id="62567-235">Praegune saldo (22) = viitvõla summa (5 × 6) – taotluse summa (8)</span><span class="sxs-lookup"><span data-stu-id="62567-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="62567-236">Kuuplaan</span><span class="sxs-lookup"><span data-stu-id="62567-236">Monthly plan</span></span>

<span data-ttu-id="62567-237">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-237">**Plan setup**</span></span>

| <span data-ttu-id="62567-238">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-238">Plan start date</span></span> | <span data-ttu-id="62567-239">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-239">Enrollment date</span></span> | <span data-ttu-id="62567-240">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-240">Accrual frequency</span></span> | <span data-ttu-id="62567-241">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-241">Accrual period basis</span></span> | <span data-ttu-id="62567-242">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="62567-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-243">1/1/2018</span></span>        | <span data-ttu-id="62567-244">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-244">2/1/2018</span></span>        | <span data-ttu-id="62567-245">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="62567-245">Semimonthly</span></span>       | <span data-ttu-id="62567-246">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-246">Plan start date</span></span>      | <span data-ttu-id="62567-247">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="62567-247">End of accrual period</span></span> |

<span data-ttu-id="62567-248">Viitvõlad töödeldakse 01. mail 2018 (01/05/2018), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="62567-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="62567-249">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-249">**Results**</span></span>

| <span data-ttu-id="62567-250">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-250">Accrual amount</span></span> | <span data-ttu-id="62567-251">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="62567-251">Minimum balance</span></span> | <span data-ttu-id="62567-252">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="62567-252">Maximum carry-forward</span></span> | <span data-ttu-id="62567-253">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="62567-253">Request amount</span></span> | <span data-ttu-id="62567-254">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="62567-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="62567-255">5</span><span class="sxs-lookup"><span data-stu-id="62567-255">5</span></span>              | <span data-ttu-id="62567-256">0</span><span class="sxs-lookup"><span data-stu-id="62567-256">0</span></span>               | <span data-ttu-id="62567-257">120</span><span class="sxs-lookup"><span data-stu-id="62567-257">120</span></span>                   | <span data-ttu-id="62567-258">8</span><span class="sxs-lookup"><span data-stu-id="62567-258">8</span></span>              | <span data-ttu-id="62567-259">7</span><span class="sxs-lookup"><span data-stu-id="62567-259">7</span></span>                                |

<span data-ttu-id="62567-260">Praegune saldo (7) = viitvõla summa (5 × 3) – taotluse summa (8)</span><span class="sxs-lookup"><span data-stu-id="62567-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="62567-261">Prognoositud saldo</span><span class="sxs-lookup"><span data-stu-id="62567-261">Forecasted balance</span></span>

<span data-ttu-id="62567-262">See *eelarvesaldo* on tulevasel kuupäeval saadaolev puhkuse kogus.</span><span class="sxs-lookup"><span data-stu-id="62567-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="62567-263">Viitvõlgade ja ülekandmise korrigeerimised on prognoositud selleks kuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="62567-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="62567-264">Arvutamisel kasutatakse järgmist valemit:</span><span class="sxs-lookup"><span data-stu-id="62567-264">The following formula is used:</span></span>

<span data-ttu-id="62567-265">Esmaspäeva prognoositud saldo = praegune saldo – taotlused + viitvõlad – ülekandmise korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="62567-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="62567-266">Prognoositud saldo näited</span><span class="sxs-lookup"><span data-stu-id="62567-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="62567-267">Aastaplaan</span><span class="sxs-lookup"><span data-stu-id="62567-267">Annual plan</span></span>

<span data-ttu-id="62567-268">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-268">**Plan setup**</span></span>

| <span data-ttu-id="62567-269">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-269">Plan start date</span></span> | <span data-ttu-id="62567-270">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-270">Enrollment date</span></span> | <span data-ttu-id="62567-271">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-271">Accrual frequency</span></span> | <span data-ttu-id="62567-272">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-272">Accrual period basis</span></span> | <span data-ttu-id="62567-273">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="62567-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-274">1/1/2018</span></span>        | <span data-ttu-id="62567-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-275">1/1/2018</span></span>        | <span data-ttu-id="62567-276">Aastane</span><span class="sxs-lookup"><span data-stu-id="62567-276">Annual</span></span>            | <span data-ttu-id="62567-277">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-277">Plan start date</span></span>      | <span data-ttu-id="62567-278">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="62567-278">End of accrual period</span></span> |

<span data-ttu-id="62567-279">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="62567-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="62567-280">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-280">**Results**</span></span>

| <span data-ttu-id="62567-281">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-281">Accrual amount</span></span> | <span data-ttu-id="62567-282">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="62567-282">Minimum balance</span></span> | <span data-ttu-id="62567-283">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="62567-283">Maximum carry-forward</span></span> | <span data-ttu-id="62567-284">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="62567-284">Current balance</span></span> | <span data-ttu-id="62567-285">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="62567-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="62567-286">20</span><span class="sxs-lookup"><span data-stu-id="62567-286">20</span></span>             | <span data-ttu-id="62567-287">0</span><span class="sxs-lookup"><span data-stu-id="62567-287">0</span></span>               | <span data-ttu-id="62567-288">20</span><span class="sxs-lookup"><span data-stu-id="62567-288">20</span></span>                    | <span data-ttu-id="62567-289">40</span><span class="sxs-lookup"><span data-stu-id="62567-289">40</span></span>              | <span data-ttu-id="62567-290">40</span><span class="sxs-lookup"><span data-stu-id="62567-290">40</span></span>                                   |

<span data-ttu-id="62567-291">Prognoositud saldo (40) = juurdekasvu summa (20) – praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="62567-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="62567-292">Poole kuu plaan</span><span class="sxs-lookup"><span data-stu-id="62567-292">Semimonthly plan</span></span>

<span data-ttu-id="62567-293">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-293">**Plan setup**</span></span>

| <span data-ttu-id="62567-294">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-294">Plan start date</span></span> | <span data-ttu-id="62567-295">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-295">Enrollment date</span></span> | <span data-ttu-id="62567-296">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-296">Accrual frequency</span></span> | <span data-ttu-id="62567-297">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-297">Accrual period basis</span></span> | <span data-ttu-id="62567-298">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="62567-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-299">1/1/2018</span></span>        | <span data-ttu-id="62567-300">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-300">2/1/2018</span></span>        | <span data-ttu-id="62567-301">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="62567-301">Semimonthly</span></span>       | <span data-ttu-id="62567-302">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-302">Plan start date</span></span>      | <span data-ttu-id="62567-303">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="62567-303">End of accrual period</span></span> |

<span data-ttu-id="62567-304">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="62567-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="62567-305">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-305">**Results**</span></span>

| <span data-ttu-id="62567-306">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-306">Accrual amount</span></span> | <span data-ttu-id="62567-307">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="62567-307">Minimum balance</span></span> | <span data-ttu-id="62567-308">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="62567-308">Maximum carry-forward</span></span> | <span data-ttu-id="62567-309">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="62567-309">Current balance</span></span> | <span data-ttu-id="62567-310">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="62567-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="62567-311">5</span><span class="sxs-lookup"><span data-stu-id="62567-311">5</span></span>              | <span data-ttu-id="62567-312">0</span><span class="sxs-lookup"><span data-stu-id="62567-312">0</span></span>               | <span data-ttu-id="62567-313">20</span><span class="sxs-lookup"><span data-stu-id="62567-313">20</span></span>                    | <span data-ttu-id="62567-314">40</span><span class="sxs-lookup"><span data-stu-id="62567-314">40</span></span>              | <span data-ttu-id="62567-315">35</span><span class="sxs-lookup"><span data-stu-id="62567-315">35</span></span>                                   |

<span data-ttu-id="62567-316">Prognoositud saldo (35) = juurdekasvu summa (5 × 3) + praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="62567-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="62567-317">Kuuplaan</span><span class="sxs-lookup"><span data-stu-id="62567-317">Monthly plan</span></span>

<span data-ttu-id="62567-318">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-318">**Plan setup**</span></span>

| <span data-ttu-id="62567-319">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-319">Plan start date</span></span> | <span data-ttu-id="62567-320">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-320">Enrollment date</span></span> | <span data-ttu-id="62567-321">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-321">Accrual frequency</span></span> | <span data-ttu-id="62567-322">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-322">Accrual period basis</span></span> | <span data-ttu-id="62567-323">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="62567-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-324">1/1/2018</span></span>        | <span data-ttu-id="62567-325">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-325">2/1/2018</span></span>        | <span data-ttu-id="62567-326">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="62567-326">Semimonthly</span></span>       | <span data-ttu-id="62567-327">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-327">Plan start date</span></span>      | <span data-ttu-id="62567-328">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="62567-328">End of accrual period</span></span> |

<span data-ttu-id="62567-329">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="62567-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="62567-330">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-330">**Results**</span></span>

| <span data-ttu-id="62567-331">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-331">Accrual amount</span></span> | <span data-ttu-id="62567-332">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="62567-332">Minimum balance</span></span> | <span data-ttu-id="62567-333">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="62567-333">Maximum carry-forward</span></span> | <span data-ttu-id="62567-334">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="62567-334">Current balance</span></span> | <span data-ttu-id="62567-335">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="62567-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="62567-336">10</span><span class="sxs-lookup"><span data-stu-id="62567-336">10</span></span>             | <span data-ttu-id="62567-337">0</span><span class="sxs-lookup"><span data-stu-id="62567-337">0</span></span>               | <span data-ttu-id="62567-338">20</span><span class="sxs-lookup"><span data-stu-id="62567-338">20</span></span>                    | <span data-ttu-id="62567-339">40</span><span class="sxs-lookup"><span data-stu-id="62567-339">40</span></span>              | <span data-ttu-id="62567-340">30</span><span class="sxs-lookup"><span data-stu-id="62567-340">30</span></span>                                   |

<span data-ttu-id="62567-341">Prognoositud saldo (30) = juurdekasvu summa (10 × 1) – praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="62567-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="62567-342">Proportsionaalse arvestuse saldo näited</span><span class="sxs-lookup"><span data-stu-id="62567-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="62567-343">Proportsionaalse arvestuse kuuplaan</span><span class="sxs-lookup"><span data-stu-id="62567-343">Prorated monthly plan</span></span>

<span data-ttu-id="62567-344">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-344">**Plan setup**</span></span>

| <span data-ttu-id="62567-345">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-345">Plan start date</span></span> | <span data-ttu-id="62567-346">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-346">Accrual frequency</span></span> | <span data-ttu-id="62567-347">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="62567-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-348">1/1/2018</span></span>        | <span data-ttu-id="62567-349">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="62567-349">Monthly</span></span>           | <span data-ttu-id="62567-350">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-350">Plan start date</span></span>      |

<span data-ttu-id="62567-351">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-351">**Results**</span></span>

| <span data-ttu-id="62567-352">Töötaja</span><span class="sxs-lookup"><span data-stu-id="62567-352">Employee</span></span>            | <span data-ttu-id="62567-353">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="62567-353">Months of service</span></span> | <span data-ttu-id="62567-354">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-354">Enrollment date</span></span> | <span data-ttu-id="62567-355">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-355">Start date</span></span> | <span data-ttu-id="62567-356">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-356">Accrual amount</span></span> | <span data-ttu-id="62567-357">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="62567-357">Process accrual</span></span> | <span data-ttu-id="62567-358">Saldo</span><span class="sxs-lookup"><span data-stu-id="62567-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="62567-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="62567-359">Jeannette Nicholson</span></span> | <span data-ttu-id="62567-360">0,00</span><span class="sxs-lookup"><span data-stu-id="62567-360">0.00</span></span>              | <span data-ttu-id="62567-361">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-361">6/1/2018</span></span>        | <span data-ttu-id="62567-362">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-362">6/1/2018</span></span>   | <span data-ttu-id="62567-363">1,00</span><span class="sxs-lookup"><span data-stu-id="62567-363">1.00</span></span>           | <span data-ttu-id="62567-364">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-364">9/1/2018</span></span>        | <span data-ttu-id="62567-365">3,00</span><span class="sxs-lookup"><span data-stu-id="62567-365">3.00</span></span>    |
| <span data-ttu-id="62567-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="62567-366">Jay Norman</span></span>          | <span data-ttu-id="62567-367">0,00</span><span class="sxs-lookup"><span data-stu-id="62567-367">0.00</span></span>              | <span data-ttu-id="62567-368">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="62567-368">6/15/2018</span></span>       | <span data-ttu-id="62567-369">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="62567-369">6/15/2018</span></span>  | <span data-ttu-id="62567-370">1,00</span><span class="sxs-lookup"><span data-stu-id="62567-370">1.00</span></span>           | <span data-ttu-id="62567-371">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-371">9/1/2018</span></span>        | <span data-ttu-id="62567-372">2,53</span><span class="sxs-lookup"><span data-stu-id="62567-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="62567-373">Täieliku arvestuse kuuplaan</span><span class="sxs-lookup"><span data-stu-id="62567-373">Full accrual monthly plan</span></span>

<span data-ttu-id="62567-374">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-374">**Plan setup**</span></span>

| <span data-ttu-id="62567-375">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-375">Plan start date</span></span> | <span data-ttu-id="62567-376">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-376">Accrual frequency</span></span> | <span data-ttu-id="62567-377">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="62567-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-378">1/1/2018</span></span>        | <span data-ttu-id="62567-379">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="62567-379">Monthly</span></span>           | <span data-ttu-id="62567-380">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-380">Plan start date</span></span>      |

<span data-ttu-id="62567-381">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-381">**Results**</span></span>

| <span data-ttu-id="62567-382">Töötaja</span><span class="sxs-lookup"><span data-stu-id="62567-382">Employee</span></span>            | <span data-ttu-id="62567-383">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="62567-383">Months of service</span></span> | <span data-ttu-id="62567-384">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-384">Enrollment date</span></span> | <span data-ttu-id="62567-385">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-385">Start date</span></span> | <span data-ttu-id="62567-386">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-386">Accrual amount</span></span> | <span data-ttu-id="62567-387">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="62567-387">Process accrual</span></span> | <span data-ttu-id="62567-388">Saldo</span><span class="sxs-lookup"><span data-stu-id="62567-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="62567-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="62567-389">Jeannette Nicholson</span></span> | <span data-ttu-id="62567-390">0,00</span><span class="sxs-lookup"><span data-stu-id="62567-390">0.00</span></span>              | <span data-ttu-id="62567-391">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-391">6/1/2018</span></span>        | <span data-ttu-id="62567-392">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-392">6/1/2018</span></span>   | <span data-ttu-id="62567-393">1,00</span><span class="sxs-lookup"><span data-stu-id="62567-393">1.00</span></span>           | <span data-ttu-id="62567-394">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-394">9/1/2018</span></span>        | <span data-ttu-id="62567-395">3,00</span><span class="sxs-lookup"><span data-stu-id="62567-395">3.00</span></span>    |
| <span data-ttu-id="62567-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="62567-396">Jay Norman</span></span>          | <span data-ttu-id="62567-397">0,00</span><span class="sxs-lookup"><span data-stu-id="62567-397">0.00</span></span>              | <span data-ttu-id="62567-398">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="62567-398">6/15/2018</span></span>       | <span data-ttu-id="62567-399">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="62567-399">6/15/2018</span></span>  | <span data-ttu-id="62567-400">1,00</span><span class="sxs-lookup"><span data-stu-id="62567-400">1.00</span></span>           | <span data-ttu-id="62567-401">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-401">9/1/2018</span></span>        | <span data-ttu-id="62567-402">3,00</span><span class="sxs-lookup"><span data-stu-id="62567-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="62567-403">Arvestuse puudumise kuuplaan</span><span class="sxs-lookup"><span data-stu-id="62567-403">No accrual monthly plan</span></span>

<span data-ttu-id="62567-404">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="62567-404">**Plan setup**</span></span>

| <span data-ttu-id="62567-405">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-405">Plan start date</span></span> | <span data-ttu-id="62567-406">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="62567-406">Accrual frequency</span></span> | <span data-ttu-id="62567-407">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="62567-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="62567-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-408">1/1/2018</span></span>        | <span data-ttu-id="62567-409">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="62567-409">Monthly</span></span>           | <span data-ttu-id="62567-410">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-410">Plan start date</span></span>      |

<span data-ttu-id="62567-411">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="62567-411">**Results**</span></span>

| <span data-ttu-id="62567-412">Töötaja</span><span class="sxs-lookup"><span data-stu-id="62567-412">Employee</span></span>            | <span data-ttu-id="62567-413">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="62567-413">Months of service</span></span> | <span data-ttu-id="62567-414">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-414">Enrollment date</span></span> | <span data-ttu-id="62567-415">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="62567-415">Start date</span></span> | <span data-ttu-id="62567-416">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="62567-416">Accrual amount</span></span> | <span data-ttu-id="62567-417">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="62567-417">Process accrual</span></span> | <span data-ttu-id="62567-418">Saldo</span><span class="sxs-lookup"><span data-stu-id="62567-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="62567-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="62567-419">Jeannette Nicholson</span></span> | <span data-ttu-id="62567-420">0,00</span><span class="sxs-lookup"><span data-stu-id="62567-420">0.00</span></span>              | <span data-ttu-id="62567-421">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-421">6/1/2018</span></span>        | <span data-ttu-id="62567-422">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-422">6/1/2018</span></span>   | <span data-ttu-id="62567-423">1,00</span><span class="sxs-lookup"><span data-stu-id="62567-423">1.00</span></span>           | <span data-ttu-id="62567-424">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-424">9/1/2018</span></span>        | <span data-ttu-id="62567-425">3,00</span><span class="sxs-lookup"><span data-stu-id="62567-425">3.00</span></span>    |
| <span data-ttu-id="62567-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="62567-426">Jay Norman</span></span>          | <span data-ttu-id="62567-427">0,00</span><span class="sxs-lookup"><span data-stu-id="62567-427">0.00</span></span>              | <span data-ttu-id="62567-428">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="62567-428">6/15/2018</span></span>       | <span data-ttu-id="62567-429">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="62567-429">6/15/2018</span></span>  | <span data-ttu-id="62567-430">1,00</span><span class="sxs-lookup"><span data-stu-id="62567-430">1.00</span></span>           | <span data-ttu-id="62567-431">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="62567-431">9/1/2018</span></span>        | <span data-ttu-id="62567-432">2.00</span><span class="sxs-lookup"><span data-stu-id="62567-432">2.00</span></span>    |
