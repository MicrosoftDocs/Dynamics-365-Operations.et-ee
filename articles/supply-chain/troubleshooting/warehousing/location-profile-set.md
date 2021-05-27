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
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026437"
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
