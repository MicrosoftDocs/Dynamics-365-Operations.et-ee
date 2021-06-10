---
title: Kandidaadi jälgimissüsteemi integreerimise API tutvustus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources kandidaadi jälgimissüsteemi (ATS) integratsiooni API-d.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c043ac9c19a810d1718f0d4907cd5e9d651d778f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055288"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="08bf4-103">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="08bf4-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="08bf4-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources kandidaadi jälgimissüsteemi (ATS) integratsiooni API-d.</span><span class="sxs-lookup"><span data-stu-id="08bf4-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="08bf4-105">API eesmärk on võimaldada sujuvat integreerimist rakenduse Dynamics 365 Human Resources ja partneriks olevate ATS-ide vahel.</span><span class="sxs-lookup"><span data-stu-id="08bf4-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS-integratsiooni voog](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="08bf4-107">Integreeritud kogemus algab rakenduses Human Resources, kui värbamisjuht loob värbamistaotluse.</span><span class="sxs-lookup"><span data-stu-id="08bf4-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="08bf4-108">Kui taotlus on aktiveeritud, tõmbab ATS üksikasjad värbamisprojekti loomise taotluse kohta.</span><span class="sxs-lookup"><span data-stu-id="08bf4-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="08bf4-109">Seejärel jälgitakse värbamise konteinerit, et valida ja palgata ametikohale kandidaat.</span><span class="sxs-lookup"><span data-stu-id="08bf4-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="08bf4-110">Lisaks lõpetab ATS integreerimise, saates valitud kandidaadi kirje rakendusse Human Resources.</span><span class="sxs-lookup"><span data-stu-id="08bf4-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="08bf4-111">Kandidaadi kirje saab siis töötajakirje loomiseks läbida rohkem kinnitusi ja töövooge.</span><span class="sxs-lookup"><span data-stu-id="08bf4-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="08bf4-112">Integratsiooni lubamiseks on Human Resources lisanud järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="08bf4-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="08bf4-113">Funktsionaalsus värbamistaotluse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="08bf4-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="08bf4-114">Laiendatud kandidaadiprofiil ja seotud töövood.</span><span class="sxs-lookup"><span data-stu-id="08bf4-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="08bf4-115">Integratsiooni API, mis avab uued funktsioonid rakenduste integreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="08bf4-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="08bf4-116">Lisateavet värbamistaotluse ja kandidaadi funktsiooni seadistamise ja kasutamise kohta leiate jaotisest [Värbamistöö kandidaadid](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="08bf4-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="08bf4-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="08bf4-117">Microsoft Dataverse</span></span>

<span data-ttu-id="08bf4-118">See API on ehitatud rakendusele Microsoft Dataverse (varem Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="08bf4-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="08bf4-119">Kogu RESTful interaktsioon selle API-ga toimub Microsoft Dataverse'i veebi API kaudu, mis kasutab OData.</span><span class="sxs-lookup"><span data-stu-id="08bf4-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="08bf4-120">See API on Dataverse'i Web API alamkogum.</span><span class="sxs-lookup"><span data-stu-id="08bf4-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="08bf4-121">Dataverse'i WEB API määratleb sellised omadused nagu autentimine, SLA-d, partii, samaaegsuse kontrolli ja tõrketöötluse.</span><span class="sxs-lookup"><span data-stu-id="08bf4-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="08bf4-122">Lisateavet Microsoft Dataverse'i Web API kohta leidke alpoolt.</span><span class="sxs-lookup"><span data-stu-id="08bf4-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="08bf4-123">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="08bf4-123">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="08bf4-124">Microsoft Dataverse'i Web API kasutamine</span><span class="sxs-lookup"><span data-stu-id="08bf4-124">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="08bf4-125">Microsoft Dataverse'i arendaja juhend</span><span class="sxs-lookup"><span data-stu-id="08bf4-125">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="08bf4-126">Ülaltoodud dokumentatsioon sisaldab üksikasju ja arendaja juhendeid Dataverse'i Web API kasutamiseks, näiteks [autentimise halduseks](/powerapps/developer/data-platform/webapi/authenticate-web-api), [toimingute tegemiseks](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postmani kasutamiseks API-ga](/powerapps/developer/data-platform/webapi/use-postman-web-api) ja [muudatuste jälgimise või delta sõnede kasutamiseks](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) API-ga.</span><span class="sxs-lookup"><span data-stu-id="08bf4-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="08bf4-127">Suvandikomplektid</span><span class="sxs-lookup"><span data-stu-id="08bf4-127">Option sets</span></span>

<span data-ttu-id="08bf4-128">Dokumendis kirjeldatud ATS-integratsiooni API andmemudel hõlmab valikukomplekte, mis pakuvad üksuse atribuutidega seostatud nummerdatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="08bf4-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="08bf4-129">Lisateavet Dataverse'i Web APIs suvandikomplektidega töötamise kohta leiate jaotisest [Suvandikomplektide loomine ja värskendamine Web API-ga](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="08bf4-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="08bf4-130">Suvandikomplektid määratakse igale Dataverse'i keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="08bf4-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="08bf4-131">Virtuaalsed tabelid rakendusele Human Resources Dataverse'is</span><span class="sxs-lookup"><span data-stu-id="08bf4-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="08bf4-132">ATS-integratsiooni API lõpp-punktid kasutavad rakenduse Microsoft Dataverse virtuaalse tabeli platvormi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="08bf4-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="08bf4-133">Vaikimisi ei juurutata virtuaalseid tabeleid ja nendega seotud API-lõpp-punkte Human Resources'i keskkondades, võimaldades organisatsioonidel määrata, millised OData lõpp-punktid keskkonnaga kokku puutuvad.</span><span class="sxs-lookup"><span data-stu-id="08bf4-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="08bf4-134">API kasutamiseks peavad keskkonna jaoks olema loodud virtuaalsed tabelid rakenduse Human Resources olemite jaoks.</span><span class="sxs-lookup"><span data-stu-id="08bf4-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="08bf4-135">Lisateavet API jaoks virtuaaltabelite loomise kohta leiate jaotisest [Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="08bf4-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="08bf4-136">Andmemudel</span><span class="sxs-lookup"><span data-stu-id="08bf4-136">Data model</span></span>

<span data-ttu-id="08bf4-137">Andmemudel on keskendunud kahe põhiüksuse ümber.</span><span class="sxs-lookup"><span data-stu-id="08bf4-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="08bf4-138">**RecruitingRequest** esindab ATS-i taotlust ühe või mitme avatud ametikoha värbamiseks. Näidispäringut vaadake jaotisest [Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="08bf4-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="08bf4-139">**CandidateToHire** tähistab kandidaadi üksikasju, kes on ametikoha pakkumise aktsepteerinud.</span><span class="sxs-lookup"><span data-stu-id="08bf4-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="08bf4-140">**Isik** tähistab isikut, kes on kandidaat.</span><span class="sxs-lookup"><span data-stu-id="08bf4-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="08bf4-141">Isikul võib ettevõttes olla mitmeid rolle (nt kandidaat, tööline, töötaja või töövõtja).</span><span class="sxs-lookup"><span data-stu-id="08bf4-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="08bf4-142">Näidispäringu leiate jaotisest [Palgatava kandidaadi näidispäring](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="08bf4-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="08bf4-143">Järgmine diagramm illustreerib seoseid API sees.</span><span class="sxs-lookup"><span data-stu-id="08bf4-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="08bf4-144">Mitmetel tüüpidel on võõrvõtmeid rakenduse Human Resources teiste, olemasolevate olemite jaoks, mida siin ei ole kujutatud.</span><span class="sxs-lookup"><span data-stu-id="08bf4-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="08bf4-145">See dokument annab teavet üksuste kohta, mis on integratsioonistsenaariumide värbamisel spetsiifilised.</span><span class="sxs-lookup"><span data-stu-id="08bf4-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="08bf4-146">Siiski on Dataverse'i Web APIs mitmeid teisi olemeid rakenduse Dynamics 365 Human Resources jaoks, mis võivad samuti olla teie integratsioonile asjakohased.</span><span class="sxs-lookup"><span data-stu-id="08bf4-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="08bf4-147">Näiteks võite vajada üksikasju töötajate, tööde, ametikohtade või muude siin määratlemata üksuste kohta.</span><span class="sxs-lookup"><span data-stu-id="08bf4-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="08bf4-148">Paljudele neile üksustele viidatakse võõrvõtme seostes või navigeerimisatribuutides.</span><span class="sxs-lookup"><span data-stu-id="08bf4-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS-integratsiooni API andmemudel](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="08bf4-150">Värbamistaotlus ja seotud üksused ning suvandikomplektid</span><span class="sxs-lookup"><span data-stu-id="08bf4-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="08bf4-151">Näidispäring:</span><span class="sxs-lookup"><span data-stu-id="08bf4-151">Example query:</span></span> 

- [<span data-ttu-id="08bf4-152">Värbamistaotluse näidispäring</span><span class="sxs-lookup"><span data-stu-id="08bf4-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="08bf4-153">Üksused:</span><span class="sxs-lookup"><span data-stu-id="08bf4-153">Entities:</span></span>

- [<span data-ttu-id="08bf4-154">Värbamistaotlus</span><span class="sxs-lookup"><span data-stu-id="08bf4-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="08bf4-155">Värbamistaotluse ametikoht</span><span class="sxs-lookup"><span data-stu-id="08bf4-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="08bf4-156">Värbamistaotluse oskus</span><span class="sxs-lookup"><span data-stu-id="08bf4-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="08bf4-157">Värbamistaotluse haridus</span><span class="sxs-lookup"><span data-stu-id="08bf4-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="08bf4-158">Värbamistaotluse asukoht</span><span class="sxs-lookup"><span data-stu-id="08bf4-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="08bf4-159">Suvandikomplektid.</span><span class="sxs-lookup"><span data-stu-id="08bf4-159">Option sets:</span></span>

- [<span data-ttu-id="08bf4-160">Töö vabastuse olek</span><span class="sxs-lookup"><span data-stu-id="08bf4-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="08bf4-161">Värbamistaotluse ametikoha olek</span><span class="sxs-lookup"><span data-stu-id="08bf4-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="08bf4-162">Värbamistaotluse olek</span><span class="sxs-lookup"><span data-stu-id="08bf4-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="08bf4-163">Regulatiivse töö kategooria</span><span class="sxs-lookup"><span data-stu-id="08bf4-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="08bf4-164">Palgatav kandidaat ja seotud üksused ning suvandikomplektid</span><span class="sxs-lookup"><span data-stu-id="08bf4-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="08bf4-165">Näidispäring:</span><span class="sxs-lookup"><span data-stu-id="08bf4-165">Example query:</span></span>

- [<span data-ttu-id="08bf4-166">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="08bf4-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="08bf4-167">Üksused:</span><span class="sxs-lookup"><span data-stu-id="08bf4-167">Entities:</span></span>

- [<span data-ttu-id="08bf4-168">Palgatav kandidaat</span><span class="sxs-lookup"><span data-stu-id="08bf4-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="08bf4-169">Isik</span><span class="sxs-lookup"><span data-stu-id="08bf4-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="08bf4-170">Isiku haridus</span><span class="sxs-lookup"><span data-stu-id="08bf4-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="08bf4-171">Isiku töökogemus</span><span class="sxs-lookup"><span data-stu-id="08bf4-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="08bf4-172">Isiku aadress</span><span class="sxs-lookup"><span data-stu-id="08bf4-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="08bf4-173">Osapoole kontakt</span><span class="sxs-lookup"><span data-stu-id="08bf4-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="08bf4-174">Isiku oskus</span><span class="sxs-lookup"><span data-stu-id="08bf4-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="08bf4-175">Hindamise tase</span><span class="sxs-lookup"><span data-stu-id="08bf4-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="08bf4-176">Isikutunnistus</span><span class="sxs-lookup"><span data-stu-id="08bf4-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="08bf4-177">Tunnistuse tüüp</span><span class="sxs-lookup"><span data-stu-id="08bf4-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="08bf4-178">Isiku skriining</span><span class="sxs-lookup"><span data-stu-id="08bf4-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="08bf4-179">Skriiningu tüübid</span><span class="sxs-lookup"><span data-stu-id="08bf4-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="08bf4-180">Isiku ID-number</span><span class="sxs-lookup"><span data-stu-id="08bf4-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="08bf4-181">Suvandikomplektid.</span><span class="sxs-lookup"><span data-stu-id="08bf4-181">Option sets:</span></span>

- [<span data-ttu-id="08bf4-182">Kandidaadi integratsiooni tulemus</span><span class="sxs-lookup"><span data-stu-id="08bf4-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="08bf4-183">Tühi Jah Ei</span><span class="sxs-lookup"><span data-stu-id="08bf4-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="08bf4-184">Lõpuleviimise olek</span><span class="sxs-lookup"><span data-stu-id="08bf4-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="08bf4-185">Kontakti tüüp</span><span class="sxs-lookup"><span data-stu-id="08bf4-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="08bf4-186">Hariduskrediidi alus</span><span class="sxs-lookup"><span data-stu-id="08bf4-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="08bf4-187">Sugu</span><span class="sxs-lookup"><span data-stu-id="08bf4-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="08bf4-188">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="08bf4-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="08bf4-189">Kuud aastast</span><span class="sxs-lookup"><span data-stu-id="08bf4-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="08bf4-190">Ei Jah</span><span class="sxs-lookup"><span data-stu-id="08bf4-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="08bf4-191">Perioodi ühik</span><span class="sxs-lookup"><span data-stu-id="08bf4-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="08bf4-192">Skriiningu sagedus</span><span class="sxs-lookup"><span data-stu-id="08bf4-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="08bf4-193">Skriiningu sageduse loomise vorm</span><span class="sxs-lookup"><span data-stu-id="08bf4-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="08bf4-194">Oskuse taseme tüüp</span><span class="sxs-lookup"><span data-stu-id="08bf4-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="08bf4-195">Vt ka</span><span class="sxs-lookup"><span data-stu-id="08bf4-195">See also</span></span>

[<span data-ttu-id="08bf4-196">Kandidaatide värbamine</span><span class="sxs-lookup"><span data-stu-id="08bf4-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="08bf4-197">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="08bf4-197">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="08bf4-198">Microsoft Dataverse'i Web API kasutamine</span><span class="sxs-lookup"><span data-stu-id="08bf4-198">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="08bf4-199">Suvandikomplektide loomine ja värskendamine Web API abil</span><span class="sxs-lookup"><span data-stu-id="08bf4-199">Create and update option sets using the Web API</span></span>](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]