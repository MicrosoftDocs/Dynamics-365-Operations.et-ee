---
title: Common Data Service’i üksused
description: Microsoft Dynamics 365 Human Resources kasutab teenust Common Data Service, et lubada laiendatavus ja integreerimise stsenaariumid.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166494"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="61e7b-103">Common Data Service’i üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-103">Common Data Service entities</span></span>

<span data-ttu-id="61e7b-104">Microsoft Dynamics 365 Human Resources kasutab teenust Common Data Service, et lubada laiendatavus ja integreerimise stsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="61e7b-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="61e7b-105">Teenuse Common Data Service kohta lisateabe saamiseks vt teemat [Mis on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="61e7b-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="61e7b-106">Teenuses Common Data Service on saadaval järgmised rakenduse Human Resources üksused.</span><span class="sxs-lookup"><span data-stu-id="61e7b-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="61e7b-107">Soodustuse üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-107">Benefit entities</span></span>

| <span data-ttu-id="61e7b-108">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-108">Name</span></span> | <span data-ttu-id="61e7b-109">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-110">Soodustuse arvutamise sagedus</span><span class="sxs-lookup"><span data-stu-id="61e7b-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="61e7b-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="61e7b-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="61e7b-112">Soodustuse arvutamise sagedus makseperioodil</span><span class="sxs-lookup"><span data-stu-id="61e7b-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="61e7b-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="61e7b-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="61e7b-114">Soodustuse arvutamise määr</span><span class="sxs-lookup"><span data-stu-id="61e7b-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="61e7b-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="61e7b-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="61e7b-116">Soodustuse arvutamise määra üksikasjad</span><span class="sxs-lookup"><span data-stu-id="61e7b-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="61e7b-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="61e7b-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="61e7b-118">Soodustuse suvand</span><span class="sxs-lookup"><span data-stu-id="61e7b-118">Benefit Option</span></span> | <span data-ttu-id="61e7b-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="61e7b-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="61e7b-120">Soodustuse plaan</span><span class="sxs-lookup"><span data-stu-id="61e7b-120">Benefit Plan</span></span> | <span data-ttu-id="61e7b-121">cdm_benefitplan (kohandatud väljade toeks pole lubatud)</span><span class="sxs-lookup"><span data-stu-id="61e7b-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="61e7b-122">Hüvitise liik</span><span class="sxs-lookup"><span data-stu-id="61e7b-122">Benefit Type</span></span> | <span data-ttu-id="61e7b-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="61e7b-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="61e7b-124">Äriprotsessi ülesannete üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-124">Business process tasks entities</span></span>

| <span data-ttu-id="61e7b-125">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-125">Name</span></span> | <span data-ttu-id="61e7b-126">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-127">Äriprotsessi kalender</span><span class="sxs-lookup"><span data-stu-id="61e7b-127">Business Process Calendar</span></span> | <span data-ttu-id="61e7b-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="61e7b-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="61e7b-129">Äriprotsessi grupimäärang</span><span class="sxs-lookup"><span data-stu-id="61e7b-129">Business Process Group Assignment</span></span> | <span data-ttu-id="61e7b-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="61e7b-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="61e7b-131">Äriprotsessi teegi ülesandegrupp</span><span class="sxs-lookup"><span data-stu-id="61e7b-131">Business Process Library Task Group</span></span> | <span data-ttu-id="61e7b-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="61e7b-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="61e7b-133">Äriprotsessi etapp</span><span class="sxs-lookup"><span data-stu-id="61e7b-133">Business Process Stage</span></span> | <span data-ttu-id="61e7b-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="61e7b-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="61e7b-135">Kontroll-loendi malli päis</span><span class="sxs-lookup"><span data-stu-id="61e7b-135">Checklist Template Header</span></span> | <span data-ttu-id="61e7b-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="61e7b-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="61e7b-137">Kontroll-loendi malli ülesanne</span><span class="sxs-lookup"><span data-stu-id="61e7b-137">Checklist Template Task</span></span> | <span data-ttu-id="61e7b-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="61e7b-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="61e7b-139">Hüvitise üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-139">Compensation entities</span></span>

