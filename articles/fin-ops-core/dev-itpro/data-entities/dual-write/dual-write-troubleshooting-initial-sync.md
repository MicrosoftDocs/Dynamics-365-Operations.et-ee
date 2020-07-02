---
title: Probleemide tõrkeotsing esmase sünkroonimise ajal
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: e4ee3bf07a1df445875197f38f655464cc9b44d3
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443845"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="cb248-103">Probleemide tõrkeotsing esmase sünkroonimise ajal</span><span class="sxs-lookup"><span data-stu-id="cb248-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb248-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="cb248-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="cb248-105">Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.</span><span class="sxs-lookup"><span data-stu-id="cb248-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb248-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="cb248-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="cb248-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="cb248-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="cb248-108">Esmase sünkroonomise tõrgete kontrollimine Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="cb248-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="cb248-109">Pärast vastendamise mallide lubamist peaks vastenduse olekuks olema **Töötab**.</span><span class="sxs-lookup"><span data-stu-id="cb248-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="cb248-110">Kui olek on **Ei tööta**, ilmnes tõrkeid esmasel sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="cb248-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="cb248-111">Tõrgete kuvamiseks valige lehel **Topeltkirjutus** vahekaart **Esmase sünkroonimise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="cb248-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Esmase sünkroonimise üksikasjade vahekaardi tõrge](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="cb248-113">Esmast sünkroonimist ei saa lõpule viia: 400 vigane päring</span><span class="sxs-lookup"><span data-stu-id="cb248-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="cb248-114">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="cb248-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="cb248-115">Kui proovite käivitada vastendust ja esmast sünkroonimist, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="cb248-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="cb248-116">*(\[Vigane päring\], kaugserver tagastas tõrke: (400) vigane päring.), AX eksportimisel ilmnes tõrge*</span><span class="sxs-lookup"><span data-stu-id="cb248-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="cb248-117">Siin on tabeli täieliku tõrketeate näide.</span><span class="sxs-lookup"><span data-stu-id="cb248-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="cb248-118">Kui see tõrge ilmneb järjepidevalt ja te ei saa esmast sünkroonimist lõpule viia, toimige probleemi lahendamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cb248-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="cb248-119">Logige rakenduse Finance and Operations virtuaalarvutisse (VM) sisse.</span><span class="sxs-lookup"><span data-stu-id="cb248-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="cb248-120">Avage Microsofti halduskonsool.</span><span class="sxs-lookup"><span data-stu-id="cb248-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="cb248-121">Paanil **Teenused** veenduge, et Microsoft Dynamics 365 andmete importimise/eksportimise raamistiku teenus töötab.</span><span class="sxs-lookup"><span data-stu-id="cb248-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="cb248-122">Taaskäivitage see, kui see on peatatud, kuna esmane sünkroonimine nõuab seda.</span><span class="sxs-lookup"><span data-stu-id="cb248-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="cb248-123">Esmase sünkroonimise tõrge: 403 keelatud</span><span class="sxs-lookup"><span data-stu-id="cb248-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="cb248-124">Teile võidakse kuvada esmase sünkroonimise ajal järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="cb248-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="cb248-125">*(\[Keelatud\], kaugserver tagastas tõrke: (403) keelatud.), AX eksportimisel ilmnes tõrge*</span><span class="sxs-lookup"><span data-stu-id="cb248-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="cb248-126">Probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="cb248-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="cb248-127">Logige rakendusse Finance and Operations sisse.</span><span class="sxs-lookup"><span data-stu-id="cb248-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="cb248-128">Kustutage lehel **Azure Active Directory rakendused** klient **DtAppID** ja seejärel lisage see uuesti.</span><span class="sxs-lookup"><span data-stu-id="cb248-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID klient Azure AD rakenduste loendis](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="cb248-130">Eneseviite või ringviite tõrked esmase sünkroonimise ajal</span><span class="sxs-lookup"><span data-stu-id="cb248-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="cb248-131">Teile võidakse kuvada tõrketeade, kui mõnel teie vastendustest on eneseviited või ringviited.</span><span class="sxs-lookup"><span data-stu-id="cb248-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="cb248-132">Tõrked jagunevad järgmistesse kategooriatesse.</span><span class="sxs-lookup"><span data-stu-id="cb248-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="cb248-133">Tõrked üksuse Hankijad V2 vastendamisel üksusega msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="cb248-133">Errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="cb248-134">Tõrked üksuse Kliendid V3 vastendamisel üksusega Kontod</span><span class="sxs-lookup"><span data-stu-id="cb248-134">Errors in the Customers V3–to–Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="cb248-135">Tõrgete lahendamine üksuse Hankijad V2 vastendamisel üksusega msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="cb248-135">Resolve errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>

<span data-ttu-id="cb248-136">Üksuse **Hankijad V2** vastendamisel üksusega **msdyn\_vendors** võivad ilmneda esmase sünkroonimise tõrked, kui üksustel on olemasolevaid kirjeid, mille väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** sisaldavad väärtusi.</span><span class="sxs-lookup"><span data-stu-id="cb248-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the entities have existing records where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="cb248-137">Tõrked ilmnevad seetõttu, et hankija vastendamisel on **InvoiceVendorAccountNumber** enesele viitav väli ja **PrimaryContactPersonId** ringviitav väli.</span><span class="sxs-lookup"><span data-stu-id="cb248-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="cb248-138">Ilmnenud tõrketeated kuvatakse järgmises vormis.</span><span class="sxs-lookup"><span data-stu-id="cb248-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="cb248-139">*Guidi ei saanud lahendada väljal: \<field\>. Otsingut ei leitud: \<value\>. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="cb248-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="cb248-140">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="cb248-140">Here are some examples:</span></span>

- <span data-ttu-id="cb248-141">*Guidi ei saanud lahendada väljal: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Otsingut ei leitud: 000056. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="cb248-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="cb248-142">*Guidi ei saanud lahendada väljal: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Otsingut ei leitud: V24-1. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="cb248-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="cb248-143">Kui hankija üksuses on kirjeid, mille väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** sisaldavad väärtusi, siis järgige neid samme, et esmane sünkroonimine lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="cb248-143">If any records in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="cb248-144">Kustutage rakenduses Finance and Operations vastendusest väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** ning seejärel salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="cb248-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="cb248-145">Avage **Hankijad V2 (msdyn\_vendors)** topeltkirjutuse vastendamisleht ja seejärel vahekaart **Üksuse vastendused**. Valige vasakpoolses filtris suvand **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="cb248-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Entity mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="cb248-146">Valige parempoolses filtris **Müük.Hankija**.</span><span class="sxs-lookup"><span data-stu-id="cb248-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="cb248-147">Otsige väärtust **primarycontactperson**, et leida allika väli **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="cb248-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="cb248-148">Valige **Tegevused** ja seejärel **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="cb248-148">Select **Actions**, and then select **Delete**.</span></span>

        ![Välja PrimaryContactPersonId kustutamine](media/vend_selfref3.png)

    4. <span data-ttu-id="cb248-150">Välja **InvoiceVendorAccountNumber** kustutamiseks korrake neid samme.</span><span class="sxs-lookup"><span data-stu-id="cb248-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![Välja InvoiceVendorAccountNumber kustutamine](media/vend-selfref4.png)

    5. <span data-ttu-id="cb248-152">Salvestage oma muudatused vastendusse.</span><span class="sxs-lookup"><span data-stu-id="cb248-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="cb248-153">Lülitage üksuse **Hankijad V2** muudatuste jälgimine välja.</span><span class="sxs-lookup"><span data-stu-id="cb248-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="cb248-154">Valige tööruumis **Andmehaldus** paan **Andmeüksused**.</span><span class="sxs-lookup"><span data-stu-id="cb248-154">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="cb248-155">Valige üksus **Hankijad V2**.</span><span class="sxs-lookup"><span data-stu-id="cb248-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="cb248-156">Valige tegumipaanilt **Suvandid** ja seejärel **Muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="cb248-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Muudatuse jälgimise suvandi valimine](media/selfref_options.png)

    4. <span data-ttu-id="cb248-158">Valige **Keela muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="cb248-158">Select **Disable Change Tracking**.</span></span>

        ![Suvandi „Keela muudatuste jälgimine” valimine](media/selfref_tracking.png)

