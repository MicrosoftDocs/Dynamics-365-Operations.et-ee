---
title: Integreeritu kohad ja laod
description: Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni rakenduse Finance and Operations ja teenuse Dataverse vahel.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d192343d78f9248e4d1232d6aee1a1f800383805
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679316"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="b4736-103">Integreeritud kohad ja laod</span><span class="sxs-lookup"><span data-stu-id="b4736-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b4736-104">Siin peatükis kirjeldatakse koha ja lao andmete integratsiooni rakenduse Finance and Operations ja teenuse Dataverse vahel.</span><span class="sxs-lookup"><span data-stu-id="b4736-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="b4736-105">Tegevuskohad ja laod on rakenduses Supply Chain Management levinud kontseptsioonid.</span><span class="sxs-lookup"><span data-stu-id="b4736-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="b4736-106">Neid kasutatakse ettevõtte tarneahela modelleerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b4736-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="b4736-107">Mallid</span><span class="sxs-lookup"><span data-stu-id="b4736-107">Templates</span></span>

<span data-ttu-id="b4736-108">Dataverse’iga integreerimisega on need kontseptsioonid ja kogu asjakohane teave saadaval Dataverse’is järgmises tabelis olevate kohtade ning ladude andmetabelite kaudu.</span><span class="sxs-lookup"><span data-stu-id="b4736-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="b4736-109">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="b4736-109">Finance and Operations apps</span></span> | <span data-ttu-id="b4736-110">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="b4736-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="b4736-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b4736-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="b4736-112">Saidid</span><span class="sxs-lookup"><span data-stu-id="b4736-112">Sites</span></span> | <span data-ttu-id="b4736-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="b4736-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="b4736-114">Laod</span><span class="sxs-lookup"><span data-stu-id="b4736-114">Warehouses</span></span> | <span data-ttu-id="b4736-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="b4736-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

