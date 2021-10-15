---
title: Palgaarvestuse töövõtja
description: See teema annab üksikasjad ja näidispäringu Palgatöötaja olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7f43476cd044a9cc2e11412aac4af1cff2f9e511
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559529"
---
# <a name="payroll-employee"></a>Palgaarvestuse töövõtja

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources palgatöötaja olemit.

Füüsiline nimi: mshr_payrollemployeeentity.

### <a name="description"></a>Kirjeldus

See üksus annab teavet töötaja kohta. Peate häälestama [palga integreerimise parameetrid](hr-admin-integration-payroll-api-parameters.md) enne selle üksuse kasutamist.

>[!IMPORTANT] 
>Väljad **Eesnimi**, **Keskmine nimi**, **Perekonnanimi**, **NimiValidVorm** ja **NimiValidKellele** pole enam selle üksuse jaoks saadaval. See tagab, et on olemas ainult üks kehtivusega andmeallikas, mis seda üksust kindlustab.
>Need väljad on saadaval olemis **DirPersonNameHistoricalEntity**, mis anti välja platvormi värskendusega 43. OData kaudu on seotud **PayrollEmployeeEntity** ja **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Juriidilise isiku ID**</br>mshr_legalentityid</br>*String* | Kirjutuskaitstud | Määratleb juriidilise isiku (ettevõtte). |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud | Töötaja kordumatu personalinumber. |
| **Töösuhte alguskuupäev**</br>mshr_employmentstartdate</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Töötaja tööhõive alguskuupäev. |
| **Töösuhte lõppkuupäev**</br>mshr_employmentenddate</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud |Töötaja tööhõive lõpukuupäev.  |
| **Sünnikuupäev**</br>mshr_birthdate</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Töötaja sünnikuupäev. |
| **Sugu**</br>mshr_gender</br>[suvandikomplekt mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | Kirjutuskaitstud | Töötaja sugu. |
| **Töölevõtu tüüp**</br>mshr_employmenttype</br>[mshr_hcmemploymenttype suvandikomplekt](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Kirjutuskaitstud | Töölevõtu tüüp. |
| **ID-tüübi ID**</br>mshr_identificationtypeid</br>*String* |Kirjutuskaitstud | Töötaja jaoks määratletud ID-tüüp. |
| **ID-number**</br>mshr_identificationnumber</br>*String* | Kirjutuskaitstud |Töötaja jaoks määratletud ID-number. |
| **Maksmiseks valmis**</br>mshr_readytopay</br>[suvandikomplekt mshr_noyes](hr-admin-integration-payroll-api-no-yes.md) | Kirjutuskaitstud | Näitab, kas töötaja on märgitud kui maksmiseks valmis. |
| **Palgatöötaja olemi ID**</br>mshr_payrollemployeeentityid</br>*GUID* | Süsteemi loodud | Süsteemi loodud globaalse ainuidentifikaatori (GUID) väärtus töövõtja unikaalseks tuvastamiseks. |

## <a name="relations"></a>Seosed

|Atribuudi väärtus | Seotud üksus | Navigeerimise atribuut | Kogumi tüüp |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_palgaarvestusehüvitiseplaanidüksus](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_töötaja |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Töötaja |

## <a name="example-query-for-payroll-employee"></a>Palgatöötaja näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Vastus**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
