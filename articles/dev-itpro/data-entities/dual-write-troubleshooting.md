---
title: Tõrkeotsingu juhend andmete integreerimiseks
description: See teema annab teavet Microsoft Dynamics 365 for Finance and Operations ja Common Data Service’i vahelise andmete integratsiooni tõrkeotsingu kohta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873101"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="aa57a-103">Tõrkeotsingu juhend andmete integreerimiseks</span><span class="sxs-lookup"><span data-stu-id="aa57a-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="aa57a-104">Lubage Common Data Service’i lisandmooduli jälituslogid ja kontrollige topeltkirjutamise lisandmooduli vea andmeid</span><span class="sxs-lookup"><span data-stu-id="aa57a-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="aa57a-105">Kui kogete topeltkirjutamise sünkroniseerimisel probleemi või viga, järgige jälituslogi vigade kontrollimiseks neid etappe.</span><span class="sxs-lookup"><span data-stu-id="aa57a-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="aa57a-106">Enne vigade kontrollimist peate lubama lisandmooduli jälituslogid.</span><span class="sxs-lookup"><span data-stu-id="aa57a-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="aa57a-107">Juhised leiate [õpetuse: lisandmooduli kirjutamine ja registreerimine](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) jaotisest „Jälituslogide vaatamine“.</span><span class="sxs-lookup"><span data-stu-id="aa57a-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="aa57a-108">Nüüd võite vigu kontrollida.</span><span class="sxs-lookup"><span data-stu-id="aa57a-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="aa57a-109">Logige sisse rakendusse Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="aa57a-109">Sign in to Microsoft Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="aa57a-110">Valige nupp **Sätted** (hammasratas) ja seejärel suvand **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="aa57a-111">Menüüs **Sätted** valige **Kohandamine\> lisandmooduli jälituslogi**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="aa57a-112">Vigade üksikasjade nägemiseks valige tüübi nimeks **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="aa57a-113">Kontrollige Finance and Operationsi topeltkirjutamise sünkroonimise vigu</span><span class="sxs-lookup"><span data-stu-id="aa57a-113">Inspect dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="aa57a-114">Järgige neid juhiseid, et kontrollida testimise ajal vigu.</span><span class="sxs-lookup"><span data-stu-id="aa57a-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="aa57a-115">Microsoft Dynamics Lifecycle Services’i (LCS) sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="aa57a-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="aa57a-116">Avage LCS projekt, mille topeltkirjutamist testida.</span><span class="sxs-lookup"><span data-stu-id="aa57a-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="aa57a-117">Valige **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="aa57a-118">Looge kaugtöölaua ühendus Dynamics 365 for Finance and Operationsi virtuaalarvutiga (VM), kasutage selleks LCS-is näidatavat kohalikku kontot.</span><span class="sxs-lookup"><span data-stu-id="aa57a-118">Make a Remote desktop connection to the Dynamics 365 for Finance and Operations virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="aa57a-119">Avage sündmusevaatur.</span><span class="sxs-lookup"><span data-stu-id="aa57a-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="aa57a-120">Minge **Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> AX-DualWriteSync \> Toiming**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="aa57a-121">Näidatakse tõrkeid ja üksikasju.</span><span class="sxs-lookup"><span data-stu-id="aa57a-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a><span data-ttu-id="aa57a-122">Linkige lahti üks Common Data Service’i keskkond rakendusest Finance and Operations ja linkige teine keskkond</span><span class="sxs-lookup"><span data-stu-id="aa57a-122">Unlink one Common Data Service environment from Finance and Operations and link another environment</span></span>

<span data-ttu-id="aa57a-123">Linkide värskendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="aa57a-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="aa57a-124">Minge Finance and Operationsi keskkonda.</span><span class="sxs-lookup"><span data-stu-id="aa57a-124">Go to the Finance and Operations environment.</span></span>
2. <span data-ttu-id="aa57a-125">Avage andmehaldus.</span><span class="sxs-lookup"><span data-stu-id="aa57a-125">Open Data Management.</span></span>
3. <span data-ttu-id="aa57a-126">Valige **CDS rakenduste jaoks link**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="aa57a-127">Valige kõik töötavad vastendused ja seejärel valige **Peata**</span><span class="sxs-lookup"><span data-stu-id="aa57a-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="aa57a-128">Valige kõik töötavad vastendused ja seejärel valige nuppu **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aa57a-129">Suvand **Kustuta** pole saadaval, kui mall **CustomerV3-Account** on valitud.</span><span class="sxs-lookup"><span data-stu-id="aa57a-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="aa57a-130">Vajadusel tühjendage selle malli valik.</span><span class="sxs-lookup"><span data-stu-id="aa57a-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="aa57a-131">**CustomerV3-Account** on vanem ettevalmistatud mall ja töötab raha väljavaate lahendusega.</span><span class="sxs-lookup"><span data-stu-id="aa57a-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="aa57a-132">Kuna see on välja antud ülemaailmselt, näidatakse seda kõigi mallide puhul.</span><span class="sxs-lookup"><span data-stu-id="aa57a-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="aa57a-133">Valige nupp **Tühista keskkonna link**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="aa57a-134">Toimingu kinnitamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="aa57a-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="aa57a-135">Uue keskkonna linkimiseks järgige [installimise juhendis](https://aka.ms/dualwrite-docs) olevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="aa57a-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
