---
title: MyLeaveRequestsi ülevaade
description: Microsofti üksus MyLeaveRequests Dynamics 365 Human Resources annab puhkusetaotluste loendi.
author: twheeloc
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20cc53ec3bcf38444ccf75f81e28d5efd9fc4537
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717051"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequestsi ülevaade


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
