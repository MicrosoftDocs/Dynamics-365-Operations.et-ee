---
title: Koondplaanimine laovarude puhul, kohustuslik ladu
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena. Ladu on kohustuslik dimensioon.
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b1890f14351734c26952511f6245efe4cce5f3e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987138"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="04ad0-104">Koondplaanimine laovarude puhul, kohustuslik ladu</span><span class="sxs-lookup"><span data-stu-id="04ad0-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04ad0-105">Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="04ad0-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="04ad0-106">Ladu on kohustuslik dimensioon.</span><span class="sxs-lookup"><span data-stu-id="04ad0-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="04ad0-107">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="04ad0-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="04ad0-108">Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="04ad0-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="04ad0-109">Seda sätet ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="04ad0-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="04ad0-110">Lao dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="04ad0-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="04ad0-111">Saidi dimensioon on seadistatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="04ad0-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="04ad0-112">Ka teised dimensioonid võivad olla seatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="04ad0-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="04ad0-113">Mitmesaidiline funktsioon siiski neid ei mõjuta.</span><span class="sxs-lookup"><span data-stu-id="04ad0-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="04ad0-114">Lao dimensioon ei ole seadistatud laovarude planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="04ad0-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="04ad0-115">Seega on tarne ja nõudlus ning võibolla ka teised laovarude planeerimisega dimensioonid koondatud saitide kaupa.</span><span class="sxs-lookup"><span data-stu-id="04ad0-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="04ad0-116">Järgmine graafik näitab, kuidas koondplaneerimine jätkub.</span><span class="sxs-lookup"><span data-stu-id="04ad0-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="04ad0-117">Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:</span><span class="sxs-lookup"><span data-stu-id="04ad0-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="04ad0-118">Kauba laovarud on kauba kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="04ad0-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="04ad0-119">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="04ad0-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="04ad0-120">Valige kaup ja klõpsake siis valikuid **Plaan &gt; Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="04ad0-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="04ad0-121">Taastäitmise suhted on laole määratud.</span><span class="sxs-lookup"><span data-stu-id="04ad0-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="04ad0-122">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="04ad0-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="04ad0-123">Vaadake vahekaardil **Koondplaneerimine** väljagruppi **Pealadu**.</span><span class="sxs-lookup"><span data-stu-id="04ad0-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="04ad0-124">Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban.</span><span class="sxs-lookup"><span data-stu-id="04ad0-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="04ad0-125">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="04ad0-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="04ad0-126">Valige kaup ja klõpsake siis valikuid **Plaan &gt; Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="04ad0-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="04ad0-127">Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.</span><span class="sxs-lookup"><span data-stu-id="04ad0-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Nõue laoala varude laole kohustuslik](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="04ad0-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="04ad0-129">Additional resources</span></span>
--------

[<span data-ttu-id="04ad0-130">Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="04ad0-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="04ad0-131">Laoala ja lao katmise koondplaanimine, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="04ad0-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="04ad0-132">Koondplaanimine laovarude puhul, kohustuslik ladu</span><span class="sxs-lookup"><span data-stu-id="04ad0-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="04ad0-133">Laoala ja lao katmise koondplaanimine, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="04ad0-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="04ad0-134">Koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="04ad0-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



