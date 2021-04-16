---
title: Dataverse'i tabelid
description: Microsoft Dynamics 365 Human Resources kasutab teenust Dataverse, et lubada laiendatavus ja integreerimise stsenaariumid.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793605"
---
# <a name="dataverse-tables"></a><span data-ttu-id="9933d-103">Dataverse'i tabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9933d-104">Microsoft Dynamics 365 Human Resources kasutab teenust Dataverse, et lubada laiendatavus ja integreerimise stsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="9933d-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="9933d-105">Human Resourcesi olemid vastavad Dataverse'i tabelitele.</span><span class="sxs-lookup"><span data-stu-id="9933d-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="9933d-106">Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="9933d-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="9933d-107">Järgmised Dataverse'i tabelid on saadaval Human Resources'i olemite põhjal.</span><span class="sxs-lookup"><span data-stu-id="9933d-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="9933d-108">Soodustustabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-108">Benefit tables</span></span>

| <span data-ttu-id="9933d-109">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-109">Name</span></span> | <span data-ttu-id="9933d-110">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-111">Hüvitise arvutamise sagedus</span><span class="sxs-lookup"><span data-stu-id="9933d-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="9933d-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="9933d-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="9933d-113">Soodustuse arvutamise sagedus makseperioodil</span><span class="sxs-lookup"><span data-stu-id="9933d-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="9933d-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="9933d-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="9933d-115">Soodustuse arvutamise määr</span><span class="sxs-lookup"><span data-stu-id="9933d-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="9933d-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="9933d-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="9933d-117">Soodustuse arvutamise määra üksikasjad</span><span class="sxs-lookup"><span data-stu-id="9933d-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="9933d-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="9933d-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="9933d-119">Soodustuse suvand</span><span class="sxs-lookup"><span data-stu-id="9933d-119">Benefit Option</span></span> | <span data-ttu-id="9933d-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="9933d-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="9933d-121">Soodustuse plaan</span><span class="sxs-lookup"><span data-stu-id="9933d-121">Benefit Plan</span></span> | <span data-ttu-id="9933d-122">cdm_benefitplan (kohandatud väljade toeks pole lubatud)</span><span class="sxs-lookup"><span data-stu-id="9933d-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="9933d-123">Hüvitise liik</span><span class="sxs-lookup"><span data-stu-id="9933d-123">Benefit Type</span></span> | <span data-ttu-id="9933d-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="9933d-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="9933d-125">Äriprotsessi ülesannete tabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-125">Business process tasks tables</span></span>

| <span data-ttu-id="9933d-126">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-126">Name</span></span> | <span data-ttu-id="9933d-127">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-128">Äriprotsessi kalender</span><span class="sxs-lookup"><span data-stu-id="9933d-128">Business Process Calendar</span></span> | <span data-ttu-id="9933d-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="9933d-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="9933d-130">Äriprotsessi grupimäärang</span><span class="sxs-lookup"><span data-stu-id="9933d-130">Business Process Group Assignment</span></span> | <span data-ttu-id="9933d-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="9933d-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="9933d-132">Äriprotsessi teegi ülesandegrupp</span><span class="sxs-lookup"><span data-stu-id="9933d-132">Business Process Library Task Group</span></span> | <span data-ttu-id="9933d-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="9933d-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="9933d-134">Äriprotsessi etapp</span><span class="sxs-lookup"><span data-stu-id="9933d-134">Business Process Stage</span></span> | <span data-ttu-id="9933d-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="9933d-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="9933d-136">Kontroll-loendi malli päis</span><span class="sxs-lookup"><span data-stu-id="9933d-136">Checklist Template Header</span></span> | <span data-ttu-id="9933d-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="9933d-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="9933d-138">Kontroll-loendi malli ülesanne</span><span class="sxs-lookup"><span data-stu-id="9933d-138">Checklist Template Task</span></span> | <span data-ttu-id="9933d-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="9933d-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="9933d-140">Hüvitise tabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-140">Compensation tables</span></span>

