---
title: Uue laopaigutuse loomine
description: Selles teemas kirjeldatakse, kuidas seadistada lao asukohtade teavet.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399c87c2e5ad26d5ccc1618cfb6520de3fcdc644
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145659"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="dad7e-103">Uue laopaigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="dad7e-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dad7e-104">Selles teemas kirjeldatakse, kuidas seadistada lao asukohtade teavet.</span><span class="sxs-lookup"><span data-stu-id="dad7e-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="dad7e-105">See rakendub ainult ladudele, mis on loodud, kasutades üldist ladustamist moodulis Varude haldus, mitte nendele ladudele, mis on loodud moodulis Laohaldus.</span><span class="sxs-lookup"><span data-stu-id="dad7e-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="dad7e-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="dad7e-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="dad7e-107">Määrake asukoha vaikemahutavus</span><span class="sxs-lookup"><span data-stu-id="dad7e-107">Set the default location capacity</span></span>
1. <span data-ttu-id="dad7e-108">Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Ladu > Varude ja laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="dad7e-109">Valige vahekaart **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="dad7e-110">Väljale **Standardlaius** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="dad7e-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="dad7e-111">Väljale **Standardmaht** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="dad7e-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="dad7e-112">Väljale **Standardkõrgus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="dad7e-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="dad7e-113">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-113">Select **Save**.</span></span>
7. <span data-ttu-id="dad7e-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dad7e-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="dad7e-115">Asukoha nime vormingu määratlemine</span><span class="sxs-lookup"><span data-stu-id="dad7e-115">Define the location name format</span></span>
1. <span data-ttu-id="dad7e-116">Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Laovarude jaotamine > Laod**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="dad7e-117">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-117">Select **New**.</span></span>
3. <span data-ttu-id="dad7e-118">Sisestage väärtus väljale **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="dad7e-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="dad7e-120">Väljal **Sait** valige otsingust soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="dad7e-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="dad7e-121">Lülituge ümber jaotise **Asukohanimed** laiendusele.</span><span class="sxs-lookup"><span data-stu-id="dad7e-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="dad7e-122">Selle jaotise suvandites saate määratleda asukohanimede vaikevormingu.</span><span class="sxs-lookup"><span data-stu-id="dad7e-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="dad7e-123">Selles näites on kasutatud riiulirea, sektsiooni ja riiuli numbrit.</span><span class="sxs-lookup"><span data-stu-id="dad7e-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="dad7e-124">Määrake suvandi **Kaasa riiulirida** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="dad7e-125">Määrake suvandi **Kaasa sektsioon** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="dad7e-126">Sisestage sektsioonile väärtus väljal **Vorming**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="dad7e-127">Määrake suvandi **Kaasa riiul** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="dad7e-128">Sisestage riiulile väärtus väljal **Vorming**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="dad7e-129">Lao asukohtade määratlemine</span><span class="sxs-lookup"><span data-stu-id="dad7e-129">Define warehouse locations</span></span>
1. <span data-ttu-id="dad7e-130">Toimingupaanil valige **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="dad7e-131">Valige **Asukohaviisard**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="dad7e-132">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-132">Select **Next**.</span></span>
4. <span data-ttu-id="dad7e-133">Tühistage suvandi **Lähetusalad** valik.</span><span class="sxs-lookup"><span data-stu-id="dad7e-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="dad7e-134">Tühistage suvandi **Partii asukohad** valik.</span><span class="sxs-lookup"><span data-stu-id="dad7e-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="dad7e-135">Valige **Järgmine** kuni jõuate suvandini **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="dad7e-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="dad7e-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dad7e-136">Close the page.</span></span>
8. <span data-ttu-id="dad7e-137">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="dad7e-137">Refresh the page.</span></span>

