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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835690"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Laoühikuga toodete sünkroonimine rakendusest Finance and Operations rakendusse Field Service

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse laoühikuga toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Kasutatud mall **Field Service'i laoühikuga tooted (rakendusest Fin and Ops rakendusse Field Service)** põhineb mallil **Field Service’i tooted (rakendusest Fin and Ops rakendusse Field Service)**. Lisateabe saamiseks vt [Field Service’i tooted (Finance and Operationsist Field Service’isse)](field-service-product.md).

Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi: 
- **Field Service’i laoühikuga tooted (rakendusest Fin and Ops rakendusse Sales)**
- **Field Service’i tooted (Fin and Opsist Field Service’isse)** 

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

**Malli nimi andmete integratsioonis:**

- Field Service’i laoühikuga tooted (rakendusest Fin and Ops rakendusse Sales)

**Ülesande nimi andmete integratsiooni projektis:**

- Tooted

Mall **Field Service'i laoühikuga tooted (rakendusest Fin and Ops rakendusse Field Service)** sisaldab ühte vastendamist, mis ei sisaldu mallis **Field Service'i tooted (rakendusest Fin and Ops rakendusse Field Service)**. See vastendus tagab, et kaasatud on varude taseme sünkroonimiseks vajalik laoühik.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>Field Service'i laoühikuga tooted (rakendusest Fin and Ops rakendusse Field Service): tooted

[![Malli vastendamine andmete integratsioonis](./media/FSProduct1.png)](./media/FSProduct1.png)
