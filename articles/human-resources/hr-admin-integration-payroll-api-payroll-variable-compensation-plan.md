---
title: Palgaarvestuse hüvitise muutlik plaan
description: See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96a644bf129de6dd3f78098bcb6415d17058d6decbd7d904a99bb6f050d3a9e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730438"
---
# <a name="payroll-variable-compensation-plan"></a>Palgaarvestuse hüvitise muutlik plaan

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources muutliku palgaplaani olemit.

### <a name="description"></a>Kirjeldus

See üksus pakub töötaja antud positsioonile määratud tulemustasu plaani.

Füüsiline nimi: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud</br>Nõutav |Töötaja kordumatu personalinumber.  |
| **Preemia kuupäev**</br>mshr_preemiakuupäev</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud</br>Nõutav | Preemia kuupäev. |
| **Preemia tüüp**</br>mshr_preemiatüüp</br>*[suvandikomplekt mshr_hcmcompletionstatus](hr-admin-integration-payroll-api-award-type.md)* | Kirjutuskaitstud</br>Nõutav | Muutuva hüvitise plaani jaoks määratud preemia tüüp. |
| **Currency**</br>mshr_üksusvaluutakood</br>*String* | Kirjutuskaitstud </br>Nõutav |Muutuva palgaplaani jaoks määratletud valuuta.   |
| **Fikseeritud palgaplaani id**</br>mshr_fikseeritudplaaniid</br>*String* | Kirjutuskaitstud | Valige preemia arvutamise aluseks olev põhipalgaplaan. |
| **Ühikuväärtus**</br>mshr_preemiahulk</br>*Kümnendkoht* | Kirjutuskaitstud | Üksuse väärtus |
| **Protsessi tüüp**</br>mshr_protsessitüüp</br>*[suvandikomplekt mshr_hcmcompletionstatus](hr-admin-integration-payroll-api-process-type.md)* | Kirjutuskaitstud | Protsessi tüüp. |
| **Muutuva hüvitisplaani tüüp**</br>String</br>*mshr_tüüpid* | Kirjutuskaitstud | Muutuva tasustamise plaani tüüp. |
| **Muutuva hüvitisplaani id**</br>String</br>*mshr_planid* | Kirjutuskaitstud | Muutuva tasustamise plaani id. |
| **Esmane väli**</br>mshr_primaryfield</br>*GUID* | Kirjutuskaitstud</br>Süsteemi loodud. | |
| **Töötaja ID**</br>mshr_fk_employee_id_value</br>*GUID* | Kirjutuskaitstud</br>Nõutav</br>Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity  | Töötaja id. |
| **Palgaarvestuse muutuva hüvitise plaani üksus**</br>mshr_palgaarvestusehüvitiseplaaniid</br>*GUID* | Nõutav</br>Süsteemi loodud | Süsteemi loodud GUID-väärtus palgaplaani kordumatuks tuvastamiseks. |


## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**Vastus**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
