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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a7ba4fa4771324b4bcb8464649bd8ce8f32024c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683551"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="0d8e3-103">Probleemide tõrkeotsing esmase sünkroonimise ajal</span><span class="sxs-lookup"><span data-stu-id="0d8e3-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0d8e3-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="0d8e3-105">Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d8e3-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0d8e3-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="0d8e3-108">Esmase sünkroonomise tõrgete kontrollimine Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="0d8e3-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="0d8e3-109">Pärast vastendamise mallide lubamist peaks vastenduse olekuks olema **Töötab**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="0d8e3-110">Kui olek on **Ei tööta**, ilmnes tõrkeid esmasel sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="0d8e3-111">Tõrgete kuvamiseks valige lehel **Topeltkirjutus** vahekaart **Esmase sünkroonimise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Esmase sünkroonimise üksikasjade vahekaardi tõrge](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="0d8e3-113">Esmast sünkroonimist ei saa lõpule viia: 400 vigane päring</span><span class="sxs-lookup"><span data-stu-id="0d8e3-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="0d8e3-114">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="0d8e3-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="0d8e3-115">Kui proovite käivitada vastendust ja esmast sünkroonimist, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="0d8e3-116">*(\[Vigane päring\], kaugserver tagastas tõrke: (400) vigane päring.), AX eksportimisel ilmnes tõrge*</span><span class="sxs-lookup"><span data-stu-id="0d8e3-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="0d8e3-117">Siin on tabeli täieliku tõrketeate näide.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="0d8e3-118">Kui see tõrge ilmneb järjepidevalt ja te ei saa esmast sünkroonimist lõpule viia, toimige probleemi lahendamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="0d8e3-119">Logige rakenduse Finance and Operations virtuaalarvutisse (VM) sisse.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="0d8e3-120">Avage Microsofti halduskonsool.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="0d8e3-121">Paanil **Teenused** veenduge, et Microsoft Dynamics 365 andmete importimise/eksportimise raamistiku teenus töötab.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="0d8e3-122">Taaskäivitage see, kui see on peatatud, kuna esmane sünkroonimine nõuab seda.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="0d8e3-123">Esmase sünkroonimise tõrge: 403 keelatud</span><span class="sxs-lookup"><span data-stu-id="0d8e3-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="0d8e3-124">Teile võidakse kuvada esmase sünkroonimise ajal järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="0d8e3-125">*(\[Keelatud\], kaugserver tagastas tõrke: (403) keelatud.), AX eksportimisel ilmnes tõrge*</span><span class="sxs-lookup"><span data-stu-id="0d8e3-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="0d8e3-126">Probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="0d8e3-127">Logige rakendusse Finance and Operations sisse.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="0d8e3-128">Kustutage lehel **Azure Active Directory rakendused** klient **DtAppID** ja seejärel lisage see uuesti.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID klient Azure AD rakenduste loendis](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="0d8e3-130">Eneseviite või ringviite tõrked esmase sünkroonimise ajal</span><span class="sxs-lookup"><span data-stu-id="0d8e3-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="0d8e3-131">Teile võidakse kuvada tõrketeade, kui mõnel teie vastendustest on eneseviited või ringviited.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="0d8e3-132">Tõrked jagunevad järgmistesse kategooriatesse.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="0d8e3-133">Tõrked tabeli Hankijad V2 vastendamisel üksusega msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="0d8e3-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="0d8e3-134">Tõrked tabeli Kliendid V3 vastendamisel üksusega Kontod</span><span class="sxs-lookup"><span data-stu-id="0d8e3-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="0d8e3-135">Tõrgete lahendamine tabeli Hankijad V2 vastendamisel üksusega msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="0d8e3-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="0d8e3-136">Üksuse **Hankijad V2** vastendamisel üksusega **msdyn\_vendors** võivad ilmneda esmase sünkroonimise tõrked, kui tabelitel on olemasolevaid ridu, mille väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** sisaldavad väärtusi.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="0d8e3-137">Tõrked ilmnevad seetõttu, et hankija vastendamisel on **InvoiceVendorAccountNumber** enesele viitav väli ja **PrimaryContactPersonId** ringviitav väli.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="0d8e3-138">Ilmnenud tõrketeated kuvatakse järgmises vormis.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="0d8e3-139">*Guidi ei saanud lahendada väljal: \<field\>. Otsingut ei leitud: \<value\>. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="0d8e3-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="0d8e3-140">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-140">Here are some examples:</span></span>

- <span data-ttu-id="0d8e3-141">*Guidi ei saanud lahendada väljal: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Otsingut ei leitud: 000056. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="0d8e3-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="0d8e3-142">*Guidi ei saanud lahendada väljal: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Otsingut ei leitud: V24-1. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="0d8e3-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="0d8e3-143">Kui hankija üksuses on read, mille väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** sisaldavad väärtusi, siis järgige neid samme, et esmane sünkroonimine lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-143">If any rows in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="0d8e3-144">Kustutage rakenduses Finance and Operations vastendusest väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** ning seejärel salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="0d8e3-145">Avage **Hankijad V2 (msdyn\_vendors)** topeltkirjutuse vastendamisleht ja seejärel vahekaart **Tabeli vastendused**. Valige vasakpoolses filtris suvand **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="0d8e3-146">Valige parempoolses filtris **Müük.Hankija**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="0d8e3-147">Otsige väärtust **primarycontactperson**, et leida allika väli **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="0d8e3-148">Valige **Tegevused** ja seejärel **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-148">Select **Actions**, and then select **Delete**.</span></span>

        ![Välja PrimaryContactPersonId kustutamine](media/vend_selfref3.png)

    4. <span data-ttu-id="0d8e3-150">Välja **InvoiceVendorAccountNumber** kustutamiseks korrake neid samme.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![Välja InvoiceVendorAccountNumber kustutamine](media/vend-selfref4.png)

    5. <span data-ttu-id="0d8e3-152">Salvestage oma muudatused vastendusse.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="0d8e3-153">Lülitage üksuse **Hankijad V2** muudatuste jälgimine välja.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="0d8e3-154">Valige tööruumis **Andmehaldus** paan **Andmetabelid**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="0d8e3-155">Valige üksus **Hankijad V2**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="0d8e3-156">Valige tegumipaanilt **Suvandid** ja seejärel **Muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Muudatuse jälgimise suvandi valimine](media/selfref_options.png)

    4. <span data-ttu-id="0d8e3-158">Valige **Keela muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-158">Select **Disable Change Tracking**.</span></span>

        ![Suvandi „Keela muudatuste jälgimine” valimine](media/selfref_tracking.png)

