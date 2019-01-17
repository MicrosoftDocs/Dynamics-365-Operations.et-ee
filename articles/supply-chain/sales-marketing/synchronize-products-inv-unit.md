---
title: "Laoühikuga toodete sünkroonimine rakendusest Finance and Operations rakendusse Field Service"
description: "See teema käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks koos laoühikuga rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Laoühikuga toodete sünkroonimine rakendusest Finance and Operations rakendusse Field Service

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks koos laoühikuga rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Kasutatud mall **Field Service’i tooted (Finance and Operationsist Field Service’isse)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (Finance and Operationsist Salesi) – otse**. Lisateabe saamiseks vt [Tooted (Finance and Operationsist Salesi) – otse](products-template-mapping-direct.md).

Selles teemas kirjeldatakse ainult mallide **Field Service’i tooted (Finance and Operationsist Field Service’isse)** ja **Field Service'i tooted (Finance and Operationsist Salesi)** erinevusi.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

**Malli nimi andmete integratsioonis:**

- Field Service'i tooted laoühikuga (rakendusest Finance and Operations rakendusse Müük)

**Ülesande nimi andmete integratsiooni projektis:**

- Tooted

**Field Service'i laoüksusega toodete (Finance and Operationsist Field Service'isse)** mall sisaldab ühte vastendamist, mis ei sisaldu mallis **Field Service'i tooted (Finance and Operationsist Field Service'isse)**. See vastendus tagab, et kaasatud on varude taseme sünkroonimiseks vajalik laoühik.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Field Service'i laoühikuga tooted (Finance and Operationsist Field Service'isse): tooted

[![Malli vastendamine andmete integratsioonis](./media/FSProduct1.png)](./media/FSProduct1.png)

