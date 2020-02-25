---
title: Integreeritu kohad ja laod
description: Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni rakenduse Finance and Operations ja teenuse Common Data Service vahel.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 0f5ed58ad50df49250aa4c001401ff52d460dfa6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019735"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="7b62c-103">Integreeritud kohad ja laod</span><span class="sxs-lookup"><span data-stu-id="7b62c-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="7b62c-104">Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni rakenduse Finance and Operations ja teenuse Common Data Service vahel.</span><span class="sxs-lookup"><span data-stu-id="7b62c-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="7b62c-105">Tegevuskohad ja laod on rakenduses Supply Chain Management levinud kontseptsioonid.</span><span class="sxs-lookup"><span data-stu-id="7b62c-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="7b62c-106">Neid kasutatakse ettevõtte tarneahela modelleerimiseks.</span><span class="sxs-lookup"><span data-stu-id="7b62c-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="7b62c-107">Mallid</span><span class="sxs-lookup"><span data-stu-id="7b62c-107">Templates</span></span>

<span data-ttu-id="7b62c-108">Common Data Service’iga integreerimisega on need kontseptsioonid ja kogu asjakohane teave saadaval Common Data Service’is järgmises tabelis olevate kohtade ning ladude üksuste kaudu.</span><span class="sxs-lookup"><span data-stu-id="7b62c-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="7b62c-109">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="7b62c-109">Finance and Operations apps</span></span> | <span data-ttu-id="7b62c-110">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="7b62c-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="7b62c-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="7b62c-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="7b62c-112">Saidid</span><span class="sxs-lookup"><span data-stu-id="7b62c-112">Sites</span></span> | <span data-ttu-id="7b62c-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="7b62c-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="7b62c-114">Laod</span><span class="sxs-lookup"><span data-stu-id="7b62c-114">Warehouses</span></span> | <span data-ttu-id="7b62c-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="7b62c-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