3. <span data-ttu-id="0d8e3-160">Käivitage üksuse **Hankijad V2 (msdyn\_vendors)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="0d8e3-161">Esmane sünkroonimine peaks toimima tõrgeteta.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="0d8e3-162">Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="0d8e3-163">Selle vastenduse peate sünkroonima juhul, kui soovite sünkroonida hankijate üksuse põhikontakti välja, kuna ka kontaktiread tuleb esmasünkroonida.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="0d8e3-164">Lisage väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** tagasi vastendusse **Hankijad V2 (msdyn\_vendors)** ning seejärel salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="0d8e3-165">Käivitage uuesti üksuse **Hankijad V2 (msdyn\_vendors)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="0d8e3-166">Kuna muudatuste jälgimine on välja lülitatud, sünkroonitakse kõik read.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="0d8e3-167">Lülitage üksuse **Hankijad V2** muudatuste jälgimine tagasi sisse.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="0d8e3-168">Tõrgete lahendamine tabeli Kliendid V3 vastendamisel üksusega Kontod</span><span class="sxs-lookup"><span data-stu-id="0d8e3-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="0d8e3-169">Üksuse **Kliendid V3** vastendamisel üksusega **Kontod** võivad ilmneda esmase sünkroonimise tõrked, kui tabelitel on olemasolevaid ridu, mille väljad **ContactPersonID** ja **InvoiceAccount** sisaldavad väärtusi.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="0d8e3-170">Need tõrked ilmnevad seetõttu, et hankija vastendamisel on **InvoiceAccount** enesele viitav väli ja **ContactPersonID** ringviitav väli.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="0d8e3-171">Ilmnenud tõrketeated kuvatakse järgmises vormis.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="0d8e3-172">*Guidi ei saanud lahendada väljal: \<field\>. Otsingut ei leitud: \<value\>. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="0d8e3-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="0d8e3-173">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-173">Here are some examples:</span></span>

- <span data-ttu-id="0d8e3-174">*Guidi ei saanud lahendada väljal: primarycontactid.msdyn\_contactpersonid. Otsingut ei leitud: 000056. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="0d8e3-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="0d8e3-175">*Guidi ei saanud lahendada väljal: msdyn\_billingaccount.accountnumber. Otsingut ei leitud: 1206-1. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="0d8e3-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="0d8e3-176">Kui kliendi üksuses on read, mille väljad **ContactPersonID** ja **InvoiceAccount** sisaldavad väärtusi, siis järgige neid samme, et esmane sünkroonimine lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-176">If any rows in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="0d8e3-177">Seda meetodit saate kasutada kõikide valmiskujul tabelite puhul, nagu näiteks **Kontod** ja **Kontaktid**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="0d8e3-178">Kustutage rakenduses Finance and Operations vastendusest **Kliendid V3 (kontod)** väljad **ContactPersonID** ja **InvoiceAccount** ning seejärel salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="0d8e3-179">Avage **Kliendid V3 (kontod)** topeltkirjutuse vastendamisleht ja seejärel vahekaart **Tabeli vastendused**. Valige vasakpoolses filtris suvand **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="0d8e3-180">Valige parempoolses filtris **Dataverse.Account**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="0d8e3-181">Otsige väärtust **contactperson**, et leida allika väli **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="0d8e3-182">Valige **Tegevused** ja seejärel **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-182">Select **Actions**, and then select **Delete**.</span></span>

        ![Välja ContactPersonID kustutamine](media/cust_selfref3.png)

    4. <span data-ttu-id="0d8e3-184">Välja **InvoiceAccount** kustutamiseks korrake neid samme.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![Välja InvoiceAccount kustutamine](media/cust_selfref4.png)

    5. <span data-ttu-id="0d8e3-186">Salvestage oma muudatused vastendusse.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="0d8e3-187">Lülitage üksuse **Kliendid V3** muudatuste jälgimine välja.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="0d8e3-188">Valige tööruumis **Andmehaldus** paan **Andmetabelid**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="0d8e3-189">Valige üksus **Kliendid V3**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="0d8e3-190">Valige tegumipaanilt **Suvandid** ja seejärel **Muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Muudatuse jälgimise suvandi valimine](media/selfref_options.png)

    4. <span data-ttu-id="0d8e3-192">Valige **Keela muudatuste jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-192">Select **Disable Change Tracking**.</span></span>

        ![Suvandi „Keela muudatuste jälgimine” valimine](media/selfref_tracking.png)