| <span data-ttu-id="61e7b-140">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-140">Name</span></span> | <span data-ttu-id="61e7b-141">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-142">Palga põhiplaan</span><span class="sxs-lookup"><span data-stu-id="61e7b-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="61e7b-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="61e7b-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="61e7b-144">Kogupalga tabel</span><span class="sxs-lookup"><span data-stu-id="61e7b-144">Compensation Grid</span></span> | <span data-ttu-id="61e7b-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="61e7b-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="61e7b-146">Hüvitustase</span><span class="sxs-lookup"><span data-stu-id="61e7b-146">Compensation Level</span></span> | <span data-ttu-id="61e7b-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="61e7b-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="61e7b-148">Palga tasumissagedus</span><span class="sxs-lookup"><span data-stu-id="61e7b-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="61e7b-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="61e7b-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="61e7b-150">Palga võrdluspunkti seadistus</span><span class="sxs-lookup"><span data-stu-id="61e7b-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="61e7b-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="61e7b-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="61e7b-152">Palga võrdluspunkti seadistuse rida</span><span class="sxs-lookup"><span data-stu-id="61e7b-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="61e7b-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="61e7b-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="61e7b-154">Hüvituspiirkond</span><span class="sxs-lookup"><span data-stu-id="61e7b-154">Compensation Region</span></span> | <span data-ttu-id="61e7b-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="61e7b-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="61e7b-156">Palga struktuur</span><span class="sxs-lookup"><span data-stu-id="61e7b-156">Compensation Structure</span></span> | <span data-ttu-id="61e7b-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="61e7b-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="61e7b-158">Muutuv hüvitisplaan</span><span class="sxs-lookup"><span data-stu-id="61e7b-158">Compensation Variable Plan</span></span> | <span data-ttu-id="61e7b-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="61e7b-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="61e7b-160">Muutuva hüvitisplaani tase</span><span class="sxs-lookup"><span data-stu-id="61e7b-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="61e7b-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="61e7b-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="61e7b-162">Muutuva hüvitisplaani tüüp</span><span class="sxs-lookup"><span data-stu-id="61e7b-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="61e7b-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="61e7b-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="61e7b-164">Põhipalga sündmus</span><span class="sxs-lookup"><span data-stu-id="61e7b-164">Fixed Compensation Event</span></span> | <span data-ttu-id="61e7b-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="61e7b-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="61e7b-166">Pensionireegel</span><span class="sxs-lookup"><span data-stu-id="61e7b-166">Vesting Rule</span></span> | <span data-ttu-id="61e7b-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="61e7b-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="61e7b-168">Töötaja põhipalk</span><span class="sxs-lookup"><span data-stu-id="61e7b-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="61e7b-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="61e7b-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="61e7b-170">Organisatsiooni üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-170">Organization entities</span></span>

| <span data-ttu-id="61e7b-171">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-171">Name</span></span> | <span data-ttu-id="61e7b-172">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-173">Osakond</span><span class="sxs-lookup"><span data-stu-id="61e7b-173">Department</span></span> | <span data-ttu-id="61e7b-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="61e7b-174">cdm_department</span></span> |
| <span data-ttu-id="61e7b-175">Töösuhe</span><span class="sxs-lookup"><span data-stu-id="61e7b-175">Employment</span></span> | <span data-ttu-id="61e7b-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="61e7b-176">cdm_employment</span></span> |
| <span data-ttu-id="61e7b-177">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="61e7b-177">Company</span></span> | <span data-ttu-id="61e7b-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="61e7b-178">cdm_company</span></span> |
| <span data-ttu-id="61e7b-179">Amet</span><span class="sxs-lookup"><span data-stu-id="61e7b-179">Job</span></span> | <span data-ttu-id="61e7b-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="61e7b-180">cdm_job</span></span> |
| <span data-ttu-id="61e7b-181">Tööfunktsioon</span><span class="sxs-lookup"><span data-stu-id="61e7b-181">Job Function</span></span> | <span data-ttu-id="61e7b-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="61e7b-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="61e7b-183">Ametikoht</span><span class="sxs-lookup"><span data-stu-id="61e7b-183">Job Position</span></span> | <span data-ttu-id="61e7b-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="61e7b-184">cdm_jobposition</span></span> |
| <span data-ttu-id="61e7b-185">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="61e7b-185">Position Type</span></span> | <span data-ttu-id="61e7b-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="61e7b-186">cdm_positiontype</span></span> |
| <span data-ttu-id="61e7b-187">Ametikoha töötaja määramine</span><span class="sxs-lookup"><span data-stu-id="61e7b-187">Position Worker Assignment</span></span> | <span data-ttu-id="61e7b-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="61e7b-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="61e7b-189">Ametikoha dimensioon</span><span class="sxs-lookup"><span data-stu-id="61e7b-189">Job Position Dimension</span></span> | <span data-ttu-id="61e7b-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="61e7b-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="61e7b-191">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="61e7b-191">Job Type</span></span> | <span data-ttu-id="61e7b-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="61e7b-192">cdm_jobtype</span></span> |
| <span data-ttu-id="61e7b-193">Keel</span><span class="sxs-lookup"><span data-stu-id="61e7b-193">Language</span></span> | <span data-ttu-id="61e7b-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="61e7b-194">cdm_language</span></span> |
| <span data-ttu-id="61e7b-195">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="61e7b-195">Title</span></span> | <span data-ttu-id="61e7b-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="61e7b-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="61e7b-197">Üksuste **Ametikoha tüüp** **Töötaja ametikoha määramine** ja **Töölevõtt** finantsdimensioonid pakuvad ühesuunalist integratsiooni Common Data Service'iga.</span><span class="sxs-lookup"><span data-stu-id="61e7b-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="61e7b-198">Finantsdimensioonide värskendusi ei saa praegu sünkroonida Common Data Service'ist Human Resourcesisse.</span><span class="sxs-lookup"><span data-stu-id="61e7b-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="61e7b-199">Puhkuste ja puudumiste üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-199">Leave and absence entities</span></span>

