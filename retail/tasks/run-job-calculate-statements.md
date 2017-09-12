--- 
title: " Väljavõtete arvutamiseks töö konfigureerimine ja käivitamine"
description: "See protseduur selgitab korduvate pakett-tööde konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete loomiseks ja arvutamiseks."
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
ms.openlocfilehash: 2bae81073fa6561c02d2dac0cd83db6a10ad00c3
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="3982a-103"> Väljavõtete arvutamiseks töö konfigureerimine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="3982a-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3982a-104">See protseduur selgitab korduvate pakett-tööde konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete loomiseks ja arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="3982a-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="3982a-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="3982a-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3982a-106">Avage Kõik tööruumid > Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="3982a-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="3982a-107">Klõpsake suvandit Väljavõtete arvutamine.</span><span class="sxs-lookup"><span data-stu-id="3982a-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="3982a-108">Valige kindel kauplus või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="3982a-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3982a-109">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="3982a-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="3982a-110">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="3982a-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="3982a-111">Valige suvandi Pakktöötlus sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="3982a-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="3982a-112">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="3982a-112">Click Recurrence.</span></span>
6. <span data-ttu-id="3982a-113">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="3982a-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="3982a-114">Sisestage kellaaeg väljale Algusaeg.</span><span class="sxs-lookup"><span data-stu-id="3982a-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="3982a-115">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="3982a-115">Select the No end date option.</span></span>
9. <span data-ttu-id="3982a-116">Sisestage väljale PatternUnit suvand Päevad.</span><span class="sxs-lookup"><span data-stu-id="3982a-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="3982a-117">Sisestage number väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="3982a-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="3982a-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3982a-118">Click OK.</span></span>
12. <span data-ttu-id="3982a-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3982a-119">Click OK.</span></span>


