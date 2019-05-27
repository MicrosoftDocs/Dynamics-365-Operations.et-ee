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
ms.openlocfilehash: 96e3aa74e513a2421b04bac049400cf71042e2c8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517788"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="1ed1d-103">Puhkuste ja puudumiste põhimõtted</span><span class="sxs-lookup"><span data-stu-id="1ed1d-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1ed1d-104">Mõistete ja tingimuste abil, mida selles teemas kirjeldatakse, saate määrata, kuidas antakse töötajale töölt vaba aega ja kuidas selle töötaja ajasaldosid arvutada.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="1ed1d-105">Puhkuste ja puudumiste halduse kohta lisateabe saamiseks vt [Puhkuste ja puudumiste haldus](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="1ed1d-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="1ed1d-106">Puhkuseplaani üksikasjad</span><span class="sxs-lookup"><span data-stu-id="1ed1d-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="1ed1d-107">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-107">Start date</span></span>

<span data-ttu-id="1ed1d-108">Alguskuupäev on see kuupäev, mil viitvõlgade töötlus algab.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="1ed1d-109">Alguskuupäev on samas ka edasikantavate summade arvutamiseks kasutatav tähtpäeva kuupäev.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="1ed1d-110">Viitvõlad</span><span class="sxs-lookup"><span data-stu-id="1ed1d-110">Accruals</span></span>

<span data-ttu-id="1ed1d-111">Viitvõlad määravad, millal ja kui sageli määratakse töötajale vaba aega.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="1ed1d-112">Poliitika selle kohta, millal viitvõlgu määrata, ja poliitika proportsionaalse arvestuse kohta on määratletud jaotises **Viitvõlad** puhkuste ja puudumiste plaani loomisel.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="1ed1d-113">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-113">Accrual frequency</span></span>

<span data-ttu-id="1ed1d-114">Puhkuse andmise sagedus määratleb, kui tihti on puhkus kogunenud või määratud.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="1ed1d-115">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="1ed1d-115">The following options are available:</span></span>

- <span data-ttu-id="1ed1d-116">Kord päevas</span><span class="sxs-lookup"><span data-stu-id="1ed1d-116">Daily</span></span>
- <span data-ttu-id="1ed1d-117">Iganädalane</span><span class="sxs-lookup"><span data-stu-id="1ed1d-117">Weekly</span></span>
- <span data-ttu-id="1ed1d-118">Kaks korda nädalas</span><span class="sxs-lookup"><span data-stu-id="1ed1d-118">Biweekly</span></span>
- <span data-ttu-id="1ed1d-119">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-119">Semimonthly</span></span>
- <span data-ttu-id="1ed1d-120">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-120">Monthly</span></span>
- <span data-ttu-id="1ed1d-121">Kord kvartalis</span><span class="sxs-lookup"><span data-stu-id="1ed1d-121">Quarterly</span></span>
- <span data-ttu-id="1ed1d-122">Poolaasta kohta</span><span class="sxs-lookup"><span data-stu-id="1ed1d-122">Semiannually</span></span>
- <span data-ttu-id="1ed1d-123">Kord aastas</span><span class="sxs-lookup"><span data-stu-id="1ed1d-123">Annually</span></span>
- <span data-ttu-id="1ed1d-124">Pole</span><span class="sxs-lookup"><span data-stu-id="1ed1d-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="1ed1d-125">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-125">Accrual period basis</span></span>

<span data-ttu-id="1ed1d-126">Puhkuseperioodi baas määratleb kuupäeva, mida kasutatakse puhkuseperioodi arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="1ed1d-127">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="1ed1d-127">The following options are available:</span></span>