3. <span data-ttu-id="0d8e3-194">Käivitage üksuse **Kliendid V3 (kontod)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="0d8e3-195">Esmane sünkroonimine peaks toimima tõrgeteta.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="0d8e3-196">Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d8e3-197">Sama nimega vastendusi on kaks.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-197">There are two maps that have the same name.</span></span> <span data-ttu-id="0d8e3-198">Valige vastendus, millel on vahekaardil **Üksikasjad** järgmine kirjeldus: **Topeltkirjutamise mall üksuse FO.CDS Hankija Kontaktid V2 sünkroonimiseks üksusega CDS.Kontaktid. Vajab uut paketti \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="0d8e3-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="0d8e3-199">Lisage väljad **InvoiceAccount** ja **ContactPersonId** tagasi vastendusse **Kliendid V3 (Kontod)** ning seejärel salvestage vastendus.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="0d8e3-200">Nüüd on nii väli **InvoiceAccount** kui ka väli **ContactPersonId** taas osa reaalajas sünkroonimise režiimist.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="0d8e3-201">Järgmise sammu käigus esmasünkroonite need väljad.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="0d8e3-202">Käivitage uuesti üksuse **Kliendid V3 (kontod)** vastenduse esmane sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="0d8e3-203">Kuna muudatuste jälgimine on välja lülitatud, siis sünkroonitakse väljade **InvoiceAccount** ja **ContactPersonId** andmed rakendusest Finance and Operations rakendusega Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="0d8e3-204">Väljade **InvoiceAccount** ja **ContactPersonId** andmete sünkroonimiseks rakendusest Dataverse rakendusega Finance and Operations peate kasutama andmeintegratsiooni projekti.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="0d8e3-205">Looge rakenduses Power Apps tabelite **Sales.Account** ja **Finance and Operations apps.Customers V3** vahel andmete integreerimise projekt.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="0d8e3-206">Andmete suund peab olema rakendusest Dataverse rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="0d8e3-207">Kuna **InvoiceAccount** on topeltkirjutuses uus atribuut, siis võite selle atribuudi esmase sünkroonimise vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="0d8e3-208">Lisateavet vt teemast [Andmete integreerimine teenusesse Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="0d8e3-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="0d8e3-209">Järgmisel illustratsioonil on toodud projekt, mis värskendab väljasid **CustomerAccount** ja **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Andmeintegratsiooni projekt väljade CustomerAccount ja ContactPersonId värskendamiseks](media/cust_selfref6.png)

    2. <span data-ttu-id="0d8e3-211">Lisage teenuse Dataverse poolel filtrite all ettevõtte kriteeriumid, et rakenduses Finance and Operations värskendataks vaid filtri kriteeriumidele vastavaid ridu.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="0d8e3-212">Filtri lisamiseks valige filtri nupp.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="0d8e3-213">Seejärel saate dialoogiboksis **Päringu redigeerimine** lisada filtri päringu, nagu näiteks **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="0d8e3-214">[MÄRKUS] Kui filtri nuppu ei kuvata, siis saate luua tugiteenusepileti, et paluda andmeintegratsiooni meeskonnal lubada teie rentnikus filtri võimalus.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="0d8e3-215">Kui te ei sisesta **\_msdyn\_company\_value** jaoks filtri päringut, siis sünkroonitakse kõik read.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Filtri päringu lisamine](media/cust_selfref7.png)

    <span data-ttu-id="0d8e3-217">Ridade esmane sünkroonimine on nüüd lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="0d8e3-218">Lülitage rakenduses Finance and Operations üksuse **Kliendid V3** muudatuste jälgimine tagasi sisse.</span><span class="sxs-lookup"><span data-stu-id="0d8e3-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
