---
title: "Tööde loomine, kinnitamine ja sisestamine Attractis"
description: "Selles teemas kirjeldatakse Attarcti töö elemente. Lisaks selgitatakse, kuidas tööd luua."
author: josaw
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: af945042c150fff1a95cdb046f2a712cb2c2c061
ms.contentlocale: et-ee
ms.lasthandoff: 10/24/2018

---

# <a name="create-approve-and-post-jobs-in-attract"></a><span data-ttu-id="1fd3e-104">Tööde loomine, kinnitamine ja sisestamine Attractis</span><span class="sxs-lookup"><span data-stu-id="1fd3e-104">Create, approve, and post jobs in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1fd3e-105">Selles teemas kirjeldatakse töö elemente rakenduses Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-105">This topic describes the elements of a job in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="1fd3e-106">Lisaks selgitatakse, kuidas tööd luua.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-106">It also explains how to create a job.</span></span>

## <a name="job-creation"></a><span data-ttu-id="1fd3e-107">Töö loomine</span><span class="sxs-lookup"><span data-stu-id="1fd3e-107">Job creation</span></span>

<span data-ttu-id="1fd3e-108">Töid saavad luua administraatorid, värbajad ja personalijuhid.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-108">Admins, recruiters, and hiring managers can create jobs.</span></span> <span data-ttu-id="1fd3e-109">Töö loomisel palutakse teil valida oma roll protsessis: personalijuht või värbaja.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-109">When you create a job, you're prompted to select your role in the process: hiring manager or recruiter.</span></span> <span data-ttu-id="1fd3e-110">Kui olete rolli valinud, palutakse teil valida protsessi mall.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-110">After you select a role, you're prompted to select a process template.</span></span> <span data-ttu-id="1fd3e-111">Kui valite **Jäta vahele**, kasutatakse vaikemalli.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-111">If you select **Skip**, the default template is used.</span></span> <span data-ttu-id="1fd3e-112">Protsessimallide kohta leiate lisateavet artiklist [Protsessimalli loomine Attractis](./process-templates-attract.md).</span><span class="sxs-lookup"><span data-stu-id="1fd3e-112">For more information about process templates, see [Create a process template in Attract](./process-templates-attract.md).</span></span>

<span data-ttu-id="1fd3e-113">Attracti tööl on töö üksikasjad, värbamistöörühm, värbamisprotsess, töösisestused ja analüütika.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-113">A job in Attract has job details, a hiring team, a hiring process, job postings, and analytics.</span></span>

## <a name="job-details"></a><span data-ttu-id="1fd3e-114">Töö üksikasjad</span><span class="sxs-lookup"><span data-stu-id="1fd3e-114">Job details</span></span>

<span data-ttu-id="1fd3e-115">Vahekaart **Töö üksikasjad** sisaldab üksikasju töökohustuste ja atribuutide kohta.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-115">The **Job details** tab contains details about the job's responsibilities and attributes.</span></span> <span data-ttu-id="1fd3e-116">Ametinimetuse, töö kirjelduse ja töö asukoha väljad on nõutavad.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-116">The fields for the job title, job description, and job location are required.</span></span> <span data-ttu-id="1fd3e-117">Teised väljad pole kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-117">The other fields are optional.</span></span>

<span data-ttu-id="1fd3e-118">Välja **Vabade kohtade arv** vaikeväärtuseks **1**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-118">By default, the **Number of openings** field is set to **1**.</span></span> <span data-ttu-id="1fd3e-119">Kuid te saate selle väärtust muuta.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-119">However, you can change the value.</span></span> <span data-ttu-id="1fd3e-120">Kui tööle on pakkumine koostatud, vähendatakse välja **Vabade kohtade arv** väärtust.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-120">When an offer has been prepared for a job, the value of the **Number of openings available** field is decremented.</span></span>

