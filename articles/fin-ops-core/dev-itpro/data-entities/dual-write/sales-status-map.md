---
title: Müügitellimuse olekuväljade vastendamise seadistamine
description: Selles teemas selgitatakse, kuidas seadistada müügitellimuse olekuvälju topeltkirjutamiseks.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4451749"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="6e914-103">Müügitellimuse olekuväljade vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="6e914-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6e914-104">Müügitellimuse olekut näitavate väljadel on rakendustes Microsoft Dynamics 365 Supply Chain Management ja Dynamics 365 Sales erinevad loetelu väärtused.</span><span class="sxs-lookup"><span data-stu-id="6e914-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="6e914-105">Nende väljade vastendamiseks topeltkirjutamises on vajalik lisaseadistus.</span><span class="sxs-lookup"><span data-stu-id="6e914-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="6e914-106">Väljad rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6e914-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="6e914-107">Rakenduses Supply Chain Management näitavad müügitellimuse olekut kaks välja.</span><span class="sxs-lookup"><span data-stu-id="6e914-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="6e914-108">Väljad, mida peate vastendama, on **Olek** ja **Dokumendi olek**.</span><span class="sxs-lookup"><span data-stu-id="6e914-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="6e914-109">Loetelu **Olek** näitab tellimuse üldist olekut.</span><span class="sxs-lookup"><span data-stu-id="6e914-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="6e914-110">See olek kuvatakse tellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="6e914-110">This status is shown on the order header.</span></span>

<span data-ttu-id="6e914-111">Loetelul **Olek** on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="6e914-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="6e914-112">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-112">Open Order</span></span>
- <span data-ttu-id="6e914-113">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="6e914-113">Delivered</span></span>
- <span data-ttu-id="6e914-114">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="6e914-114">Invoiced</span></span>
- <span data-ttu-id="6e914-115">Cancelled</span><span class="sxs-lookup"><span data-stu-id="6e914-115">Cancelled</span></span>

<span data-ttu-id="6e914-116">Loetelu **Dokumendi olek** täpsustab kõige hiljutisemat tellimuse jaoks loodud dokumenti.</span><span class="sxs-lookup"><span data-stu-id="6e914-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="6e914-117">Näiteks kui tellimus on kinnitatud, on see dokument müügitellimuse kinnitus.</span><span class="sxs-lookup"><span data-stu-id="6e914-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="6e914-118">Kui müügitellimus on osaliselt arveldatud ja seejärel kinnitatakse järelejäänud rida, jääb dokumendi olekuks **Arve**, kuna arve luuakse protsessis hiljem.</span><span class="sxs-lookup"><span data-stu-id="6e914-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="6e914-119">Loetelul **Dokumendi olek** on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="6e914-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="6e914-120">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="6e914-120">Confirmation</span></span>
- <span data-ttu-id="6e914-121">Komplekteerimisleht</span><span class="sxs-lookup"><span data-stu-id="6e914-121">Picking List</span></span>
- <span data-ttu-id="6e914-122">Saateleht</span><span class="sxs-lookup"><span data-stu-id="6e914-122">Packing Slip</span></span>
- <span data-ttu-id="6e914-123">Arve</span><span class="sxs-lookup"><span data-stu-id="6e914-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="6e914-124">Väljad rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="6e914-124">Fields in Sales</span></span>

<span data-ttu-id="6e914-125">Rakenduses Sales näitavad tellimuse olekut kaks välja.</span><span class="sxs-lookup"><span data-stu-id="6e914-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="6e914-126">Väljad, mida peate vastendama, on **Olek** ja **Töötlemise olek**.</span><span class="sxs-lookup"><span data-stu-id="6e914-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="6e914-127">Loetelu **Olek** näitab tellimuse üldist olekut.</span><span class="sxs-lookup"><span data-stu-id="6e914-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="6e914-128">Sellel on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="6e914-128">It has the following values:</span></span>

- <span data-ttu-id="6e914-129">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="6e914-129">Active</span></span>
- <span data-ttu-id="6e914-130">Edastatud</span><span class="sxs-lookup"><span data-stu-id="6e914-130">Submitted</span></span>
- <span data-ttu-id="6e914-131">Täidetud</span><span class="sxs-lookup"><span data-stu-id="6e914-131">Fulfilled</span></span>
- <span data-ttu-id="6e914-132">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="6e914-132">Invoiced</span></span>
- <span data-ttu-id="6e914-133">Cancelled</span><span class="sxs-lookup"><span data-stu-id="6e914-133">Cancelled</span></span>

