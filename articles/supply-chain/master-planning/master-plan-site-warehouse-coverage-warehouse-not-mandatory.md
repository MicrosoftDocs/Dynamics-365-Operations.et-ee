---
title: Koondplaanimine laoala ja laovarude jaoks, ladu ei ole kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena. Lao dimensioon ei ole kohustuslik.
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
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1073f4d41b9fd4c37e2a079e2718869056a86252
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="26b36-104">Koondplaanimine laoala ja laovarude jaoks, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="26b36-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26b36-105">Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="26b36-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="26b36-106">Lao dimensioon ei ole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="26b36-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="26b36-107">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="26b36-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="26b36-108">Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="26b36-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="26b36-109">Seda sätet ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="26b36-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="26b36-110">Lao dimensioon ei ole seatud kohustuslikuks.</span><span class="sxs-lookup"><span data-stu-id="26b36-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="26b36-111">Ladu võib olla teada, kuid seda ei kasutata koondplaneerimise arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="26b36-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="26b36-112">Laoala ja lao dimensioonid seadistatakse laovarude plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="26b36-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="26b36-113">Muidki dimensioone võib seadistada laovarude plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="26b36-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="26b36-114">Mitme laoala režiimi funktsioonid neid siiski ei mõjuta.</span><span class="sxs-lookup"><span data-stu-id="26b36-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="26b36-115">Järgmine graafik näitab, kuidas koondplaneerimine jätkub.</span><span class="sxs-lookup"><span data-stu-id="26b36-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="26b36-116">Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:</span><span class="sxs-lookup"><span data-stu-id="26b36-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="26b36-117">Ladu on seatud Käsitsi peale.</span><span class="sxs-lookup"><span data-stu-id="26b36-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="26b36-118">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="26b36-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="26b36-119">Vaadake kiirkaardil **Koondplaneerimine** välja **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="26b36-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="26b36-120">Kauba laovarud on kauba kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="26b36-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="26b36-121">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="26b36-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="26b36-122">Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="26b36-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="26b36-123">Taastäitmise suhted on laole määratud.</span><span class="sxs-lookup"><span data-stu-id="26b36-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="26b36-124">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="26b36-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="26b36-125">Vaadake kiirkaardil **Koondplaneerimine** väljagruppi **Pealadu**.</span><span class="sxs-lookup"><span data-stu-id="26b36-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="26b36-126">Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban.</span><span class="sxs-lookup"><span data-stu-id="26b36-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="26b36-127">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="26b36-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="26b36-128">Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="26b36-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="26b36-129">Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.</span><span class="sxs-lookup"><span data-stu-id="26b36-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Nõude laoala ja laovarud, ladu pole    ](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)


-



<a name="additional-resources"></a><span data-ttu-id="26b36-131">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="26b36-131">Additional resources</span></span>
--------

[<span data-ttu-id="26b36-132">Koondplaneerimine ja mitme laoala režiim</span><span class="sxs-lookup"><span data-stu-id="26b36-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="26b36-133">Koondplaneerimine – laoala ja laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="26b36-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="26b36-134">Koondplaneerimine – laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="26b36-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="26b36-135">Koondplaneerimine – laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="26b36-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="26b36-136">Koondplaneerimine – koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="26b36-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




