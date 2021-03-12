---
title: Eelarvesoovituste lubamine (eelversioon)
description: Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse eelarvesoovituste funktsioon.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995136"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="07c2d-103">Eelarvesoovituste lubamine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="07c2d-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="07c2d-104">Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse eelarvesoovituste funktsioon.</span><span class="sxs-lookup"><span data-stu-id="07c2d-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="07c2d-105">Kasutage teavet teenuse Microsoft Dynamics Lifecycle Services (LCS) lehelt, et ühendada Azure SQL-i esmane eksemplar selle keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="07c2d-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="07c2d-106">Käivitage järgmine Transact-SQL (T-SQL) käsk, et lülitada liivakasti keskkonna eelväljaanded sisse.</span><span class="sxs-lookup"><span data-stu-id="07c2d-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="07c2d-107">(Enne rakendusobjekti serveriga \[AOS\] eemalt ühenduse loomist võib olla vajalik, et peate LCS-is lülitama oma IP-aadressi juurdepääsu sisse.)</span><span class="sxs-lookup"><span data-stu-id="07c2d-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="07c2d-108">Kui teie Microsoft Dynamics 365 Finance on Service Fabricu juurutus, saate selle sammu vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="07c2d-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="07c2d-109">Finantsülevaadete meeskond peaks olema väljaande juba teie jaoks sisse lülitanud.</span><span class="sxs-lookup"><span data-stu-id="07c2d-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="07c2d-110">Kui te funktsiooni tööruumis **Funktsiooni haldus** ei näe või kui teil esineb selle sisselülitamisel probleeme, saatke [finantsülevaadete rakenduse eelversiooni meeskonnale](mailto:fiap@microsoft.com) meil.</span><span class="sxs-lookup"><span data-stu-id="07c2d-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="07c2d-111">Avage tööruum **Funktsioonide haldus** ja järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="07c2d-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="07c2d-112">Valige **Otsi värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="07c2d-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="07c2d-113">Otsige suvandit **Eelarve soovitus** ja lülitage see funktsioon sisse.</span><span class="sxs-lookup"><span data-stu-id="07c2d-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="07c2d-114">Avage suvand **Eelarvestamine \> Seadistus \> Põhiline eelarvestamine \> Eelarvesoovitus (eelversioon)** ja valige suvand **Luba funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="07c2d-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="07c2d-115">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="07c2d-115">Privacy notice</span></span>
<span data-ttu-id="07c2d-116">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="07c2d-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
