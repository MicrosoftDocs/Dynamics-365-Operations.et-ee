---
title: Palgaarvestuse töötaja aadress
description: See teema annab üksikasjad ja näidispäringu Palgtöötaja aadressi olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 70e42cbf657a28327699d927731edd36de7c4a64
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069753"
---
# <a name="payroll-worker-address"></a>Palgaarvestuse töötaja aadress


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources palgatöötaja aadressi olemit.

Füüsiline nimi: mshr_payrollworkeraddressentity.

### <a name="description"></a>Kirjeldus

See üksus annab palgaarvestuse asukoha ja palgatöö asukoha antud töötaja kohta.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud | Töötaja kordumatu personalinumber. |
| **Asukoha ID**</br>mshr_locationidbr>*String* | Kirjutuskaitstud | Aadressi ID. |
| **Elab aadressil**</br>mshr_elabaadressil </br> *[suvandikomplekt mshr_noyes](hr-admin-integration-payroll-api-no-yes.md)* | Kirjutuskaitstud | Väärtus, mis näitab, kas aadress on seal, kus töötaja elab. |
| **Töötas aadressil** </br> mshr_töötasaadressilbr </br>*[suvandikomplekt mshr_noyes](hr-admin-integration-payroll-api-no-yes.md)* | Kirjutuskaitstud | Väärtus, mis näitab, kas aadress on seal, kus töötaja töötab. |
| **Riik/regioon**</br>mshr_countryregionid</br>*String* | Kirjutuskaitstud</br>Nõutav | Aadressi jaoks defineeritud riik või regioon. |
| **Sihtnumber**</br>mshr_zipcode<br>*String* | Kirjutuskaitstud | Töötaja jaoks määratletud ID-number. |
| **Tänav**</br>mshr_street</br>*String* | Kirjutuskaitstud | Aadressiks määratletud tänav. |
| **Linn**</br>mshr_city</br>*String* | Kirjutuskaitstud | Aadressiks määratletud linn. |
| **Maakond**</br>mshr_state</br>*String* | Kirjutuskaitstud | Aadressi jaoks defineeritud osariik või maakond. |
| **Maakond**</br>mshr_county</br>*String* | Kirjutuskaitstud | Aadressiks määratletud maakond. |
| **Kehtiv alates**</br>mshr_postaladdressvalidfrom</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Aadressi kehtimise alguskuupäev. |
| **Kehtiv kuni**</br>mshr_postaladdressvalidto</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud | Aadressi kehtimise lõpukuupäev. |
| **Esmane väli**</br>mshr_primaryfield</br>*String* | Kirjutuskaitstud | Esmane väli. |
| **Palgatöötaja aadressi ID**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Süsteemi loodud | Süsteemi loodud globaalse ainuidentifikaatori (GUID) väärtus aadressi unikaalseks tuvastamiseks. |

## <a name="relations"></a>Seosed

| Atribuudi väärtus | Seotud üksus | Navigeerimise atribuut | Kogumi tüüp |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Vastus**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
