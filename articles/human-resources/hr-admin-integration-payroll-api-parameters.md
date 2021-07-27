---
title: Palgaarvestuse integratsiooni parameetrid
description: See teema kirjeldab Dynamics 365 Human Resources palgaarvestuse integratsiooni parameetreid.
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
ms.openlocfilehash: 5f76ce395d7f5a82ab622dd323aee52a39b09847
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314370"
---
# <a name="payroll-integration-parameters"></a>Palgaarvestuse integratsiooni parameetrid

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Enne Dynamics 365 Human Resources palgaarvestuse integreerimist peate seadistama selles teemas kirjeldatud parameetrid.

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
