---
title: Kui seerianumber on häälestatud, ei saa dimensiooni asukoht olla tühi
description: Kui saate selle vea saadetise kinnitamisel pärast seeriakaubale üleviimistellimuse loomist, on sissetuleku vaikeasukoha väli tühi.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476156"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Tõrge saadetise kinnitamisel pärast seeriakaubale üleviimistellimuse loomist

## <a name="symptoms"></a>Sümptomid

See tõrketeade kuvatakse, kui loote seeriaüksusele üleviimistellimuse, kasutades ladu, mis on lubatud täiustatud laohalduse (WMS) jaoks, ja proovite pärast töö lõpetamist saadetist kinnitada.

> Kui seerianumber on häälestatud, ei saa dimensiooni asukohta jätta tühjaks.

## <a name="cause"></a>Põhjus

See ilmub, kuna **Vastuvõtu vaikimisi asukoht** on "päritolu" lao transiidilao jaoks tühi.

## <a name="resolution"></a>Lahendus

Probleemi lahendamiseks määrake transiidilaos vaikimisi vastuvõtu asukoht. Veenduge, et see asukoht on identifitseerimisnumbritega kontrollitav.
