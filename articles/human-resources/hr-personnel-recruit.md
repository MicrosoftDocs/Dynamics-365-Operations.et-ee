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
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669163"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="7aacc-103">Kandidaatide värbamine</span><span class="sxs-lookup"><span data-stu-id="7aacc-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7aacc-104">Dynamics 365 Human Resources aitab teil värbamistaotlusi hallata.</span><span class="sxs-lookup"><span data-stu-id="7aacc-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="7aacc-105">Samuti aitab see teil sujuvalt kandidaadid töövõtjateks üle viia.</span><span class="sxs-lookup"><span data-stu-id="7aacc-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="7aacc-106">Kui teie organisatsioon kasutab eraldi värbamisrakendust, võib teie värbamisprotsess hõlmata järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="7aacc-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="7aacc-107">Sisestate värbamistaotluse rakendusse Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7aacc-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="7aacc-108">Saate värbamisrakenduse kaudu kandidaatide soovitused kätte rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7aacc-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="7aacc-109">Viite kandidaadi kinnitamise lõpule rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7aacc-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="7aacc-110">Kui te ei kasuta eraldi värbamisrakendust, saate rakenduses Human Resources kandidaate ka käsitsi hallata.</span><span class="sxs-lookup"><span data-stu-id="7aacc-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="7aacc-111">Kui olete administraator või arendaja ja soovite integreerida Human Resourcesi kolmanda osapoole värbamisrakendusega, vaadake jaotist [Teenuse Common Data Service integreerimise konfigureerimine](hr-admin-integration-common-data-service.md) ja [Teenuse Common Data Service virtuaalsetüksuste konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="7aacc-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="7aacc-112">Lisaks saate otsida värbamisrakendusi siit: [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="7aacc-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="7aacc-113">Vt jaotist [LinkedIn Talent Hubi integreerimine](hr-admin-integration-linkedin.md), et proovida LinkedIn Talent Hubi integreerimise eelvaatefunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="7aacc-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="7aacc-114">Luba värbamistaotlused</span><span class="sxs-lookup"><span data-stu-id="7aacc-114">Enable recruiting requests</span></span>

<span data-ttu-id="7aacc-115">Kui soovite Human Resourcesi kaudu esitada töötajate värbamiskutseid, peate esmalt lubama funktsioonid jaotises **Human resourcesi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="7aacc-116">Tööruumis **Personalihaldus** valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="7aacc-117">Jaotises **Seadistus** valige suvand **Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="7aacc-118">Määrake jaotise **VÄRBAMINE** vahekaardil **Üldine** suvandi **Luba värbamistaotlused** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Luba värbamistaotlused](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="7aacc-120">Värbamistaotluse asukoha lisamine</span><span class="sxs-lookup"><span data-stu-id="7aacc-120">Add a recruiting request location</span></span>

<span data-ttu-id="7aacc-121">Kui teie organisatsioonil on mitu asukohta, saate need lisada, et taotluse esitajad saaksid valida asukoha, kus uus töövõtja tööle hakkab.</span><span class="sxs-lookup"><span data-stu-id="7aacc-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="7aacc-122">Asukoht lisatakse töökuulutusele.</span><span class="sxs-lookup"><span data-stu-id="7aacc-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="7aacc-123">Sisestage otsinguribale tekst **värbamistaotluse asukoht**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="7aacc-124">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-124">Select **New**.</span></span>

3. <span data-ttu-id="7aacc-125">Sisestage asukoha nimi väljale **Värbamistaotluse asukoht**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Värbamistaotluse asukoha lisamine](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="7aacc-127">Sisestage väljale **Kirjeldus** asukoha kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="7aacc-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="7aacc-128">Valige jaotises **Asukoht** nupp **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="7aacc-129">Kui kuvatakse hüpikaken **Uus aadress**, sisestage asukoha aadress.</span><span class="sxs-lookup"><span data-stu-id="7aacc-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Sisestage aadress](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="7aacc-131">Jaotises **Kontaktteave** sisestage asukoha kontaktisiku teave.</span><span class="sxs-lookup"><span data-stu-id="7aacc-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="7aacc-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="7aacc-133">Värbamistaotluse lisamine</span><span class="sxs-lookup"><span data-stu-id="7aacc-133">Add a recruiting request</span></span>

<span data-ttu-id="7aacc-134">Rakenduse Human Resources saavad juhid värbamistaotlusi esitada.</span><span class="sxs-lookup"><span data-stu-id="7aacc-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="7aacc-135">Kui kasutate eraldi värbamisrakendust ja viite need toimingud lõpule, saadetakse värbamisrakendus ja vastavas rakenduses alustatakse värbamisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="7aacc-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="7aacc-136">Muul juhul viige see protseduur lõpule, et alustada töövoogu ettevõttesisese värbamisprotsessiga.</span><span class="sxs-lookup"><span data-stu-id="7aacc-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="7aacc-137">Valige **Töövõtja iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="7aacc-138">Valige vahekaart **Minu töörühm**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="7aacc-139">Valige **Värbamistaotlus**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-139">Select  **Request to recruit**.</span></span>

   ![Värbamistaotluse alustamine](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="7aacc-141">Täitke väli **Kirjeldus**, **Töö** ja **Eeldatav alguskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Värbamistaotluse lõpuleviimine](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="7aacc-143">Valige nupp **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-143">Select **Continue**.</span></span> <span data-ttu-id="7aacc-144">Kuvatakse teie ametikoha värbamistaotlus.</span><span class="sxs-lookup"><span data-stu-id="7aacc-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="7aacc-145">Jaotises **Üldine** valige värbaja rippmenüüst **Värbaja** ja seejärel valige asukoht rippmenüüst **Värbamistaotluse asukoht**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="7aacc-146">Jaotises **Töö** muutke teavet vastavalt vajadusele ja seejärel valige käsk **Loo töö põhjal üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Loo üksikasjad töö põhjal](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="7aacc-148">Ülejäänud värbamistaotlus täidetakse sisestatud töö vaiketeabega.</span><span class="sxs-lookup"><span data-stu-id="7aacc-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="7aacc-149">Sisestage jaotises **Väline kirjeldus** ettevõtteväline töökirjeldus.</span><span class="sxs-lookup"><span data-stu-id="7aacc-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="7aacc-150">Jaotises **Ametikohad** valige nupp **Lisa** ja seejärel selle värbamistaotluse ametikoht.</span><span class="sxs-lookup"><span data-stu-id="7aacc-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Ametikoha lisamine](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="7aacc-152">Jaotises **Oskused** valige nupp **Lisa** ja seejärel valige oskus.</span><span class="sxs-lookup"><span data-stu-id="7aacc-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="7aacc-153">Jaotises **Haridusnõuded** valige nupp **Lisa** ja seejärel valige väärtused ripploendist **Haridus** ja **Haridustase**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Haridusnõuete lisamine](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="7aacc-155">Jaotises **Kommenteerimine** lisage vajaduse korral kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="7aacc-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="7aacc-156">Jaotises **Kompensatsioon** valige tase ripploendist **Tase** ja seejärel kohandage vastavalt vajadusele väärtust **Madal lävi**, **Kontrollpunkt** ja **Kõrge lävi**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="7aacc-157">Kui teie värbamistaotlus on lõpule viidud ja olete valmis alustama värbamisprotsessi, valige menüüribalt käsk **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Värbamistaotluse aktiveerimine](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="7aacc-159">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="7aacc-160">Värbamistaotluste kuvamine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="7aacc-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="7aacc-161">Kui olete juht ja soovite oma taotlusi vaadata, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7aacc-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="7aacc-162">Valige **Töövõtja iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="7aacc-163">Valige vahekaart **Minu töörühm**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="7aacc-164">Jaotises **Minu töörühma teave** valige vahekaart **Värbamistaotlused**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Värbamistaotluste vahekaardi valimine](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="7aacc-166">Värbamistaotluse vaatamiseks või muutmiseks valige see ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="7aacc-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="7aacc-167">Kui olete personalispetsialist ja soovite vaadata kõiki värbamistaotlusi, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7aacc-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="7aacc-168">Valige **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="7aacc-169">valige **Värbamistaotlused**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-169">Select **Recruiting requests**.</span></span>

   ![Personalihalduse kaudu värbamistaotluste kuvamine](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="7aacc-171">Värbamistaotluse vaatamiseks või muutmiseks valige see ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="7aacc-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="7aacc-172">Kandidaadi profiili lisamine või muutmine</span><span class="sxs-lookup"><span data-stu-id="7aacc-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="7aacc-173">Kui teie organisatsioon on integreeritud mõne muu rakendusega, et hallata värbamisaotlusi, edastatakse värbamistaotlused sellele rakendusele.</span><span class="sxs-lookup"><span data-stu-id="7aacc-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="7aacc-174">Värbamisrakendus saadab seejärel kandidaadi teabe tagasi rakendusele Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7aacc-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="7aacc-175">Muidu saate jälgida ettevõttesiseseid värbamisprotsesse ja kandidaaditeavet sisestada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="7aacc-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="7aacc-176">Valige **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="7aacc-177">Valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-177">Select **Links**.</span></span>

3. <span data-ttu-id="7aacc-178">Jaotises **Värbamine** valige **Kandidaadid**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Kandidaatide kuvamine](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="7aacc-180">Kandidaadi lisamiseks valige nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="7aacc-181">Olemasoleva kandidaadi redigeerimiseks valige loendist aadress ja seejärel valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="7aacc-182">Kuvatakse kandidaadi profiil.</span><span class="sxs-lookup"><span data-stu-id="7aacc-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="7aacc-183">Jaotises **Kandidaadi ülevaade** saate kandidaadi teavet vajaduse korral sisestada või redigeerida.</span><span class="sxs-lookup"><span data-stu-id="7aacc-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="7aacc-184">Jaotises **Värbamistaotlus** valige kandidaadi linkimiseks värbamistaotlus.</span><span class="sxs-lookup"><span data-stu-id="7aacc-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="7aacc-185">Seejärel täitke väli **Eeldatav alguskuupäev**, **Värbamisjuht**, **Ametikoht** ja **Kirjeldus** vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="7aacc-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Värbamistaotluse link](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="7aacc-187">Lisage kõik andmed järgmistes valdkondades, mida soovite kandidaadi kirjele lisada.</span><span class="sxs-lookup"><span data-stu-id="7aacc-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="7aacc-188">**Kommentaarid**</span><span class="sxs-lookup"><span data-stu-id="7aacc-188">**Comments**</span></span>
   - <span data-ttu-id="7aacc-189">**Töökogemus**</span><span class="sxs-lookup"><span data-stu-id="7aacc-189">**Professional experience**</span></span>
   - <span data-ttu-id="7aacc-190">**Kontaktandmed**</span><span class="sxs-lookup"><span data-stu-id="7aacc-190">**Contact information**</span></span>
   - <span data-ttu-id="7aacc-191">**Haridus**</span><span class="sxs-lookup"><span data-stu-id="7aacc-191">**Education**</span></span>
   - <span data-ttu-id="7aacc-192">**Oskused**</span><span class="sxs-lookup"><span data-stu-id="7aacc-192">**Skills**</span></span>
   - <span data-ttu-id="7aacc-193">**Serdid**</span><span class="sxs-lookup"><span data-stu-id="7aacc-193">**Certificates**</span></span>
   - <span data-ttu-id="7aacc-194">**Skriiningud**</span><span class="sxs-lookup"><span data-stu-id="7aacc-194">**Screenings**</span></span>

8. <span data-ttu-id="7aacc-195">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="7aacc-196">Kandidaadi palkamine</span><span class="sxs-lookup"><span data-stu-id="7aacc-196">Hire a candidate</span></span>

<span data-ttu-id="7aacc-197">Kui olete kandidaadi palkamiseks valmis, järgige seda protseduuri, et muuta kandidaat töövõtjaks.</span><span class="sxs-lookup"><span data-stu-id="7aacc-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="7aacc-198">Kandidaadi vormil valige käsk **Palka**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-198">On the candidate form, select **Hire**.</span></span>

   ![Kandidaadi palkamine](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="7aacc-200">Täitke kõik väljad vormi **Uue töövõtja palkamine** jaotises **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Palgatud töövõtja üksikasjade sisestamine](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="7aacc-202">Jaotises **Ametikoha üksikasjad** kontrollige ja muutke vajaduse korral teavet.</span><span class="sxs-lookup"><span data-stu-id="7aacc-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="7aacc-203">Valige jaotisest **Palkamise kontroll-loendid** selle töövõtja jaoks asjakohased kontroll-loendid.</span><span class="sxs-lookup"><span data-stu-id="7aacc-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="7aacc-204">Valige **Jätka**, et luua töötaja kirje.</span><span class="sxs-lookup"><span data-stu-id="7aacc-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="7aacc-205">Sõltuvalt teie organisatsiooni töövoogudest võib kandidaadi kirje enne töövõtja kirje muutumist läbida täiendavaid kinnitamise etappe.</span><span class="sxs-lookup"><span data-stu-id="7aacc-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="7aacc-206">Otsus kandidaati mitte palgata</span><span class="sxs-lookup"><span data-stu-id="7aacc-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="7aacc-207">Kui otsustate kandidaati mitte palgata, järgige seda protseduuri, et eemaldada ta taustakontrollist.</span><span class="sxs-lookup"><span data-stu-id="7aacc-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="7aacc-208">Kandidaadi vormil valige käsk **Ära palka**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-208">On the candidate form, select **Do not hire**.</span></span>

   ![Kandidaadi mittepalkamine](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="7aacc-210">Saate valida **Põhjuse koodi** ja kommentaare lisada.</span><span class="sxs-lookup"><span data-stu-id="7aacc-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="7aacc-211">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="7aacc-212">Kandidaadist loobumine</span><span class="sxs-lookup"><span data-stu-id="7aacc-212">Dismiss a candidate</span></span>

<span data-ttu-id="7aacc-213">Vajaduse korral saate kandidaadist pärast tema palkamist loobuda.</span><span class="sxs-lookup"><span data-stu-id="7aacc-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="7aacc-214">Näiteks võib kandidaat teie pakkumise tagasi lükata või ei ilmu esimesel päeval kohale.</span><span class="sxs-lookup"><span data-stu-id="7aacc-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="7aacc-215">Valige kandidaadi vormil käsk **Loobu kandidaadist**.</span><span class="sxs-lookup"><span data-stu-id="7aacc-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Lõpeta kandidaat](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="7aacc-217">Vt ka</span><span class="sxs-lookup"><span data-stu-id="7aacc-217">See also</span></span>

[<span data-ttu-id="7aacc-218">Common Data Service'i virtuaalüksuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7aacc-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="7aacc-219">Tööjõu korraldamine</span><span class="sxs-lookup"><span data-stu-id="7aacc-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="7aacc-220">Töö komponentide häälestus</span><span class="sxs-lookup"><span data-stu-id="7aacc-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)