- <span data-ttu-id="1ed1d-128">**Plaanitav alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-128">**Plan start date**</span></span>
- <span data-ttu-id="1ed1d-129">**Töötajale kindlal kuupäeval** - selle suvandi valimisel määratleb selle väärtus puhkuseperioodide alguskuupäeva allikat.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="1ed1d-130">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="1ed1d-130">The following options are available:</span></span>

    - <span data-ttu-id="1ed1d-131">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="1ed1d-131">Custom</span></span>
    - <span data-ttu-id="1ed1d-132">Tähtpäeva kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-132">Anniversary date</span></span>
    - <span data-ttu-id="1ed1d-133">Värbamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-133">Original hire date</span></span>
    - <span data-ttu-id="1ed1d-134">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="1ed1d-134">Seniority date</span></span>
    - <span data-ttu-id="1ed1d-135">Töötaja töösuhte korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="1ed1d-136">Töötaja töösuhte alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="1ed1d-137">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-137">Accrual award date</span></span>

<span data-ttu-id="1ed1d-138">Puhkuse andmise kuupäev määrab, millal antakse töötajale vaba aega.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="1ed1d-139">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="1ed1d-139">The following options are available:</span></span>

- <span data-ttu-id="1ed1d-140">**Viitvõlgade lõppkuupäev** – töötajale määratakse puhkus puhkuseperioodi viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="1ed1d-141">Õige koguse lisandumisel peab viitvõlgade protsess sisaldama kogu perioodi.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="1ed1d-142">Näiteks puhkuseperiood on 1. jaanuarist 2018 kuni 31. jaanuarini 2018.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="1ed1d-143">Sel juhul, et kaasata jaanuari, käivitatakse viitvõlg 1. veebruaril 2018.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="1ed1d-144">**Viitvõlgade alguskuupäev** – töötajale määratakse puhkus puhkuseperioodi esimesel päeval.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="1ed1d-145">Viitvõlgade poliitika registreerimine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="1ed1d-146">Viitvõlgade poliitika registreerimise määratleb viitvõlgade arvutamise, kui töötaja on liitunud keset puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="1ed1d-147">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="1ed1d-147">The following options are available:</span></span>

- <span data-ttu-id="1ed1d-148">**Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="1ed1d-149">Viitvõlgade töötlemisel rakendatakse seda erinevust.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="1ed1d-150">**Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="1ed1d-151">**Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="1ed1d-152">Viitvõlgade poliitika registreerimise tühistamise kohta</span><span class="sxs-lookup"><span data-stu-id="1ed1d-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="1ed1d-153">Viitvõlgade poliitika registreerimise tühistamise kohta määratleb viitvõlgade arvutamise, kui töötaja on lahkunud keset puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="1ed1d-154">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="1ed1d-154">The following options are available:</span></span>

- <span data-ttu-id="1ed1d-155">**Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="1ed1d-156">Viitvõlgade töötlemisel rakendatakse seda erinevust.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="1ed1d-157">**Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="1ed1d-158">**Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="1ed1d-159">Viitvõlgade skeemid</span><span class="sxs-lookup"><span data-stu-id="1ed1d-159">Accrual schedule</span></span>

<span data-ttu-id="1ed1d-160">Viitvõlgade graafik määrab, kuidas töötaja puhkuse aeg koguneb ja millised summad antud töötajal kogunevad ja edasi kanduvad.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="1ed1d-161">Järkusid saab luua nii, et vaba aega premeeritakse erinevate tasemete alusel.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="1ed1d-162">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="1ed1d-162">Months of service</span></span>

<span data-ttu-id="1ed1d-163">Jaotise **Töötatud kuud** väärtus määratleb kuude miinimumarvu, kui palju töötaja peab töötama, et tal oleks õigus viitvõlgadele.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="1ed1d-164">Kui miinimuumarv töötajate kohta puudub, määrake väärtuseks **0**.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="1ed1d-165">Töötunnid</span><span class="sxs-lookup"><span data-stu-id="1ed1d-165">Hours worked</span></span>

<span data-ttu-id="1ed1d-166">Jaotise **Töötunnid** väärtus määratleb tundide miinimumarvu, kui palju töötaja peab puhkuseperioodi kohta töötama, et tal oleks õigus viitvõlgadele.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="1ed1d-167">Kui miinimuumarv töötajate kohta puudub, määrake väärtuseks **0**.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="1ed1d-168">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-168">Accrual amount</span></span>

