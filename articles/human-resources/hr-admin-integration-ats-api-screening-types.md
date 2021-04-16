---
title: Skriiningu tüübid
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Skriiningu tüübid.
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
ms.openlocfilehash: 361f8c866abb9d34eb3e2be7ea42626e98e34779
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805126"
---
# <a name="screening-types"></a><span data-ttu-id="f87c9-103">Skriiningu tüübid</span><span class="sxs-lookup"><span data-stu-id="f87c9-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f87c9-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Skriiningu tüübid.</span><span class="sxs-lookup"><span data-stu-id="f87c9-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f87c9-105">Füüsiline nimi: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="f87c9-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="f87c9-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f87c9-106">Description</span></span>

<span data-ttu-id="f87c9-107">See üksus kirjeldab skriiningu tüüpe, mille ettevõte on seadistanud värbamiseelseks ja jooksvaks töötajate skriininguks.</span><span class="sxs-lookup"><span data-stu-id="f87c9-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f87c9-108">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="f87c9-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="f87c9-109">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="f87c9-109">Properties</span></span>

| <span data-ttu-id="f87c9-110">Atribuut</span><span class="sxs-lookup"><span data-stu-id="f87c9-110">Property</span></span><br><span data-ttu-id="f87c9-111">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="f87c9-111">**Physical name**</span></span><br><span data-ttu-id="f87c9-112">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="f87c9-112">**_Type_**</span></span> | <span data-ttu-id="f87c9-113">Kasuta</span><span class="sxs-lookup"><span data-stu-id="f87c9-113">Use</span></span> | <span data-ttu-id="f87c9-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f87c9-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f87c9-115">**Skriiningu tüübi olemi ID**</span><span class="sxs-lookup"><span data-stu-id="f87c9-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="f87c9-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="f87c9-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="f87c9-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f87c9-117">*GUID*</span></span> | <span data-ttu-id="f87c9-118">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="f87c9-118">Read-only</span></span><br><span data-ttu-id="f87c9-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="f87c9-119">Required</span></span><br><span data-ttu-id="f87c9-120">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="f87c9-120">System-generated</span></span> | <span data-ttu-id="f87c9-121">Skriiningu tüübi kirje kordumatu peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="f87c9-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="f87c9-122">**Skriiningu tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="f87c9-122">**Screening Type ID**</span></span><br><span data-ttu-id="f87c9-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="f87c9-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="f87c9-124">*String*</span><span class="sxs-lookup"><span data-stu-id="f87c9-124">*String*</span></span> | <span data-ttu-id="f87c9-125">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="f87c9-125">Read/write</span></span><br><span data-ttu-id="f87c9-126">Nõutav</span><span class="sxs-lookup"><span data-stu-id="f87c9-126">Required</span></span> | <span data-ttu-id="f87c9-127">Skriiningu tüübi kasutaja määratletud kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="f87c9-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="f87c9-128">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="f87c9-128">**Description**</span></span><br><span data-ttu-id="f87c9-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="f87c9-129">mshr_description</span></span><br><span data-ttu-id="f87c9-130">*String*</span><span class="sxs-lookup"><span data-stu-id="f87c9-130">*String*</span></span> | <span data-ttu-id="f87c9-131">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="f87c9-131">Read/write</span></span><br><span data-ttu-id="f87c9-132">Nõutav</span><span class="sxs-lookup"><span data-stu-id="f87c9-132">Required</span></span> | <span data-ttu-id="f87c9-133">Skriiningu tüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f87c9-133">The description of the screening type.</span></span> |
| <span data-ttu-id="f87c9-134">**Sageduse üksus**</span><span class="sxs-lookup"><span data-stu-id="f87c9-134">**Frequency Unit**</span></span><br><span data-ttu-id="f87c9-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="f87c9-135">mshr_frequencyunit</span></span><br><span data-ttu-id="f87c9-136">*suvandikomplekt mshr_hcmfrequencyunit*</span><span class="sxs-lookup"><span data-stu-id="f87c9-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="f87c9-137">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="f87c9-137">Read/write</span></span><br><span data-ttu-id="f87c9-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="f87c9-138">Required</span></span> | <span data-ttu-id="f87c9-139">Kirjeldab sagedust, millal skriining tuleb määratud isiku jaoks läbi viia.</span><span class="sxs-lookup"><span data-stu-id="f87c9-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="f87c9-140">**Loo alates**</span><span class="sxs-lookup"><span data-stu-id="f87c9-140">**Generate From**</span></span><br><span data-ttu-id="f87c9-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="f87c9-141">mshr_generatefrom</span></span><br><span data-ttu-id="f87c9-142">*suvandikomplekt mshr_hcmfrequencygeneratefrom*</span><span class="sxs-lookup"><span data-stu-id="f87c9-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="f87c9-143">Loe-kirjuta</span><span class="sxs-lookup"><span data-stu-id="f87c9-143">Read-write</span></span><br><span data-ttu-id="f87c9-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="f87c9-144">Required</span></span> | <span data-ttu-id="f87c9-145">Kui sageduse väärtus on muu kui "Ainult üks kord", määrab funktsiooni GenerateFrom väärtus kuupäeva, millest arvutada järgmine skriiningu sündmus.</span><span class="sxs-lookup"><span data-stu-id="f87c9-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="f87c9-146">**Sageduse intervall**</span><span class="sxs-lookup"><span data-stu-id="f87c9-146">**Frequency Interval**</span></span><br><span data-ttu-id="f87c9-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="f87c9-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="f87c9-148">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="f87c9-148">*Integer*</span></span> | <span data-ttu-id="f87c9-149">Loe-kirjuta</span><span class="sxs-lookup"><span data-stu-id="f87c9-149">Read-write</span></span><br><span data-ttu-id="f87c9-150">Nõutav</span><span class="sxs-lookup"><span data-stu-id="f87c9-150">Required</span></span> | <span data-ttu-id="f87c9-151">Kui sageduse väärtus on muu kui "ainult üks kord", peate iga skriiningu sündmuse vaheliste ajaühikute jaoks intervalli määrama.</span><span class="sxs-lookup"><span data-stu-id="f87c9-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f87c9-152">Vt ka</span><span class="sxs-lookup"><span data-stu-id="f87c9-152">See also</span></span>

[<span data-ttu-id="f87c9-153">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="f87c9-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f87c9-154">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="f87c9-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]