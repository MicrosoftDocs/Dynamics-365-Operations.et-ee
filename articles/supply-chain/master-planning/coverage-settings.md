---
title: Laovarude sätted
description: Selles teemas on teave laovarude sätete kohta, mida Koondplaneerimises kasutatakse kaubavajaduse arvutamiseks.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538890"
---
# <a name="coverage-settings"></a><span data-ttu-id="16f2a-103">Laovarude sätted</span><span class="sxs-lookup"><span data-stu-id="16f2a-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16f2a-104">Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi.</span><span class="sxs-lookup"><span data-stu-id="16f2a-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="16f2a-105">saate määratleda laovarude sätteid mitmel viisil:</span><span class="sxs-lookup"><span data-stu-id="16f2a-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="16f2a-106">Määrake laovarude grupi laovarude sätted.</span><span class="sxs-lookup"><span data-stu-id="16f2a-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="16f2a-107">Saate luua laovarude grupi, mis sisaldab kõigi laovarude grupiga lingitud toodete sätteid.</span><span class="sxs-lookup"><span data-stu-id="16f2a-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="16f2a-108">Klõpsake laovarude grupi loomiseks valikuid **Koondplaneerimine &gt; Seadistus &gt; Laovarud &gt; Laovarude grupid**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="16f2a-109">Saate linkida tootega laovarude grupi.</span><span class="sxs-lookup"><span data-stu-id="16f2a-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="16f2a-110">Kui link on tegevuskoha-, lao- või tootedimensiooni kohane, kasutage lehel **Kauba laovarud** välja **Laovarude grupp**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="16f2a-111">Kui link on üldine olenemata tootedimensioonidest kasutage välja **Toote üksikasjad** kiirkaardi **Plaan** lehte **Laovarude grupp**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="16f2a-112">Kui te ei lingi laovarude gruppi tootega, kasutab koondplaneerimine vaikesättena suvandit Üldine laovarude grupp, mis on määratud lehel **Koondplaneerimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="16f2a-113">Määrake toote laovarude sätted.</span><span class="sxs-lookup"><span data-stu-id="16f2a-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="16f2a-114">Saate luua laovarude sätted kindlale tootele.</span><span class="sxs-lookup"><span data-stu-id="16f2a-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="16f2a-115">Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="16f2a-116">Valige toode ja klõpsake toimingupaanil vahekaardi **Plaan** jaotises **Laovarude** grupp valikut **Kauba laovarud**, et avada leht **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="16f2a-117">Kui toode on laovarude grupiga juba lingitud, saate laovarude grupi sätted tühistada, kasutades välja **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="16f2a-118">Laovarude sätted lehel**Kauba laovarud** alistavad lehel **Laovarude grupp** olevad sätted.</span><span class="sxs-lookup"><span data-stu-id="16f2a-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="16f2a-119">Määrake toote laovarude sätted viisardi abil.</span><span class="sxs-lookup"><span data-stu-id="16f2a-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="16f2a-120">Viisard juhendab teid sammhaaval läbi esmase kauba laovarude seadistamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="16f2a-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="16f2a-121">Klõpsake lehel **Kauba laovarud**, Toimingupaanil valige suvand **Viisard**, et avada leht **Kauba laovarude viisard**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="16f2a-122">Määrake dimensioonigrupi kaubavarude sätted.</span><span class="sxs-lookup"><span data-stu-id="16f2a-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="16f2a-123">Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="16f2a-124">Klõpsake lehe **Väljastatud toote üksikasjad** kiirkaardil **Üldine**, jaotises **Administreerimine** valige link **Laoala dimensioonigrupp**.</span><span class="sxs-lookup"><span data-stu-id="16f2a-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="16f2a-125">Valige lehel **Laoala dimensioonigrupid** märkeruut **Laovarude planeerimine dimensiooni järgi**, et luua laovarude sätted laoala dimensioonigrupi dimensiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="16f2a-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="16f2a-126">Kõigi tootedimensioonide, nagu konfiguratsioon, värv, suurus, stiil, puhul peab olema väli **Laovarude planeerimine dimensiooni järgi** valitud.</span><span class="sxs-lookup"><span data-stu-id="16f2a-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16f2a-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="16f2a-127">Additional resources</span></span>

[<span data-ttu-id="16f2a-128">Koondplaanid</span><span class="sxs-lookup"><span data-stu-id="16f2a-128">Master plans</span></span>](master-plans.md)