<span data-ttu-id="1fd3e-121">Kui halduskeskuses on ametikoha haldamine sisse lülitatud, on saadaval otsing **Värskenda ametikohti**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-121">If position management has been turned on in the Admin Center, the **Update positions** lookup is available.</span></span> <span data-ttu-id="1fd3e-122">See otsing loeb teenuse Common Data Service for Apps JobPosition üksust ja annab vastuseks loendi ametikohtadest, mida antud tööle saab valida.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-122">This lookup reads the JobPosition entity in Common Data Service for Apps and returns a list of positions that can be selected for the job.</span></span> <span data-ttu-id="1fd3e-123">Kui valitud ametikohtade arv ületab vabade ametikohtade arvu, kuvatakse hoiatus.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-123">If the number of positions that you select exceeds the number of open positions, you receive a warning.</span></span> <span data-ttu-id="1fd3e-124">Samuti kuvatakse hoiatus, kui ametikohta kasutatakse mitme tööga.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-124">You also receive a warning if a position is used on multiple jobs.</span></span>

> [!NOTE]
> <span data-ttu-id="1fd3e-125">Ametikoha haldus on saadaval tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-125">Position management is available with the Comprehensive Hiring Add-on.</span></span>

<span data-ttu-id="1fd3e-126">Olenevalt värbamisprotsessi pakkumise tegevuse sätetest, saab ametikoha numbrit pakkumises kasutada kaks korda.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-126">Depending on the settings in the Offer activity of the hiring process, a position number can be used twice in an offer.</span></span> <span data-ttu-id="1fd3e-127">Lisateavet vt teemast [Värbamisprotsess](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="1fd3e-127">For more information, see [Hiring process](./activities-attract.md).</span></span>

<span data-ttu-id="1fd3e-128">Attract sisaldav vaikimisi **Oskuste** komplekti.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-128">Attract includes a default set of **Skills**.</span></span> <span data-ttu-id="1fd3e-129">Need oskused kuvatakse trükkimisel soovitustena.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-129">These skills appear as suggestions as you type.</span></span> <span data-ttu-id="1fd3e-130">Saate oskusi juurde lisada, sisestades uue oskuse teksti väljale ja vajutades sisestusklahvi.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-130">You can add more skills by entering the new skill text in the field and then pressing Enter.</span></span>

<span data-ttu-id="1fd3e-131">Attract sisaldav vaikimisi **Tööfunktsioonide** komplekti.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-131">Attract includes a default set of **Job functions**.</span></span> <span data-ttu-id="1fd3e-132">Saate kuni kolm tööfunktsiooni juurde lisada, sisestades uue tööfunktsiooni väljale ja vajutades sisestusklahvi.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-132">You can add up to three more job functions by entering the new job function in the field and then pressing Enter.</span></span>

<span data-ttu-id="1fd3e-133">Attract sisaldav vaikimisi **Ettevõtte valdkondade** komplekti.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-133">Attract includes a default set of **Company industry**.</span></span> <span data-ttu-id="1fd3e-134">Saate kuni kolm ettevõtte valdkonda juurde lisada, sisestades uue ettevõtte valdkonna väljale ja vajutades sisestusklahvi.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-134">You can add up to three more company industries by entering the new company industry in the field and then pressing Enter.</span></span>

## <a name="hiring-team"></a><span data-ttu-id="1fd3e-135">Värbamistöörühm</span><span class="sxs-lookup"><span data-stu-id="1fd3e-135">Hiring team</span></span>

<span data-ttu-id="1fd3e-136">Vahekaart **Värbamistöörühm** sisaldab tööga seotud isikute loendit.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-136">The **Hiring team** tab contains the list of individuals who will be involved in the job.</span></span> <span data-ttu-id="1fd3e-137">Kasutajate lisamisel värbamistöörühma peab neile määrama rolli värbamistöörühmas.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-137">When users are added to a hiring team, they must be assigned a role on the hiring team.</span></span> <span data-ttu-id="1fd3e-138">Roll määrab, millistele andmetele kasutajatel juurdepääs on ja milliseid teavitusi nad saavad.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-138">The role determines the data that the users have access to and the notifications that they receive.</span></span> <span data-ttu-id="1fd3e-139">Rollid, mida saab valida, on **Värbaja**, **Personalijuht**, **Delegaat** ja **Intervjueerija**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-139">The roles that can be selected are **Recruiter**, **Hiring manager**, **Delegate**, and **Interviewer**.</span></span> <span data-ttu-id="1fd3e-140">Lisainfot rolli privileegide kohta leiate dokumendist "Rollihaldus".</span><span class="sxs-lookup"><span data-stu-id="1fd3e-140">For more information about role privileges, see the "Role management" document.</span></span> <span data-ttu-id="1fd3e-141">Värbajad ja personalijuhid võivad määrata ühe või rohkem delegaate nende nimel töötama.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-141">Recruiters and hiring managers can appoint one or more delegates to work on their behalf.</span></span> <span data-ttu-id="1fd3e-142">Lisainfot delegaatide kohta leiate artiklist [Turvalisus ja rollihaldus Attractis](./security-attract.md).</span><span class="sxs-lookup"><span data-stu-id="1fd3e-142">For more information about delegates, see [Security and role management in Attract](./security-attract.md).</span></span>

