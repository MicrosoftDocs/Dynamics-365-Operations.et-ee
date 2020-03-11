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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087342"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="6dd0c-103">Common Data Service’i üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-103">Common Data Service entities</span></span>

<span data-ttu-id="6dd0c-104">Microsoft Dynamics 365 Human Resources kasutab teenust Common Data Service, et lubada laiendatavus ja integreerimise stsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="6dd0c-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="6dd0c-105">Teenuse Common Data Service kohta lisateabe saamiseks vt teemat [Mis on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="6dd0c-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="6dd0c-106">Teenuses Common Data Service on saadaval järgmised rakenduse Human Resources üksused.</span><span class="sxs-lookup"><span data-stu-id="6dd0c-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="6dd0c-107">Soodustuse üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-107">Benefit entities</span></span>

| <span data-ttu-id="6dd0c-108">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-108">Name</span></span> | <span data-ttu-id="6dd0c-109">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-110">Soodustuse arvutamise sagedus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="6dd0c-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="6dd0c-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="6dd0c-112">Soodustuse arvutamise sagedus makseperioodil</span><span class="sxs-lookup"><span data-stu-id="6dd0c-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="6dd0c-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="6dd0c-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="6dd0c-114">Soodustuse arvutamise määr</span><span class="sxs-lookup"><span data-stu-id="6dd0c-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="6dd0c-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="6dd0c-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="6dd0c-116">Soodustuse arvutamise määra üksikasjad</span><span class="sxs-lookup"><span data-stu-id="6dd0c-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="6dd0c-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="6dd0c-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="6dd0c-118">Soodustuse suvand</span><span class="sxs-lookup"><span data-stu-id="6dd0c-118">Benefit Option</span></span> | <span data-ttu-id="6dd0c-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="6dd0c-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="6dd0c-120">Soodustuse plaan</span><span class="sxs-lookup"><span data-stu-id="6dd0c-120">Benefit Plan</span></span> | <span data-ttu-id="6dd0c-121">cdm_benefitplan (kohandatud väljade toeks pole lubatud)</span><span class="sxs-lookup"><span data-stu-id="6dd0c-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="6dd0c-122">Hüvitise liik</span><span class="sxs-lookup"><span data-stu-id="6dd0c-122">Benefit Type</span></span> | <span data-ttu-id="6dd0c-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="6dd0c-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="6dd0c-124">Äriprotsessi ülesannete üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-124">Business process tasks entities</span></span>

| <span data-ttu-id="6dd0c-125">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-125">Name</span></span> | <span data-ttu-id="6dd0c-126">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-127">Äriprotsessi kalender</span><span class="sxs-lookup"><span data-stu-id="6dd0c-127">Business Process Calendar</span></span> | <span data-ttu-id="6dd0c-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="6dd0c-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="6dd0c-129">Äriprotsessi grupimäärang</span><span class="sxs-lookup"><span data-stu-id="6dd0c-129">Business Process Group Assignment</span></span> | <span data-ttu-id="6dd0c-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="6dd0c-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="6dd0c-131">Äriprotsessi teegi ülesandegrupp</span><span class="sxs-lookup"><span data-stu-id="6dd0c-131">Business Process Library Task Group</span></span> | <span data-ttu-id="6dd0c-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="6dd0c-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="6dd0c-133">Äriprotsessi etapp</span><span class="sxs-lookup"><span data-stu-id="6dd0c-133">Business Process Stage</span></span> | <span data-ttu-id="6dd0c-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="6dd0c-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="6dd0c-135">Kontroll-loendi malli päis</span><span class="sxs-lookup"><span data-stu-id="6dd0c-135">Checklist Template Header</span></span> | <span data-ttu-id="6dd0c-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="6dd0c-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="6dd0c-137">Kontroll-loendi malli ülesanne</span><span class="sxs-lookup"><span data-stu-id="6dd0c-137">Checklist Template Task</span></span> | <span data-ttu-id="6dd0c-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="6dd0c-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="6dd0c-139">Hüvitise üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-139">Compensation entities</span></span>

