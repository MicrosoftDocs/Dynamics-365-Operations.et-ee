---
title: Isikutunnistus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isikutunnistus.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 796a57a5f97de08ff8c8440bc00d4dc5ced18f58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798125"
---
# <a name="person-certificate"></a>Isikutunnistus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isikutunnistus.

Füüsiline nimi: mshr_hcmpersoncertificateentity

## <a name="description"></a>Kirjeldus

See üksus kirjeldab kandidaadi kutsetunnistusi.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Isikutunnistuse olemi ID**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav | Süsteemi loodud kordumatu identifikaator isikutunnistuse üksuse kirjele. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Loe/kirjuta<br>Nõutav | Kandidaadi osapoole (isiku) ID. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator. |
| **Sertifikaadi tüübi ID**<br>mshr_certificatetypeid<br>*String* | Loe/kirjuta<br>Nõutav |  Human Resourcesis määratletud serditüübi identifikaator. |
| **Sertifikaadi tüübi ID väärtus**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmcertificatetypeentityid olemist mshr_hcmcertificatetypeentity | Seostatud üksuse serditüübi süsteemi loodud kordumatu identifikaator. |
| **Alguskuupäev**<br>mshr_startdate<br>*Datetime* | Loe/kirjuta<br>Nõutav | Serdi väljastamise kuupäev. |
| **Lõppkuupäev**<br>mshr_enddate<br>*Datetime* | Loe/kirjuta<br>Valikuline | Sertifikaadi aegumise kuupäev. |
| **Märkmed**<br>mshr_notes<br>*String* | Loe/kirjuta<br>Valikuline | Märkused värbamishalduritele ja värbajatele kasutamiseks. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav |  Väli, mida kasutatakse üksusekirje esmase ID-na. Osapoole numbri, sertifikaadi tüübi ID ja alguskuupäeva kombinatsioon. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]