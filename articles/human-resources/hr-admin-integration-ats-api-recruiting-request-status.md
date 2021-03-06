---
title: Värbamistaotluse olek
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Värbamistaotluse olek.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059180"
---
# <a name="recruiting-request-status"></a>Värbamistaotluse olek

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]