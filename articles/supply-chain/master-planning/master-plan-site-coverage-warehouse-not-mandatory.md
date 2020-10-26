---
title: Koondplaanimine laoala varudele, ladu ei ole kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f4cde5c570148ca58c4ea583a8f538a72d4957d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987042"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="0608d-103">Koondplaanimine laoala varudele, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="0608d-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0608d-104">Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="0608d-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="0608d-105">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="0608d-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="0608d-106">Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="0608d-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="0608d-107">Lao dimensioon ei ole seatud kohustuslikuks.</span><span class="sxs-lookup"><span data-stu-id="0608d-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="0608d-108">Ladu võib olla teada, kuid seda ei kasutata koondplaneerimise arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="0608d-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="0608d-109">Saidi dimensioon on seadistatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="0608d-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="0608d-110">Lao dimensioon ei ole seadistatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="0608d-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="0608d-111">Seega on tarne ja nõudlus ning võibolla ka teised laovarude planeerimisega dimensioonid koondatud saitide kaupa.</span><span class="sxs-lookup"><span data-stu-id="0608d-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="0608d-112">Järgmine graafik näitab, kuidas koondplaneerimine jätkub.</span><span class="sxs-lookup"><span data-stu-id="0608d-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="0608d-113">Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:</span><span class="sxs-lookup"><span data-stu-id="0608d-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="0608d-114">Kauba laovarud on kauba kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="0608d-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="0608d-115">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="0608d-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="0608d-116">Valige kaup ja klõpsake siis valikuid **Plaan &gt; Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="0608d-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="0608d-117">Taastäitmise suhted on laole määratud.</span><span class="sxs-lookup"><span data-stu-id="0608d-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="0608d-118">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="0608d-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="0608d-119">Vaadake vahekaardil **Koondplaneerimine** väljagruppi **Pealadu**.</span><span class="sxs-lookup"><span data-stu-id="0608d-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="0608d-120">Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban.</span><span class="sxs-lookup"><span data-stu-id="0608d-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="0608d-121">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="0608d-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="0608d-122">Valige kaup ja klõpsake siis valikuid **Plaan &gt; Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="0608d-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="0608d-123">Vaadake vormi **Tellimuse vaikesätted** välja **Tellimuse vaiketüüp**.</span><span class="sxs-lookup"><span data-stu-id="0608d-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Nõue laoala varude laole pole kohustuslik](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="0608d-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0608d-125">Additional resources</span></span>
--------

[<span data-ttu-id="0608d-126">Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="0608d-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="0608d-127">Laoala ja lao katmise koondplaanimine, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="0608d-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="0608d-128">Koondplaanimine laovarude puhul, kohustuslik ladu</span><span class="sxs-lookup"><span data-stu-id="0608d-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="0608d-129">Koondplaanimine laovarude puhul, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="0608d-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="0608d-130">Koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="0608d-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



