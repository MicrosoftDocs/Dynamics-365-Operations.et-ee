---
title: Skriiningu tüübid
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Skriiningu tüübid.
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
ms.openlocfilehash: 2acb99c2fb57df883ab376c7f6aab547073bd0ff
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058292"
---
# <a name="screening-types"></a><span data-ttu-id="4aba0-103">Skriiningu tüübid</span><span class="sxs-lookup"><span data-stu-id="4aba0-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4aba0-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Skriiningu tüübid.</span><span class="sxs-lookup"><span data-stu-id="4aba0-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4aba0-105">Füüsiline nimi: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="4aba0-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="4aba0-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4aba0-106">Description</span></span>

<span data-ttu-id="4aba0-107">See üksus kirjeldab skriiningu tüüpe, mille ettevõte on seadistanud värbamiseelseks ja jooksvaks töötajate skriininguks.</span><span class="sxs-lookup"><span data-stu-id="4aba0-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4aba0-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="4aba0-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="4aba0-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="4aba0-109">Properties</span></span>

| <span data-ttu-id="4aba0-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="4aba0-110">Property</span></span><br><span data-ttu-id="4aba0-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="4aba0-111">**Physical name**</span></span><br><span data-ttu-id="4aba0-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="4aba0-112">**_Type_**</span></span> | <span data-ttu-id="4aba0-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="4aba0-113">Use</span></span> | <span data-ttu-id="4aba0-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4aba0-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4aba0-115">**Skriiningu tüübi olemi ID**</span><span class="sxs-lookup"><span data-stu-id="4aba0-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="4aba0-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="4aba0-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="4aba0-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4aba0-117">*GUID*</span></span> | <span data-ttu-id="4aba0-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="4aba0-118">Read-only</span></span><br><span data-ttu-id="4aba0-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="4aba0-119">Required</span></span><br><span data-ttu-id="4aba0-120">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="4aba0-120">System-generated</span></span> | <span data-ttu-id="4aba0-121">Skriiningu tüübi kirje kordumatu peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="4aba0-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="4aba0-122">**Skriiningu tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="4aba0-122">**Screening Type ID**</span></span><br><span data-ttu-id="4aba0-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="4aba0-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="4aba0-124">*String*</span><span class="sxs-lookup"><span data-stu-id="4aba0-124">*String*</span></span> | <span data-ttu-id="4aba0-125">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="4aba0-125">Read/write</span></span><br><span data-ttu-id="4aba0-126">Nõutav</span><span class="sxs-lookup"><span data-stu-id="4aba0-126">Required</span></span> | <span data-ttu-id="4aba0-127">Skriiningu tüübi kasutaja määratletud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="4aba0-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="4aba0-128">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="4aba0-128">**Description**</span></span><br><span data-ttu-id="4aba0-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="4aba0-129">mshr_description</span></span><br><span data-ttu-id="4aba0-130">*String*</span><span class="sxs-lookup"><span data-stu-id="4aba0-130">*String*</span></span> | <span data-ttu-id="4aba0-131">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="4aba0-131">Read/write</span></span><br><span data-ttu-id="4aba0-132">Nõutav</span><span class="sxs-lookup"><span data-stu-id="4aba0-132">Required</span></span> | <span data-ttu-id="4aba0-133">Skriiningu tüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="4aba0-133">The description of the screening type.</span></span> |
| <span data-ttu-id="4aba0-134">**Sageduse üksus**</span><span class="sxs-lookup"><span data-stu-id="4aba0-134">**Frequency Unit**</span></span><br><span data-ttu-id="4aba0-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="4aba0-135">mshr_frequencyunit</span></span><br><span data-ttu-id="4aba0-136">*suvandikomplekt mshr_hcmfrequencyunit*</span><span class="sxs-lookup"><span data-stu-id="4aba0-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="4aba0-137">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="4aba0-137">Read/write</span></span><br><span data-ttu-id="4aba0-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="4aba0-138">Required</span></span> | <span data-ttu-id="4aba0-139">Kirjeldab sagedust, millal skriining tuleb määratud isiku jaoks läbi viia.</span><span class="sxs-lookup"><span data-stu-id="4aba0-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="4aba0-140">**Loo alates**</span><span class="sxs-lookup"><span data-stu-id="4aba0-140">**Generate From**</span></span><br><span data-ttu-id="4aba0-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="4aba0-141">mshr_generatefrom</span></span><br><span data-ttu-id="4aba0-142">*suvandikomplekt mshr_hcmfrequencygeneratefrom*</span><span class="sxs-lookup"><span data-stu-id="4aba0-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="4aba0-143">Loe-kirjuta</span><span class="sxs-lookup"><span data-stu-id="4aba0-143">Read-write</span></span><br><span data-ttu-id="4aba0-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="4aba0-144">Required</span></span> | <span data-ttu-id="4aba0-145">Kui sageduse väärtus on muu kui "Ainult üks kord", määrab funktsiooni GenerateFrom väärtus kuupäeva, millest arvutada järgmine skriiningu sündmus.</span><span class="sxs-lookup"><span data-stu-id="4aba0-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="4aba0-146">**Sageduse intervall**</span><span class="sxs-lookup"><span data-stu-id="4aba0-146">**Frequency Interval**</span></span><br><span data-ttu-id="4aba0-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="4aba0-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="4aba0-148">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="4aba0-148">*Integer*</span></span> | <span data-ttu-id="4aba0-149">Loe-kirjuta</span><span class="sxs-lookup"><span data-stu-id="4aba0-149">Read-write</span></span><br><span data-ttu-id="4aba0-150">Nõutav</span><span class="sxs-lookup"><span data-stu-id="4aba0-150">Required</span></span> | <span data-ttu-id="4aba0-151">Kui sageduse väärtus on muu kui "ainult üks kord", peate iga skriiningu sündmuse vaheliste ajaühikute jaoks intervalli määrama.</span><span class="sxs-lookup"><span data-stu-id="4aba0-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4aba0-152">Vt ka</span><span class="sxs-lookup"><span data-stu-id="4aba0-152">See also</span></span>

[<span data-ttu-id="4aba0-153">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="4aba0-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4aba0-154">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="4aba0-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]