| <span data-ttu-id="6dd0c-140">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-140">Name</span></span> | <span data-ttu-id="6dd0c-141">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-142">Palga põhiplaan</span><span class="sxs-lookup"><span data-stu-id="6dd0c-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="6dd0c-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="6dd0c-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="6dd0c-144">Kogupalga tabel</span><span class="sxs-lookup"><span data-stu-id="6dd0c-144">Compensation Grid</span></span> | <span data-ttu-id="6dd0c-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="6dd0c-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="6dd0c-146">Hüvitustase</span><span class="sxs-lookup"><span data-stu-id="6dd0c-146">Compensation Level</span></span> | <span data-ttu-id="6dd0c-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="6dd0c-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="6dd0c-148">Palga tasumissagedus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="6dd0c-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="6dd0c-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="6dd0c-150">Palga võrdluspunkti seadistus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="6dd0c-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="6dd0c-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="6dd0c-152">Palga võrdluspunkti seadistuse rida</span><span class="sxs-lookup"><span data-stu-id="6dd0c-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="6dd0c-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="6dd0c-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="6dd0c-154">Hüvituspiirkond</span><span class="sxs-lookup"><span data-stu-id="6dd0c-154">Compensation Region</span></span> | <span data-ttu-id="6dd0c-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="6dd0c-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="6dd0c-156">Palga struktuur</span><span class="sxs-lookup"><span data-stu-id="6dd0c-156">Compensation Structure</span></span> | <span data-ttu-id="6dd0c-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="6dd0c-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="6dd0c-158">Muutuv hüvitisplaan</span><span class="sxs-lookup"><span data-stu-id="6dd0c-158">Compensation Variable Plan</span></span> | <span data-ttu-id="6dd0c-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="6dd0c-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="6dd0c-160">Muutuva hüvitisplaani tase</span><span class="sxs-lookup"><span data-stu-id="6dd0c-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="6dd0c-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="6dd0c-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="6dd0c-162">Muutuva hüvitisplaani tüüp</span><span class="sxs-lookup"><span data-stu-id="6dd0c-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="6dd0c-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="6dd0c-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="6dd0c-164">Põhipalga sündmus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-164">Fixed Compensation Event</span></span> | <span data-ttu-id="6dd0c-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="6dd0c-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="6dd0c-166">Pensionireegel</span><span class="sxs-lookup"><span data-stu-id="6dd0c-166">Vesting Rule</span></span> | <span data-ttu-id="6dd0c-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="6dd0c-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="6dd0c-168">Töötaja põhipalk</span><span class="sxs-lookup"><span data-stu-id="6dd0c-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="6dd0c-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="6dd0c-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="6dd0c-170">Organisatsiooni üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-170">Organization entities</span></span>

| <span data-ttu-id="6dd0c-171">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-171">Name</span></span> | <span data-ttu-id="6dd0c-172">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-173">Osakond</span><span class="sxs-lookup"><span data-stu-id="6dd0c-173">Department</span></span> | <span data-ttu-id="6dd0c-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="6dd0c-174">cdm_department</span></span> |
| <span data-ttu-id="6dd0c-175">Töösuhe</span><span class="sxs-lookup"><span data-stu-id="6dd0c-175">Employment</span></span> | <span data-ttu-id="6dd0c-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="6dd0c-176">cdm_employment</span></span> |
| <span data-ttu-id="6dd0c-177">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="6dd0c-177">Company</span></span> | <span data-ttu-id="6dd0c-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="6dd0c-178">cdm_company</span></span> |
| <span data-ttu-id="6dd0c-179">Amet</span><span class="sxs-lookup"><span data-stu-id="6dd0c-179">Job</span></span> | <span data-ttu-id="6dd0c-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="6dd0c-180">cdm_job</span></span> |
| <span data-ttu-id="6dd0c-181">Tööfunktsioon</span><span class="sxs-lookup"><span data-stu-id="6dd0c-181">Job Function</span></span> | <span data-ttu-id="6dd0c-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="6dd0c-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="6dd0c-183">Ametikoht</span><span class="sxs-lookup"><span data-stu-id="6dd0c-183">Job Position</span></span> | <span data-ttu-id="6dd0c-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="6dd0c-184">cdm_jobposition</span></span> |
| <span data-ttu-id="6dd0c-185">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="6dd0c-185">Position Type</span></span> | <span data-ttu-id="6dd0c-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="6dd0c-186">cdm_positiontype</span></span> |
| <span data-ttu-id="6dd0c-187">Ametikoha töötaja määramine</span><span class="sxs-lookup"><span data-stu-id="6dd0c-187">Position Worker Assignment</span></span> | <span data-ttu-id="6dd0c-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="6dd0c-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="6dd0c-189">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="6dd0c-189">Job Type</span></span> | <span data-ttu-id="6dd0c-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="6dd0c-190">cdm_jobtype</span></span> |
| <span data-ttu-id="6dd0c-191">Keel</span><span class="sxs-lookup"><span data-stu-id="6dd0c-191">Language</span></span> | <span data-ttu-id="6dd0c-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="6dd0c-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="6dd0c-193">Puhkuste ja puudumiste üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-193">Leave and absence entities</span></span>

