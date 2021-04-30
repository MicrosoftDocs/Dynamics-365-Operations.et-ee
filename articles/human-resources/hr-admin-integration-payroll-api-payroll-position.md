---
title: Ametikohtade palga üksikasjad
description: See teema annab üksikasjad ja näidispäringu ametikohtade üksikasjade olemi kohta rakenduses Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881964"
---
# <a name="payroll-position"></a><span data-ttu-id="0a117-103">Palga positsioon</span><span class="sxs-lookup"><span data-stu-id="0a117-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0a117-104">See teema annab üksikasjad ja näidispäringu ametikohtade üksikasjade olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0a117-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="0a117-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="0a117-105">Properties</span></span>

| <span data-ttu-id="0a117-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="0a117-106">Property</span></span><br><span data-ttu-id="0a117-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="0a117-107">**Physical name**</span></span><br><span data-ttu-id="0a117-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="0a117-108">**_Type_**</span></span> | <span data-ttu-id="0a117-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="0a117-109">Use</span></span> | <span data-ttu-id="0a117-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0a117-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0a117-111">**Iga-aastased regulaarsed tunnid**</span><span class="sxs-lookup"><span data-stu-id="0a117-111">**Annual regular hours**</span></span><br><span data-ttu-id="0a117-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="0a117-112">annualregularhours</span></span><br><span data-ttu-id="0a117-113">*Kümnendkoht*</span><span class="sxs-lookup"><span data-stu-id="0a117-113">*Decimal*</span></span> | <span data-ttu-id="0a117-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0a117-114">Read-only</span></span><br><span data-ttu-id="0a117-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-115">Required</span></span> | <span data-ttu-id="0a117-116">Ametikohal määratletud iga-aastased regulaarsed tunnid.</span><span class="sxs-lookup"><span data-stu-id="0a117-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="0a117-117">**Palgaarvestuse ametikoha üksikasjade olemi ID**</span><span class="sxs-lookup"><span data-stu-id="0a117-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="0a117-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="0a117-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="0a117-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="0a117-119">*Guid*</span></span> | <span data-ttu-id="0a117-120">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-120">Required</span></span><br><span data-ttu-id="0a117-121">Süsteemi loodud.</span><span class="sxs-lookup"><span data-stu-id="0a117-121">System generated.</span></span> | <span data-ttu-id="0a117-122">Süsteemi loodud GUID-väärtus ametikoha kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="0a117-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="0a117-123">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="0a117-123">**Primary field**</span></span><br><span data-ttu-id="0a117-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0a117-124">mshr_primaryfield</span></span><br><span data-ttu-id="0a117-125">*String*</span><span class="sxs-lookup"><span data-stu-id="0a117-125">*String*</span></span> | <span data-ttu-id="0a117-126">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-126">Required</span></span><br><span data-ttu-id="0a117-127">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="0a117-127">System generated</span></span> |  |
| <span data-ttu-id="0a117-128">**Ametikoha töö ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="0a117-128">**Position job ID value**</span></span><br><span data-ttu-id="0a117-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="0a117-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="0a117-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0a117-130">*GUID*</span></span> | <span data-ttu-id="0a117-131">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0a117-131">Read-only</span></span><br><span data-ttu-id="0a117-132">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-132">Required</span></span><br><span data-ttu-id="0a117-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="0a117-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="0a117-134">Ametikohaga seotud töö ID.</span><span class="sxs-lookup"><span data-stu-id="0a117-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="0a117-135">**Põhipalgaplaani ID**</span><span class="sxs-lookup"><span data-stu-id="0a117-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="0a117-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="0a117-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="0a117-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0a117-137">*GUID*</span></span> | <span data-ttu-id="0a117-138">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0a117-138">Read-only</span></span><br><span data-ttu-id="0a117-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-139">Required</span></span><br><span data-ttu-id="0a117-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="0a117-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="0a117-141">Põhipalgaplaaniga seotud töö ID.</span><span class="sxs-lookup"><span data-stu-id="0a117-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="0a117-142">**Palgatsükli ID**</span><span class="sxs-lookup"><span data-stu-id="0a117-142">**Pay cycle ID**</span></span><br><span data-ttu-id="0a117-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0a117-143">mshr_primaryfield</span></span><br><span data-ttu-id="0a117-144">*String*</span><span class="sxs-lookup"><span data-stu-id="0a117-144">*String*</span></span> | <span data-ttu-id="0a117-145">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0a117-145">Read-only</span></span><br><span data-ttu-id="0a117-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-146">Required</span></span> | <span data-ttu-id="0a117-147">Ametikohal määratletud palgatsükkel.</span><span class="sxs-lookup"><span data-stu-id="0a117-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="0a117-148">**Maksja juriidiline isik**</span><span class="sxs-lookup"><span data-stu-id="0a117-148">**Paid by legal entity**</span></span><br><span data-ttu-id="0a117-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="0a117-149">paidbylegalentity</span></span><br><span data-ttu-id="0a117-150">*String*</span><span class="sxs-lookup"><span data-stu-id="0a117-150">*String*</span></span> | <span data-ttu-id="0a117-151">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0a117-151">Read-only</span></span><br><span data-ttu-id="0a117-152">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-152">Required</span></span> | <span data-ttu-id="0a117-153">Makse tegemise eest vastutaval ametikohal määratletud juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="0a117-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="0a117-154">**Ametikoha ID**</span><span class="sxs-lookup"><span data-stu-id="0a117-154">**Position ID**</span></span><br><span data-ttu-id="0a117-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="0a117-155">mshr_positionid</span></span><br><span data-ttu-id="0a117-156">*String*</span><span class="sxs-lookup"><span data-stu-id="0a117-156">*String*</span></span> | <span data-ttu-id="0a117-157">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0a117-157">Read-only</span></span><br><span data-ttu-id="0a117-158">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-158">Required</span></span> | <span data-ttu-id="0a117-159">Ametikoha ID.</span><span class="sxs-lookup"><span data-stu-id="0a117-159">The ID of the position.</span></span> |
| <span data-ttu-id="0a117-160">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="0a117-160">**Valid to**</span></span><br><span data-ttu-id="0a117-161">validto</span><span class="sxs-lookup"><span data-stu-id="0a117-161">validto</span></span><br><span data-ttu-id="0a117-162">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="0a117-162">*Date Time Offset*</span></span> | <span data-ttu-id="0a117-163">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0a117-163">Read-only</span></span><br><span data-ttu-id="0a117-164">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-164">Required</span></span> |<span data-ttu-id="0a117-165">Kuupäev, millest alates ametikoha üksikasjad kehtivad.</span><span class="sxs-lookup"><span data-stu-id="0a117-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="0a117-166">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="0a117-166">**Valid from**</span></span><br><span data-ttu-id="0a117-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="0a117-167">validfrom</span></span><br><span data-ttu-id="0a117-168">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="0a117-168">*Date Time Offset*</span></span> | <span data-ttu-id="0a117-169">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="0a117-169">Read-only</span></span><br><span data-ttu-id="0a117-170">Nõutav</span><span class="sxs-lookup"><span data-stu-id="0a117-170">Required</span></span> |<span data-ttu-id="0a117-171">Kuupäev, milleni ametikoha üksikasjad kehtivad.</span><span class="sxs-lookup"><span data-stu-id="0a117-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="0a117-172">**Päring**</span><span class="sxs-lookup"><span data-stu-id="0a117-172">**Query**</span></span>

<span data-ttu-id="0a117-173">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="0a117-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="0a117-174">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="0a117-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
