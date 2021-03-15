---
title: Osapoole kontakt
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Osapoole kontakt.
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
ms.openlocfilehash: 38f53d402ebe9f9f358281dd3996797a20923056
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125469"
---
# <a name="party-contact"></a>Osapoole kontakt

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Osapoole kontakt.

Füüsiline nimi: mshr_dirpartycontactentities

## <a name="description"></a>Kirjeldus

Seelles olemis kirjeldatakse kandidaadi kontaktandmeid, sealhulgas telefoninumbrit, meiliaadressi ja sotsiaalmeedia kontosid.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Osapoole kontakti olemi ID**<br>mshr_dirpartycontactentityid<br>*String* | Kirjutuskaitstud<br>Nõutav | Olemi kirje süsteemi loodud kordumatu identifikaator. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Loe/kirjuta<br>Nõutav | Seotud osapoole (isiku) ID. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator. |
| **Asukoha ID**<br>mshr_locationid<br>*String* | Loe/kirjuta<br>Nõutav | Aadressikirje asukoha ID. Seadistamine olemis mshr_logisticspostaladdresslocationcdsentity. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe/kirjuta<br>Nõutav | Kontaktandmete kirjeldus. |
| **Tüüp**<br>mshr_type<br>*Suvandikomplekt mshr_logisticselectronicaddressmethodtype* | Loe/kirjuta<br>Nõutav | Kontaktandmete tüüp. |
| **Riigi regiooni kood**<br>mshr_countryregioncode<br>*String* | Loe/kirjuta<br>Valikuline | Aadressi riik või regioon. |
| **Lokaator**<br>mshr_locator<br>*String* | Loe/kirjuta<br>Valikuline | Kontaktandmed. Näiteks kui tüübiks on **Meiliaadress**, sisaldab see väli kandidaadi meiliaadressi. |
| **Lokaatori laiend**<br>mshr_locatorextension<br>*String* | Loe/kirjuta<br>Valikuline | Lokaatori laiend. Kui tüübiks on näiteks **Telefon**, sisaldab see atribuut telefoninumbri laiendit. |
| **On mobiil**<br>mshr_ismobile<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Nõutav | Määratleb, kas telefoninumber on mobiiltelefon. |
| **On kiirsõnumside**<br>mshr_isinstantmessage<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Nõutav | Määrab, kas telefon on kiirsõnumside jaoks lubatud. |
| **On esmane**<br>mshr_isprimary<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Nõutav | Määratleb kontakti tüübi esmase kontakti. Kontakti tüübi kohta peab olema ainult üks esmane kirje. |
| **Privaatne**<br>mshr_isprivate<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Nõutav | Näitab, kas see aadress on isiku privaatne aadress. |
| **Eesmärk**<br>mshr_purpose<br>*String* | Loe/kirjuta<br>Valikuline | Kontaktandmete eesmärk/roll. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Väli, mida kasutatakse üksusekirje esmase ID-na. Osapoole numbri, tüübi, kirjelduse ja lokaatori kombinatsioon. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]