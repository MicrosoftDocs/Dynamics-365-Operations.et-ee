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
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/14/2019
ms.locfileid: "842458"
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
