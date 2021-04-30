---
title: Palgaarvestuse töötaja aadress
description: See teema annab üksikasjad ja näidispäringu Palgtöötaja aadressi olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881966"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="db6f1-103">Palgaarvestuse töötaja aadress</span><span class="sxs-lookup"><span data-stu-id="db6f1-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="db6f1-104">See teema annab üksikasjad ja näidispäringu Palgtöötaja aadressi olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="db6f1-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="db6f1-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="db6f1-105">Properties</span></span>

| <span data-ttu-id="db6f1-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="db6f1-106">Property</span></span><br><span data-ttu-id="db6f1-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="db6f1-107">**Physical name**</span></span><br><span data-ttu-id="db6f1-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="db6f1-108">**_Type_**</span></span> | <span data-ttu-id="db6f1-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="db6f1-109">Use</span></span> | <span data-ttu-id="db6f1-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="db6f1-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="db6f1-111">**Linn**</span><span class="sxs-lookup"><span data-stu-id="db6f1-111">**City**</span></span><br><span data-ttu-id="db6f1-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="db6f1-112">mshr_city</span></span><br><span data-ttu-id="db6f1-113">*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-113">*String*</span></span> | <span data-ttu-id="db6f1-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-114">Read-only</span></span><br><span data-ttu-id="db6f1-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-115">Required</span></span> | <span data-ttu-id="db6f1-116">Määratletud linna aadress.</span><span class="sxs-lookup"><span data-stu-id="db6f1-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="db6f1-117">**Personalinumber**</span><span class="sxs-lookup"><span data-stu-id="db6f1-117">**Personnel number**</span></span><br><span data-ttu-id="db6f1-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="db6f1-118">mshr_personnelnumber</span></span><br><span data-ttu-id="db6f1-119">*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-119">*String*</span></span> | <span data-ttu-id="db6f1-120">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-120">Read-only</span></span><br><span data-ttu-id="db6f1-121">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-121">Required</span></span> | <span data-ttu-id="db6f1-122">Töötaja kordumatu personalinumber.</span><span class="sxs-lookup"><span data-stu-id="db6f1-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="db6f1-123">**Riik/regioon**</span><span class="sxs-lookup"><span data-stu-id="db6f1-123">**Country region**</span></span><br><span data-ttu-id="db6f1-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="db6f1-124">mshr_countryregionid</span></span><br><span data-ttu-id="db6f1-125">*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-125">*String*</span></span> | <span data-ttu-id="db6f1-126">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-126">Read-only</span></span><br><span data-ttu-id="db6f1-127">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-127">Required</span></span> | <span data-ttu-id="db6f1-128">Defineeritud riigi või regiooni aadress</span><span class="sxs-lookup"><span data-stu-id="db6f1-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="db6f1-129">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="db6f1-129">**Valid from**</span></span><br><span data-ttu-id="db6f1-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="db6f1-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="db6f1-131">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="db6f1-131">*Date Time Offset*</span></span> | <span data-ttu-id="db6f1-132">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-132">Read-only</span></span> <br><span data-ttu-id="db6f1-133">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-133">Required</span></span> | <span data-ttu-id="db6f1-134">Aadressi kehtimise alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="db6f1-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="db6f1-135">**Töötas aadressil**</span><span class="sxs-lookup"><span data-stu-id="db6f1-135">**Worked in address**</span></span><br><span data-ttu-id="db6f1-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="db6f1-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="db6f1-137">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-137">Read-only</span></span><br><span data-ttu-id="db6f1-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-138">Required</span></span> | <span data-ttu-id="db6f1-139">Näitab, kas aadress on töötaja töökohaks.</span><span class="sxs-lookup"><span data-stu-id="db6f1-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="db6f1-140">**Maakond**</span><span class="sxs-lookup"><span data-stu-id="db6f1-140">**County**</span></span><br><span data-ttu-id="db6f1-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="db6f1-141">mshr_county</span></span><br><span data-ttu-id="db6f1-142">*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-142">*String*</span></span> | <span data-ttu-id="db6f1-143">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-143">Read-only</span></span><br><span data-ttu-id="db6f1-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-144">Required</span></span> | <span data-ttu-id="db6f1-145">Määratletud riigi aadress.</span><span class="sxs-lookup"><span data-stu-id="db6f1-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="db6f1-146">**Palgatöötaja aadressi ID**</span><span class="sxs-lookup"><span data-stu-id="db6f1-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="db6f1-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="db6f1-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="db6f1-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="db6f1-148">*GUID*</span></span> | <span data-ttu-id="db6f1-149">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-149">Required</span></span><br><span data-ttu-id="db6f1-150">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="db6f1-150">System generated</span></span> | <span data-ttu-id="db6f1-151">Süsteemi loodud GUID-väärtus aadressi kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="db6f1-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="db6f1-152">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="db6f1-152">**Primary field**</span></span><br><span data-ttu-id="db6f1-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="db6f1-153">mshr_primaryfield</span></span><br><span data-ttu-id="db6f1-154">*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-154">*String*</span></span> | <span data-ttu-id="db6f1-155">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-155">Read-only</span></span><br><span data-ttu-id="db6f1-156">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-156">Required</span></span> |  |
| <span data-ttu-id="db6f1-157">**Tänav**</span><span class="sxs-lookup"><span data-stu-id="db6f1-157">**Street**</span></span><br><span data-ttu-id="db6f1-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="db6f1-158">mshr_street</span></span><br><span data-ttu-id="db6f1-159">*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-159">*String*</span></span> | <span data-ttu-id="db6f1-160">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-160">Read-only</span></span><br><span data-ttu-id="db6f1-161">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-161">Required</span></span> | <span data-ttu-id="db6f1-162">Aadressis määratletud tänav.</span><span class="sxs-lookup"><span data-stu-id="db6f1-162">The street defined for the address.</span></span> |
| <span data-ttu-id="db6f1-163">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="db6f1-163">**Valid to**</span></span><br><span data-ttu-id="db6f1-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="db6f1-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="db6f1-165">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="db6f1-165">*Date Time Offset*</span></span> | <span data-ttu-id="db6f1-166">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-166">Read-only</span></span> <br><span data-ttu-id="db6f1-167">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-167">Required</span></span> | <span data-ttu-id="db6f1-168">Aadressi kehtimise lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="db6f1-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="db6f1-169">**Asukoha ID**</span><span class="sxs-lookup"><span data-stu-id="db6f1-169">**Location ID**</span></span><br><span data-ttu-id="db6f1-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="db6f1-171">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-171">Read-only</span></span> <br><span data-ttu-id="db6f1-172">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-172">Required</span></span> | <span data-ttu-id="db6f1-173">Aadressi ID.</span><span class="sxs-lookup"><span data-stu-id="db6f1-173">The ID for the address.</span></span>  |
| <span data-ttu-id="db6f1-174">**Sihtnumber**</span><span class="sxs-lookup"><span data-stu-id="db6f1-174">**Postal code**</span></span><br><span data-ttu-id="db6f1-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="db6f1-175">mshr_zipcode</span></span><br><span data-ttu-id="db6f1-176">*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-176">*String*</span></span> | <span data-ttu-id="db6f1-177">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-177">Read-only</span></span> <br><span data-ttu-id="db6f1-178">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-178">Required</span></span> |<span data-ttu-id="db6f1-179">Töötaja jaoks määratletud ID-number.</span><span class="sxs-lookup"><span data-stu-id="db6f1-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="db6f1-180">**Elab aadressil**</span><span class="sxs-lookup"><span data-stu-id="db6f1-180">**Lived in address**</span></span><br><span data-ttu-id="db6f1-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="db6f1-182">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-182">Read-only</span></span><br><span data-ttu-id="db6f1-183">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-183">Required</span></span> | <span data-ttu-id="db6f1-184">Näitab, kas aadress on töötaja elukohaks.</span><span class="sxs-lookup"><span data-stu-id="db6f1-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="db6f1-185">**Maakond**</span><span class="sxs-lookup"><span data-stu-id="db6f1-185">**State**</span></span><br><span data-ttu-id="db6f1-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="db6f1-186">mshr_state</span></span><br><span data-ttu-id="db6f1-187">*String*</span><span class="sxs-lookup"><span data-stu-id="db6f1-187">*String*</span></span> | <span data-ttu-id="db6f1-188">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="db6f1-188">Read-only</span></span><br><span data-ttu-id="db6f1-189">Nõutav</span><span class="sxs-lookup"><span data-stu-id="db6f1-189">Required</span></span> | <span data-ttu-id="db6f1-190">Aadressis määratletud maakond.</span><span class="sxs-lookup"><span data-stu-id="db6f1-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="db6f1-191">Näidispäring</span><span class="sxs-lookup"><span data-stu-id="db6f1-191">Example query</span></span>

<span data-ttu-id="db6f1-192">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="db6f1-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="db6f1-193">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="db6f1-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
