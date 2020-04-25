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
ms.openlocfilehash: 3485e4f284218924cee01e45d5248f5af1a64010
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215949"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Toodete sünkroonimine varude üksusega rakendusest Supply Chain Management rakendusse Field Service

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse laoühikuga toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.

[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Kasutatud mall **Field Service’i laoühikuga tooted (rakendusest Supply Chain Management rakendusse Field Service)** põhineb mallil **Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)**. Lisateavet vt jaotisest [Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega](field-service-product.md).

Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi: 
- **Field Service’i tooted laoühikuga (rakendusest Supply Chain Management rakendusse Müük)**
- **Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)** 

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

**Malli nimi andmete integratsioonis:**

- Field Service’i tooted laoühikuga (rakendusest Supply Chain Management rakendusse Müük)

**Ülesande nimi andmete integratsiooni projektis:**

- Tooted

Kasutatud mall **Field Service’i laoühikuga tooted (rakendusest Supply Chain Management rakendusse Field Service)** põhineb mallil **Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)**. See vastendus tagab, et kaasatud on varude taseme sünkroonimiseks vajalik laoühik.

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service’i laoühikuga tooted (Supply Chain Managementist Field Service’isse): tooted

[![Malli vastendamine andmete integratsioonis](./media/FSProduct1.png)](./media/FSProduct1.png)
