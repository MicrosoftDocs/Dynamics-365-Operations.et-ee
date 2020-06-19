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
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410077"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="ca531-103">Probleemide tõrkeotsing esmase sünkroonimise ajal</span><span class="sxs-lookup"><span data-stu-id="ca531-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca531-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="ca531-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="ca531-105">Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.</span><span class="sxs-lookup"><span data-stu-id="ca531-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca531-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="ca531-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="ca531-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="ca531-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="ca531-108">Esmase sünkroonomise tõrgete kontrollimine Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="ca531-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="ca531-109">Pärast vastendamise mallide lubamist peaks vastenduse olekuks olema **Töötab**.</span><span class="sxs-lookup"><span data-stu-id="ca531-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="ca531-110">Kui olek on **Ei tööta**, ilmnes tõrkeid esmasel sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="ca531-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="ca531-111">Tõrgete kuvamiseks valige lehel **Topeltkirjutus** vahekaart **Esmase sünkroonimise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ca531-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Esmase sünkroonimise üksikasjade vahekaart](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="ca531-113">Esmast sünkroonimist ei saa lõpule viia: 400 vigane päring</span><span class="sxs-lookup"><span data-stu-id="ca531-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="ca531-114">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="ca531-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="ca531-115">Kui proovite käivitada vastendust ja esmast sünkroonimist, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="ca531-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="ca531-116">*Kaugserver tagastas tõrke: (400) vigane päring.), AXeksportimisel ilmnes tõrge*</span><span class="sxs-lookup"><span data-stu-id="ca531-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="ca531-117">Siin on tabeli täieliku tõrketeate näide.</span><span class="sxs-lookup"><span data-stu-id="ca531-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="ca531-118">Kui see tõrge ilmneb järjepidevalt ja te ei saa esmast sünkroonimist lõpule viia, toimige probleemi lahendamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ca531-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="ca531-119">Logige rakenduse Finance and Operations virtuaalarvutisse (VM) sisse.</span><span class="sxs-lookup"><span data-stu-id="ca531-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="ca531-120">Avage Microsofti halduskonsool.</span><span class="sxs-lookup"><span data-stu-id="ca531-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="ca531-121">Paanil **Teenused** veenduge, et Microsoft Dynamics 365 andmete importimise/eksportimise raamistiku teenus töötab.</span><span class="sxs-lookup"><span data-stu-id="ca531-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="ca531-122">Taaskäivitage see, kui see on peatatud, kuna esmane sünkroonimine nõuab seda.</span><span class="sxs-lookup"><span data-stu-id="ca531-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="ca531-123">Esmase sünkroonimise tõrge: 403 keelatud</span><span class="sxs-lookup"><span data-stu-id="ca531-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="ca531-124">Teile võidakse kuvada esmase sünkroonimise ajal järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="ca531-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="ca531-125">*(\[Keelatud\], kaugserver tagastas tõrke: (403) keelatud.), AX eksportimisel ilmnes tõrge*</span><span class="sxs-lookup"><span data-stu-id="ca531-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="ca531-126">Probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="ca531-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="ca531-127">Logige rakendusse Finance and Operations sisse.</span><span class="sxs-lookup"><span data-stu-id="ca531-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="ca531-128">Kustutage lehel **Azure Active Directory rakendused** klient **DtAppID** ja seejärel lisage see uuesti.</span><span class="sxs-lookup"><span data-stu-id="ca531-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD rakenduste loend](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="ca531-130">Eneseviite või ringviite tõrked esmase sünkroonimise ajal</span><span class="sxs-lookup"><span data-stu-id="ca531-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="ca531-131">Teile võidakse kuvada tõrketeade, kui mõnel teie vastendustest on eneseviited või ringviited.</span><span class="sxs-lookup"><span data-stu-id="ca531-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="ca531-132">Tõrked jagunevad järgmistesse kategooriatesse.</span><span class="sxs-lookup"><span data-stu-id="ca531-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="ca531-133">Üksuse Hankijad V2 vastendamine üksusega msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="ca531-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="ca531-134">Üksuse Kliendid V3 vastendamine üksusega Kontod</span><span class="sxs-lookup"><span data-stu-id="ca531-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="ca531-135">Tõrgete lahendamine üksuse Hankijad V2 vastendamisel üksusega msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="ca531-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="ca531-136">Üksuse **Hankijad V2** vastendamisel üksusega **msdyn_vendors** võivad tekkida järgmised esmase sünkroonimise tõrked, kui üksustel on olemas väärtustatud kirjed väljadel **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="ca531-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="ca531-137">See juhtub seetõttu, et hankija vastendamisel on **InvoiceVendorAccountNumber** enesele viitav väli ja **PrimaryContactPersonId** ringviitav väli.</span><span class="sxs-lookup"><span data-stu-id="ca531-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="ca531-138">*Guidi ei saanud lahendada väljal: <field>. Otsingut ei leitud: <value>. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="ca531-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="ca531-139">Järgnevalt on esitatud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="ca531-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="ca531-140">*Guidi ei saanud lahendada väljal: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Otsingut ei leitud: 000056. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="ca531-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="ca531-141">*Guidi ei saanud lahendada väljal: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Otsingut ei leitud: V24-1. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="ca531-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="ca531-142">Kui teil on hankija üksuses nendel väljadel väärtusi sisaldavaid kirjeid, siis järgige alltoodud jaotises esitatud etappe, et esmane sünkroonimine edukalt lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="ca531-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="ca531-143">Kustutage rakenduses Finance and Operations vastendamisest väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** ning salvestage muudatused.</span><span class="sxs-lookup"><span data-stu-id="ca531-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="ca531-144">Liikuge **Hankijad V2 (msdyn_vendors)** topeltkirjutuse vastendamislehele ja valige vahekaart **Üksuse vastendused**. Valige vasakpoolses filtris suvand **Finance and Operationsi rakendused. Hankijad V2**.</span><span class="sxs-lookup"><span data-stu-id="ca531-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="ca531-145">Valige parempoolses filtris **Müük.Hankija**.</span><span class="sxs-lookup"><span data-stu-id="ca531-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="ca531-146">Otsige väärtust **primarycontactperson**, et leida allika väli **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="ca531-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="ca531-147">Klõpsake nuppu **Toimingud** ja valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="ca531-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![enese- või ringviide 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="ca531-149">Välja **InvoiceVendorAccountNumber** kustutamiseks korrake toimingut.</span><span class="sxs-lookup"><span data-stu-id="ca531-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![enese- või ringviide 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="ca531-151">Salvestage vastendamise muudatused.</span><span class="sxs-lookup"><span data-stu-id="ca531-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="ca531-152">Keelake üksuse **Hankijad V2** muudatuste jälgimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="ca531-153">Avage **Andmehaldus \> Andmeüksused**.</span><span class="sxs-lookup"><span data-stu-id="ca531-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="ca531-154">Valige üksus **Hankijad V2**.</span><span class="sxs-lookup"><span data-stu-id="ca531-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="ca531-155">Klõpsake menüüribal **Suvandid** ja seejärel **Muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="ca531-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![enese- või ringviide 5](media/selfref_options.png)
    
    4. <span data-ttu-id="ca531-157">Klõpsake suvandil **Keela muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="ca531-157">Click **Disable Change Tracking**.</span></span>
    
        ![enese- või ringviide 6](media/selfref_tracking.png)

3. <span data-ttu-id="ca531-159">Käivitage üksuse **Hankijad V2 (msdyn_vendors)** vastendamise esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="ca531-160">Esmane sünkroonimine peaks toimima tõrgeteta.</span><span class="sxs-lookup"><span data-stu-id="ca531-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="ca531-161">Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastendamise esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="ca531-162">Selle vastenduse peate sünkroonima juhul, kui soovite sünkroonida hankijate üksuse põhikontakti välja, kuna ka kontaktide kirjed tuleb esmasünkroonida.</span><span class="sxs-lookup"><span data-stu-id="ca531-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="ca531-163">Lisage vastendusele **Hankijad V2 (msdyn_vendors)** tagasi väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** ning salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="ca531-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="ca531-164">Käivitage uuesti üksuse **Hankijad V2 (msdyn_vendors)** vastendamise esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="ca531-165">Kõik kirjed sünkroonitakse, kuna muudatuste jälgimine on keelatud.</span><span class="sxs-lookup"><span data-stu-id="ca531-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="ca531-166">Lubage üksuse **Hankijad V2** muudatuste jälgimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="ca531-167">Tõrgete lahendamine üksuse Kliendid V3 vastendamisel üksusega Kontod</span><span class="sxs-lookup"><span data-stu-id="ca531-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="ca531-168">Üksuse **Kliendid V3** vastendamisel üksusega **Kontod** võivad tekkida järgmised esmase sünkroonimise tõrked, kui üksustel on olemas väärtustatud kirjed väljadel **ContactPersonID** ja **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="ca531-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="ca531-169">See juhtub seetõttu, et hankija vastendamisel on **InvoiceAccount** enesele viitav väli ja **ContactPersonID** ringviitav väli.</span><span class="sxs-lookup"><span data-stu-id="ca531-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="ca531-170">*Guidi ei saanud lahendada väljal: <field>. Otsingut ei leitud: <value>. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="ca531-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="ca531-171">*Guidi ei saanud lahendada väljal: primarycontactid.msdyn_contactpersonid. Otsingut ei leitud: 000056. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="ca531-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="ca531-172">*Guidi ei saanud lahendada väljal: msdyn_billingaccount.accountnumber. Otsingut ei leitud: 1206-1. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="ca531-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="ca531-173">Kui teil on kliendi üksuses nendel väljadel väärtusi sisaldavaid kirjeid, siis järgige alltoodud jaotises esitatud etappe, et esmane sünkroonimine edukalt lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="ca531-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="ca531-174">Seda lähenemist saab kasutada kõikide valmiskujul üksuste, nagu näiteks Kontode ja Kontaktide puhul.</span><span class="sxs-lookup"><span data-stu-id="ca531-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="ca531-175">Kustutage rakenduses Finance and Operations vastendusest **Kliendid V3 (kontod)** väljad **ContactPersonID** ja **InvoiceAccount** ning salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="ca531-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="ca531-176">Liikuge **Kliendid V3 (kontod)** topeltkirjutuse vastendamislehele ja valige vahekaart **Üksuse vastendused**. Valige vasakpoolses filtris suvand **Finance and Operationsi rakendus. Kliendid V3**.</span><span class="sxs-lookup"><span data-stu-id="ca531-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="ca531-177">Valige parempoolses filtris **Common Data Service. Konto**.</span><span class="sxs-lookup"><span data-stu-id="ca531-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="ca531-178">Otsige väärtust **contactperson**, et leida allika väli **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="ca531-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="ca531-179">Klõpsake nuppu **Toimingud** ja valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="ca531-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![enese- või ringviide 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="ca531-181">Välja **InvoiceAccount** kustutamiseks korrake toimingut.</span><span class="sxs-lookup"><span data-stu-id="ca531-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![enese- või ringviide](media/cust_selfref4.png)
    
    5. <span data-ttu-id="ca531-183">Salvestage vastendamise muudatused.</span><span class="sxs-lookup"><span data-stu-id="ca531-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="ca531-184">Keelake üksuse **Kliendid V3** muudatuste jälgimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="ca531-185">Avage **Andmehaldus \> Andmeüksused**.</span><span class="sxs-lookup"><span data-stu-id="ca531-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="ca531-186">Valige üksus **Kliendid V3**.</span><span class="sxs-lookup"><span data-stu-id="ca531-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="ca531-187">Klõpsake menüüribal **Suvandid** ja seejärel **Muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="ca531-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![enese- või ringviide 5](media/selfref_options.png)
    
    4. <span data-ttu-id="ca531-189">Klõpsake suvandil **Keela muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="ca531-189">Click **Disable Change Tracking**.</span></span>
    
        ![enese- või ringviide 6](media/selfref_tracking.png)

3. <span data-ttu-id="ca531-191">Käivitage üksuse **Kliendid V3 (kontod)** vastendamise esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="ca531-192">Esmane sünkroonimine peaks toimima tõrgeteta.</span><span class="sxs-lookup"><span data-stu-id="ca531-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="ca531-193">Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastendamise esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="ca531-194">Seal on kaks sama nimega vastendust.</span><span class="sxs-lookup"><span data-stu-id="ca531-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="ca531-195">Valige järgmise kirjeldusega vastendus: **Topeltkirjutamise mall FO.CDS Hankija Kontaktid V2 üksusega CDS.Kontaktid sünkroonimiseks. Vajab uut paketti \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="ca531-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="ca531-196">vastenduse vahekaardil **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ca531-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="ca531-197">Lisage väljad **InvoiceAccount** ja **ContactPersonId** tagasi vastendusele **Kliendid V3 (Kontod)** ning salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="ca531-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="ca531-198">Nüüd on nii väli **InvoiceAccount** kui ka väli **ContactPersonId** taas osa reaalajas sünkroonimise režiimist.</span><span class="sxs-lookup"><span data-stu-id="ca531-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="ca531-199">Järgmises etapi käigus viite väljade esmase sünkroonimise lõpule.</span><span class="sxs-lookup"><span data-stu-id="ca531-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="ca531-200">Käivitage uuesti üksuse **Kliendid V3 (kontod)** vastendamise esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="ca531-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="ca531-201">Kuna muudatuste jälgimine on keelatud, siis sünkroonitakse sünkroonimise käivitamisel väljade **InvoiceAccount** ja **ContactPersonId** andmed rakendusest Finance and Operations rakendusega Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ca531-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="ca531-202">Väljade **InvoiceAccount** ja **ContactPersonId** andmete sünkroonimiseks rakendusest Common Data Service rakendusega Finance and Operations saate kasutada andmete integreerimise projekti.</span><span class="sxs-lookup"><span data-stu-id="ca531-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="ca531-203">Looge rakenduses Power Apps üksuste **Müük. Konto** ja **Finance and Operationsi rakendused. Kliendid V3** vahel andmete integreerimise projekt.</span><span class="sxs-lookup"><span data-stu-id="ca531-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="ca531-204">Andmete suund peab olema rakendusest Common Data Service rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca531-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="ca531-205">Kuna **InvoiceAccount** on topeltkirjutuses uus atribuut, siis võiksite selle atribuudi esmase sünkroonimise vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="ca531-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="ca531-206">Lisateavet vt teemast [Andmete integreerimine teenusesse Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="ca531-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="ca531-207">Järgmisel pildil on toodud projekt, mis värskendab väljasid **CustomerAccount** ja **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="ca531-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![enese- või ringviide](media/cust_selfref6.png)

    2. <span data-ttu-id="ca531-209">Lisage teenuse Common Data Service poolel filtrite all ettevõtte kriteeriumid, kuna rakenduses Finance and Operations värskendatakse vaid filtri kriteeriumidele vastavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="ca531-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="ca531-210">Filtri lisamiseks klõpsake filtri ikoonil.</span><span class="sxs-lookup"><span data-stu-id="ca531-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="ca531-211">Dialoogis **Päringu redigeerimine** saate lisada filtri päringu, nagu näiteks **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="ca531-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="ca531-212">Kui filtri ikooni ei paista, siis saate luua tugiteenuse pileti, et paluda andmete integreerimise meeskonnal lubada teie rentnikus filtri võimalus.</span><span class="sxs-lookup"><span data-stu-id="ca531-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="ca531-213">Kui te ei sisesta **_msdyn_company_value** jaoks filtri päringut, siis sünkroonitakse kõik kirjed.</span><span class="sxs-lookup"><span data-stu-id="ca531-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![enese- või ringviide](media/cust_selfref7.png)

        <span data-ttu-id="ca531-215">See viib kirjete esialgse sünkroonimise lõpule.</span><span class="sxs-lookup"><span data-stu-id="ca531-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="ca531-216">Finance and Operationsi rakenduses üksuse **Kliendid V3** muudatuste jälgimise lubamine.</span><span class="sxs-lookup"><span data-stu-id="ca531-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

