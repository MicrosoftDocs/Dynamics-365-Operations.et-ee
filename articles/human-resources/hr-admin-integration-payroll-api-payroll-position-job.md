---
title: Palga positsiooni töö
description: See teema annab üksikasjad ja näidispäringu Palgalise ametikoha olemi kohta rakenduses Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d5f84a1a6ff794cdc8b4b81e8518983789a0b33f1708719906f6ad094d9c4285
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722627"
---
# <a name="payroll-position-job"></a>Palga positsiooni töö

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources palgatöötaja ametikoha olemit.

### <a name="description"></a>Kirjeldus

See üksus pakub positsiooni ja töö vahelist suhet antud põhitasuplaani jaoks.

Füüsiline nimi: mshr_payrollpositionjobentity.

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Töö ID**<br>mshr_jobid<br>*String* | Kirjutuskaitstud<br>Nõutav |Töö ID. |
| **Kehtiv alates**<br>mshr_validto<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud <br>Nõutav | Kuupäev, millest alates ametikoht ja töösuhe kehtivad. |
| **Kehtiv kuni**<br>mshr_validto<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud <br>Nõutav | Kuupäev, milleni ametikoht ja töösuhe kehtivad.  |
| **Ametikoha ID**<br>mshr_positionid<br>*String* | Kirjutuskaitstud<br>Nõutav | Ametikoha ID. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Nõutav<br>Süsteemi loodud |  |
| **Ametikoha töö ID väärtus**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |Ametikohaga seotud töö ID.|
| **Põhipalgaplaani ID**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | Põhipalgaplaaniga seotud töö ID. |
| **Palgaarvestuse töökoha olemi ID**<br>mshr_payrollpositionjobentityid<br>*Guid* | Nõutav<br>Süsteemi loodud. | Süsteemi loodud GUID-väärtus töö kordumatuks tuvastamiseks.  |

## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Vastus**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
