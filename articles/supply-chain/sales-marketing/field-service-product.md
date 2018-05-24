---
title: "Rakenduse Finance and Operations toodete sünkroonimine rakenduse Field Service toodetega"
description: "See teema käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Rakenduse Finance and Operations toodete sünkroonimine rakenduse Field Service toodetega

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

Kasutatud mall **Field Service’i tooted (Fin and Opsist Field Service’isse)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (Fin and Opsist Salesi) – otse**. Lisateabe saamiseks vt [Tooted (Fin and Opsist Salesi) – otse](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Selles teemas kirjeldatakse ainult mallide **Field Service’i tooted (Fin and Opsist Field Service’isse)** ja **Tooted (Fin and Opsist Salesi) – otse** erinevusi.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

**Malli nimi andmete integratsioonis:**

- Field Service’i tooted (Fin and Opsist Field Service’isse)

**Ülesande nimi andmete integratsiooni projektis:**

- Tooted – tooted

Mall **Field Service’i tooted (Fin and Opsist Field Service’isse)** sisaldab üht vastendust, mida pole mallil **Tooted (Fin and Opsist Salesi) – otse**. See vastendus tagab, et kohustuslik spetsiifiline Field Service’i väli **Service’i toote tüüp** on õigesti seadistatud.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Kasutatakse järgmist vastendamist.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Välja **Field Service’i toote tüüp** väärtus andmeüksusel **Müüdavad väljastatud tooted** rakenduses Finance and Operations arvutatakse järgmiselt.

- **Varud:** Toote tüüp = Toote ja kauba mudeligrupp, Ladustatav toode = Tõene
- **Mittevarud:** Toote tüüp = Toote ja kauba mudeligrupp, Ladustatav toode = Väär
- **Teenus:** Toote tüüp = Teenus

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Service’i tooted (Fin and Opsist Field Service’isse): tooted – tooted

[![Malli vastendamine andmete integratsioonis](./media/FSProduct.png)](./media/FSProduct.png)

