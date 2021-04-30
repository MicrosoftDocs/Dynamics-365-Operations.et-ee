---
title: Palgaarvestuse põhipalgaplaan
description: See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881969"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="c7b80-103">Palgaarvestuse põhipalgaplaan</span><span class="sxs-lookup"><span data-stu-id="c7b80-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c7b80-104">See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c7b80-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="c7b80-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="c7b80-105">Properties</span></span>

| <span data-ttu-id="c7b80-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="c7b80-106">Property</span></span><br><span data-ttu-id="c7b80-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="c7b80-107">**Physical name**</span></span><br><span data-ttu-id="c7b80-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="c7b80-108">**_Type_**</span></span> | <span data-ttu-id="c7b80-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="c7b80-109">Use</span></span> | <span data-ttu-id="c7b80-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7b80-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c7b80-111">**Töötaja ID**</span><span class="sxs-lookup"><span data-stu-id="c7b80-111">**Employee ID**</span></span><br><span data-ttu-id="c7b80-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="c7b80-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="c7b80-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c7b80-113">*GUID*</span></span> | <span data-ttu-id="c7b80-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-114">Read-only</span></span><br><span data-ttu-id="c7b80-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-115">Required</span></span><br><span data-ttu-id="c7b80-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="c7b80-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="c7b80-117">Töötaja ID</span><span class="sxs-lookup"><span data-stu-id="c7b80-117">Employee ID</span></span> |
| <span data-ttu-id="c7b80-118">**Tasumäär**</span><span class="sxs-lookup"><span data-stu-id="c7b80-118">**Pay rate**</span></span><br><span data-ttu-id="c7b80-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="c7b80-119">mshr_payrate</span></span><br><span data-ttu-id="c7b80-120">*Kümnendkoht*</span><span class="sxs-lookup"><span data-stu-id="c7b80-120">*Decimal*</span></span> | <span data-ttu-id="c7b80-121">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-121">Read-only</span></span><br><span data-ttu-id="c7b80-122">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-122">Required</span></span> | <span data-ttu-id="c7b80-123">Põhipalgaplaanis määratletud tasumäär.</span><span class="sxs-lookup"><span data-stu-id="c7b80-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="c7b80-124">**Plaani ID**</span><span class="sxs-lookup"><span data-stu-id="c7b80-124">**Plan ID**</span></span><br><span data-ttu-id="c7b80-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="c7b80-125">mshr_planid</span></span><br><span data-ttu-id="c7b80-126">*String*</span><span class="sxs-lookup"><span data-stu-id="c7b80-126">*String*</span></span> | <span data-ttu-id="c7b80-127">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-127">Read-only</span></span><br><span data-ttu-id="c7b80-128">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-128">Required</span></span> |<span data-ttu-id="c7b80-129">Määrab palgaplaani.</span><span class="sxs-lookup"><span data-stu-id="c7b80-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="c7b80-130">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="c7b80-130">**Valid from**</span></span><br><span data-ttu-id="c7b80-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="c7b80-131">mshr_validfrom</span></span><br><span data-ttu-id="c7b80-132">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="c7b80-132">*Date Time Offset*</span></span> |  <span data-ttu-id="c7b80-133">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-133">Read-only</span></span><br><span data-ttu-id="c7b80-134">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-134">Required</span></span> |<span data-ttu-id="c7b80-135">Töötajaga seotud põhipalga kehtivuse algkuupäev.</span><span class="sxs-lookup"><span data-stu-id="c7b80-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="c7b80-136">**Palgaarvestuse põhipalgaplaani olem**</span><span class="sxs-lookup"><span data-stu-id="c7b80-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="c7b80-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="c7b80-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="c7b80-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c7b80-138">*GUID*</span></span> | <span data-ttu-id="c7b80-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-139">Required</span></span><br><span data-ttu-id="c7b80-140">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="c7b80-140">Sytem generated</span></span> | <span data-ttu-id="c7b80-141">Süsteemi loodud GUID-väärtus palgaplaani kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7b80-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="c7b80-142">**Tasusagedus**</span><span class="sxs-lookup"><span data-stu-id="c7b80-142">**Pay frequency**</span></span><br><span data-ttu-id="c7b80-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="c7b80-143">mshr_payfrequency</span></span><br><span data-ttu-id="c7b80-144">*String*</span><span class="sxs-lookup"><span data-stu-id="c7b80-144">*String*</span></span> | <span data-ttu-id="c7b80-145">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-145">Read-only</span></span><br><span data-ttu-id="c7b80-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-146">Required</span></span> |<span data-ttu-id="c7b80-147">Töötajale makstava tasu maksmise sagedus.</span><span class="sxs-lookup"><span data-stu-id="c7b80-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="c7b80-148">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="c7b80-148">**Valid to**</span></span><br><span data-ttu-id="c7b80-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="c7b80-149">mshr_validto</span></span><br><span data-ttu-id="c7b80-150">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="c7b80-150">*Date Time Offset*</span></span> | <span data-ttu-id="c7b80-151">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-151">Read-only</span></span> <br><span data-ttu-id="c7b80-152">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-152">Required</span></span> | <span data-ttu-id="c7b80-153">Töötajaga seotud põhipalga kehtivuse lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="c7b80-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="c7b80-154">**Ametikoha ID**</span><span class="sxs-lookup"><span data-stu-id="c7b80-154">**Position ID**</span></span><br><span data-ttu-id="c7b80-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="c7b80-155">mshr_positionid</span></span><br><span data-ttu-id="c7b80-156">*String*</span><span class="sxs-lookup"><span data-stu-id="c7b80-156">*String*</span></span> | <span data-ttu-id="c7b80-157">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-157">Read-only</span></span> <br><span data-ttu-id="c7b80-158">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-158">Required</span></span> | <span data-ttu-id="c7b80-159">Töötaja ja põhipalgaplaani registreerimisega seotud ID.</span><span class="sxs-lookup"><span data-stu-id="c7b80-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="c7b80-160">**Currency**</span><span class="sxs-lookup"><span data-stu-id="c7b80-160">**Currency**</span></span><br><span data-ttu-id="c7b80-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="c7b80-161">mshr_currency</span></span><br><span data-ttu-id="c7b80-162">*String*</span><span class="sxs-lookup"><span data-stu-id="c7b80-162">*String*</span></span> | <span data-ttu-id="c7b80-163">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-163">Read-only</span></span> <br><span data-ttu-id="c7b80-164">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-164">Required</span></span> |<span data-ttu-id="c7b80-165">Põhipalgaplaani jaoks määratletud valuuta</span><span class="sxs-lookup"><span data-stu-id="c7b80-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="c7b80-166">**Personalinumber**</span><span class="sxs-lookup"><span data-stu-id="c7b80-166">**Personnel number**</span></span><br><span data-ttu-id="c7b80-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="c7b80-167">mshr_personnelnumber</span></span><br><span data-ttu-id="c7b80-168">*String*</span><span class="sxs-lookup"><span data-stu-id="c7b80-168">*String*</span></span> | <span data-ttu-id="c7b80-169">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c7b80-169">Read-only</span></span><br><span data-ttu-id="c7b80-170">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c7b80-170">Required</span></span> |<span data-ttu-id="c7b80-171">Töötaja kordumatu personalinumber.</span><span class="sxs-lookup"><span data-stu-id="c7b80-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="c7b80-172">**Päring**</span><span class="sxs-lookup"><span data-stu-id="c7b80-172">**Query**</span></span>

<span data-ttu-id="c7b80-173">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="c7b80-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="c7b80-174">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="c7b80-174">**Response**</span></span>

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
