---
title: Toodete sünkroonimine varude üksusega rakendusest Supply Chain Management rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse laoühikuga toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 62ed33d101f7d7e47b560c417dc05e5aecc83478
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546334"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="86584-103">Toodete sünkroonimine varude üksusega rakendusest Supply Chain Management rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="86584-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="86584-104">Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse laoühikuga toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="86584-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="86584-105">[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="86584-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="86584-106">Kasutatud mall **Field Service’i laoühikuga tooted (rakendusest Supply Chain Management rakendusse Field Service)** põhineb mallil **Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="86584-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="86584-107">Lisateavet vt jaotisest [Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="86584-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="86584-108">Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi:</span><span class="sxs-lookup"><span data-stu-id="86584-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="86584-109">**Field Service’i tooted laoühikuga (rakendusest Supply Chain Management rakendusse Müük)**</span><span class="sxs-lookup"><span data-stu-id="86584-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="86584-110">**Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)**</span><span class="sxs-lookup"><span data-stu-id="86584-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="86584-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="86584-111">Templates and tasks</span></span>

<span data-ttu-id="86584-112">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="86584-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="86584-113">Field Service’i tooted laoühikuga (rakendusest Supply Chain Management rakendusse Müük)</span><span class="sxs-lookup"><span data-stu-id="86584-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="86584-114">**Ülesande nimi andmete integratsiooni projektis:**</span><span class="sxs-lookup"><span data-stu-id="86584-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="86584-115">Tooted</span><span class="sxs-lookup"><span data-stu-id="86584-115">Products</span></span>

<span data-ttu-id="86584-116">Kasutatud mall **Field Service’i laoühikuga tooted (rakendusest Supply Chain Management rakendusse Field Service)** põhineb mallil **Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="86584-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="86584-117">See vastendus tagab, et kaasatud on varude taseme sünkroonimiseks vajalik laoühik.</span><span class="sxs-lookup"><span data-stu-id="86584-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="86584-118">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="86584-118">Template mapping in Data integration</span></span>

<span data-ttu-id="86584-119">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="86584-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="86584-120">Field Service’i laoühikuga tooted (Supply Chain Managementist Field Service’isse): tooted</span><span class="sxs-lookup"><span data-stu-id="86584-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="86584-121">[![Malli vastendamine andmete integratsioonis](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="86584-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
