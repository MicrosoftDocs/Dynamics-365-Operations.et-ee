---
title: Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
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
ms.openlocfilehash: 09460139ba2ae7c9be78b1441e1d095952b405f8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566475"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.

Kasutatud mall **Field Service’i tooted (rakendus Supply Chain Management rakendusele Field Service)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (rakendus Supply Chain Management rakendusele Salesi) – otse**. Lisateabe saamiseks vt [Tooted (Supply Chain Managementist Salesi) – otse](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Selles teemas kirjeldatakse ainult mallide **Field Service’i tooted (Supply Chain Managementist Field Service’isse)** ja **Tooted (Supply Chain Managementist Salesi) – otse** erinevusi.

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