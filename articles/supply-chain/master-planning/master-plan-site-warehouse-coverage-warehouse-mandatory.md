---
title: Koondplaanimine laoala ja laovarude jaoks, ladu on kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena. Lao dimensioon on kohustuslik.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c52fc9955afe2a7502d0e1f9e7cdfc5b89bbb31d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559274"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="aa859-104">Koondplaanimine laoala ja laovarude jaoks, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="aa859-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa859-105">Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="aa859-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="aa859-106">Lao dimensioon on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="aa859-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="aa859-107">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="aa859-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="aa859-108">Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="aa859-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="aa859-109">Lao dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="aa859-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="aa859-110">Laoala ja lao dimensioonid seadistatakse laovarude plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="aa859-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="aa859-111">Muidki dimensioone võib seadistada laovarude plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="aa859-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="aa859-112">Mitme laoala režiimi funktsioonid neid siiski ei mõjuta.</span><span class="sxs-lookup"><span data-stu-id="aa859-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="aa859-113">Järgmine graafik näitab, kuidas koondplaneerimine jätkub.</span><span class="sxs-lookup"><span data-stu-id="aa859-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="aa859-114">Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:</span><span class="sxs-lookup"><span data-stu-id="aa859-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="aa859-115">Ladu on seatud **Käsitsi** peale.</span><span class="sxs-lookup"><span data-stu-id="aa859-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="aa859-116">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="aa859-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="aa859-117">Vaadake kiirkaardil **Koondplaneerimine** välja **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="aa859-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="aa859-118">Kauba laovarud on kauba kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="aa859-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="aa859-119">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="aa859-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="aa859-120">Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="aa859-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="aa859-121">Taastäitmise suhted on laole määratud.</span><span class="sxs-lookup"><span data-stu-id="aa859-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="aa859-122">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="aa859-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="aa859-123">Vaadake kiirkaardil **Koondplaneerimine** väljagruppi **Pealadu**.</span><span class="sxs-lookup"><span data-stu-id="aa859-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="aa859-124">Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban.</span><span class="sxs-lookup"><span data-stu-id="aa859-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="aa859-125">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="aa859-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="aa859-126">Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="aa859-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="aa859-127">Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.</span><span class="sxs-lookup"><span data-stu-id="aa859-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Nõude laoala ja laovarud, ladu kohustuslik](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="aa859-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="aa859-129">Additional resources</span></span>
--------

[<span data-ttu-id="aa859-130">Koondplaneerimine ja mitme laoala režiim</span><span class="sxs-lookup"><span data-stu-id="aa859-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="aa859-131">Koondplaneerimine – laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="aa859-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="aa859-132">Koondplaneerimine – laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="aa859-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="aa859-133">Koondplaneerimine – laoala ja laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="aa859-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="aa859-134">Koondplaneerimine – koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="aa859-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



