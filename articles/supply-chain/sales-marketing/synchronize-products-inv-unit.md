---
title: Toodete sünkroonimine varude üksusega rakendusest Supply Chain Management rakendusse Field Service
description: See artikkel käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks laoühikuga alates kuni Dynamics 365 Supply Chain Management Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887250"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Toodete sünkroonimine varude üksusega rakendusest Supply Chain Management rakendusse Field Service

[!include[banner](../includes/banner.md)]

See artikkel käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks laoühikuga alates kuni Dynamics 365 Supply Chain Management Dynamics 365 Field Service.

[![Äriprotsesside sünkroniseerimine rakenduste Supply Chain Management ja Field Service vahel.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Kasutatud mall **Field Service’i laoühikuga tooted (rakendusest Supply Chain Management rakendusse Field Service)** põhineb mallil **Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)**. Lisateavet vt jaotisest [Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega](field-service-product.md).

See artikkel kirjeldab ainult erinevusi kahe malli vahel: 
- **Field Service’i tooted laoühikuga (rakendusest Supply Chain Management rakendusse Müük)**
- **Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)** 

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

**Malli nimi andmete integratsioonis:**

- Field Service’i tooted laoühikuga (rakendusest Supply Chain Management rakendusse Müük)

**Ülesande nimi andmete integratsiooni projektis:**

- Tooted

Mall **Field Service’i laoühikuga tooted (rakendusest Supply Chain Management rakendusse Field Service)** sisaldab üht vastendust, mida pole mallis **Field Service’i tooted (rakendusest Supply Chain Management rakendusse Field Service)**. See vastendus tagab, et kaasatud on varude taseme sünkroonimiseks vajalik laoühik.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service’i laoühikuga tooted (Supply Chain Managementist Field Service’isse): tooted

[![Malli vastendamine andmete integratsioonis.](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]