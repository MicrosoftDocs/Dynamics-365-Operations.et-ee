---
title: Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine
description: See teema kirjeldab, kuidas rakenduses Dynamics 365 Commerce edukat variatsiooni esile tõsta ja eksperimenti lõpule viia.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097089"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="a72d0-103">Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="a72d0-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="a72d0-104">Selles teemas kirjeldatakse, kuidas tõsta esile variatsiooni, mis sai teie eksperimendis parima tulemuse, ja kuidas eksperimenti lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="a72d0-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="a72d0-105">Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a72d0-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a72d0-106">Täiendavad etapid on toodud eraldi teemades.</span><span class="sxs-lookup"><span data-stu-id="a72d0-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="a72d0-107">[ ![Eksperimendi kasutaja teekond – ülevaatamine ja lõpetamine](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a72d0-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="a72d0-108">Kui olete [oma eksperimendi käivitanud](experimentation-run-monitor.md) ja kogunud piisavalt andmeid, et määrata, millist variatsiooni te oma aktiivsel saidil kasutada soovite, tõstate variatsiooni esile ja lõpetate eksperimendi.</span><span class="sxs-lookup"><span data-stu-id="a72d0-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="a72d0-109">Variatsiooni esiletõstmine</span><span class="sxs-lookup"><span data-stu-id="a72d0-109">Promote a variation</span></span>
<span data-ttu-id="a72d0-110">Kasutage kolmanda osapoole teenuses oleva eksperimendiga seotud andmeid ja analüüsi, et otsustada, millise variatsiooni tulemused olid parimad.</span><span class="sxs-lookup"><span data-stu-id="a72d0-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="a72d0-111">Seejärel saate seda reklaamida, asendades aktiivsel saidil oleva praeguse sisu parima variatsiooniga, et see oleks saadaval kõigile teie veebisaidi kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="a72d0-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="a72d0-112">Parima variatsiooni reklaamimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a72d0-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="a72d0-113">Valige Commerce'i saidiehitaja vasakpoolsel navigeerimispaanil **Eksperimendid** ja seejärel valige eksperiment.</span><span class="sxs-lookup"><span data-stu-id="a72d0-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="a72d0-114">Valige käsuribal **Eksperimendi lõpule viimine**.</span><span class="sxs-lookup"><span data-stu-id="a72d0-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="a72d0-115">Valige dialoogiboksis **Eksperimendi lõpule viimine** suvand **Vaata eksperimendi andmed läbi**.</span><span class="sxs-lookup"><span data-stu-id="a72d0-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="a72d0-116">Avaneb kolmanda osapoole teenus, kus saate mõõdikuid kontrollida ja teha kindlaks, milline variatsioon oli parim.</span><span class="sxs-lookup"><span data-stu-id="a72d0-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="a72d0-117">Valige dialoogiboksis **Eksperimendi lõpule viimine** parim variatsioon ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="a72d0-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="a72d0-118">Avage kolmanda osapoole teenus ja peatage eksperiment.</span><span class="sxs-lookup"><span data-stu-id="a72d0-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="a72d0-119">Valige saidiehitajas suvand **Lõpeta** , et kirjutada üle originaalne aktiivne leht ja avaldada parim variatsioon nii, et see on saadaval kõigile teie veebisaidi kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="a72d0-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="a72d0-120">Kui otsustate praegust aktiivset lehte säilitada ja variatsiooni mitte avaldada, valige **Avalda originaalne leht uuesti**.</span><span class="sxs-lookup"><span data-stu-id="a72d0-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="a72d0-121">Eksperimendi kustutamine</span><span class="sxs-lookup"><span data-stu-id="a72d0-121">Delete your experiment</span></span>
<span data-ttu-id="a72d0-122">Kuigi te ei pea lõpetatud eksperimenti rakenduses Commerce kustutama, võite selle kustutada, et säästa ruumi või puhastada oma tööruumi.</span><span class="sxs-lookup"><span data-stu-id="a72d0-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="a72d0-123">Eksperimendi kustutamiseks Commerce'i saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a72d0-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a72d0-124">Valige vasakpoolsel navigeerimispaanil **Eksperimendid** ja seejärel valige eksperiment.</span><span class="sxs-lookup"><span data-stu-id="a72d0-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="a72d0-125">Kui eksperiment on ikka aktiivne, peatage eksperiment enne jätkamist kolmanda osapoole teenuses.</span><span class="sxs-lookup"><span data-stu-id="a72d0-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="a72d0-126">Valige käsuribalt **Tühista avaldamine** , et eemaldada variatsiooni sisu aktiivselt saidilt.</span><span class="sxs-lookup"><span data-stu-id="a72d0-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="a72d0-127">Eksperimendi kustutamiseks valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="a72d0-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="a72d0-128">Eelmine etapp</span><span class="sxs-lookup"><span data-stu-id="a72d0-128">Previous step</span></span>
[<span data-ttu-id="a72d0-129">Katse käitamine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="a72d0-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
