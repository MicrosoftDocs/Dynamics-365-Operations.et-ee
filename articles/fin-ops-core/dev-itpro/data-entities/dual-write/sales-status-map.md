---
title: Müügitellimuse olekuveergude vastendamise seadistamine
description: Selles teemas selgitatakse, kuidas seadistada müügitellimuse olekuveerge topeltkirjutamiseks.
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
ms.openlocfilehash: cc70501d231390ea15104d508a36300a1b2cd44c
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744295"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="207de-103">Müügitellimuse olekuveergude vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="207de-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="207de-104">Müügitellimuse olekut näitavatel veergudel on rakendustes Microsoft Dynamics 365 Supply Chain Management ja Dynamics 365 Sales erinevad loetelu väärtused.</span><span class="sxs-lookup"><span data-stu-id="207de-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="207de-105">Nende veergude vastendamiseks topeltkirjutamises on vajalik lisaseadistus.</span><span class="sxs-lookup"><span data-stu-id="207de-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="207de-106">veerud rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="207de-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="207de-107">Rakenduses Supply Chain Management näitavad müügitellimuse olekut kaks veergu.</span><span class="sxs-lookup"><span data-stu-id="207de-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="207de-108">Veerud, mida peate vastendama, on **Olek** ja **Dokumendi olek**.</span><span class="sxs-lookup"><span data-stu-id="207de-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="207de-109">Loetelu **Olek** näitab tellimuse üldist olekut.</span><span class="sxs-lookup"><span data-stu-id="207de-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="207de-110">See olek kuvatakse tellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="207de-110">This status is shown on the order header.</span></span>

<span data-ttu-id="207de-111">Loetelul **Olek** on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="207de-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="207de-112">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-112">Open Order</span></span>
- <span data-ttu-id="207de-113">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="207de-113">Delivered</span></span>
- <span data-ttu-id="207de-114">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="207de-114">Invoiced</span></span>
- <span data-ttu-id="207de-115">Cancelled</span><span class="sxs-lookup"><span data-stu-id="207de-115">Cancelled</span></span>

<span data-ttu-id="207de-116">Loetelu **Dokumendi olek** täpsustab kõige hiljutisemat tellimuse jaoks loodud dokumenti.</span><span class="sxs-lookup"><span data-stu-id="207de-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="207de-117">Näiteks kui tellimus on kinnitatud, on see dokument müügitellimuse kinnitus.</span><span class="sxs-lookup"><span data-stu-id="207de-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="207de-118">Kui müügitellimus on osaliselt arveldatud ja seejärel kinnitatakse järelejäänud rida, jääb dokumendi olekuks **Arve**, kuna arve luuakse protsessis hiljem.</span><span class="sxs-lookup"><span data-stu-id="207de-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="207de-119">Loetelul **Dokumendi olek** on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="207de-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="207de-120">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="207de-120">Confirmation</span></span>
- <span data-ttu-id="207de-121">Komplekteerimisleht</span><span class="sxs-lookup"><span data-stu-id="207de-121">Picking List</span></span>
- <span data-ttu-id="207de-122">Saateleht</span><span class="sxs-lookup"><span data-stu-id="207de-122">Packing Slip</span></span>
- <span data-ttu-id="207de-123">Arve</span><span class="sxs-lookup"><span data-stu-id="207de-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="207de-124">veerud rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="207de-124">columns in Sales</span></span>

<span data-ttu-id="207de-125">Rakenduses Sales näitavad tellimuse olekut kaks veergu.</span><span class="sxs-lookup"><span data-stu-id="207de-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="207de-126">Veerud, mida peate vastendama, on **Olek** ja **Töötlemise olek**.</span><span class="sxs-lookup"><span data-stu-id="207de-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="207de-127">Loetelu **Olek** näitab tellimuse üldist olekut.</span><span class="sxs-lookup"><span data-stu-id="207de-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="207de-128">Sellel on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="207de-128">It has the following values:</span></span>

- <span data-ttu-id="207de-129">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="207de-129">Active</span></span>
- <span data-ttu-id="207de-130">Edastatud</span><span class="sxs-lookup"><span data-stu-id="207de-130">Submitted</span></span>
- <span data-ttu-id="207de-131">Täidetud</span><span class="sxs-lookup"><span data-stu-id="207de-131">Fulfilled</span></span>
- <span data-ttu-id="207de-132">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="207de-132">Invoiced</span></span>
- <span data-ttu-id="207de-133">Cancelled</span><span class="sxs-lookup"><span data-stu-id="207de-133">Cancelled</span></span>

