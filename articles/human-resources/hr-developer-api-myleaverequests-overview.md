---
title: MyLeaveRequestsi ülevaade
description: Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803629"
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