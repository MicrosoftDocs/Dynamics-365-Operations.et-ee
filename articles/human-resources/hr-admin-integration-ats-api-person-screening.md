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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125373"
---
# <a name="person-screening"></a><span data-ttu-id="eaa7b-103">Isiku skriining</span><span class="sxs-lookup"><span data-stu-id="eaa7b-103">Person screening</span></span>

<span data-ttu-id="eaa7b-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku skriinig.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="eaa7b-105">Füüsiline nimi: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="eaa7b-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="eaa7b-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="eaa7b-106">Description</span></span>

<span data-ttu-id="eaa7b-107">See üksus kirjeldab skriininguid, mille kandidaat on läbinud või peab tööle võtmiseks läbima.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="eaa7b-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="eaa7b-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="eaa7b-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="eaa7b-109">Properties</span></span>

| <span data-ttu-id="eaa7b-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="eaa7b-110">Property</span></span><br><span data-ttu-id="eaa7b-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-111">**Physical name**</span></span><br><span data-ttu-id="eaa7b-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-112">**_Type_**</span></span> | <span data-ttu-id="eaa7b-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="eaa7b-113">Use</span></span> | <span data-ttu-id="eaa7b-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="eaa7b-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="eaa7b-115">**Isiku skriiningu olemi ID**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="eaa7b-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="eaa7b-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="eaa7b-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-117">*GUID*</span></span> | <span data-ttu-id="eaa7b-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="eaa7b-118">Read-only</span></span><br><span data-ttu-id="eaa7b-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="eaa7b-119">Required</span></span><br><span data-ttu-id="eaa7b-120">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="eaa7b-120">System-generated</span></span> | <span data-ttu-id="eaa7b-121">Isiku skriiningu kirje kordumatu peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="eaa7b-122">**Osapoole number**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-122">**Party Number**</span></span><br><span data-ttu-id="eaa7b-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="eaa7b-123">mshr_partynumber</span></span><br><span data-ttu-id="eaa7b-124">*String*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-124">*String*</span></span> | <span data-ttu-id="eaa7b-125">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="eaa7b-125">Read/write</span></span><br><span data-ttu-id="eaa7b-126">Nõutav</span><span class="sxs-lookup"><span data-stu-id="eaa7b-126">Required</span></span> | <span data-ttu-id="eaa7b-127">Kandidaadiga seotud osapoole (isiku) number.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="eaa7b-128">**Isiku ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-128">**Person ID Value**</span></span><br><span data-ttu-id="eaa7b-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="eaa7b-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="eaa7b-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-130">*GUID*</span></span> | <span data-ttu-id="eaa7b-131">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="eaa7b-131">Read-only</span></span><br><span data-ttu-id="eaa7b-132">Nõutav</span><span class="sxs-lookup"><span data-stu-id="eaa7b-132">Required</span></span><br><span data-ttu-id="eaa7b-133">Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="eaa7b-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="eaa7b-134">Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="eaa7b-135">**Skriiningu tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-135">**Screening Type ID**</span></span><br><span data-ttu-id="eaa7b-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="eaa7b-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="eaa7b-137">*String*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-137">*String*</span></span> | <span data-ttu-id="eaa7b-138">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="eaa7b-138">Read/write</span></span><br><span data-ttu-id="eaa7b-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="eaa7b-139">Required</span></span><br><span data-ttu-id="eaa7b-140">Võõrvõti: screeningtype</span><span class="sxs-lookup"><span data-stu-id="eaa7b-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="eaa7b-141">Human Resourcesis määratletud skriiningu tüübi identifikaator.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="eaa7b-142">**Skriiningu tüübi ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="eaa7b-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="eaa7b-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="eaa7b-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-144">*GUID*</span></span> | <span data-ttu-id="eaa7b-145">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="eaa7b-145">Read-only</span></span><br><span data-ttu-id="eaa7b-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="eaa7b-146">Required</span></span><br><span data-ttu-id="eaa7b-147">Võõrvõti: mshr_hcmscreeningtypeentityid olemist mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="eaa7b-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="eaa7b-148">Seostatud üksuse skriiningu tüübi kirje süsteemi loodud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="eaa7b-149">**Nõutav kuupäevaks**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-149">**Required By**</span></span><br><span data-ttu-id="eaa7b-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="eaa7b-150">mshr_requiredby</span></span><br><span data-ttu-id="eaa7b-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-151">*Datetime*</span></span> | <span data-ttu-id="eaa7b-152">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="eaa7b-152">Read/write</span></span><br><span data-ttu-id="eaa7b-153">Valikuline</span><span class="sxs-lookup"><span data-stu-id="eaa7b-153">Optional</span></span> | <span data-ttu-id="eaa7b-154">Skriiningu nõutav lõpule viismise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="eaa7b-155">**Olek**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-155">**Status**</span></span><br><span data-ttu-id="eaa7b-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="eaa7b-156">mshr_status</span></span><br><span data-ttu-id="eaa7b-157">*suvandikomplekt mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="eaa7b-158">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="eaa7b-158">Read/write</span></span><br><span data-ttu-id="eaa7b-159">Nõutav</span><span class="sxs-lookup"><span data-stu-id="eaa7b-159">Required</span></span> | <span data-ttu-id="eaa7b-160">Esitab skriiningu jaoks kandidaadi oleku.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="eaa7b-161">**Lõpule viimise kuupäev**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-161">**Completed Date**</span></span><br><span data-ttu-id="eaa7b-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="eaa7b-162">mshr_completeddate</span></span><br><span data-ttu-id="eaa7b-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-163">*Datetime*</span></span> | <span data-ttu-id="eaa7b-164">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="eaa7b-164">Read/write</span></span><br><span data-ttu-id="eaa7b-165">Valikuline</span><span class="sxs-lookup"><span data-stu-id="eaa7b-165">Optional</span></span> | <span data-ttu-id="eaa7b-166">Skriiningu lõpule viimise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="eaa7b-167">**Märkmed**</span><span class="sxs-lookup"><span data-stu-id="eaa7b-167">**Notes**</span></span><br><span data-ttu-id="eaa7b-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="eaa7b-168">mshr_note</span></span><br><span data-ttu-id="eaa7b-169">*String*</span><span class="sxs-lookup"><span data-stu-id="eaa7b-169">*String*</span></span> | <span data-ttu-id="eaa7b-170">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="eaa7b-170">Read/write</span></span><br><span data-ttu-id="eaa7b-171">Valikuline</span><span class="sxs-lookup"><span data-stu-id="eaa7b-171">Optional</span></span> | <span data-ttu-id="eaa7b-172">Märkused värbamishalduritele ja värbajatele kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="eaa7b-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="eaa7b-173">Vt ka</span><span class="sxs-lookup"><span data-stu-id="eaa7b-173">See also</span></span>

[<span data-ttu-id="eaa7b-174">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="eaa7b-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="eaa7b-175">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="eaa7b-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