| <span data-ttu-id="6dd0c-194">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-194">Name</span></span> | <span data-ttu-id="6dd0c-195">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-196">Puhkuse pangakanne</span><span class="sxs-lookup"><span data-stu-id="6dd0c-196">Leave Bank Transaction</span></span> | <span data-ttu-id="6dd0c-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="6dd0c-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="6dd0c-198">Puhkuse registreerimine</span><span class="sxs-lookup"><span data-stu-id="6dd0c-198">Leave Enrollment</span></span> | <span data-ttu-id="6dd0c-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="6dd0c-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="6dd0c-200">Puhkuseplaan</span><span class="sxs-lookup"><span data-stu-id="6dd0c-200">Leave Plan</span></span> | <span data-ttu-id="6dd0c-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="6dd0c-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="6dd0c-202">Puhkusetaotlus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-202">Leave Request</span></span> | <span data-ttu-id="6dd0c-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="6dd0c-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="6dd0c-204">Puhkuse taotluse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="6dd0c-204">Leave Request Detail</span></span> | <span data-ttu-id="6dd0c-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="6dd0c-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="6dd0c-206">Puhkuse tüüp</span><span class="sxs-lookup"><span data-stu-id="6dd0c-206">Leave Type</span></span> | <span data-ttu-id="6dd0c-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="6dd0c-207">cdm_leavetype</span></span> |
| <span data-ttu-id="6dd0c-208">Puhkusetüübi põhjusekood</span><span class="sxs-lookup"><span data-stu-id="6dd0c-208">Leave Type Reason Code</span></span> | <span data-ttu-id="6dd0c-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="6dd0c-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="6dd0c-210">Palgaolemid</span><span class="sxs-lookup"><span data-stu-id="6dd0c-210">Payroll entities</span></span>

| <span data-ttu-id="6dd0c-211">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-211">Name</span></span> | <span data-ttu-id="6dd0c-212">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-213">Palgatsükkel</span><span class="sxs-lookup"><span data-stu-id="6dd0c-213">Pay Cycle</span></span> | <span data-ttu-id="6dd0c-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="6dd0c-214">cdm_paycycle</span></span> |
| <span data-ttu-id="6dd0c-215">Makseperiood</span><span class="sxs-lookup"><span data-stu-id="6dd0c-215">Pay Period</span></span> | <span data-ttu-id="6dd0c-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="6dd0c-216">cdm_payperiod</span></span> |
| <span data-ttu-id="6dd0c-217">Palga tulukood</span><span class="sxs-lookup"><span data-stu-id="6dd0c-217">Payroll Earning Code</span></span> | <span data-ttu-id="6dd0c-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="6dd0c-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="6dd0c-219">Pangakonto väljamakse</span><span class="sxs-lookup"><span data-stu-id="6dd0c-219">Bank Account Disbursement</span></span> | <span data-ttu-id="6dd0c-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="6dd0c-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="6dd0c-221">Maksuregioon</span><span class="sxs-lookup"><span data-stu-id="6dd0c-221">Tax Region</span></span> | <span data-ttu-id="6dd0c-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="6dd0c-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="6dd0c-223">Töötaja üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-223">Worker entities</span></span>