| <span data-ttu-id="61e7b-200">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-200">Name</span></span> | <span data-ttu-id="61e7b-201">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-202">Puhkuste panga kanne</span><span class="sxs-lookup"><span data-stu-id="61e7b-202">Leave Bank Transaction</span></span> | <span data-ttu-id="61e7b-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="61e7b-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="61e7b-204">Puhkuse registreerimine</span><span class="sxs-lookup"><span data-stu-id="61e7b-204">Leave Enrollment</span></span> | <span data-ttu-id="61e7b-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="61e7b-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="61e7b-206">Puhkuseplaan</span><span class="sxs-lookup"><span data-stu-id="61e7b-206">Leave Plan</span></span> | <span data-ttu-id="61e7b-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="61e7b-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="61e7b-208">Puhkusetaotlus</span><span class="sxs-lookup"><span data-stu-id="61e7b-208">Leave Request</span></span> | <span data-ttu-id="61e7b-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="61e7b-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="61e7b-210">Puhkuse taotluse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="61e7b-210">Leave Request Detail</span></span> | <span data-ttu-id="61e7b-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="61e7b-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="61e7b-212">Puhkuse tüüp</span><span class="sxs-lookup"><span data-stu-id="61e7b-212">Leave Type</span></span> | <span data-ttu-id="61e7b-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="61e7b-213">cdm_leavetype</span></span> |
| <span data-ttu-id="61e7b-214">Puhkusetüübi põhjusekood</span><span class="sxs-lookup"><span data-stu-id="61e7b-214">Leave Type Reason Code</span></span> | <span data-ttu-id="61e7b-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="61e7b-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="61e7b-216">Palgaolemid</span><span class="sxs-lookup"><span data-stu-id="61e7b-216">Payroll entities</span></span>

| <span data-ttu-id="61e7b-217">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-217">Name</span></span> | <span data-ttu-id="61e7b-218">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-219">Palgatsükkel</span><span class="sxs-lookup"><span data-stu-id="61e7b-219">Pay Cycle</span></span> | <span data-ttu-id="61e7b-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="61e7b-220">cdm_paycycle</span></span> |
| <span data-ttu-id="61e7b-221">Makseperiood</span><span class="sxs-lookup"><span data-stu-id="61e7b-221">Pay Period</span></span> | <span data-ttu-id="61e7b-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="61e7b-222">cdm_payperiod</span></span> |
| <span data-ttu-id="61e7b-223">Palga tulukood</span><span class="sxs-lookup"><span data-stu-id="61e7b-223">Payroll Earning Code</span></span> | <span data-ttu-id="61e7b-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="61e7b-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="61e7b-225">Pangakonto väljamakse</span><span class="sxs-lookup"><span data-stu-id="61e7b-225">Bank Account Disbursement</span></span> | <span data-ttu-id="61e7b-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="61e7b-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="61e7b-227">Maksuregioon</span><span class="sxs-lookup"><span data-stu-id="61e7b-227">Tax Region</span></span> | <span data-ttu-id="61e7b-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="61e7b-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="61e7b-229">Töötaja üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-229">Worker entities</span></span>

