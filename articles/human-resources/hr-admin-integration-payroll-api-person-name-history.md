---
title: Isiku nime ajalugu
description: See teema annab üksikasjad ja näidispäringu isiku nime ajaloo üksuse kohta rakenduses Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 418047a0643ee29b89763dbe2b030753f405b575
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559639"
---
# <a name="person-name-history"></a>Isiku nime ajalugu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse isiku nime ajalugu rakenduses Dynamics 365 Human Resources.

Füüsiline nimi: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Kirjeldus

See üksus annab teavet antud isiku nime ajaloo kohta.

> [!IMPORTANT] 
> Väljad **Eesnimi**, **TeineEesnimi**, **Perekonnanimi**, **NimiKehtivAlates** ja **NimiKehtivKuni** pole enam palgaarvestuse töötaja üksuse jaoks saadaval. Need on eemaldatud tagamaks, et seda üksust toetab ainult üks kuupäevast tõhus andmeallikas.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Eesnimi**</br>mshr_firstname</br>*String* | Kirjutuskaitstud | Eesnimi. |
| **Perekonnanime eesliide**</br>mshr_lastnameprefix</br>*String*) | Kirjutuskaitstud | Perekonnanime eesliide. |
| **Perekonnanimi**</br>mshr_lastname</br>*String*) | Kirjutuskaitstud | Perekonnanimi. |
| **Teine eesnimi**</br>mshr_middlename</br>*String*) | Kirjutuskaitstud | Teine eesnimi. |
| **Kehtiv kuni**</br>mshr_validto</br>*String*) | Kirjutuskaitstud | Nime kehtimise lõpukuupäev. |
| **Osapoole number**</br>mshr_partynumber</br>*String* | Kirjutuskaitstud | Isiku süsteemi loodud kordumatu kasutaja poolt loetav identifikaator. |
| **Esmane väli**</br>mshr_primaryfield</br>*String* | Kirjutuskaitstud | Kirje ainuidentifikaator. |
| **Isiku nime ajalooüksuse ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Süsteemi loodud | Süsteemi loodud globaalse ainuidentifikaatori (GUID) väärtus kirje unikaalseks tuvastamiseks. |

## <a name="relations"></a>Seosed

| Atribuudi väärtus | Seotud üksus | Navigeerimise atribuut | Kogumi tüüp |
| --- | --- | --- | --- |
| Pole kohaldatav | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Pole kohaldatav | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Palgatöötaja näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Vastus**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
