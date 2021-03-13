---
title: Kandidaadi jälgimissüsteemi integreerimise API tutvustus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources kandidaadi jälgimissüsteemi (ATS) integratsiooni API-d.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 48e368fe69443a5105ddba78a887bf9159bfe52a
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125589"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="3786e-103">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="3786e-103">Applicant Tracking System integration API introduction</span></span>

<span data-ttu-id="3786e-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources kandidaadi jälgimissüsteemi (ATS) integratsiooni API-d.</span><span class="sxs-lookup"><span data-stu-id="3786e-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="3786e-105">API eesmärk on võimaldada sujuvat integreerimist rakenduse Dynamics 365 Human Resources ja partneriks olevate ATS-ide vahel.</span><span class="sxs-lookup"><span data-stu-id="3786e-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS-integratsiooni voog](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="3786e-107">Integreeritud kogemus algab rakenduses Human Resources, kui värbamisjuht loob värbamistaotluse.</span><span class="sxs-lookup"><span data-stu-id="3786e-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="3786e-108">Kui taotlus on aktiveeritud, tõmbab ATS üksikasjad värbamisprojekti loomise taotluse kohta.</span><span class="sxs-lookup"><span data-stu-id="3786e-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="3786e-109">Seejärel jälgitakse värbamise konteinerit, et valida ja palgata ametikohale kandidaat.</span><span class="sxs-lookup"><span data-stu-id="3786e-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="3786e-110">Lisaks lõpetab ATS integreerimise, saates valitud kandidaadi kirje rakendusse Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3786e-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="3786e-111">Kandidaadi kirje saab siis töötajakirje loomiseks läbida rohkem kinnitusi ja töövooge.</span><span class="sxs-lookup"><span data-stu-id="3786e-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="3786e-112">Integratsiooni lubamiseks on Human Resources lisanud järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="3786e-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="3786e-113">Funktsionaalsus värbamistaotluse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="3786e-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="3786e-114">Laiendatud kandidaadiprofiil ja seotud töövood.</span><span class="sxs-lookup"><span data-stu-id="3786e-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="3786e-115">Integratsiooni API, mis avab uued funktsioonid rakenduste integreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="3786e-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="3786e-116">Lisateavet värbamistaotluse ja kandidaadi funktsiooni seadistamise ja kasutamise kohta leiate jaotisest [Värbamistöö kandidaadid](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="3786e-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="3786e-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="3786e-117">Microsoft Dataverse</span></span>

