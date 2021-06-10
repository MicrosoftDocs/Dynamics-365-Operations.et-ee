---
title: Hindamise tase
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Hindamistase.
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
ms.openlocfilehash: 8bbd10bcc47a928070da7cd82e6d996f71c65698
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054832"
---
# <a name="rating-level"></a><span data-ttu-id="5d383-103">Hindamise tase</span><span class="sxs-lookup"><span data-stu-id="5d383-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5d383-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Hindamistase.</span><span class="sxs-lookup"><span data-stu-id="5d383-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5d383-105">Füüsiline nimi: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="5d383-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="5d383-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5d383-106">Description</span></span>

<span data-ttu-id="5d383-107">See olem annab saadaolevad oskuste hindamistasemed.</span><span class="sxs-lookup"><span data-stu-id="5d383-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="5d383-108">Hindamistasemed kehtivad kõigi juriidiliste isikute lõikes.</span><span class="sxs-lookup"><span data-stu-id="5d383-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5d383-109">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="5d383-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="5d383-110">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="5d383-110">Properties</span></span>

| <span data-ttu-id="5d383-111">Atribuut</span><span class="sxs-lookup"><span data-stu-id="5d383-111">Property</span></span><br><span data-ttu-id="5d383-112">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="5d383-112">**Physical name**</span></span><br><span data-ttu-id="5d383-113">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="5d383-113">**_Type_**</span></span> | <span data-ttu-id="5d383-114">Kasuta</span><span class="sxs-lookup"><span data-stu-id="5d383-114">Use</span></span> | <span data-ttu-id="5d383-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5d383-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5d383-116">**Hindamistaseme üksuse ID**</span><span class="sxs-lookup"><span data-stu-id="5d383-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="5d383-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="5d383-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="5d383-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5d383-118">*GUID*</span></span> | <span data-ttu-id="5d383-119">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="5d383-119">Read-only</span></span><br><span data-ttu-id="5d383-120">Nõutav</span><span class="sxs-lookup"><span data-stu-id="5d383-120">Required</span></span><br><span data-ttu-id="5d383-121">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="5d383-121">System-generated</span></span> | <span data-ttu-id="5d383-122">Tase,e süsteemi loodud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="5d383-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="5d383-123">**Hindamistaseme ID**</span><span class="sxs-lookup"><span data-stu-id="5d383-123">**Rating Level ID**</span></span><br><span data-ttu-id="5d383-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="5d383-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="5d383-125">*String*</span><span class="sxs-lookup"><span data-stu-id="5d383-125">*String*</span></span> | <span data-ttu-id="5d383-126">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="5d383-126">Read/write</span></span><br><span data-ttu-id="5d383-127">Nõutav</span><span class="sxs-lookup"><span data-stu-id="5d383-127">Required</span></span> | <span data-ttu-id="5d383-128">Tase,e kordumatu kasutaja loetav identifikaator.</span><span class="sxs-lookup"><span data-stu-id="5d383-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="5d383-129">**Hindamismudeli ID**</span><span class="sxs-lookup"><span data-stu-id="5d383-129">**Rating Model ID**</span></span><br><span data-ttu-id="5d383-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="5d383-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="5d383-131">*String*</span><span class="sxs-lookup"><span data-stu-id="5d383-131">*String*</span></span> | <span data-ttu-id="5d383-132">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="5d383-132">Read/write</span></span><br><span data-ttu-id="5d383-133">Nõutav</span><span class="sxs-lookup"><span data-stu-id="5d383-133">Required</span></span> | <span data-ttu-id="5d383-134">Hindamismudel, millesse hindamistase kuulub.</span><span class="sxs-lookup"><span data-stu-id="5d383-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="5d383-135">**Hindamismudeli üksuse ID**</span><span class="sxs-lookup"><span data-stu-id="5d383-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="5d383-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="5d383-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="5d383-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5d383-137">*GUID*</span></span> | <span data-ttu-id="5d383-138">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="5d383-138">Read-only</span></span><br><span data-ttu-id="5d383-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="5d383-139">Required</span></span><br><span data-ttu-id="5d383-140">Võõrvõti: mshr_hcmratingmodelentityid olemist mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="5d383-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="5d383-141">Süsteemi loodud identifikaator hindamismudelile, kuhu hindamistase kuulub.</span><span class="sxs-lookup"><span data-stu-id="5d383-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="5d383-142">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="5d383-142">**Description**</span></span><br><span data-ttu-id="5d383-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="5d383-143">mshr_description</span></span><br><span data-ttu-id="5d383-144">*String*</span><span class="sxs-lookup"><span data-stu-id="5d383-144">*String*</span></span> | <span data-ttu-id="5d383-145">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="5d383-145">Read/write</span></span><br><span data-ttu-id="5d383-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="5d383-146">Required</span></span> | <span data-ttu-id="5d383-147">Hindamistaseme kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="5d383-147">The description of the rating level.</span></span> |
| <span data-ttu-id="5d383-148">**Tegur**</span><span class="sxs-lookup"><span data-stu-id="5d383-148">**Factor**</span></span><br><span data-ttu-id="5d383-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="5d383-149">mshr_factor</span></span><br><span data-ttu-id="5d383-150">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="5d383-150">*Integer*</span></span> | <span data-ttu-id="5d383-151">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="5d383-151">Read/write</span></span><br><span data-ttu-id="5d383-152">Nõutav</span><span class="sxs-lookup"><span data-stu-id="5d383-152">Required</span></span> | <span data-ttu-id="5d383-153">Hindamistaseme tegur.</span><span class="sxs-lookup"><span data-stu-id="5d383-153">The factor for the rating level.</span></span> <span data-ttu-id="5d383-154">Kui võrdlete erinevate hindamistasemete arvuga üksusi, kasutatakse seda tegurit tulemuste normaliseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="5d383-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="5d383-155">Väärtus peab olema täisarv vahemikus 0–9.</span><span class="sxs-lookup"><span data-stu-id="5d383-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="5d383-156">**Märkus.**</span><span class="sxs-lookup"><span data-stu-id="5d383-156">**Note**</span></span><br><span data-ttu-id="5d383-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="5d383-157">mshr_note</span></span><br><span data-ttu-id="5d383-158">*String*</span><span class="sxs-lookup"><span data-stu-id="5d383-158">*String*</span></span> | <span data-ttu-id="5d383-159">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="5d383-159">Read/write</span></span><br><span data-ttu-id="5d383-160">Valikuline</span><span class="sxs-lookup"><span data-stu-id="5d383-160">Optional</span></span> | <span data-ttu-id="5d383-161">Reitingutasemega seostatud märkused.</span><span class="sxs-lookup"><span data-stu-id="5d383-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="5d383-162">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="5d383-162">**Primary Field**</span></span><br><span data-ttu-id="5d383-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="5d383-163">mshr_primaryfield</span></span><br><span data-ttu-id="5d383-164">*String*</span><span class="sxs-lookup"><span data-stu-id="5d383-164">*String*</span></span> | <span data-ttu-id="5d383-165">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="5d383-165">Read-only</span></span><br><span data-ttu-id="5d383-166">Nõutav</span><span class="sxs-lookup"><span data-stu-id="5d383-166">Required</span></span> | <span data-ttu-id="5d383-167">Väli, mida kasutatakse üksusekirje esmase ID-na.</span><span class="sxs-lookup"><span data-stu-id="5d383-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="5d383-168">Hindamistaseme ID ja hindamismudeli ID kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="5d383-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5d383-169">Vt ka</span><span class="sxs-lookup"><span data-stu-id="5d383-169">See also</span></span>

[<span data-ttu-id="5d383-170">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="5d383-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5d383-171">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="5d383-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]