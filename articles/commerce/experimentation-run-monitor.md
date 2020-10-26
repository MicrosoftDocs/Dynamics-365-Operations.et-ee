---
title: Eksperimendi käitamine ja jälgimine
description: Selles teemas kirjeldatakse, kuidas käitada ja jälgida eksperimenti kolmanda osapoole teenuses. Selles kirjeldatakse ka, kuidas muuta variatsioone pärast eksperimendi alustamist.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930179"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="dd5bd-104">Eksperimendi käitamine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="dd5bd-104">Run and monitor an experiment</span></span>

<span data-ttu-id="dd5bd-105">Selles teemas kirjeldatakse, kuidas käitada ja jälgida oma eksperimenti kolmanda osapoole rakenduses ning vajadusel variatsioone muuta.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="dd5bd-106">Enne selle teema juhiste täitmist tuleb teil oma eksperiment rakenduses Commerce [avaldada](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="dd5bd-106">Before you complete the steps in this topic, you'll need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> <span data-ttu-id="dd5bd-107">Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="dd5bd-108">Täiendavad etapid on toodud eraldi teemades.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="dd5bd-109">[ ![Eksperimendi kasutaja teekond – käitamine ja jälgimine](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="dd5bd-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="dd5bd-110">Kui olete oma variatsioonid avaldanud, on tehtud rakenduses Commerce kõik vajalikud sammud eksperimendi käitamiseks.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-110">After you publish your variations, all the steps you need to do in Commerce to run your experiment are done.</span></span> <span data-ttu-id="dd5bd-111">Järgmine samm on määrata kindlaks, millist variatsiooni igale kasutajale lehe pärimisel näidata.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="dd5bd-112">Selle teeb kindlaks kolmanda osapoole teenus, kuid esmalt tuleb teil teenuses eksperiment aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="dd5bd-113">Kuna eksperimendi aktiveerimine varieerub iga teenuse puhul, peate järgima teenuse või pakkuja juhiseid.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="dd5bd-114">Kui eksperiment ei ole aktiveeritud, näevad kasutajad ainult lehe vaikeversiooni – ühtegi variatsiooni ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-114">If the experiment is not activated, users will only see the default version of the page - no variations will be displayed.</span></span>

<span data-ttu-id="dd5bd-115">Peate eksperimenti piisavalt kaua töös hoidma, et koguda andmeid statistiliselt paikapidavate tulemuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="dd5bd-116">Kasutage kolmanda osapoole teenust, et jälgida eksperimendi käitamise ajal eksperimendiga seotud andmeid ja analüüsi.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="dd5bd-117">Variatsioonide kohandamine</span><span class="sxs-lookup"><span data-stu-id="dd5bd-117">Adjust your variations</span></span>
<span data-ttu-id="dd5bd-118">Kui peate mingil põhjusel variatsioone muutma, järgige alltoodud samme.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd5bd-119">Kui muudate aktiivset eksperimenti rakenduses Commerce või kolmanda osapoole teenuses, võib see tulemusi oluliselt mõjutada.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="dd5bd-120">Võib-olla on parem lasta eksperimendil lõpuni jõuda ja seejärel suurte muudatuste jaoks uus eksperiment luua.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="dd5bd-121">Avage saidiehitajas vahekaart **Eksperimendid** ja valige eksperiment.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-121">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
1. <span data-ttu-id="dd5bd-122">Valige rippmenüüst variatsioon, mida soovite värskendada.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="dd5bd-123">Tehke vajalikud muudatused, seejärel vaadake variatsioonid üle ja avaldage need.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-123">Make needed changes, then preview and publish the variations.</span></span> <span data-ttu-id="dd5bd-124">Lisateavet leiate teemast [Eksperimendi eelversioon ja avaldamine](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="dd5bd-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="dd5bd-125">Minge kolmanda osapoole teenusesse, et muuta eksperimendi seadistust.</span><span class="sxs-lookup"><span data-stu-id="dd5bd-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="dd5bd-126">Eelmine etapp</span><span class="sxs-lookup"><span data-stu-id="dd5bd-126">Previous step</span></span>
[<span data-ttu-id="dd5bd-127">Eksperimendi eelversioon ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="dd5bd-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="dd5bd-128">Järgmine etapp</span><span class="sxs-lookup"><span data-stu-id="dd5bd-128">Next step</span></span>
[<span data-ttu-id="dd5bd-129">Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="dd5bd-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
