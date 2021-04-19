---
title: Eksperimendi eelversioon ja avaldamine
description: Selles teemas kirjeldatakse, kuidas vaadata rakendusest Dynamics 365 Commerce pärit eksperimendi eelversiooni ja seda avaldada.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 52ca23e5aaeb7058853fed2241d5804180fa7f8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798959"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="ed472-103">Eksperimendi eelversioon ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="ed472-103">Preview and publish an experiment</span></span>

<span data-ttu-id="ed472-104">Selles teemas kirjeldatakse, kuidas vaadata rakenduses Dynamics 365 Commerce oma eksperimendi eelversiooni ning seda avaldada pärast seda, kui olete [oma eksperimendi ühendanud ja oma variatsioone redigeerinud](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="ed472-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="ed472-105">Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ed472-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ed472-106">Täiendavad etapid on toodud eraldi teemades.</span><span class="sxs-lookup"><span data-stu-id="ed472-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="ed472-107">[ ![Eksperimendi kasutaja teekond – eelversioon ja avaldamine](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ed472-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="ed472-108">Eksperimendi variatsioonide eelversiooni vaatamine</span><span class="sxs-lookup"><span data-stu-id="ed472-108">Preview your experiment variations</span></span>
<span data-ttu-id="ed472-109">Saate vaadata oma variatsioonide eelversiooni ja jätkata nende redigeerimist, kuni need näevad välja nii, nagu te tahate.</span><span class="sxs-lookup"><span data-stu-id="ed472-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="ed472-110">Oma eksperimendi variatsioonide eelversiooni kuvamiseks Commerce'i saidiehitajaga, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ed472-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ed472-111">Valige saidiehitajas käsuriba all asuvast variatsioonide rippmenüüst sisu, mille eelversiooni te kuvada soovite.</span><span class="sxs-lookup"><span data-stu-id="ed472-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="ed472-112">Klõpsake käsuribal käsul **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="ed472-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="ed472-113">Kuvatakse eelversioon sellest, kuidas sisu avaldamise korral välja näeks.</span><span class="sxs-lookup"><span data-stu-id="ed472-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="ed472-114">Teistsuguse variatsiooni eelversiooni kuvamiseks valige see variatsioonide rippmenüüst ning valige uuesti **Eelversioon**.</span><span class="sxs-lookup"><span data-stu-id="ed472-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="ed472-115">Eksperimendi avaldamine</span><span class="sxs-lookup"><span data-stu-id="ed472-115">Publish your experiment</span></span>
<span data-ttu-id="ed472-116">Kui te ei kasuta avaldamisrühma, et ajastada seda, millal teie eksperiment kasutusele võetakse, ja soovite selle kohe avaldada, valige käsuribal suvand **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="ed472-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="ed472-117">Avaldatakse kõik eksperimenti kuuluvad variatsioonid.</span><span class="sxs-lookup"><span data-stu-id="ed472-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="ed472-118">Kui lehel on avaldamata URL, peate esmalt URL-i avaldama, muidu ei ole see teie veebisaidi kasutajatele nähtav.</span><span class="sxs-lookup"><span data-stu-id="ed472-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="ed472-119">Üksikasjad leiate teemast [Lehe salvestamine, eelversioon ja avaldamine](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="ed472-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="ed472-120">Avaldamisrühmade kasutamine eksperimendi kasutuselevõtu ajastamiseks</span><span class="sxs-lookup"><span data-stu-id="ed472-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="ed472-121">Saidiehitajas loodud variatsioonide avaldamist saab ajastada avaldamisrühma kaudu.</span><span class="sxs-lookup"><span data-stu-id="ed472-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="ed472-122">Saate avaldamisrühma kaudu ühendada oma eksperimendiga lehe või fragmendi, valides vasakpoolsel navigeerimispaanil **Eksperimendid**.</span><span class="sxs-lookup"><span data-stu-id="ed472-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="ed472-123">Samuti saate teha seda, kui valite **Lehed** või **Fragmendid** ja järgite juhiseid jaotises [Eksperimendi ühendamine ja variatsioonide redigeerimine](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="ed472-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="ed472-124">Lisateavet avaldamisrühmade kohta leiate teemast [Avaldamisrühmadega töötamine](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="ed472-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="ed472-125">Kui kasutate eksperimentidega koos avaldamisrühmi, tuleb arvestada mõnda olulist asja.</span><span class="sxs-lookup"><span data-stu-id="ed472-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="ed472-126">Kui lisate avaldamisrühma lehe või fragmendi, milles on aktiivne eksperiment, eemaldatakse eksperiment avaldamisrühmas lehelt või fragmendist.</span><span class="sxs-lookup"><span data-stu-id="ed472-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="ed472-127">Eksperimendid, mis on ühendatud aktiivse saidi lehtedega, ei ole avaldamisrühma lehtedele kättesaadavad ning sama kehtib vastupidi.</span><span class="sxs-lookup"><span data-stu-id="ed472-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="ed472-128">Samamoodi ei ole aktiivse saidi lehed, millel on aktiivsed eksperimendid, kättesaadavad muudele avaldamisrühmades olevatele eksperimentidele ning sama kehtib vastupidi.</span><span class="sxs-lookup"><span data-stu-id="ed472-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="ed472-129">Kui avaldate või ajastate avaldamisrühma, avaldatakse kogu rühmas olev sisu hoolimata sellest, kas avaldamisrühmaga on seotud mõni eksperiment.</span><span class="sxs-lookup"><span data-stu-id="ed472-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="ed472-130">Kuna avaldamisrühm jääb alles ka pärast selle avaldamist aktiivsel saidil, jäävad alles ka avaldamisrühmas olevad eksperimendid.</span><span class="sxs-lookup"><span data-stu-id="ed472-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="ed472-131">Seetõttu ei saa te sama lehe või fragmendiga teisi eksperimente seostada.</span><span class="sxs-lookup"><span data-stu-id="ed472-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="ed472-132">Selle piirangu vältimiseks kustutage kõik avaldamisrühmad, mis sisaldavad eksperimente.</span><span class="sxs-lookup"><span data-stu-id="ed472-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="ed472-133">Kui soovite kustutada aktiivselt saidilt eksperimendi, mis sisaldub ka avaldamisrühmas, kustutage see esmalt avaldamisrühmast.</span><span class="sxs-lookup"><span data-stu-id="ed472-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="ed472-134">Eelmine etapp</span><span class="sxs-lookup"><span data-stu-id="ed472-134">Previous step</span></span>
[<span data-ttu-id="ed472-135">Eksperimendi ühendamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="ed472-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="ed472-136">Järgmine etapp</span><span class="sxs-lookup"><span data-stu-id="ed472-136">Next step</span></span>
[<span data-ttu-id="ed472-137">Eksperimendi käitamine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="ed472-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]