| <span data-ttu-id="9933d-141">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-141">Name</span></span> | <span data-ttu-id="9933d-142">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-143">Tasu fikseeritud plaan</span><span class="sxs-lookup"><span data-stu-id="9933d-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="9933d-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="9933d-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="9933d-145">Kogupalga tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-145">Compensation Grid</span></span> | <span data-ttu-id="9933d-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="9933d-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="9933d-147">Hüvitustase</span><span class="sxs-lookup"><span data-stu-id="9933d-147">Compensation Level</span></span> | <span data-ttu-id="9933d-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="9933d-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="9933d-149">Palga tasumissagedus</span><span class="sxs-lookup"><span data-stu-id="9933d-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="9933d-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="9933d-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="9933d-151">Palga võrdluspunkti seadistus</span><span class="sxs-lookup"><span data-stu-id="9933d-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="9933d-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="9933d-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="9933d-153">Palga võrdluspunkti seadistuse rida</span><span class="sxs-lookup"><span data-stu-id="9933d-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="9933d-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="9933d-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="9933d-155">Hüvituspiirkond</span><span class="sxs-lookup"><span data-stu-id="9933d-155">Compensation Region</span></span> | <span data-ttu-id="9933d-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="9933d-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="9933d-157">Palga struktuur</span><span class="sxs-lookup"><span data-stu-id="9933d-157">Compensation Structure</span></span> | <span data-ttu-id="9933d-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="9933d-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="9933d-159">Muutuv hüvitisplaan</span><span class="sxs-lookup"><span data-stu-id="9933d-159">Compensation Variable Plan</span></span> | <span data-ttu-id="9933d-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="9933d-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="9933d-161">Muutuva hüvitisplaani tase</span><span class="sxs-lookup"><span data-stu-id="9933d-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="9933d-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="9933d-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="9933d-163">Muutuva hüvitisplaani tüüp</span><span class="sxs-lookup"><span data-stu-id="9933d-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="9933d-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="9933d-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="9933d-165">Põhipalga sündmus</span><span class="sxs-lookup"><span data-stu-id="9933d-165">Fixed Compensation Event</span></span> | <span data-ttu-id="9933d-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="9933d-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="9933d-167">Pensionireegel</span><span class="sxs-lookup"><span data-stu-id="9933d-167">Vesting Rule</span></span> | <span data-ttu-id="9933d-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="9933d-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="9933d-169">Töötaja põhipalk</span><span class="sxs-lookup"><span data-stu-id="9933d-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="9933d-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="9933d-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="9933d-171">Organisatsiooni tabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-171">Organization tables</span></span>

| <span data-ttu-id="9933d-172">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-172">Name</span></span> | <span data-ttu-id="9933d-173">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-174">Osakond</span><span class="sxs-lookup"><span data-stu-id="9933d-174">Department</span></span> | <span data-ttu-id="9933d-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="9933d-175">cdm_department</span></span> |
| <span data-ttu-id="9933d-176">Töösuhe</span><span class="sxs-lookup"><span data-stu-id="9933d-176">Employment</span></span> | <span data-ttu-id="9933d-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="9933d-177">cdm_employment</span></span> |
| <span data-ttu-id="9933d-178">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="9933d-178">Company</span></span> | <span data-ttu-id="9933d-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="9933d-179">cdm_company</span></span> |
| <span data-ttu-id="9933d-180">Amet</span><span class="sxs-lookup"><span data-stu-id="9933d-180">Job</span></span> | <span data-ttu-id="9933d-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="9933d-181">cdm_job</span></span> |
| <span data-ttu-id="9933d-182">Tööfunktsioon</span><span class="sxs-lookup"><span data-stu-id="9933d-182">Job Function</span></span> | <span data-ttu-id="9933d-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="9933d-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="9933d-184">Ametikoht</span><span class="sxs-lookup"><span data-stu-id="9933d-184">Job Position</span></span> | <span data-ttu-id="9933d-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="9933d-185">cdm_jobposition</span></span> |
| <span data-ttu-id="9933d-186">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="9933d-186">Position Type</span></span> | <span data-ttu-id="9933d-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="9933d-187">cdm_positiontype</span></span> |
| <span data-ttu-id="9933d-188">Ametikoha töötaja määramine</span><span class="sxs-lookup"><span data-stu-id="9933d-188">Position Worker Assignment</span></span> | <span data-ttu-id="9933d-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="9933d-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="9933d-190">Ametikoha dimensioon</span><span class="sxs-lookup"><span data-stu-id="9933d-190">Job Position Dimension</span></span> | <span data-ttu-id="9933d-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="9933d-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="9933d-192">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="9933d-192">Job Type</span></span> | <span data-ttu-id="9933d-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="9933d-193">cdm_jobtype</span></span> |
| <span data-ttu-id="9933d-194">Keel</span><span class="sxs-lookup"><span data-stu-id="9933d-194">Language</span></span> | <span data-ttu-id="9933d-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="9933d-195">cdm_language</span></span> |
| <span data-ttu-id="9933d-196">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="9933d-196">Title</span></span> | <span data-ttu-id="9933d-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="9933d-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="9933d-198">Üksuste **Ametikoha tüüp** **Töötaja ametikoha määramine** ja **Töölevõtt** finantsdimensioonid pakuvad ühesuunalist integratsiooni Dataverse'iga.</span><span class="sxs-lookup"><span data-stu-id="9933d-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="9933d-199">Finantsdimensioonide värskendusi ei saa praegu sünkroonida Dataverse'ist Human Resourcesisse.</span><span class="sxs-lookup"><span data-stu-id="9933d-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="9933d-200">Puhkuste ja puudumiste tabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-200">Leave and absence tables</span></span>