3. <span data-ttu-id="cb248-160">Käivitage üksuse **Hankijad V2 (msdyn\_vendors)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="cb248-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="cb248-161">Esmane sünkroonimine peaks toimima tõrgeteta.</span><span class="sxs-lookup"><span data-stu-id="cb248-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="cb248-162">Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="cb248-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="cb248-163">Selle vastenduse peate sünkroonima juhul, kui soovite sünkroonida hankijate üksuse põhikontakti välja, kuna ka kontaktikirjed tuleb esmasünkroonida.</span><span class="sxs-lookup"><span data-stu-id="cb248-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact records.</span></span>
5. <span data-ttu-id="cb248-164">Lisage väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** tagasi vastendusse **Hankijad V2 (msdyn\_vendors)** ning seejärel salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="cb248-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="cb248-165">Käivitage uuesti üksuse **Hankijad V2 (msdyn\_vendors)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="cb248-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="cb248-166">Kuna muudatuste jälgimine on välja lülitatud, sünkroonitakse kõik kirjed.</span><span class="sxs-lookup"><span data-stu-id="cb248-166">Because change tracking is turned off, all the records will be synced.</span></span>
7. <span data-ttu-id="cb248-167">Lülitage üksuse **Hankijad V2** muudatuste jälgimine tagasi sisse.</span><span class="sxs-lookup"><span data-stu-id="cb248-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="cb248-168">Tõrgete lahendamine üksuse Kliendid V3 vastendamisel üksusega Kontod</span><span class="sxs-lookup"><span data-stu-id="cb248-168">Resolve errors in the Customers V3–to–Accounts entity mapping</span></span>

