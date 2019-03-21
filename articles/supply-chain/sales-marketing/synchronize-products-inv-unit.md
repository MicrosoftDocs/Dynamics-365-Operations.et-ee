---
title: Laoühikuga toodete sünkroonimine rakendusest Finance and Operations rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse laoühikuga toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2019
ms.locfileid: "836298"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c2f92-103">Laoühikuga toodete sünkroonimine rakendusest Finance and Operations rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="c2f92-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c2f92-104">Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse laoühikuga toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c2f92-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c2f92-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="c2f92-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="c2f92-106">Kasutatud **Field Service’i laoüksusega toodete (Finance and Operationsist Field Service’isse)** mall põhineb mallil **Field Service’i tooted (Finance and Operationsist Field Service’isse)**.</span><span class="sxs-lookup"><span data-stu-id="c2f92-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="c2f92-107">Lisateabe saamiseks vt [Field Service’i tooted (Finance and Operationsist Field Service’isse)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="c2f92-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="c2f92-108">Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi:</span><span class="sxs-lookup"><span data-stu-id="c2f92-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="c2f92-109">**Field Service'i tooted laoühikuga (rakendusest Finance and Operations rakendusse Müük)**</span><span class="sxs-lookup"><span data-stu-id="c2f92-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="c2f92-110">**Field Service’i tooted (Finance and Operationsist Field Service’isse)**</span><span class="sxs-lookup"><span data-stu-id="c2f92-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="c2f92-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="c2f92-111">Templates and tasks</span></span>

<span data-ttu-id="c2f92-112">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="c2f92-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="c2f92-113">Field Service'i tooted laoühikuga (rakendusest Finance and Operations rakendusse Müük)</span><span class="sxs-lookup"><span data-stu-id="c2f92-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="c2f92-114">**Ülesande nimi andmete integratsiooni projektis:**</span><span class="sxs-lookup"><span data-stu-id="c2f92-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="c2f92-115">Tooted</span><span class="sxs-lookup"><span data-stu-id="c2f92-115">Products</span></span>

<span data-ttu-id="c2f92-116">**Field Service'i laoüksusega toodete (Finance and Operationsist Field Service'isse)** mall sisaldab ühte vastendamist, mis ei sisaldu mallis **Field Service'i tooted (Finance and Operationsist Field Service'isse)**.</span><span class="sxs-lookup"><span data-stu-id="c2f92-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="c2f92-117">See vastendus tagab, et kaasatud on varude taseme sünkroonimiseks vajalik laoühik.</span><span class="sxs-lookup"><span data-stu-id="c2f92-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c2f92-118">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="c2f92-118">Template mapping in Data integration</span></span>

<span data-ttu-id="c2f92-119">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="c2f92-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="c2f92-120">Field Service'i laoühikuga tooted (Finance and Operationsist Field Service'isse): tooted</span><span class="sxs-lookup"><span data-stu-id="c2f92-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="c2f92-121">[![Malli vastendamine andmete integratsioonis](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="c2f92-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
