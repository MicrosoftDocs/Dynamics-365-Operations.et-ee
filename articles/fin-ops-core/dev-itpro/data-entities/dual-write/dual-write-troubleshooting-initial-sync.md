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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172710"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="58942-103">Probleemide tõrkeotsing esmase sünkroonimise ajal</span><span class="sxs-lookup"><span data-stu-id="58942-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="58942-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="58942-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="58942-105">Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.</span><span class="sxs-lookup"><span data-stu-id="58942-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="58942-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="58942-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="58942-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="58942-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="58942-108">Esmase sünkroonomise tõrgete kontrollimine Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="58942-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="58942-109">Pärast vastendamise mallide lubamist peaks vastenduse olekuks olema **Töötab**.</span><span class="sxs-lookup"><span data-stu-id="58942-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="58942-110">Kui olek on **Ei tööta**, ilmnes tõrkeid esmasel sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="58942-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="58942-111">Tõrgete kuvamiseks valige lehel **Topeltkirjutus** vahekaart **Esmase sünkroonimise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="58942-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Esmase sünkroonimise üksikasjade vahekaart](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="58942-113">Esmast sünkroonimist ei saa lõpule viia: 400 vigane päring</span><span class="sxs-lookup"><span data-stu-id="58942-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="58942-114">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="58942-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="58942-115">Kui proovite käivitada vastendust ja esmast sünkroonimist, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="58942-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="58942-116">*Kaugserver tagastas tõrke: (400) vigane päring.), AXeksportimisel ilmnes tõrge*</span><span class="sxs-lookup"><span data-stu-id="58942-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="58942-117">Siin on tabeli täieliku tõrketeate näide.</span><span class="sxs-lookup"><span data-stu-id="58942-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="58942-118">Kui see tõrge ilmneb järjepidevalt ja te ei saa esmast sünkroonimist lõpule viia, toimige probleemi lahendamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="58942-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="58942-119">Logige rakenduse Finance and Operations virtuaalarvutisse (VM) sisse.</span><span class="sxs-lookup"><span data-stu-id="58942-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="58942-120">Avage Microsofti halduskonsool.</span><span class="sxs-lookup"><span data-stu-id="58942-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="58942-121">Paanil **Teenused** veenduge, et Microsoft Dynamics 365 andmete importimise/eksportimise raamistiku teenus töötab.</span><span class="sxs-lookup"><span data-stu-id="58942-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="58942-122">Taaskäivitage see, kui see on peatatud, kuna esmane sünkroonimine nõuab seda.</span><span class="sxs-lookup"><span data-stu-id="58942-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="58942-123">Esmase sünkroonimise tõrge: 403 keelatud</span><span class="sxs-lookup"><span data-stu-id="58942-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="58942-124">Teile võidakse kuvada esmase sünkroonimise ajal järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="58942-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="58942-125">*(\[Keelatud\], kaugserver tagastas tõrke: (403) keelatud.), AX eksportimisel ilmnes tõrge*</span><span class="sxs-lookup"><span data-stu-id="58942-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="58942-126">Probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="58942-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="58942-127">Logige rakendusse Finance and Operations sisse.</span><span class="sxs-lookup"><span data-stu-id="58942-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="58942-128">Kustutage lehel **Azure Active Directory rakendused** klient **DtAppID** ja seejärel lisage see uuesti.</span><span class="sxs-lookup"><span data-stu-id="58942-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD rakenduste loend](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="58942-130">Eneseviite tõrked esmase sünkroonimise ajal</span><span class="sxs-lookup"><span data-stu-id="58942-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="58942-131">Teile võidakse kuvada tõrketeade, mis sarnaneb järgmisele näitele, kui mõnel teie vastendustest on eneseviited.</span><span class="sxs-lookup"><span data-stu-id="58942-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="58942-132">*Hankijatel V2 järgnev tõrge: kirje ID: uus kirje, ErrorMessage: guidi ei saanud lahendada väljal: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Otsinguväärtust ei leitud: CN-001. Proovige URL-i, et kontrollida kas viiteandmed on olemas: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="58942-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="58942-133">Seda tüüpi tõrget ilmneb vastenduste esmastel sünkroonimistel, millel on eneseviited.</span><span class="sxs-lookup"><span data-stu-id="58942-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="58942-134">Eelnevas näites viitab välja arve konto hankija üksusele.</span><span class="sxs-lookup"><span data-stu-id="58942-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="58942-135">Probleemi lahendamiseks peate tõenäoliselt edukaks esmaseks sünkroonimiseks käitama vastendamist kaks korda.</span><span class="sxs-lookup"><span data-stu-id="58942-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

