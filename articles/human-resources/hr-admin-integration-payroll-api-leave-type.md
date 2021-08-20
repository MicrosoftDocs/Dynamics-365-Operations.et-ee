---
title: Puhkuse tüüp
description: See teema annab üksikasjad ja näidispäringu puhkuse üksuse tüübi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5e64b533ad7be23060701e8826a25736a078b59d1ecf824bee0e2dd05c9c78f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713098"
---
# <a name="leave-type"></a>Puhkuse tüüp

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources puhkuse tüübi olemit.

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
