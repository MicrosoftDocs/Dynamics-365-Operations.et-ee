---
title: Tõrkeotsingu juhend andmete integreerimiseks
description: See teema pakub tõrkeotsingu teavet andmete integreerimise kohta rakenduste Microsoft Dynamics 365 for Finance and Operations ja Common Data Service vahel.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797271"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="74289-103">Tõrkeotsingu juhend andmete integreerimiseks</span><span class="sxs-lookup"><span data-stu-id="74289-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="74289-104">Lülitage sisse lisandmoodulite jälgimine rakenduses Common Data Service ja kontrollige topeltkirjutamise lisandmooduli vea üksikasju.</span><span class="sxs-lookup"><span data-stu-id="74289-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="74289-105">Kui teil esineb probleem või tõrge topeltkirjutamise sünkroonimisega, saate kontrollida vigu jälituslogis.</span><span class="sxs-lookup"><span data-stu-id="74289-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="74289-106">Enne kui saate vigu kontrollida, peate lubama lisandmooduli jälgimise, kasutades juhiseid teemas [Lisandmooduli registreerimine](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) lisandmooduli jälgimise lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="74289-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="74289-107">Nüüd saate tõrkeid kontrollida.</span><span class="sxs-lookup"><span data-stu-id="74289-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="74289-108">Dynamics 365 for Sales-sse sisselogimine</span><span class="sxs-lookup"><span data-stu-id="74289-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="74289-109">Klõpsake ikoonil Sätted (käik) ja valige **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="74289-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="74289-110">Menüüs **Sätted** valige **Kohandamine > Lisandmooduli jälituslogi**.</span><span class="sxs-lookup"><span data-stu-id="74289-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="74289-111">Klõpsake tüübi nimetus **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, et kuvada tõrke üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="74289-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="74289-112">Topeltkirjutamise sünkroonimise tõrgete kontrollimine rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="74289-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="74289-113">Tõrgete kontrollimiseks testimisel toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="74289-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="74289-114">Logige sisse teenusesse Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="74289-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="74289-115">Avage LCS-i projekt, mille valisite topeltkirjutamise testimiseks.</span><span class="sxs-lookup"><span data-stu-id="74289-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="74289-116">Avage Pilve majutatud keskkonnad.</span><span class="sxs-lookup"><span data-stu-id="74289-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="74289-117">Kaugtöölaud Finance and Operations VM, kasutades kohalikku kontot, mis kuvatakse LCS-is.</span><span class="sxs-lookup"><span data-stu-id="74289-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="74289-118">Aruandevaaturi avamine</span><span class="sxs-lookup"><span data-stu-id="74289-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="74289-119">Liikuge **Rakenduste ja teenuste logid > Microsoft > Dynamics > AX-DualWriteSync > Toiming**.</span><span class="sxs-lookup"><span data-stu-id="74289-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="74289-120">Kuvatakse tõrked ja üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="74289-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="74289-121">Kuidas linkida ja lahti linkida teise Common Data Service’i keskkond rekandusest Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="74289-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="74289-122">Saate värskendada linke, järgides neid samme.</span><span class="sxs-lookup"><span data-stu-id="74289-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="74289-123">Liikuge Finance and Operationsi keskkonda.</span><span class="sxs-lookup"><span data-stu-id="74289-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="74289-124">Avage andmehaldus.</span><span class="sxs-lookup"><span data-stu-id="74289-124">Open Data Management.</span></span>
+ <span data-ttu-id="74289-125">Klõpsake **Lingi CDS rakenduste jaoks**.</span><span class="sxs-lookup"><span data-stu-id="74289-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="74289-126">Valige kõik töötavad vastendused ja klõpsake nuppu **Peata**.</span><span class="sxs-lookup"><span data-stu-id="74289-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="74289-127">Valige kõik töötavad vastendused ja klõpsake nuppu **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="74289-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="74289-128">Suvandit **Kustuta** ei kuvata, kui mall **CustomerV3-Account** on valitud.</span><span class="sxs-lookup"><span data-stu-id="74289-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="74289-129">Vajaduse korral tühistage see valik.</span><span class="sxs-lookup"><span data-stu-id="74289-129">Unselect it if needed.</span></span> <span data-ttu-id="74289-130">**CustomerV3-Account** on vanem ettevalmistatud mall ja töötab raha väljavaate lahendusega.</span><span class="sxs-lookup"><span data-stu-id="74289-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="74289-131">Kuna see on välja antud ülemaailmselt, kuvatakse see kõigi mallide puhul.</span><span class="sxs-lookup"><span data-stu-id="74289-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="74289-132">Klõpsake nuppu **Tühista keskkonna link**.</span><span class="sxs-lookup"><span data-stu-id="74289-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="74289-133">Kinnitamiseks klõpsake **Jah**.</span><span class="sxs-lookup"><span data-stu-id="74289-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="74289-134">Uue keskkonna linkimiseks järgige [installimise juhendis](https://aka.ms/dualwrite-docs) olevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="74289-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

