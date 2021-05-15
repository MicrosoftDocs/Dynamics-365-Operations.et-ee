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
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921313"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="8bc0f-103">Toote konfiguratsioonimudeli koosluse haldamine</span><span class="sxs-lookup"><span data-stu-id="8bc0f-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8bc0f-104">Selle protseduuri käitamine nõuab olemasolevat toote konfiguratsioonimudelit.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="8bc0f-105">Tipptasemel kõlari mudelit demoettevõttes USMF kasutatakse selle protseduuri loomiseks.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="8bc0f-106">Koosluse rea lisamine</span><span class="sxs-lookup"><span data-stu-id="8bc0f-106">Add a BOM line</span></span>

1. <span data-ttu-id="8bc0f-107">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="8bc0f-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8bc0f-109">Valige selle protseduuri jaoks Tipptasemel kõlar.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="8bc0f-110">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="8bc0f-111">Laiendage jaotist **Koosluse read**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="8bc0f-112">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-112">Select **Add**.</span></span>
1. <span data-ttu-id="8bc0f-113">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="8bc0f-114">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="8bc0f-115">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="8bc0f-116">Koosluse rea üksikasjade lisamine</span><span class="sxs-lookup"><span data-stu-id="8bc0f-116">Add BOM line details</span></span>

1. <span data-ttu-id="8bc0f-117">Valige **koosluse rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="8bc0f-118">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="8bc0f-119">Näiteks võite valida kauba M0055.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="8bc0f-120">Iga koosluse rea atribuudi puhul saab valida, kas see võtab endale fikseeritud väärtuse või see vastendatakse atribuudiga.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="8bc0f-121">Märkige ruut **Määra**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="8bc0f-122">Valige suvand *Jah* väljal **Kalkulatsioon**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="8bc0f-123">Kui määrate atribuudi **Arvutus** väärtuseks *Jah*, lisatakse koosluse rida kuluarvutustesse.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="8bc0f-124">Valige vahekaart **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="8bc0f-125">Märkige ruut **Määra**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="8bc0f-126">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="8bc0f-127">Koguse väli määrab, kui palju kaupa kooslusse lisatakse.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="8bc0f-128">See võib olla ilmne atribuudi vastendamise kandidaat.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="8bc0f-129">Valige vahekaart **Mõõtmed**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="8bc0f-130">Kontrollige, kas mõni tootedimensioon on aktiivne ja seetõttu peab sellele olema määratud väärtus või atribuut.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="8bc0f-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bc0f-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]