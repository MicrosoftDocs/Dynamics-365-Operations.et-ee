---
title: Palga positsiooni töö
description: See artikkel annab üksikasju ja näitepäringut palgaarvestuse positsiooni tööüksuse kohta üksuses Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa347f4b99adc7c29d69daf62ad2bbfc14726a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864079"
---
# <a name="payroll-position-job"></a>Palga positsiooni töö


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab palga positsiooni töö üksust üksuse jaoks Dynamics 365 Human Resources.

### <a name="description"></a>Kirjeldus

See üksus pakub positsiooni ja töö vahelist suhet antud põhitasuplaani jaoks.

Füüsiline nimi: mshr_payrollpositionjobentity.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Ametikoha ID**</br>mshr_positionid</br>*String* | Kirjutuskaitstud | Ametikoha ID. |
| **Kehtiv alates**</br>mshr_validto</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Kuupäev, millest alates ametikoht ja töösuhe kehtivad. |
| **Kehtiv kuni**</br>mshr_validto</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Kuupäev, milleni ametikoht ja töösuhe kehtivad. |
| **Töö ID**</br>mshr_jobid</br>*String* | Kirjutuskaitstud | Töö ID. |
| **Esmane väli**</br>mshr_primaryfield</br>*String* | Süsteemi loodud | Esmane väli. |
| **Palgaarvestuse töökoha olemi ID**</br>mshr_payrollpositionjobentityid</br>*Guid* | Süsteemi loodud. | Süsteemi loodud globaalse ainuidentifikaatori (GUID) väärtus töö unikaalseks tuvastamiseks. |

## <a name="relations"></a>Seosed

| Atribuudi väärtus | Seotud üksus | Navigeerimise atribuut | Kogumi tüüp |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Pole kohaldatav |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

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