| <span data-ttu-id="6dd0c-224">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-224">Name</span></span> | <span data-ttu-id="6dd0c-225">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-226">Töötaja</span><span class="sxs-lookup"><span data-stu-id="6dd0c-226">Worker</span></span> | <span data-ttu-id="6dd0c-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="6dd0c-227">cdm_worker</span></span> |
| <span data-ttu-id="6dd0c-228">Töötaja aadress</span><span class="sxs-lookup"><span data-stu-id="6dd0c-228">Worker Address</span></span> | <span data-ttu-id="6dd0c-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="6dd0c-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="6dd0c-230">Töötaja isikuteave</span><span class="sxs-lookup"><span data-stu-id="6dd0c-230">Worker Personal Detail</span></span> | <span data-ttu-id="6dd0c-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="6dd0c-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="6dd0c-232">Töötaja isiku ID-number</span><span class="sxs-lookup"><span data-stu-id="6dd0c-232">Worker Person Identification Number</span></span> | <span data-ttu-id="6dd0c-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="6dd0c-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="6dd0c-234">Töötaja isiku identifitseerimistüüp</span><span class="sxs-lookup"><span data-stu-id="6dd0c-234">Worker Person Identification Type</span></span> | <span data-ttu-id="6dd0c-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="6dd0c-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="6dd0c-236">Töökalender</span><span class="sxs-lookup"><span data-stu-id="6dd0c-236">Work Calendar</span></span> | <span data-ttu-id="6dd0c-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="6dd0c-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="6dd0c-238">Töökalendri päev</span><span class="sxs-lookup"><span data-stu-id="6dd0c-238">Work Calendar Day</span></span> | <span data-ttu-id="6dd0c-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="6dd0c-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="6dd0c-240">Töökalendri püha</span><span class="sxs-lookup"><span data-stu-id="6dd0c-240">Work Calendar Holiday</span></span> |<span data-ttu-id="6dd0c-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="6dd0c-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="6dd0c-242">Töökalendri puhkuse rida</span><span class="sxs-lookup"><span data-stu-id="6dd0c-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="6dd0c-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="6dd0c-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="6dd0c-244">Töökalendri ajaintervall</span><span class="sxs-lookup"><span data-stu-id="6dd0c-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="6dd0c-245">cdm_workcalendartimeinterval (kohandatud väljade toeks pole lubatud)</span><span class="sxs-lookup"><span data-stu-id="6dd0c-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="6dd0c-246">Töötaja pangakonto</span><span class="sxs-lookup"><span data-stu-id="6dd0c-246">Worker Bank Account</span></span> | <span data-ttu-id="6dd0c-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="6dd0c-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="6dd0c-248">Töötaja seadistuse üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-248">Worker setup entities</span></span>

| <span data-ttu-id="6dd0c-249">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-249">Name</span></span> | <span data-ttu-id="6dd0c-250">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-251">Veterani staatus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-251">Veteran Status</span></span> | <span data-ttu-id="6dd0c-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="6dd0c-253">Etniline päritolu</span><span class="sxs-lookup"><span data-stu-id="6dd0c-253">Ethnic Origin</span></span> | <span data-ttu-id="6dd0c-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="6dd0c-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="6dd0c-255">Põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="6dd0c-255">Reason Code</span></span> | <span data-ttu-id="6dd0c-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="6dd0c-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="6dd0c-257">Isikut ID väljastanud asutus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="6dd0c-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="6dd0c-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="6dd0c-259">Pädevuse üksused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-259">Competency entities</span></span>

| <span data-ttu-id="6dd0c-260">Nimi</span><span class="sxs-lookup"><span data-stu-id="6dd0c-260">Name</span></span> | <span data-ttu-id="6dd0c-261">Üksus</span><span class="sxs-lookup"><span data-stu-id="6dd0c-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="6dd0c-262">Oskuse tüüp</span><span class="sxs-lookup"><span data-stu-id="6dd0c-262">Skill Type</span></span> | <span data-ttu-id="6dd0c-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="6dd0c-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="6dd0c-264">Üksuse seose mudelid</span><span class="sxs-lookup"><span data-stu-id="6dd0c-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="6dd0c-265">Töötaja</span><span class="sxs-lookup"><span data-stu-id="6dd0c-265">Worker</span></span>

![Töötaja](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="6dd0c-267">Töö ja ametikoht</span><span class="sxs-lookup"><span data-stu-id="6dd0c-267">Job and Job Position</span></span>

![Töö ja ametikoht](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="6dd0c-269">Soodustused</span><span class="sxs-lookup"><span data-stu-id="6dd0c-269">Benefits</span></span>

![Soodustused](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="6dd0c-271">Kompensatsioon</span><span class="sxs-lookup"><span data-stu-id="6dd0c-271">Compensation</span></span>

![Kompensatsioon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="6dd0c-273">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="6dd0c-273">Leave</span></span>

![Lahkumine](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="6dd0c-275">Töökalender</span><span class="sxs-lookup"><span data-stu-id="6dd0c-275">Work Calendar</span></span>

![Töökalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="6dd0c-277">Vt ka</span><span class="sxs-lookup"><span data-stu-id="6dd0c-277">See also</span></span>

[<span data-ttu-id="6dd0c-278">Andme integratsioonitehnoloogia valimine</span><span class="sxs-lookup"><span data-stu-id="6dd0c-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="6dd0c-279">Common Data Service’i integratsiooni konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6dd0c-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)