<span data-ttu-id="1fd3e-143">Värbamistöörühma saab pärast töö aktiveerimist värskendada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-143">The hiring team can be updated after the job is activated.</span></span>

## <a name="process"></a><span data-ttu-id="1fd3e-144">Töötlemine</span><span class="sxs-lookup"><span data-stu-id="1fd3e-144">Process</span></span>

<span data-ttu-id="1fd3e-145">Värbamisprotsessi vaiketeave põhineb töö loomisel valitud protsessimallil.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-145">Default information about the hiring process is based on the process template that was selected when the job was created.</span></span> <span data-ttu-id="1fd3e-146">Kui sel ajal kindlat malli ei valitud, kasutatakse vaikemalli.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-146">If a specific template wasn't selected at that time, the default template is used.</span></span> <span data-ttu-id="1fd3e-147">Kui määratlete värbamisprotsessi, saate lisada või eemaldada erinevaid etappe, välja arvatud potentsiaalselt sobiva kandidaadi, avalduse ja pakkumise etappe.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-147">When you define the hiring process, you can add or remove various stages, except the Prospect, Application, and Offer stages.</span></span> <span data-ttu-id="1fd3e-148">Kuigi potentsiaalselt sobiva kandidaadi etappi ei saa eemaldada, võib selle välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-148">Although the Prospect stage can't be removed, it can be turned off.</span></span> <span data-ttu-id="1fd3e-149">Igas etapis saate lisada või eemaldada ühe või mitu eelmääratletud tegevust.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-149">Within each stage, you can add or remove one or more predefined activities.</span></span>

