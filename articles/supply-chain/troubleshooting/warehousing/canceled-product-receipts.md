---
title: Tühistatud toote kviitungid ei värskenda kande olekut olekusse Registreeritud
description: Kui olete tühistanud toote kviitungid sissetuleval kaubal, uuendab süsteem automaatselt laokande olekut olekust Saadud olekuks Tellitud.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731099"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Tühistatud toote kviitungid ei värskenda kande olekut olekusse Registreeritud

## <a name="symptoms"></a>Sümptomid

Kui olete käivitanud toimingu **Tühista toote kviitungid** sissetulevale kaubale, uuendab süsteem automaatselt laokande olekut olekust *Saadud* olekuks *Tellitud*.

## <a name="resolution"></a>Lahendus

Väljamineva kauba saatelehtede tühistamisel jääb laokannete olekuks *Valitud*. Kui sissetulevast kaubast toote sissetulekud tühistatakse, ei taastata laokannete olekuks *Registreeritud*. Seetõttu peab laotöötaja pärast sissetulevast kaubast toote sissetuleku tühistamist kaubakogused selle jaoks uuesti registreerima.

Lisateavet vt jaotisest [Sissetuleva kaubaga saabuvate kaubakoguste registreerimine](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
