---
title: Palgaarvestuse põhipalgaplaan
description: See artikkel annab üksikasjad ja näitepäringu Palga fikseeritud tasu plaani üksuse jaoks üksuses Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 83fa8aeb38cc44191242cf029022939cefb22cb8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909842"
---
# <a name="payroll-fixed-compensation-plan"></a>Palgaarvestuse põhipalgaplaan


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab palga fikseeritud tasu plaani üksust üksuse jaoks Dynamics 365 Human Resources.

### <a name="description"></a>Kirjeldus

See üksus pakub töötaja antud positsioonile määratud tulemustasu plaani.

Füüsiline nimi: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Plaani ID**</br>mshr_planid</br>*String* | Kirjutuskaitstud | Määrab palgaplaani.  |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud | Töötaja kordumatu personalinumber. |
| **Tasumäär**</br>mshr_payrate</br>*Kümnendkoht* | Kirjutuskaitstud | Põhipalgaplaanis määratletud tasumäär. |
| **Ametikoha ID**</br>mshr_positionid</br>*String* | Kirjutuskaitstud | Töötajaga seotud ametikoha ID ja fikseeritud hüvitisteplaani registreerimine. |
| **Kehtiv alates**</br>mshr_validfrom</br>*Kuupäeva ja kellaaja nihe* |  Kirjutuskaitstud | Töötajaga seotud põhipalga kehtivuse algkuupäev.  |
| **Kehtiv kuni**</br>mshr_validto</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Töötajaga seotud põhipalga kehtivuse lõpukuupäev. |
| **Tasusagedus**</br>mshr_payfrequency</br>*String* | Kirjutuskaitstud | [Kompensatsioonitasude sageduse ID](hr-admin-integration-payroll-api-compensation-pay-frequency.md) antud palgamäära jaoks. |
| **Valuuta**</br>mshr_currency</br>*String* | Kirjutuskaitstud | Põhipalgaplaani jaoks määratletud valuuta. |
| **Palgaarvestuse põhipalgaplaani olem**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Süsteemi loodud | Süsteemi loodud GUID-väärtus palgaplaani kordumatuks tuvastamiseks. |

## <a name="relations"></a>Seosed

|Atribuudi väärtus | Seotud üksus | Navigeerimise atribuut | Kogumi tüüp |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Eployee_id | mshr_FK_PayrollEmployeeEntity_FixeddCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_palgaarvestusehüvitiseplaanidüksus](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Vastus**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