<span data-ttu-id="207de-134">Loetelu **Töötlemise olek** võeti kasutusele, et olekut saaks rakendusega Supply Chain Management täpsemini vastendada.</span><span class="sxs-lookup"><span data-stu-id="207de-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="207de-135">Järgmises tabelis on toodud suvandi **Töötlemise olek** vastendus rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="207de-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="207de-136">Töötlemise olek</span><span class="sxs-lookup"><span data-stu-id="207de-136">Processing Status</span></span>   | <span data-ttu-id="207de-137">Olek rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="207de-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="207de-138">Dokumendi olek rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="207de-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="207de-139">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="207de-139">Active</span></span>              | <span data-ttu-id="207de-140">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-140">Open Order</span></span>                        | <span data-ttu-id="207de-141">None</span><span class="sxs-lookup"><span data-stu-id="207de-141">None</span></span>                                       |
| <span data-ttu-id="207de-142">Kinnitatud</span><span class="sxs-lookup"><span data-stu-id="207de-142">Confirmed</span></span>           | <span data-ttu-id="207de-143">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-143">Open Order</span></span>                        | <span data-ttu-id="207de-144">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="207de-144">Confirmation</span></span>                               |
| <span data-ttu-id="207de-145">Valitud</span><span class="sxs-lookup"><span data-stu-id="207de-145">Picked</span></span>              | <span data-ttu-id="207de-146">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-146">Open Order</span></span>                        | <span data-ttu-id="207de-147">Komplekteerimisleht</span><span class="sxs-lookup"><span data-stu-id="207de-147">Picking List</span></span>                               |
| <span data-ttu-id="207de-148">Osaliselt tarnitud</span><span class="sxs-lookup"><span data-stu-id="207de-148">Partially Delivered</span></span> | <span data-ttu-id="207de-149">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-149">Open Order</span></span>                        | <span data-ttu-id="207de-150">Saateleht</span><span class="sxs-lookup"><span data-stu-id="207de-150">Packing Slip</span></span>                               |
| <span data-ttu-id="207de-151">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="207de-151">Delivered</span></span>           | <span data-ttu-id="207de-152">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="207de-152">Delivered</span></span>                         | <span data-ttu-id="207de-153">Saateleht</span><span class="sxs-lookup"><span data-stu-id="207de-153">Packing Slip</span></span>                               |
| <span data-ttu-id="207de-154">Osaliselt arvele kantud</span><span class="sxs-lookup"><span data-stu-id="207de-154">Partially Invoiced</span></span>  | <span data-ttu-id="207de-155">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="207de-155">Delivered</span></span>                         | <span data-ttu-id="207de-156">Arve</span><span class="sxs-lookup"><span data-stu-id="207de-156">Invoice</span></span>                                    |
| <span data-ttu-id="207de-157">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="207de-157">Invoiced</span></span>            | <span data-ttu-id="207de-158">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="207de-158">Invoiced</span></span>                          | <span data-ttu-id="207de-159">Arve</span><span class="sxs-lookup"><span data-stu-id="207de-159">Invoice</span></span>                                    |
| <span data-ttu-id="207de-160">Cancelled</span><span class="sxs-lookup"><span data-stu-id="207de-160">Cancelled</span></span>           | <span data-ttu-id="207de-161">Cancelled</span><span class="sxs-lookup"><span data-stu-id="207de-161">Cancelled</span></span>                         | <span data-ttu-id="207de-162">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="207de-162">Not applicable</span></span>                             |

<span data-ttu-id="207de-163">Järgmises tabelis on toodud suvandi **Töötlemise olek** vastendus rakendustes Sales ja Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="207de-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="207de-164">Töötlemise olek</span><span class="sxs-lookup"><span data-stu-id="207de-164">Processing Status</span></span>   | <span data-ttu-id="207de-165">Olek rakenduses Sales</span><span class="sxs-lookup"><span data-stu-id="207de-165">Status in Sales</span></span> | <span data-ttu-id="207de-166">Olek rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="207de-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="207de-167">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="207de-167">Active</span></span>              | <span data-ttu-id="207de-168">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="207de-168">Active</span></span>          | <span data-ttu-id="207de-169">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-169">Open Order</span></span>                        |
| <span data-ttu-id="207de-170">Kinnitatud</span><span class="sxs-lookup"><span data-stu-id="207de-170">Confirmed</span></span>           | <span data-ttu-id="207de-171">Edastatud</span><span class="sxs-lookup"><span data-stu-id="207de-171">Submitted</span></span>       | <span data-ttu-id="207de-172">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-172">Open Order</span></span>                        |
| <span data-ttu-id="207de-173">Valitud</span><span class="sxs-lookup"><span data-stu-id="207de-173">Picked</span></span>              | <span data-ttu-id="207de-174">Edastatud</span><span class="sxs-lookup"><span data-stu-id="207de-174">Submitted</span></span>       | <span data-ttu-id="207de-175">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-175">Open Order</span></span>                        |
| <span data-ttu-id="207de-176">Osaliselt tarnitud</span><span class="sxs-lookup"><span data-stu-id="207de-176">Partially Delivered</span></span> | <span data-ttu-id="207de-177">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="207de-177">Active</span></span>          | <span data-ttu-id="207de-178">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-178">Open Order</span></span>                        |
| <span data-ttu-id="207de-179">Osaliselt arvele kantud</span><span class="sxs-lookup"><span data-stu-id="207de-179">Partially Invoiced</span></span>  | <span data-ttu-id="207de-180">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="207de-180">Active</span></span>          | <span data-ttu-id="207de-181">Avatud tellimus</span><span class="sxs-lookup"><span data-stu-id="207de-181">Open Order</span></span>                        |
| <span data-ttu-id="207de-182">Osaliselt arvele kantud</span><span class="sxs-lookup"><span data-stu-id="207de-182">Partially Invoiced</span></span>  | <span data-ttu-id="207de-183">Täidetud</span><span class="sxs-lookup"><span data-stu-id="207de-183">Fulfilled</span></span>       | <span data-ttu-id="207de-184">Tarnitud</span><span class="sxs-lookup"><span data-stu-id="207de-184">Delivered</span></span>                         |
| <span data-ttu-id="207de-185">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="207de-185">Invoiced</span></span>            | <span data-ttu-id="207de-186">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="207de-186">Invoiced</span></span>        | <span data-ttu-id="207de-187">Arveldatud</span><span class="sxs-lookup"><span data-stu-id="207de-187">Invoiced</span></span>                          |
| <span data-ttu-id="207de-188">Cancelled</span><span class="sxs-lookup"><span data-stu-id="207de-188">Cancelled</span></span>           | <span data-ttu-id="207de-189">Cancelled</span><span class="sxs-lookup"><span data-stu-id="207de-189">Cancelled</span></span>       | <span data-ttu-id="207de-190">Cancelled</span><span class="sxs-lookup"><span data-stu-id="207de-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="207de-191">Seadistus</span><span class="sxs-lookup"><span data-stu-id="207de-191">Setup</span></span>

