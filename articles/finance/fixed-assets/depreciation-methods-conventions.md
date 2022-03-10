---
title: Kulumimeetodid ja kulumiarvestusreeglid
description: See artikkel annab ülevaate Microsoft Dynamics 365 Finance'is toetatud kulumiarvestusreeglitest ja -meetoditest.
author: moaamer
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f0f3b8be86225fd68df9b099e5c8e13a220a213
ms.sourcegitcommit: a5861c2fef4071e130208ad20e26cb3a42a45cf1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2021
ms.locfileid: "7927425"
---
# <a name="depreciation-methods-and-conventions"></a>Kulumimeetodid ja kulumiarvestusreeglid

[!include [banner](../includes/banner.md)]

See artikkel annab ülevaate toetatud kulumiarvestusreeglitest ja -meetoditest.

Saate valida mitmesuguste kulumimeetodite ja kulumiarvestusreeglite hulgast. Meetodi eesmärk on põhivara amortiseeruva väärtuse jaotamine rahandusperioodidele. Põhivara amortiseeruv väärtus on mahakandmismaksumuse võrra (kui see on kasutusel) vähendatud soetamismaksumus. 

Kui kasutate kulumiarvestusreegleid ja muudate vara viimase kulumiarvestuse käituskuupäeva, mis seejärel põhjustab mõne kulumi vahelejätmist, võib viimase aasta kulum olla oodatust suurem või väiksem. Kulumit korrigeeritakse viimase kulumikäituskuupäeva muutmisega mõjutatavate kulumiperioodide arvuga.

Näiteks kui kasutate poolaasta kulumireeglit kolme aasta puhul, kestab kulumiarvestus tavaliselt kolm ja pool aastat. Kui muudate kolme ja poole aasta jooksul viimast kulumiarvestuskuupäeva, siis viimasel kulumiaastal mõjutatud perioodide arv suureneb. Kui viite kuupäeva edasi kolme kuu võrra, arvestatakse viimasel aastal kulumit tavalise kuue kuu asemel üheksa kuu eest.

Kulumiarvestusreegli saate valida järgmisest loendist.


-   Poolaasta
-   Terve kuu
-   Kvartali keskel
-   Kuu keskel (kuu 1. päev)
-   Kuu keskel (kuu 15. päev)
-   Poolaasta (aasta algus)
-   Poolaasta (järgmine aasta)

Saate valida järgmiste kulumimeetodite hulgast.
-   Tööea lineo
-   Vähenev saldo
-   Käsitsi
-   Tegur
-   Tarbimine
-   Otse-joone allesjäänud elu
-   200% vähenev saldo
-   175% vähenev saldo
-   150% vähenev saldo
-   125% vähenev saldo





## <a name="additional-resources"></a>Lisaressursid

[Põhivara kulum](fixed-asset-depreciation.md)

[Otse-joone teenuselu kulum](Straight-line-service-life-depreciation.md)

[Väheneva jääkväärtuse kuluarvestusmeetod](reduce-balance-depreciation.md)

[Käsitsi kulumiarvestus](manual-depreciation.md)

[Kulumiarvestus kordaja alusel](factor-depreciation.md)

[Tarbimise kulum](consumption-depreciation.md)

[Otse-joone eluea allesjäänud kulum](straight-line-life-remaining-depreciation.md)

[125 protsenti väheneva saldoga kulum](125-percent-reducing-balance-depreciation.md)

[150 protsenti väheneva saldoga kulum](150-percent-reducing-balance-depreciation.md)

[175 protsenti väheneva saldoga kulum](175-percent-reducing-balance-depreciation.md)

[200 protsenti väheneva saldoga kulum](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
