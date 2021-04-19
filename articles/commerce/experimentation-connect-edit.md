---
title: Eksperimendi ühendamine ja variatsioonide redigeerimine
description: Selles teemas kirjeldatakse, kuidas ühendada kolmanda osapoole teenuses olev eksperiment rakendusega Dynamics 365 Commerce ja redigeerida eksperimendi variatsioone.
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
ms.openlocfilehash: 4c9c9463162f21cdaf40f1c4ed6d5ae51e97cb88
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799079"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="cefd6-103">Eksperimendi ühendamine ja variatsioonide redigeerimine</span><span class="sxs-lookup"><span data-stu-id="cefd6-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="cefd6-104">Selles teemas kirjeldatakse, kuidas ühendada oma eksperiment rakenduses Commerce ning variatsioone muuta, et need ühtiks teie hüpoteesiga.</span><span class="sxs-lookup"><span data-stu-id="cefd6-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="cefd6-105">Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cefd6-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="cefd6-106">Täiendavad etapid on toodud eraldi teemades.</span><span class="sxs-lookup"><span data-stu-id="cefd6-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="cefd6-107">[ ![Eksperimendi kasutaja teekond – ühendamine ja redigeerimine](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="cefd6-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="cefd6-108">Kui olete kolmanda osapoole teenuses [oma eksperimendi seadistanud](experimentation-setup.md), ühendate eksperimendi rakendusega Dynamics 365 Commerce ja redigeerite eksperimendi variatsioone.</span><span class="sxs-lookup"><span data-stu-id="cefd6-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="cefd6-109">Plaanimine</span><span class="sxs-lookup"><span data-stu-id="cefd6-109">Planning considerations</span></span>

<span data-ttu-id="cefd6-110">Enne kui ühendate oma eksperimendi rakenduses Commerce, peate tegema mõne otsuse, mis mõjutavad seda, kuidas Commerce teie sisu haldab.</span><span class="sxs-lookup"><span data-stu-id="cefd6-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="cefd6-111">Oma eksperimendi ulatuse määratlemine</span><span class="sxs-lookup"><span data-stu-id="cefd6-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="cefd6-112">Eksperimendi ühendamisel palutakse teil määratleda eksperimendi ulatus.</span><span class="sxs-lookup"><span data-stu-id="cefd6-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="cefd6-113">Eksperimentide ulatus võib olla **osaline** või **terve**.</span><span class="sxs-lookup"><span data-stu-id="cefd6-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="cefd6-114">Valige **osaline**, kui soovite teha eksperimenti lehe kindla osa põhjal.</span><span class="sxs-lookup"><span data-stu-id="cefd6-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="cefd6-115">Selle suvandi valimisel peate määrama, millised moodulid eksperimenti kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="cefd6-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="cefd6-116">Eksperimendiga mitteseotud vaikelehe või fragmendi osade muudatused sünkroonitakse automaatselt kõikides variatsioonides.</span><span class="sxs-lookup"><span data-stu-id="cefd6-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="cefd6-117">Valige **terve**, kui soovite eksperimendis kasutada tervet lehte või fragmenti.</span><span class="sxs-lookup"><span data-stu-id="cefd6-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="cefd6-118">Luuakse vaikelehe või fragmendi eraldi koopiad.</span><span class="sxs-lookup"><span data-stu-id="cefd6-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="cefd6-119">Te ei pea valima, millised moodulid on eksperimenti kaasatud, kuna kogu redigeerimispind on muutmiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="cefd6-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="cefd6-120">Saate mooduleid lisada, kustutada või järjekorda seada nii, nagu on vaja.</span><span class="sxs-lookup"><span data-stu-id="cefd6-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="cefd6-121">Kui aga muudetakse eksperimendiga seotud vaikelehte või fragmenti, tuleb need muudatused kõigis variatsioonides käsitsi sünkroonida.</span><span class="sxs-lookup"><span data-stu-id="cefd6-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="cefd6-122">Kui seostate oma eksperimendi lehega, mis kasutab paigutust, saate määrata eksperimendi ulatuseks ainult **terve**.</span><span class="sxs-lookup"><span data-stu-id="cefd6-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="cefd6-123">Otsustamine, kas soovite ajastada seda, millal teie eksperiment avaldatakse</span><span class="sxs-lookup"><span data-stu-id="cefd6-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="cefd6-124">Kui soovite ajastada seda, millal teie eksperiment aktiivsel saidil avaldatakse, veenduge *enne* eksperimendi ühendamist, et eksperimendiga seostatav sisu on saadaval avaldamisrühmas.</span><span class="sxs-lookup"><span data-stu-id="cefd6-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="cefd6-125">Lisateavet avaldamisrühmade kohta leiate teemast [Avaldamisrühmadega töötamine](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="cefd6-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="cefd6-126">Eksperimendi ühendamine</span><span class="sxs-lookup"><span data-stu-id="cefd6-126">Connect your experiment</span></span>
<span data-ttu-id="cefd6-127">Oma eksperimendi ühendamiseks käivitate viisardi **Eksperimendi ühendamine**.</span><span class="sxs-lookup"><span data-stu-id="cefd6-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="cefd6-128">Viisardist leiate oma eksperimendi ühendamiseks vajalikud sammud.</span><span class="sxs-lookup"><span data-stu-id="cefd6-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="cefd6-129">Kui viisard on lõpule jõudnud, on teie eksperiment ühendatud ja luuakse muudatused, mis on redigeerimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="cefd6-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="cefd6-130">Oma eksperimendi ühendamise alustamiseks Commerce'i saidiehitajaga, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cefd6-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cefd6-131">Viisardi **Eksperimendi ühendamine** käivitamiseks valige vasakpoolselt paanilt **Eksperimendid** ja seejärel valige **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="cefd6-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="cefd6-132">Teine võimalus viisardile juurde pääsemiseks lehe või fragmendi redaktori kaudu, on selle redigeerimine ja suvandi **Eksperimendi ühendamine** valimine käsureal.</span><span class="sxs-lookup"><span data-stu-id="cefd6-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cefd6-133">Lehe saab korraga ühendada ainult ühe eksperimendiga.</span><span class="sxs-lookup"><span data-stu-id="cefd6-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="cefd6-134">Lehe ühendamiseks teise eksperimendiga kustutage esiteks see eksperiment, millega leht on praegu ühendatud.</span><span class="sxs-lookup"><span data-stu-id="cefd6-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="cefd6-135">Valige leht või fragment, mida soovite eksperimendis kasutada.</span><span class="sxs-lookup"><span data-stu-id="cefd6-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="cefd6-136">Seadistage eksperimendi ulatus **osaliseks** või **terveks**, lähtudes valikust, mille tegite ülaltoodud jaotises [Oma eksperimendi ulatuse määratlemine](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="cefd6-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="cefd6-137">Funktsiooni **Lehtede või fragmentide kasutamine eksperimentides** lipp peab olema lubatud, kui soovite eksperimendis kasutada tervet lehte või fragmenti.</span><span class="sxs-lookup"><span data-stu-id="cefd6-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="cefd6-138">Lisateavet leiate teemast [Eksperimenteerimine rakenduses Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cefd6-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="cefd6-139">Viisardi viimases etapis valige **Loo variatsioonid ja välju viisardist**.</span><span class="sxs-lookup"><span data-stu-id="cefd6-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="cefd6-140">Eksperimendi jaoks luuakse variatsioonid.</span><span class="sxs-lookup"><span data-stu-id="cefd6-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="cefd6-141">Variatsioonide redigeerimine</span><span class="sxs-lookup"><span data-stu-id="cefd6-141">Edit your variations</span></span>
<span data-ttu-id="cefd6-142">Viisardist väljumisel luuakse teie jaoks variatsioonid.</span><span class="sxs-lookup"><span data-stu-id="cefd6-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="cefd6-143">Seejärel redigeerige variatsioone nii, et need peegeldaksid valikuid, mida te peate eksperimendi hüpoteesis kontrollima.</span><span class="sxs-lookup"><span data-stu-id="cefd6-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="cefd6-144">Valige üks järgmistest meetoditest, mis vastab teie eksperimendi ulatusele, mille valisite ülaltoodud teemas [Oma eksperimendi ulatuse määratlemine](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="cefd6-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="cefd6-145">Variatsioonide redigeerimine osalise ulatusega eksperimentide puhul</span><span class="sxs-lookup"><span data-stu-id="cefd6-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="cefd6-146">Kui määrasite viisardis **Eksperimendi ühendamine** oma eksperimendi ulatuseks **osaline**, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cefd6-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="cefd6-147">Kasutage redaktoris käsuriba all asuvat variatsioonide rippmenüüd, et redigeerida iga variatsiooni oma algse hüpoteesi alusel.</span><span class="sxs-lookup"><span data-stu-id="cefd6-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="cefd6-148">Samuti võite tahta luua kontroll- või baasvariatsiooni, jättes ühe variatsiooni muutmata.</span><span class="sxs-lookup"><span data-stu-id="cefd6-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="cefd6-149">Valige moodul, mida eksperimendis kasutada, valige kolmikpunkt (...) ja seejärel valige **Lisa eksperimendile**.</span><span class="sxs-lookup"><span data-stu-id="cefd6-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="cefd6-150">Variatsioonide redigeerimine täisulatusega eksperimentide puhul</span><span class="sxs-lookup"><span data-stu-id="cefd6-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="cefd6-151">Kui määrasite viisardis **Eksperimendi ühendamine** oma eksperimendi ulatuseks **terve**, kasutage käsuriba all olevat variatsioonide rippmenüüd, et redigeerida iga variatsiooni algse hüpoteesi alusel.</span><span class="sxs-lookup"><span data-stu-id="cefd6-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="cefd6-152">Mõlemal juhul võite tahta ka luua kontroll- või baasvariatsiooni, jättes ühe variatsiooni muutmata.</span><span class="sxs-lookup"><span data-stu-id="cefd6-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="cefd6-153">Eelmine etapp</span><span class="sxs-lookup"><span data-stu-id="cefd6-153">Previous step</span></span>
[<span data-ttu-id="cefd6-154">Eksperimendi seadistamine</span><span class="sxs-lookup"><span data-stu-id="cefd6-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="cefd6-155">Järgmine etapp</span><span class="sxs-lookup"><span data-stu-id="cefd6-155">Next step</span></span>
[<span data-ttu-id="cefd6-156">Eksperimendi eelversioon ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="cefd6-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]