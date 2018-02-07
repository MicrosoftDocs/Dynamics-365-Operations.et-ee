--- 
title: " Väljavõtete sisestamiseks töö konfigureerimine ja käivitamine"
description: "See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete sisestamiseks."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: f3587fe70dc6a0d8330063db77e625040a53da98
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="40f1a-103"> Väljavõtete sisestamiseks töö konfigureerimine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="40f1a-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="40f1a-104">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="40f1a-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="40f1a-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="40f1a-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="40f1a-106">Avage Kõik tööruumid >...</span><span class="sxs-lookup"><span data-stu-id="40f1a-106">Go to All workspaces > ..</span></span> <span data-ttu-id="40f1a-107">> Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="40f1a-107">> Retail store financials.</span></span>
2. <span data-ttu-id="40f1a-108">Klõpsake suvandit Väljavõtete sisestamine.</span><span class="sxs-lookup"><span data-stu-id="40f1a-108">Click Post statements.</span></span>
    * <span data-ttu-id="40f1a-109">Valige organisatsiooni hierarhia ja seejärel valige organisatsiooni sõlmepuul kindel kauplus või sõlm.</span><span class="sxs-lookup"><span data-stu-id="40f1a-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="40f1a-110">Valige sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="40f1a-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="40f1a-111">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="40f1a-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="40f1a-112">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="40f1a-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="40f1a-113">Märkige või tühjendage ruut Pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="40f1a-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="40f1a-114">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="40f1a-114">Click Recurrence.</span></span>
6. <span data-ttu-id="40f1a-115">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="40f1a-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="40f1a-116">Sisestage kellaaeg väljale Algusaeg.</span><span class="sxs-lookup"><span data-stu-id="40f1a-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="40f1a-117">Valige, kas soovite kordumise lõpetada pärast teatud arvu käitamisi, kindlal kuupäeval või mitte kunagi.</span><span class="sxs-lookup"><span data-stu-id="40f1a-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="40f1a-118">See kasutage erinevaid suvandeid, et määratleda töö käitamissagedus.</span><span class="sxs-lookup"><span data-stu-id="40f1a-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="40f1a-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="40f1a-119">Click OK.</span></span>
9. <span data-ttu-id="40f1a-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="40f1a-120">Click OK.</span></span>


