---
title: Protsessimalli loomine Attractis
description: Selles teemas antakse teavet selle kohta, kuidas Attractis protsessimalli luua.
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 54c80f3d785ba7a7e0158c51201468f45796c193
ms.contentlocale: et-ee
ms.lasthandoff: 10/22/2018

---

# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="22e48-103">Protsessimalli loomine Attractis</span><span class="sxs-lookup"><span data-stu-id="22e48-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22e48-104">*Värbamisprotsessi mall* sisaldab kõiki tegevusi, mis peaksid olema tööle värbamise protsessi osad.</span><span class="sxs-lookup"><span data-stu-id="22e48-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="22e48-105">Selles teemas kirjeldatakse protsessimalli elemente rakenduses Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="22e48-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="22e48-106">Lisaks selgitatakse, kuidas malli luua.</span><span class="sxs-lookup"><span data-stu-id="22e48-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="22e48-107">Malli loomine on osa tervikliku värbamise lisamoodulist rakendusele Attract.</span><span class="sxs-lookup"><span data-stu-id="22e48-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="22e48-108">Mallihaldus</span><span class="sxs-lookup"><span data-stu-id="22e48-108">Template management</span></span>

<span data-ttu-id="22e48-109">Organisatsioonid saavad otsustada, kas Attractis saavad protsessimalle luua kõik töörühma liikmed või ainult administraatorid.</span><span class="sxs-lookup"><span data-stu-id="22e48-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="22e48-110">Mallihalduse konfigureerimiseks avage **Halduskeskus** \> **Mallihaldus**.</span><span class="sxs-lookup"><span data-stu-id="22e48-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="22e48-111">Selleks, et töörühma liikmed saaksid oma malle luua, lülitage sisse mallihaldus.</span><span class="sxs-lookup"><span data-stu-id="22e48-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="22e48-112">Kui te ei lülita mallihaldust sisse, saavad malle luua ainult administraatorid.</span><span class="sxs-lookup"><span data-stu-id="22e48-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="22e48-113">Vaikemall</span><span class="sxs-lookup"><span data-stu-id="22e48-113">Default template</span></span>

<span data-ttu-id="22e48-114">Vaikemalli saab määrata ainult adminisitraator.</span><span class="sxs-lookup"><span data-stu-id="22e48-114">Only admins can set the default template.</span></span> <span data-ttu-id="22e48-115">Vaikemalli kasutatakse siis kui töö loomisel on mall valimata.</span><span class="sxs-lookup"><span data-stu-id="22e48-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="22e48-116">Vaikemalli määramiseks avage **Halduskeskus** \> **Mallihaldus**.</span><span class="sxs-lookup"><span data-stu-id="22e48-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="22e48-117">Valige malli kaardil, mis peaks olema vaikemall, kolmikpunkti nupp (**...**) ja seejärel valige **Sea vaikeseadeks**.</span><span class="sxs-lookup"><span data-stu-id="22e48-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="22e48-118">Protsessimalli loomine</span><span class="sxs-lookup"><span data-stu-id="22e48-118">Create a process template</span></span>

<span data-ttu-id="22e48-119">Protsessimalle saavad luua administraatorid, värbajad ja personalijuhid.</span><span class="sxs-lookup"><span data-stu-id="22e48-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="22e48-120">Protsessimall koosneb *etappidest* ja *tegevustest*.</span><span class="sxs-lookup"><span data-stu-id="22e48-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="22e48-121">Etapid grupeerivad ühe või mitu tegevust.</span><span class="sxs-lookup"><span data-stu-id="22e48-121">Stages group together one or more activities.</span></span> <span data-ttu-id="22e48-122">Vaikimisi on igal protsessimallil potentsiaalse töövõtja, avalduse ja pakkumise tegevused.</span><span class="sxs-lookup"><span data-stu-id="22e48-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="22e48-123">Neid tegevusi sisaldavad etapid saab ümber nimetada.</span><span class="sxs-lookup"><span data-stu-id="22e48-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="22e48-124">Saate lisada rohkem etappe, valides **+ Uus etapp**.</span><span class="sxs-lookup"><span data-stu-id="22e48-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="22e48-125">Saate etappidele tegevusi lisada, pukseerides need sobivasse etappi või tehes neile tegevuste loendis topeltklõpsu.</span><span class="sxs-lookup"><span data-stu-id="22e48-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="22e48-126">Etapi nimed on kandidaatidele **Avalduse oleku** lehel näha.</span><span class="sxs-lookup"><span data-stu-id="22e48-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="22e48-127">Pidage seda etappidele nimede valimisel meeles.</span><span class="sxs-lookup"><span data-stu-id="22e48-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="22e48-128">Tegevuste kohta lisateabe saamiseks vt [Värbamisprotsessi tegevused Attractis](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="22e48-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="22e48-129">Värbamisprotsessi malli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="22e48-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="22e48-130">Avage **Mallid**.</span><span class="sxs-lookup"><span data-stu-id="22e48-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="22e48-131">Valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="22e48-131">Select **New**.</span></span>
3. <span data-ttu-id="22e48-132">Sisestage **Mallinime** väljale malli nimi ja seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="22e48-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="22e48-133">Valige **Kinnitusprotsessi valimise** loendist **Vaikimisi**, et tööle kinnitust nõuda.</span><span class="sxs-lookup"><span data-stu-id="22e48-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="22e48-134">Valige potentsiaalsete töövõtjate lubamiseks või keelamiseks.</span><span class="sxs-lookup"><span data-stu-id="22e48-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="22e48-135">Valikuline: etappide lisamine või eemaldamine.</span><span class="sxs-lookup"><span data-stu-id="22e48-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="22e48-136">Etapi lisamiseks valige **+ Uus etapp**.</span><span class="sxs-lookup"><span data-stu-id="22e48-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="22e48-137">Etapi eemaldamiseks hoidke kursorit etapi kohal ja valige seejärel ilmunud prügikastinupule.</span><span class="sxs-lookup"><span data-stu-id="22e48-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="22e48-138">Potentsiaalse töövõtja, Rakenduse ja Pakkumise etappe ei saa eemaldada, kuid need saab ümber nimetada.</span><span class="sxs-lookup"><span data-stu-id="22e48-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="22e48-139">Valikuline: tegevuste lisamine või eemaldamine.</span><span class="sxs-lookup"><span data-stu-id="22e48-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="22e48-140">Tegevuse lisamiseks lohistage see tegevuste loendist otse sobivasse etappi.</span><span class="sxs-lookup"><span data-stu-id="22e48-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="22e48-141">Teise võimalusena topeltklõpsake tegevusel ja valige etapp, kuhu see lisada.</span><span class="sxs-lookup"><span data-stu-id="22e48-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="22e48-142">Tegevuse eemaldamiseks laiendage seda ja seejärel valige prügikasti nupp tegevuse päises.</span><span class="sxs-lookup"><span data-stu-id="22e48-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="22e48-143">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="22e48-143">Select **Save**.</span></span>
