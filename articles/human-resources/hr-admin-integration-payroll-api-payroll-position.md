---
title: Ametikohtade palga üksikasjad
description: See teema annab üksikasjad ja näidispäringu ametikohtade üksikasjade olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056776"
---
# <a name="payroll-position"></a>Palga positsioon

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema annab üksikasjad ja näidispäringu ametikohtade üksikasjade olemi kohta rakenduses Dynamics 365 Human Resources.

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Iga-aastased regulaarsed tunnid**<br>annualregularhours<br>*Kümnendkoht* | Kirjutuskaitstud<br>Nõutav | Ametikohal määratletud iga-aastased regulaarsed tunnid.  |
| **Palgaarvestuse ametikoha üksikasjade olemi ID**<br>payrollpositiondetailsentityid<br>*Guid* | Nõutav<br>Süsteemi loodud. | Süsteemi loodud GUID-väärtus ametikoha kordumatuks tuvastamiseks.  |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Nõutav<br>Süsteemi loodud |  |
| **Ametikoha töö ID väärtus**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |Ametikohaga seotud töö ID.|
| **Põhipalgaplaani ID**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | Põhipalgaplaaniga seotud töö ID. |
| **Palgatsükli ID**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Ametikohal määratletud palgatsükkel. |
| **Maksja juriidiline isik**<br>paidbylegalentity<br>*String* | Kirjutuskaitstud<br>Nõutav | Makse tegemise eest vastutaval ametikohal määratletud juriidiline isik. |
| **Ametikoha ID**<br>mshr_positionid<br>*String* | Kirjutuskaitstud<br>Nõutav | Ametikoha ID. |
| **Kehtiv kuni**<br>validto<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud<br>Nõutav |Kuupäev, millest alates ametikoha üksikasjad kehtivad.  |
| **Kehtiv alates**<br>validfrom<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud<br>Nõutav |Kuupäev, milleni ametikoha üksikasjad kehtivad.  |

**Päring**

**Taotlus**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Vastus**

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
