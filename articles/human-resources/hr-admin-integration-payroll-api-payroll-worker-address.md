---
title: Palgaarvestuse töötaja aadress
description: See teema annab üksikasjad ja näidispäringu Palgtöötaja aadressi olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020701"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="3b49a-103">Palgaarvestuse töötaja aadress</span><span class="sxs-lookup"><span data-stu-id="3b49a-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3b49a-104">See teema annab üksikasjad ja näidispäringu Palgtöötaja aadressi olemi kohta rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3b49a-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="3b49a-105">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="3b49a-105">Properties</span></span>

| <span data-ttu-id="3b49a-106">Atribuut</span><span class="sxs-lookup"><span data-stu-id="3b49a-106">Property</span></span><br><span data-ttu-id="3b49a-107">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="3b49a-107">**Physical name**</span></span><br><span data-ttu-id="3b49a-108">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="3b49a-108">**_Type_**</span></span> | <span data-ttu-id="3b49a-109">Kasuta</span><span class="sxs-lookup"><span data-stu-id="3b49a-109">Use</span></span> | <span data-ttu-id="3b49a-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3b49a-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3b49a-111">**Linn**</span><span class="sxs-lookup"><span data-stu-id="3b49a-111">**City**</span></span><br><span data-ttu-id="3b49a-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="3b49a-112">mshr_city</span></span><br><span data-ttu-id="3b49a-113">*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-113">*String*</span></span> | <span data-ttu-id="3b49a-114">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-114">Read-only</span></span><br><span data-ttu-id="3b49a-115">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-115">Required</span></span> | <span data-ttu-id="3b49a-116">Määratletud linna aadress.</span><span class="sxs-lookup"><span data-stu-id="3b49a-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="3b49a-117">**Personalinumber**</span><span class="sxs-lookup"><span data-stu-id="3b49a-117">**Personnel number**</span></span><br><span data-ttu-id="3b49a-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="3b49a-118">mshr_personnelnumber</span></span><br><span data-ttu-id="3b49a-119">*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-119">*String*</span></span> | <span data-ttu-id="3b49a-120">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-120">Read-only</span></span><br><span data-ttu-id="3b49a-121">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-121">Required</span></span> | <span data-ttu-id="3b49a-122">Töötaja kordumatu personalinumber.</span><span class="sxs-lookup"><span data-stu-id="3b49a-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="3b49a-123">**Riik/regioon**</span><span class="sxs-lookup"><span data-stu-id="3b49a-123">**Country region**</span></span><br><span data-ttu-id="3b49a-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="3b49a-124">mshr_countryregionid</span></span><br><span data-ttu-id="3b49a-125">*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-125">*String*</span></span> | <span data-ttu-id="3b49a-126">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-126">Read-only</span></span><br><span data-ttu-id="3b49a-127">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-127">Required</span></span> | <span data-ttu-id="3b49a-128">Defineeritud riigi või regiooni aadress</span><span class="sxs-lookup"><span data-stu-id="3b49a-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="3b49a-129">**Kehtiv alates**</span><span class="sxs-lookup"><span data-stu-id="3b49a-129">**Valid from**</span></span><br><span data-ttu-id="3b49a-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="3b49a-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="3b49a-131">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="3b49a-131">*Date Time Offset*</span></span> | <span data-ttu-id="3b49a-132">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-132">Read-only</span></span> <br><span data-ttu-id="3b49a-133">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-133">Required</span></span> | <span data-ttu-id="3b49a-134">Aadressi kehtimise alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="3b49a-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="3b49a-135">**Töötas aadressil**</span><span class="sxs-lookup"><span data-stu-id="3b49a-135">**Worked in address**</span></span><br><span data-ttu-id="3b49a-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="3b49a-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="3b49a-137">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-137">Read-only</span></span><br><span data-ttu-id="3b49a-138">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-138">Required</span></span> | <span data-ttu-id="3b49a-139">Näitab, kas aadress on töötaja töökohaks.</span><span class="sxs-lookup"><span data-stu-id="3b49a-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="3b49a-140">**Maakond**</span><span class="sxs-lookup"><span data-stu-id="3b49a-140">**County**</span></span><br><span data-ttu-id="3b49a-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="3b49a-141">mshr_county</span></span><br><span data-ttu-id="3b49a-142">*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-142">*String*</span></span> | <span data-ttu-id="3b49a-143">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-143">Read-only</span></span><br><span data-ttu-id="3b49a-144">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-144">Required</span></span> | <span data-ttu-id="3b49a-145">Määratletud riigi aadress.</span><span class="sxs-lookup"><span data-stu-id="3b49a-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="3b49a-146">**Palgatöötaja aadressi ID**</span><span class="sxs-lookup"><span data-stu-id="3b49a-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="3b49a-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="3b49a-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="3b49a-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3b49a-148">*GUID*</span></span> | <span data-ttu-id="3b49a-149">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-149">Required</span></span><br><span data-ttu-id="3b49a-150">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="3b49a-150">System generated</span></span> | <span data-ttu-id="3b49a-151">Süsteemi loodud GUID-väärtus aadressi kordumatuks tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="3b49a-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="3b49a-152">**Esmane väli**</span><span class="sxs-lookup"><span data-stu-id="3b49a-152">**Primary field**</span></span><br><span data-ttu-id="3b49a-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3b49a-153">mshr_primaryfield</span></span><br><span data-ttu-id="3b49a-154">*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-154">*String*</span></span> | <span data-ttu-id="3b49a-155">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-155">Read-only</span></span><br><span data-ttu-id="3b49a-156">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-156">Required</span></span> |  |
| <span data-ttu-id="3b49a-157">**Tänav**</span><span class="sxs-lookup"><span data-stu-id="3b49a-157">**Street**</span></span><br><span data-ttu-id="3b49a-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="3b49a-158">mshr_street</span></span><br><span data-ttu-id="3b49a-159">*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-159">*String*</span></span> | <span data-ttu-id="3b49a-160">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-160">Read-only</span></span><br><span data-ttu-id="3b49a-161">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-161">Required</span></span> | <span data-ttu-id="3b49a-162">Aadressis määratletud tänav.</span><span class="sxs-lookup"><span data-stu-id="3b49a-162">The street defined for the address.</span></span> |
| <span data-ttu-id="3b49a-163">**Kehtiv kuni**</span><span class="sxs-lookup"><span data-stu-id="3b49a-163">**Valid to**</span></span><br><span data-ttu-id="3b49a-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="3b49a-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="3b49a-165">*Kuupäeva ja kellaaja nihe*</span><span class="sxs-lookup"><span data-stu-id="3b49a-165">*Date Time Offset*</span></span> | <span data-ttu-id="3b49a-166">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-166">Read-only</span></span> <br><span data-ttu-id="3b49a-167">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-167">Required</span></span> | <span data-ttu-id="3b49a-168">Aadressi kehtimise lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="3b49a-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="3b49a-169">**Asukoha ID**</span><span class="sxs-lookup"><span data-stu-id="3b49a-169">**Location ID**</span></span><br><span data-ttu-id="3b49a-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="3b49a-171">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-171">Read-only</span></span> <br><span data-ttu-id="3b49a-172">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-172">Required</span></span> | <span data-ttu-id="3b49a-173">Aadressi ID.</span><span class="sxs-lookup"><span data-stu-id="3b49a-173">The ID for the address.</span></span>  |
| <span data-ttu-id="3b49a-174">**Sihtnumber**</span><span class="sxs-lookup"><span data-stu-id="3b49a-174">**Postal code**</span></span><br><span data-ttu-id="3b49a-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="3b49a-175">mshr_zipcode</span></span><br><span data-ttu-id="3b49a-176">*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-176">*String*</span></span> | <span data-ttu-id="3b49a-177">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-177">Read-only</span></span> <br><span data-ttu-id="3b49a-178">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-178">Required</span></span> |<span data-ttu-id="3b49a-179">Töötaja jaoks määratletud ID-number.</span><span class="sxs-lookup"><span data-stu-id="3b49a-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="3b49a-180">**Elab aadressil**</span><span class="sxs-lookup"><span data-stu-id="3b49a-180">**Lived in address**</span></span><br><span data-ttu-id="3b49a-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="3b49a-182">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-182">Read-only</span></span><br><span data-ttu-id="3b49a-183">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-183">Required</span></span> | <span data-ttu-id="3b49a-184">Näitab, kas aadress on töötaja elukohaks.</span><span class="sxs-lookup"><span data-stu-id="3b49a-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="3b49a-185">**Maakond**</span><span class="sxs-lookup"><span data-stu-id="3b49a-185">**State**</span></span><br><span data-ttu-id="3b49a-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="3b49a-186">mshr_state</span></span><br><span data-ttu-id="3b49a-187">*String*</span><span class="sxs-lookup"><span data-stu-id="3b49a-187">*String*</span></span> | <span data-ttu-id="3b49a-188">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="3b49a-188">Read-only</span></span><br><span data-ttu-id="3b49a-189">Nõutav</span><span class="sxs-lookup"><span data-stu-id="3b49a-189">Required</span></span> | <span data-ttu-id="3b49a-190">Aadressis määratletud maakond.</span><span class="sxs-lookup"><span data-stu-id="3b49a-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="3b49a-191">Näidispäring</span><span class="sxs-lookup"><span data-stu-id="3b49a-191">Example query</span></span>

<span data-ttu-id="3b49a-192">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="3b49a-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="3b49a-193">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="3b49a-193">**Response**</span></span>

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
