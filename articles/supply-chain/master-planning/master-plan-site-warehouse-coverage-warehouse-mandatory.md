---
title: Koondplaanimine laoala ja laovarude jaoks, ladu on kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena. Lao dimensioon on kohustuslik.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f500f163a731264b8f2e5e61c094dc7887cea752
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="23b5a-104">Koondplaanimine laoala ja laovarude jaoks, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="23b5a-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="23b5a-105">Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="23b5a-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="23b5a-106">Lao dimensioon on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="23b5a-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="23b5a-107">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="23b5a-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="23b5a-108">Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="23b5a-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="23b5a-109">Lao dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="23b5a-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="23b5a-110">Laoala ja lao dimensioonid seadistatakse laovarude plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="23b5a-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="23b5a-111">Muidki dimensioone võib seadistada laovarude plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="23b5a-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="23b5a-112">Mitme laoala režiimi funktsioonid neid siiski ei mõjuta.</span><span class="sxs-lookup"><span data-stu-id="23b5a-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="23b5a-113">Järgmine graafik näitab, kuidas koondplaneerimine jätkub.</span><span class="sxs-lookup"><span data-stu-id="23b5a-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="23b5a-114">Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:</span><span class="sxs-lookup"><span data-stu-id="23b5a-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="23b5a-115">Ladu on seatud **Käsitsi** peale.</span><span class="sxs-lookup"><span data-stu-id="23b5a-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="23b5a-116">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="23b5a-117">Vaadake kiirkaardil **Koondplaneerimine** välja **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="23b5a-118">Kauba laovarud on kauba kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="23b5a-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="23b5a-119">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="23b5a-120">Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="23b5a-121">Taastäitmise suhted on laole määratud.</span><span class="sxs-lookup"><span data-stu-id="23b5a-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="23b5a-122">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="23b5a-123">Vaadake kiirkaardil **Koondplaneerimine** väljagruppi **Pealadu**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="23b5a-124">Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban.</span><span class="sxs-lookup"><span data-stu-id="23b5a-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="23b5a-125">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="23b5a-126">Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="23b5a-127">Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.</span><span class="sxs-lookup"><span data-stu-id="23b5a-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Nõude laoala ja laovarud, ladu kohustuslik](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="23b5a-129">Vt ka</span><span class="sxs-lookup"><span data-stu-id="23b5a-129">See also</span></span>
--------

[<span data-ttu-id="23b5a-130">Koondplaanimine ja mitme laoala funktsioon</span><span class="sxs-lookup"><span data-stu-id="23b5a-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="23b5a-131">Koondplaneerimine – laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="23b5a-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="23b5a-132">Koondplaneerimine – laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="23b5a-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="23b5a-133">Koondplaneerimine – laoala ja laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="23b5a-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="23b5a-134">Koondplaneerimine – koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="23b5a-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




