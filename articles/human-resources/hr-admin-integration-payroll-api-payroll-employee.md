---
title: Palgaarvestuse töövõtja
description: See teema annab üksikasjad ja näidispäringu Palgatöötaja olemi kohta rakenduses Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0cd37a7323c0dd0dc6e60ff0495f827e9a8582c1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019366"
---
# <a name="payroll-employee"></a>Palgaarvestuse töövõtja

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema annab üksikasjad ja näidispäringu Palgatöötaja olemi kohta rakenduses Dynamics 365 Human Resources.

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Personalinumber**<br>mshr_personnelnumber<br>*String* | Kirjutuskaitstud<br>Nõutav | Töötaja kordumatu personalinumber. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Nõutav<br>Süsteemi loodud |  |
| **Perekonnanimi**<br>mshr_lastname<br>*String* | Kirjutuskaitstud<br>Nõutav | Töötaja perekonnanimi. |
| **Juriidilise isiku ID**<br>mshr_legalentityID<br>*String* | Kirjutuskaitstud<br>Nõutav | Määratleb juriidilise isiku (ettevõtte). |
| **Kehtiv alates**<br>mshr_namevalidfrom<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud <br>Nõutav | Töötajaga seotud teabe kehtivuse algkuupäev.  |
| **Sugu**<br>mshr_gender<br>*Int32* | Kirjutuskaitstud<br>Nõutav | Töötaja sugu. |
| **Palgatöötaja olemi ID**<br>mshr_payrollemployeeentityid<br>*GUID* | Nõutav<br>Süsteemi loodud | Süsteemi loodud GUID-väärtus töötaja kordumatuks tuvastamiseks. |
| **Töösuhte alguskuupäev**<br>mshr_employmentstartdate<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud<br>Nõutav | Töötaja tööhõive alguskuupäev. |
| **ID-tüübi ID**<br>mshr_identificationtypeid<br>*String* |Kirjutuskaitstud<br>Nõutav | Töötaja jaoks määratletud ID-tüüp. |
| **Töösuhte lõppkuupäev**<br>mshr_employmentenddate<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud<br>Nõutav |Töötaja tööhõive lõpukuupäev.  |
| **Andmeala ID**<br>mshr_dataareaid_id<br>*GUID* | Nõutav <br>Süsteemi loodud | Süsteemi loodud GUID-väärtus, mis identifitseerib juriidilise isiku (ettevõtte). |
| **Kehtiv kuni**<br>mshr_namevalidto<br>*Kuupäeva ja kellaaja nihe* |  Kirjutuskaitstud<br>Nõutav | Töötajaga seotud teabe kehtivuse lõpukuupäev. |
| **Sünnikuupäev**<br>mshr_birthdate<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud <br>Nõutav | Töötaja sünnikuupäev |
| **ID-number**<br>mshr_identificationnumber<br>*String* | Kirjutuskaitstud <br>Nõutav |Töötaja jaoks määratletud ID-number.  |
| **Eesnimi**<br>mshr_firstname<br>*String* | Kirjutuskaitstud<br>Nõutav | Töötaja eesnimi. |
| **Teine eesnimi**<br>mshr_middlename<br>*String* | Kirjutuskaitstud<br>Nõutav |Töötaja keskmine nimi.  |

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
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
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
