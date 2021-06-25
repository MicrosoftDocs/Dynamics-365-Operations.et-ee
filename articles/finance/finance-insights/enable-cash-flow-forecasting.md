---
title: Rahavoo prognoosimise lubamine (eelversioon)
description: Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse rahavoo prognoosimise funktsioon.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222554"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="8ef29-103">Rahavoo prognoosimise lubamine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="8ef29-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8ef29-104">Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse rahavoo prognoosimise funktsioon.</span><span class="sxs-lookup"><span data-stu-id="8ef29-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="8ef29-105">Maksete prognoosimises rahavoo kasutamiseks peate häälestama kliendimaksete prognoosimise funktsiooni, nagu on kirjeldatud jaotises [Kliendimaksete prognoosimise lubamine](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="8ef29-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="8ef29-106">Kasutage teavet teenuse Microsoft Dynamics Lifecycle Services (LCS) lehelt, et ühendada Azure SQL-i esmane eksemplar selle keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="8ef29-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="8ef29-107">Käivitage järgmine Transact-SQL (T-SQL) käsk, et lülitada liivakasti keskkonna eelväljaanded sisse.</span><span class="sxs-lookup"><span data-stu-id="8ef29-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="8ef29-108">(Enne rakendusobjekti serveriga \[AOS\] eemalt ühenduse loomist võib olla vajalik, et peate LCS-is lülitama oma IP-aadressi juurdepääsu sisse.)</span><span class="sxs-lookup"><span data-stu-id="8ef29-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="8ef29-109">Jätke see samm vahele, kui kasutate 10.0.20 või uuemat versiooni või kui kasutate Service Fabric juurutamist.</span><span class="sxs-lookup"><span data-stu-id="8ef29-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="8ef29-110">Finantsülevaadete meeskond peaks olema väljaande juba teie jaoks sisse lülitanud.</span><span class="sxs-lookup"><span data-stu-id="8ef29-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="8ef29-111">Kui te funktsiooni tööruumis **Funktsioonihaldus** ei näe või kui selle sisselülitamisel esineb probleeme, võtke ühendust aadressil <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="8ef29-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="8ef29-112">Avage tööruum **Funktsioonide haldus** ja järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="8ef29-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="8ef29-113">Valige **Otsi värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="8ef29-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="8ef29-114">Järgmiste funktsioonide sisselülitamine.</span><span class="sxs-lookup"><span data-stu-id="8ef29-114">Turn on the following features:</span></span>

        - <span data-ttu-id="8ef29-115">Uus ruudustiku juhtelement</span><span class="sxs-lookup"><span data-stu-id="8ef29-115">New grid control</span></span>
        - <span data-ttu-id="8ef29-116">Ruudustikus grupeerimine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="8ef29-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="8ef29-117">Kliendimaksete prognoosid (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="8ef29-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="8ef29-118">Likviidsuse planeerimine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="8ef29-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="8ef29-119">Avage jaotis **Sularaha ja panga haldus \>Rahavoo prognoosimise seadistus** ja lisage likviiduses kontod, mis peaksid olema prognoosi kaasatud.</span><span class="sxs-lookup"><span data-stu-id="8ef29-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8ef29-120">Kui likviidsuse kontosid ei ole seadistatud, ei saa rahavoogu luua.</span><span class="sxs-lookup"><span data-stu-id="8ef29-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="8ef29-121">Avage jaotis **Sularaha ja panga haldus \> Seadistus \> Finantsülevaated (eelversioon) \> Rahavoo prognoosid (eelversioon)** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="8ef29-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="8ef29-122">Valige vahekaardil **Rahavoo prognoosimine** suvand **Luba funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="8ef29-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="8ef29-123">Valige **Prognoosimise mudeli loomine**.</span><span class="sxs-lookup"><span data-stu-id="8ef29-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="8ef29-124">Lisainfo saamiseks rahavoo prognoosimise võimaluste kohta vt teemast [Rahavoo prognoosimine](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="8ef29-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
