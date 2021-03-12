---
title: Rahavoo prognoosimise lubamine (eelversioon)
description: Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse rahavoo prognoosimise funktsioon.
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
ms.openlocfilehash: 1977dac4a3ab66cca2248dc0124d3a06d6963f40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978760"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="c6b02-103">Rahavoo prognoosimise lubamine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="c6b02-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c6b02-104">Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse rahavoo prognoosimise funktsioon.</span><span class="sxs-lookup"><span data-stu-id="c6b02-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="c6b02-105">Maksete prognoosimises rahavoo kasutamiseks peate häälestama kliendimaksete prognoosimise funktsiooni, nagu on kirjeldatud jaotises [Kliendimaksete prognoosimise lubamine](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="c6b02-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="c6b02-106">Kasutage teavet teenuse Microsoft Dynamics Lifecycle Services (LCS) lehelt, et ühendada Azure SQL-i esmane eksemplar selle keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="c6b02-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="c6b02-107">Käivitage järgmine Transact-SQL (T-SQL) käsk, et lülitada liivakasti keskkonna eelväljaanded sisse.</span><span class="sxs-lookup"><span data-stu-id="c6b02-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="c6b02-108">(Enne rakendusobjekti serveriga \[AOS\] eemalt ühenduse loomist võib olla vajalik, et peate LCS-is lülitama oma IP-aadressi juurdepääsu sisse.)</span><span class="sxs-lookup"><span data-stu-id="c6b02-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="c6b02-109">Kui teie Microsoft Dynamics 365 Finance on Service Fabricu juurutus, saate selle sammu vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="c6b02-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="c6b02-110">Finantsülevaadete meeskond peaks olema väljaande juba teie jaoks sisse lülitanud.</span><span class="sxs-lookup"><span data-stu-id="c6b02-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="c6b02-111">Kui te funktsioone tööruumis **Funktsioonihaldus** ei näe või kui nende sisselülitamisel esineb probleeme, võtke ühendust aadressil <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="c6b02-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="c6b02-112">Avage tööruum **Funktsioonide haldus** ja järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="c6b02-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="c6b02-113">Valige **Otsi värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="c6b02-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="c6b02-114">Järgmiste funktsioonide sisselülitamine.</span><span class="sxs-lookup"><span data-stu-id="c6b02-114">Turn on the following features:</span></span>

        - <span data-ttu-id="c6b02-115">Uus ruudustiku juhtelement</span><span class="sxs-lookup"><span data-stu-id="c6b02-115">New grid control</span></span>
        - <span data-ttu-id="c6b02-116">Ruudustikus grupeerimine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="c6b02-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="c6b02-117">Kliendimaksete prognoosid (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="c6b02-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="c6b02-118">Likviidsuse planeerimine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="c6b02-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="c6b02-119">Avage jaotis **Sularaha ja panga haldus \>Rahavoo prognoosimise seadistus** ja lisage likviiduses kontod, mis peaksid olema prognoosi kaasatud.</span><span class="sxs-lookup"><span data-stu-id="c6b02-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6b02-120">Kui likviidsuse kontosid ei ole seadistatud, ei saa rahavoogu luua.</span><span class="sxs-lookup"><span data-stu-id="c6b02-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="c6b02-121">Avage jaotis **Sularaha ja panga haldus \> Seadistus \> Finantsülevaated (eelversioon) \> Rahavoo prognoosid (eelversioon)** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c6b02-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="c6b02-122">Valige vahekaardil **Rahavoo prognoosimine** suvand **Luba funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="c6b02-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="c6b02-123">Valige **Prognoosimise mudeli loomine**.</span><span class="sxs-lookup"><span data-stu-id="c6b02-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="c6b02-124">Lisainfo saamiseks rahavoo prognoosimise võimaluste kohta vt teemast [Rahavoo prognoosimine](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="c6b02-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="c6b02-125">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="c6b02-125">Privacy notice</span></span>

<span data-ttu-id="c6b02-126">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="c6b02-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
