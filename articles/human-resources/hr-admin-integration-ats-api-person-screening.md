---
title: Isiku skriining
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku skriinig.
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
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059276"
---
# <a name="person-screening"></a><span data-ttu-id="75eb5-103">Isiku skriining</span><span class="sxs-lookup"><span data-stu-id="75eb5-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="75eb5-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku skriinig.</span><span class="sxs-lookup"><span data-stu-id="75eb5-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="75eb5-105">Füüsiline nimi: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="75eb5-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="75eb5-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="75eb5-106">Description</span></span>

<span data-ttu-id="75eb5-107">See üksus kirjeldab skriininguid, mille kandidaat on läbinud või peab tööle võtmiseks läbima.</span><span class="sxs-lookup"><span data-stu-id="75eb5-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="75eb5-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="75eb5-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="75eb5-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="75eb5-109">Properties</span></span>

| <span data-ttu-id="75eb5-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="75eb5-110">Property</span></span><br><span data-ttu-id="75eb5-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="75eb5-111">**Physical name**</span></span><br><span data-ttu-id="75eb5-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="75eb5-112">**_Type_**</span></span> | <span data-ttu-id="75eb5-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="75eb5-113">Use</span></span> | <span data-ttu-id="75eb5-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="75eb5-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="75eb5-115">**Isiku skriiningu olemi ID**</span><span class="sxs-lookup"><span data-stu-id="75eb5-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="75eb5-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="75eb5-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="75eb5-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="75eb5-117">*GUID*</span></span> | <span data-ttu-id="75eb5-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="75eb5-118">Read-only</span></span><br><span data-ttu-id="75eb5-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="75eb5-119">Required</span></span><br><span data-ttu-id="75eb5-120">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="75eb5-120">System-generated</span></span> | <span data-ttu-id="75eb5-121">Isiku skriiningu kirje kordumatu peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="75eb5-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="75eb5-122">**Osapoole number**</span><span class="sxs-lookup"><span data-stu-id="75eb5-122">**Party Number**</span></span><br><span data-ttu-id="75eb5-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="75eb5-123">mshr_partynumber</span></span><br><span data-ttu-id="75eb5-124">*String*</span><span class="sxs-lookup"><span data-stu-id="75eb5-124">*String*</span></span> | <span data-ttu-id="75eb5-125">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="75eb5-125">Read/write</span></span><br><span data-ttu-id="75eb5-126">Nõutav</span><span class="sxs-lookup"><span data-stu-id="75eb5-126">Required</span></span> | <span data-ttu-id="75eb5-127">Kandidaadiga seotud osapoole (isiku) number.</span><span class="sxs-lookup"><span data-stu-id="75eb5-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="75eb5-128">**Isiku ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="75eb5-128">**Person ID Value**</span></span><br><span data-ttu-id="75eb5-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="75eb5-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="75eb5-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="75eb5-130">*GUID*</span></span> | <span data-ttu-id="75eb5-131">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="75eb5-131">Read-only</span></span><br><span data-ttu-id="75eb5-132">Nõutav</span><span class="sxs-lookup"><span data-stu-id="75eb5-132">Required</span></span><br><span data-ttu-id="75eb5-133">Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="75eb5-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="75eb5-134">Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="75eb5-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="75eb5-135">**Skriiningu tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="75eb5-135">**Screening Type ID**</span></span><br><span data-ttu-id="75eb5-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="75eb5-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="75eb5-137">*String*</span><span class="sxs-lookup"><span data-stu-id="75eb5-137">*String*</span></span> | <span data-ttu-id="75eb5-138">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="75eb5-138">Read/write</span></span><br><span data-ttu-id="75eb5-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="75eb5-139">Required</span></span><br><span data-ttu-id="75eb5-140">Võõrvõti: screeningtype</span><span class="sxs-lookup"><span data-stu-id="75eb5-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="75eb5-141">Human Resourcesis määratletud skriiningu tüübi identifikaator.</span><span class="sxs-lookup"><span data-stu-id="75eb5-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="75eb5-142">**Skriiningu tüübi ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="75eb5-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="75eb5-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="75eb5-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="75eb5-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="75eb5-144">*GUID*</span></span> | <span data-ttu-id="75eb5-145">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="75eb5-145">Read-only</span></span><br><span data-ttu-id="75eb5-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="75eb5-146">Required</span></span><br><span data-ttu-id="75eb5-147">Võõrvõti: mshr_hcmscreeningtypeentityid olemist mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="75eb5-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="75eb5-148">Seostatud üksuse skriiningu tüübi kirje süsteemi loodud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="75eb5-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="75eb5-149">**Nõutav kuupäevaks**</span><span class="sxs-lookup"><span data-stu-id="75eb5-149">**Required By**</span></span><br><span data-ttu-id="75eb5-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="75eb5-150">mshr_requiredby</span></span><br><span data-ttu-id="75eb5-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="75eb5-151">*Datetime*</span></span> | <span data-ttu-id="75eb5-152">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="75eb5-152">Read/write</span></span><br><span data-ttu-id="75eb5-153">Valikuline</span><span class="sxs-lookup"><span data-stu-id="75eb5-153">Optional</span></span> | <span data-ttu-id="75eb5-154">Skriiningu nõutav lõpule viismise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="75eb5-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="75eb5-155">**Olek**</span><span class="sxs-lookup"><span data-stu-id="75eb5-155">**Status**</span></span><br><span data-ttu-id="75eb5-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="75eb5-156">mshr_status</span></span><br><span data-ttu-id="75eb5-157">*suvandikomplekt mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="75eb5-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="75eb5-158">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="75eb5-158">Read/write</span></span><br><span data-ttu-id="75eb5-159">Nõutav</span><span class="sxs-lookup"><span data-stu-id="75eb5-159">Required</span></span> | <span data-ttu-id="75eb5-160">Esitab skriiningu jaoks kandidaadi oleku.</span><span class="sxs-lookup"><span data-stu-id="75eb5-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="75eb5-161">**Lõpule viimise kuupäev**</span><span class="sxs-lookup"><span data-stu-id="75eb5-161">**Completed Date**</span></span><br><span data-ttu-id="75eb5-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="75eb5-162">mshr_completeddate</span></span><br><span data-ttu-id="75eb5-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="75eb5-163">*Datetime*</span></span> | <span data-ttu-id="75eb5-164">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="75eb5-164">Read/write</span></span><br><span data-ttu-id="75eb5-165">Valikuline</span><span class="sxs-lookup"><span data-stu-id="75eb5-165">Optional</span></span> | <span data-ttu-id="75eb5-166">Skriiningu lõpule viimise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="75eb5-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="75eb5-167">**Märkmed**</span><span class="sxs-lookup"><span data-stu-id="75eb5-167">**Notes**</span></span><br><span data-ttu-id="75eb5-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="75eb5-168">mshr_note</span></span><br><span data-ttu-id="75eb5-169">*String*</span><span class="sxs-lookup"><span data-stu-id="75eb5-169">*String*</span></span> | <span data-ttu-id="75eb5-170">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="75eb5-170">Read/write</span></span><br><span data-ttu-id="75eb5-171">Valikuline</span><span class="sxs-lookup"><span data-stu-id="75eb5-171">Optional</span></span> | <span data-ttu-id="75eb5-172">Märkused värbamishalduritele ja värbajatele kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="75eb5-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="75eb5-173">Vt ka</span><span class="sxs-lookup"><span data-stu-id="75eb5-173">See also</span></span>

[<span data-ttu-id="75eb5-174">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="75eb5-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="75eb5-175">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="75eb5-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]