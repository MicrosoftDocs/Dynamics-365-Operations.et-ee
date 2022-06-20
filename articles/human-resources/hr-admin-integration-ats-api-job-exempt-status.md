---
title: Töö vabastuse olek
description: See artikkel kirjeldab töövabastuse oleku valikut, mille jaoks on määratud Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894668"
---
# <a name="job-exempt-status"></a>Töö vabastuse olek


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab töövabastuse oleku valikut, mille jaoks on määratud Dynamics 365 Human Resources.

Füüsiline nimi: cdm_jobexemptstatus

Selles loetelus määratakse FLSA töö vabastuse oleku väärtuste suvandikomplekt. See on esitatud olemasolevas suvandikomplektis cdm_jobexemptstatus.

| Väärtus | Silt | Kirjeldus |
| --- | --- | --- |
| 200000000 | Vabastus | Tööl on FLSA juhiste põhjal vabastatud olek. |
| 200000001 | NonExempt | Tööl on FLSA juhiste põhjal mittevabastatud olek. |
| 200000002 | Ei rakendu | FLSA oleku juhised ei rakendu tööle. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
