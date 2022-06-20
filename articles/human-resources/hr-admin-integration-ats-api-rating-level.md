---
title: Hindamise tase
description: See artikkel kirjeldab reitingutaseme üksust üksuse <a0/& jaoks Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dcd366632456c186eca9682d79a0c8690772e8bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893870"
---
# <a name="rating-level"></a>Hindamise tase


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab reitingutaseme üksust üksuse <a0/& jaoks Dynamics 365 Human Resources.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
