---
title: MyLeaveRequestsi ülevaade
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008747"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequestsi ülevaade

Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.

## <a name="key"></a>Võti

  | Atribuudi nimi | Andmetüüp |
  |---------------|-----------|
  | dataAreaId    | String    |
  | RequestId     | String    |
  | LeaveType     | String    |
  | LeaveDate     | Kuupäev      |
  
## <a name="properties"></a>Atribuudid

  | Atribuudi nimi     | Andmetüüp | Nõutav |
  |-------------------|-----------|----------|
  | dataAreaId        | String    | X        |
  | RequestId         | String    | X        |
  | LeaveType         | String    | X        |
  | LeaveDate         | Kuupäev      | X        |
  | ReasonCodeId      | String    |          |
  | PersonnelNumber   | String    | X        |
  | RequestDate       | Kuupäev      | X        |
  | Kommentaar           | String    |          |
  | Olek            | Loetelu      | X        |
  | Summa            | Tegelik      |          |
  | HalfDayDefinition | Loetelu      |          |

## <a name="actions"></a>Tegevused

 | Tegevuse nimi                               | Kirjeldus                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [esita](hr-developer-api-myleaverequests-submit.md)   | Esitage taotlus töövoo poolt töötlemiseks.. |

## <a name="see-also"></a>Vt ka

- [Puhkusetaotluse edastamine töövoogu](hr-developer-api-myleaverequests-submit.md)
- [Autentimine](hr-developer-api-authentication.md)