---
title: Palga positsiooni töö
description: See teema annab üksikasjad ja näidispäringu Palgalise ametikoha olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: 62b9caf94f1c9aa8bb5758e62565fe57dfdd245a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055024"
---
# <a name="payroll-position-job"></a>Palga positsiooni töö

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema annab üksikasjad ja näidispäringu Palgalise töösuhte olemi kohta rakenduses Dynamics 365 Human Resources.

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Töö ID**<br>mshr_jobid<br>*String* | Kirjutuskaitstud<br>Nõutav |Töö ID. |
| **Kehtiv alates**<br>mshr_validto<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud <br>Nõutav | Kuupäev, millest alates ametikoht ja töösuhe kehtivad. |
| **Kehtiv kuni**<br>mshr_validto<br>*Kuupäeva ja kellaaja nihe* | Kirjutuskaitstud <br>Nõutav | Kuupäev, milleni ametikoht ja töösuhe kehtivad.  |
| **Ametikoha ID**<br>mshr_positionid<br>*String* | Kirjutuskaitstud<br>Nõutav | Ametikoha ID. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Nõutav<br>Süsteemi loodud |  |
| **Ametikoha töö ID väärtus**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |Ametikohaga seotud töö ID.|
| **Põhipalgaplaani ID**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | Põhipalgaplaaniga seotud töö ID. |
| **Palgaarvestuse töökoha olemi ID**<br>mshr_payrollpositionjobentityid<br>*Guid* | Nõutav<br>Süsteemi loodud. | Süsteemi loodud GUID-väärtus töö kordumatuks tuvastamiseks.  |