| <span data-ttu-id="9933d-201">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-201">Name</span></span> | <span data-ttu-id="9933d-202">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-203">Puhkuste panga kanne</span><span class="sxs-lookup"><span data-stu-id="9933d-203">Leave Bank Transaction</span></span> | <span data-ttu-id="9933d-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="9933d-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="9933d-205">Puhkuste registreerimine</span><span class="sxs-lookup"><span data-stu-id="9933d-205">Leave Enrollment</span></span> | <span data-ttu-id="9933d-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="9933d-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="9933d-207">Puhkuseplaan</span><span class="sxs-lookup"><span data-stu-id="9933d-207">Leave Plan</span></span> | <span data-ttu-id="9933d-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="9933d-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="9933d-209">Puhkusetaotlus</span><span class="sxs-lookup"><span data-stu-id="9933d-209">Leave Request</span></span> | <span data-ttu-id="9933d-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="9933d-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="9933d-211">Puhkuse taotluse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="9933d-211">Leave Request Detail</span></span> | <span data-ttu-id="9933d-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="9933d-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="9933d-213">Puhkuse tüüp</span><span class="sxs-lookup"><span data-stu-id="9933d-213">Leave Type</span></span> | <span data-ttu-id="9933d-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="9933d-214">cdm_leavetype</span></span> |
| <span data-ttu-id="9933d-215">Puhkusetüübi põhjusekood</span><span class="sxs-lookup"><span data-stu-id="9933d-215">Leave Type Reason Code</span></span> | <span data-ttu-id="9933d-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="9933d-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="9933d-217">Palgatabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-217">Payroll tables</span></span>

| <span data-ttu-id="9933d-218">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-218">Name</span></span> | <span data-ttu-id="9933d-219">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-220">Palgatsükkel</span><span class="sxs-lookup"><span data-stu-id="9933d-220">Pay Cycle</span></span> | <span data-ttu-id="9933d-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="9933d-221">cdm_paycycle</span></span> |
| <span data-ttu-id="9933d-222">Makseperiood</span><span class="sxs-lookup"><span data-stu-id="9933d-222">Pay Period</span></span> | <span data-ttu-id="9933d-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="9933d-223">cdm_payperiod</span></span> |
| <span data-ttu-id="9933d-224">Palga tulukood</span><span class="sxs-lookup"><span data-stu-id="9933d-224">Payroll Earning Code</span></span> | <span data-ttu-id="9933d-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="9933d-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="9933d-226">Pangakonto väljamakse</span><span class="sxs-lookup"><span data-stu-id="9933d-226">Bank Account Disbursement</span></span> | <span data-ttu-id="9933d-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="9933d-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="9933d-228">Maksuregioon</span><span class="sxs-lookup"><span data-stu-id="9933d-228">Tax Region</span></span> | <span data-ttu-id="9933d-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="9933d-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="9933d-230">Töötajatabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-230">Worker tables</span></span>

