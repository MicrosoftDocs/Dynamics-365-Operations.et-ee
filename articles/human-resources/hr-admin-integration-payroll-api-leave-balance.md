---
title: Puhkuse saldo
description: See artikkel annab üksikasjad ja näitepäringu saldoüksuse puhkuse kohta üksuses Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4792c316b8b7af3e86b097029eb281af4a10d113
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899697"
---
# <a name="leave-balance"></a>Puhkuse saldo


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab puhkuse saldo üksust üksusele Dynamics 365 Human Resources.

### <a name="description"></a>Kirjeldus

See üksus annab puhkuse saldo puhkuse tüübi kohta antud töötaja kohta.

Füüsiline nimi: mshr_essleavebalanceentities.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud | Töötaja kordumatu personalinumber. |
| **Praegune saldo**</br>mshr_balansssaadaval</br>*Kümnendkoht* | Kirjutuskaitstud | Töötaja praegune saldo. |
| **Tüüp**</br>mshr_balansssaadaval</br>*String* | Kirjutuskaitstud | Puhkuse tüübi Id. |
| **Kogumismäär**</br>mshr_kogumismäärakirjeldus</br> | Kirjutuskaitstud | Kogumismäär. |
| **Viimane edasikantav summa**</br>mshr_viimaneedasikantavsumma</br>*Kümnendkoht* | Kirjutuskaitstud | Viimane edasikandmise summa. |
| **Võetud sel aastal**</br>mshr_võetudselaastal</br>*Kümnendkoht* | Kirjutuskaitstud | Sel aastal võetud puhkuse summa. |
| **Kokku sel aastal**</br>mshr_kokkuselaastal</br>*Kümnendkoht* | Kirjutuskaitstud | Selle aasta kogusumma. |
| **Andmeala ID**</br>mshr_dataareaid_id</br>*String* | Kirjutuskaitstud | Määratleb juriidilise isiku (ettevõtte). |
| **Esmane väli**</br>mshr_primaryfield</br>*GUID* | Kirjutuskaitstud</br>Süsteemi loodud | |
| **Puhkuse tüübi id**</br>_mshr_fk_puhkusetüübi_id_väärtus</br>*GUID* | Kirjutuskaitstud</br>Võõrvõti: mshr_essleavetypeentityid olemist mshr_essleavetypeentity  | Puhkuse tüübi ID |
| **Puhkuse saldo üksus**</br>mshr_esspuhkusesaldoüksuseid</br>*GUID* | Süsteemi loodud | Süsteemi loodud GUID-väärtus aadressi kordumatuks saldo tuvastamiseks. |

## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Vastus**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