<span data-ttu-id="1fd3e-150">Lisainfot tegevuste kohta, mida värbamisprotsessile lisada saab, leiate artiklist [Värbamisprotsessi tegevused Attractis](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="1fd3e-150">For more information about activities that can be added to the hiring process, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1fd3e-151">Värbamisprotsessi saab pärast töö aktiveerimist värskendada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-151">The process hiring can't be updated after a job is activated.</span></span>

## <a name="postings"></a><span data-ttu-id="1fd3e-152">Sisestamised</span><span class="sxs-lookup"><span data-stu-id="1fd3e-152">Postings</span></span>

<span data-ttu-id="1fd3e-153">Pärast töö aktiveerimist saab selle sisestada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-153">After a job is activated, it can be posted.</span></span> <span data-ttu-id="1fd3e-154">Ainult värbajad ja administraatorid saavad töid sisestada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-154">Only recruiters and admins can post jobs.</span></span> <span data-ttu-id="1fd3e-155">Töö saab sisestada kas rakendusse Talent Careers (Microsoft Dynamics 365 for Talent karjäärisait) või LinkedIni.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-155">The job can be posted to either Talent Careers (a Microsoft Dynamics 365 for Talent career site) or LinkedIn.</span></span> <span data-ttu-id="1fd3e-156">Attracti meeskond töötab pidevalt töökuulutuste vahendajatega koostöös.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-156">The Attract team continually works to partner with job board aggregators.</span></span> <span data-ttu-id="1fd3e-157">Seetõttu laieneb see loend aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-157">Therefore, this list will expand over time.</span></span>

<span data-ttu-id="1fd3e-158">Töösisestuste kohta lisainfo saamiseks vt [Karjäärisaidi funktsionaalsus Attractis](./career-site.md).</span><span class="sxs-lookup"><span data-stu-id="1fd3e-158">For more information about job postings, see [Career site functionality in Attract](./career-site.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1fd3e-159">Töösisestuste funktsionaalsus on saadaval ainult tervikliku värbamise lisandmooduliga Attractile.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-159">The job posting functionality is available only with the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="activate"></a><span data-ttu-id="1fd3e-160">Aktiveeri</span><span class="sxs-lookup"><span data-stu-id="1fd3e-160">Activate</span></span>

<span data-ttu-id="1fd3e-161">Pärast seda, kui töö on aktiveeritud, saab sellele potentsiaalselt sobivaid kandidaate ja kandidaate lisada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-161">After a job is activated, it can be posted, and prospects and applicants can be added to it.</span></span> <span data-ttu-id="1fd3e-162">Tööle potentsiaalselt sobivate kandidaatide lisamise valik on määratud värbamisprotsessi potentsiaalselt sobiva kandidaadi tegevuses.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-162">The option to add prospects to a job is set in the Prospect activity in the hiring process.</span></span>

> [!NOTE]
> <span data-ttu-id="1fd3e-163">Värbamisprotsessi saab pärast töö aktiveerimist värskendada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-163">The process hiring can't be updated after a job is activated.</span></span>

## <a name="prospects-and-applicants"></a><span data-ttu-id="1fd3e-164">Potentsiaalselt sobivad kandidaadid ja kandidaadid</span><span class="sxs-lookup"><span data-stu-id="1fd3e-164">Prospects and applicants</span></span>

<span data-ttu-id="1fd3e-165">Tööle potentsiaalselt sobivate kandidaatide lisamise valik on määratud värbamisprotsessis [Potentsiaalselt sobiva kandidaadi tegevus](./activities-attract.md#prospect-activity) all.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-165">The option to add prospects to a job is set in the [Prospect activity](./activities-attract.md#prospect-activity) in the hiring process.</span></span> <span data-ttu-id="1fd3e-166">See valik peaks olema enne töö aktiveerimist määratud..</span><span class="sxs-lookup"><span data-stu-id="1fd3e-166">This option should be set before you activate the job.</span></span> <span data-ttu-id="1fd3e-167">Pärast seda, kui töö on aktiveeritud, saab sellele potentsiaalselt sobivaid kandidaate ja kandidaate lisada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-167">After a job is activated, prospects and applicants can be added to it.</span></span>

## <a name="approvals"></a><span data-ttu-id="1fd3e-168">Kinnitused</span><span class="sxs-lookup"><span data-stu-id="1fd3e-168">Approvals</span></span>

<span data-ttu-id="1fd3e-169">Attracti töid saab kinnitamiseks esitada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-169">Attract jobs can be submitted for approval.</span></span> <span data-ttu-id="1fd3e-170">Kõik tööd ei vaja kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-170">Not all jobs require approval.</span></span> <span data-ttu-id="1fd3e-171">Nõue määratakse malli tasandilt.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-171">The requirement is set at the template level.</span></span> <span data-ttu-id="1fd3e-172">Vaikimisi on mallil kinnitused välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-172">By default, approvals are turned off on the template.</span></span> <span data-ttu-id="1fd3e-173">Kinnituste seadistamiseks minge protsessimallile ja määrake väli **Kinnitamine** vaikeväärtuseks.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-173">To set up approvals, go to a process template, and set the **Approval** field to Default.</span></span> <span data-ttu-id="1fd3e-174">Siis valige tööd luues see mall.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-174">Then select that template when you create the job.</span></span>

<span data-ttu-id="1fd3e-175">Pärast töö salvestamist saab selle kinnitamiseks esitada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-175">After a job is saved, it can be submitted for approval.</span></span> <span data-ttu-id="1fd3e-176">Järgnev tabel loetleb kinnitamist kasutava dokumendi olekut.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-176">The following table lists the statuses of a document that uses approvals.</span></span>

| <span data-ttu-id="1fd3e-177">Olek</span><span class="sxs-lookup"><span data-stu-id="1fd3e-177">Status</span></span>   | <span data-ttu-id="1fd3e-178">Riik</span><span class="sxs-lookup"><span data-stu-id="1fd3e-178">State</span></span>                                                               |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="1fd3e-179">Mustand</span><span class="sxs-lookup"><span data-stu-id="1fd3e-179">Draft</span></span>    | <span data-ttu-id="1fd3e-180">Töö on salvestatud, kuid see pole töövoogu esitatud.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-180">The job has been saved, but it hasn't been submitted to a workflow.</span></span> |
| <span data-ttu-id="1fd3e-181">Ootel</span><span class="sxs-lookup"><span data-stu-id="1fd3e-181">Pending</span></span>  | <span data-ttu-id="1fd3e-182">Töö on edastatud kinnitajatele.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-182">The job has been submitted to approvers.</span></span>                            |
| <span data-ttu-id="1fd3e-183">Kinnitatud</span><span class="sxs-lookup"><span data-stu-id="1fd3e-183">Approved</span></span> | <span data-ttu-id="1fd3e-184">Töö on kinnitatud, kuid see ei ole aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-184">The job has been approved, but it hasn't been activated.</span></span>            |
| <span data-ttu-id="1fd3e-185">Tagasi lükatud</span><span class="sxs-lookup"><span data-stu-id="1fd3e-185">Rejected</span></span> | <span data-ttu-id="1fd3e-186">Töö on tagasi lükatud ja seda ei saa aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-186">The job has been rejected, and it can't be activated.</span></span>               |
| <span data-ttu-id="1fd3e-187">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="1fd3e-187">Active</span></span>   | <span data-ttu-id="1fd3e-188">Töö on kinnitatud ja aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-188">The job has been approved and activated.</span></span>                            |

<span data-ttu-id="1fd3e-189">Tööde loendis, saate filtreerida tööde olekuid.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-189">In the job list, you can filter on the job statuses.</span></span>

<span data-ttu-id="1fd3e-190">Kinnitusi saab saata ettevõttes mistahes Microsoft Azure Active Directory (Azure AD) kasutajale.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-190">Approvals can be sent to any Microsoft Azure Active Directory (Azure AD) user in the company.</span></span> <span data-ttu-id="1fd3e-191">Kinnitused saadakse paralleelselt kõigile inimestele, kes on kinnitajate loendis.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-191">The approvals are sent in parallel to all the people who are listed as approvers.</span></span> <span data-ttu-id="1fd3e-192">Pärast töö kinnitamist saab selle aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-192">After a job is approved, it can be activated.</span></span>

<span data-ttu-id="1fd3e-193">Kinnitajatena loetletud inimesed saavad Attracti teatise, mis annab teada, et neil on üksus kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-193">The people who are listed as approvers will receive a notification in Attract to inform them that they have an item to approve.</span></span> <span data-ttu-id="1fd3e-194">Kinnitamise üksus ilmub ka armatuurlaua jaotisesse **Teile määratud**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-194">An approval item will also appear in the **Assigned to you** section on the dashboard.</span></span> <span data-ttu-id="1fd3e-195">Pärast seda, kui keegi töö aktsepteerib või kinnitab, saab värbamistöörühm teatise.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-195">After someone accepts or approves a job, the hiring team will receive a notification.</span></span> <span data-ttu-id="1fd3e-196">Lõpuks saab värbamistöörühm teatise, kui töö on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-196">Finally, the hiring team will receive a notification when the job is approved.</span></span>

## <a name="create-a-job"></a><span data-ttu-id="1fd3e-197">Töö loomine</span><span class="sxs-lookup"><span data-stu-id="1fd3e-197">Create a job</span></span>

<span data-ttu-id="1fd3e-198">Töö loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-198">Follow these steps to create a job.</span></span>

1. <span data-ttu-id="1fd3e-199">Minge valikusse **Tööd**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-199">Go to **Jobs**.</span></span>
2. <span data-ttu-id="1fd3e-200">Valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-200">Select **New**.</span></span>
3. <span data-ttu-id="1fd3e-201">Sisestage töö nimetus väljale **Töö nimetus**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-201">In the **Job title** field, enter the job title.</span></span> <span data-ttu-id="1fd3e-202">Sisestage oma roll väljale **Roll**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-202">In the **Role** field, enter your role.</span></span>
4. <span data-ttu-id="1fd3e-203">Valige mall väljal **Mall**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-203">In the **Template** field, select a template.</span></span> <span data-ttu-id="1fd3e-204">Teise võimalusena valige **Jäta vahele**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-204">Alternatively, select **Skip**.</span></span> <span data-ttu-id="1fd3e-205">Kui valite **Jäta vahele**, kasutatakse vaikemalliks märgitud malli.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-205">If you select **Skip**, the template that is marked as the default template is used.</span></span>

    <span data-ttu-id="1fd3e-206">Kui dokumendi peab läbima kinnitusprotsessi, valige mall mille väli **Kinnitusprotsess** on määratud **Vaikimisi** peale.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-206">If the document should go through an approval process, select a template where the **Approval process** field is set to **Default**.</span></span>

5. <span data-ttu-id="1fd3e-207">Sisestage töö üksikasjad vahekaardile **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-207">On the **Details** tab, enter the details of the job.</span></span> <span data-ttu-id="1fd3e-208">Väljad **Pealkiri**, **Töö kirjeldus** ja **Asukoht** on nõutavad.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-208">The **Title**, **Job description**, and **Location** fields are required.</span></span>
6. <span data-ttu-id="1fd3e-209">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-209">Select **Save**.</span></span>
7. <span data-ttu-id="1fd3e-210">Lisage vahekaardile **Värbamistöörühm** personalijuht, värbaja või intervjueerija.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-210">On the **Hiring team** tab, add a hiring manager, recruiter, or interviewer.</span></span>
8. <span data-ttu-id="1fd3e-211">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-211">Select **Save**.</span></span>
9. <span data-ttu-id="1fd3e-212">Vajadusel lisage etappe vahekaardile **Protsess** või eemaldage sealt etappe.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-212">On the **Process** tab, add or remove stages as you require:</span></span>

    - <span data-ttu-id="1fd3e-213">Etapi lisamiseks valige **+ Uus etapp**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-213">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="1fd3e-214">Etapi eemaldamiseks hoidke kursorit eemaldatava etapi kohal ja valige seejärel ilmunud prügikastinupp.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-214">To remove a stage, hover the pointer over the stage to remove, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1fd3e-215">Potentsiaalselt sobiva kandidaadi, avalduse ja pakkumise etappe ei saa eemaldada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-215">The Prospect, Application, and Offer stages can't be removed.</span></span>

10. <span data-ttu-id="1fd3e-216">Vajadusel lisage või eemaldage tegevusi.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-216">Add or remove activities as you require:</span></span>

    - <span data-ttu-id="1fd3e-217">Tegevuse lisamiseks lohistage see paremal asuvast loendist otse sobivasse etappi.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-217">To add an activity, drag it from the list on the right to the appropriate stage.</span></span> <span data-ttu-id="1fd3e-218">Teise võimalusena topeltklõpsake tegevusel ja valige etapp, kuhu see lisada.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-218">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="1fd3e-219">Tegevuse eemaldamiseks laiendage tegevust ja seejärel valige prügikasti nupp tegevuse päises.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-219">To remove an activity, expand the activity, and then select the trash can button on the activity header.</span></span>

11. <span data-ttu-id="1fd3e-220">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-220">Select **Save**.</span></span>
12. <span data-ttu-id="1fd3e-221">Kui valisite kinnitusprotsessi kasutamise, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-221">If you selected to use an approval process, follow these steps:</span></span>

    1. <span data-ttu-id="1fd3e-222">Valige **+ Lisa kinnitaja** ja sisestage kasutaja, kellel on Azure AD konto.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-222">Select **+ Add approver**, and then enter a user who has an Azure AD account.</span></span> <span data-ttu-id="1fd3e-223">Saate lisada mitu kinnitajat.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-223">You can add multiple approvers.</span></span>
    2. <span data-ttu-id="1fd3e-224">Valige **Saada kinnitajatele**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-224">Select **Send to approvers**.</span></span>

    <span data-ttu-id="1fd3e-225">Töö väli **Töö olek** määratakse **Ootel** peale.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-225">The **Job status** field of the job is set to **Pending**.</span></span> <span data-ttu-id="1fd3e-226">Pärast välja **Töö olek** muutumist olekusse **Kinnitatud**, saab töö aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-226">After the value of the **Job status** field changes to **Approved**, the job can be activated.</span></span>

13. <span data-ttu-id="1fd3e-227">Töö aktiveerimiseks valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-227">To activate the job, select **Activate**.</span></span>
14. <span data-ttu-id="1fd3e-228">Töö sisestamiseks avage **Töökuulutused**, ja seejärel valige Talent Careers saidi või LinkedIni all **Sisesta kohe**.</span><span class="sxs-lookup"><span data-stu-id="1fd3e-228">To post the job, go to **Postings**, and then select **Post Now** under the Talent Careers site or LinkedIn.</span></span>

