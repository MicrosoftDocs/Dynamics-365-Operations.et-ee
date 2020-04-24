---
title: Vara tootjad ja mudelid
description: Selles teemas selgitatakse, kuidas seadistada varade tootjaid ja seotud mudeleid varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2ef8a9afc007ce7e453f5e9cadfb912490545c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205111"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="331e9-103">Vara tootjad ja mudelid</span><span class="sxs-lookup"><span data-stu-id="331e9-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="331e9-104">Selles teemas selgitatakse, kuidas seadistada varade tootjaid ja seotud mudeleid varahalduses.</span><span class="sxs-lookup"><span data-stu-id="331e9-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="331e9-105">Mudelid võivad olla seotud varade tüüpidega.</span><span class="sxs-lookup"><span data-stu-id="331e9-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="331e9-106">Tooteseoste häälestamine</span><span class="sxs-lookup"><span data-stu-id="331e9-106">Set up product-model relations</span></span>

1. <span data-ttu-id="331e9-107">Valige **Varahaldus**\>**Häälestus**\>**Varad**\>**Tootja ja mudel**.</span><span class="sxs-lookup"><span data-stu-id="331e9-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="331e9-108">Valige uue toote loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="331e9-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="331e9-109">Väljale **Tootja** sisestage vara tootja nimi.</span><span class="sxs-lookup"><span data-stu-id="331e9-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="331e9-110">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="331e9-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="331e9-111">Kiirkaardil **Mudelid** valige **Lisa** varamudeli loomiseks, mis peaks olema seotud vara tootjaga.</span><span class="sxs-lookup"><span data-stu-id="331e9-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="331e9-112">Väljale **Mudel** sisestage vara mudeli nimi.</span><span class="sxs-lookup"><span data-stu-id="331e9-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="331e9-113">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="331e9-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="331e9-114">Väljal **Vara tüüp** valige vara tüüp, millega tootja mudel peaks seotud olema.</span><span class="sxs-lookup"><span data-stu-id="331e9-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="331e9-115">Samuti saate seadistada vara tüüpide, tootjate ja mudelite vahelisi seoseid otsingus **Vara tüübid**.</span><span class="sxs-lookup"><span data-stu-id="331e9-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="331e9-116">Lisateavet leiate teemast [Vara tüübid](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="331e9-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="331e9-117">Kiirkaardil **Üksikasjad** kuvatakse väljal **Mudelid** valitud vara tootja jaoks seadistatud vara mudelite arv.</span><span class="sxs-lookup"><span data-stu-id="331e9-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="331e9-118">Väljal **Varad** kuvatakse valitud tootja kasutavate varade arv.</span><span class="sxs-lookup"><span data-stu-id="331e9-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="331e9-119">Väljal **varad** kuvatakse valitud tootja kasutavate objektid arv.</span><span class="sxs-lookup"><span data-stu-id="331e9-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="331e9-120">Vara tüübil ei saa olla vara tootja mudeli seoste kogumeid, see võib olla seotud ühe vara tootja mudeliga või mitme vara tootja mudeliga.</span><span class="sxs-lookup"><span data-stu-id="331e9-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="331e9-121">Kui vara tüüp on seotud vähemalt ühe tootja mudeliga, saab nende varahalduse lehtedel valida ainult neid kombinatsioone, mis on sätestatud otsingus **Tootja mudel**, kus saab sätestada vara tüübi, tootja ja mudeli kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="331e9-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="331e9-122">Need leheküljed hõlmavad suvandeid **Kõik varad**, **Vara teenindustasemed**, **Töö tüübi vaikesätted** ja **Hoolduse eelarveread**.</span><span class="sxs-lookup"><span data-stu-id="331e9-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="331e9-123">Kui mõned vara tüübid ei ole seotud ühegi tootja mudeliga, kuvatakse lehtedel ainult need vara tüübid ja tootja mudelid, millel puudub seos vara tüüpidega.</span><span class="sxs-lookup"><span data-stu-id="331e9-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="331e9-124">Valige objektil tootja ja mudel</span><span class="sxs-lookup"><span data-stu-id="331e9-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="331e9-125">Valige **Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="331e9-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="331e9-126">Veerus **Vara** valige vara link.</span><span class="sxs-lookup"><span data-stu-id="331e9-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="331e9-127">Kuvatakse leht **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="331e9-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="331e9-128">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="331e9-128">Select **Edit**.</span></span>
4. <span data-ttu-id="331e9-129">Kiirkaardil **Üldine** valige väärtused väljadel **Tootja** ja **Mudel**.</span><span class="sxs-lookup"><span data-stu-id="331e9-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
