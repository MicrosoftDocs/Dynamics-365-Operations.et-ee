---
title: Asukohaprofiil keelab negatiivsed varud, kuid negatiivne käsivarude loend on lubatud
description: Asukohaprofiili valik Luba negatiivne varu väärtuseks on seatud Ei, kuid süsteem lubab siiski negatiivset käsivarude loendit.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 2a7345281301ee70a512dfadcd553cb4eb33003904d0dddf6967659b693f60d7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742604"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Asukohaprofiil keelab negatiivsed varud, kuid negatiivne käsivarude loend on lubatud

KB number: 4613622

## <a name="symptoms"></a>Sümptomid

Asukohaprofiili valik **Luba negatiivne varu** väärtuseks on seatud *Ei*, kuid süsteem lubab siiski negatiivset käsivarude loendit.

## <a name="example-scenario"></a>Näidisstsenaarium

Valitsuse reguleeritud kannete puhul peab süsteem saama kirjendada negatiivseid varusid kahjumite reserveerimiseks. Soovite, et kaubal oleks võimalik näidata negatiivset laovaru, kuid ainult määratud asukohtades, nagu näiteks saadetav. Kui aga kauba mudeligrupp lubab negatiivset laovaru, siis leiate, et pole oluline, kas asukoht on seatud lubama negatiivset laovaru. Kui kaup on seadistatud nii, et negatiivne laovaru ei ole lubatud, pole oluline, kuidas asukoha profiil seadistatakse.

## <a name="resolution"></a>Eraldusvõime

Säte **Luba negatiivne laovaru** asukohaprofiilist kehtib ainult laoprotsessidele, nt komplekteerimisele. Kauba mudeligrupid, mis on seadistatud lubama negatiivset laovaru, mõjutavad kõiki laohalduse ja laohalduse mooduli protsesse ning asukohaprofiil ei alista seadistust.

Saate kontrollida, kas laol on lubatud negatiivseid varusid kanda. Seadistage kaubamudeligrupid keelama negatiivset füüsilist laovaru ning seadistama negatiivse laovaru lubamiseks ainult vastava lao.
