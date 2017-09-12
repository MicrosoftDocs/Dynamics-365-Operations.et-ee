--- 
title: Toote konfiguratsioonimudeli koosluse haldamine
description: "Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 380e902f9c8266f583e44fa7ea643dc5d5ab52d3
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="09f39-103">Toote konfiguratsioonimudeli koosluse haldamine</span><span class="sxs-lookup"><span data-stu-id="09f39-103">Maintain BOM for a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09f39-104">Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit.</span><span class="sxs-lookup"><span data-stu-id="09f39-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="09f39-105">Tipptasemel kõlari mudelit demoettevõttes USMF kasutatakse selle protseduuri loomiseks.</span><span class="sxs-lookup"><span data-stu-id="09f39-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="09f39-106">Koosluse rea lisamine</span><span class="sxs-lookup"><span data-stu-id="09f39-106">Add a BOM line</span></span>
1. <span data-ttu-id="09f39-107">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="09f39-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="09f39-108">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="09f39-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="09f39-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="09f39-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="09f39-110">Valige selle protseduuri jaoks Tipptasemel kõlar.</span><span class="sxs-lookup"><span data-stu-id="09f39-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="09f39-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="09f39-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="09f39-112">Laiendage jaotist Koosluse read.</span><span class="sxs-lookup"><span data-stu-id="09f39-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="09f39-113">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="09f39-113">Click Add.</span></span>
7. <span data-ttu-id="09f39-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="09f39-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="09f39-115">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="09f39-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="09f39-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="09f39-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="09f39-117">Koosluse rea üksikasjade lisamine</span><span class="sxs-lookup"><span data-stu-id="09f39-117">Add BOM line details</span></span>
1. <span data-ttu-id="09f39-118">Klõpsake valikut Koosluse rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="09f39-118">Click BOM line details.</span></span>
2. <span data-ttu-id="09f39-119">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="09f39-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="09f39-120">Näiteks võite valida kauba M0055.</span><span class="sxs-lookup"><span data-stu-id="09f39-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="09f39-121">Iga koosluse rea atribuudi puhul saab valida, kas see võtab endale fikseeritud väärtuse või see vastendatakse atribuudiga.</span><span class="sxs-lookup"><span data-stu-id="09f39-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="09f39-122">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="09f39-122">Select the Set check box.</span></span>
4. <span data-ttu-id="09f39-123">Tehke väljal Arvutus valik Jah.</span><span class="sxs-lookup"><span data-stu-id="09f39-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="09f39-124">Kui määrate arvutuse atribuudi väärtuseks Jah, lisatakse koosluse rida kuluarvutustesse.</span><span class="sxs-lookup"><span data-stu-id="09f39-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="09f39-125">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="09f39-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="09f39-126">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="09f39-126">Select the Set check box.</span></span>
7. <span data-ttu-id="09f39-127">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="09f39-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="09f39-128">Koguse väli määrab, kui palju kaupa kooslusse lisatakse.</span><span class="sxs-lookup"><span data-stu-id="09f39-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="09f39-129">See võib olla ilmne atribuudi vastendamise kandidaat.</span><span class="sxs-lookup"><span data-stu-id="09f39-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="09f39-130">Klõpsake vahekaarti Dimensioon.</span><span class="sxs-lookup"><span data-stu-id="09f39-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="09f39-131">Kontrollige, kas mõni tootedimensioon on aktiivne ja seetõttu peab sellele olema määratud väärtus või atribuut.</span><span class="sxs-lookup"><span data-stu-id="09f39-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="09f39-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="09f39-132">Click OK.</span></span>


