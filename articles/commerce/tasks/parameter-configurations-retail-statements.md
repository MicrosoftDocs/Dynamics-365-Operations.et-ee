---
title: Jaemüügi väljavõtteid mõjutavate parameetrite konfigureerimine
description: Selles teemas demonstreeritakse Kaubanduse parameetrite konfiguratsioone, mis mõjutavad väljavõtete loomist ja sisestamist.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022247"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="46a18-103">Jaemüügi väljavõtteid mõjutavate parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="46a18-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="46a18-104">Selles teemas demonstreeritakse Kaubanduse parameetrite konfiguratsioone, mis mõjutavad väljavõtete loomist ja sisestamist.</span><span class="sxs-lookup"><span data-stu-id="46a18-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="46a18-105">See protsess kasutab demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="46a18-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="46a18-106">Avage navigeerimispaanil **Moodulid > Jaemüük ja kaubandus > Peakontori seadistus > Parameetrid > Kaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="46a18-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="46a18-107">Valige vahekaart **Sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="46a18-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="46a18-108">Valige **Jah**, kui soovite sisestada just perioodilise allahindluse summasid.</span><span class="sxs-lookup"><span data-stu-id="46a18-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="46a18-109">Valige **Standardne**, et kasutada vaikekontosid, või valige **Perioodiline**, kui soovite määratleda, milliseid kontosid iga perioodilise allahindluse jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="46a18-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="46a18-110">Kui varude read tuleks võimalusel alati kokku võtta, valige **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="46a18-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="46a18-111">Valige **Jah**, kui arved ja maksed tuleks alati aruande sisestamise protsessi käigus automaatselt tasuda.</span><span class="sxs-lookup"><span data-stu-id="46a18-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="46a18-112">Valige **Jah**, kui Seifi vähenemise tehingud tuleks kokku võtta.</span><span class="sxs-lookup"><span data-stu-id="46a18-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="46a18-113">Valige **Jah**, kui Panga vähenemise tehingud tuleks kokku võtta.</span><span class="sxs-lookup"><span data-stu-id="46a18-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="46a18-114">Valige **Jah**, et lülitada sisse aruannete sisestamise kokku võtmine.</span><span class="sxs-lookup"><span data-stu-id="46a18-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="46a18-115">Valige **Jah**, et aruannete sisestamisel paralleelselt tellimusi luua ja töödelda.</span><span class="sxs-lookup"><span data-stu-id="46a18-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="46a18-116">Sisestage igas pakett-töö ülesandes töödeldav tellimuste maksimumkogus.</span><span class="sxs-lookup"><span data-stu-id="46a18-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="46a18-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="46a18-117">Select **Save**.</span></span>

