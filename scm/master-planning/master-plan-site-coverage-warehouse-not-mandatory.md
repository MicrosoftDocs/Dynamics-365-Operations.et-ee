---
title: Koondplaanimine laoala varudele, ladu ei ole kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena.
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 79582e92daeaf0afb032448d36be12edd0926089
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="964a0-103">Koondplaanimine laoala varudele, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="964a0-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="964a0-104">Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="964a0-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="964a0-105">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="964a0-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="964a0-106">Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="964a0-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="964a0-107">Lao dimensioon ei ole seatud kohustuslikuks.</span><span class="sxs-lookup"><span data-stu-id="964a0-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="964a0-108">Ladu võib olla teada, kuid seda ei kasutata koondplaneerimise arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="964a0-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="964a0-109">Saidi dimensioon on seadistatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="964a0-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="964a0-110">Lao dimensioon ei ole seadistatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="964a0-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="964a0-111">Seega on tarne ja nõudlus ning võibolla ka teised laovarude planeerimisega dimensioonid koondatud saitide kaupa.</span><span class="sxs-lookup"><span data-stu-id="964a0-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="964a0-112">Järgmine graafik näitab, kuidas koondplaneerimine jätkub.</span><span class="sxs-lookup"><span data-stu-id="964a0-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="964a0-113">Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:</span><span class="sxs-lookup"><span data-stu-id="964a0-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="964a0-114">Kauba laovarud on kauba kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="964a0-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="964a0-115">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="964a0-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="964a0-116">Valige kaup ja klõpsake siis valikuid **Plaan &gt; Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="964a0-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="964a0-117">Taastäitmise suhted on laole määratud.</span><span class="sxs-lookup"><span data-stu-id="964a0-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="964a0-118">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="964a0-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="964a0-119">Vaadake vahekaardil **Koondplaneerimine** väljagruppi **Pealadu**.</span><span class="sxs-lookup"><span data-stu-id="964a0-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="964a0-120">Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban.</span><span class="sxs-lookup"><span data-stu-id="964a0-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="964a0-121">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="964a0-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="964a0-122">Valige kaup ja klõpsake siis valikuid **Plaan &gt; Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="964a0-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="964a0-123">Vaadake vormi **Tellimuse vaikesätted** välja **Tellimuse vaiketüüp**.</span><span class="sxs-lookup"><span data-stu-id="964a0-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Nõue laoala varude laole pole kohustuslik](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a><span data-ttu-id="964a0-125">Vt ka</span><span class="sxs-lookup"><span data-stu-id="964a0-125">See also</span></span>
--------

[<span data-ttu-id="964a0-126">Koondplaanimine ja mitme laoala funktsioon</span><span class="sxs-lookup"><span data-stu-id="964a0-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="964a0-127">Koondplaneerimine – laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="964a0-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="964a0-128">Koondplaneerimine – laoala ja laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="964a0-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="964a0-129">Koondplaneerimine – laoala ja laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="964a0-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="964a0-130">Koondplaanimine – koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="964a0-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




