---
title: Töö vabastuse olek
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Töö vabastuse olek.
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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464448"
---
# <a name="job-exempt-status"></a>Töö vabastuse olek

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources suvandikomplekti Töö vabastuse olek.

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