---
title: Töötajate põhipalga plaan
description: See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0837d9a153aba554d0a5293d16afb309bd37963c270da5b67e691558cae63b0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758708"
---
# <a name="payroll-worker-benefit-plan"></a>Töötajate põhipalga plaan

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources fikseeritud palgaplaani olemit.

Füüsiline nimi: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>Kirjeldus

See üksus annab teavet antud töötaja soodustuste plaani kohta.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud</br>Nõutav | Töötaja kordumatu personalinumber. |
| **Juriidilise isiku ID**</br>mshr_legalentityID</br>*String* | Kirjutuskaitstud | Määratleb juriidilise isiku (ettevõtte). |
| **Perioodi ID**</br>mshr_perioodid</br>*String* | Kirjutuskaitstud | Perioodi identifikaator. |
| **Plaani ID**</br>mshr_planid</br>*String* | Kirjutuskaitstud | Plaani identifikaator. |
| **Katvuse valik**</br>mshr_coverageoptionid</br>*String* | Kirjutuskaitstud | Kattevõimaluse identifikaator. |
| **Mahaarvamise alguskuupäev**</br>mshr_deductionstartdatetime</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Mahaarvamise alguskuupäev. |
| **Mahaarvamise lõppkuupäev**</br>mshr_deductionenddatetime</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Mahaarvamise lõppkuupäev. |
| **Olek**</br>mshr_status</br>*[Kasuks töötajaplaani oleku suvandikomplekt](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Kirjutuskaitstud | Hüvede plaani olek. |
| **Kehtiv alates**</br>mshr_validfrom</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Kellaaeg, millest alates see kirje kehtib |
| **Kehtiv kuni**</br>mshr_validto</br>*Kuupäeva ja kellaaja nihe* |  Kirjutuskaitstud | Kellaaeg, milleni see kirje kehtib |
| **Plaani tüüp ID**</br>mshr_plantypeid</br>*String* | Kirjutuskaitstud | Plaani tüübi identifikaator. |
| **Plaani tüübi kood**</br>mshr_plantypecode</br>*[soodustusplaani tüübi tiitli suvandikomplekt](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Kirjutuskaitstud | Plaani tüübi spetsifikatsioon. |
| **Makseperioodide arv**</br>mshr_payperiod</br>*Täisarv* | Kirjutuskaitstud | Makseperioodide arv, mis näitab, kui tihti soodustuse pakkujale või töövõtjatele makstakse. Seda summat kasutatakse töövõtja aastase soodustuse palga summa arvutamiseks. |
| **Töövõtja summa**</br>mshr_amountemployee</br>*Kümnendkoht* | Kirjutuskaitstud | Töötaja summa või protsent. |
| **Tööandja summa**</br>mshr_amountemployer</br>*Kümnendkoht* | Kirjutuskaitstud | Tööandja summa või protsent. |
| **Esmane väli**</br>mshr_primaryfield</br>*String* | Süsteemi loodud | Esmane väli. |
| **Töötaja ID väärtus** </br>_mshr_fk_worker_id_value</br>*GUID* | Võõrvõti: mshr_hcmworkerbaseentityid olemist mshr_hcmworkerbaseentity. | Süsteemi loodud unikaalne identifikaator töötaja jaoks. |
| **Perioodi ID väärtus**</br> _mshr_fk_period_id_value</br>*GUID* | Võõrvõti: mshr_benefitperiodentityid olemist mshr_benefitperiodentity. | Süsteemi loodud perioodi kordumatu identifikaator. |
| **Plaani ID väärtus**</br> _mshr_fk_plan_id_value</br>*GUID* | Võõrvõti: mshr_benefitperiodentityid olemist mshr_benefitperiodentity. | Süsteemi loodud plaani kordumatu identifikaator. |
| **Plaani tüübi ID väärtus**</br> _mshr_fk_plantype_id_value</br>*GUID* | Võõrvõti: mshr_benefitperiodentityid olemist mshr_benefitperiodentity. | Süsteemi loodud plaani kordumatu identifikaator. |
| **Katte valiku ID väärtus**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Võõrvõti: mshr_benefitcoverageoptionentityid olemist mshr_benefitcoverageoptionentity. | Süsteemi loodud plaani kordumatu identifikaator. |
| **Palgatöötaja soodustusplaani üksuse ID väärtus**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Kirjutuskaitstud </br> Süsteemi loodud | Süsteemi loodud kirje kordumatu identifikaator. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Näidispäring palgatöötajate hüvitiste plaani kohta

**Taotlus**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Vastus**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
