---
title: Palgaarvestuse hüvitise muutlik plaan
description: See artikkel annab üksikasjad ja näitepäringu Palga tulemustasu plaani üksuse jaoks üksuses Dynamics 365 Human Resources.
author: twheeloc
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c6190084c3f1ce15d6a4ab8f13843a5da801dd3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868126"
---
# <a name="payroll-variable-compensation-plan"></a>Palgaarvestuse hüvitise muutlik plaan


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab palga tulemustasu plaanimise üksust üksuse jaoks Dynamics 365 Human Resources.

### <a name="description"></a>Kirjeldus

See üksus pakub töötaja antud positsioonile määratud tulemustasu plaani.

Füüsiline nimi: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud | Töötaja kordumatu personalinumber.  |
| **Preemia kuupäev**</br>mshr_preemiakuupäev</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Preemia kuupäev. |
| **Preemia tüüp**</br>mshr_preemiatüüp</br>*[suvandikomplekt mshr_hcmcompletionstatus](hr-admin-integration-payroll-api-award-type.md)* | Kirjutuskaitstud | Muutuva hüvitise plaani jaoks määratud preemia tüüp. |
| **Currency**</br>mshr_üksusvaluutakood</br>*String* | Kirjutuskaitstud |Muutuva palgaplaani jaoks määratletud valuuta.   |
| **Fikseeritud palgaplaani id**</br>mshr_fikseeritudplaaniid</br>*String* | Kirjutuskaitstud | Valige preemia arvutamise aluseks olev põhipalgaplaan. |
| **Ühikuväärtus**</br>mshr_preemiahulk</br>*Kümnendkoht* | Kirjutuskaitstud | Üksuse väärtus |
| **Protsessi tüüp**</br>mshr_protsessitüüp</br>*[suvandikomplekt mshr_hcmcompletionstatus](hr-admin-integration-payroll-api-process-type.md)* | Kirjutuskaitstud | Protsessi tüüp. |
| **Muutuva hüvitisplaani tüüp**</br>String</br>*mshr_tüüpid* | Kirjutuskaitstud | Muutuva tasustamise plaani tüüp. |
| **Muutuva hüvitisplaani id**</br>String</br>*mshr_planid* | Kirjutuskaitstud | Muutuva tasustamise plaani id. |
| **Ühikute arv**</br>Kümnendkoht</br>*mshr_numberofunits* | Kirjutuskaitstud | Auhinna ühikute arv. |
| **Esmane väli**</br>mshr_primaryfield</br>*GUID* | Kirjutuskaitstud</br>Süsteemi loodud. | |
| **Palgaarvestuse muutuva hüvitise plaani üksus**</br>mshr_palgaarvestusehüvitiseplaaniid</br>*GUID* | Süsteemi loodud | Süsteemi loodud GUID-väärtus palgaplaani kordumatuks tuvastamiseks. |

## <a name="relations"></a>Seosed 

|Atribuudi väärtus | Seotud üksus | Navigeerimise atribuut | Kogumi tüüp |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentityid](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Eployee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Vastus**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