| <span data-ttu-id="9933d-231">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-231">Name</span></span> | <span data-ttu-id="9933d-232">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-233">Töötaja</span><span class="sxs-lookup"><span data-stu-id="9933d-233">Worker</span></span> | <span data-ttu-id="9933d-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="9933d-234">cdm_worker</span></span> |
| <span data-ttu-id="9933d-235">Töötaja aadress</span><span class="sxs-lookup"><span data-stu-id="9933d-235">Worker Address</span></span> | <span data-ttu-id="9933d-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="9933d-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="9933d-237">Töötaja isikuteave</span><span class="sxs-lookup"><span data-stu-id="9933d-237">Worker Personal Detail</span></span> | <span data-ttu-id="9933d-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="9933d-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="9933d-239">Töötaja isiku ID-number</span><span class="sxs-lookup"><span data-stu-id="9933d-239">Worker Person Identification Number</span></span> | <span data-ttu-id="9933d-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="9933d-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="9933d-241">Töötaja isiku identifitseerimistüüp</span><span class="sxs-lookup"><span data-stu-id="9933d-241">Worker Person Identification Type</span></span> | <span data-ttu-id="9933d-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="9933d-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="9933d-243">Töökalender</span><span class="sxs-lookup"><span data-stu-id="9933d-243">Work Calendar</span></span> | <span data-ttu-id="9933d-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="9933d-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="9933d-245">Töökalendri päev</span><span class="sxs-lookup"><span data-stu-id="9933d-245">Work Calendar Day</span></span> | <span data-ttu-id="9933d-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="9933d-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="9933d-247">Töökalendri püha</span><span class="sxs-lookup"><span data-stu-id="9933d-247">Work Calendar Holiday</span></span> |<span data-ttu-id="9933d-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="9933d-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="9933d-249">Töökalendri puhkuse rida</span><span class="sxs-lookup"><span data-stu-id="9933d-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="9933d-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="9933d-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="9933d-251">Töökalendri ajaintervall</span><span class="sxs-lookup"><span data-stu-id="9933d-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="9933d-252">cdm_workcalendartimeinterval (kohandatud väljade toeks pole lubatud)</span><span class="sxs-lookup"><span data-stu-id="9933d-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="9933d-253">Töötaja pangakonto</span><span class="sxs-lookup"><span data-stu-id="9933d-253">Worker Bank Account</span></span> | <span data-ttu-id="9933d-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="9933d-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="9933d-255">Töötaja seadistamise tabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-255">Worker setup tables</span></span>

| <span data-ttu-id="9933d-256">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-256">Name</span></span> | <span data-ttu-id="9933d-257">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-258">Veterani olek</span><span class="sxs-lookup"><span data-stu-id="9933d-258">Veteran Status</span></span> | <span data-ttu-id="9933d-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="9933d-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="9933d-260">Etniline päritolu</span><span class="sxs-lookup"><span data-stu-id="9933d-260">Ethnic Origin</span></span> | <span data-ttu-id="9933d-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="9933d-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="9933d-262">Põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="9933d-262">Reason Code</span></span> | <span data-ttu-id="9933d-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="9933d-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="9933d-264">Isiku ID-d väljaandev asutus</span><span class="sxs-lookup"><span data-stu-id="9933d-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="9933d-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="9933d-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="9933d-266">Kompetentsitabelid</span><span class="sxs-lookup"><span data-stu-id="9933d-266">Competency tables</span></span>

| <span data-ttu-id="9933d-267">Nimi</span><span class="sxs-lookup"><span data-stu-id="9933d-267">Name</span></span> | <span data-ttu-id="9933d-268">Tabel</span><span class="sxs-lookup"><span data-stu-id="9933d-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9933d-269">Oskuse tüüp</span><span class="sxs-lookup"><span data-stu-id="9933d-269">Skill Type</span></span> | <span data-ttu-id="9933d-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="9933d-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="9933d-271">Tabelite seose mudelid</span><span class="sxs-lookup"><span data-stu-id="9933d-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="9933d-272">Töötaja</span><span class="sxs-lookup"><span data-stu-id="9933d-272">Worker</span></span>

![Töötaja](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="9933d-274">Töö ja ametikoht</span><span class="sxs-lookup"><span data-stu-id="9933d-274">Job and Job Position</span></span>

![Töö ja ametikoht](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="9933d-276">Soodustused</span><span class="sxs-lookup"><span data-stu-id="9933d-276">Benefits</span></span>

![Soodustused](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="9933d-278">Kompensatsioon</span><span class="sxs-lookup"><span data-stu-id="9933d-278">Compensation</span></span>

![Kompensatsioon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="9933d-280">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="9933d-280">Leave</span></span>

![Lahkumine](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="9933d-282">Töökalender</span><span class="sxs-lookup"><span data-stu-id="9933d-282">Work Calendar</span></span>

![Töökalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="9933d-284">Vt ka</span><span class="sxs-lookup"><span data-stu-id="9933d-284">See also</span></span>

[<span data-ttu-id="9933d-285">Andme integratsioonitehnoloogia valimine</span><span class="sxs-lookup"><span data-stu-id="9933d-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="9933d-286">Dataverse’i integratsiooni konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9933d-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="9933d-287">Dataverse'i virtuaalsete tabelite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9933d-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="9933d-288">Human Resourcesi virtuaaltabelite KKK</span><span class="sxs-lookup"><span data-stu-id="9933d-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="9933d-289">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="9933d-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="9933d-290">Terminoloogia uuendused</span><span class="sxs-lookup"><span data-stu-id="9933d-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]