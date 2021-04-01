---
title: Osapoole kontakt
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Osapoole kontakt.
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
ms.openlocfilehash: 38f53d402ebe9f9f358281dd3996797a20923056
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125469"
---
# <a name="party-contact"></a><span data-ttu-id="3fb86-103">Osapoole kontakt</span><span class="sxs-lookup"><span data-stu-id="3fb86-103">Party contact</span></span>

<span data-ttu-id="3fb86-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Osapoole kontakt.</span><span class="sxs-lookup"><span data-stu-id="3fb86-104">This topic describes the Party contact entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3fb86-105">Füüsiline nimi: mshr_dirpartycontactentities</span><span class="sxs-lookup"><span data-stu-id="3fb86-105">Physical name: mshr_dirpartycontactentities</span></span>

## <a name="description"></a><span data-ttu-id="3fb86-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3fb86-106">Description</span></span>

<span data-ttu-id="3fb86-107">Seelles olemis kirjeldatakse kandidaadi kontaktandmeid, sealhulgas telefoninumbrit, meiliaadressi ja sotsiaalmeedia kontosid.</span><span class="sxs-lookup"><span data-stu-id="3fb86-107">This entity describes the candidate’s contact information, including phone, email, and social media accounts.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3fb86-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="3fb86-108">JSON representation</span></span>

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a><span data-ttu-id="3fb86-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="3fb86-109">Properties</span></span>

