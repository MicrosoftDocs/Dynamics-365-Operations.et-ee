---
title: Eksperimendi seadistamine
description: Selles teemas kirjeldatakse, kuidas seadistada eksperimenti kolmanda osapoole teenuses.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 1a60eb459d6d6f710e43ac5418b9375420ca8387
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000776"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="26cef-103">Eksperimendi seadistamine</span><span class="sxs-lookup"><span data-stu-id="26cef-103">Set up an experiment</span></span>

<span data-ttu-id="26cef-104">Pärast [hüpoteesi määratlemist ja eksperimendi edumõõdikute kindlaks määramist](experimentation-identify.md) peate oma eksperimendi seadistama kolmanda osapoole teenuses.</span><span class="sxs-lookup"><span data-stu-id="26cef-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="26cef-105">Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="26cef-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="26cef-106">Täiendavad etapid on toodud eraldi teemades.</span><span class="sxs-lookup"><span data-stu-id="26cef-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="26cef-107">[ ![Eksperimendi kasutaja teekond – seadistamine](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="26cef-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="26cef-108">Eksperimendi seadistamine kolmanda osapoole teenuses</span><span class="sxs-lookup"><span data-stu-id="26cef-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="26cef-109">Nüüdseks peaks teil olema valitud kolmanda osapoole teenus oma eksperimendi käitamiseks ja jälgimiseks ning eksperimendi konnektori seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="26cef-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="26cef-110">Need eeltingimused on loetletud teemas [Eksperimenteerimine rakenduses Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="26cef-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="26cef-111">Järgige samme, mis on vajalikud eksperimendi loomiseks kolmanda osapoole teenuses.</span><span class="sxs-lookup"><span data-stu-id="26cef-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="26cef-112">Kui konnektor on õigesti konfigureeritud, siis kuvatakse kolmanda osapoole teenuses seadistatud eksperimentide täielik loend Commerce'i saidiehitajas umbes viie minuti jooksul.</span><span class="sxs-lookup"><span data-stu-id="26cef-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="26cef-113">Edumõõdikute seadistamine</span><span class="sxs-lookup"><span data-stu-id="26cef-113">Set up your success metrics</span></span>
<span data-ttu-id="26cef-114">Iga eksperiment vajab mõõdikuid variatsioonide mõju mõõtmiseks ja hüpoteesi kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="26cef-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="26cef-115">Järgige alltoodud samme, et lubada mõõdikute arvutamine kolmanda osapoole teenuses, kasutades reaalajas telemeetriasündmusi rakendusest Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="26cef-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="26cef-116">Edumõõdikute häälestamiseks järgige neid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="26cef-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="26cef-117">Valige Commerce'i saidiehitajas vasakpoolselt navigeerimispaanilt vahekaart **Lehed** ja seejärel valige leht, mille jaoks soovite mõõdikuid koguda.</span><span class="sxs-lookup"><span data-stu-id="26cef-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="26cef-118">Avage jaotis **Jälgitavad sündmuse ID-d** jälgitava lehe või mooduli parempoolselt atribuudipaanilt.</span><span class="sxs-lookup"><span data-stu-id="26cef-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="26cef-119">Valige suvand **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="26cef-119">Select **View**.</span></span> <span data-ttu-id="26cef-120">Kuvatakse kõigi sündmuse ID-de loend.</span><span class="sxs-lookup"><span data-stu-id="26cef-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="26cef-121">Kopeerige sündmus, mida soovite jälgida, ja kleepige sündmusevõti selleks mõeldud kohta kolmanda osapoole teenuses.</span><span class="sxs-lookup"><span data-stu-id="26cef-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="26cef-122">Kui vajate rohkem kui üht sündmust, kopeerige võtmed ükshaaval.</span><span class="sxs-lookup"><span data-stu-id="26cef-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="26cef-123">Teavet selle kohta, kuidas vaadata kõiki saadaolevaid sündmusi ja atribuute, sh lehevaatamisi ja tulu, leiate teemast [Commerce'i komponentide sündmused diagnostika ja tõrkeotsingu jaoks](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="26cef-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="26cef-124">Kui kolmanda osapoole teenuses on vaja mõõdikute jälgimiseks veel midagi teha, tehke seda.</span><span class="sxs-lookup"><span data-stu-id="26cef-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="26cef-125">Eelmine etapp</span><span class="sxs-lookup"><span data-stu-id="26cef-125">Previous step</span></span>
[<span data-ttu-id="26cef-126">Hüpoteesi tuvastamine ja eksperimendi mõõdikute määramine</span><span class="sxs-lookup"><span data-stu-id="26cef-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="26cef-127">Järgmine etapp</span><span class="sxs-lookup"><span data-stu-id="26cef-127">Next step</span></span>
[<span data-ttu-id="26cef-128">Eksperimendi ühendamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="26cef-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
