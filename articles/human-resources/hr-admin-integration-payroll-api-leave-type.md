---
title: Puhkuse tüüp
description: See artikkel annab puhkuse tüübi üksuse üksikasjad ja näidepäringu üksuses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893782"
---
# <a name="leave-type"></a>Puhkuse tüüp


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab puhkuse tüübi üksust üksuse jaoks Dynamics 365 Human Resources.

### <a name="description"></a>Kirjeldus

See üksus annab teavet antud puhkuse tüübi kohta.

Füüsiline nimi: mshr_essleavetypeentity.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Puhkuse tüübi ID**</br>mshr_puhkusetüüpid</br>*String* | Kirjutuskaitstud | Puhkuse tüübi Id. |
| **Kirjeldus**</br>mshr_description</br>*String* | Kirjutuskaitstud | Puhkusetüübi kirjeldus. |
| **Kategooria**</br>mshr_kategooria</br>*mshr_PuhkuseTüübiKategooria suvandikomplekt* | Kirjutuskaitstud | Puhkuse tüübi kategooria. |
| **Nõutav põhjuse kood**</br>mshr_onpõhjusekoodnõutud</br>*suvandikomplekt mshr_eijah* | Kirjutuskaitstud | Määratleb, kas puhkuse tüübi jaoks on vaja põhjuse koodi. |
| **Puhkuse ühik**</br>mshr_puhkusekoguseüksus</br>*suvandikomplekt mshr_LeaveAmountUnit* | Kirjutuskaitstud | Selle puhkusetüübi ühikud. |
| **Luba pool päeva**</br>mshr_lubapoolepäevadefinitsioon</br>*suvandikomplekt mshr_eijah* | Määratleb, kas puhkuse tüübi jaoks on pool päeva lubatud. |
| **Andmeala ID**</br>mshr_dataareaid_id</br>*String* | Kirjutuskaitstud | Määratleb juriidilise isiku (ettevõtte). |
| **Puhkuse tüübi üksus**</br>mshr_esspuhkusetüüpüksusid</br>*GUID* | Süsteemi loodud | Süsteemi loodud GUID-väärtus palga kordumatuks tuvastamiseks. |

## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Vastus**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
