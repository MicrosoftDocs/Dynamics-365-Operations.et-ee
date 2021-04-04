---
title: Isiku skriining
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku skriinig.
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
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467237"
---
# <a name="person-screening"></a><span data-ttu-id="41647-103">Isiku skriining</span><span class="sxs-lookup"><span data-stu-id="41647-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="41647-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku skriinig.</span><span class="sxs-lookup"><span data-stu-id="41647-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="41647-105">Füüsiline nimi: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="41647-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="41647-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="41647-106">Description</span></span>

<span data-ttu-id="41647-107">See üksus kirjeldab skriininguid, mille kandidaat on läbinud või peab tööle võtmiseks läbima.</span><span class="sxs-lookup"><span data-stu-id="41647-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="41647-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="41647-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="41647-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="41647-109">Properties</span></span>

| <span data-ttu-id="41647-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="41647-110">Property</span></span><br><span data-ttu-id="41647-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="41647-111">**Physical name**</span></span><br><span data-ttu-id="41647-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="41647-112">**_Type_**</span></span> | <span data-ttu-id="41647-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="41647-113">Use</span></span> | <span data-ttu-id="41647-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="41647-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="41647-115">**Isiku skriiningu olemi ID**</span><span class="sxs-lookup"><span data-stu-id="41647-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="41647-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="41647-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="41647-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="41647-117">*GUID*</span></span> | <span data-ttu-id="41647-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="41647-118">Read-only</span></span><br><span data-ttu-id="41647-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="41647-119">Required</span></span><br><span data-ttu-id="41647-120">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="41647-120">System-generated</span></span> | <span data-ttu-id="41647-121">Isiku skriiningu kirje kordumatu peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="41647-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="41647-122">**Osapoole number**</span><span class="sxs-lookup"><span data-stu-id="41647-122">**Party Number**</span></span><br><span data-ttu-id="41647-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="41647-123">mshr_partynumber</span></span><br><span data-ttu-id="41647-124">*String*</span><span class="sxs-lookup"><span data-stu-id="41647-124">*String*</span></span> | <span data-ttu-id="41647-125">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="41647-125">Read/write</span></span><br><span data-ttu-id="41647-126">Nõutav</span><span class="sxs-lookup"><span data-stu-id="41647-126">Required</span></span> | <span data-ttu-id="41647-127">Kandidaadiga seotud osapoole (isiku) number.</span><span class="sxs-lookup"><span data-stu-id="41647-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="41647-128">**Isiku ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="41647-128">**Person ID Value**</span></span><br><span data-ttu-id="41647-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="41647-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="41647-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="41647-130">*GUID*</span></span> | <span data-ttu-id="41647-131">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="41647-131">Read-only</span></span><br><span data-ttu-id="41647-132">Nõutav</span><span class="sxs-lookup"><span data-stu-id="41647-132">Required</span></span><br><span data-ttu-id="41647-133">Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="41647-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="41647-134">Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="41647-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="41647-135">**Skriiningu tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="41647-135">**Screening Type ID**</span></span><br><span data-ttu-id="41647-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="41647-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="41647-137">*String*</span><span class="sxs-lookup"><span data-stu-id="41647-137">*String*</span></span> | <span data-ttu-id="41647-138">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="41647-138">Read/write</span></span><br><span data-ttu-id="41647-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="41647-139">Required</span></span><br><span data-ttu-id="41647-140">Võõrvõti: screeningtype</span><span class="sxs-lookup"><span data-stu-id="41647-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="41647-141">Human Resourcesis määratletud skriiningu tüübi identifikaator.</span><span class="sxs-lookup"><span data-stu-id="41647-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="41647-142">**Skriiningu tüübi ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="41647-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="41647-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="41647-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="41647-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="41647-144">*GUID*</span></span> | <span data-ttu-id="41647-145">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="41647-145">Read-only</span></span><br><span data-ttu-id="41647-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="41647-146">Required</span></span><br><span data-ttu-id="41647-147">Võõrvõti: mshr_hcmscreeningtypeentityid olemist mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="41647-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="41647-148">Seostatud üksuse skriiningu tüübi kirje süsteemi loodud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="41647-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="41647-149">**Nõutav kuupäevaks**</span><span class="sxs-lookup"><span data-stu-id="41647-149">**Required By**</span></span><br><span data-ttu-id="41647-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="41647-150">mshr_requiredby</span></span><br><span data-ttu-id="41647-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="41647-151">*Datetime*</span></span> | <span data-ttu-id="41647-152">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="41647-152">Read/write</span></span><br><span data-ttu-id="41647-153">Valikuline</span><span class="sxs-lookup"><span data-stu-id="41647-153">Optional</span></span> | <span data-ttu-id="41647-154">Skriiningu nõutav lõpule viismise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="41647-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="41647-155">**Olek**</span><span class="sxs-lookup"><span data-stu-id="41647-155">**Status**</span></span><br><span data-ttu-id="41647-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="41647-156">mshr_status</span></span><br><span data-ttu-id="41647-157">*suvandikomplekt mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="41647-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="41647-158">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="41647-158">Read/write</span></span><br><span data-ttu-id="41647-159">Nõutav</span><span class="sxs-lookup"><span data-stu-id="41647-159">Required</span></span> | <span data-ttu-id="41647-160">Esitab skriiningu jaoks kandidaadi oleku.</span><span class="sxs-lookup"><span data-stu-id="41647-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="41647-161">**Lõpule viimise kuupäev**</span><span class="sxs-lookup"><span data-stu-id="41647-161">**Completed Date**</span></span><br><span data-ttu-id="41647-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="41647-162">mshr_completeddate</span></span><br><span data-ttu-id="41647-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="41647-163">*Datetime*</span></span> | <span data-ttu-id="41647-164">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="41647-164">Read/write</span></span><br><span data-ttu-id="41647-165">Valikuline</span><span class="sxs-lookup"><span data-stu-id="41647-165">Optional</span></span> | <span data-ttu-id="41647-166">Skriiningu lõpule viimise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="41647-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="41647-167">**Märkmed**</span><span class="sxs-lookup"><span data-stu-id="41647-167">**Notes**</span></span><br><span data-ttu-id="41647-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="41647-168">mshr_note</span></span><br><span data-ttu-id="41647-169">*String*</span><span class="sxs-lookup"><span data-stu-id="41647-169">*String*</span></span> | <span data-ttu-id="41647-170">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="41647-170">Read/write</span></span><br><span data-ttu-id="41647-171">Valikuline</span><span class="sxs-lookup"><span data-stu-id="41647-171">Optional</span></span> | <span data-ttu-id="41647-172">Märkused värbamishalduritele ja värbajatele kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="41647-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="41647-173">Vt ka</span><span class="sxs-lookup"><span data-stu-id="41647-173">See also</span></span>

[<span data-ttu-id="41647-174">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="41647-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="41647-175">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="41647-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]