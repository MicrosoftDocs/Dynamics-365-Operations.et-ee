---
title: Isikutunnistus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isikutunnistus.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055192"
---
# <a name="person-certificate"></a><span data-ttu-id="e166e-103">Isikutunnistus</span><span class="sxs-lookup"><span data-stu-id="e166e-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e166e-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isikutunnistus.</span><span class="sxs-lookup"><span data-stu-id="e166e-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e166e-105">Füüsiline nimi: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="e166e-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="e166e-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e166e-106">Description</span></span>

<span data-ttu-id="e166e-107">See üksus kirjeldab kandidaadi kutsetunnistusi.</span><span class="sxs-lookup"><span data-stu-id="e166e-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e166e-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="e166e-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="e166e-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="e166e-109">Properties</span></span>

| <span data-ttu-id="e166e-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="e166e-110">Property</span></span><br><span data-ttu-id="e166e-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="e166e-111">**Physical name**</span></span><br><span data-ttu-id="e166e-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="e166e-112">**_Type_**</span></span> | <span data-ttu-id="e166e-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="e166e-113">Use</span></span> | <span data-ttu-id="e166e-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e166e-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e166e-115">**Isikutunnistuse olemi ID**</span><span class="sxs-lookup"><span data-stu-id="e166e-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="e166e-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="e166e-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="e166e-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e166e-117">*GUID*</span></span> | <span data-ttu-id="e166e-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="e166e-118">Read-only</span></span><br><span data-ttu-id="e166e-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="e166e-119">Required</span></span> | <span data-ttu-id="e166e-120">Süsteemi loodud kordumatu identifikaator isikutunnistuse üksuse kirjele.</span><span class="sxs-lookup"><span data-stu-id="e166e-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="e166e-121">**Osapoole number**</span><span class="sxs-lookup"><span data-stu-id="e166e-121">**Party Number**</span></span><br><span data-ttu-id="e166e-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="e166e-122">mshr_partynumber</span></span><br><span data-ttu-id="e166e-123">*String*</span><span class="sxs-lookup"><span data-stu-id="e166e-123">*String*</span></span> | <span data-ttu-id="e166e-124">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="e166e-124">Read/write</span></span><br><span data-ttu-id="e166e-125">Nõutav</span><span class="sxs-lookup"><span data-stu-id="e166e-125">Required</span></span> | <span data-ttu-id="e166e-126">Kandidaadi osapoole (isiku) ID.</span><span class="sxs-lookup"><span data-stu-id="e166e-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="e166e-127">**Isiku ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="e166e-127">**Person ID Value**</span></span><br><span data-ttu-id="e166e-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="e166e-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="e166e-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e166e-129">*GUID*</span></span> | <span data-ttu-id="e166e-130">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="e166e-130">Read-only</span></span><br><span data-ttu-id="e166e-131">Nõutav</span><span class="sxs-lookup"><span data-stu-id="e166e-131">Required</span></span><br><span data-ttu-id="e166e-132">Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="e166e-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="e166e-133">Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="e166e-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="e166e-134">**Sertifikaadi tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="e166e-134">**Certificate Type ID**</span></span><br><span data-ttu-id="e166e-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="e166e-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="e166e-136">*String*</span><span class="sxs-lookup"><span data-stu-id="e166e-136">*String*</span></span> | <span data-ttu-id="e166e-137">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="e166e-137">Read/write</span></span><br><span data-ttu-id="e166e-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="e166e-138">Required</span></span> |  <span data-ttu-id="e166e-139">Human Resourcesis määratletud serditüübi identifikaator.</span><span class="sxs-lookup"><span data-stu-id="e166e-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="e166e-140">**Sertifikaadi tüübi ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="e166e-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="e166e-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="e166e-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="e166e-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e166e-142">*GUID*</span></span> | <span data-ttu-id="e166e-143">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="e166e-143">Read-only</span></span><br><span data-ttu-id="e166e-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="e166e-144">Required</span></span><br><span data-ttu-id="e166e-145">Võõrvõti: mshr_hcmcertificatetypeentityid olemist mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="e166e-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="e166e-146">Seostatud üksuse serditüübi süsteemi loodud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="e166e-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="e166e-147">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="e166e-147">**Start Date**</span></span><br><span data-ttu-id="e166e-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="e166e-148">mshr_startdate</span></span><br><span data-ttu-id="e166e-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="e166e-149">*Datetime*</span></span> | <span data-ttu-id="e166e-150">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="e166e-150">Read/write</span></span><br><span data-ttu-id="e166e-151">Nõutav</span><span class="sxs-lookup"><span data-stu-id="e166e-151">Required</span></span> | <span data-ttu-id="e166e-152">Serdi väljastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="e166e-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="e166e-153">**Lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="e166e-153">**End Date**</span></span><br><span data-ttu-id="e166e-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="e166e-154">mshr_enddate</span></span><br><span data-ttu-id="e166e-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="e166e-155">*Datetime*</span></span> | <span data-ttu-id="e166e-156">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="e166e-156">Read/write</span></span><br><span data-ttu-id="e166e-157">Valikuline</span><span class="sxs-lookup"><span data-stu-id="e166e-157">Optional</span></span> | <span data-ttu-id="e166e-158">Sertifikaadi aegumise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="e166e-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="e166e-159">**Märkmed**</span><span class="sxs-lookup"><span data-stu-id="e166e-159">**Notes**</span></span><br><span data-ttu-id="e166e-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="e166e-160">mshr_notes</span></span><br><span data-ttu-id="e166e-161">*String*</span><span class="sxs-lookup"><span data-stu-id="e166e-161">*String*</span></span> | <span data-ttu-id="e166e-162">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="e166e-162">Read/write</span></span><br><span data-ttu-id="e166e-163">Valikuline</span><span class="sxs-lookup"><span data-stu-id="e166e-163">Optional</span></span> | <span data-ttu-id="e166e-164">Märkused värbamishalduritele ja värbajatele kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="e166e-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="e166e-165">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="e166e-165">**Primary Field**</span></span><br><span data-ttu-id="e166e-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e166e-166">mshr_primaryfield</span></span><br><span data-ttu-id="e166e-167">*String*</span><span class="sxs-lookup"><span data-stu-id="e166e-167">*String*</span></span> | <span data-ttu-id="e166e-168">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="e166e-168">Read-only</span></span><br><span data-ttu-id="e166e-169">Nõutav</span><span class="sxs-lookup"><span data-stu-id="e166e-169">Required</span></span> |  <span data-ttu-id="e166e-170">Väli, mida kasutatakse üksusekirje esmase ID-na.</span><span class="sxs-lookup"><span data-stu-id="e166e-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="e166e-171">Osapoole numbri, sertifikaadi tüübi ID ja alguskuupäeva kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="e166e-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e166e-172">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e166e-172">See also</span></span>

[<span data-ttu-id="e166e-173">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="e166e-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e166e-174">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="e166e-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]