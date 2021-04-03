---
title: Koondplaanimine laoala ja laovarude jaoks, ladu ei ole kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena. Lao dimensioon ei ole kohustuslik.
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
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b1cd11cc62f551e43a04b9a8cc17bf7a7e961ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255585"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="3cf92-104">Koondplaanimine laoala ja laovarude jaoks, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="3cf92-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cf92-105">Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena.</span><span class="sxs-lookup"><span data-stu-id="3cf92-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="3cf92-106">Lao dimensioon ei ole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="3cf92-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="3cf92-107">See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.</span><span class="sxs-lookup"><span data-stu-id="3cf92-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="3cf92-108">Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.</span><span class="sxs-lookup"><span data-stu-id="3cf92-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="3cf92-109">Seda sätet ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="3cf92-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="3cf92-110">Lao dimensioon ei ole seatud kohustuslikuks.</span><span class="sxs-lookup"><span data-stu-id="3cf92-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="3cf92-111">Ladu võib olla teada, kuid seda ei kasutata koondplaneerimise arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="3cf92-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="3cf92-112">Laoala ja lao dimensioonid seadistatakse laovarude plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="3cf92-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="3cf92-113">Muidki dimensioone võib seadistada laovarude plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="3cf92-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="3cf92-114">Mitme laoala režiimi funktsioonid neid siiski ei mõjuta.</span><span class="sxs-lookup"><span data-stu-id="3cf92-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="3cf92-115">Järgmine graafik näitab, kuidas koondplaneerimine jätkub.</span><span class="sxs-lookup"><span data-stu-id="3cf92-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="3cf92-116">Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:</span><span class="sxs-lookup"><span data-stu-id="3cf92-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="3cf92-117">Ladu on seatud Käsitsi peale.</span><span class="sxs-lookup"><span data-stu-id="3cf92-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="3cf92-118">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="3cf92-119">Vaadake kiirkaardil **Koondplaneerimine** välja **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="3cf92-120">Kauba laovarud on kauba kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="3cf92-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="3cf92-121">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="3cf92-122">Valige kaup ja seejärel klõpsake Toimingupaanil vahekaardil **Plaan** valikut **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="3cf92-123">Taastäitmise suhted on laole määratud.</span><span class="sxs-lookup"><span data-stu-id="3cf92-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="3cf92-124">Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="3cf92-125">Vaadake kiirkaardil **Koondplaneerimine** väljagruppi **Pealadu**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="3cf92-126">Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban.</span><span class="sxs-lookup"><span data-stu-id="3cf92-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="3cf92-127">Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="3cf92-128">Valige kaup ja seejärel klõpsake Toimingupaani vahekaardil **Plaan** valikut **Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="3cf92-129">Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.</span><span class="sxs-lookup"><span data-stu-id="3cf92-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Nõude laoala ja laovarud, ladu pole    ](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="3cf92-131">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3cf92-131">Additional resources</span></span>
--------

[<span data-ttu-id="3cf92-132">Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="3cf92-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="3cf92-133">Koondplaanimine laovarude puhul, kohustuslik ladu</span><span class="sxs-lookup"><span data-stu-id="3cf92-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3cf92-134">Laoala ja lao katmise koondplaanimine, ladu on kohustuslik</span><span class="sxs-lookup"><span data-stu-id="3cf92-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="3cf92-135">Laoala ja lao katmise koondplaanimine, ladu ei ole kohustuslik</span><span class="sxs-lookup"><span data-stu-id="3cf92-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="3cf92-136">Koosluse versiooni määratlemine</span><span class="sxs-lookup"><span data-stu-id="3cf92-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]