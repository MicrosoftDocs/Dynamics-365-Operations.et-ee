---
title: Asukoha litsentsiplaat peab olema määratud
description: Kui saate selle tõrke pärast WMS-toega lao ülekandekorralduse loomist, on transiitlao jaoks kättesaamise vaikimisi asukoht tühi.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476087"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Litsentsiplaadi spetsifikatsiooni tõrge üleviimistellimuse saadetise kinnitamisel

## <a name="symptoms"></a>Sümptomid

Kui loote üleviimistellimuse, kasutades ladu, mis on lubatud täiustatud warehouse management (WMS) jaoks, ja proovite pärast töö lõpetamist saadetist kinnitada, võite saada selle tõrketeate:

> Asukoha litsentsiplaat peab olema määratud.

## <a name="cause"></a>Põhjus

See ilmub, kuna **Vastuvõtu vaikimisi asukoht** on "päritolu" lao transiidilao jaoks tühi.

## <a name="resolution"></a>Lahendus

Probleemi lahendamiseks määrake transiidilaos vaikimisi vastuvõtu asukoht. Veenduge, et see asukoht on identifitseerimisnumbritega kontrollitav.
