---
title: Palgaarvestuse integratsiooni API tutvustus
description: See teema kirjeldab Dynamics 365 Human Resources palgaarvestuse integratsiooni API-d.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a7be5ad42642de48ffdb2731a1300a953c5ede4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022759"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="e01bc-103">Palgaarvestuse integratsiooni API tutvustus</span><span class="sxs-lookup"><span data-stu-id="e01bc-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e01bc-104">See dokument kirjeldab Dynamics 365 Human Resources palgaarvestuse integratsiooni API-d.</span><span class="sxs-lookup"><span data-stu-id="e01bc-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="e01bc-105">API võimaldab sujuvaid otsast otsani integratsioone personaliosakonna ja partnerite palgasüsteemide vahel.</span><span class="sxs-lookup"><span data-stu-id="e01bc-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="e01bc-106">Integreeritud kogemus algab personaliosakonna töötaja profiili, palga ja mahaarvamise ning panuse teabega.</span><span class="sxs-lookup"><span data-stu-id="e01bc-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="e01bc-107">Kui palkate töötaja ja sisestate nõutava profiili ning sisestate teabe personaliosakonna süsteemi, tõmbab palgasüsteem selle teabe palgaarvestuse töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="e01bc-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="e01bc-108">Võetakse ka kõiki töötajale tehtud uuendusi või palgateavet hilisemaks maksekäitumiseks.</span><span class="sxs-lookup"><span data-stu-id="e01bc-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Palgaarvestuse integratsiooni voog](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="e01bc-110">Integratsiooni lubamiseks on personaliosakond sisaldanud järgmisi komponente.</span><span class="sxs-lookup"><span data-stu-id="e01bc-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="e01bc-111">Funktsioon töötaja staatuse muutmiseks kui "valmis makseks"</span><span class="sxs-lookup"><span data-stu-id="e01bc-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="e01bc-112">Integratsiooni API, mis avab uued funktsioonid rakenduste integreerimiseks</span><span class="sxs-lookup"><span data-stu-id="e01bc-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="e01bc-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="e01bc-113">Microsoft Dataverse</span></span>

<span data-ttu-id="e01bc-114">See API on ehitatud rakendusele Microsoft Dataverse (varem Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="e01bc-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="e01bc-115">Kogu RESTful interaktsioon selle API-ga toimub Microsoft Dataverse'i veebi API kaudu, mis kasutab OData.</span><span class="sxs-lookup"><span data-stu-id="e01bc-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="e01bc-116">See API on Dataverse'i Web API alamkogum.</span><span class="sxs-lookup"><span data-stu-id="e01bc-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="e01bc-117">Dataverse'i WEB API määratleb sellised omadused nagu autentimine, SLA-d, partii, samaaegsuse kontrolli ja tõrketöötluse.</span><span class="sxs-lookup"><span data-stu-id="e01bc-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="e01bc-118">Lisateavet Microsoft Dataverse'i Web API kohta leidke alpoolt.</span><span class="sxs-lookup"><span data-stu-id="e01bc-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="e01bc-119">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="e01bc-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="e01bc-120">Microsoft Dataverse'i Web API kasutamine</span><span class="sxs-lookup"><span data-stu-id="e01bc-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="e01bc-121">Microsoft Dataverse'i arendaja juhend</span><span class="sxs-lookup"><span data-stu-id="e01bc-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="e01bc-122">See dokumentatsioon sisaldab üksikasju ja arendaja juhendeid Dataverse Web API kasutamiseks, sh järgmisi teemasid.</span><span class="sxs-lookup"><span data-stu-id="e01bc-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="e01bc-123">Autendi Microsoft Dataverse-ga üle veebi-API</span><span class="sxs-lookup"><span data-stu-id="e01bc-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="e01bc-124">Soorita toimingud veebi API abil</span><span class="sxs-lookup"><span data-stu-id="e01bc-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="e01bc-125">Kasutage veebi API-s Postmani</span><span class="sxs-lookup"><span data-stu-id="e01bc-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="e01bc-126">Kasuta muudatuste jälitamist andmete sünkroonimiseks välissüsteemidega</span><span class="sxs-lookup"><span data-stu-id="e01bc-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="e01bc-127">Virtuaalsed tabelid rakendusele Human Resources Dataverse'is</span><span class="sxs-lookup"><span data-stu-id="e01bc-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="e01bc-128">Palgaarvestuse integratsiooni API lõpp-punktid kasutavad rakenduse Microsoft Dataverse virtuaalse tabeli platvormi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="e01bc-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="e01bc-129">Vaikimisi ei juurutata virtuaalseid tabeleid ja nendega seotud API-lõpp-punkte Human Resources'i keskkondades, võimaldades organisatsioonidel määrata, millised OData lõpp-punktid keskkonnaga kokku puutuvad.</span><span class="sxs-lookup"><span data-stu-id="e01bc-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="e01bc-130">API kasutamiseks peavad keskkonna jaoks olema loodud virtuaalsed tabelid rakenduse Human Resources olemite jaoks.</span><span class="sxs-lookup"><span data-stu-id="e01bc-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="e01bc-131">Lisateavet API jaoks virtuaaltabelite loomise kohta leiate jaotisest [Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="e01bc-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="e01bc-132">Andmemudel</span><span class="sxs-lookup"><span data-stu-id="e01bc-132">Data model</span></span>

<span data-ttu-id="e01bc-133">Järgmine diagramm illustreerib seoseid API sees.</span><span class="sxs-lookup"><span data-stu-id="e01bc-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="e01bc-134">Mitmetel tüüpidel on võõrvõtmeid rakenduse Human Resources teiste, olemasolevate olemite jaoks, mida siin ei ole kujutatud.</span><span class="sxs-lookup"><span data-stu-id="e01bc-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="e01bc-135">See dokument annab teavet üksuste kohta, mis on integratsioonistsenaariumide palgaarvestusel spetsiifilised.</span><span class="sxs-lookup"><span data-stu-id="e01bc-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="e01bc-136">Siiski on Dataverse'i Web APIs mitmeid teisi olemeid personaliosakonna jaoks, mis võivad samuti olla teie integratsioonile asjakohased.</span><span class="sxs-lookup"><span data-stu-id="e01bc-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="e01bc-137">Mõnedele neile üksustele viidatakse võõrvõtme seostes või navigeerimisatribuutides.</span><span class="sxs-lookup"><span data-stu-id="e01bc-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Palgaarvestuse integratsiooni API andmemudel](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="e01bc-139">Palgatöötaja ja seotud üksused</span><span class="sxs-lookup"><span data-stu-id="e01bc-139">Payroll employee and related entities</span></span>

<span data-ttu-id="e01bc-140">Üksused:</span><span class="sxs-lookup"><span data-stu-id="e01bc-140">Entities:</span></span>

- [<span data-ttu-id="e01bc-141">Palgaarvestuse töövõtja</span><span class="sxs-lookup"><span data-stu-id="e01bc-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="e01bc-142">Palgaarvestuse töötaja aadress</span><span class="sxs-lookup"><span data-stu-id="e01bc-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="e01bc-143">Palgaarvestuse põhipalgaplaan</span><span class="sxs-lookup"><span data-stu-id="e01bc-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="e01bc-144">Palga positsiooni töö</span><span class="sxs-lookup"><span data-stu-id="e01bc-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="e01bc-145">Palga positsioon</span><span class="sxs-lookup"><span data-stu-id="e01bc-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="e01bc-146">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e01bc-146">See also</span></span>

[<span data-ttu-id="e01bc-147">Palgaarvestuse üksuste loomine ja ülevaatus</span><span class="sxs-lookup"><span data-stu-id="e01bc-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="e01bc-148">Human Resourcesi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e01bc-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="e01bc-149">Human Resourcesi (personaliosakonna) ühiskasutuses parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e01bc-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="e01bc-150">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="e01bc-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="e01bc-151">Microsoft Dataverse'i Web API kasutamine</span><span class="sxs-lookup"><span data-stu-id="e01bc-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]