<span data-ttu-id="3786e-118">See API on ehitatud rakendusele Microsoft Dataverse (varem Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="3786e-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="3786e-119">Kogu RESTful interaktsioon selle API-ga toimub Microsoft Dataverse'i veebi API kaudu, mis kasutab OData.</span><span class="sxs-lookup"><span data-stu-id="3786e-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="3786e-120">See API on Dataverse'i Web API alamkogum.</span><span class="sxs-lookup"><span data-stu-id="3786e-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="3786e-121">Dataverse'i WEB API määratleb sellised omadused nagu autentimine, SLA-d, partii, samaaegsuse kontrolli ja tõrketöötluse.</span><span class="sxs-lookup"><span data-stu-id="3786e-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="3786e-122">Lisateavet Microsoft Dataverse'i Web API kohta leidke alpoolt.</span><span class="sxs-lookup"><span data-stu-id="3786e-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="3786e-123">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="3786e-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="3786e-124">Microsoft Dataverse'i Web API kasutamine</span><span class="sxs-lookup"><span data-stu-id="3786e-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="3786e-125">Microsoft Dataverse'i arendaja juhend</span><span class="sxs-lookup"><span data-stu-id="3786e-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="3786e-126">Ülaltoodud dokumentatsioon sisaldab üksikasju ja arendaja juhendeid Dataverse'i Web API kasutamiseks, näiteks [autentimise halduseks](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [toimingute tegemiseks](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postmani kasutamiseks API-ga](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) ja [muudatuste jälgimise või delta sõnede kasutamiseks](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) API-ga.</span><span class="sxs-lookup"><span data-stu-id="3786e-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="3786e-127">Suvandikomplektid</span><span class="sxs-lookup"><span data-stu-id="3786e-127">Option sets</span></span>

<span data-ttu-id="3786e-128">Dokumendis kirjeldatud ATS-integratsiooni API andmemudel hõlmab valikukomplekte, mis pakuvad üksuse atribuutidega seostatud nummerdatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="3786e-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="3786e-129">Lisateavet Dataverse'i Web APIs suvandikomplektidega töötamise kohta leiate jaotisest [Suvandikomplektide loomine ja värskendamine Web API-ga](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="3786e-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="3786e-130">Suvandikomplektid määratakse igale Dataverse'i keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="3786e-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="3786e-131">Virtuaalsed tabelid rakendusele Human Resources Dataverse'is</span><span class="sxs-lookup"><span data-stu-id="3786e-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="3786e-132">ATS-integratsiooni API lõpp-punktid kasutavad rakenduse Microsoft Dataverse virtuaalse tabeli platvormi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="3786e-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="3786e-133">Vaikimisi ei juurutata virtuaalseid tabeleid ja nendega seotud API-lõpp-punkte Human Resources'i keskkondades, võimaldades organisatsioonidel määrata, millised OData lõpp-punktid keskkonnaga kokku puutuvad.</span><span class="sxs-lookup"><span data-stu-id="3786e-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="3786e-134">API kasutamiseks peavad keskkonna jaoks olema loodud virtuaalsed tabelid rakenduse Human Resources olemite jaoks.</span><span class="sxs-lookup"><span data-stu-id="3786e-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="3786e-135">Lisateavet API jaoks virtuaaltabelite loomise kohta leiate jaotisest [Dataverse'i virtuaalsete tabelite konfigureerimine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="3786e-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="3786e-136">Andmemudel</span><span class="sxs-lookup"><span data-stu-id="3786e-136">Data model</span></span>

<span data-ttu-id="3786e-137">Andmemudel on keskendunud kahe põhiüksuse ümber.</span><span class="sxs-lookup"><span data-stu-id="3786e-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="3786e-138">**RecruitingRequest** esindab ATS-i taotlust ühe või mitme avatud ametikoha värbamiseks. Näidispäringut vaadake jaotisest [Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="3786e-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="3786e-139">**CandidateToHire** tähistab kandidaadi üksikasju, kes on ametikoha pakkumise aktsepteerinud.</span><span class="sxs-lookup"><span data-stu-id="3786e-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="3786e-140">**Isik** tähistab isikut, kes on kandidaat.</span><span class="sxs-lookup"><span data-stu-id="3786e-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="3786e-141">Isikul võib ettevõttes olla mitmeid rolle (nt kandidaat, tööline, töötaja või töövõtja).</span><span class="sxs-lookup"><span data-stu-id="3786e-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="3786e-142">Näidispäringu leiate jaotisest [Palgatava kandidaadi näidispäring](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="3786e-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="3786e-143">Järgmine diagramm illustreerib seoseid API sees.</span><span class="sxs-lookup"><span data-stu-id="3786e-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="3786e-144">Mitmetel tüüpidel on võõrvõtmeid rakenduse Human Resources teiste, olemasolevate olemite jaoks, mida siin ei ole kujutatud.</span><span class="sxs-lookup"><span data-stu-id="3786e-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="3786e-145">See dokument annab teavet üksuste kohta, mis on integratsioonistsenaariumide värbamisel spetsiifilised.</span><span class="sxs-lookup"><span data-stu-id="3786e-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="3786e-146">Siiski on Dataverse'i Web APIs mitmeid teisi olemeid rakenduse Dynamics 365 Human Resources jaoks, mis võivad samuti olla teie integratsioonile asjakohased.</span><span class="sxs-lookup"><span data-stu-id="3786e-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="3786e-147">Näiteks võite vajada üksikasju töötajate, tööde, ametikohtade või muude siin määratlemata üksuste kohta.</span><span class="sxs-lookup"><span data-stu-id="3786e-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="3786e-148">Paljudele neile üksustele viidatakse võõrvõtme seostes või navigeerimisatribuutides.</span><span class="sxs-lookup"><span data-stu-id="3786e-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS-integratsiooni API andmemudel](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="3786e-150">Värbamistaotlus ja seotud üksused ning suvandikomplektid</span><span class="sxs-lookup"><span data-stu-id="3786e-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="3786e-151">Näidispäring:</span><span class="sxs-lookup"><span data-stu-id="3786e-151">Example query:</span></span> 

- [<span data-ttu-id="3786e-152">Värbamistaotluse näidispäring</span><span class="sxs-lookup"><span data-stu-id="3786e-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="3786e-153">Üksused:</span><span class="sxs-lookup"><span data-stu-id="3786e-153">Entities:</span></span>

- [<span data-ttu-id="3786e-154">Värbamistaotlus</span><span class="sxs-lookup"><span data-stu-id="3786e-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="3786e-155">Värbamistaotluse ametikoht</span><span class="sxs-lookup"><span data-stu-id="3786e-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="3786e-156">Värbamistaotluse oskus</span><span class="sxs-lookup"><span data-stu-id="3786e-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="3786e-157">Värbamistaotluse haridus</span><span class="sxs-lookup"><span data-stu-id="3786e-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="3786e-158">Värbamistaotluse asukoht</span><span class="sxs-lookup"><span data-stu-id="3786e-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="3786e-159">Suvandikomplektid.</span><span class="sxs-lookup"><span data-stu-id="3786e-159">Option sets:</span></span>

- [<span data-ttu-id="3786e-160">Töö vabastuse olek</span><span class="sxs-lookup"><span data-stu-id="3786e-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="3786e-161">Värbamistaotluse ametikoha olek</span><span class="sxs-lookup"><span data-stu-id="3786e-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="3786e-162">Värbamistaotluse olek</span><span class="sxs-lookup"><span data-stu-id="3786e-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="3786e-163">Regulatiivse töö kategooria</span><span class="sxs-lookup"><span data-stu-id="3786e-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="3786e-164">Palgatav kandidaat ja seotud üksused ning suvandikomplektid</span><span class="sxs-lookup"><span data-stu-id="3786e-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="3786e-165">Näidispäring:</span><span class="sxs-lookup"><span data-stu-id="3786e-165">Example query:</span></span>

- [<span data-ttu-id="3786e-166">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="3786e-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="3786e-167">Üksused:</span><span class="sxs-lookup"><span data-stu-id="3786e-167">Entities:</span></span>

- [<span data-ttu-id="3786e-168">Palgatav kandidaat</span><span class="sxs-lookup"><span data-stu-id="3786e-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="3786e-169">Isik</span><span class="sxs-lookup"><span data-stu-id="3786e-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="3786e-170">Isiku haridus</span><span class="sxs-lookup"><span data-stu-id="3786e-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="3786e-171">Isiku töökogemus</span><span class="sxs-lookup"><span data-stu-id="3786e-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="3786e-172">Isiku aadress</span><span class="sxs-lookup"><span data-stu-id="3786e-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="3786e-173">Osapoole kontakt</span><span class="sxs-lookup"><span data-stu-id="3786e-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="3786e-174">Isiku oskus</span><span class="sxs-lookup"><span data-stu-id="3786e-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="3786e-175">Hindamise tase</span><span class="sxs-lookup"><span data-stu-id="3786e-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="3786e-176">Isikutunnistus</span><span class="sxs-lookup"><span data-stu-id="3786e-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="3786e-177">Tunnistuse tüüp</span><span class="sxs-lookup"><span data-stu-id="3786e-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="3786e-178">Isiku skriining</span><span class="sxs-lookup"><span data-stu-id="3786e-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="3786e-179">Skriiningu tüübid</span><span class="sxs-lookup"><span data-stu-id="3786e-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="3786e-180">Isiku ID-number</span><span class="sxs-lookup"><span data-stu-id="3786e-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="3786e-181">Suvandikomplektid.</span><span class="sxs-lookup"><span data-stu-id="3786e-181">Option sets:</span></span>

- [<span data-ttu-id="3786e-182">Kandidaadi integratsiooni tulemus</span><span class="sxs-lookup"><span data-stu-id="3786e-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="3786e-183">Tühi Jah Ei</span><span class="sxs-lookup"><span data-stu-id="3786e-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="3786e-184">Lõpuleviimise olek</span><span class="sxs-lookup"><span data-stu-id="3786e-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="3786e-185">Kontakti tüüp</span><span class="sxs-lookup"><span data-stu-id="3786e-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="3786e-186">Hariduse ainepunktide alus</span><span class="sxs-lookup"><span data-stu-id="3786e-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="3786e-187">Sugu</span><span class="sxs-lookup"><span data-stu-id="3786e-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="3786e-188">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="3786e-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="3786e-189">Kuud aastast</span><span class="sxs-lookup"><span data-stu-id="3786e-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="3786e-190">Ei Jah</span><span class="sxs-lookup"><span data-stu-id="3786e-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="3786e-191">Perioodi ühik</span><span class="sxs-lookup"><span data-stu-id="3786e-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="3786e-192">Skriiningu sagedus</span><span class="sxs-lookup"><span data-stu-id="3786e-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="3786e-193">Skriiningu sageduse loomise vorm</span><span class="sxs-lookup"><span data-stu-id="3786e-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="3786e-194">Oskuse taseme tüüp</span><span class="sxs-lookup"><span data-stu-id="3786e-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="3786e-195">Vt ka</span><span class="sxs-lookup"><span data-stu-id="3786e-195">See also</span></span>

[<span data-ttu-id="3786e-196">Kandidaatide värbamine</span><span class="sxs-lookup"><span data-stu-id="3786e-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="3786e-197">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="3786e-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="3786e-198">Microsoft Dataverse'i Web API kasutamine</span><span class="sxs-lookup"><span data-stu-id="3786e-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="3786e-199">Suvandikomplektide loomine ja värskendamine Web API abil</span><span class="sxs-lookup"><span data-stu-id="3786e-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>