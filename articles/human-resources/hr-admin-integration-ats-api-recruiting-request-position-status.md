---
title: Värbamistaotluse ametikoha olek
description: Selles teemas kirjeldatakse värbamisetaotluse ametikoha oleku suvandikomplekti rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051877"
---
# <a name="recruiting-request-position-status"></a>Värbamistaotluse ametikoha olek

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse värbamisetaotluse ametikoha oleku suvandikomplekti rakenduses Dynamics 365 Human Resources.

Füüsiline nimi: mshr_hcmrecruitingrequestpositionstatus

See loetelu annab olemis RecruitingRequestPosition iga värbamistaotluse ametikoha väärtuste oleku suvandikomplekti.

| Väärtus | Silt | Kirjeldus |
| --- | --- | --- |
| 200000000 | Avamine | Värbamistaotluse ametikoht on värbamiseks vaba. See ei näita, et ametikohale puuduksid hetkel aktiivesd ametikoha määramised. Värbamise ajal võib ametikohal töötaja olla. See näitab ainult seda, et ametikoht on värbamistaotluse kontekstis värbamiseks saadaval. |
| 200000001 | Täidetud | Töötaja on ametikohale määramiseks valitud. |
| 200000002 | Tühistatud | Taotlus sellele ametikohale värbamiseks on tühistatud. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]