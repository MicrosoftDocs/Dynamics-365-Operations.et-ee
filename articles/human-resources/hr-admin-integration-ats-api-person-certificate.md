---
title: Isikutunnistus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isikutunnistus.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 796a57a5f97de08ff8c8440bc00d4dc5ced18f58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798125"
---
# <a name="person-certificate"></a><span data-ttu-id="9f74c-103">Isikutunnistus</span><span class="sxs-lookup"><span data-stu-id="9f74c-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9f74c-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isikutunnistus.</span><span class="sxs-lookup"><span data-stu-id="9f74c-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9f74c-105">Füüsiline nimi: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="9f74c-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="9f74c-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9f74c-106">Description</span></span>

<span data-ttu-id="9f74c-107">See üksus kirjeldab kandidaadi kutsetunnistusi.</span><span class="sxs-lookup"><span data-stu-id="9f74c-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9f74c-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="9f74c-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="9f74c-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="9f74c-109">Properties</span></span>

| <span data-ttu-id="9f74c-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="9f74c-110">Property</span></span><br><span data-ttu-id="9f74c-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="9f74c-111">**Physical name**</span></span><br><span data-ttu-id="9f74c-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="9f74c-112">**_Type_**</span></span> | <span data-ttu-id="9f74c-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="9f74c-113">Use</span></span> | <span data-ttu-id="9f74c-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9f74c-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9f74c-115">**Isikutunnistuse olemi ID**</span><span class="sxs-lookup"><span data-stu-id="9f74c-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="9f74c-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="9f74c-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="9f74c-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9f74c-117">*GUID*</span></span> | <span data-ttu-id="9f74c-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="9f74c-118">Read-only</span></span><br><span data-ttu-id="9f74c-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="9f74c-119">Required</span></span> | <span data-ttu-id="9f74c-120">Süsteemi loodud kordumatu identifikaator isikutunnistuse üksuse kirjele.</span><span class="sxs-lookup"><span data-stu-id="9f74c-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="9f74c-121">**Osapoole number**</span><span class="sxs-lookup"><span data-stu-id="9f74c-121">**Party Number**</span></span><br><span data-ttu-id="9f74c-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="9f74c-122">mshr_partynumber</span></span><br><span data-ttu-id="9f74c-123">*String*</span><span class="sxs-lookup"><span data-stu-id="9f74c-123">*String*</span></span> | <span data-ttu-id="9f74c-124">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="9f74c-124">Read/write</span></span><br><span data-ttu-id="9f74c-125">Nõutav</span><span class="sxs-lookup"><span data-stu-id="9f74c-125">Required</span></span> | <span data-ttu-id="9f74c-126">Kandidaadi osapoole (isiku) ID.</span><span class="sxs-lookup"><span data-stu-id="9f74c-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="9f74c-127">**Isiku ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="9f74c-127">**Person ID Value**</span></span><br><span data-ttu-id="9f74c-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="9f74c-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="9f74c-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9f74c-129">*GUID*</span></span> | <span data-ttu-id="9f74c-130">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="9f74c-130">Read-only</span></span><br><span data-ttu-id="9f74c-131">Nõutav</span><span class="sxs-lookup"><span data-stu-id="9f74c-131">Required</span></span><br><span data-ttu-id="9f74c-132">Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="9f74c-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="9f74c-133">Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9f74c-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="9f74c-134">**Sertifikaadi tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="9f74c-134">**Certificate Type ID**</span></span><br><span data-ttu-id="9f74c-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="9f74c-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="9f74c-136">*String*</span><span class="sxs-lookup"><span data-stu-id="9f74c-136">*String*</span></span> | <span data-ttu-id="9f74c-137">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="9f74c-137">Read/write</span></span><br><span data-ttu-id="9f74c-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="9f74c-138">Required</span></span> |  <span data-ttu-id="9f74c-139">Human Resourcesis määratletud serditüübi identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9f74c-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="9f74c-140">**Sertifikaadi tüübi ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="9f74c-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="9f74c-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="9f74c-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="9f74c-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9f74c-142">*GUID*</span></span> | <span data-ttu-id="9f74c-143">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="9f74c-143">Read-only</span></span><br><span data-ttu-id="9f74c-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="9f74c-144">Required</span></span><br><span data-ttu-id="9f74c-145">Võõrvõti: mshr_hcmcertificatetypeentityid olemist mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="9f74c-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="9f74c-146">Seostatud üksuse serditüübi süsteemi loodud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9f74c-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="9f74c-147">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="9f74c-147">**Start Date**</span></span><br><span data-ttu-id="9f74c-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="9f74c-148">mshr_startdate</span></span><br><span data-ttu-id="9f74c-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="9f74c-149">*Datetime*</span></span> | <span data-ttu-id="9f74c-150">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="9f74c-150">Read/write</span></span><br><span data-ttu-id="9f74c-151">Nõutav</span><span class="sxs-lookup"><span data-stu-id="9f74c-151">Required</span></span> | <span data-ttu-id="9f74c-152">Serdi väljastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="9f74c-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="9f74c-153">**Lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="9f74c-153">**End Date**</span></span><br><span data-ttu-id="9f74c-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="9f74c-154">mshr_enddate</span></span><br><span data-ttu-id="9f74c-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="9f74c-155">*Datetime*</span></span> | <span data-ttu-id="9f74c-156">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="9f74c-156">Read/write</span></span><br><span data-ttu-id="9f74c-157">Valikuline</span><span class="sxs-lookup"><span data-stu-id="9f74c-157">Optional</span></span> | <span data-ttu-id="9f74c-158">Sertifikaadi aegumise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="9f74c-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="9f74c-159">**Märkmed**</span><span class="sxs-lookup"><span data-stu-id="9f74c-159">**Notes**</span></span><br><span data-ttu-id="9f74c-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="9f74c-160">mshr_notes</span></span><br><span data-ttu-id="9f74c-161">*String*</span><span class="sxs-lookup"><span data-stu-id="9f74c-161">*String*</span></span> | <span data-ttu-id="9f74c-162">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="9f74c-162">Read/write</span></span><br><span data-ttu-id="9f74c-163">Valikuline</span><span class="sxs-lookup"><span data-stu-id="9f74c-163">Optional</span></span> | <span data-ttu-id="9f74c-164">Märkused värbamishalduritele ja värbajatele kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f74c-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="9f74c-165">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="9f74c-165">**Primary Field**</span></span><br><span data-ttu-id="9f74c-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="9f74c-166">mshr_primaryfield</span></span><br><span data-ttu-id="9f74c-167">*String*</span><span class="sxs-lookup"><span data-stu-id="9f74c-167">*String*</span></span> | <span data-ttu-id="9f74c-168">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="9f74c-168">Read-only</span></span><br><span data-ttu-id="9f74c-169">Nõutav</span><span class="sxs-lookup"><span data-stu-id="9f74c-169">Required</span></span> |  <span data-ttu-id="9f74c-170">Väli, mida kasutatakse üksusekirje esmase ID-na.</span><span class="sxs-lookup"><span data-stu-id="9f74c-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="9f74c-171">Osapoole numbri, sertifikaadi tüübi ID ja alguskuupäeva kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="9f74c-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9f74c-172">Vt ka</span><span class="sxs-lookup"><span data-stu-id="9f74c-172">See also</span></span>

[<span data-ttu-id="9f74c-173">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="9f74c-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9f74c-174">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="9f74c-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]