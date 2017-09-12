--- 
title: " Jaemüügi väljavõtete parameetrikonfiguratsioonid"
description: "See protseduur selgitab jaemüügi parameetrikonfiguratsioone, mis mõjutavad jaemüügi väljavõtete loomise ja sisestamise viisi."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 731a3ec06efa103ba663df83240c77dfe78bb7cd
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="ce575-103"> Jaemüügi väljavõtete parameetrikonfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="ce575-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ce575-104">See protseduur selgitab jaemüügi parameetrikonfiguratsioone, mis mõjutavad jaemüügi väljavõtete loomise ja sisestamise viisi.</span><span class="sxs-lookup"><span data-stu-id="ce575-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="ce575-105">See protsess kasutab demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ce575-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="ce575-106">Avage Jaemüük ja kaubandus > Peakontori seadistamine > Parameetrid > Jaemüügi parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ce575-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="ce575-107">Klõpsake vahekaarti Sisestamine.</span><span class="sxs-lookup"><span data-stu-id="ce575-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="ce575-108">Valige suvand Jah, kui soovite sisestada eraldi perioodilise allahindluse summad.</span><span class="sxs-lookup"><span data-stu-id="ce575-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="ce575-109">Valige suvand Standard, kui soovite kasutada vaikekontosid, või suvand Perioodiline, kui soovite määratleda, millist kontot iga perioodilise allahindluse puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="ce575-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="ce575-110">Valige suvand Kokkuvõte, kui varude read tuleks võimaluse korral liita.</span><span class="sxs-lookup"><span data-stu-id="ce575-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="ce575-111">Valige suvand Jah, kui arved ja maksed tuleks osana väljavõtte sisestamise protsessist automaatselt tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="ce575-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="ce575-112">Valige suvand Jah, kui raha seifi viimise kanded tuleks liita.</span><span class="sxs-lookup"><span data-stu-id="ce575-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="ce575-113">Valige suvand Jah, kui raha panka hoiustamise kanded tuleks liita.</span><span class="sxs-lookup"><span data-stu-id="ce575-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="ce575-114">Valige suvand Jah, kui soovite liitmise väljavõtte sisestamise jaoks sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="ce575-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="ce575-115">Valige suvand Jah, kui soovite tellimusi luua ja töödelda paralleelselt väljavõtete sisestamisega.</span><span class="sxs-lookup"><span data-stu-id="ce575-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="ce575-116">Sisestage igas pakett-töö ülesandes töödeldav tellimuste maksimumkogus.</span><span class="sxs-lookup"><span data-stu-id="ce575-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="ce575-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ce575-117">Click Save.</span></span>


