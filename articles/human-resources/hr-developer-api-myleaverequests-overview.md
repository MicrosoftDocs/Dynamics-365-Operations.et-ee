---
title: MyLeaveRequestsi ülevaade
description: Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 90698ddcc8fcf0eb975dffed0bdad11e6b277c90
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984692"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequestsi ülevaade

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