---
title: Eksperimendi oleku ülevaatamine
description: Selles teemas selgitatakse, millises olekus on eksperiment oma elutsüklis rakenduses Dynamics 365 Commerce.
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
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930177"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="24263-103">Eksperimendi oleku ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="24263-103">Review the status of an experiment</span></span>
<span data-ttu-id="24263-104">Eksperimendi seadistamine ja käitamine rakenduses Dynamics 365 Commerce hõlmavad palju samme.</span><span class="sxs-lookup"><span data-stu-id="24263-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="24263-105">Lisateavet eksperimendi elutsükli kohta leiate teemast [Eksperimenteerimine rakenduses Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="24263-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="24263-106">Et saada teada, kus eksperiment elutsüklis on, avage saidiehitajas vahekaart **Eksperimendid**.</span><span class="sxs-lookup"><span data-stu-id="24263-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="24263-107">Kuvatakse loend eksperimentidest, mille olek on toodud nii rakenduses Commerce kui ka kolmanda osapoole teenuses, mida kasutatakse eksperimentide loomise lubamiseks, variatsioonide määramiseks ja andmete analüüsimiseks.</span><span class="sxs-lookup"><span data-stu-id="24263-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="24263-108">Veerus **Commerce'i olek** võidakse kuvada järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="24263-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="24263-109">**Mustand** – eksperiment on seotud lehe või fragmendiga rakenduses Commerce ning seda redigeeritakse.</span><span class="sxs-lookup"><span data-stu-id="24263-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="24263-110">**Avaldatud** – eksperimendi variatsioonid on teie veebisaidil kuvamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="24263-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="24263-111">Kui eksperimenti käitatakse kolmanda osapoole teenuses, näevad veebisaidi kasutajad lehe või fragmendi variatsiooni, mille valis kolmanda osapoole teenus.</span><span class="sxs-lookup"><span data-stu-id="24263-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="24263-112">**Avaldamata** – eksperiment ei ole enam teie veebisaidil saadaval.</span><span class="sxs-lookup"><span data-stu-id="24263-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="24263-113">Isegi kui eksperimenti käitatakse kolmanda osapoole teenuses, näevad veebisaidi kasutajad ainult lehe või fragmendi vaikeversiooni.</span><span class="sxs-lookup"><span data-stu-id="24263-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="24263-114">**Lõpetatud** – eksperiment on oma rada kulgenud ja variatsioon tõsteti kõigi veebisaidi kasutajate jaoks esile.</span><span class="sxs-lookup"><span data-stu-id="24263-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="24263-115">Sarnaselt võidakse veerus **kolmanda osapoole olek** kuvada järgmiseid väärtusi, et näidata, millises olekus on eksperimendid kolmanda osapoole teenuses.</span><span class="sxs-lookup"><span data-stu-id="24263-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="24263-116">**Mustand** – eksperiment on kolmanda osapoole teenuses seadistatud, kuid seda ei ole alustatud.</span><span class="sxs-lookup"><span data-stu-id="24263-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="24263-117">**Käitamine** – eksperiment käivitati kolmanda osapoole teenuses ja kogub andmeid.</span><span class="sxs-lookup"><span data-stu-id="24263-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="24263-118">**Peatatud** – eksperiment on peatatud ja andmeid ei koguta.</span><span class="sxs-lookup"><span data-stu-id="24263-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="24263-119">Uuesti andmete kogumiseks peate eksperimenti jätkama.</span><span class="sxs-lookup"><span data-stu-id="24263-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="24263-120">**Arhiivitud** – eksperiment on oma rada kulgenud ja salvestati kolmanda osapoole teenusesse hilisemaks vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="24263-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="24263-121">Allolevas diagrammis on toodud mõlemat olekute kogumid ja see, kuidas need üksteisega seotud on.</span><span class="sxs-lookup"><span data-stu-id="24263-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="24263-122">[ ![Eksperimenteerimise olekud](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="24263-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>