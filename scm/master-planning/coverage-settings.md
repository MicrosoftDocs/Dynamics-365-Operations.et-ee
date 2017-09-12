---
title: "Laovarude sätted"
description: "Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fb11a470d98a9742749daaac3244a5bb0d3a689c
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="d5223-103">Laovarude sätted</span><span class="sxs-lookup"><span data-stu-id="d5223-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d5223-104">Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi.</span><span class="sxs-lookup"><span data-stu-id="d5223-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="d5223-105">saate määratleda laovarude sätteid mitmel viisil:</span><span class="sxs-lookup"><span data-stu-id="d5223-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="d5223-106">Määrake laovarude grupi laovarude sätted.</span><span class="sxs-lookup"><span data-stu-id="d5223-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="d5223-107">Saate luua laovarude grupi, mis sisaldab kõigi laovarude grupiga lingitud toodete sätteid.</span><span class="sxs-lookup"><span data-stu-id="d5223-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="d5223-108">Klõpsake laovarude grupi loomiseks valikuid **Koondplaneerimine &gt; Seadistus &gt; Laovarud &gt; Laovarude grupid**.</span><span class="sxs-lookup"><span data-stu-id="d5223-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="d5223-109">Saate linkida tootega laovarude grupi.</span><span class="sxs-lookup"><span data-stu-id="d5223-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="d5223-110">Kui link on tegevuskoha-, lao- või tootedimensiooni kohane, kasutage lehel **Kauba laovarud** välja **Laovarude grupp**.</span><span class="sxs-lookup"><span data-stu-id="d5223-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="d5223-111">Kui link on üldine olenemata tootedimensioonidest kasutage lehe **Toote üksikasjad** kiirkaardi **Plaan** lehte **Laovarude grupp**.</span><span class="sxs-lookup"><span data-stu-id="d5223-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="d5223-112">Kui te ei lingi laovarude gruppi tootega, kasutab koondplaneerimine suvandit **Üldine laovarude grupp**, mis on määratud lehel **Koondplaneerimise parameetrid** vaikesättena.</span><span class="sxs-lookup"><span data-stu-id="d5223-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="d5223-113">Määrake toote laovarude sätted.</span><span class="sxs-lookup"><span data-stu-id="d5223-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="d5223-114">Saate luua laovarude sätted kindlale tootele.</span><span class="sxs-lookup"><span data-stu-id="d5223-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="d5223-115">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="d5223-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="d5223-116">Valige toode ja klõpsake **toimingupaanil** vahekaardi **Plaan** jaotises **Laovarude grupp** valikut **Kauba laovarud**, et avada leht **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="d5223-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="d5223-117">Kui toode on laovarude grupiga juba lingitud, saate laovarude grupi sätted tühistada, kasutades välja **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="d5223-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="d5223-118">Laovarude sätted lehel**Kauba laovarud** alistavad lehel **Laovarude grupp** olevad sätted.</span><span class="sxs-lookup"><span data-stu-id="d5223-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="d5223-119">Määrake toote laovarude sätted viisardi abil.</span><span class="sxs-lookup"><span data-stu-id="d5223-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="d5223-120">Viisard on etapiviisiline juhend, mis aitab teil häälestada esmaseid kauba laovarude parameetreid.</span><span class="sxs-lookup"><span data-stu-id="d5223-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="d5223-121">Klõpsake lehel **Kauba laovarud** suvandit **Viisard**, et avada leht **Kauba laovarude viisard**.</span><span class="sxs-lookup"><span data-stu-id="d5223-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="d5223-122">Määrake dimensioonigrupi kaubavarude sätted.</span><span class="sxs-lookup"><span data-stu-id="d5223-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="d5223-123">Klõpsake valikuid **Tooteteabe haldus &gt; Üldine &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="d5223-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="d5223-124">Klõpsake lehe **Väljastatud toote üksikasjad** vahekaardil **Üldine** grupis **Administreerimine** linki **Laoala dimensioonigrupp**.</span><span class="sxs-lookup"><span data-stu-id="d5223-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="d5223-125">Valige lehel **Laoala dimensioonigrupp** väli **Laovarude planeerimine dimensiooni järgi**, et luua laovarude sätted laoala dimensioonigrupi dimensiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="d5223-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="d5223-126">Kõigi tootedimensioonide, nagu konfiguratsioon, värv, suurus, stiil, puhul peab olema väli **Laovarude planeerimine dimensiooni järgi** valitud.</span><span class="sxs-lookup"><span data-stu-id="d5223-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="d5223-127">Vt ka</span><span class="sxs-lookup"><span data-stu-id="d5223-127">See also</span></span>
--------

[<span data-ttu-id="d5223-128">Koondplaanid</span><span class="sxs-lookup"><span data-stu-id="d5223-128">Master plans</span></span>](master-plans.md)




