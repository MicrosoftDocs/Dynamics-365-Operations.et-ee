---
title: Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine
description: See teema kirjeldab, kuidas rakenduses Dynamics 365 Commerce edukat variatsiooni esile tõsta ja eksperimenti lõpule viia.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930176"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="cb5e7-103">Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="cb5e7-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="cb5e7-104">Selles teemas kirjeldatakse, kuidas tõsta esile variatsiooni, mis sai teie eksperimendis parima tulemuse, ja kuidas eksperimenti lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="cb5e7-105">Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="cb5e7-106">Täiendavad etapid on toodud eraldi teemades.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="cb5e7-107">[ ![Eksperimendi kasutaja teekond – ülevaatamine ja lõpetamine](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="cb5e7-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="cb5e7-108">Kui olete [oma eksperimendi käivitanud](experimentation-run-monitor.md) ja kogunud piisavalt andmeid, et määrata, millist variatsiooni te oma aktiivsel saidil kasutada soovite, tõstate variatsiooni esile ja lõpetate eksperimendi.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="cb5e7-109">Variatsiooni esiletõstmine</span><span class="sxs-lookup"><span data-stu-id="cb5e7-109">Promote a variation</span></span>
<span data-ttu-id="cb5e7-110">Kasutage kolmanda osapoole teenuses oleva eksperimendiga seotud andmeid ja analüüsi, et otsustada, millise variatsiooni tulemused olid parimad.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="cb5e7-111">Et asendada aktiivsel saidil olev praegune sisu parima variatsiooniga, et see oleks saadaval kõigile teie veebisaidi kasutajatele, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="cb5e7-112">Avage saidiehitajas vahekaart **Eksperimendid** ja valige eksperiment.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="cb5e7-113">Valige ülemisel ribal suvand **Lõpeta eksperiment**.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="cb5e7-114">Valige dialoogimenüüs **Eksperimendi lõpetamine** suvand **Vaata eksperimendi andmed läbi**.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="cb5e7-115">Avaneb kolmanda osapoole teenus, kus saate mõõdikuid kontrollida ja teha kindlaks, milline variatsioon oli parim.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="cb5e7-116">Valige saidiehitaja dialoogimenüüs **Eksperimendi lõpetamine** parim variatsioon ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="cb5e7-117">Avage kolmanda osapoole teenus ja peatage eksperiment.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="cb5e7-118">Valige saidiehitajas suvand **Lõpeta**, et kirjutada üle originaalne aktiivne leht ja avaldada parim variatsioon nii, et see on saadaval kõigile teie veebisaidi kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="cb5e7-119">Kui otsustate praegust aktiivset lehte säilitada ja variatsiooni mitte avaldada, valige **Avalda originaalne leht uuesti**.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="cb5e7-120">Eksperimendi kustutamine</span><span class="sxs-lookup"><span data-stu-id="cb5e7-120">Delete your experiment</span></span>
<span data-ttu-id="cb5e7-121">Kuigi te ei pea lõpetatud eksperimenti rakenduses Commerce kustutama, võite selle kustutada, et säästa ruumi või puhastada oma tööruumi.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="cb5e7-122">Eksperimendi kustutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="cb5e7-123">Avage saidiehitajas vahekaart **Eksperimendid** ja valige eksperiment.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="cb5e7-124">Kui eksperiment on ikka aktiivne, peatage eksperiment enne jätkamist kolmanda osapoole teenuses.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="cb5e7-125">Valige käsuribalt **Tühista avaldamine**, et eemaldada variatsiooni sisu aktiivselt saidilt.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="cb5e7-126">Valige käsuribalt **Kustuta**, et eksperiment kustutada.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="cb5e7-127">Eelmine etapp</span><span class="sxs-lookup"><span data-stu-id="cb5e7-127">Previous step</span></span>
[<span data-ttu-id="cb5e7-128">Eksperimendi käitamine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="cb5e7-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
