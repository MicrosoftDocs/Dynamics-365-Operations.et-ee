---
title: Väljavõtete sisestamiseks töö konfigureerimine ja käivitamine
description: See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete sisestamiseks.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550112"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="8b9c3-103">Väljavõtete sisestamiseks töö konfigureerimine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="8b9c3-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8b9c3-104">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="8b9c3-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8b9c3-106">Avage Kõik tööruumid >...</span><span class="sxs-lookup"><span data-stu-id="8b9c3-106">Go to All workspaces > ..</span></span> <span data-ttu-id="8b9c3-107">> Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-107">> Retail store financials.</span></span>
2. <span data-ttu-id="8b9c3-108">Klõpsake suvandit Väljavõtete sisestamine.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-108">Click Post statements.</span></span>
    * <span data-ttu-id="8b9c3-109">Valige organisatsiooni hierarhia ja seejärel valige organisatsiooni sõlmepuul kindel kauplus või sõlm.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="8b9c3-110">Valige sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="8b9c3-111">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="8b9c3-112">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="8b9c3-113">Märkige või tühjendage ruut Pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="8b9c3-114">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-114">Click Recurrence.</span></span>
6. <span data-ttu-id="8b9c3-115">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="8b9c3-116">Sisestage kellaaeg väljale Algusaeg.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="8b9c3-117">Valige, kas soovite kordumise lõpetada pärast teatud arvu käitamisi, kindlal kuupäeval või mitte kunagi.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="8b9c3-118">See kasutage erinevaid suvandeid, et määratleda töö käitamissagedus.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="8b9c3-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-119">Click OK.</span></span>
9. <span data-ttu-id="8b9c3-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8b9c3-120">Click OK.</span></span>

