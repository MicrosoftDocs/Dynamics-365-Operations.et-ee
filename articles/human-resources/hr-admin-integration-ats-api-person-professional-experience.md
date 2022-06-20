---
title: Isiku töökogemus
description: See artikkel kirjeldab isiku töökogemuse üksust isikule Dynamics 365 Human Resources.
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
ms.openlocfilehash: d306213e4c647ecd4be98598cba92376aba0d5bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856421"
---
# <a name="person-professional-experience"></a>Isiku töökogemus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab isiku töökogemuse üksust isikule Dynamics 365 Human Resources.

Füüsiline nimi: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>Kirjeldus

Üksus kirjeldab kandidaadi töökogemust või töö ajalugu.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Isiku töökogemuse olemi ID**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav | Olemi kirje süsteemi loodud kordumatu identifikaator. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Loe/kirjuta<br>Nõutav | Kandidaadi isikukirje kordumatu identifikaator. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Isiku olemi kirje süsteemi loodud kordumatu identifikaator. |
| **Tööandja ametikoht**<br>mshr_employerposition<br>*String* | Loe/kirjuta<br>Nõutav | Kandidaadi ametinimetus töösuhte ajal. |
| **Tööandja nimi**<br>mshr_employername<br>*String* | Loe/kirjuta<br>Nõutav | Tööandja nimi. |
| **Tööandja asukoht**<br>mshr_employerlocation<br>*String* | Loe/kirjuta<br>Valikuline | Tööandja asukoht. Maksimaalne pikkus: 60. Konkreetset vormingut pole määratletud ega nõutud. |
| **Telefon**<br>mshr_phone<br>*String* | Loe/kirjuta<br>Valikuline | Tööandja telefoninumber. |
| **URL**<br>mshr_url<br>*String* | Loe/kirjuta<br>Valikuline | Tööandja veebisaidi URL. |
| **Alguskuupäev**<br>mshr_startdate<br>*Datetime* | Loe/kirjuta<br>Nõutav | Kandidaadi tööhõive alguskuupäev. |
| **Lõppkuupäev**<br>mshr_enddate<br>*Datetime* | Loe/kirjuta<br>Valikuline | Kandidaadi töösuhte lõppkuupäev ehk nullväärtus, kui kandidaat töötab endiselt siin. |
| **Lubatud tööandjaga ühendust võtta**<br>mshr_allowcontactemployer<br>*suvandikomplekt mshr_hrmblankyesno* | Loe/kirjuta<br>Valikuline | Näitab, kas kandidaat lubab võtta ühendust eelmise tööandjaga. |
| **Märkmed**<br>mshr_note<br>*String* | Loe/kirjuta<br>Valikuline | Märkused värbamishalduritele ja värbajatele kasutamiseks. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Väli, mida kasutatakse üksusekirje esmase ID-na. Osapoole numbri, alguskuupäeva, tööandja positsiooni ja tööandja nime kombinatsioon. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
