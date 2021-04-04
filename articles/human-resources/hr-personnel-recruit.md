---
title: Kandidaatide värbamine
description: See teema näitab, kuidas rakenduses Dynamics 365 Human Resources kandidaate värvata.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
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
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6aca285133495dfe023dfd18bdeb050aabcafee6
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478280"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="dcf02-103">Kandidaatide värbamine</span><span class="sxs-lookup"><span data-stu-id="dcf02-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dcf02-104">Dynamics 365 Human Resources aitab teil värbamistaotlusi hallata.</span><span class="sxs-lookup"><span data-stu-id="dcf02-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="dcf02-105">Samuti aitab see teil sujuvalt kandidaadid töövõtjateks üle viia.</span><span class="sxs-lookup"><span data-stu-id="dcf02-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="dcf02-106">Kui teie organisatsioon kasutab eraldi värbamisrakendust, võib teie värbamisprotsess hõlmata järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="dcf02-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="dcf02-107">Sisestate värbamistaotluse rakendusse Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dcf02-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="dcf02-108">Saate värbamisrakenduse kaudu kandidaatide soovitused kätte rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dcf02-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="dcf02-109">Viite kandidaadi kinnitamise lõpule rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dcf02-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="dcf02-110">Kui te ei kasuta eraldi värbamisrakendust, saate rakenduses Human Resources kandidaate ka käsitsi hallata.</span><span class="sxs-lookup"><span data-stu-id="dcf02-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="dcf02-111">Kui olete administraator või arendaja ja soovite integreerida Human Resourcesi kolmanda osapoole värbamisrakendusega, vaadake jaotist [Teenuse Dataverse integreerimise konfigureerimine](hr-admin-integration-common-data-service.md) ja [Teenuse Dataverse virtuaalsete tabelite konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="dcf02-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="dcf02-112">Lisaks saate otsida värbamisrakendusi siit: [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="dcf02-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="dcf02-113">Vt jaotist [LinkedIn Talent Hubi integreerimine](hr-admin-integration-linkedin.md), et proovida LinkedIn Talent Hubi integreerimise eelvaatefunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="dcf02-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="dcf02-114">Luba värbamistaotlused</span><span class="sxs-lookup"><span data-stu-id="dcf02-114">Enable recruiting requests</span></span>

<span data-ttu-id="dcf02-115">Kui soovite Human Resourcesi kaudu esitada töötajate värbamiskutseid, peate esmalt lubama funktsioonid jaotises **Human Resourcesi ühiskasutuses olevad parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="dcf02-116">Tööruumis **Personalihaldus** valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="dcf02-117">Jaotises **Häälestus** valige suvand **Human Resourcesi ühiskasutuses parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="dcf02-118">Määrake jaotise **VÄRBAMINE** vahekaardil **Värbamine** suvandi **Luba värbamistaotlused** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="dcf02-119">Värbamistaotluse asukoha lisamine</span><span class="sxs-lookup"><span data-stu-id="dcf02-119">Add a recruiting request location</span></span>

<span data-ttu-id="dcf02-120">Kui teie organisatsioonil on mitu asukohta, saate need lisada, et taotluse esitajad saaksid valida asukoha, kus uus töövõtja tööle hakkab.</span><span class="sxs-lookup"><span data-stu-id="dcf02-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="dcf02-121">Asukoht lisatakse töökuulutusele.</span><span class="sxs-lookup"><span data-stu-id="dcf02-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="dcf02-122">Sisestage otsinguribale tekst **värbamistaotluse asukoht**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="dcf02-123">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-123">Select **New**.</span></span>

3. <span data-ttu-id="dcf02-124">Sisestage asukoha nimi väljale **Värbamistaotluse asukoht**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Värbamistaotluse asukoha lisamine](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="dcf02-126">Sisestage väljale **Kirjeldus** asukoha kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="dcf02-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="dcf02-127">Valige jaotises **Asukoht** nupp **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="dcf02-128">Kui kuvatakse hüpikaken **Uus aadress**, sisestage asukoha aadress.</span><span class="sxs-lookup"><span data-stu-id="dcf02-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Sisestage aadress](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="dcf02-130">Jaotises **Kontaktteave** sisestage asukoha kontaktisiku teave.</span><span class="sxs-lookup"><span data-stu-id="dcf02-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="dcf02-131">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="dcf02-132">Värbamistaotluse lisamine</span><span class="sxs-lookup"><span data-stu-id="dcf02-132">Add a recruiting request</span></span>

<span data-ttu-id="dcf02-133">Rakenduse Human Resources saavad juhid värbamistaotlusi esitada.</span><span class="sxs-lookup"><span data-stu-id="dcf02-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="dcf02-134">Kui kasutate eraldi värbamisrakendust ja viite need toimingud lõpule, saadetakse värbamisrakendus ja vastavas rakenduses alustatakse värbamisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="dcf02-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="dcf02-135">Muul juhul viige see protseduur lõpule, et alustada töövoogu ettevõttesisese värbamisprotsessiga.</span><span class="sxs-lookup"><span data-stu-id="dcf02-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="dcf02-136">Valige **Töövõtja iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="dcf02-137">Valige vahekaart **Minu töörühm**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="dcf02-138">Valige **Värbamistaotlus**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-138">Select  **Request to recruit**.</span></span>

   ![Värbamistaotluse alustamine](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="dcf02-140">Täitke väli **Kirjeldus**, **Töö** ja **Eeldatav alguskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Värbamistaotluse lõpuleviimine](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="dcf02-142">Valige nupp **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-142">Select **Continue**.</span></span> <span data-ttu-id="dcf02-143">Kuvatakse teie ametikoha värbamistaotlus.</span><span class="sxs-lookup"><span data-stu-id="dcf02-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="dcf02-144">Jaotises **Üldine** valige värbaja rippmenüüst **Värbaja** ja seejärel valige asukoht rippmenüüst **Värbamistaotluse asukoht**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="dcf02-145">Jaotises **Töö** muutke teavet vastavalt vajadusele ja seejärel valige käsk **Loo töö põhjal üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Loo üksikasjad töö põhjal](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="dcf02-147">Ülejäänud värbamistaotlus täidetakse sisestatud töö vaiketeabega.</span><span class="sxs-lookup"><span data-stu-id="dcf02-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="dcf02-148">Sisestage jaotises **Väline kirjeldus** ettevõtteväline töökirjeldus.</span><span class="sxs-lookup"><span data-stu-id="dcf02-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="dcf02-149">Jaotises **Ametikohad** valige nupp **Lisa** ja seejärel selle värbamistaotluse ametikoht.</span><span class="sxs-lookup"><span data-stu-id="dcf02-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Ametikoha lisamine](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="dcf02-151">Jaotises **Oskused** valige nupp **Lisa** ja seejärel valige oskus.</span><span class="sxs-lookup"><span data-stu-id="dcf02-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="dcf02-152">Jaotises **Haridusnõuded** valige nupp **Lisa** ja seejärel valige väärtused ripploendist **Haridus** ja **Haridustase**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Haridusnõuete lisamine](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="dcf02-154">Jaotises **Kommenteerimine** lisage vajaduse korral kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="dcf02-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="dcf02-155">Jaotises **Kompensatsioon** valige tase ripploendist **Tase** ja seejärel kohandage vastavalt vajadusele väärtust **Madal lävi**, **Kontrollpunkt** ja **Kõrge lävi**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="dcf02-156">Kui teie värbamistaotlus on lõpule viidud ja olete valmis alustama värbamisprotsessi, valige menüüribalt käsk **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Värbamistaotluse aktiveerimine](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="dcf02-158">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="dcf02-159">Värbamistaotluste kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="dcf02-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="dcf02-160">Kui olete juht ja soovite oma taotlusi vaadata, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="dcf02-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="dcf02-161">Valige **Töövõtja iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="dcf02-162">Valige vahekaart **Minu töörühm**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="dcf02-163">Jaotises **Minu töörühma teave** valige vahekaart **Värbamistaotlused**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Värbamistaotluste vahekaardi valimine](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="dcf02-165">Värbamistaotluse vaatamiseks või muutmiseks valige see ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="dcf02-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="dcf02-166">Kui olete personalispetsialist ja soovite vaadata kõiki värbamistaotlusi, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="dcf02-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="dcf02-167">Valige **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="dcf02-168">valige **Värbamistaotlused**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-168">Select **Recruiting requests**.</span></span>

   ![Personalihalduse kaudu värbamistaotluste kuvamine](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="dcf02-170">Värbamistaotluse vaatamiseks või muutmiseks valige see ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="dcf02-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="dcf02-171">Kandidaadi profiili lisamine või muutmine</span><span class="sxs-lookup"><span data-stu-id="dcf02-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="dcf02-172">Kui teie organisatsioon on integreeritud mõne muu rakendusega, et hallata värbamisaotlusi, edastatakse värbamistaotlused sellele rakendusele.</span><span class="sxs-lookup"><span data-stu-id="dcf02-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="dcf02-173">Värbamisrakendus saadab seejärel kandidaadi teabe tagasi rakendusele Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dcf02-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="dcf02-174">Muidu saate jälgida ettevõttesiseseid värbamisprotsesse ja kandidaaditeavet sisestada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="dcf02-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="dcf02-175">Valige **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="dcf02-176">Valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-176">Select **Links**.</span></span>

3. <span data-ttu-id="dcf02-177">Jaotises **Värbamine** valige **Kandidaadid**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Kandidaatide kuvamine](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="dcf02-179">Kandidaadi lisamiseks valige nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="dcf02-180">Olemasoleva kandidaadi redigeerimiseks valige loendist aadress ja seejärel valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="dcf02-181">Kuvatakse kandidaadi profiil.</span><span class="sxs-lookup"><span data-stu-id="dcf02-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="dcf02-182">Jaotises **Kandidaadi ülevaade** saate kandidaadi teavet vajaduse korral sisestada või redigeerida.</span><span class="sxs-lookup"><span data-stu-id="dcf02-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="dcf02-183">Jaotises **Värbamistaotlus** valige kandidaadi linkimiseks värbamistaotlus.</span><span class="sxs-lookup"><span data-stu-id="dcf02-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="dcf02-184">Seejärel täitke väli **Eeldatav alguskuupäev**, **Värbamisjuht**, **Ametikoht** ja **Kirjeldus** vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="dcf02-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Värbamistaotluse link](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="dcf02-186">Lisage kõik andmed järgmistes valdkondades, mida soovite kandidaadi kirjele lisada.</span><span class="sxs-lookup"><span data-stu-id="dcf02-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="dcf02-187">**Kommentaarid**</span><span class="sxs-lookup"><span data-stu-id="dcf02-187">**Comments**</span></span>
   - <span data-ttu-id="dcf02-188">**Töökogemus**</span><span class="sxs-lookup"><span data-stu-id="dcf02-188">**Professional experience**</span></span>
   - <span data-ttu-id="dcf02-189">**Kontaktandmed**</span><span class="sxs-lookup"><span data-stu-id="dcf02-189">**Contact information**</span></span>
   - <span data-ttu-id="dcf02-190">**Haridus**</span><span class="sxs-lookup"><span data-stu-id="dcf02-190">**Education**</span></span>
   - <span data-ttu-id="dcf02-191">**Oskused**</span><span class="sxs-lookup"><span data-stu-id="dcf02-191">**Skills**</span></span>
   - <span data-ttu-id="dcf02-192">**Serdid**</span><span class="sxs-lookup"><span data-stu-id="dcf02-192">**Certificates**</span></span>
   - <span data-ttu-id="dcf02-193">**Skriiningud**</span><span class="sxs-lookup"><span data-stu-id="dcf02-193">**Screenings**</span></span>

8. <span data-ttu-id="dcf02-194">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="dcf02-195">Kandidaadi palkamine</span><span class="sxs-lookup"><span data-stu-id="dcf02-195">Hire a candidate</span></span>

<span data-ttu-id="dcf02-196">Kui olete kandidaadi palkamiseks valmis, järgige seda protseduuri, et muuta kandidaat töövõtjaks.</span><span class="sxs-lookup"><span data-stu-id="dcf02-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="dcf02-197">Kandidaadi vormil valige käsk **Palka**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-197">On the candidate form, select **Hire**.</span></span>

   ![Kandidaadi palkamine](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="dcf02-199">Täitke kõik väljad vormi **Uue töövõtja palkamine** jaotises **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Palgatud töövõtja üksikasjade sisestamine](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="dcf02-201">Jaotises **Ametikoha üksikasjad** kontrollige ja muutke vajaduse korral teavet.</span><span class="sxs-lookup"><span data-stu-id="dcf02-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="dcf02-202">Valige jaotisest **Palkamise kontroll-loendid** selle töövõtja jaoks asjakohased kontroll-loendid.</span><span class="sxs-lookup"><span data-stu-id="dcf02-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="dcf02-203">Valige **Jätka**, et luua töötaja kirje.</span><span class="sxs-lookup"><span data-stu-id="dcf02-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="dcf02-204">Sõltuvalt teie organisatsiooni töövoogudest võib kandidaadi kirje enne töövõtja kirje muutumist läbida täiendavaid kinnitamise etappe.</span><span class="sxs-lookup"><span data-stu-id="dcf02-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="dcf02-205">Otsus kandidaati mitte palgata</span><span class="sxs-lookup"><span data-stu-id="dcf02-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="dcf02-206">Kui otsustate kandidaati mitte palgata, järgige seda protseduuri, et eemaldada ta taustakontrollist.</span><span class="sxs-lookup"><span data-stu-id="dcf02-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="dcf02-207">Kandidaadi vormil valige käsk **Ära palka**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-207">On the candidate form, select **Do not hire**.</span></span>

   ![Kandidaadi mittepalkamine](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="dcf02-209">Saate valida **Põhjuse koodi** ja kommentaare lisada.</span><span class="sxs-lookup"><span data-stu-id="dcf02-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="dcf02-210">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="dcf02-211">Kandidaadist loobumine</span><span class="sxs-lookup"><span data-stu-id="dcf02-211">Dismiss a candidate</span></span>

<span data-ttu-id="dcf02-212">Vajaduse korral saate kandidaadist pärast tema palkamist loobuda.</span><span class="sxs-lookup"><span data-stu-id="dcf02-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="dcf02-213">Näiteks võib kandidaat teie pakkumise tagasi lükata või ei ilmu esimesel päeval kohale.</span><span class="sxs-lookup"><span data-stu-id="dcf02-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="dcf02-214">Valige kandidaadi vormil käsk **Loobu kandidaadist**.</span><span class="sxs-lookup"><span data-stu-id="dcf02-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Lõpeta kandidaat](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="dcf02-216">Vt ka</span><span class="sxs-lookup"><span data-stu-id="dcf02-216">See also</span></span>

[<span data-ttu-id="dcf02-217">Dataverse'i virtuaalsete tabelite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dcf02-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="dcf02-218">Tööjõu korraldamine</span><span class="sxs-lookup"><span data-stu-id="dcf02-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="dcf02-219">Töö komponentide häälestus</span><span class="sxs-lookup"><span data-stu-id="dcf02-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
