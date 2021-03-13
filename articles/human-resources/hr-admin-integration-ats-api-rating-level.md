---
title: Hindamise tase
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Hindamistase.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125253"
---
# <a name="rating-level"></a>Hindamise tase

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Hindamistase.

Füüsiline nimi: mshr_hcmratinglevelentity

## <a name="description"></a>Kirjeldus

See olem annab saadaolevad oskuste hindamistasemed. Hindamistasemed kehtivad kõigi juriidiliste isikute lõikes.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Hindamistaseme üksuse ID**<br>mshr_hcmratinglevelentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Tase,e süsteemi loodud kordumatu identifikaator. |
| **Hindamistaseme ID**<br>mshr_ratinglevelid<br>*String* | Loe/kirjuta<br>Nõutav | Tase,e kordumatu kasutaja loetav identifikaator. |
| **Hindamismudeli ID**<br>mshr_ratingmodelid<br>*String* | Loe/kirjuta<br>Nõutav | Hindamismudel, millesse hindamistase kuulub. |
| **Hindamismudeli üksuse ID**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmratingmodelentityid olemist mshr_hcmratingmodelentity | Süsteemi loodud identifikaator hindamismudelile, kuhu hindamistase kuulub. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe/kirjuta<br>Nõutav | Hindamistaseme kirjeldus. |
| **Tegur**<br>mshr_factor<br>*Täisarv* | Loe/kirjuta<br>Nõutav | Hindamistaseme tegur. Kui võrdlete erinevate hindamistasemete arvuga üksusi, kasutatakse seda tegurit tulemuste normaliseerimiseks. Väärtus peab olema täisarv vahemikus 0–9. |
| **Märkus.**<br>mshr_note<br>*String* | Loe/kirjuta<br>Valikuline | Reitingutasemega seostatud märkused. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Väli, mida kasutatakse üksusekirje esmase ID-na. Hindamistaseme ID ja hindamismudeli ID kombinatsioon. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

