---
title: Isiku haridus
description: See artikkel kirjeldab isiku haridusüksust isikule Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0fbbb467852d2aeb070c7732c9aa3108fd504de0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893899"
---
# <a name="person-education"></a>Isiku haridus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab isiku haridusüksust isikule Dynamics 365 Human Resources.

Füüsiline nimi: mshr_hcmpersoneducationentity

## <a name="description"></a>Kirjeldus

See üksus sisaldab kandidaadiks oleva isiku hariduslugu. Haridus on seotud isikukirjega, mis võimaldab hariduse seostamist mistahes muude rollidega, mis on isikule loodud lisaks kandidaadikirjele (töötaja, peatöövõtja jne).

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Isiku hariduse olemi ID**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav | Isiku hariduse kirje süsteemi loodud kordumatu identifikaator. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Loe/kirjuta<br>Nõutav | Kandidaadi osapoole (isiku) kirje kordumatu identifikaator. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Süsteemi loodud kandidaadi isiku kirje kordumatu identifikaator. |
| **Ainepunktide alus**<br>mshr_creditbasis<br>*suvandikomplekt mshr_hcmeducationcreditbasis* | Loe/kirjuta<br>Valikuline | Haridustaseme ainepunktide alus. |
| **Lõpetatud ainepunktid**<br>mshr_creditscompleted<br>*Kümnendkoht* | Loe/kirjuta<br>Valikuline | Hariduse jaoks lõpetatud ainepunktide arv. |
| **Teenitud ainepunktid**<br>mshr_creditsearned<br>*Kümnendkoht* | Loe/kirjuta<br>Valikuline | Pooleli oleva haridustaseme hariduskirje eest saadud ainepunktide arv. |
| **Vajalikud ainepunktid**<br>mshr_creditsneeded<br>*Kümnendkoht* | Loe/kirjuta<br>Valikuline | Poolelioleva kraadi ajoks vajalike ainepunktide arv. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe/kirjuta<br>Valikuline | Kandidaadi kraadi kirjeldus. |
| **Haridustaseme ID**<br>mshr_educationlevelid<br>*String* | Loe/kirjuta<br>Valikuline | Haridustaseme ID. | 
| **Haridustaseme ID väärtus**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmeducationdegreeentityid olemist mshr_hcmeducationdegreeentity entity | Hairdustaseme kirje süsteemi loodud kordumatu identifikaator. See identifikaator annab organisatsioonile määratletud kraadid ja haridustaseme. |
| **Haridusdistsipliini ID**<br>mshr_educationdisciplineid<br>*String* | Loe/kirjuta<br>Nõutav<br>Võõrvõti: EducationDiscipline | Haridusdistsipliini ID. |
| **Haridusdistsipliini ID väärtus**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmeducationdisciplineentityid olemist mshr_hcmeducationdisciplineentity | Süsteemi loodud hariduskirje haridusdistsipliini kordumatu identifikaator. |
| **Teisene rõhutus**<br>mshr_secondaryemphasis<br>*String* | Loe/kirjuta<br>Valikuline | Saadud kraad teisene rõhutus. |
| **Haridusasutuse ID**<br>mshr_educationinstitutionid<br>*String* | Loe/kirjuta<br>Valikuline | Lõpetatud haridusasutuse ID. |
| **Haridusasutuse ID väärtus**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmeducationinstitutionentityid olemist mshr_hcmeducationinstitutionentity | Haridusasutuse süsteemi loodud identifikaator. |
| **Alguskuupäev**<br>mshr_startdate<br>*Datetime* | Loe/kirjuta<br>Valikuline | Teenitud teaduskraadi hariduse alguskuupäev. |
| **Lõppkuupäev**<br>mshr_enddate<br>*Datetime* | Loe/kirjuta<br>Nõutav | Mandaadi väljastamise kuupäev. |
| **Kestus**<br>mshr_duration<br>*Kümnendkoht* | Loe/kirjuta<br>Valikuline | Hariduskirje aja kestus. |
| **Kestuse ühik**<br>mshr_durationunit<br>*suvandikomplekt mshr_periodunit* | Loe/kirjuta<br>Valikuline | Hariduskirje kestusega seotud ajaühik. |
| **Keskmine hinne**<br>mshr_gradepointaverage<br>*Kümnendkoht* | Loe/kirjuta<br>Valikuline | Hariduse omandamisel saadud hinnete keskmine. |
| **Astmeskaala**<br>mshr_gradescale<br>*String* | Loe/kirjuta<br>Valikuline | Keskmise hinde saamise astmeskaala. |
| **Märkmed**<br>mshr_notes<br>*String* | Loe/kirjuta<br>Valikuline | Märkused värbamishalduritele ja värbajatele kasutamiseks. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Väli, mida kasutatakse üksusekirje teise esmase ID-na. Osapoole numbri, haridusdistsipliini ID, haridusasutuse ID ja haridustaseme ID kombinatsioon. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
