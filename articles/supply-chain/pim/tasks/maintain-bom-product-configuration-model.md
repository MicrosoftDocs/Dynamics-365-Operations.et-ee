---
title: Toote konfiguratsioonimudeli koosluse haldamine
description: Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457aa5720919d8455a3099b200980bb36f60577f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "342381"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="9dc10-103">Toote konfiguratsioonimudeli koosluse haldamine</span><span class="sxs-lookup"><span data-stu-id="9dc10-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9dc10-104">Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit.</span><span class="sxs-lookup"><span data-stu-id="9dc10-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="9dc10-105">Tipptasemel kõlari mudelit demoettevõttes USMF kasutatakse selle protseduuri loomiseks.</span><span class="sxs-lookup"><span data-stu-id="9dc10-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="9dc10-106">Koosluse rea lisamine</span><span class="sxs-lookup"><span data-stu-id="9dc10-106">Add a BOM line</span></span>
1. <span data-ttu-id="9dc10-107">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="9dc10-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="9dc10-108">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="9dc10-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="9dc10-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9dc10-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9dc10-110">Valige selle protseduuri jaoks Tipptasemel kõlar.</span><span class="sxs-lookup"><span data-stu-id="9dc10-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="9dc10-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9dc10-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9dc10-112">Laiendage jaotist Koosluse read.</span><span class="sxs-lookup"><span data-stu-id="9dc10-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="9dc10-113">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9dc10-113">Click Add.</span></span>
7. <span data-ttu-id="9dc10-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9dc10-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="9dc10-115">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="9dc10-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="9dc10-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9dc10-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="9dc10-117">Koosluse rea üksikasjade lisamine</span><span class="sxs-lookup"><span data-stu-id="9dc10-117">Add BOM line details</span></span>
1. <span data-ttu-id="9dc10-118">Klõpsake valikut Koosluse rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="9dc10-118">Click BOM line details.</span></span>
2. <span data-ttu-id="9dc10-119">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="9dc10-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9dc10-120">Näiteks võite valida kauba M0055.</span><span class="sxs-lookup"><span data-stu-id="9dc10-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="9dc10-121">Iga koosluse rea atribuudi puhul saab valida, kas see võtab endale fikseeritud väärtuse või see vastendatakse atribuudiga.</span><span class="sxs-lookup"><span data-stu-id="9dc10-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="9dc10-122">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="9dc10-122">Select the Set check box.</span></span>
4. <span data-ttu-id="9dc10-123">Tehke väljal Arvutus valik Jah.</span><span class="sxs-lookup"><span data-stu-id="9dc10-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="9dc10-124">Kui määrate arvutuse atribuudi väärtuseks Jah, lisatakse koosluse rida kuluarvutustesse.</span><span class="sxs-lookup"><span data-stu-id="9dc10-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="9dc10-125">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="9dc10-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="9dc10-126">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="9dc10-126">Select the Set check box.</span></span>
7. <span data-ttu-id="9dc10-127">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="9dc10-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9dc10-128">Koguse väli määrab, kui palju kaupa kooslusse lisatakse.</span><span class="sxs-lookup"><span data-stu-id="9dc10-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="9dc10-129">See võib olla ilmne atribuudi vastendamise kandidaat.</span><span class="sxs-lookup"><span data-stu-id="9dc10-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="9dc10-130">Klõpsake vahekaarti Dimensioon.</span><span class="sxs-lookup"><span data-stu-id="9dc10-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="9dc10-131">Kontrollige, kas mõni tootedimensioon on aktiivne ja seetõttu peab sellele olema määratud väärtus või atribuut.</span><span class="sxs-lookup"><span data-stu-id="9dc10-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="9dc10-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9dc10-132">Click OK.</span></span>

