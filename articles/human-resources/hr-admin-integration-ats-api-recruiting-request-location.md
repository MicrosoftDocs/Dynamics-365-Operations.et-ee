---
title: Värbamistaotluse asukoht
description: Selles teemas kirjeldatakse olemit värbamistaotluse asukoht rakenduse Dynamics 365 Human Resources jaoks.
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
ms.openlocfilehash: 4dbc676e25c1ec24350607b10787924b0738e102
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069167"
---
# <a name="recruiting-request-location"></a>Värbamistaotluse asukoht


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse olemit värbamistaotluse asukoht rakenduse Dynamics 365 Human Resources jaoks.

Füüsiline nimi: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>Kirjeldus

Asukohtadeks määratletud asukohtade loend, kus töötajad värbamisel töötavad. Need on juriidilise isiku alusel loodud asukohad.

### <a name="json-representation"></a>JSON-i esindus

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Asukoha ID**<br>mshr_locationid<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav | Süsteemi loodud, kasutaja loetav värbamise asukoha identifikaator. |
| **Värbamistaotluse asukoht**<br>mshr_recruitingrequestlocationid<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav | Värbamise asukoha kasutaja määratletud kordumatu identifikaator. |
| **Värbamistaotluse asukoha olemi ID**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav | Süsteemi loodud kordumatu identifikaator värbamistaotluse asukoha kirjele. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe/kirjuta<br>Nõutav | Asukoha kirjeldus. |
| **Riigi/regiooni ID**<br>mshr_countryregionid<br>*String* | Kirjutuskaitstud<br>Valikuline | Määrab riigi või regiooni, kus kandidaadil on kodakondsus. |
| **Riigi/regiooni ID väärtus**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_logisticaddresscountryregionentityid olemist mshr_logisticsaddresscountryregionentity | Süsteemi loodud aadressi riigi/regiooni ainuidentifikaator. |
| **Sihtnumber**<br>mshr_zipcode<br>*String* | Kirjutuskaitstud<br>Valikuline | Sihtnumber/postikood. |
| **Tänav**<br>mshr_street<br>*String* | Kirjutuskaitstud<br>Valikuline | Tänava aadress. |
| **Linn**<br>mshr_city<br>*String* | Kirjutuskaitstud<br>Valikuline | Linn. |
| **Maakond**<br>mshr_state<br>*String* | Kirjutuskaitstud<br>Valikuline | Osariik või provints. |
| **Maakond**<br>mshr_county<br>*String* | Kirjutuskaitstud<br>Valikuline | Maakond. |
| **Telefon**<br>mshr_telephone<br>*String* | Loe/kirjuta<br>Valikuline | Asukoha telefoninumber. |
| **E-post**<br>mshr_email<br>*String* | Loe/kirjuta<br>Valikuline | Meiliaadress. |
| **InternetAddress**<br>mshr_internetaddress<br>*String* | Loe/kirjuta<br>Valikuline | Asukoha veebisaidi URL. |
| **Andmeala ID**<br>mshr_dataareaid<br>*String* | Loe/kirjuta<br>Valikuline | Määratleb juriidilise isiku (ettevõtte). |
| **Andmeala ID väärtus**<br>_mshr_dataareaid_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: cdm_companyid olemist cdm_company | Süsteemi loodud GUID-väärtus, mis identifitseerib juriidilise isiku (ettevõtte). |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
