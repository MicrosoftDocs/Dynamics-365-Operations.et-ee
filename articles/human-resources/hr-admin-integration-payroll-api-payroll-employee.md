---
title: Palgaarvestuse töövõtja
description: See teema annab üksikasjad ja näidispäringu Palgatöötaja olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: d3977b758f65875a36749a49459c2a81459a7b69
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881970"
---
# <a name="payroll-employee"></a><span data-ttu-id="06864-103">Palgaarvestuse töövõtja</span><span class="sxs-lookup"><span data-stu-id="06864-103">Payroll employee</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="06864-104">See teema annab üksikasjad ja näidispäringu Palgatöötaja olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="06864-104">This topic provides details and an example query for the Payroll employee entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="06864-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="06864-105">Properties</span></span>

| <span data-ttu-id="06864-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="06864-106">Property</span></span><br><span data-ttu-id="06864-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="06864-107">**Physical name**</span></span><br><span data-ttu-id="06864-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="06864-108">**_Type_**</span></span> | <span data-ttu-id="06864-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="06864-109">Use</span></span> | <span data-ttu-id="06864-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="06864-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="06864-111">**Personalinumber**</span><span class="sxs-lookup"><span data-stu-id="06864-111">**Personnel number**</span></span><br><span data-ttu-id="06864-112">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="06864-112">mshr_personnelnumber</span></span><br><span data-ttu-id="06864-113">*String*</span><span class="sxs-lookup"><span data-stu-id="06864-113">*String*</span></span> | <span data-ttu-id="06864-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-114">Read-only</span></span><br><span data-ttu-id="06864-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-115">Required</span></span> | <span data-ttu-id="06864-116">Töötaja kordumatu personalinumber.</span><span class="sxs-lookup"><span data-stu-id="06864-116">The employee's unique personnel number.</span></span> |
| <span data-ttu-id="06864-117">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="06864-117">**Primary field**</span></span><br><span data-ttu-id="06864-118">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="06864-118">mshr_primaryfield</span></span><br><span data-ttu-id="06864-119">*String*</span><span class="sxs-lookup"><span data-stu-id="06864-119">*String*</span></span> | <span data-ttu-id="06864-120">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-120">Required</span></span><br><span data-ttu-id="06864-121">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="06864-121">System generated</span></span> |  |
| <span data-ttu-id="06864-122">**Perekonnanimi**</span><span class="sxs-lookup"><span data-stu-id="06864-122">**Last name**</span></span><br><span data-ttu-id="06864-123">mshr_lastname</span><span class="sxs-lookup"><span data-stu-id="06864-123">mshr_lastname</span></span><br><span data-ttu-id="06864-124">*String*</span><span class="sxs-lookup"><span data-stu-id="06864-124">*String*</span></span> | <span data-ttu-id="06864-125">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-125">Read only</span></span><br><span data-ttu-id="06864-126">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-126">Required</span></span> | <span data-ttu-id="06864-127">Töötaja perekonnanimi.</span><span class="sxs-lookup"><span data-stu-id="06864-127">Employee last name.</span></span> |
| <span data-ttu-id="06864-128">**Juriidilise isiku ID**</span><span class="sxs-lookup"><span data-stu-id="06864-128">**Legal entity ID**</span></span><br><span data-ttu-id="06864-129">mshr_legalentityID</span><span class="sxs-lookup"><span data-stu-id="06864-129">mshr_legalentityID</span></span><br><span data-ttu-id="06864-130">*String*</span><span class="sxs-lookup"><span data-stu-id="06864-130">*String*</span></span> | <span data-ttu-id="06864-131">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-131">Read-only</span></span><br><span data-ttu-id="06864-132">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-132">Required</span></span> | <span data-ttu-id="06864-133">Määratleb juriidilise isiku (ettevõtte).</span><span class="sxs-lookup"><span data-stu-id="06864-133">Specifies the legal entity (company).</span></span> |
| <span data-ttu-id="06864-134">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="06864-134">**Valid from**</span></span><br><span data-ttu-id="06864-135">mshr_namevalidfrom</span><span class="sxs-lookup"><span data-stu-id="06864-135">mshr_namevalidfrom</span></span><br><span data-ttu-id="06864-136">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="06864-136">*Date Time Offset*</span></span> | <span data-ttu-id="06864-137">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-137">Read-only</span></span> <br><span data-ttu-id="06864-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-138">Required</span></span> | <span data-ttu-id="06864-139">Töötajaga seotud teabe kehtivuse algkuupäev.</span><span class="sxs-lookup"><span data-stu-id="06864-139">Date the employee information is valid from.</span></span>  |
| <span data-ttu-id="06864-140">**Sugu**</span><span class="sxs-lookup"><span data-stu-id="06864-140">**Gender**</span></span><br><span data-ttu-id="06864-141">mshr_gender</span><span class="sxs-lookup"><span data-stu-id="06864-141">mshr_gender</span></span><br><span data-ttu-id="06864-142">*Int32*</span><span class="sxs-lookup"><span data-stu-id="06864-142">*Int32*</span></span> | <span data-ttu-id="06864-143">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-143">Read-only</span></span><br><span data-ttu-id="06864-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-144">Required</span></span> | <span data-ttu-id="06864-145">Töötaja sugu.</span><span class="sxs-lookup"><span data-stu-id="06864-145">The employee's gender.</span></span> |
| <span data-ttu-id="06864-146">**Palgatöötaja olemi ID**</span><span class="sxs-lookup"><span data-stu-id="06864-146">**Payroll employee entity ID**</span></span><br><span data-ttu-id="06864-147">mshr_payrollemployeeentityid</span><span class="sxs-lookup"><span data-stu-id="06864-147">mshr_payrollemployeeentityid</span></span><br><span data-ttu-id="06864-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="06864-148">*GUID*</span></span> | <span data-ttu-id="06864-149">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-149">Required</span></span><br><span data-ttu-id="06864-150">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="06864-150">System generated</span></span> | <span data-ttu-id="06864-151">Süsteemi loodud GUID-väärtus töötaja kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="06864-151">A system-generated GUID value to uniquely identify the employee.</span></span> |
| <span data-ttu-id="06864-152">**Töösuhte alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="06864-152">**Employment start date**</span></span><br><span data-ttu-id="06864-153">mshr_employmentstartdate</span><span class="sxs-lookup"><span data-stu-id="06864-153">mshr_employmentstartdate</span></span><br><span data-ttu-id="06864-154">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="06864-154">*Date time offset*</span></span> | <span data-ttu-id="06864-155">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-155">Read-only</span></span><br><span data-ttu-id="06864-156">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-156">Required</span></span> | <span data-ttu-id="06864-157">Töötaja tööhõive alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="06864-157">The start date of the employee's employment.</span></span> |
| <span data-ttu-id="06864-158">**ID-tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="06864-158">**Identification type ID**</span></span><br><span data-ttu-id="06864-159">mshr_identificationtypeid</span><span class="sxs-lookup"><span data-stu-id="06864-159">mshr_identificationtypeid</span></span><br><span data-ttu-id="06864-160">*String*</span><span class="sxs-lookup"><span data-stu-id="06864-160">*String*</span></span> |<span data-ttu-id="06864-161">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-161">Read-only</span></span><br><span data-ttu-id="06864-162">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-162">Required</span></span> | <span data-ttu-id="06864-163">Töötaja jaoks määratletud ID-tüüp.</span><span class="sxs-lookup"><span data-stu-id="06864-163">The identification type defined for the employee.</span></span> |
| <span data-ttu-id="06864-164">**Töösuhte lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="06864-164">**Employment end date**</span></span><br><span data-ttu-id="06864-165">mshr_employmentenddate</span><span class="sxs-lookup"><span data-stu-id="06864-165">mshr_employmentenddate</span></span><br><span data-ttu-id="06864-166">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="06864-166">*Date time offset*</span></span> | <span data-ttu-id="06864-167">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-167">Read-only</span></span><br><span data-ttu-id="06864-168">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-168">Required</span></span> |<span data-ttu-id="06864-169">Töötaja tööhõive lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="06864-169">The end of the employee's employment.</span></span>  |
| <span data-ttu-id="06864-170">**Andmeala ID**</span><span class="sxs-lookup"><span data-stu-id="06864-170">**Data area ID**</span></span><br><span data-ttu-id="06864-171">mshr_dataareaid_id</span><span class="sxs-lookup"><span data-stu-id="06864-171">mshr_dataareaid_id</span></span><br><span data-ttu-id="06864-172">*GUID*</span><span class="sxs-lookup"><span data-stu-id="06864-172">*GUID*</span></span> | <span data-ttu-id="06864-173">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-173">Required</span></span> <br><span data-ttu-id="06864-174">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="06864-174">System generated</span></span> | <span data-ttu-id="06864-175">Süsteemi loodud GUID-väärtus, mis identifitseerib juriidilise isiku (ettevõtte).</span><span class="sxs-lookup"><span data-stu-id="06864-175">System-generated GUID value identifying the legal entity (company).</span></span> |
| <span data-ttu-id="06864-176">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="06864-176">**Valid to**</span></span><br><span data-ttu-id="06864-177">mshr_namevalidto</span><span class="sxs-lookup"><span data-stu-id="06864-177">mshr_namevalidto</span></span><br><span data-ttu-id="06864-178">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="06864-178">*Date Time Offset*</span></span> |  <span data-ttu-id="06864-179">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-179">Read-only</span></span><br><span data-ttu-id="06864-180">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-180">Required</span></span> | <span data-ttu-id="06864-181">Töötajaga seotud teabe kehtivuse lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="06864-181">Date the employee information is valid to.</span></span> |
| <span data-ttu-id="06864-182">**Sünnikuupäev**</span><span class="sxs-lookup"><span data-stu-id="06864-182">**Birth date**</span></span><br><span data-ttu-id="06864-183">mshr_birthdate</span><span class="sxs-lookup"><span data-stu-id="06864-183">mshr_birthdate</span></span><br><span data-ttu-id="06864-184">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="06864-184">*Date Time Offset*</span></span> | <span data-ttu-id="06864-185">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-185">Read-only</span></span> <br><span data-ttu-id="06864-186">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-186">Required</span></span> | <span data-ttu-id="06864-187">Töötaja sünnikuupäev</span><span class="sxs-lookup"><span data-stu-id="06864-187">The employee's birth date</span></span> |
| <span data-ttu-id="06864-188">**ID-number**</span><span class="sxs-lookup"><span data-stu-id="06864-188">**Identification number to**</span></span><br><span data-ttu-id="06864-189">mshr_identificationnumber</span><span class="sxs-lookup"><span data-stu-id="06864-189">mshr_identificationnumber</span></span><br><span data-ttu-id="06864-190">*String*</span><span class="sxs-lookup"><span data-stu-id="06864-190">*String*</span></span> | <span data-ttu-id="06864-191">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-191">Read-only</span></span> <br><span data-ttu-id="06864-192">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-192">Required</span></span> |<span data-ttu-id="06864-193">Töötaja jaoks määratletud ID-number.</span><span class="sxs-lookup"><span data-stu-id="06864-193">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="06864-194">**Eesnimi**</span><span class="sxs-lookup"><span data-stu-id="06864-194">**First name**</span></span><br><span data-ttu-id="06864-195">mshr_firstname</span><span class="sxs-lookup"><span data-stu-id="06864-195">mshr_firstname</span></span><br><span data-ttu-id="06864-196">*String*</span><span class="sxs-lookup"><span data-stu-id="06864-196">*String*</span></span> | <span data-ttu-id="06864-197">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-197">Read-only</span></span><br><span data-ttu-id="06864-198">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-198">Required</span></span> | <span data-ttu-id="06864-199">Töötaja eesnimi.</span><span class="sxs-lookup"><span data-stu-id="06864-199">Employee first name.</span></span> |
| <span data-ttu-id="06864-200">**Teine eesnimi**</span><span class="sxs-lookup"><span data-stu-id="06864-200">**Middle name**</span></span><br><span data-ttu-id="06864-201">mshr_middlename</span><span class="sxs-lookup"><span data-stu-id="06864-201">mshr_middlename</span></span><br><span data-ttu-id="06864-202">*String*</span><span class="sxs-lookup"><span data-stu-id="06864-202">*String*</span></span> | <span data-ttu-id="06864-203">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="06864-203">Read-only</span></span><br><span data-ttu-id="06864-204">Nõutav</span><span class="sxs-lookup"><span data-stu-id="06864-204">Required</span></span> |<span data-ttu-id="06864-205">Töötaja keskmine nimi.</span><span class="sxs-lookup"><span data-stu-id="06864-205">Employee middle name.</span></span>  |

## <a name="example-query-for-payroll-employee"></a><span data-ttu-id="06864-206">Palgatöötaja näidispäring</span><span class="sxs-lookup"><span data-stu-id="06864-206">Example query for Payroll employee</span></span>

<span data-ttu-id="06864-207">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="06864-207">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

<span data-ttu-id="06864-208">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="06864-208">**Response**</span></span>

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```