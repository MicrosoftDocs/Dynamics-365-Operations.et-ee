---
title: Palgaarvestuse põhipalgaplaan
description: See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059084"
---
# <a name="payroll-fixed-compensation-plan"></a>Palgaarvestuse põhipalgaplaan

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema annab üksikasjad ja näidispäringu põhipalgaplaani olemi kohta rakenduses Dynamics 365 Human Resources.

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Töötaja ID**<br>mshr_fk_employee_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity  | Töötaja ID |
| **Tasumäär**<br>mshr_payrate<br>*Kümnendkoht* | Kirjutuskaitstud<br>Nõutav | Põhipalgaplaanis määratletud tasumäär. |
| **Plaani ID**<br>mshr_planid<br>*String* | Kirjutuskaitstud<br>Nõutav |Määrab palgaplaani.  |
| **Kehtiv alates**<br>mshr_validfrom<br>*Kuupäeva ja kellaaja nihe* |  Kirjutuskaitstud<br>Nõutav |Töötajaga seotud põhipalga kehtivuse algkuupäev.  |
| **Palgaarvestuse põhipalgaplaani olem**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Nõutav<br>Süsteemi loodud | Süsteemi loodud GUID-väärtus palgaplaani kordumatuks tuvastamiseks. |
| **Tasusagedus**<br>mshr_payfrequency<br>*String* | Kirjutuskaitstud<br>Nõutav |Töötajale makstava tasu maksmise sagedus.  |
| **Kehtiv kuni**<br>mshr_validto<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud <br>Nõutav | Töötajaga seotud põhipalga kehtivuse lõpukuupäev. |
| **Ametikoha ID**<br>mshr_positionid<br>*String* | Kirjutuskaitstud <br>Nõutav | Töötaja ja põhipalgaplaani registreerimisega seotud ID. |
| **Currency**<br>mshr_currency<br>*String* | Kirjutuskaitstud <br>Nõutav |Põhipalgaplaani jaoks määratletud valuuta   |
| **Personalinumber**<br>mshr_personnelnumber<br>*String* | Kirjutuskaitstud<br>Nõutav |Töötaja kordumatu personalinumber.  |

**Päring**

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Vastus**

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