<span data-ttu-id="207de-192">Müügitellimuse olekuveergude vastendamise seadistamiseks peate lubama atribuudid **IsSOPIntegrationEnabled** ja **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="207de-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="207de-193">Atribuudi **IsSOPIntegrationEnabled** lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="207de-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="207de-194">Avage brauseris leht `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="207de-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="207de-195">Asendage **\<test-name\>** oma ettevõtte rakenduse Sales lingiga.</span><span class="sxs-lookup"><span data-stu-id="207de-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="207de-196">Otsige avatud lehel üles **organizationid** ja kirjutage selle väärtus üles.</span><span class="sxs-lookup"><span data-stu-id="207de-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Väärtuse organizationid leidmine](media/sales-map-orgid.png)

3. <span data-ttu-id="207de-198">Avage rakenduses Sales brauserikonsool ja käivitage järgmine skript.</span><span class="sxs-lookup"><span data-stu-id="207de-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="207de-199">Kasutage sammust 2 pärit üksuse **organizationid** väärtust.</span><span class="sxs-lookup"><span data-stu-id="207de-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScripti kood brauserikonsoolis](media/sales-map-script.png)

4. <span data-ttu-id="207de-201">Veenduge, et suvandi **IsSOPIntegrationEnabled** väärtuseks oleks seatud **tõene**.</span><span class="sxs-lookup"><span data-stu-id="207de-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="207de-202">Kasutage väärtuse kontrollimiseks sammust 1 pärit URL-i.</span><span class="sxs-lookup"><span data-stu-id="207de-202">Use the URL from step 1 to check the value.</span></span>

    ![Tõeseks seatud IsSOPIntegrationEnabled](media/sales-map-integration-enabled.png)

<span data-ttu-id="207de-204">Atribuudi **isIntegrationUser** lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="207de-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="207de-205">Valige rakenduses Sales **Sätted \> Kohandamine \> Kohanda süsteemi**, valige **Kasutaja tabel** ja seejärel avage **Vorm \> Kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="207de-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Kasutaja vormi avamine](media/sales-map-user.png)

2. <span data-ttu-id="207de-207">Leidke väljauurijas üles **Integratsiooni kasutaja režiim** ja topeltklõpsake sellel, et lisada see vormile.</span><span class="sxs-lookup"><span data-stu-id="207de-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="207de-208">Salvestage muudatus.</span><span class="sxs-lookup"><span data-stu-id="207de-208">Save your change.</span></span>

    ![Integratsiooni kasutaja režiimi veeru lisamine vormile](media/sales-map-field-explorer.png)

3. <span data-ttu-id="207de-210">Valige rakenduses Sales **Sätted \> Turve \> Kasutajad** ja muutke vaade väärtuselt **Lubatud kasutajad** väärtusele **Rakenduse kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="207de-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Vaate muutmine lubatud kasutajatelt rakenduse kasutajatele](media/sales-map-enabled-users.png)

4. <span data-ttu-id="207de-212">Valige kaks kirjet nimega **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="207de-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Rakenduse kasutajate loend](media/sales-map-user-mode.png)

5. <span data-ttu-id="207de-214">Muutke veeru **Integratsiooni kasutaja režiim** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="207de-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Integratsiooni kasutaja režiimi veeru väärtuse muutmine](media/sales-map-user-mode-yes.png)

<span data-ttu-id="207de-216">Teie müügitellimused on nüüd vastendatud.</span><span class="sxs-lookup"><span data-stu-id="207de-216">Your sales orders are now mapped.</span></span>
