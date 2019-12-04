---
title: Integreeritu kohad ja laod
description: Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni Finance and Operationsi ning Common Data Service’i vahel.
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
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770980"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="bb08e-103">Integreeritu kohad ja laod</span><span class="sxs-lookup"><span data-stu-id="bb08e-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb08e-104">Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni Finance and Operationsi ning Common Data Service’i vahel.</span><span class="sxs-lookup"><span data-stu-id="bb08e-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="bb08e-105">Tegevuskohad ja laod on rakenduses Supply Chain Management levinud kontseptsioonid.</span><span class="sxs-lookup"><span data-stu-id="bb08e-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="bb08e-106">Neid kasutatakse ettevõtte tarneahela modelleerimiseks.</span><span class="sxs-lookup"><span data-stu-id="bb08e-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="bb08e-107">Mallid</span><span class="sxs-lookup"><span data-stu-id="bb08e-107">Templates</span></span>

<span data-ttu-id="bb08e-108">Common Data Service’iga integreerimisega on need kontseptsioonid ja kogu asjakohane teave saadaval Common Data Service’is järgmises tabelis olevate kohtade ning ladude üksuste kaudu.</span><span class="sxs-lookup"><span data-stu-id="bb08e-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="bb08e-109">Finance and Operationsi rakendused</span><span class="sxs-lookup"><span data-stu-id="bb08e-109">Finance and Operations apps</span></span> | <span data-ttu-id="bb08e-110">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="bb08e-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="bb08e-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bb08e-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="bb08e-112">Saidid</span><span class="sxs-lookup"><span data-stu-id="bb08e-112">Sites</span></span> | <span data-ttu-id="bb08e-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="bb08e-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="bb08e-114">Laod</span><span class="sxs-lookup"><span data-stu-id="bb08e-114">Warehouses</span></span> | <span data-ttu-id="bb08e-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="bb08e-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