<span data-ttu-id="6e914-134">Loetelu **Töötlemise olek** võeti kasutusele, et olekut saaks rakendusega Supply Chain Management täpsemini vastendada.</span><span class="sxs-lookup"><span data-stu-id="6e914-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="6e914-135">Järgmises tabelis on toodud suvandi **Töötlemise olek** vastendus rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6e914-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="6e914-136">Töötlemise olek</span><span class="sxs-lookup"><span data-stu-id="6e914-136">Processing Status</span></span>   | <span data-ttu-id="6e914-137">Olek rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6e914-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="6e914-138">Dokumendi olek rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6e914-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="6e914-139">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="6e914-139">Active</span></span>              | <span data-ttu-id="6e914-140">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-140">Open Order</span></span>                        | <span data-ttu-id="6e914-141">None</span><span class="sxs-lookup"><span data-stu-id="6e914-141">None</span></span>                                       |
| <span data-ttu-id="6e914-142">Kinnitatud</span><span class="sxs-lookup"><span data-stu-id="6e914-142">Confirmed</span></span>           | <span data-ttu-id="6e914-143">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-143">Open Order</span></span>                        | <span data-ttu-id="6e914-144">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="6e914-144">Confirmation</span></span>                               |
| <span data-ttu-id="6e914-145">Valitud</span><span class="sxs-lookup"><span data-stu-id="6e914-145">Picked</span></span>              | <span data-ttu-id="6e914-146">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-146">Open Order</span></span>                        | <span data-ttu-id="6e914-147">Komplekteerimisleht</span><span class="sxs-lookup"><span data-stu-id="6e914-147">Picking List</span></span>                               |
| <span data-ttu-id="6e914-148">Osaliselt tarnitud</span><span class="sxs-lookup"><span data-stu-id="6e914-148">Partially Delivered</span></span> | <span data-ttu-id="6e914-149">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-149">Open Order</span></span>                        | <span data-ttu-id="6e914-150">Saateleht</span><span class="sxs-lookup"><span data-stu-id="6e914-150">Packing Slip</span></span>                               |
| <span data-ttu-id="6e914-151">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="6e914-151">Delivered</span></span>           | <span data-ttu-id="6e914-152">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="6e914-152">Delivered</span></span>                         | <span data-ttu-id="6e914-153">Saateleht</span><span class="sxs-lookup"><span data-stu-id="6e914-153">Packing Slip</span></span>                               |
| <span data-ttu-id="6e914-154">Osaliselt arvele kantud</span><span class="sxs-lookup"><span data-stu-id="6e914-154">Partially Invoiced</span></span>  | <span data-ttu-id="6e914-155">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="6e914-155">Delivered</span></span>                         | <span data-ttu-id="6e914-156">Arve</span><span class="sxs-lookup"><span data-stu-id="6e914-156">Invoice</span></span>                                    |
| <span data-ttu-id="6e914-157">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="6e914-157">Invoiced</span></span>            | <span data-ttu-id="6e914-158">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="6e914-158">Invoiced</span></span>                          | <span data-ttu-id="6e914-159">Arve</span><span class="sxs-lookup"><span data-stu-id="6e914-159">Invoice</span></span>                                    |
| <span data-ttu-id="6e914-160">Cancelled</span><span class="sxs-lookup"><span data-stu-id="6e914-160">Cancelled</span></span>           | <span data-ttu-id="6e914-161">Cancelled</span><span class="sxs-lookup"><span data-stu-id="6e914-161">Cancelled</span></span>                         | <span data-ttu-id="6e914-162">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="6e914-162">Not applicable</span></span>                             |

<span data-ttu-id="6e914-163">Järgmises tabelis on toodud suvandi **Töötlemise olek** vastendus rakendustes Sales ja Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6e914-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="6e914-164">Töötlemise olek</span><span class="sxs-lookup"><span data-stu-id="6e914-164">Processing Status</span></span>   | <span data-ttu-id="6e914-165">Olek rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="6e914-165">Status in Sales</span></span> | <span data-ttu-id="6e914-166">Olek rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6e914-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="6e914-167">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="6e914-167">Active</span></span>              | <span data-ttu-id="6e914-168">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="6e914-168">Active</span></span>          | <span data-ttu-id="6e914-169">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-169">Open Order</span></span>                        |
| <span data-ttu-id="6e914-170">Kinnitatud</span><span class="sxs-lookup"><span data-stu-id="6e914-170">Confirmed</span></span>           | <span data-ttu-id="6e914-171">Edastatud</span><span class="sxs-lookup"><span data-stu-id="6e914-171">Submitted</span></span>       | <span data-ttu-id="6e914-172">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-172">Open Order</span></span>                        |
| <span data-ttu-id="6e914-173">Valitud</span><span class="sxs-lookup"><span data-stu-id="6e914-173">Picked</span></span>              | <span data-ttu-id="6e914-174">Edastatud</span><span class="sxs-lookup"><span data-stu-id="6e914-174">Submitted</span></span>       | <span data-ttu-id="6e914-175">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-175">Open Order</span></span>                        |
| <span data-ttu-id="6e914-176">Osaliselt tarnitud</span><span class="sxs-lookup"><span data-stu-id="6e914-176">Partially Delivered</span></span> | <span data-ttu-id="6e914-177">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="6e914-177">Active</span></span>          | <span data-ttu-id="6e914-178">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-178">Open Order</span></span>                        |
| <span data-ttu-id="6e914-179">Osaliselt arvele kantud</span><span class="sxs-lookup"><span data-stu-id="6e914-179">Partially Invoiced</span></span>  | <span data-ttu-id="6e914-180">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="6e914-180">Active</span></span>          | <span data-ttu-id="6e914-181">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="6e914-181">Open Order</span></span>                        |
| <span data-ttu-id="6e914-182">Osaliselt arvele kantud</span><span class="sxs-lookup"><span data-stu-id="6e914-182">Partially Invoiced</span></span>  | <span data-ttu-id="6e914-183">Täidetud</span><span class="sxs-lookup"><span data-stu-id="6e914-183">Fulfilled</span></span>       | <span data-ttu-id="6e914-184">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="6e914-184">Delivered</span></span>                         |
| <span data-ttu-id="6e914-185">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="6e914-185">Invoiced</span></span>            | <span data-ttu-id="6e914-186">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="6e914-186">Invoiced</span></span>        | <span data-ttu-id="6e914-187">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="6e914-187">Invoiced</span></span>                          |
| <span data-ttu-id="6e914-188">Cancelled</span><span class="sxs-lookup"><span data-stu-id="6e914-188">Cancelled</span></span>           | <span data-ttu-id="6e914-189">Cancelled</span><span class="sxs-lookup"><span data-stu-id="6e914-189">Cancelled</span></span>       | <span data-ttu-id="6e914-190">Cancelled</span><span class="sxs-lookup"><span data-stu-id="6e914-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="6e914-191">Seadistus</span><span class="sxs-lookup"><span data-stu-id="6e914-191">Setup</span></span>

