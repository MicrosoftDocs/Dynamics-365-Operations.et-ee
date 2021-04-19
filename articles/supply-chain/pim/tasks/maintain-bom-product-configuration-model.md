---
title: Toote konfiguratsioonimudeli koosluse haldamine
description: Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49aa17aa376f8536e9d2290292f877d314c2c078
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818009"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="5c012-103">Toote konfiguratsioonimudeli koosluse haldamine</span><span class="sxs-lookup"><span data-stu-id="5c012-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c012-104">Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit.</span><span class="sxs-lookup"><span data-stu-id="5c012-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="5c012-105">Tipptasemel kõlari mudelit demoettevõttes USMF kasutatakse selle protseduuri loomiseks.</span><span class="sxs-lookup"><span data-stu-id="5c012-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="5c012-106">Koosluse rea lisamine</span><span class="sxs-lookup"><span data-stu-id="5c012-106">Add a BOM line</span></span>
1. <span data-ttu-id="5c012-107">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="5c012-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="5c012-108">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="5c012-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="5c012-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5c012-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5c012-110">Valige selle protseduuri jaoks Tipptasemel kõlar.</span><span class="sxs-lookup"><span data-stu-id="5c012-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="5c012-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5c012-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5c012-112">Laiendage jaotist Koosluse read.</span><span class="sxs-lookup"><span data-stu-id="5c012-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="5c012-113">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5c012-113">Click Add.</span></span>
7. <span data-ttu-id="5c012-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5c012-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="5c012-115">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="5c012-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="5c012-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5c012-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="5c012-117">Koosluse rea üksikasjade lisamine</span><span class="sxs-lookup"><span data-stu-id="5c012-117">Add BOM line details</span></span>
1. <span data-ttu-id="5c012-118">Klõpsake valikut Koosluse rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="5c012-118">Click BOM line details.</span></span>
2. <span data-ttu-id="5c012-119">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="5c012-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="5c012-120">Näiteks võite valida kauba M0055.</span><span class="sxs-lookup"><span data-stu-id="5c012-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="5c012-121">Iga koosluse rea atribuudi puhul saab valida, kas see võtab endale fikseeritud väärtuse või see vastendatakse atribuudiga.</span><span class="sxs-lookup"><span data-stu-id="5c012-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="5c012-122">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="5c012-122">Select the Set check box.</span></span>
4. <span data-ttu-id="5c012-123">Tehke väljal Arvutus valik Jah.</span><span class="sxs-lookup"><span data-stu-id="5c012-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="5c012-124">Kui määrate arvutuse atribuudi väärtuseks Jah, lisatakse koosluse rida kuluarvutustesse.</span><span class="sxs-lookup"><span data-stu-id="5c012-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="5c012-125">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="5c012-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="5c012-126">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="5c012-126">Select the Set check box.</span></span>
7. <span data-ttu-id="5c012-127">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="5c012-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="5c012-128">Koguse väli määrab, kui palju kaupa kooslusse lisatakse.</span><span class="sxs-lookup"><span data-stu-id="5c012-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="5c012-129">See võib olla ilmne atribuudi vastendamise kandidaat.</span><span class="sxs-lookup"><span data-stu-id="5c012-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="5c012-130">Klõpsake vahekaarti Dimensioon.</span><span class="sxs-lookup"><span data-stu-id="5c012-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="5c012-131">Kontrollige, kas mõni tootedimensioon on aktiivne ja seetõttu peab sellele olema määratud väärtus või atribuut.</span><span class="sxs-lookup"><span data-stu-id="5c012-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="5c012-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5c012-132">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]