<span data-ttu-id="cb248-169">Üksuse **Kliendid V3** vastendamisel üksusega **Kontod** võivad ilmneda esmase sünkroonimise tõrked, kui üksustel on olemasolevaid kirjeid, mille väljad **ContactPersonID** ja **InvoiceAccount** sisaldavad väärtusi.</span><span class="sxs-lookup"><span data-stu-id="cb248-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the entities have existing records where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="cb248-170">Need tõrked ilmnevad seetõttu, et hankija vastendamisel on **InvoiceAccount** enesele viitav väli ja **ContactPersonID** ringviitav väli.</span><span class="sxs-lookup"><span data-stu-id="cb248-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="cb248-171">Ilmnenud tõrketeated kuvatakse järgmises vormis.</span><span class="sxs-lookup"><span data-stu-id="cb248-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="cb248-172">*Guidi ei saanud lahendada väljal: \<field\>. Otsingut ei leitud: \<value\>. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="cb248-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="cb248-173">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="cb248-173">Here are some examples:</span></span>

- <span data-ttu-id="cb248-174">*Guidi ei saanud lahendada väljal: primarycontactid.msdyn\_contactpersonid. Otsingut ei leitud: 000056. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="cb248-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="cb248-175">*Guidi ei saanud lahendada väljal: msdyn\_billingaccount.accountnumber. Otsingut ei leitud: 1206-1. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="cb248-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="cb248-176">Kui kliendi üksuses on kirjeid, mille väljad **ContactPersonID** ja **InvoiceAccount** sisaldavad väärtusi, siis järgige neid samme, et esmane sünkroonimine lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="cb248-176">If any records in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="cb248-177">Seda meetodit saate kasutada kõikide valmiskujul üksuste puhul, nagu näiteks **Kontod** ja **Kontaktid**.</span><span class="sxs-lookup"><span data-stu-id="cb248-177">You can use this approach for any out-of-box entities, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="cb248-178">Kustutage rakenduses Finance and Operations vastendusest **Kliendid V3 (kontod)** väljad **ContactPersonID** ja **InvoiceAccount** ning seejärel salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="cb248-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="cb248-179">Avage **Kliendid V3 (kontod)** topeltkirjutuse vastendamisleht ja seejärel vahekaart **Üksuse vastendused**. Valige vasakpoolses filtris suvand **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="cb248-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Entity mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="cb248-180">Valige parempoolses filtris **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="cb248-180">In the right filter, select **Common Data Service.Account**.</span></span>
    2. <span data-ttu-id="cb248-181">Otsige väärtust **contactperson**, et leida allika väli **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="cb248-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="cb248-182">Valige **Tegevused** ja seejärel **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="cb248-182">Select **Actions**, and then select **Delete**.</span></span>

        ![Välja ContactPersonID kustutamine](media/cust_selfref3.png)

    4. <span data-ttu-id="cb248-184">Välja **InvoiceAccount** kustutamiseks korrake neid samme.</span><span class="sxs-lookup"><span data-stu-id="cb248-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![Välja InvoiceAccount kustutamine](media/cust_selfref4.png)

    5. <span data-ttu-id="cb248-186">Salvestage oma muudatused vastendusse.</span><span class="sxs-lookup"><span data-stu-id="cb248-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="cb248-187">Lülitage üksuse **Kliendid V3** muudatuste jälgimine välja.</span><span class="sxs-lookup"><span data-stu-id="cb248-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="cb248-188">Valige tööruumis **Andmehaldus** paan **Andmeüksused**.</span><span class="sxs-lookup"><span data-stu-id="cb248-188">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="cb248-189">Valige üksus **Kliendid V3**.</span><span class="sxs-lookup"><span data-stu-id="cb248-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="cb248-190">Valige tegumipaanilt **Suvandid** ja seejärel **Muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="cb248-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Muudatuse jälgimise suvandi valimine](media/selfref_options.png)

    4. <span data-ttu-id="cb248-192">Valige **Keela muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="cb248-192">Select **Disable Change Tracking**.</span></span>

        ![Suvandi „Keela muudatuste jälgimine” valimine](media/selfref_tracking.png)

