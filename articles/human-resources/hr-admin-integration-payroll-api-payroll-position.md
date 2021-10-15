---
title: Ametikohtade palga üksikasjad
description: See teema annab üksikasjad ja näidispäringu ametikohtade üksikasjade olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 76131b6cc7ee58d4a095da4ac56cd97124e42587
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559358"
---
# <a name="payroll-position"></a>Palga positsioon

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources palga ametikoha olemit.

Füüsiline nimi: mshr_payrollpositionentity.

### <a name="description"></a>Kirjeldus

See üksus annab konkreetse töötaja kohta positsiooni puudutavat teavet.

Füüsiline nimi: mshr_payrollpositionentity.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Ametikoha ID**</br>mshr_positionid</br>*String* | Kirjutuskaitstud | Ametikoha ID. |
| **Palgatsükli ID**</br>mshr_paycycleid</br>*String* | Kirjutuskaitstud | Ametikohal määratletud palgatsükkel. |
| **Iga-aastased regulaarsed tunnid**</br>annualregularhours</br>*Kümnendkoht* | Kirjutuskaitstud | Ametikohal määratletud iga-aastased regulaarsed tunnid. |
| **Maksja juriidiline isik**</br>paidbylegalentity</br>*String* | Kirjutuskaitstud | Makse tegemise eest vastutavale ametikohale määratletud juriidiline isik. |
| **Kehtiv kuni**</br>validto</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Kuupäev, milleni ametikoha üksikasjad kehtivad. |
| **Kehtiv alates**</br>validfrom</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Kuupäev, millest ametikoha üksikasjad kehtivad. |
| **Esmane väli**</br>mshr_primaryfield</br>*String* | Süsteemi loodud | Esmane väli. |
| **Palgaarvestuse ametikoha üksikasjade olemi ID**</br>payrollpositiondetailsentityid</br>*Guid* | Nõutav</br>Süsteemi loodud. | Süsteemi loodud globaalse ainuidentifikaatori (GUID) väärtus positsiooni unikaalseks tuvastamiseks. |

## <a name="relations"></a>Seosed

| Atribuudi väärtus | Seotud üksus | Navigeerimise atribuut | Kogumi tüüp |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Pole kohaldatav |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Pole kohaldatav |

## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Vastus**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
