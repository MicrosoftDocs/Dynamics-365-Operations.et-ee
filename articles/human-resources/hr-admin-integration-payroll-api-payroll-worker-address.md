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
ms.openlocfilehash: 898ca7b33e39ec33990fecc4c3a7229620fbfddd5ce8ad14423af38047187e55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761970"
---
# <a name="payroll-worker-address"></a>Palgaarvestuse töötaja aadress

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources palgatöötaja aadressi olemit.

Füüsiline nimi: mshr_payrollworkeraddressentity.

### <a name="description"></a>Kirjeldus

See üksus annab palgaarvestuse asukoha ja palgatöö asukoha antud töötaja kohta.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Linn**</br>mshr_city</br>*String* | Kirjutuskaitstud</br>Nõutav | Määratletud linna aadress.   |
| **Personalinumber**</br>mshr_personnelnumber</br>*String* | Kirjutuskaitstud</br>Nõutav | Töötaja kordumatu personalinumber.  |
| **Riik/regioon**</br>mshr_countryregionid</br>*String* | Kirjutuskaitstud</br>Nõutav | Aadressi jaoks defineeritud riigi regioon.  |
| **Kehtiv alates**</br>mshr_postaladdressvalidfrom</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud </br>Nõutav | Aadressi kehtimise alguskuupäev. |
| **Töötas aadressil** </br> mshr_töötasaadressilbr </br>*[suvandikomplekt mshr_noyes](hr-admin-integration-payroll-api-no-yes.md)* | Kirjutuskaitstud</br>Nõutav | Näitab, kas aadress on töötaja töökohaks. |
| **Maakond**</br>mshr_county</br>*String* | Kirjutuskaitstud</br>Nõutav | Määratletud riigi aadress.  |
| **Palgatöötaja aadressi ID**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Nõutav</br>Süsteemi loodud | Süsteemi loodud GUID-väärtus aadressi kordumatuks tuvastamiseks.  |
| **Esmane väli**</br>mshr_primaryfield</br>*String* | Kirjutuskaitstud</br>Nõutav |  |
| **Tänav**</br>mshr_street</br>*String* | Kirjutuskaitstud</br>Nõutav | Aadressis määratletud tänav. |
| **Kehtiv kuni**</br>mshr_postaladdressvalidto</br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud </br>Nõutav | Aadressi kehtimise lõpukuupäev.  |
| **Asukoha ID**</br>mshr_locationidbr>*String* | Kirjutuskaitstud <br>Nõutav | Aadressi ID.  |
| **Sihtnumber**</br>mshr_zipcode<br>*String* | Kirjutuskaitstud <br>Nõutav |Töötaja jaoks määratletud ID-number.  |
| **Elab aadressil**</br>mshr_elabaadressil </br> *[suvandikomplekt mshr_noyes](hr-admin-integration-payroll-api-no-yes.md)* | Kirjutuskaitstud</br>Nõutav | Näitab, kas aadress on töötaja elukohaks. |
| **Maakond**</br>mshr_state</br>*String* | Kirjutuskaitstud</br>Nõutav | Aadressis määratletud maakond.  |

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
