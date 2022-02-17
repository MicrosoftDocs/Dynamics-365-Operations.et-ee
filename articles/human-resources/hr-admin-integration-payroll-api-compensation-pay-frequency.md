---
title: Tasu tasusagedus
description: See teema annab üksikasjad ja näidispäringu kompensatsiooni maksmise sageduse üksuse kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 171b7fb7b361bd1fe2e7e637cd555c88a81a8bcf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066139"
---
# <a name="compensation-pay-frequency"></a>Tasu tasusagedus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse kompensatsiooni maksmise sageduse üksust rakenduses Dynamics 365 Human Resources.

Füüsiline nimi: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Kirjeldus

See üksus pakub teavet tasumäära teisendamise kohta antud kompensatsiooni maksmise sageduse puhul.

## <a name="properties"></a>Atribuudid

| Atribuut</br>**Füüsiline nimi**</br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Aastase tasumäära teisendamine**</br>mshr_annualconversionfactor</br>*Kümnendkoht* | Kirjutuskaitstud | Maksesageduse aastane teisendustegur. |
| **Kirjeldus**</br>mshr_description</br>*String* | Kirjutuskaitstud | Teisenduskursi kirjeldus. |
| **Tunnitasu teisendamine**</br>mshr_hourlyconversionfactor</br>*Kümnendkoht* | Kirjutuskaitstud | Maksesageduse igatunnine teisendustegur. |
| **Kuutasu teisendamine**</br>mshr_monthlyconversionfactor</br>*Kümnendkoht* | Kirjutuskaitstud | Maksesageduse igakuine teisendustegur. |
| **Palgamäära teisendamine**</br>mshr_payrateconversion</br>*String* | Kirjutuskaitstud | Unikaalne string teisenduse määra tuvastamiseks. |
| **Periood**</br>mshr_period</br>*perioodi suvandikomplekt* | Kirjutuskaitstud | Antud tasumäära teisendamise põhiperiood. |
| **Nädalatasu teisendamine**</br>mshr_weeklyconversionfactor</br>*Kümnendkoht* | Kirjutuskaitstud | Maksesageduse iganädalane teisendustegur. |
| **Andmeala id**</br>mshr_dataareaid</br>*String* | Kirjutuskaitstud | Juriidiline isik (ettevõtte). |
| **Kompensatsiooni tasusageduse olemi ID**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Süsteemi loodud | Süsteemi loodud globaalse ainuidentifikaatori (GUID) väärtus kirje unikaalseks tuvastamiseks. |

## <a name="example-query-for-payroll-employee"></a>Palgatöötaja näidispäring

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Vastus**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
