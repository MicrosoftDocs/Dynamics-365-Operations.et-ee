---
title: Värbamistaotluse olek
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125950"
---
# <a name="recruiting-request-status"></a>Värbamistaotluse olek

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.

Füüsiline nimi: mshr_hcmrecruitingrequeststatus

See loetelu annab kandidaatide värbamistaotluste oleku väärtuste suvandikomplekti.

| Väärtus | Silt | Kirjeldus |
| --- | --- | --- |
| 200000000 | Mustand | Taotlus on mustandis ja ei ole valmis aktiivseks värbamiseks. |
| 200000001 | Ülevaatamisel | Taotlus on esitatud ja töövoog suunab selle kinnitamiseks. Saadaval ainult siis, kui töövoog on lubatud. |
| 200000002 | Ootel | Taotlus on töövoo tegevuse ootel. Saadaval ainult siis, kui töövoog on lubatud. |
| 200000003 | Tühistatud | Taotlus on tühistatud. Saadaval ainult siis, kui töövoog on lubatud. |
| 200000004 | Keelatud | Taotlusest keelduti. Saadaval ainult siis, kui töövoog on lubatud. |
| 200000005 | Aktiivne | Mis tahes töövoog on lõpetatud ja kinnitatud ning taotlus on aktiivseks värbamiseks valmis. |
| 200000006 | Suletud | Värbamistaotlus on suletud. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)
