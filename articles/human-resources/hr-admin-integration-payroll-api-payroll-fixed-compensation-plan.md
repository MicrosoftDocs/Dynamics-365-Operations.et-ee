---
title: Palgaarvestuse põhipalgaplaan
description: See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059084"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="91eae-103">Palgaarvestuse põhipalgaplaan</span><span class="sxs-lookup"><span data-stu-id="91eae-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="91eae-104">See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="91eae-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="91eae-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="91eae-105">Properties</span></span>

| <span data-ttu-id="91eae-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="91eae-106">Property</span></span><br><span data-ttu-id="91eae-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="91eae-107">**Physical name**</span></span><br><span data-ttu-id="91eae-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="91eae-108">**_Type_**</span></span> | <span data-ttu-id="91eae-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="91eae-109">Use</span></span> | <span data-ttu-id="91eae-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eae-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="91eae-111">**Töötaja ID**</span><span class="sxs-lookup"><span data-stu-id="91eae-111">**Employee ID**</span></span><br><span data-ttu-id="91eae-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="91eae-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="91eae-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="91eae-113">*GUID*</span></span> | <span data-ttu-id="91eae-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-114">Read-only</span></span><br><span data-ttu-id="91eae-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-115">Required</span></span><br><span data-ttu-id="91eae-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="91eae-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="91eae-117">Töötaja ID</span><span class="sxs-lookup"><span data-stu-id="91eae-117">Employee ID</span></span> |
| <span data-ttu-id="91eae-118">**Tasumäär**</span><span class="sxs-lookup"><span data-stu-id="91eae-118">**Pay rate**</span></span><br><span data-ttu-id="91eae-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="91eae-119">mshr_payrate</span></span><br><span data-ttu-id="91eae-120">*Kümnendkoht*</span><span class="sxs-lookup"><span data-stu-id="91eae-120">*Decimal*</span></span> | <span data-ttu-id="91eae-121">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-121">Read-only</span></span><br><span data-ttu-id="91eae-122">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-122">Required</span></span> | <span data-ttu-id="91eae-123">Põhipalgaplaanis määratletud tasumäär.</span><span class="sxs-lookup"><span data-stu-id="91eae-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="91eae-124">**Plaani ID**</span><span class="sxs-lookup"><span data-stu-id="91eae-124">**Plan ID**</span></span><br><span data-ttu-id="91eae-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="91eae-125">mshr_planid</span></span><br><span data-ttu-id="91eae-126">*String*</span><span class="sxs-lookup"><span data-stu-id="91eae-126">*String*</span></span> | <span data-ttu-id="91eae-127">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-127">Read-only</span></span><br><span data-ttu-id="91eae-128">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-128">Required</span></span> |<span data-ttu-id="91eae-129">Määrab palgaplaani.</span><span class="sxs-lookup"><span data-stu-id="91eae-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="91eae-130">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="91eae-130">**Valid from**</span></span><br><span data-ttu-id="91eae-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="91eae-131">mshr_validfrom</span></span><br><span data-ttu-id="91eae-132">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="91eae-132">*Date Time Offset*</span></span> |  <span data-ttu-id="91eae-133">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-133">Read-only</span></span><br><span data-ttu-id="91eae-134">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-134">Required</span></span> |<span data-ttu-id="91eae-135">Töötajaga seotud põhipalga kehtivuse algkuupäev.</span><span class="sxs-lookup"><span data-stu-id="91eae-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="91eae-136">**Palgaarvestuse põhipalgaplaani olem**</span><span class="sxs-lookup"><span data-stu-id="91eae-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="91eae-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="91eae-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="91eae-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="91eae-138">*GUID*</span></span> | <span data-ttu-id="91eae-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-139">Required</span></span><br><span data-ttu-id="91eae-140">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="91eae-140">Sytem generated</span></span> | <span data-ttu-id="91eae-141">Süsteemi loodud GUID-väärtus palgaplaani kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="91eae-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="91eae-142">**Tasusagedus**</span><span class="sxs-lookup"><span data-stu-id="91eae-142">**Pay frequency**</span></span><br><span data-ttu-id="91eae-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="91eae-143">mshr_payfrequency</span></span><br><span data-ttu-id="91eae-144">*String*</span><span class="sxs-lookup"><span data-stu-id="91eae-144">*String*</span></span> | <span data-ttu-id="91eae-145">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-145">Read-only</span></span><br><span data-ttu-id="91eae-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-146">Required</span></span> |<span data-ttu-id="91eae-147">Töötajale makstava tasu maksmise sagedus.</span><span class="sxs-lookup"><span data-stu-id="91eae-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="91eae-148">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="91eae-148">**Valid to**</span></span><br><span data-ttu-id="91eae-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="91eae-149">mshr_validto</span></span><br><span data-ttu-id="91eae-150">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="91eae-150">*Date Time Offset*</span></span> | <span data-ttu-id="91eae-151">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-151">Read-only</span></span> <br><span data-ttu-id="91eae-152">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-152">Required</span></span> | <span data-ttu-id="91eae-153">Töötajaga seotud põhipalga kehtivuse lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="91eae-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="91eae-154">**Ametikoha ID**</span><span class="sxs-lookup"><span data-stu-id="91eae-154">**Position ID**</span></span><br><span data-ttu-id="91eae-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="91eae-155">mshr_positionid</span></span><br><span data-ttu-id="91eae-156">*String*</span><span class="sxs-lookup"><span data-stu-id="91eae-156">*String*</span></span> | <span data-ttu-id="91eae-157">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-157">Read-only</span></span> <br><span data-ttu-id="91eae-158">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-158">Required</span></span> | <span data-ttu-id="91eae-159">Töötaja ja põhipalgaplaani registreerimisega seotud ID.</span><span class="sxs-lookup"><span data-stu-id="91eae-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="91eae-160">**Currency**</span><span class="sxs-lookup"><span data-stu-id="91eae-160">**Currency**</span></span><br><span data-ttu-id="91eae-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="91eae-161">mshr_currency</span></span><br><span data-ttu-id="91eae-162">*String*</span><span class="sxs-lookup"><span data-stu-id="91eae-162">*String*</span></span> | <span data-ttu-id="91eae-163">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-163">Read-only</span></span> <br><span data-ttu-id="91eae-164">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-164">Required</span></span> |<span data-ttu-id="91eae-165">Põhipalgaplaani jaoks määratletud valuuta</span><span class="sxs-lookup"><span data-stu-id="91eae-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="91eae-166">**Personalinumber**</span><span class="sxs-lookup"><span data-stu-id="91eae-166">**Personnel number**</span></span><br><span data-ttu-id="91eae-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="91eae-167">mshr_personnelnumber</span></span><br><span data-ttu-id="91eae-168">*String*</span><span class="sxs-lookup"><span data-stu-id="91eae-168">*String*</span></span> | <span data-ttu-id="91eae-169">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="91eae-169">Read-only</span></span><br><span data-ttu-id="91eae-170">Nõutav</span><span class="sxs-lookup"><span data-stu-id="91eae-170">Required</span></span> |<span data-ttu-id="91eae-171">Töötaja kordumatu personalinumber.</span><span class="sxs-lookup"><span data-stu-id="91eae-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="91eae-172">**Päring**</span><span class="sxs-lookup"><span data-stu-id="91eae-172">**Query**</span></span>

<span data-ttu-id="91eae-173">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="91eae-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="91eae-174">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="91eae-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
