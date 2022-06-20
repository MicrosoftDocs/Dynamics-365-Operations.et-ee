---
title: Puhkusetaotlus
description: See artikkel annab üksikasjad ja näidispäringu puhkuse taotluse üksuse jaoks üksuses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899668"
---
# <a name="leave-request"></a>Puhkusetaotlus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab puhkuse taotluse üksust üksusele Dynamics 365 Human Resources

### <a name="description"></a>Kirjeldus

See üksus annab teavet antud puhkusetaotluse kohta.

Füüsiline nimi: mshr_essleaverequestentity.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Taotluse id**</br>mshr_taotluseid</br>*String* | Kirjutuskaitstud | Taotluse id. |
| **Puhkuse tüübi id**</br>mshr_puhkusetüübiid</br>*String* | Kirjutuskaitstud | Puhkuse tüübi Id. |
| **Kuupäev**</br>mshr_puhkusekuupäev</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Puhkusetaotluse kuupäev. |
| **summa**</br>mshr_summa</br>*Kümnendkoht* | Kirjutuskaitstud | Puhkuse taotluse summa. |
| **Poole päeva tüüp**</br>mshr_poolepäevadefinitsioon</br>*mshr_LeaveHalfDayDefinition suvandikomplekt* | Kirjutuskaitstud | Poole päeva puhkuse tüüp. |
| **Kommentaar**</br>mshr_comments</br>*String* | Kirjutuskaitstud | Taotluse kommentaar. |
| **Olek**</br>mshr_status</br>*suvandikomplekt mshr_olek* | Kirjutuskaitstud | Taotluse olek. |
| **Kuupäev**</br>mshr_taotlusekuupäev</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Puhkusetaotluse kuupäev. |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud | Töötaja kordumatu personalinumber. |
| **Põhjuse koodi id**</br>mshr_põhjusekoodiid</br>*String* | Kirjutuskaitstud | Põhjuse koodi id. |
| **Andmeala ID**</br>mshr_dataareaid</br>*String* | Kirjutuskaitstud | Määratleb juriidilise isiku (ettevõtte). |
| **Esmane väli**</br>mshr_primaryfield</br>*GUID* | Kirjutuskaitstud</br>Süsteemi loodud | |
| **Puhkuse tüübi üksus**</br>mshr_esspuhkusetaotluseid</br>*GUID* | Süsteemi loodud | Süsteemi loodud GUID-väärtus puhkusetaotluse kordumatuks tuvastamiseks. |

## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Vastus**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
