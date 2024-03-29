---
title: Isiku aadress
description: See artikkel kirjeldab isiku aadressi üksuse jaoks Dynamics 365 Human Resources.
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
ms.openlocfilehash: be5cf649771eaddcb4f2198821530e61b76b2cd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871012"
---
# <a name="person-address"></a>Isiku aadress


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab isiku aadressi üksuse jaoks Dynamics 365 Human Resources.

Füüsiline nimi: mshr_hcmpersonaddressentities

## <a name="description"></a>Kirjeldus

Üksus sisaldab kandidaadi kirjete postiaadresside loendit.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Isiku aadressi olemi ID**<br>mshr_hcmpersonaddressentityid<br>*String* | Kirjutuskaitstud<br>Nõutav | Olemi kirje süsteemi loodud kordumatu identifikaator. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Loe/kirjuta<br>Nõutav | Seotud osapoole (isiku) ID. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator. |
| **Asukoha ID**<br>mshr_locationid<br>*String* | Loe/kirjuta<br>Nõutav | Aadressikirje asukoha ID. Seadistamine olemis mshr_logisticspostaladdresslocationcdsentity. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe/kirjuta<br>Nõutav | Kandidaadi aadressi kirjeldus. |
| **Rollid**<br>mshr_roles<br>*String* | Loe/kirjuta<br>Nõutav | Aadressile määratud rollid. Määrata saab rohkem kui ühe rolli. Iga roll tuleb eraldada semikooloniga. Üksuses mshr_logisticslocationroleentity sisalduvad kehtivad väärtused. |
| **Tänav**<br>mshr_street<br>*String* | Loe/kirjuta<br>Valikuline | Majanumber. |
| **Linn**<br>mshr_city<br>*String* | Loe/kirjuta<br>Valikuline | Aadressi linn. Olemi mshr_logisticsaddresscityentity seadistamine. |
| **Maakond**<br>mshr_state<br>*String* | Loe/kirjuta<br>Valikuline | Aadressi maakond. Olemi mshr_logisticsaddressstateentity seadistamine. |
| **Maakond**<br>mshr_county<br>*String* | Loe/kirjuta<br>Valikuline | Aadressi maakond. Olemi mshr_logisticsaddresscountyentity seadistamine. |
| **Sihtnumber**<br>mshr_zipcode<br>*String* | Loe/kirjuta<br>Valikuline | Aadressi sihtnumber/postikood. Olemi mshr_logisticsaddresspostalcodeentity seadistamine. |
| **Riigi regiooni ID**<br>mshr_countryregionid<br>*String* | Loe/kirjuta<br>Valikuline | Aadressi riik või regioon. |
| **Riigi/regiooni ID väärtus**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_logisticaddresscountryregionentityid olemist mshr_logisticsaddresscountryregionentity | Süsteemi loodud aadressi riigi/regiooni ainuidentifikaator. |
| **On esmane**<br>mshr_isprimary<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Nõutav | Näitab, kas see aadress on määratletud rolli isiku esmane aadress. |
| **Privaatne**<br>mshr_isprivate<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Nõutav | Näitab, kas see aadress on isiku privaatne aadress. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Väli, mida kasutatakse üksusekirje esmase ID-na. Osapoole numbri ja asukoha ID kombinatsioon. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
