---
title: Palgaarvestuse töötaja aadress
description: See teema annab üksikasjad ja näidispäringu Palgtöötaja aadressi olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3407128b0172f0e253d51bcfa23a894f981e21e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052285"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="c375b-103">Palgaarvestuse töötaja aadress</span><span class="sxs-lookup"><span data-stu-id="c375b-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c375b-104">See teema annab üksikasjad ja näidispäringu Palgtöötaja aadressi olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c375b-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="c375b-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="c375b-105">Properties</span></span>

| <span data-ttu-id="c375b-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="c375b-106">Property</span></span><br><span data-ttu-id="c375b-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="c375b-107">**Physical name**</span></span><br><span data-ttu-id="c375b-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="c375b-108">**_Type_**</span></span> | <span data-ttu-id="c375b-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="c375b-109">Use</span></span> | <span data-ttu-id="c375b-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c375b-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c375b-111">**Linn**</span><span class="sxs-lookup"><span data-stu-id="c375b-111">**City**</span></span><br><span data-ttu-id="c375b-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="c375b-112">mshr_city</span></span><br><span data-ttu-id="c375b-113">*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-113">*String*</span></span> | <span data-ttu-id="c375b-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-114">Read-only</span></span><br><span data-ttu-id="c375b-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-115">Required</span></span> | <span data-ttu-id="c375b-116">Määratletud linna aadress.</span><span class="sxs-lookup"><span data-stu-id="c375b-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="c375b-117">**Personalinumber**</span><span class="sxs-lookup"><span data-stu-id="c375b-117">**Personnel number**</span></span><br><span data-ttu-id="c375b-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="c375b-118">mshr_personnelnumber</span></span><br><span data-ttu-id="c375b-119">*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-119">*String*</span></span> | <span data-ttu-id="c375b-120">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-120">Read-only</span></span><br><span data-ttu-id="c375b-121">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-121">Required</span></span> | <span data-ttu-id="c375b-122">Töötaja kordumatu personalinumber.</span><span class="sxs-lookup"><span data-stu-id="c375b-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="c375b-123">**Riik/regioon**</span><span class="sxs-lookup"><span data-stu-id="c375b-123">**Country region**</span></span><br><span data-ttu-id="c375b-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="c375b-124">mshr_countryregionid</span></span><br><span data-ttu-id="c375b-125">*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-125">*String*</span></span> | <span data-ttu-id="c375b-126">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-126">Read-only</span></span><br><span data-ttu-id="c375b-127">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-127">Required</span></span> | <span data-ttu-id="c375b-128">Defineeritud riigi või regiooni aadress</span><span class="sxs-lookup"><span data-stu-id="c375b-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="c375b-129">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="c375b-129">**Valid from**</span></span><br><span data-ttu-id="c375b-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="c375b-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="c375b-131">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="c375b-131">*Date Time Offset*</span></span> | <span data-ttu-id="c375b-132">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-132">Read-only</span></span> <br><span data-ttu-id="c375b-133">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-133">Required</span></span> | <span data-ttu-id="c375b-134">Aadressi kehtimise alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="c375b-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="c375b-135">**Töötas aadressil**</span><span class="sxs-lookup"><span data-stu-id="c375b-135">**Worked in address**</span></span><br><span data-ttu-id="c375b-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="c375b-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="c375b-137">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-137">Read-only</span></span><br><span data-ttu-id="c375b-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-138">Required</span></span> | <span data-ttu-id="c375b-139">Näitab, kas aadress on töötaja töökohaks.</span><span class="sxs-lookup"><span data-stu-id="c375b-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="c375b-140">**Maakond**</span><span class="sxs-lookup"><span data-stu-id="c375b-140">**County**</span></span><br><span data-ttu-id="c375b-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="c375b-141">mshr_county</span></span><br><span data-ttu-id="c375b-142">*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-142">*String*</span></span> | <span data-ttu-id="c375b-143">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-143">Read-only</span></span><br><span data-ttu-id="c375b-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-144">Required</span></span> | <span data-ttu-id="c375b-145">Määratletud riigi aadress.</span><span class="sxs-lookup"><span data-stu-id="c375b-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="c375b-146">**Palgatöötaja aadressi ID**</span><span class="sxs-lookup"><span data-stu-id="c375b-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="c375b-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="c375b-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="c375b-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c375b-148">*GUID*</span></span> | <span data-ttu-id="c375b-149">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-149">Required</span></span><br><span data-ttu-id="c375b-150">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="c375b-150">System generated</span></span> | <span data-ttu-id="c375b-151">Süsteemi loodud GUID-väärtus aadressi kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="c375b-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="c375b-152">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="c375b-152">**Primary field**</span></span><br><span data-ttu-id="c375b-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="c375b-153">mshr_primaryfield</span></span><br><span data-ttu-id="c375b-154">*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-154">*String*</span></span> | <span data-ttu-id="c375b-155">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-155">Read-only</span></span><br><span data-ttu-id="c375b-156">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-156">Required</span></span> |  |
| <span data-ttu-id="c375b-157">**Tänav**</span><span class="sxs-lookup"><span data-stu-id="c375b-157">**Street**</span></span><br><span data-ttu-id="c375b-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="c375b-158">mshr_street</span></span><br><span data-ttu-id="c375b-159">*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-159">*String*</span></span> | <span data-ttu-id="c375b-160">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-160">Read-only</span></span><br><span data-ttu-id="c375b-161">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-161">Required</span></span> | <span data-ttu-id="c375b-162">Aadressis määratletud tänav.</span><span class="sxs-lookup"><span data-stu-id="c375b-162">The street defined for the address.</span></span> |
| <span data-ttu-id="c375b-163">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="c375b-163">**Valid to**</span></span><br><span data-ttu-id="c375b-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="c375b-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="c375b-165">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="c375b-165">*Date Time Offset*</span></span> | <span data-ttu-id="c375b-166">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-166">Read-only</span></span> <br><span data-ttu-id="c375b-167">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-167">Required</span></span> | <span data-ttu-id="c375b-168">Aadressi kehtimise lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="c375b-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="c375b-169">**Asukoha ID**</span><span class="sxs-lookup"><span data-stu-id="c375b-169">**Location ID**</span></span><br><span data-ttu-id="c375b-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="c375b-171">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-171">Read-only</span></span> <br><span data-ttu-id="c375b-172">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-172">Required</span></span> | <span data-ttu-id="c375b-173">Aadressi ID.</span><span class="sxs-lookup"><span data-stu-id="c375b-173">The ID for the address.</span></span>  |
| <span data-ttu-id="c375b-174">**Sihtnumber**</span><span class="sxs-lookup"><span data-stu-id="c375b-174">**Postal code**</span></span><br><span data-ttu-id="c375b-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="c375b-175">mshr_zipcode</span></span><br><span data-ttu-id="c375b-176">*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-176">*String*</span></span> | <span data-ttu-id="c375b-177">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-177">Read-only</span></span> <br><span data-ttu-id="c375b-178">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-178">Required</span></span> |<span data-ttu-id="c375b-179">Töötaja jaoks määratletud ID-number.</span><span class="sxs-lookup"><span data-stu-id="c375b-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="c375b-180">**Elab aadressil**</span><span class="sxs-lookup"><span data-stu-id="c375b-180">**Lived in address**</span></span><br><span data-ttu-id="c375b-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="c375b-182">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-182">Read-only</span></span><br><span data-ttu-id="c375b-183">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-183">Required</span></span> | <span data-ttu-id="c375b-184">Näitab, kas aadress on töötaja elukohaks.</span><span class="sxs-lookup"><span data-stu-id="c375b-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="c375b-185">**Maakond**</span><span class="sxs-lookup"><span data-stu-id="c375b-185">**State**</span></span><br><span data-ttu-id="c375b-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="c375b-186">mshr_state</span></span><br><span data-ttu-id="c375b-187">*String*</span><span class="sxs-lookup"><span data-stu-id="c375b-187">*String*</span></span> | <span data-ttu-id="c375b-188">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="c375b-188">Read-only</span></span><br><span data-ttu-id="c375b-189">Nõutav</span><span class="sxs-lookup"><span data-stu-id="c375b-189">Required</span></span> | <span data-ttu-id="c375b-190">Aadressis määratletud maakond.</span><span class="sxs-lookup"><span data-stu-id="c375b-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="c375b-191">Näidispäring</span><span class="sxs-lookup"><span data-stu-id="c375b-191">Example query</span></span>

<span data-ttu-id="c375b-192">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="c375b-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="c375b-193">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="c375b-193">**Response**</span></span>

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
