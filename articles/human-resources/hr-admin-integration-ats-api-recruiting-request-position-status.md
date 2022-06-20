---
title: Värbamistaotluse ametikoha olek
description: See artikkel kirjeldab värbamise taotluse ametikoha oleku suvandit, mis on seatud väärtusele Dynamics 365 Human Resources.
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846403"
---
# <a name="recruiting-request-position-status"></a>Värbamistaotluse ametikoha olek


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab värbamise taotluse ametikoha oleku suvandit, mis on seatud väärtusele Dynamics 365 Human Resources.

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