<span data-ttu-id="1ed1d-169">Viitvõla summat arvestatakse tundides või päevades, mis kogunevad töötajale perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="1ed1d-170">Periood põhineb puhkuse andmise sageduse põhjal.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="1ed1d-171">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-171">Minimum balance</span></span>

<span data-ttu-id="1ed1d-172">Kui töötajad võtavad rohkem puhkust välja, kui neile on ette nähtud, võib miinimumsaldole anda negatiivse väärtuse.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="1ed1d-173">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-173">Maximum carry-forward</span></span>

<span data-ttu-id="1ed1d-174">Viitvõlgade protsess kohandab puhkusesaldod, mis ületab alguskuupäeva aastapäeva ülekandmise maksimumsaldot.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="1ed1d-175">Hüvitise summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-175">Grant amount</span></span>

<span data-ttu-id="1ed1d-176">Hüvitise summa on tundide või päevade esmane arv, mis töötajale antakse, kui nad esmakordselt registreeruvad puhkuseplaani.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="1ed1d-177">See summa ei kogune iga viitvõlaperioodiga.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="1ed1d-178">Registreerimised ja saldod</span><span class="sxs-lookup"><span data-stu-id="1ed1d-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="1ed1d-179">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-179">Enrollment date</span></span>

<span data-ttu-id="1ed1d-180">Registreerimise kuupäev määratleb, millal töötaja saaks alustada vaba aja kogumist.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="1ed1d-181">Näiteks kui töötaja on liitunud 15. juunil 2018 puhkusekavasse, ei saa tal vaba aega koguneda enne 15. juunit 2018.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="1ed1d-182">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-182">Current balance</span></span>

<span data-ttu-id="1ed1d-183">Praegune saldo on puhkuse aja taotluste jaoks saadaolev summa.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="1ed1d-184">See summa sisaldab viitvõlgu, kinnitatud taotlusi ja korrigeerimisi kuni praeguse kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="1ed1d-185">Praeguse saldo näited</span><span class="sxs-lookup"><span data-stu-id="1ed1d-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="1ed1d-186">Aastaplaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-186">Annual plan</span></span>

<span data-ttu-id="1ed1d-187">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-187">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-188">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-188">Plan start date</span></span> | <span data-ttu-id="1ed1d-189">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-189">Enrollment date</span></span> | <span data-ttu-id="1ed1d-190">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-190">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-191">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-191">Accrual period basis</span></span> | <span data-ttu-id="1ed1d-192">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="1ed1d-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-193">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-194">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-195">Aastane</span><span class="sxs-lookup"><span data-stu-id="1ed1d-195">Annual</span></span>            | <span data-ttu-id="1ed1d-196">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-196">Plan start date</span></span>      | <span data-ttu-id="1ed1d-197">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="1ed1d-197">End of accrual period</span></span> |