<span data-ttu-id="6e914-192">Müügitellimuse olekuväljade vastendamise seadistamiseks peate lubama atribuudid **IsSOPIntegrationEnabled** ja **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="6e914-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="6e914-193">Atribuudi **IsSOPIntegrationEnabled** lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6e914-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="6e914-194">Avage brauseris leht `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="6e914-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="6e914-195">Asendage **\<test-name\>** oma ettevõtte rakenduse Sales lingiga.</span><span class="sxs-lookup"><span data-stu-id="6e914-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="6e914-196">Otsige avatud lehel üles **organizationid** ja kirjutage selle väärtus üles.</span><span class="sxs-lookup"><span data-stu-id="6e914-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Väärtuse organizationid leidmine](media/sales-map-orgid.png)

3. <span data-ttu-id="6e914-198">Avage rakenduses Sales brauserikonsool ja käivitage järgmine skript.</span><span class="sxs-lookup"><span data-stu-id="6e914-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="6e914-199">Kasutage sammust 2 pärit üksuse **organizationid** väärtust.</span><span class="sxs-lookup"><span data-stu-id="6e914-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScripti kood brauserikonsoolis](media/sales-map-script.png)

4. <span data-ttu-id="6e914-201">Veenduge, et suvandi **IsSOPIntegrationEnabled** väärtuseks oleks seatud **tõene**.</span><span class="sxs-lookup"><span data-stu-id="6e914-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="6e914-202">Kasutage väärtuse kontrollimiseks sammust 1 pärit URL-i.</span><span class="sxs-lookup"><span data-stu-id="6e914-202">Use the URL from step 1 to check the value.</span></span>

    ![Tõeseks seatud IsSOPIntegrationEnabled](media/sales-map-integration-enabled.png)

<span data-ttu-id="6e914-204">Atribuudi **isIntegrationUser** lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6e914-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="6e914-205">Valige rakenduses Sales **Sätted \> Kohandamine \> Kohanda süsteemi**, valige **Kasutajaüksus** ja seejärel avage **Vorm \> Kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="6e914-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Kasutaja vormi avamine](media/sales-map-user.png)

2. <span data-ttu-id="6e914-207">Leidke väljauurijas üles **Integratsiooni kasutaja režiim** ja topeltklõpsake sellel, et lisada see vormile.</span><span class="sxs-lookup"><span data-stu-id="6e914-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="6e914-208">Salvestage muudatus.</span><span class="sxs-lookup"><span data-stu-id="6e914-208">Save your change.</span></span>

    ![Integratsiooni kasutaja režiimi välja lisamine vormile](media/sales-map-field-explorer.png)

3. <span data-ttu-id="6e914-210">Valige rakenduses Sales **Sätted \> Turve \> Kasutajad** ja muutke vaade väärtuselt **Lubatud kasutajad** väärtusele **Rakenduse kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="6e914-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Vaate muutmine lubatud kasutajatelt rakenduse kasutajatele](media/sales-map-enabled-users.png)

4. <span data-ttu-id="6e914-212">Valige kaks kirjet nimega **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="6e914-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Rakenduse kasutajate loend](media/sales-map-user-mode.png)

5. <span data-ttu-id="6e914-214">Muutke välja **Integratsiooni kasutaja režiim** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6e914-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Integratsiooni kasutaja režiimi välja väärtuse muutmine](media/sales-map-user-mode-yes.png)

<span data-ttu-id="6e914-216">Teie müügitellimused on nüüd vastendatud.</span><span class="sxs-lookup"><span data-stu-id="6e914-216">Your sales orders are now mapped.</span></span>
