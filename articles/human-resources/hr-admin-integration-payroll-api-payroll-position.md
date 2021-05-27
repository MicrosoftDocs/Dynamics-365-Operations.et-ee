---
title: Ametikohtade palga üksikasjad
description: See teema annab üksikasjad ja näidispäringu ametikohtade üksikasjade olemi kohta rakenduses Dynamics 365 Human Resources.
author: jcart
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
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019318"
---
# <a name="payroll-position"></a><span data-ttu-id="80888-103">Palga positsioon</span><span class="sxs-lookup"><span data-stu-id="80888-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="80888-104">See teema annab üksikasjad ja näidispäringu ametikohtade üksikasjade olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="80888-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="80888-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="80888-105">Properties</span></span>

| <span data-ttu-id="80888-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="80888-106">Property</span></span><br><span data-ttu-id="80888-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="80888-107">**Physical name**</span></span><br><span data-ttu-id="80888-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="80888-108">**_Type_**</span></span> | <span data-ttu-id="80888-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="80888-109">Use</span></span> | <span data-ttu-id="80888-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="80888-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="80888-111">**Iga-aastased regulaarsed tunnid**</span><span class="sxs-lookup"><span data-stu-id="80888-111">**Annual regular hours**</span></span><br><span data-ttu-id="80888-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="80888-112">annualregularhours</span></span><br><span data-ttu-id="80888-113">*Kümnendkoht*</span><span class="sxs-lookup"><span data-stu-id="80888-113">*Decimal*</span></span> | <span data-ttu-id="80888-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="80888-114">Read-only</span></span><br><span data-ttu-id="80888-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-115">Required</span></span> | <span data-ttu-id="80888-116">Ametikohal määratletud iga-aastased regulaarsed tunnid.</span><span class="sxs-lookup"><span data-stu-id="80888-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="80888-117">**Palgaarvestuse ametikoha üksikasjade olemi ID**</span><span class="sxs-lookup"><span data-stu-id="80888-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="80888-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="80888-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="80888-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="80888-119">*Guid*</span></span> | <span data-ttu-id="80888-120">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-120">Required</span></span><br><span data-ttu-id="80888-121">Süsteemi loodud.</span><span class="sxs-lookup"><span data-stu-id="80888-121">System generated.</span></span> | <span data-ttu-id="80888-122">Süsteemi loodud GUID-väärtus ametikoha kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="80888-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="80888-123">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="80888-123">**Primary field**</span></span><br><span data-ttu-id="80888-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="80888-124">mshr_primaryfield</span></span><br><span data-ttu-id="80888-125">*String*</span><span class="sxs-lookup"><span data-stu-id="80888-125">*String*</span></span> | <span data-ttu-id="80888-126">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-126">Required</span></span><br><span data-ttu-id="80888-127">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="80888-127">System generated</span></span> |  |
| <span data-ttu-id="80888-128">**Ametikoha töö ID väärtus**</span><span class="sxs-lookup"><span data-stu-id="80888-128">**Position job ID value**</span></span><br><span data-ttu-id="80888-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="80888-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="80888-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="80888-130">*GUID*</span></span> | <span data-ttu-id="80888-131">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="80888-131">Read-only</span></span><br><span data-ttu-id="80888-132">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-132">Required</span></span><br><span data-ttu-id="80888-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="80888-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="80888-134">Ametikohaga seotud töö ID.</span><span class="sxs-lookup"><span data-stu-id="80888-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="80888-135">**Põhipalgaplaani ID**</span><span class="sxs-lookup"><span data-stu-id="80888-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="80888-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="80888-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="80888-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="80888-137">*GUID*</span></span> | <span data-ttu-id="80888-138">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="80888-138">Read-only</span></span><br><span data-ttu-id="80888-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-139">Required</span></span><br><span data-ttu-id="80888-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="80888-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="80888-141">Põhipalgaplaaniga seotud töö ID.</span><span class="sxs-lookup"><span data-stu-id="80888-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="80888-142">**Palgatsükli ID**</span><span class="sxs-lookup"><span data-stu-id="80888-142">**Pay cycle ID**</span></span><br><span data-ttu-id="80888-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="80888-143">mshr_primaryfield</span></span><br><span data-ttu-id="80888-144">*String*</span><span class="sxs-lookup"><span data-stu-id="80888-144">*String*</span></span> | <span data-ttu-id="80888-145">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="80888-145">Read-only</span></span><br><span data-ttu-id="80888-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-146">Required</span></span> | <span data-ttu-id="80888-147">Ametikohal määratletud palgatsükkel.</span><span class="sxs-lookup"><span data-stu-id="80888-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="80888-148">**Maksja juriidiline isik**</span><span class="sxs-lookup"><span data-stu-id="80888-148">**Paid by legal entity**</span></span><br><span data-ttu-id="80888-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="80888-149">paidbylegalentity</span></span><br><span data-ttu-id="80888-150">*String*</span><span class="sxs-lookup"><span data-stu-id="80888-150">*String*</span></span> | <span data-ttu-id="80888-151">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="80888-151">Read-only</span></span><br><span data-ttu-id="80888-152">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-152">Required</span></span> | <span data-ttu-id="80888-153">Makse tegemise eest vastutaval ametikohal määratletud juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="80888-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="80888-154">**Ametikoha ID**</span><span class="sxs-lookup"><span data-stu-id="80888-154">**Position ID**</span></span><br><span data-ttu-id="80888-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="80888-155">mshr_positionid</span></span><br><span data-ttu-id="80888-156">*String*</span><span class="sxs-lookup"><span data-stu-id="80888-156">*String*</span></span> | <span data-ttu-id="80888-157">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="80888-157">Read-only</span></span><br><span data-ttu-id="80888-158">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-158">Required</span></span> | <span data-ttu-id="80888-159">Ametikoha ID.</span><span class="sxs-lookup"><span data-stu-id="80888-159">The ID of the position.</span></span> |
| <span data-ttu-id="80888-160">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="80888-160">**Valid to**</span></span><br><span data-ttu-id="80888-161">validto</span><span class="sxs-lookup"><span data-stu-id="80888-161">validto</span></span><br><span data-ttu-id="80888-162">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="80888-162">*Date Time Offset*</span></span> | <span data-ttu-id="80888-163">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="80888-163">Read-only</span></span><br><span data-ttu-id="80888-164">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-164">Required</span></span> |<span data-ttu-id="80888-165">Kuupäev, millest alates ametikoha üksikasjad kehtivad.</span><span class="sxs-lookup"><span data-stu-id="80888-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="80888-166">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="80888-166">**Valid from**</span></span><br><span data-ttu-id="80888-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="80888-167">validfrom</span></span><br><span data-ttu-id="80888-168">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="80888-168">*Date Time Offset*</span></span> | <span data-ttu-id="80888-169">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="80888-169">Read-only</span></span><br><span data-ttu-id="80888-170">Nõutav</span><span class="sxs-lookup"><span data-stu-id="80888-170">Required</span></span> |<span data-ttu-id="80888-171">Kuupäev, milleni ametikoha üksikasjad kehtivad.</span><span class="sxs-lookup"><span data-stu-id="80888-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="80888-172">**Päring**</span><span class="sxs-lookup"><span data-stu-id="80888-172">**Query**</span></span>

<span data-ttu-id="80888-173">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="80888-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="80888-174">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="80888-174">**Response**</span></span>

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
