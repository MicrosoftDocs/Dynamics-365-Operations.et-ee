---
title: Palgaarvestuse põhipalgaplaan
description: See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021292"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="7fa73-103">Palgaarvestuse põhipalgaplaan</span><span class="sxs-lookup"><span data-stu-id="7fa73-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7fa73-104">See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7fa73-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="7fa73-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="7fa73-105">Properties</span></span>

| <span data-ttu-id="7fa73-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="7fa73-106">Property</span></span><br><span data-ttu-id="7fa73-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="7fa73-107">**Physical name**</span></span><br><span data-ttu-id="7fa73-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="7fa73-108">**_Type_**</span></span> | <span data-ttu-id="7fa73-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="7fa73-109">Use</span></span> | <span data-ttu-id="7fa73-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="7fa73-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7fa73-111">**Töötaja ID**</span><span class="sxs-lookup"><span data-stu-id="7fa73-111">**Employee ID**</span></span><br><span data-ttu-id="7fa73-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="7fa73-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="7fa73-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7fa73-113">*GUID*</span></span> | <span data-ttu-id="7fa73-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-114">Read-only</span></span><br><span data-ttu-id="7fa73-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-115">Required</span></span><br><span data-ttu-id="7fa73-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="7fa73-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="7fa73-117">Töötaja ID</span><span class="sxs-lookup"><span data-stu-id="7fa73-117">Employee ID</span></span> |
| <span data-ttu-id="7fa73-118">**Tasumäär**</span><span class="sxs-lookup"><span data-stu-id="7fa73-118">**Pay rate**</span></span><br><span data-ttu-id="7fa73-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="7fa73-119">mshr_payrate</span></span><br><span data-ttu-id="7fa73-120">*Kümnendkoht*</span><span class="sxs-lookup"><span data-stu-id="7fa73-120">*Decimal*</span></span> | <span data-ttu-id="7fa73-121">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-121">Read-only</span></span><br><span data-ttu-id="7fa73-122">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-122">Required</span></span> | <span data-ttu-id="7fa73-123">Põhipalgaplaanis määratletud tasumäär.</span><span class="sxs-lookup"><span data-stu-id="7fa73-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="7fa73-124">**Plaani ID**</span><span class="sxs-lookup"><span data-stu-id="7fa73-124">**Plan ID**</span></span><br><span data-ttu-id="7fa73-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="7fa73-125">mshr_planid</span></span><br><span data-ttu-id="7fa73-126">*String*</span><span class="sxs-lookup"><span data-stu-id="7fa73-126">*String*</span></span> | <span data-ttu-id="7fa73-127">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-127">Read-only</span></span><br><span data-ttu-id="7fa73-128">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-128">Required</span></span> |<span data-ttu-id="7fa73-129">Määrab palgaplaani.</span><span class="sxs-lookup"><span data-stu-id="7fa73-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="7fa73-130">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="7fa73-130">**Valid from**</span></span><br><span data-ttu-id="7fa73-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="7fa73-131">mshr_validfrom</span></span><br><span data-ttu-id="7fa73-132">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="7fa73-132">*Date Time Offset*</span></span> |  <span data-ttu-id="7fa73-133">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-133">Read-only</span></span><br><span data-ttu-id="7fa73-134">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-134">Required</span></span> |<span data-ttu-id="7fa73-135">Töötajaga seotud põhipalga kehtivuse algkuupäev.</span><span class="sxs-lookup"><span data-stu-id="7fa73-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="7fa73-136">**Palgaarvestuse põhipalgaplaani olem**</span><span class="sxs-lookup"><span data-stu-id="7fa73-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="7fa73-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="7fa73-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="7fa73-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7fa73-138">*GUID*</span></span> | <span data-ttu-id="7fa73-139">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-139">Required</span></span><br><span data-ttu-id="7fa73-140">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="7fa73-140">Sytem generated</span></span> | <span data-ttu-id="7fa73-141">Süsteemi loodud GUID-väärtus palgaplaani kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="7fa73-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="7fa73-142">**Tasusagedus**</span><span class="sxs-lookup"><span data-stu-id="7fa73-142">**Pay frequency**</span></span><br><span data-ttu-id="7fa73-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="7fa73-143">mshr_payfrequency</span></span><br><span data-ttu-id="7fa73-144">*String*</span><span class="sxs-lookup"><span data-stu-id="7fa73-144">*String*</span></span> | <span data-ttu-id="7fa73-145">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-145">Read-only</span></span><br><span data-ttu-id="7fa73-146">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-146">Required</span></span> |<span data-ttu-id="7fa73-147">Töötajale makstava tasu maksmise sagedus.</span><span class="sxs-lookup"><span data-stu-id="7fa73-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="7fa73-148">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="7fa73-148">**Valid to**</span></span><br><span data-ttu-id="7fa73-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="7fa73-149">mshr_validto</span></span><br><span data-ttu-id="7fa73-150">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="7fa73-150">*Date Time Offset*</span></span> | <span data-ttu-id="7fa73-151">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-151">Read-only</span></span> <br><span data-ttu-id="7fa73-152">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-152">Required</span></span> | <span data-ttu-id="7fa73-153">Töötajaga seotud põhipalga kehtivuse lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="7fa73-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="7fa73-154">**Ametikoha ID**</span><span class="sxs-lookup"><span data-stu-id="7fa73-154">**Position ID**</span></span><br><span data-ttu-id="7fa73-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="7fa73-155">mshr_positionid</span></span><br><span data-ttu-id="7fa73-156">*String*</span><span class="sxs-lookup"><span data-stu-id="7fa73-156">*String*</span></span> | <span data-ttu-id="7fa73-157">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-157">Read-only</span></span> <br><span data-ttu-id="7fa73-158">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-158">Required</span></span> | <span data-ttu-id="7fa73-159">Töötaja ja põhipalgaplaani registreerimisega seotud ID.</span><span class="sxs-lookup"><span data-stu-id="7fa73-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="7fa73-160">**Currency**</span><span class="sxs-lookup"><span data-stu-id="7fa73-160">**Currency**</span></span><br><span data-ttu-id="7fa73-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="7fa73-161">mshr_currency</span></span><br><span data-ttu-id="7fa73-162">*String*</span><span class="sxs-lookup"><span data-stu-id="7fa73-162">*String*</span></span> | <span data-ttu-id="7fa73-163">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-163">Read-only</span></span> <br><span data-ttu-id="7fa73-164">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-164">Required</span></span> |<span data-ttu-id="7fa73-165">Põhipalgaplaani jaoks määratletud valuuta</span><span class="sxs-lookup"><span data-stu-id="7fa73-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="7fa73-166">**Personalinumber**</span><span class="sxs-lookup"><span data-stu-id="7fa73-166">**Personnel number**</span></span><br><span data-ttu-id="7fa73-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="7fa73-167">mshr_personnelnumber</span></span><br><span data-ttu-id="7fa73-168">*String*</span><span class="sxs-lookup"><span data-stu-id="7fa73-168">*String*</span></span> | <span data-ttu-id="7fa73-169">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="7fa73-169">Read-only</span></span><br><span data-ttu-id="7fa73-170">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7fa73-170">Required</span></span> |<span data-ttu-id="7fa73-171">Töötaja kordumatu personalinumber.</span><span class="sxs-lookup"><span data-stu-id="7fa73-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="7fa73-172">**Päring**</span><span class="sxs-lookup"><span data-stu-id="7fa73-172">**Query**</span></span>

<span data-ttu-id="7fa73-173">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="7fa73-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="7fa73-174">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="7fa73-174">**Response**</span></span>

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
