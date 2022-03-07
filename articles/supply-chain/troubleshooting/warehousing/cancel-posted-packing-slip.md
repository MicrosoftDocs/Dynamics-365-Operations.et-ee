---
title: Pärast müügitellimuse sisestamist ei saa saatelehte tühistada
description: Kui komplekteerimislehe ja saatmise protsessid on WMS-i jaoks lubatud, ei saa te saatelehte pärast müügitellimusest sisestamist tühistada. See leht pakub lahendust.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476173"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Pärast müügitellimusest sisestamist ei saa saatelehte tühistada

## <a name="symptoms"></a>Sümptomid

Kui komplekteerimis- ja saatmisprotsessid on lubatud warehouse management (WMS) jaoks, ei saa te saatelehte pärast müügitellimuse sisestamist tühistada.

## <a name="resolution"></a>Lahendus

WMS-i jaoks lubatud kaupade sisestatud saatelehtede korrigeerimiseks peab sisestus olema tehtud koormast, mitte otse tellimusest. Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.  

Üldiselt saab laohaldusprotsesside käigus korjatud ja kohale toimetatud müügitellimuse koorma või saadetise ja müügitellimuse dokumendi enda kohta saatelehte värskendada. Kui aga müügitellimuse müügitellimuse dokumendilt saatelehte värskendate, ei saa saatelehe tühistamist siiski teha koorma-või müügitellimusest. Seetõttu soovitame kasutada koormast saatelehe sisestamist. Sellisel juhul lubatakse tagasivõttu, mis tuleb teha koormast.
