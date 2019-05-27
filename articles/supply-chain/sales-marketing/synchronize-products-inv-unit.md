---
title: Laoühikuga toodete sünkroonimine rakendusest Finance and Operations rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse laoühikuga toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535855"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="a8a7e-103">Laoühikuga toodete sünkroonimine rakendusest Finance and Operations rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="a8a7e-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a8a7e-104">Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse laoühikuga toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="a8a7e-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a8a7e-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="a8a7e-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="a8a7e-106">Kasutatud mall **Field Service'i laoühikuga tooted (rakendusest Fin and Ops rakendusse Field Service)** põhineb mallil **Field Service’i tooted (rakendusest Fin and Ops rakendusse Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="a8a7e-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="a8a7e-107">Lisateabe saamiseks vt [Field Service’i tooted (Finance and Operationsist Field Service’isse)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="a8a7e-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="a8a7e-108">Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi:</span><span class="sxs-lookup"><span data-stu-id="a8a7e-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="a8a7e-109">**Field Service’i laoühikuga tooted (rakendusest Fin and Ops rakendusse Sales)**</span><span class="sxs-lookup"><span data-stu-id="a8a7e-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="a8a7e-110">**Field Service’i tooted (Fin and Opsist Field Service’isse)**</span><span class="sxs-lookup"><span data-stu-id="a8a7e-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="a8a7e-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="a8a7e-111">Templates and tasks</span></span>

<span data-ttu-id="a8a7e-112">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="a8a7e-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="a8a7e-113">Field Service’i laoühikuga tooted (rakendusest Fin and Ops rakendusse Sales)</span><span class="sxs-lookup"><span data-stu-id="a8a7e-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="a8a7e-114">**Ülesande nimi andmete integratsiooni projektis:**</span><span class="sxs-lookup"><span data-stu-id="a8a7e-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="a8a7e-115">Tooted</span><span class="sxs-lookup"><span data-stu-id="a8a7e-115">Products</span></span>

<span data-ttu-id="a8a7e-116">Mall **Field Service'i laoühikuga tooted (rakendusest Fin and Ops rakendusse Field Service)** sisaldab ühte vastendamist, mis ei sisaldu mallis **Field Service'i tooted (rakendusest Fin and Ops rakendusse Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="a8a7e-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="a8a7e-117">See vastendus tagab, et kaasatud on varude taseme sünkroonimiseks vajalik laoühik.</span><span class="sxs-lookup"><span data-stu-id="a8a7e-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a8a7e-118">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="a8a7e-118">Template mapping in Data integration</span></span>

<span data-ttu-id="a8a7e-119">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="a8a7e-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="a8a7e-120">Field Service'i laoühikuga tooted (rakendusest Fin and Ops rakendusse Field Service): tooted</span><span class="sxs-lookup"><span data-stu-id="a8a7e-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="a8a7e-121">[![Malli vastendamine andmete integratsioonis](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="a8a7e-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