3. <span data-ttu-id="cb248-194">Käivitage üksuse **Kliendid V3 (kontod)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="cb248-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="cb248-195">Esmane sünkroonimine peaks toimima tõrgeteta.</span><span class="sxs-lookup"><span data-stu-id="cb248-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="cb248-196">Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="cb248-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb248-197">Sama nimega vastendusi on kaks.</span><span class="sxs-lookup"><span data-stu-id="cb248-197">There are two maps that have the same name.</span></span> <span data-ttu-id="cb248-198">Valige vastendus, millel on vahekaardil **Üksikasjad** järgmine kirjeldus: **Topeltkirjutamise mall üksuse FO.CDS Hankija Kontaktid V2 sünkroonimiseks üksusega CDS.Kontaktid. Vajab uut paketti \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="cb248-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="cb248-199">Lisage väljad **InvoiceAccount** ja **ContactPersonId** tagasi vastendusse **Kliendid V3 (Kontod)** ning seejärel salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="cb248-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="cb248-200">Nüüd on nii väli **InvoiceAccount** kui ka väli **ContactPersonId** taas osa reaalajas sünkroonimise režiimist.</span><span class="sxs-lookup"><span data-stu-id="cb248-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="cb248-201">Järgmise sammu käigus esmasünkroonite need väljad.</span><span class="sxs-lookup"><span data-stu-id="cb248-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="cb248-202">Käivitage uuesti üksuse **Kliendid V3 (kontod)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="cb248-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="cb248-203">Kuna muudatuste jälgimine on välja lülitatud, siis sünkroonitakse väljade **InvoiceAccount** ja **ContactPersonId** andmed rakendusest Finance and Operations rakendusega Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cb248-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Common Data Service.</span></span>
7. <span data-ttu-id="cb248-204">Väljade **InvoiceAccount** ja **ContactPersonId** andmete sünkroonimiseks rakendusest Common Data Service rakendusega Finance and Operations peate kasutama andmeintegratsiooni projekti.</span><span class="sxs-lookup"><span data-stu-id="cb248-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="cb248-205">Looge rakenduses Power Apps üksuste **Sales.Account** ja **Finance and Operations apps.Customers V3** vahel andmete integreerimise projekt.</span><span class="sxs-lookup"><span data-stu-id="cb248-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="cb248-206">Andmete suund peab olema rakendusest Common Data Service rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cb248-206">The data direction must be from Common Data Service to the Finance and Operations app.</span></span> <span data-ttu-id="cb248-207">Kuna **InvoiceAccount** on topeltkirjutuses uus atribuut, siis võite selle atribuudi esmase sünkroonimise vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="cb248-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="cb248-208">Lisateavet vt teemast [Andmete integreerimine teenusesse Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="cb248-208">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="cb248-209">Järgmisel illustratsioonil on toodud projekt, mis värskendab väljasid **CustomerAccount** ja **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="cb248-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Andmeintegratsiooni projekt väljade CustomerAccount ja ContactPersonId värskendamiseks](media/cust_selfref6.png)

    2. <span data-ttu-id="cb248-211">Lisage teenuse Common Data Service poolel filtrite all ettevõtte kriteeriumid, et rakenduses Finance and Operations värskendataks vaid filtri kriteeriumidele vastavaid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="cb248-211">Add the company criteria in the filter on the Common Data Service side, so that only records that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="cb248-212">Filtri lisamiseks valige filtri nupp.</span><span class="sxs-lookup"><span data-stu-id="cb248-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="cb248-213">Seejärel saate dialoogiboksis **Päringu redigeerimine** lisada filtri päringu, nagu näiteks **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="cb248-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="cb248-214">[MÄRKUS] Kui filtri nuppu ei kuvata, siis saate luua tugiteenusepileti, et paluda andmeintegratsiooni meeskonnal lubada teie rentnikus filtri võimalus.</span><span class="sxs-lookup"><span data-stu-id="cb248-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="cb248-215">Kui te ei sisesta **\_msdyn\_company\_value** jaoks filtri päringut, siis sünkroonitakse kõik kirjed.</span><span class="sxs-lookup"><span data-stu-id="cb248-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the records will be synced.</span></span>

        ![Filtri päringu lisamine](media/cust_selfref7.png)

    <span data-ttu-id="cb248-217">Kirjete esmane sünkroonimine on nüüd lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="cb248-217">The initial synchronization of the records is now completed.</span></span>

8. <span data-ttu-id="cb248-218">Lülitage rakenduses Finance and Operations üksuse **Kliendid V3** muudatuste jälgimine tagasi sisse.</span><span class="sxs-lookup"><span data-stu-id="cb248-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
