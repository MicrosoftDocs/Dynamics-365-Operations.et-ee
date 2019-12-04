---
title: Puhkuste ja puudumiste põhimõtted
description: Selles teemas kirjeldatakse puhkuste ja puudumiste mõisteid ja kuidas vaba aja saldosid määratletakse.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3dbf5807a213e425b24d5a4809df694393faeb9b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832764"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="a4ecd-103">Puhkuste ja puudumiste põhimõtted</span><span class="sxs-lookup"><span data-stu-id="a4ecd-103">Leave and absence concepts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4ecd-104">Mõistete ja tingimuste abil, mida selles teemas kirjeldatakse, saate määrata, kuidas antakse töötajale töölt vaba aega ja kuidas selle töötaja ajasaldosid arvutada.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="a4ecd-105">Puhkuste ja puudumiste halduse kohta lisateabe saamiseks vt [Puhkuste ja puudumiste haldus](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="a4ecd-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="a4ecd-106">Puhkuseplaani üksikasjad</span><span class="sxs-lookup"><span data-stu-id="a4ecd-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="a4ecd-107">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-107">Start date</span></span>

<span data-ttu-id="a4ecd-108">Alguskuupäev on see kuupäev, mil viitvõlgade töötlus algab.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="a4ecd-109">Alguskuupäev on samas ka edasikantavate summade arvutamiseks kasutatav tähtpäeva kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="a4ecd-110">Viitvõlad</span><span class="sxs-lookup"><span data-stu-id="a4ecd-110">Accruals</span></span>

<span data-ttu-id="a4ecd-111">Viitvõlad määravad, millal ja kui sageli määratakse töötajale vaba aega.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="a4ecd-112">Poliitika selle kohta, millal viitvõlgu määrata, ja poliitika proportsionaalse arvestuse kohta on määratletud jaotises **Viitvõlad** puhkuste ja puudumiste plaani loomisel.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="a4ecd-113">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-113">Accrual frequency</span></span>

<span data-ttu-id="a4ecd-114">Puhkuse andmise sagedus määratleb, kui tihti on puhkus kogunenud või määratud.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="a4ecd-115">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="a4ecd-115">The following options are available:</span></span>

- <span data-ttu-id="a4ecd-116">Kord päevas</span><span class="sxs-lookup"><span data-stu-id="a4ecd-116">Daily</span></span>
- <span data-ttu-id="a4ecd-117">Iganädalane</span><span class="sxs-lookup"><span data-stu-id="a4ecd-117">Weekly</span></span>
- <span data-ttu-id="a4ecd-118">Kaks korda nädalas</span><span class="sxs-lookup"><span data-stu-id="a4ecd-118">Biweekly</span></span>
- <span data-ttu-id="a4ecd-119">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-119">Semimonthly</span></span>
- <span data-ttu-id="a4ecd-120">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-120">Monthly</span></span>
- <span data-ttu-id="a4ecd-121">Kord kvartalis</span><span class="sxs-lookup"><span data-stu-id="a4ecd-121">Quarterly</span></span>
- <span data-ttu-id="a4ecd-122">Poolaasta kohta</span><span class="sxs-lookup"><span data-stu-id="a4ecd-122">Semiannually</span></span>
- <span data-ttu-id="a4ecd-123">Kord aastas</span><span class="sxs-lookup"><span data-stu-id="a4ecd-123">Annually</span></span>
- <span data-ttu-id="a4ecd-124">Pole</span><span class="sxs-lookup"><span data-stu-id="a4ecd-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="a4ecd-125">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-125">Accrual period basis</span></span>

<span data-ttu-id="a4ecd-126">Puhkuseperioodi baas määratleb kuupäeva, mida kasutatakse puhkuseperioodi arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="a4ecd-127">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="a4ecd-127">The following options are available:</span></span>

- <span data-ttu-id="a4ecd-128">**Plaanitav alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-128">**Plan start date**</span></span>
- <span data-ttu-id="a4ecd-129">**Töötajale kindlal kuupäeval** - selle suvandi valimisel määratleb selle väärtus puhkuseperioodide alguskuupäeva allikat.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="a4ecd-130">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="a4ecd-130">The following options are available:</span></span>

    - <span data-ttu-id="a4ecd-131">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="a4ecd-131">Custom</span></span>
    - <span data-ttu-id="a4ecd-132">Tähtpäeva kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-132">Anniversary date</span></span>
    - <span data-ttu-id="a4ecd-133">Värbamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-133">Original hire date</span></span>
    - <span data-ttu-id="a4ecd-134">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="a4ecd-134">Seniority date</span></span>
    - <span data-ttu-id="a4ecd-135">Töötaja töösuhte korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="a4ecd-136">Töötaja töösuhte alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="a4ecd-137">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-137">Accrual award date</span></span>

<span data-ttu-id="a4ecd-138">Puhkuse andmise kuupäev määrab, millal antakse töötajale vaba aega.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="a4ecd-139">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="a4ecd-139">The following options are available:</span></span>

- <span data-ttu-id="a4ecd-140">**Viitvõlgade lõppkuupäev** – töötajale määratakse puhkus puhkuseperioodi viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="a4ecd-141">Õige koguse lisandumisel peab viitvõlgade protsess sisaldama kogu perioodi.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="a4ecd-142">Näiteks puhkuseperiood on 1. jaanuarist 2018 kuni 31. jaanuarini 2018.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="a4ecd-143">Sel juhul, et kaasata jaanuari, käivitatakse viitvõlg 1. veebruaril 2018.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="a4ecd-144">**Viitvõlgade alguskuupäev** – töötajale määratakse puhkus puhkuseperioodi esimesel päeval.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="a4ecd-145">Viitvõlgade poliitika registreerimine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="a4ecd-146">Viitvõlgade poliitika registreerimise määratleb viitvõlgade arvutamise, kui töötaja on liitunud keset puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="a4ecd-147">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="a4ecd-147">The following options are available:</span></span>

- <span data-ttu-id="a4ecd-148">**Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="a4ecd-149">Viitvõlgade töötlemisel rakendatakse seda erinevust.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="a4ecd-150">**Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="a4ecd-151">**Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="a4ecd-152">Viitvõlgade poliitika registreerimise tühistamise kohta</span><span class="sxs-lookup"><span data-stu-id="a4ecd-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="a4ecd-153">Viitvõlgade poliitika registreerimise tühistamise kohta määratleb viitvõlgade arvutamise, kui töötaja on lahkunud keset puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="a4ecd-154">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="a4ecd-154">The following options are available:</span></span>

- <span data-ttu-id="a4ecd-155">**Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="a4ecd-156">Viitvõlgade töötlemisel rakendatakse seda erinevust.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="a4ecd-157">**Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="a4ecd-158">**Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="a4ecd-159">Viitvõlgade skeemid</span><span class="sxs-lookup"><span data-stu-id="a4ecd-159">Accrual schedule</span></span>

<span data-ttu-id="a4ecd-160">Viitvõlgade graafik määrab, kuidas töötaja puhkuse aeg koguneb ja millised summad antud töötajal kogunevad ja edasi kanduvad.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="a4ecd-161">Järkusid saab luua nii, et vaba aega premeeritakse erinevate tasemete alusel.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="a4ecd-162">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="a4ecd-162">Months of service</span></span>

<span data-ttu-id="a4ecd-163">Jaotise **Töötatud kuud** väärtus määratleb kuude miinimumarvu, kui palju töötaja peab töötama, et tal oleks õigus viitvõlgadele.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="a4ecd-164">Kui miinimuumarv töötajate kohta puudub, määrake väärtuseks **0**.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="a4ecd-165">Töötunnid</span><span class="sxs-lookup"><span data-stu-id="a4ecd-165">Hours worked</span></span>

<span data-ttu-id="a4ecd-166">Jaotise **Töötunnid** väärtus määratleb tundide miinimumarvu, kui palju töötaja peab puhkuseperioodi kohta töötama, et tal oleks õigus viitvõlgadele.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="a4ecd-167">Kui miinimuumarv töötajate kohta puudub, määrake väärtuseks **0**.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="a4ecd-168">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-168">Accrual amount</span></span>

<span data-ttu-id="a4ecd-169">Viitvõla summat arvestatakse tundides või päevades, mis kogunevad töötajale perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="a4ecd-170">Periood põhineb puhkuse andmise sageduse põhjal.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="a4ecd-171">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-171">Minimum balance</span></span>

<span data-ttu-id="a4ecd-172">Kui töötajad võtavad rohkem puhkust välja, kui neile on ette nähtud, võib miinimumsaldole anda negatiivse väärtuse.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="a4ecd-173">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-173">Maximum carry-forward</span></span>

<span data-ttu-id="a4ecd-174">Viitvõlgade protsess kohandab puhkusesaldod, mis ületab alguskuupäeva aastapäeva ülekandmise maksimumsaldot.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="a4ecd-175">Hüvitise summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-175">Grant amount</span></span>

<span data-ttu-id="a4ecd-176">Hüvitise summa on tundide või päevade esmane arv, mis töötajale antakse, kui nad esmakordselt registreeruvad puhkuseplaani.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="a4ecd-177">See summa ei kogune iga viitvõlaperioodiga.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="a4ecd-178">Registreerimised ja saldod</span><span class="sxs-lookup"><span data-stu-id="a4ecd-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="a4ecd-179">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-179">Enrollment date</span></span>

<span data-ttu-id="a4ecd-180">Registreerimise kuupäev määratleb, millal töötaja saaks alustada vaba aja kogumist.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="a4ecd-181">Näiteks kui töötaja on liitunud 15. juunil 2018 puhkusekavasse, ei saa tal vaba aega koguneda enne 15. juunit 2018.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="a4ecd-182">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-182">Current balance</span></span>

<span data-ttu-id="a4ecd-183">Praegune saldo on puhkuse aja taotluste jaoks saadaolev summa.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="a4ecd-184">See summa sisaldab viitvõlgu, kinnitatud taotlusi ja korrigeerimisi kuni praeguse kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="a4ecd-185">Praeguse saldo näited</span><span class="sxs-lookup"><span data-stu-id="a4ecd-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="a4ecd-186">Aastaplaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-186">Annual plan</span></span>

<span data-ttu-id="a4ecd-187">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-187">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-188">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-188">Plan start date</span></span> | <span data-ttu-id="a4ecd-189">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-189">Enrollment date</span></span> | <span data-ttu-id="a4ecd-190">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-190">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-191">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-191">Accrual period basis</span></span> | <span data-ttu-id="a4ecd-192">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a4ecd-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-193">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-194">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-195">Aastane</span><span class="sxs-lookup"><span data-stu-id="a4ecd-195">Annual</span></span>            | <span data-ttu-id="a4ecd-196">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-196">Plan start date</span></span>      | <span data-ttu-id="a4ecd-197">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="a4ecd-197">End of accrual period</span></span> |

<span data-ttu-id="a4ecd-198">Viitvõlad töödeldakse 01. jaanuaril 2019 (01/01/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="a4ecd-199">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-199">**Results**</span></span>

| <span data-ttu-id="a4ecd-200">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-200">Accrual amount</span></span> | <span data-ttu-id="a4ecd-201">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-201">Minimum balance</span></span> | <span data-ttu-id="a4ecd-202">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-202">Maximum carry-forward</span></span> | <span data-ttu-id="a4ecd-203">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-203">Request amount</span></span> | <span data-ttu-id="a4ecd-204">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="a4ecd-205">200</span><span class="sxs-lookup"><span data-stu-id="a4ecd-205">200</span></span>            | <span data-ttu-id="a4ecd-206">0</span><span class="sxs-lookup"><span data-stu-id="a4ecd-206">0</span></span>               | <span data-ttu-id="a4ecd-207">120</span><span class="sxs-lookup"><span data-stu-id="a4ecd-207">120</span></span>                   | <span data-ttu-id="a4ecd-208">40</span><span class="sxs-lookup"><span data-stu-id="a4ecd-208">40</span></span>             | <span data-ttu-id="a4ecd-209">160</span><span class="sxs-lookup"><span data-stu-id="a4ecd-209">160</span></span>                              |

<span data-ttu-id="a4ecd-210">Praegune saldo (160) = viitvõla summa (200) – taotluse summa (40)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="a4ecd-211">Poole kuu plaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-211">Semimonthly plan</span></span>

<span data-ttu-id="a4ecd-212">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-212">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-213">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-213">Plan start date</span></span> | <span data-ttu-id="a4ecd-214">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-214">Enrollment date</span></span> | <span data-ttu-id="a4ecd-215">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-215">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-216">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-216">Accrual period basis</span></span> | <span data-ttu-id="a4ecd-217">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a4ecd-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-218">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-219">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-219">2/1/2018</span></span>        | <span data-ttu-id="a4ecd-220">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-220">Semimonthly</span></span>       | <span data-ttu-id="a4ecd-221">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-221">Plan start date</span></span>      | <span data-ttu-id="a4ecd-222">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="a4ecd-222">End of accrual period</span></span> |

<span data-ttu-id="a4ecd-223">Viitvõlad töödeldakse 01. mail 2018 (01/05/2018), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="a4ecd-224">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-224">**Results**</span></span>

| <span data-ttu-id="a4ecd-225">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-225">Accrual amount</span></span> | <span data-ttu-id="a4ecd-226">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-226">Minimum balance</span></span> | <span data-ttu-id="a4ecd-227">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-227">Maximum carry-forward</span></span> | <span data-ttu-id="a4ecd-228">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-228">Request amount</span></span> | <span data-ttu-id="a4ecd-229">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="a4ecd-230">5</span><span class="sxs-lookup"><span data-stu-id="a4ecd-230">5</span></span>              | <span data-ttu-id="a4ecd-231">0</span><span class="sxs-lookup"><span data-stu-id="a4ecd-231">0</span></span>               | <span data-ttu-id="a4ecd-232">120</span><span class="sxs-lookup"><span data-stu-id="a4ecd-232">120</span></span>                   | <span data-ttu-id="a4ecd-233">8</span><span class="sxs-lookup"><span data-stu-id="a4ecd-233">8</span></span>              | <span data-ttu-id="a4ecd-234">22</span><span class="sxs-lookup"><span data-stu-id="a4ecd-234">22</span></span>                               |

<span data-ttu-id="a4ecd-235">Praegune saldo (22) = viitvõla summa (5 × 6) – taotluse summa (8)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="a4ecd-236">Kuuplaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-236">Monthly plan</span></span>

<span data-ttu-id="a4ecd-237">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-237">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-238">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-238">Plan start date</span></span> | <span data-ttu-id="a4ecd-239">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-239">Enrollment date</span></span> | <span data-ttu-id="a4ecd-240">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-240">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-241">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-241">Accrual period basis</span></span> | <span data-ttu-id="a4ecd-242">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a4ecd-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-243">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-244">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-244">2/1/2018</span></span>        | <span data-ttu-id="a4ecd-245">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-245">Semimonthly</span></span>       | <span data-ttu-id="a4ecd-246">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-246">Plan start date</span></span>      | <span data-ttu-id="a4ecd-247">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="a4ecd-247">End of accrual period</span></span> |

<span data-ttu-id="a4ecd-248">Viitvõlad töödeldakse 01. mail 2018 (01/05/2018), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="a4ecd-249">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-249">**Results**</span></span>

| <span data-ttu-id="a4ecd-250">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-250">Accrual amount</span></span> | <span data-ttu-id="a4ecd-251">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-251">Minimum balance</span></span> | <span data-ttu-id="a4ecd-252">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-252">Maximum carry-forward</span></span> | <span data-ttu-id="a4ecd-253">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-253">Request amount</span></span> | <span data-ttu-id="a4ecd-254">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="a4ecd-255">5</span><span class="sxs-lookup"><span data-stu-id="a4ecd-255">5</span></span>              | <span data-ttu-id="a4ecd-256">0</span><span class="sxs-lookup"><span data-stu-id="a4ecd-256">0</span></span>               | <span data-ttu-id="a4ecd-257">120</span><span class="sxs-lookup"><span data-stu-id="a4ecd-257">120</span></span>                   | <span data-ttu-id="a4ecd-258">8</span><span class="sxs-lookup"><span data-stu-id="a4ecd-258">8</span></span>              | <span data-ttu-id="a4ecd-259">7</span><span class="sxs-lookup"><span data-stu-id="a4ecd-259">7</span></span>                                |

<span data-ttu-id="a4ecd-260">Praegune saldo (7) = viitvõla summa (5 × 3) – taotluse summa (8)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="a4ecd-261">Prognoositud saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-261">Forecasted balance</span></span>

<span data-ttu-id="a4ecd-262">See *eelarvesaldo* on tulevasel kuupäeval saadaolev puhkuse kogus.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="a4ecd-263">Viitvõlgade ja ülekandmise korrigeerimised on prognoositud selleks kuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="a4ecd-264">Arvutamisel kasutatakse järgmist valemit:</span><span class="sxs-lookup"><span data-stu-id="a4ecd-264">The following formula is used:</span></span>

<span data-ttu-id="a4ecd-265">Esmaspäeva prognoositud saldo = praegune saldo – taotlused + viitvõlad – ülekandmise korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="a4ecd-266">Prognoositud saldo näited</span><span class="sxs-lookup"><span data-stu-id="a4ecd-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="a4ecd-267">Aastaplaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-267">Annual plan</span></span>

<span data-ttu-id="a4ecd-268">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-268">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-269">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-269">Plan start date</span></span> | <span data-ttu-id="a4ecd-270">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-270">Enrollment date</span></span> | <span data-ttu-id="a4ecd-271">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-271">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-272">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-272">Accrual period basis</span></span> | <span data-ttu-id="a4ecd-273">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a4ecd-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-274">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-275">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-276">Aastane</span><span class="sxs-lookup"><span data-stu-id="a4ecd-276">Annual</span></span>            | <span data-ttu-id="a4ecd-277">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-277">Plan start date</span></span>      | <span data-ttu-id="a4ecd-278">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="a4ecd-278">End of accrual period</span></span> |

<span data-ttu-id="a4ecd-279">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="a4ecd-280">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-280">**Results**</span></span>

| <span data-ttu-id="a4ecd-281">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-281">Accrual amount</span></span> | <span data-ttu-id="a4ecd-282">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-282">Minimum balance</span></span> | <span data-ttu-id="a4ecd-283">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-283">Maximum carry-forward</span></span> | <span data-ttu-id="a4ecd-284">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-284">Current balance</span></span> | <span data-ttu-id="a4ecd-285">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="a4ecd-286">20</span><span class="sxs-lookup"><span data-stu-id="a4ecd-286">20</span></span>             | <span data-ttu-id="a4ecd-287">0</span><span class="sxs-lookup"><span data-stu-id="a4ecd-287">0</span></span>               | <span data-ttu-id="a4ecd-288">20</span><span class="sxs-lookup"><span data-stu-id="a4ecd-288">20</span></span>                    | <span data-ttu-id="a4ecd-289">40</span><span class="sxs-lookup"><span data-stu-id="a4ecd-289">40</span></span>              | <span data-ttu-id="a4ecd-290">40</span><span class="sxs-lookup"><span data-stu-id="a4ecd-290">40</span></span>                                   |

<span data-ttu-id="a4ecd-291">Prognoositud saldo (40) = juurdekasvu summa (20) – praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="a4ecd-292">Poole kuu plaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-292">Semimonthly plan</span></span>

<span data-ttu-id="a4ecd-293">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-293">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-294">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-294">Plan start date</span></span> | <span data-ttu-id="a4ecd-295">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-295">Enrollment date</span></span> | <span data-ttu-id="a4ecd-296">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-296">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-297">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-297">Accrual period basis</span></span> | <span data-ttu-id="a4ecd-298">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a4ecd-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-299">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-300">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-300">2/1/2018</span></span>        | <span data-ttu-id="a4ecd-301">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-301">Semimonthly</span></span>       | <span data-ttu-id="a4ecd-302">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-302">Plan start date</span></span>      | <span data-ttu-id="a4ecd-303">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="a4ecd-303">End of accrual period</span></span> |

<span data-ttu-id="a4ecd-304">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="a4ecd-305">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-305">**Results**</span></span>

| <span data-ttu-id="a4ecd-306">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-306">Accrual amount</span></span> | <span data-ttu-id="a4ecd-307">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-307">Minimum balance</span></span> | <span data-ttu-id="a4ecd-308">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-308">Maximum carry-forward</span></span> | <span data-ttu-id="a4ecd-309">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-309">Current balance</span></span> | <span data-ttu-id="a4ecd-310">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="a4ecd-311">5</span><span class="sxs-lookup"><span data-stu-id="a4ecd-311">5</span></span>              | <span data-ttu-id="a4ecd-312">0</span><span class="sxs-lookup"><span data-stu-id="a4ecd-312">0</span></span>               | <span data-ttu-id="a4ecd-313">20</span><span class="sxs-lookup"><span data-stu-id="a4ecd-313">20</span></span>                    | <span data-ttu-id="a4ecd-314">40</span><span class="sxs-lookup"><span data-stu-id="a4ecd-314">40</span></span>              | <span data-ttu-id="a4ecd-315">35</span><span class="sxs-lookup"><span data-stu-id="a4ecd-315">35</span></span>                                   |

<span data-ttu-id="a4ecd-316">Prognoositud saldo (35) = juurdekasvu summa (5 × 3) + praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="a4ecd-317">Kuuplaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-317">Monthly plan</span></span>

<span data-ttu-id="a4ecd-318">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-318">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-319">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-319">Plan start date</span></span> | <span data-ttu-id="a4ecd-320">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-320">Enrollment date</span></span> | <span data-ttu-id="a4ecd-321">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-321">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-322">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-322">Accrual period basis</span></span> | <span data-ttu-id="a4ecd-323">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a4ecd-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-324">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-325">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-325">2/1/2018</span></span>        | <span data-ttu-id="a4ecd-326">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-326">Semimonthly</span></span>       | <span data-ttu-id="a4ecd-327">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-327">Plan start date</span></span>      | <span data-ttu-id="a4ecd-328">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="a4ecd-328">End of accrual period</span></span> |

<span data-ttu-id="a4ecd-329">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="a4ecd-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="a4ecd-330">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-330">**Results**</span></span>

| <span data-ttu-id="a4ecd-331">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-331">Accrual amount</span></span> | <span data-ttu-id="a4ecd-332">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-332">Minimum balance</span></span> | <span data-ttu-id="a4ecd-333">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="a4ecd-333">Maximum carry-forward</span></span> | <span data-ttu-id="a4ecd-334">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-334">Current balance</span></span> | <span data-ttu-id="a4ecd-335">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="a4ecd-336">10</span><span class="sxs-lookup"><span data-stu-id="a4ecd-336">10</span></span>             | <span data-ttu-id="a4ecd-337">0</span><span class="sxs-lookup"><span data-stu-id="a4ecd-337">0</span></span>               | <span data-ttu-id="a4ecd-338">20</span><span class="sxs-lookup"><span data-stu-id="a4ecd-338">20</span></span>                    | <span data-ttu-id="a4ecd-339">40</span><span class="sxs-lookup"><span data-stu-id="a4ecd-339">40</span></span>              | <span data-ttu-id="a4ecd-340">30</span><span class="sxs-lookup"><span data-stu-id="a4ecd-340">30</span></span>                                   |

<span data-ttu-id="a4ecd-341">Prognoositud saldo (30) = juurdekasvu summa (10 × 1) – praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="a4ecd-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="a4ecd-342">Proportsionaalse arvestuse saldo näited</span><span class="sxs-lookup"><span data-stu-id="a4ecd-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="a4ecd-343">Proportsionaalse arvestuse kuuplaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-343">Prorated monthly plan</span></span>

<span data-ttu-id="a4ecd-344">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-344">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-345">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-345">Plan start date</span></span> | <span data-ttu-id="a4ecd-346">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-346">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-347">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="a4ecd-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-348">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-349">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-349">Monthly</span></span>           | <span data-ttu-id="a4ecd-350">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-350">Plan start date</span></span>      |

<span data-ttu-id="a4ecd-351">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-351">**Results**</span></span>

| <span data-ttu-id="a4ecd-352">Töötaja</span><span class="sxs-lookup"><span data-stu-id="a4ecd-352">Employee</span></span>            | <span data-ttu-id="a4ecd-353">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="a4ecd-353">Months of service</span></span> | <span data-ttu-id="a4ecd-354">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-354">Enrollment date</span></span> | <span data-ttu-id="a4ecd-355">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-355">Start date</span></span> | <span data-ttu-id="a4ecd-356">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-356">Accrual amount</span></span> | <span data-ttu-id="a4ecd-357">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="a4ecd-357">Process accrual</span></span> | <span data-ttu-id="a4ecd-358">Saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="a4ecd-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="a4ecd-359">Jeannette Nicholson</span></span> | <span data-ttu-id="a4ecd-360">0,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-360">0.00</span></span>              | <span data-ttu-id="a4ecd-361">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-361">6/1/2018</span></span>        | <span data-ttu-id="a4ecd-362">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-362">6/1/2018</span></span>   | <span data-ttu-id="a4ecd-363">1,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-363">1.00</span></span>           | <span data-ttu-id="a4ecd-364">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-364">9/1/2018</span></span>        | <span data-ttu-id="a4ecd-365">3,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-365">3.00</span></span>    |
| <span data-ttu-id="a4ecd-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="a4ecd-366">Jay Norman</span></span>          | <span data-ttu-id="a4ecd-367">0,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-367">0.00</span></span>              | <span data-ttu-id="a4ecd-368">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-368">6/15/2018</span></span>       | <span data-ttu-id="a4ecd-369">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-369">6/15/2018</span></span>  | <span data-ttu-id="a4ecd-370">1,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-370">1.00</span></span>           | <span data-ttu-id="a4ecd-371">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-371">9/1/2018</span></span>        | <span data-ttu-id="a4ecd-372">2,53</span><span class="sxs-lookup"><span data-stu-id="a4ecd-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="a4ecd-373">Täieliku arvestuse kuuplaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-373">Full accrual monthly plan</span></span>

<span data-ttu-id="a4ecd-374">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-374">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-375">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-375">Plan start date</span></span> | <span data-ttu-id="a4ecd-376">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-376">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-377">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="a4ecd-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-378">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-379">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-379">Monthly</span></span>           | <span data-ttu-id="a4ecd-380">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-380">Plan start date</span></span>      |

<span data-ttu-id="a4ecd-381">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-381">**Results**</span></span>

| <span data-ttu-id="a4ecd-382">Töötaja</span><span class="sxs-lookup"><span data-stu-id="a4ecd-382">Employee</span></span>            | <span data-ttu-id="a4ecd-383">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="a4ecd-383">Months of service</span></span> | <span data-ttu-id="a4ecd-384">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-384">Enrollment date</span></span> | <span data-ttu-id="a4ecd-385">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-385">Start date</span></span> | <span data-ttu-id="a4ecd-386">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-386">Accrual amount</span></span> | <span data-ttu-id="a4ecd-387">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="a4ecd-387">Process accrual</span></span> | <span data-ttu-id="a4ecd-388">Saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="a4ecd-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="a4ecd-389">Jeannette Nicholson</span></span> | <span data-ttu-id="a4ecd-390">0,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-390">0.00</span></span>              | <span data-ttu-id="a4ecd-391">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-391">6/1/2018</span></span>        | <span data-ttu-id="a4ecd-392">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-392">6/1/2018</span></span>   | <span data-ttu-id="a4ecd-393">1,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-393">1.00</span></span>           | <span data-ttu-id="a4ecd-394">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-394">9/1/2018</span></span>        | <span data-ttu-id="a4ecd-395">3,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-395">3.00</span></span>    |
| <span data-ttu-id="a4ecd-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="a4ecd-396">Jay Norman</span></span>          | <span data-ttu-id="a4ecd-397">0,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-397">0.00</span></span>              | <span data-ttu-id="a4ecd-398">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-398">6/15/2018</span></span>       | <span data-ttu-id="a4ecd-399">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-399">6/15/2018</span></span>  | <span data-ttu-id="a4ecd-400">1,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-400">1.00</span></span>           | <span data-ttu-id="a4ecd-401">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-401">9/1/2018</span></span>        | <span data-ttu-id="a4ecd-402">3,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="a4ecd-403">Arvestuse puudumise kuuplaan</span><span class="sxs-lookup"><span data-stu-id="a4ecd-403">No accrual monthly plan</span></span>

<span data-ttu-id="a4ecd-404">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-404">**Plan setup**</span></span>

| <span data-ttu-id="a4ecd-405">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-405">Plan start date</span></span> | <span data-ttu-id="a4ecd-406">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-406">Accrual frequency</span></span> | <span data-ttu-id="a4ecd-407">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="a4ecd-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-408">1/1/2018</span></span>        | <span data-ttu-id="a4ecd-409">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="a4ecd-409">Monthly</span></span>           | <span data-ttu-id="a4ecd-410">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-410">Plan start date</span></span>      |

<span data-ttu-id="a4ecd-411">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="a4ecd-411">**Results**</span></span>

| <span data-ttu-id="a4ecd-412">Töötaja</span><span class="sxs-lookup"><span data-stu-id="a4ecd-412">Employee</span></span>            | <span data-ttu-id="a4ecd-413">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="a4ecd-413">Months of service</span></span> | <span data-ttu-id="a4ecd-414">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-414">Enrollment date</span></span> | <span data-ttu-id="a4ecd-415">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a4ecd-415">Start date</span></span> | <span data-ttu-id="a4ecd-416">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="a4ecd-416">Accrual amount</span></span> | <span data-ttu-id="a4ecd-417">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="a4ecd-417">Process accrual</span></span> | <span data-ttu-id="a4ecd-418">Saldo</span><span class="sxs-lookup"><span data-stu-id="a4ecd-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="a4ecd-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="a4ecd-419">Jeannette Nicholson</span></span> | <span data-ttu-id="a4ecd-420">0,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-420">0.00</span></span>              | <span data-ttu-id="a4ecd-421">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-421">6/1/2018</span></span>        | <span data-ttu-id="a4ecd-422">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-422">6/1/2018</span></span>   | <span data-ttu-id="a4ecd-423">1,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-423">1.00</span></span>           | <span data-ttu-id="a4ecd-424">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-424">9/1/2018</span></span>        | <span data-ttu-id="a4ecd-425">3,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-425">3.00</span></span>    |
| <span data-ttu-id="a4ecd-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="a4ecd-426">Jay Norman</span></span>          | <span data-ttu-id="a4ecd-427">0,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-427">0.00</span></span>              | <span data-ttu-id="a4ecd-428">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-428">6/15/2018</span></span>       | <span data-ttu-id="a4ecd-429">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-429">6/15/2018</span></span>  | <span data-ttu-id="a4ecd-430">1,00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-430">1.00</span></span>           | <span data-ttu-id="a4ecd-431">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="a4ecd-431">9/1/2018</span></span>        | <span data-ttu-id="a4ecd-432">2.00</span><span class="sxs-lookup"><span data-stu-id="a4ecd-432">2.00</span></span>    |