| <span data-ttu-id="61e7b-230">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-230">Name</span></span> | <span data-ttu-id="61e7b-231">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-232">Töötaja</span><span class="sxs-lookup"><span data-stu-id="61e7b-232">Worker</span></span> | <span data-ttu-id="61e7b-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="61e7b-233">cdm_worker</span></span> |
| <span data-ttu-id="61e7b-234">Töötaja aadress</span><span class="sxs-lookup"><span data-stu-id="61e7b-234">Worker Address</span></span> | <span data-ttu-id="61e7b-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="61e7b-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="61e7b-236">Töötaja isikuteave</span><span class="sxs-lookup"><span data-stu-id="61e7b-236">Worker Personal Detail</span></span> | <span data-ttu-id="61e7b-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="61e7b-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="61e7b-238">Töötaja isiku ID-number</span><span class="sxs-lookup"><span data-stu-id="61e7b-238">Worker Person Identification Number</span></span> | <span data-ttu-id="61e7b-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="61e7b-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="61e7b-240">Töötaja isiku identifitseerimistüüp</span><span class="sxs-lookup"><span data-stu-id="61e7b-240">Worker Person Identification Type</span></span> | <span data-ttu-id="61e7b-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="61e7b-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="61e7b-242">Töökalender</span><span class="sxs-lookup"><span data-stu-id="61e7b-242">Work Calendar</span></span> | <span data-ttu-id="61e7b-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="61e7b-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="61e7b-244">Töökalendri päev</span><span class="sxs-lookup"><span data-stu-id="61e7b-244">Work Calendar Day</span></span> | <span data-ttu-id="61e7b-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="61e7b-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="61e7b-246">Töökalendri püha</span><span class="sxs-lookup"><span data-stu-id="61e7b-246">Work Calendar Holiday</span></span> |<span data-ttu-id="61e7b-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="61e7b-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="61e7b-248">Töökalendri puhkuse rida</span><span class="sxs-lookup"><span data-stu-id="61e7b-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="61e7b-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="61e7b-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="61e7b-250">Töökalendri ajaintervall</span><span class="sxs-lookup"><span data-stu-id="61e7b-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="61e7b-251">cdm_workcalendartimeinterval (kohandatud väljade toeks pole lubatud)</span><span class="sxs-lookup"><span data-stu-id="61e7b-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="61e7b-252">Töötaja pangakonto</span><span class="sxs-lookup"><span data-stu-id="61e7b-252">Worker Bank Account</span></span> | <span data-ttu-id="61e7b-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="61e7b-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="61e7b-254">Töötaja seadistuse üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-254">Worker setup entities</span></span>

| <span data-ttu-id="61e7b-255">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-255">Name</span></span> | <span data-ttu-id="61e7b-256">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-257">Veterani staatus</span><span class="sxs-lookup"><span data-stu-id="61e7b-257">Veteran Status</span></span> | <span data-ttu-id="61e7b-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="61e7b-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="61e7b-259">Etniline päritolu</span><span class="sxs-lookup"><span data-stu-id="61e7b-259">Ethnic Origin</span></span> | <span data-ttu-id="61e7b-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="61e7b-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="61e7b-261">Põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="61e7b-261">Reason Code</span></span> | <span data-ttu-id="61e7b-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="61e7b-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="61e7b-263">Isikut ID väljastanud asutus</span><span class="sxs-lookup"><span data-stu-id="61e7b-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="61e7b-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="61e7b-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="61e7b-265">Pädevuse üksused</span><span class="sxs-lookup"><span data-stu-id="61e7b-265">Competency entities</span></span>

| <span data-ttu-id="61e7b-266">Nimi</span><span class="sxs-lookup"><span data-stu-id="61e7b-266">Name</span></span> | <span data-ttu-id="61e7b-267">Üksus</span><span class="sxs-lookup"><span data-stu-id="61e7b-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="61e7b-268">Oskuse tüüp</span><span class="sxs-lookup"><span data-stu-id="61e7b-268">Skill Type</span></span> | <span data-ttu-id="61e7b-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="61e7b-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="61e7b-270">Üksuse seose mudelid</span><span class="sxs-lookup"><span data-stu-id="61e7b-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="61e7b-271">Töötaja</span><span class="sxs-lookup"><span data-stu-id="61e7b-271">Worker</span></span>

![Töötaja](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="61e7b-273">Töö ja ametikoht</span><span class="sxs-lookup"><span data-stu-id="61e7b-273">Job and Job Position</span></span>

![Töö ja ametikoht](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="61e7b-275">Soodustused</span><span class="sxs-lookup"><span data-stu-id="61e7b-275">Benefits</span></span>

![Soodustused](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="61e7b-277">Kompensatsioon</span><span class="sxs-lookup"><span data-stu-id="61e7b-277">Compensation</span></span>

![Kompensatsioon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="61e7b-279">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="61e7b-279">Leave</span></span>

![Lahkumine](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="61e7b-281">Töökalender</span><span class="sxs-lookup"><span data-stu-id="61e7b-281">Work Calendar</span></span>

![Töökalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="61e7b-283">Vt ka</span><span class="sxs-lookup"><span data-stu-id="61e7b-283">See also</span></span>

[<span data-ttu-id="61e7b-284">Andme integratsioonitehnoloogia valimine</span><span class="sxs-lookup"><span data-stu-id="61e7b-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="61e7b-285">Common Data Service’i integratsiooni konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="61e7b-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
