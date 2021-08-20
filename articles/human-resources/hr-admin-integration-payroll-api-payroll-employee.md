---
title: Palgaarvestuse töövõtja
description: See teema annab üksikasjad ja näidispäringu Palgatöötaja olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 20e74e97f98d0bc0fd454d54cbf969d4f1b46c7c98b2949b0ed8cfe671312dd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768187"
---
# <a name="payroll-employee"></a>Palgaarvestuse töövõtja

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources palgatöötaja olemit.

Füüsiline nimi: mshr_payrollemployeeentity.

### <a name="description"></a>Kirjeldus

See üksus annab teavet töötaja kohta. Peate häälestama [palga integreerimise parameetrid](hr-admin-integration-payroll-api-parameters.md) enne selle üksuse kasutamist.

>[!IMPORTANT] 
>Väljad **Eesnimi**, **Keskmine nimi**, **Perekonnanimi**, **NimiValidVorm** ja **NimiValidKellele** pole enam selle üksuse jaoks saadaval. See tagab, et on olemas ainult üks kehtivusega andmeallikas, mis seda üksust kindlustab.
>Need väljad on saadaval olemis **DirPersonNameHistoricalEntity**, mis anti välja platvormi värskendusega 43. Väljal **Isik** on OData kaudu seotud **PayrollEmployeeEntity** ja **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Personalinumber**<br>mshr_personnelnumber<br>*String* | Kirjutuskaitstud | Töötaja kordumatu personalinumber. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Süsteemi loodud |  |
| **Juriidilise isiku ID**<br>mshr_legalentityID<br>*String* | Kirjutuskaitstud | Määratleb juriidilise isiku (ettevõtte). |
| **Sugu**<br>mshr_gender<br>[suvandikomplekt mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | Kirjutuskaitstud | Töötaja sugu. |
| **Palgatöötaja olemi ID**<br>mshr_payrollemployeeentityid<br>*GUID* | Nõutav<br>Süsteemi loodud | Süsteemi loodud GUID-väärtus töötaja kordumatuks tuvastamiseks. |
| **Töösuhte alguskuupäev**<br>mshr_employmentstartdate<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Töötaja tööhõive alguskuupäev. |
| **ID-tüübi ID**<br>mshr_identificationtypeid<br>*String* |Kirjutuskaitstud | Töötaja jaoks määratletud ID-tüüp. |
| **Töösuhte lõppkuupäev**<br>mshr_employmentenddate<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud |Töötaja tööhõive lõpukuupäev.  |
| **Andmeala ID**<br>mshr_dataareaid_id<br>*GUID* | Kirjutuskaitstud <br>Süsteemi loodud | Süsteemi loodud GUID-väärtus, mis identifitseerib juriidilise isiku (ettevõtte). |
| **Kehtiv kuni**<br>mshr_namevalidto<br>*Kuupäeva ja kellaaja nihe* |  Kirjutuskaitstud | Töötajaga seotud teabe kehtivuse lõpukuupäev. |
| **Sünnikuupäev**<br>mshr_birthdate<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Töötaja sünnikuupäev |
| **ID-number**<br>mshr_identificationnumber<br>*String* | Kirjutuskaitstud |Töötaja jaoks määratletud ID-number.  |

## <a name="example-query-for-payroll-employee"></a>Palgatöötaja näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
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
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
