---
title: Ettevõttesisesed varad teenindamiseks
description: See teema kirjeldab, kuidas saate Microsoft Dynamics 365 Field Service kasutada nii kliendi kui ka majavarade hooldamiseks.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941410"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="73f5c-103">Ettevõttesisesed varad teenindamiseks</span><span class="sxs-lookup"><span data-stu-id="73f5c-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="73f5c-104">Microsoft Dynamics 365 Field Service on loodud kliendivarade teenindamiseks.</span><span class="sxs-lookup"><span data-stu-id="73f5c-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="73f5c-105">Dynamics 365 Supply Chain Managementi varahaldus on loodud ettevõttesiseste varade haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="73f5c-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="73f5c-106">Nende kahe rakenduse integreerimine võimaldab teil kasutada Field Service'it nii klientide kui ka ettevõttesiseste varade teenindamiseks.</span><span class="sxs-lookup"><span data-stu-id="73f5c-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="73f5c-107">Samuti saate varasid liigitada töö asukoha ja hierarhia järgi ning jälgida teenindust üksikasjalikul tasemel.</span><span class="sxs-lookup"><span data-stu-id="73f5c-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="73f5c-108">Lisateavet vaadake teemast [Dynamics 365 Field Service'i ja Supply Chain Managementi integreerimine](/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="73f5c-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="73f5c-109">Mallid</span><span class="sxs-lookup"><span data-stu-id="73f5c-109">Templates</span></span>

<span data-ttu-id="73f5c-110">Ettevõttesisesed varad sisaldavad põhiliste tabelikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="73f5c-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="73f5c-111">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="73f5c-111">Finance and Operations apps</span></span> | <span data-ttu-id="73f5c-112">Mudeljuhitud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="73f5c-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="73f5c-113">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="73f5c-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="73f5c-114">Varahalduse vara töötsükli mudelid</span><span class="sxs-lookup"><span data-stu-id="73f5c-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="73f5c-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="73f5c-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="73f5c-116">Varahalduse vara töötsükli olekud</span><span class="sxs-lookup"><span data-stu-id="73f5c-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="73f5c-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="73f5c-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="73f5c-118">Varahalduse varad</span><span class="sxs-lookup"><span data-stu-id="73f5c-118">Asset management assets</span></span> | <span data-ttu-id="73f5c-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="73f5c-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="73f5c-120">Varahalduse varade tüübid</span><span class="sxs-lookup"><span data-stu-id="73f5c-120">Asset management asset types</span></span> | <span data-ttu-id="73f5c-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="73f5c-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="73f5c-122">Varahalduse töö asukoha töötsükli mudelid</span><span class="sxs-lookup"><span data-stu-id="73f5c-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="73f5c-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="73f5c-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="73f5c-124">Varahalduse töö asukoha töötsükli olekud</span><span class="sxs-lookup"><span data-stu-id="73f5c-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="73f5c-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="73f5c-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="73f5c-126">Varahalduse töö asukohad</span><span class="sxs-lookup"><span data-stu-id="73f5c-126">Asset management functional locations</span></span> | <span data-ttu-id="73f5c-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="73f5c-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="73f5c-128">Varahalduse töö asukohtade tüübid</span><span class="sxs-lookup"><span data-stu-id="73f5c-128">Asset management functional location types</span></span> | <span data-ttu-id="73f5c-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="73f5c-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="73f5c-130">Varahalduse tootjad</span><span class="sxs-lookup"><span data-stu-id="73f5c-130">Asset management manufacturers</span></span> | <span data-ttu-id="73f5c-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="73f5c-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="73f5c-132">Varahalduse mudelid</span><span class="sxs-lookup"><span data-stu-id="73f5c-132">Asset management models</span></span> | <span data-ttu-id="73f5c-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="73f5c-133">msdyn\_models</span></span> | |
| <span data-ttu-id="73f5c-134">Varahalduse garantii</span><span class="sxs-lookup"><span data-stu-id="73f5c-134">Asset management warranty</span></span> | <span data-ttu-id="73f5c-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="73f5c-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]