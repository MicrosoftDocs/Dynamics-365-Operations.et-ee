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
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0b97f5f9a9a1447027e55d6c6b30253506caff70
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="b94ff-103">Koondplaanimine laoala varudele, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="b94ff-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b94ff-104">Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="b94ff-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="b94ff-105">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="b94ff-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b94ff-106">Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="b94ff-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b94ff-107">Lao dimensioon ei ole seatud kohustuslikuks.</span><span class="sxs-lookup"><span data-stu-id="b94ff-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="b94ff-108">Ladu võib olla teada, kuid seda ei kasutata koondplaneerimise arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="b94ff-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="b94ff-109">Saidi dimensioon on seadistatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b94ff-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="b94ff-110">Lao dimensioon ei ole seadistatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b94ff-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="b94ff-111">Seega on tarne ja nõudlus ning võibolla ka teised laovarude planeerimisega dimensioonid koondatud saitide kaupa.</span><span class="sxs-lookup"><span data-stu-id="b94ff-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="b94ff-112">Järgmine graafik näitab, kuidas koondplaneerimine jätkub.</span><span class="sxs-lookup"><span data-stu-id="b94ff-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="b94ff-113">Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:</span><span class="sxs-lookup"><span data-stu-id="b94ff-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="b94ff-114">Kauba laovarud on kauba kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="b94ff-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="b94ff-115">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="b94ff-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b94ff-116">Valige kaup ja klõpsake siis valikuid **Plaan &gt; Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="b94ff-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="b94ff-117">Taastäitmise suhted on laole määratud.</span><span class="sxs-lookup"><span data-stu-id="b94ff-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="b94ff-118">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="b94ff-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b94ff-119">Vaadake vahekaardil **Koondplaneerimine** väljagruppi **Pealadu**.</span><span class="sxs-lookup"><span data-stu-id="b94ff-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="b94ff-120">Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban.</span><span class="sxs-lookup"><span data-stu-id="b94ff-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="b94ff-121">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="b94ff-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b94ff-122">Valige kaup ja klõpsake siis valikuid **Plaan &gt; Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="b94ff-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="b94ff-123">Vaadake vormi **Tellimuse vaikesätted** välja **Tellimuse vaiketüüp**.</span><span class="sxs-lookup"><span data-stu-id="b94ff-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Nõue laoala varude laole pole kohustuslik](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="b94ff-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b94ff-125">Additional resources</span></span>
--------

[<span data-ttu-id="b94ff-126">Koondplaneerimine ja mitme laoala režiim</span><span class="sxs-lookup"><span data-stu-id="b94ff-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="b94ff-127">Koondplaneerimine – laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="b94ff-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b94ff-128">Koondplaneerimine – laoala ja laovarud, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="b94ff-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b94ff-129">Koondplaneerimine – laoala ja laovarud, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="b94ff-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b94ff-130">Koondplaanimine – koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="b94ff-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