| <span data-ttu-id="3fb86-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="3fb86-110">Property</span></span><br><span data-ttu-id="3fb86-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="3fb86-111">**Physical name**</span></span><br><span data-ttu-id="3fb86-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="3fb86-112">**_Type_**</span></span> | <span data-ttu-id="3fb86-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-113">Use</span></span> | <span data-ttu-id="3fb86-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3fb86-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3fb86-115">**Osapoole kontakti olemi ID**</span><span class="sxs-lookup"><span data-stu-id="3fb86-115">**Party Contact Entity ID**</span></span><br><span data-ttu-id="3fb86-116">mshr_dirpartycontactentityid</span><span class="sxs-lookup"><span data-stu-id="3fb86-116">mshr_dirpartycontactentityid</span></span><br><span data-ttu-id="3fb86-117">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-117">*String*</span></span> | <span data-ttu-id="3fb86-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3fb86-118">Read-only</span></span><br><span data-ttu-id="3fb86-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-119">Required</span></span> | <span data-ttu-id="3fb86-120">Olemi kirje süsteemi loodud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="3fb86-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="3fb86-121">**Osapoole number**</span><span class="sxs-lookup"><span data-stu-id="3fb86-121">**Party Number**</span></span><br><span data-ttu-id="3fb86-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="3fb86-122">mshr_partynumber</span></span><br><span data-ttu-id="3fb86-123">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-123">*String*</span></span> | <span data-ttu-id="3fb86-124">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-124">Read/write</span></span><br><span data-ttu-id="3fb86-125">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-125">Required</span></span> | <span data-ttu-id="3fb86-126">Seotud osapoole (isiku) ID.</span><span class="sxs-lookup"><span data-stu-id="3fb86-126">The ID of the associated party (person) record.</span></span> |
| <span data-ttu-id="3fb86-127">**Isiku ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="3fb86-127">**Person ID Value**</span></span><br><span data-ttu-id="3fb86-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="3fb86-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="3fb86-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3fb86-129">*GUID*</span></span> | <span data-ttu-id="3fb86-130">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3fb86-130">Read-only</span></span><br><span data-ttu-id="3fb86-131">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-131">Required</span></span><br><span data-ttu-id="3fb86-132">Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="3fb86-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="3fb86-133">Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="3fb86-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="3fb86-134">**Asukoha ID**</span><span class="sxs-lookup"><span data-stu-id="3fb86-134">**Location ID**</span></span><br><span data-ttu-id="3fb86-135">mshr_locationid</span><span class="sxs-lookup"><span data-stu-id="3fb86-135">mshr_locationid</span></span><br><span data-ttu-id="3fb86-136">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-136">*String*</span></span> | <span data-ttu-id="3fb86-137">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-137">Read/write</span></span><br><span data-ttu-id="3fb86-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-138">Required</span></span> | <span data-ttu-id="3fb86-139">Aadressikirje asukoha ID.</span><span class="sxs-lookup"><span data-stu-id="3fb86-139">The location ID of the address record.</span></span> <span data-ttu-id="3fb86-140">Seadistamine olemis mshr_logisticspostaladdresslocationcdsentity.</span><span class="sxs-lookup"><span data-stu-id="3fb86-140">Set up in mshr_logisticspostaladdresslocationcdsentity entity.</span></span> |
| <span data-ttu-id="3fb86-141">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="3fb86-141">**Description**</span></span><br><span data-ttu-id="3fb86-142">mshr_description</span><span class="sxs-lookup"><span data-stu-id="3fb86-142">mshr_description</span></span><br><span data-ttu-id="3fb86-143">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-143">*String*</span></span> | <span data-ttu-id="3fb86-144">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-144">Read/write</span></span><br><span data-ttu-id="3fb86-145">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-145">Required</span></span> | <span data-ttu-id="3fb86-146">Kontaktandmete kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3fb86-146">The description of the contact details.</span></span> |
| <span data-ttu-id="3fb86-147">**Tüüp**</span><span class="sxs-lookup"><span data-stu-id="3fb86-147">**Type**</span></span><br><span data-ttu-id="3fb86-148">mshr_type</span><span class="sxs-lookup"><span data-stu-id="3fb86-148">mshr_type</span></span><br><span data-ttu-id="3fb86-149">*Suvandikomplekt mshr_logisticselectronicaddressmethodtype*</span><span class="sxs-lookup"><span data-stu-id="3fb86-149">*mshr_logisticselectronicaddressmethodtype option set*</span></span> | <span data-ttu-id="3fb86-150">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-150">Read/write</span></span><br><span data-ttu-id="3fb86-151">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-151">Required</span></span> | <span data-ttu-id="3fb86-152">Kontaktandmete tüüp.</span><span class="sxs-lookup"><span data-stu-id="3fb86-152">The contact detail type.</span></span> |
| <span data-ttu-id="3fb86-153">**Riigi regiooni kood**</span><span class="sxs-lookup"><span data-stu-id="3fb86-153">**Country Region Code**</span></span><br><span data-ttu-id="3fb86-154">mshr_countryregioncode</span><span class="sxs-lookup"><span data-stu-id="3fb86-154">mshr_countryregioncode</span></span><br><span data-ttu-id="3fb86-155">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-155">*String*</span></span> | <span data-ttu-id="3fb86-156">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-156">Read/write</span></span><br><span data-ttu-id="3fb86-157">Valikuline</span><span class="sxs-lookup"><span data-stu-id="3fb86-157">Optional</span></span> | <span data-ttu-id="3fb86-158">Aadressi riik või regioon.</span><span class="sxs-lookup"><span data-stu-id="3fb86-158">The country or region of the address.</span></span> |
| <span data-ttu-id="3fb86-159">**Lokaator**</span><span class="sxs-lookup"><span data-stu-id="3fb86-159">**Locator**</span></span><br><span data-ttu-id="3fb86-160">mshr_locator</span><span class="sxs-lookup"><span data-stu-id="3fb86-160">mshr_locator</span></span><br><span data-ttu-id="3fb86-161">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-161">*String*</span></span> | <span data-ttu-id="3fb86-162">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-162">Read/write</span></span><br><span data-ttu-id="3fb86-163">Valikuline</span><span class="sxs-lookup"><span data-stu-id="3fb86-163">Optional</span></span> | <span data-ttu-id="3fb86-164">Kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="3fb86-164">The contact details.</span></span> <span data-ttu-id="3fb86-165">Näiteks kui tüübiks on **Meiliaadress**, sisaldab see väli kandidaadi meiliaadressi.</span><span class="sxs-lookup"><span data-stu-id="3fb86-165">For example, if the type is **Email address**, then this field contains the candidate’s email address.</span></span> |
| <span data-ttu-id="3fb86-166">**Lokaatori laiend**</span><span class="sxs-lookup"><span data-stu-id="3fb86-166">**Locator Extension**</span></span><br><span data-ttu-id="3fb86-167">mshr_locatorextension</span><span class="sxs-lookup"><span data-stu-id="3fb86-167">mshr_locatorextension</span></span><br><span data-ttu-id="3fb86-168">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-168">*String*</span></span> | <span data-ttu-id="3fb86-169">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-169">Read/write</span></span><br><span data-ttu-id="3fb86-170">Valikuline</span><span class="sxs-lookup"><span data-stu-id="3fb86-170">Optional</span></span> | <span data-ttu-id="3fb86-171">Lokaatori laiend.</span><span class="sxs-lookup"><span data-stu-id="3fb86-171">The locator extension.</span></span> <span data-ttu-id="3fb86-172">Kui tüübiks on näiteks **Telefon**, sisaldab see atribuut telefoninumbri laiendit.</span><span class="sxs-lookup"><span data-stu-id="3fb86-172">For example, if the type is **Phone**, then this property would contain the phone number extension.</span></span> |
| <span data-ttu-id="3fb86-173">**On mobiil**</span><span class="sxs-lookup"><span data-stu-id="3fb86-173">**Is Mobile**</span></span><br><span data-ttu-id="3fb86-174">mshr_ismobile</span><span class="sxs-lookup"><span data-stu-id="3fb86-174">mshr_ismobile</span></span><br><span data-ttu-id="3fb86-175">*suvandikomplekt mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="3fb86-175">*mshr_noyes option set*</span></span> | <span data-ttu-id="3fb86-176">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-176">Read/write</span></span><br><span data-ttu-id="3fb86-177">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-177">Required</span></span> | <span data-ttu-id="3fb86-178">Määratleb, kas telefoninumber on mobiiltelefon.</span><span class="sxs-lookup"><span data-stu-id="3fb86-178">Specifies whether the phone is a mobile number.</span></span> |
| <span data-ttu-id="3fb86-179">**On kiirsõnumside**</span><span class="sxs-lookup"><span data-stu-id="3fb86-179">**Is Instant Message**</span></span><br><span data-ttu-id="3fb86-180">mshr_isinstantmessage</span><span class="sxs-lookup"><span data-stu-id="3fb86-180">mshr_isinstantmessage</span></span><br><span data-ttu-id="3fb86-181">*suvandikomplekt mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="3fb86-181">*mshr_noyes option set*</span></span> | <span data-ttu-id="3fb86-182">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-182">Read/write</span></span><br><span data-ttu-id="3fb86-183">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-183">Required</span></span> | <span data-ttu-id="3fb86-184">Määrab, kas telefon on kiirsõnumside jaoks lubatud.</span><span class="sxs-lookup"><span data-stu-id="3fb86-184">Specifies whether the phone is enabled for instant messaging.</span></span> |
| <span data-ttu-id="3fb86-185">**On esmane**</span><span class="sxs-lookup"><span data-stu-id="3fb86-185">**Is Primary**</span></span><br><span data-ttu-id="3fb86-186">mshr_isprimary</span><span class="sxs-lookup"><span data-stu-id="3fb86-186">mshr_isprimary</span></span><br><span data-ttu-id="3fb86-187">*suvandikomplekt mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="3fb86-187">*mshr_noyes option set*</span></span> | <span data-ttu-id="3fb86-188">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-188">Read/write</span></span><br><span data-ttu-id="3fb86-189">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-189">Required</span></span> | <span data-ttu-id="3fb86-190">Määratleb kontakti tüübi esmase kontakti.</span><span class="sxs-lookup"><span data-stu-id="3fb86-190">Determines the primary contact of the contact type.</span></span> <span data-ttu-id="3fb86-191">Kontakti tüübi kohta peab olema ainult üks esmane kirje.</span><span class="sxs-lookup"><span data-stu-id="3fb86-191">There must be only one primary record per contact type.</span></span> |
| <span data-ttu-id="3fb86-192">**Privaatne**</span><span class="sxs-lookup"><span data-stu-id="3fb86-192">**Is Private**</span></span><br><span data-ttu-id="3fb86-193">mshr_isprivate</span><span class="sxs-lookup"><span data-stu-id="3fb86-193">mshr_isprivate</span></span><br><span data-ttu-id="3fb86-194">*suvandikomplekt mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="3fb86-194">*mshr_noyes option set*</span></span> | <span data-ttu-id="3fb86-195">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-195">Read/write</span></span><br><span data-ttu-id="3fb86-196">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-196">Required</span></span> | <span data-ttu-id="3fb86-197">Näitab, kas see aadress on isiku privaatne aadress.</span><span class="sxs-lookup"><span data-stu-id="3fb86-197">Identifies whether this address is a private address for the person.</span></span> |
| <span data-ttu-id="3fb86-198">**Eesmärk**</span><span class="sxs-lookup"><span data-stu-id="3fb86-198">**Purpose**</span></span><br><span data-ttu-id="3fb86-199">mshr_purpose</span><span class="sxs-lookup"><span data-stu-id="3fb86-199">mshr_purpose</span></span><br><span data-ttu-id="3fb86-200">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-200">*String*</span></span> | <span data-ttu-id="3fb86-201">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="3fb86-201">Read/write</span></span><br><span data-ttu-id="3fb86-202">Valikuline</span><span class="sxs-lookup"><span data-stu-id="3fb86-202">Optional</span></span> | <span data-ttu-id="3fb86-203">Kontaktandmete eesmärk/roll.</span><span class="sxs-lookup"><span data-stu-id="3fb86-203">The purpose/role of the contact details.</span></span> |
| <span data-ttu-id="3fb86-204">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="3fb86-204">**Primary Field**</span></span><br><span data-ttu-id="3fb86-205">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3fb86-205">mshr_primaryfield</span></span><br><span data-ttu-id="3fb86-206">*String*</span><span class="sxs-lookup"><span data-stu-id="3fb86-206">*String*</span></span> | <span data-ttu-id="3fb86-207">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3fb86-207">Read-only</span></span><br><span data-ttu-id="3fb86-208">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3fb86-208">Required</span></span> | <span data-ttu-id="3fb86-209">Väli, mida kasutatakse üksusekirje esmase ID-na.</span><span class="sxs-lookup"><span data-stu-id="3fb86-209">Field used as a primary identifier of the entity record.</span></span> <span data-ttu-id="3fb86-210">Osapoole numbri, tüübi, kirjelduse ja lokaatori kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="3fb86-210">Combination of party number, type, description, and locator.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3fb86-211">Vt ka</span><span class="sxs-lookup"><span data-stu-id="3fb86-211">See also</span></span>

[<span data-ttu-id="3fb86-212">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="3fb86-212">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3fb86-213">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="3fb86-213">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
