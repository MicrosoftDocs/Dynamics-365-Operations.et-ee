---
title: Isikutunnistus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isikutunnistus.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
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
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466516"
---
# <a name="person-certificate"></a><span data-ttu-id="04900-103">Isikutunnistus</span><span class="sxs-lookup"><span data-stu-id="04900-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="04900-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isikutunnistus.</span><span class="sxs-lookup"><span data-stu-id="04900-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="04900-105">Füüsiline nimi: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="04900-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="04900-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="04900-106">Description</span></span>

<span data-ttu-id="04900-107">See üksus kirjeldab kandidaadi kutsetunnistusi.</span><span class="sxs-lookup"><span data-stu-id="04900-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="04900-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="04900-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="04900-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="04900-109">Properties</span></span>

| <span data-ttu-id="04900-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="04900-110">Property</span></span><br><span data-ttu-id="04900-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="04900-111">**Physical name**</span></span><br><span data-ttu-id="04900-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="04900-112">**_Type_**</span></span> | <span data-ttu-id="04900-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="04900-113">Use</span></span> | <span data-ttu-id="04900-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="04900-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="04900-115">**Isikutunnistuse olemi ID**</span><span class="sxs-lookup"><span data-stu-id="04900-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="04900-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="04900-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="04900-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="04900-117">*GUID*</span></span> | <span data-ttu-id="04900-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="04900-118">Read-only</span></span><br><span data-ttu-id="04900-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="04900-119">Required</span></span> | <span data-ttu-id="04900-120">Süsteemi loodud kordumatu identifikaator isikutunnistuse üksuse kirjele.</span><span class="sxs-lookup"><span data-stu-id="04900-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="04900-121">**Osapoole number**</span><span class="sxs-lookup"><span data-stu-id="04900-121">**Party Number**</span></span><br><span data-ttu-id="04900-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="04900-122">mshr_partynumber</span></span><br><span data-ttu-id="04900-123">*String*</span><span class="sxs-lookup"><span data-stu-id="04900-123">*String*</span></span> | <span data-ttu-id="04900-124">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="04900-124">Read/write</span></span><br><span data-ttu-id="04900-125">Nõutav</span><span class="sxs-lookup"><span data-stu-id="04900-125">Required</span></span> | <span data-ttu-id="04900-126">Kandidaadi osapoole (isiku) ID.</span><span class="sxs-lookup"><span data-stu-id="04900-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="04900-127">**Isiku ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="04900-127">**Person ID Value**</span></span><br><span data-ttu-id="04900-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="04900-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="04900-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="04900-129">*GUID*</span></span> | <span data-ttu-id="04900-130">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="04900-130">Read-only</span></span><br><span data-ttu-id="04900-131">Nõutav</span><span class="sxs-lookup"><span data-stu-id="04900-131">Required</span></span><br><span data-ttu-id="04900-132">Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="04900-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="04900-133">Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="04900-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="04900-134">**Sertifikaadi tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="04900-134">**Certificate Type ID**</span></span><br><span data-ttu-id="04900-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="04900-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="04900-136">*String*</span><span class="sxs-lookup"><span data-stu-id="04900-136">*String*</span></span> | <span data-ttu-id="04900-137">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="04900-137">Read/write</span></span><br><span data-ttu-id="04900-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="04900-138">Required</span></span> |  <span data-ttu-id="04900-139">Human Resourcesis määratletud serditüübi identifikaator.</span><span class="sxs-lookup"><span data-stu-id="04900-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="04900-140">**Sertifikaadi tüübi ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="04900-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="04900-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="04900-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="04900-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="04900-142">*GUID*</span></span> | <span data-ttu-id="04900-143">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="04900-143">Read-only</span></span><br><span data-ttu-id="04900-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="04900-144">Required</span></span><br><span data-ttu-id="04900-145">Võõrvõti: mshr_hcmcertificatetypeentityid olemist mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="04900-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="04900-146">Seostatud üksuse serditüübi süsteemi loodud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="04900-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="04900-147">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="04900-147">**Start Date**</span></span><br><span data-ttu-id="04900-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="04900-148">mshr_startdate</span></span><br><span data-ttu-id="04900-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="04900-149">*Datetime*</span></span> | <span data-ttu-id="04900-150">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="04900-150">Read/write</span></span><br><span data-ttu-id="04900-151">Nõutav</span><span class="sxs-lookup"><span data-stu-id="04900-151">Required</span></span> | <span data-ttu-id="04900-152">Serdi väljastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="04900-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="04900-153">**Lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="04900-153">**End Date**</span></span><br><span data-ttu-id="04900-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="04900-154">mshr_enddate</span></span><br><span data-ttu-id="04900-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="04900-155">*Datetime*</span></span> | <span data-ttu-id="04900-156">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="04900-156">Read/write</span></span><br><span data-ttu-id="04900-157">Valikuline</span><span class="sxs-lookup"><span data-stu-id="04900-157">Optional</span></span> | <span data-ttu-id="04900-158">Sertifikaadi aegumise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="04900-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="04900-159">**Märkmed**</span><span class="sxs-lookup"><span data-stu-id="04900-159">**Notes**</span></span><br><span data-ttu-id="04900-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="04900-160">mshr_notes</span></span><br><span data-ttu-id="04900-161">*String*</span><span class="sxs-lookup"><span data-stu-id="04900-161">*String*</span></span> | <span data-ttu-id="04900-162">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="04900-162">Read/write</span></span><br><span data-ttu-id="04900-163">Valikuline</span><span class="sxs-lookup"><span data-stu-id="04900-163">Optional</span></span> | <span data-ttu-id="04900-164">Märkused värbamishalduritele ja värbajatele kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="04900-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="04900-165">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="04900-165">**Primary Field**</span></span><br><span data-ttu-id="04900-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="04900-166">mshr_primaryfield</span></span><br><span data-ttu-id="04900-167">*String*</span><span class="sxs-lookup"><span data-stu-id="04900-167">*String*</span></span> | <span data-ttu-id="04900-168">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="04900-168">Read-only</span></span><br><span data-ttu-id="04900-169">Nõutav</span><span class="sxs-lookup"><span data-stu-id="04900-169">Required</span></span> |  <span data-ttu-id="04900-170">Väli, mida kasutatakse üksusekirje esmase ID-na.</span><span class="sxs-lookup"><span data-stu-id="04900-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="04900-171">Osapoole numbri, sertifikaadi tüübi ID ja alguskuupäeva kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="04900-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="04900-172">Vt ka</span><span class="sxs-lookup"><span data-stu-id="04900-172">See also</span></span>

[<span data-ttu-id="04900-173">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="04900-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="04900-174">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="04900-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]