<span data-ttu-id="1ed1d-198">Viitvõlad töödeldakse 01. jaanuaril 2019 (01/01/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="1ed1d-199">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-199">**Results**</span></span>

| <span data-ttu-id="1ed1d-200">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-200">Accrual amount</span></span> | <span data-ttu-id="1ed1d-201">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-201">Minimum balance</span></span> | <span data-ttu-id="1ed1d-202">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-202">Maximum carry-forward</span></span> | <span data-ttu-id="1ed1d-203">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-203">Request amount</span></span> | <span data-ttu-id="1ed1d-204">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="1ed1d-205">200</span><span class="sxs-lookup"><span data-stu-id="1ed1d-205">200</span></span>            | <span data-ttu-id="1ed1d-206">0</span><span class="sxs-lookup"><span data-stu-id="1ed1d-206">0</span></span>               | <span data-ttu-id="1ed1d-207">120</span><span class="sxs-lookup"><span data-stu-id="1ed1d-207">120</span></span>                   | <span data-ttu-id="1ed1d-208">40</span><span class="sxs-lookup"><span data-stu-id="1ed1d-208">40</span></span>             | <span data-ttu-id="1ed1d-209">160</span><span class="sxs-lookup"><span data-stu-id="1ed1d-209">160</span></span>                              |

<span data-ttu-id="1ed1d-210">Praegune saldo (160) = viitvõla summa (200) – taotluse summa (40)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="1ed1d-211">Poole kuu plaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-211">Semimonthly plan</span></span>

<span data-ttu-id="1ed1d-212">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-212">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-213">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-213">Plan start date</span></span> | <span data-ttu-id="1ed1d-214">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-214">Enrollment date</span></span> | <span data-ttu-id="1ed1d-215">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-215">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-216">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-216">Accrual period basis</span></span> | <span data-ttu-id="1ed1d-217">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="1ed1d-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-218">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-219">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-219">2/1/2018</span></span>        | <span data-ttu-id="1ed1d-220">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-220">Semimonthly</span></span>       | <span data-ttu-id="1ed1d-221">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-221">Plan start date</span></span>      | <span data-ttu-id="1ed1d-222">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="1ed1d-222">End of accrual period</span></span> |

<span data-ttu-id="1ed1d-223">Viitvõlad töödeldakse 01. mail 2018 (01/05/2018), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="1ed1d-224">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-224">**Results**</span></span>

| <span data-ttu-id="1ed1d-225">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-225">Accrual amount</span></span> | <span data-ttu-id="1ed1d-226">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-226">Minimum balance</span></span> | <span data-ttu-id="1ed1d-227">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-227">Maximum carry-forward</span></span> | <span data-ttu-id="1ed1d-228">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-228">Request amount</span></span> | <span data-ttu-id="1ed1d-229">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="1ed1d-230">5</span><span class="sxs-lookup"><span data-stu-id="1ed1d-230">5</span></span>              | <span data-ttu-id="1ed1d-231">0</span><span class="sxs-lookup"><span data-stu-id="1ed1d-231">0</span></span>               | <span data-ttu-id="1ed1d-232">120</span><span class="sxs-lookup"><span data-stu-id="1ed1d-232">120</span></span>                   | <span data-ttu-id="1ed1d-233">8</span><span class="sxs-lookup"><span data-stu-id="1ed1d-233">8</span></span>              | <span data-ttu-id="1ed1d-234">22</span><span class="sxs-lookup"><span data-stu-id="1ed1d-234">22</span></span>                               |

<span data-ttu-id="1ed1d-235">Praegune saldo (22) = viitvõla summa (5 × 6) – taotluse summa (8)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="1ed1d-236">Kuuplaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-236">Monthly plan</span></span>

<span data-ttu-id="1ed1d-237">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-237">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-238">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-238">Plan start date</span></span> | <span data-ttu-id="1ed1d-239">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-239">Enrollment date</span></span> | <span data-ttu-id="1ed1d-240">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-240">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-241">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-241">Accrual period basis</span></span> | <span data-ttu-id="1ed1d-242">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="1ed1d-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-243">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-244">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-244">2/1/2018</span></span>        | <span data-ttu-id="1ed1d-245">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-245">Semimonthly</span></span>       | <span data-ttu-id="1ed1d-246">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-246">Plan start date</span></span>      | <span data-ttu-id="1ed1d-247">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="1ed1d-247">End of accrual period</span></span> |

<span data-ttu-id="1ed1d-248">Viitvõlad töödeldakse 01. mail 2018 (01/05/2018), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="1ed1d-249">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-249">**Results**</span></span>

| <span data-ttu-id="1ed1d-250">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-250">Accrual amount</span></span> | <span data-ttu-id="1ed1d-251">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-251">Minimum balance</span></span> | <span data-ttu-id="1ed1d-252">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-252">Maximum carry-forward</span></span> | <span data-ttu-id="1ed1d-253">Taotletud summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-253">Request amount</span></span> | <span data-ttu-id="1ed1d-254">Praegune saldo (01. jaanuari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="1ed1d-255">5</span><span class="sxs-lookup"><span data-stu-id="1ed1d-255">5</span></span>              | <span data-ttu-id="1ed1d-256">0</span><span class="sxs-lookup"><span data-stu-id="1ed1d-256">0</span></span>               | <span data-ttu-id="1ed1d-257">120</span><span class="sxs-lookup"><span data-stu-id="1ed1d-257">120</span></span>                   | <span data-ttu-id="1ed1d-258">8</span><span class="sxs-lookup"><span data-stu-id="1ed1d-258">8</span></span>              | <span data-ttu-id="1ed1d-259">7</span><span class="sxs-lookup"><span data-stu-id="1ed1d-259">7</span></span>                                |

<span data-ttu-id="1ed1d-260">Praegune saldo (7) = viitvõla summa (5 × 3) – taotluse summa (8)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="1ed1d-261">Prognoositud saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-261">Forecasted balance</span></span>

<span data-ttu-id="1ed1d-262">See *eelarvesaldo* on tulevasel kuupäeval saadaolev puhkuse kogus.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="1ed1d-263">Viitvõlgade ja ülekandmise korrigeerimised on prognoositud selleks kuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="1ed1d-264">Arvutamisel kasutatakse järgmist valemit:</span><span class="sxs-lookup"><span data-stu-id="1ed1d-264">The following formula is used:</span></span>

<span data-ttu-id="1ed1d-265">Esmaspäeva prognoositud saldo = praegune saldo – taotlused + viitvõlad – ülekandmise korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="1ed1d-266">Prognoositud saldo näited</span><span class="sxs-lookup"><span data-stu-id="1ed1d-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="1ed1d-267">Aastaplaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-267">Annual plan</span></span>

<span data-ttu-id="1ed1d-268">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-268">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-269">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-269">Plan start date</span></span> | <span data-ttu-id="1ed1d-270">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-270">Enrollment date</span></span> | <span data-ttu-id="1ed1d-271">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-271">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-272">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-272">Accrual period basis</span></span> | <span data-ttu-id="1ed1d-273">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="1ed1d-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-274">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-275">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-276">Aastane</span><span class="sxs-lookup"><span data-stu-id="1ed1d-276">Annual</span></span>            | <span data-ttu-id="1ed1d-277">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-277">Plan start date</span></span>      | <span data-ttu-id="1ed1d-278">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="1ed1d-278">End of accrual period</span></span> |

<span data-ttu-id="1ed1d-279">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="1ed1d-280">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-280">**Results**</span></span>

| <span data-ttu-id="1ed1d-281">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-281">Accrual amount</span></span> | <span data-ttu-id="1ed1d-282">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-282">Minimum balance</span></span> | <span data-ttu-id="1ed1d-283">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-283">Maximum carry-forward</span></span> | <span data-ttu-id="1ed1d-284">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-284">Current balance</span></span> | <span data-ttu-id="1ed1d-285">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="1ed1d-286">20</span><span class="sxs-lookup"><span data-stu-id="1ed1d-286">20</span></span>             | <span data-ttu-id="1ed1d-287">0</span><span class="sxs-lookup"><span data-stu-id="1ed1d-287">0</span></span>               | <span data-ttu-id="1ed1d-288">20</span><span class="sxs-lookup"><span data-stu-id="1ed1d-288">20</span></span>                    | <span data-ttu-id="1ed1d-289">40</span><span class="sxs-lookup"><span data-stu-id="1ed1d-289">40</span></span>              | <span data-ttu-id="1ed1d-290">40</span><span class="sxs-lookup"><span data-stu-id="1ed1d-290">40</span></span>                                   |

<span data-ttu-id="1ed1d-291">Prognoositud saldo (40) = juurdekasvu summa (20) – praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="1ed1d-292">Poole kuu plaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-292">Semimonthly plan</span></span>

<span data-ttu-id="1ed1d-293">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-293">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-294">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-294">Plan start date</span></span> | <span data-ttu-id="1ed1d-295">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-295">Enrollment date</span></span> | <span data-ttu-id="1ed1d-296">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-296">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-297">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-297">Accrual period basis</span></span> | <span data-ttu-id="1ed1d-298">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="1ed1d-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-299">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-300">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-300">2/1/2018</span></span>        | <span data-ttu-id="1ed1d-301">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-301">Semimonthly</span></span>       | <span data-ttu-id="1ed1d-302">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-302">Plan start date</span></span>      | <span data-ttu-id="1ed1d-303">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="1ed1d-303">End of accrual period</span></span> |

<span data-ttu-id="1ed1d-304">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="1ed1d-305">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-305">**Results**</span></span>

| <span data-ttu-id="1ed1d-306">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-306">Accrual amount</span></span> | <span data-ttu-id="1ed1d-307">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-307">Minimum balance</span></span> | <span data-ttu-id="1ed1d-308">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-308">Maximum carry-forward</span></span> | <span data-ttu-id="1ed1d-309">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-309">Current balance</span></span> | <span data-ttu-id="1ed1d-310">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="1ed1d-311">5</span><span class="sxs-lookup"><span data-stu-id="1ed1d-311">5</span></span>              | <span data-ttu-id="1ed1d-312">0</span><span class="sxs-lookup"><span data-stu-id="1ed1d-312">0</span></span>               | <span data-ttu-id="1ed1d-313">20</span><span class="sxs-lookup"><span data-stu-id="1ed1d-313">20</span></span>                    | <span data-ttu-id="1ed1d-314">40</span><span class="sxs-lookup"><span data-stu-id="1ed1d-314">40</span></span>              | <span data-ttu-id="1ed1d-315">35</span><span class="sxs-lookup"><span data-stu-id="1ed1d-315">35</span></span>                                   |

<span data-ttu-id="1ed1d-316">Prognoositud saldo (35) = juurdekasvu summa (5 × 3) + praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="1ed1d-317">Kuuplaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-317">Monthly plan</span></span>

<span data-ttu-id="1ed1d-318">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-318">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-319">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-319">Plan start date</span></span> | <span data-ttu-id="1ed1d-320">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-320">Enrollment date</span></span> | <span data-ttu-id="1ed1d-321">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-321">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-322">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-322">Accrual period basis</span></span> | <span data-ttu-id="1ed1d-323">Puhkuse andmise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="1ed1d-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-324">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-325">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-325">2/1/2018</span></span>        | <span data-ttu-id="1ed1d-326">Kaks korda kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-326">Semimonthly</span></span>       | <span data-ttu-id="1ed1d-327">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-327">Plan start date</span></span>      | <span data-ttu-id="1ed1d-328">Puhkuseperioodi lõpp</span><span class="sxs-lookup"><span data-stu-id="1ed1d-328">End of accrual period</span></span> |

<span data-ttu-id="1ed1d-329">Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.</span><span class="sxs-lookup"><span data-stu-id="1ed1d-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="1ed1d-330">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-330">**Results**</span></span>

| <span data-ttu-id="1ed1d-331">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-331">Accrual amount</span></span> | <span data-ttu-id="1ed1d-332">Minimaalne saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-332">Minimum balance</span></span> | <span data-ttu-id="1ed1d-333">Maksimaalne edasikandmine</span><span class="sxs-lookup"><span data-stu-id="1ed1d-333">Maximum carry-forward</span></span> | <span data-ttu-id="1ed1d-334">Praegune saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-334">Current balance</span></span> | <span data-ttu-id="1ed1d-335">Prognoositud saldo (15. veebruari 2019 seisuga)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="1ed1d-336">10</span><span class="sxs-lookup"><span data-stu-id="1ed1d-336">10</span></span>             | <span data-ttu-id="1ed1d-337">0</span><span class="sxs-lookup"><span data-stu-id="1ed1d-337">0</span></span>               | <span data-ttu-id="1ed1d-338">20</span><span class="sxs-lookup"><span data-stu-id="1ed1d-338">20</span></span>                    | <span data-ttu-id="1ed1d-339">40</span><span class="sxs-lookup"><span data-stu-id="1ed1d-339">40</span></span>              | <span data-ttu-id="1ed1d-340">30</span><span class="sxs-lookup"><span data-stu-id="1ed1d-340">30</span></span>                                   |

<span data-ttu-id="1ed1d-341">Prognoositud saldo (30) = juurdekasvu summa (10 × 1) – praegune saldo (40) – ülekandmise korrigeerimine (20)</span><span class="sxs-lookup"><span data-stu-id="1ed1d-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="1ed1d-342">Proportsionaalse arvestuse saldo näited</span><span class="sxs-lookup"><span data-stu-id="1ed1d-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="1ed1d-343">Proportsionaalse arvestuse kuuplaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-343">Prorated monthly plan</span></span>

<span data-ttu-id="1ed1d-344">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-344">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-345">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-345">Plan start date</span></span> | <span data-ttu-id="1ed1d-346">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-346">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-347">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="1ed1d-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-348">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-349">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-349">Monthly</span></span>           | <span data-ttu-id="1ed1d-350">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-350">Plan start date</span></span>      |

<span data-ttu-id="1ed1d-351">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-351">**Results**</span></span>

| <span data-ttu-id="1ed1d-352">Töötaja</span><span class="sxs-lookup"><span data-stu-id="1ed1d-352">Employee</span></span>            | <span data-ttu-id="1ed1d-353">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="1ed1d-353">Months of service</span></span> | <span data-ttu-id="1ed1d-354">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-354">Enrollment date</span></span> | <span data-ttu-id="1ed1d-355">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-355">Start date</span></span> | <span data-ttu-id="1ed1d-356">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-356">Accrual amount</span></span> | <span data-ttu-id="1ed1d-357">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="1ed1d-357">Process accrual</span></span> | <span data-ttu-id="1ed1d-358">Saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="1ed1d-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="1ed1d-359">Jeannette Nicholson</span></span> | <span data-ttu-id="1ed1d-360">0,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-360">0.00</span></span>              | <span data-ttu-id="1ed1d-361">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-361">6/1/2018</span></span>        | <span data-ttu-id="1ed1d-362">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-362">6/1/2018</span></span>   | <span data-ttu-id="1ed1d-363">1,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-363">1.00</span></span>           | <span data-ttu-id="1ed1d-364">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-364">9/1/2018</span></span>        | <span data-ttu-id="1ed1d-365">3,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-365">3.00</span></span>    |
| <span data-ttu-id="1ed1d-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="1ed1d-366">Jay Norman</span></span>          | <span data-ttu-id="1ed1d-367">0,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-367">0.00</span></span>              | <span data-ttu-id="1ed1d-368">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-368">6/15/2018</span></span>       | <span data-ttu-id="1ed1d-369">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-369">6/15/2018</span></span>  | <span data-ttu-id="1ed1d-370">1,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-370">1.00</span></span>           | <span data-ttu-id="1ed1d-371">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-371">9/1/2018</span></span>        | <span data-ttu-id="1ed1d-372">2,53</span><span class="sxs-lookup"><span data-stu-id="1ed1d-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="1ed1d-373">Täieliku arvestuse kuuplaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-373">Full accrual monthly plan</span></span>

<span data-ttu-id="1ed1d-374">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-374">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-375">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-375">Plan start date</span></span> | <span data-ttu-id="1ed1d-376">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-376">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-377">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="1ed1d-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-378">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-379">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-379">Monthly</span></span>           | <span data-ttu-id="1ed1d-380">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-380">Plan start date</span></span>      |

<span data-ttu-id="1ed1d-381">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-381">**Results**</span></span>

| <span data-ttu-id="1ed1d-382">Töötaja</span><span class="sxs-lookup"><span data-stu-id="1ed1d-382">Employee</span></span>            | <span data-ttu-id="1ed1d-383">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="1ed1d-383">Months of service</span></span> | <span data-ttu-id="1ed1d-384">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-384">Enrollment date</span></span> | <span data-ttu-id="1ed1d-385">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-385">Start date</span></span> | <span data-ttu-id="1ed1d-386">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-386">Accrual amount</span></span> | <span data-ttu-id="1ed1d-387">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="1ed1d-387">Process accrual</span></span> | <span data-ttu-id="1ed1d-388">Saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="1ed1d-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="1ed1d-389">Jeannette Nicholson</span></span> | <span data-ttu-id="1ed1d-390">0,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-390">0.00</span></span>              | <span data-ttu-id="1ed1d-391">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-391">6/1/2018</span></span>        | <span data-ttu-id="1ed1d-392">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-392">6/1/2018</span></span>   | <span data-ttu-id="1ed1d-393">1,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-393">1.00</span></span>           | <span data-ttu-id="1ed1d-394">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-394">9/1/2018</span></span>        | <span data-ttu-id="1ed1d-395">3,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-395">3.00</span></span>    |
| <span data-ttu-id="1ed1d-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="1ed1d-396">Jay Norman</span></span>          | <span data-ttu-id="1ed1d-397">0,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-397">0.00</span></span>              | <span data-ttu-id="1ed1d-398">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-398">6/15/2018</span></span>       | <span data-ttu-id="1ed1d-399">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-399">6/15/2018</span></span>  | <span data-ttu-id="1ed1d-400">1,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-400">1.00</span></span>           | <span data-ttu-id="1ed1d-401">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-401">9/1/2018</span></span>        | <span data-ttu-id="1ed1d-402">3,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="1ed1d-403">Arvestuse puudumise kuuplaan</span><span class="sxs-lookup"><span data-stu-id="1ed1d-403">No accrual monthly plan</span></span>

<span data-ttu-id="1ed1d-404">**Plaani seadistus**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-404">**Plan setup**</span></span>

| <span data-ttu-id="1ed1d-405">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-405">Plan start date</span></span> | <span data-ttu-id="1ed1d-406">Puhkuse andmise sagedus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-406">Accrual frequency</span></span> | <span data-ttu-id="1ed1d-407">Puhkuseperioodi alus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="1ed1d-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-408">1/1/2018</span></span>        | <span data-ttu-id="1ed1d-409">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="1ed1d-409">Monthly</span></span>           | <span data-ttu-id="1ed1d-410">Plaanitav alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-410">Plan start date</span></span>      |

<span data-ttu-id="1ed1d-411">**Tulemused**</span><span class="sxs-lookup"><span data-stu-id="1ed1d-411">**Results**</span></span>

| <span data-ttu-id="1ed1d-412">Töötaja</span><span class="sxs-lookup"><span data-stu-id="1ed1d-412">Employee</span></span>            | <span data-ttu-id="1ed1d-413">Töötatud kuud</span><span class="sxs-lookup"><span data-stu-id="1ed1d-413">Months of service</span></span> | <span data-ttu-id="1ed1d-414">Registreerimise kuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-414">Enrollment date</span></span> | <span data-ttu-id="1ed1d-415">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="1ed1d-415">Start date</span></span> | <span data-ttu-id="1ed1d-416">Juurdekasvu summa</span><span class="sxs-lookup"><span data-stu-id="1ed1d-416">Accrual amount</span></span> | <span data-ttu-id="1ed1d-417">Viitvõlgade protsess</span><span class="sxs-lookup"><span data-stu-id="1ed1d-417">Process accrual</span></span> | <span data-ttu-id="1ed1d-418">Saldo</span><span class="sxs-lookup"><span data-stu-id="1ed1d-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="1ed1d-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="1ed1d-419">Jeannette Nicholson</span></span> | <span data-ttu-id="1ed1d-420">0,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-420">0.00</span></span>              | <span data-ttu-id="1ed1d-421">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-421">6/1/2018</span></span>        | <span data-ttu-id="1ed1d-422">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-422">6/1/2018</span></span>   | <span data-ttu-id="1ed1d-423">1,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-423">1.00</span></span>           | <span data-ttu-id="1ed1d-424">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-424">9/1/2018</span></span>        | <span data-ttu-id="1ed1d-425">3,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-425">3.00</span></span>    |
| <span data-ttu-id="1ed1d-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="1ed1d-426">Jay Norman</span></span>          | <span data-ttu-id="1ed1d-427">0,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-427">0.00</span></span>              | <span data-ttu-id="1ed1d-428">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-428">6/15/2018</span></span>       | <span data-ttu-id="1ed1d-429">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-429">6/15/2018</span></span>  | <span data-ttu-id="1ed1d-430">1,00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-430">1.00</span></span>           | <span data-ttu-id="1ed1d-431">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="1ed1d-431">9/1/2018</span></span>        | <span data-ttu-id="1ed1d-432">2.00</span><span class="sxs-lookup"><span data-stu-id="1ed1d-432">2.00</span></span>    |
