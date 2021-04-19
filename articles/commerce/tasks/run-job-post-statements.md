---
title: Väljavõtete sisestamiseks töö konfigureerimine ja käivitamine
description: See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete sisestamiseks.
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52baa707c36f3468263782dc8ec735e44af88e38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804229"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="2c334-103">Väljavõtete sisestamiseks töö konfigureerimine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="2c334-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c334-104">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="2c334-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="2c334-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="2c334-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2c334-106">Avage Kõik tööruumid >...</span><span class="sxs-lookup"><span data-stu-id="2c334-106">Go to All workspaces > ..</span></span> <span data-ttu-id="2c334-107">> Kaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="2c334-107">> Store financials.</span></span>
2. <span data-ttu-id="2c334-108">Klõpsake Siseta pakett-väljavõtted.</span><span class="sxs-lookup"><span data-stu-id="2c334-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="2c334-109">Valige organisatsiooni hierarhia ja seejärel valige organisatsiooni sõlmepuul kindel kauplus või sõlm.</span><span class="sxs-lookup"><span data-stu-id="2c334-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="2c334-110">Valige sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="2c334-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="2c334-111">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="2c334-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="2c334-112">Klõpsake tausta vahekaardil Käita. ![Käita taustal](../dev-itpro/media/runbackground.png "Käivita taustal")</span><span class="sxs-lookup"><span data-stu-id="2c334-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="2c334-113">Märkige või tühjendage ruut Pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="2c334-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="2c334-114">![Pakktöötlus](../dev-itpro/media/batchprocessing.png "Pakktöötlus ja korduvus")</span><span class="sxs-lookup"><span data-stu-id="2c334-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="2c334-115">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="2c334-115">Click Recurrence.</span></span>
6. <span data-ttu-id="2c334-116">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="2c334-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="2c334-117">Sisestage kellaaeg väljale Algusaeg.</span><span class="sxs-lookup"><span data-stu-id="2c334-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="2c334-118">Valige, kas soovite kordumise lõpetada pärast teatud arvu käitamisi, kindlal kuupäeval või mitte kunagi.</span><span class="sxs-lookup"><span data-stu-id="2c334-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="2c334-119">See kasutage erinevaid suvandeid, et määratleda töö käitamissagedus.</span><span class="sxs-lookup"><span data-stu-id="2c334-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="2c334-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2c334-120">Click OK.</span></span>
9. <span data-ttu-id="2c334-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2c334-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]