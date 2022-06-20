---
title: Palgaarvestuse integratsiooni parameetrid
description: See artikkel kirjeldab Dynamics 365 Human Resources Palga integratsiooni parameetreid.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d784909fc8c5fa05557566b62b19802cd2acece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896093"
---
# <a name="payroll-integration-parameters"></a>Palgaarvestuse integratsiooni parameetrid


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Enne palga Dynamics 365 Human Resources integreerimist peate seadistama selles artiklis kirjeldatud parameetrid.

## <a name="enable-payroll-address"></a>Luba palgaarvestuse aadress

Et saada palgaaadressi kasutada, peate selle lubama palgaarvestuse [jagatud parameetrite vormi](hr-setup-shared-parameters.md) palgaarvestuse integreerimise vahekaardil.

## <a name="define-the-identification-type"></a>Määrake idendifitseerimise tüüp

ID-tüübi ID tuvastamiseks [palgaarvestuse töötaja üksuses](hr-admin-integration-payroll-api-payroll-employee.md) peate [konfigureerima inimressursside parameetrid](hr-setup-shared-parameters.md) iga ettevõtte jaoks.

1. Tööruumis **Hüvitiste haldus**, jaotises lingid, valige suvand **Inimressursside parameetrid**. 
2. Määratlege **palgaarvestuse integreerimise** vahekaardil järgmiste väljade väärtus.

| Field | Kirjeldus |
| --- | --- |
| Kasuta palgaarvestuses ID tüüpe | Kui see suvand on valitud, kuvatakse valitud tüübi ID palga töötaja üksuses. |
| ID tüüp | Idendifitseerimise tüüp kuvatakse väljal **mshr_palgatöötajaüksuseid** suvandist [palgatöötaja üksus](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>Vt ka

[Palgaarvestuse integratsiooni API tutvustus](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
