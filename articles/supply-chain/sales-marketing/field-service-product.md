---
title: Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega
description: See artikkel käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks alates Dynamics 365 Supply Chain Management Dynamics 365 Field Service.
author: Henrikan
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 114550f01f3aed197480fb6830fe913dbfa7b570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860547"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega

[!include[banner](../includes/banner.md)]

See artikkel käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks Dynamics Dynamics 365 Supply Chain Management 365 Field Service'ist.

Kasutatud mall **Field Service’i tooted (rakendus Supply Chain Management rakendusele Field Service)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (rakendus Supply Chain Management rakendusele Salesi) – otse**. Lisateabe saamiseks vt [Tooted (Supply Chain Managementist Salesi) – otse](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

See artikkel kirjeldab ainult erinevusi **Field Service'i toodete (tarneahela haldus field Service'ile)** **ja toodete (tarneahela haldus müügile) vahel – otsesed mallid**.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

**Malli nimi andmete integratsioonis:**

- Rakenduse Field Service tooted (Supply Chain Managementist Field Service'isse)

**Ülesande nimi andmete integratsiooni projektis**

- Tooted – tooted

Kasutatud mall **Field Service’i tooted (rakendus Supply Chain Management rakendusele Field Service)** sisaldab ühte vastendust, mis pole kaasatud malli **Tooted (rakendus Supply Chain Management rakendusele Salesi) – otse**. See vastendus tagab, et kohustuslik spetsiifiline Field Service’i väli **Service’i toote tüüp** on õigesti seadistatud.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Kasutatakse järgmist vastendamist.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Välja **Field Service’i toote tüüp** väärtus andmeüksusel **Müüdavad väljastatud tooted** rakenduses Supply Chain Management arvutatakse järgmiselt.

- **Varud:** Toote tüüp = Toote ja kauba mudeligrupp, Ladustatav toode = Tõene
- **Mittevarud:** Toote tüüp = Toote ja kauba mudeligrupp, Ladustatav toode = Väär
- **Teenus:** Toote tüüp = Teenus

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Rakenduse Field Service tooted (Supply Chain Managementist Field Service'isse): tooted – tooted

[![Malli vastendamine andmete integratsioonis.](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]