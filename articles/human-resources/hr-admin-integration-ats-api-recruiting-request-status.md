---
title: Värbamistaotluse olek
description: See artikkel kirjeldab värbamistaotluse oleku suvandit, mis on seatud väärtusele Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859600"
---
# <a name="recruiting-request-status"></a>Värbamistaotluse olek


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab värbamistaotluse oleku suvandit, mis on seatud väärtusele Dynamics 365 Human Resources.

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
