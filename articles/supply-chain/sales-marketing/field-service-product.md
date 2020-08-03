---
title: Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d96d1cd91bad4f950868074d9558cb403821d73f
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546358"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="ecca3-103">Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega</span><span class="sxs-lookup"><span data-stu-id="ecca3-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ecca3-104">Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="ecca3-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="ecca3-105">Kasutatud mall **Field Service’i tooted (rakendus Supply Chain Management rakendusele Field Service)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (rakendus Supply Chain Management rakendusele Salesi) – otse**.</span><span class="sxs-lookup"><span data-stu-id="ecca3-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="ecca3-106">Lisateabe saamiseks vt [Tooted (Supply Chain Managementist Salesi) – otse](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="ecca3-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="ecca3-107">Selles teemas kirjeldatakse ainult mallide **Field Service’i tooted (Supply Chain Managementist Field Service’isse)** ja **Tooted (Supply Chain Managementist Salesi) – otse** erinevusi.</span><span class="sxs-lookup"><span data-stu-id="ecca3-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ecca3-108">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="ecca3-108">Templates and tasks</span></span>

<span data-ttu-id="ecca3-109">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="ecca3-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="ecca3-110">Rakenduse Field Service tooted (Supply Chain Managementist Field Service'isse)</span><span class="sxs-lookup"><span data-stu-id="ecca3-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="ecca3-111">**Ülesande nimi andmete integratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="ecca3-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="ecca3-112">Tooted – tooted</span><span class="sxs-lookup"><span data-stu-id="ecca3-112">Products - Products</span></span>

<span data-ttu-id="ecca3-113">Kasutatud mall **Field Service’i tooted (rakendus Supply Chain Management rakendusele Field Service)** sisaldab ühte vastendust, mis pole kaasatud malli **Tooted (rakendus Supply Chain Management rakendusele Salesi) – otse**.</span><span class="sxs-lookup"><span data-stu-id="ecca3-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="ecca3-114">See vastendus tagab, et kohustuslik spetsiifiline Field Service’i väli **Service’i toote tüüp** on õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="ecca3-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="ecca3-115">Kasutatakse järgmist vastendamist.</span><span class="sxs-lookup"><span data-stu-id="ecca3-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="ecca3-116">Välja **Field Service’i toote tüüp** väärtus andmeüksusel **Müüdavad väljastatud tooted** rakenduses Supply Chain Management arvutatakse järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ecca3-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="ecca3-117">**Varud:** Toote tüüp = Toote ja kauba mudeligrupp, Ladustatav toode = Tõene</span><span class="sxs-lookup"><span data-stu-id="ecca3-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="ecca3-118">**Mittevarud:** Toote tüüp = Toote ja kauba mudeligrupp, Ladustatav toode = Väär</span><span class="sxs-lookup"><span data-stu-id="ecca3-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="ecca3-119">**Teenus:** Toote tüüp = Teenus</span><span class="sxs-lookup"><span data-stu-id="ecca3-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ecca3-120">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="ecca3-120">Template mapping in Data integration</span></span>

<span data-ttu-id="ecca3-121">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="ecca3-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="ecca3-122">Rakenduse Field Service tooted (Supply Chain Managementist Field Service'isse): tooted – tooted</span><span class="sxs-lookup"><span data-stu-id="ecca3-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="ecca3-123">[![Malli vastendamine andmete integratsioonis](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="ecca3-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
