---
title: Vanima partii komplekteerimine mobiilsel seadmel
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada mobiilselt seadmelt vanima partii komplekteerimise valikuid.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb0012689cc814daaf8f685c81d4630164b6e0c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810434"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a>Vanima partii komplekteerimine mobiilsel seadmel

[!include [banner](../includes/banner.md)]

Konfiguratsioonile **Komplekteeri vanim partii** pääseb juurde mobiilse seadme menüü kaudu ja see võimaldab sundida laotöötajaid või hoiatada neid, et nad komplekteeriksid oma praeguses asukohas vanima partii.  

## <a name="where-it-applies"></a>Kus see kehtib
Vanima partii komplekteerimine on konfigureeritud mobiilse seadme menüüelementides ja see käivitab allpool nimetatud kaupade partii komplekteerimise.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Vanima partii komplekteerimise konfiguratsiooni seadistamine 
Kaupade puhul, mis on seadistatud kasutama olemasolevat tööd, saab valiku **Komplekteeri vanim partii** olekuks määrata mobiilse seadme menüüst **Pole**, **Hoiata** või **Sunni**.

**Pole**: töötajad ei saa ühtegi teadet ja neil lubatakse komplekteerida nende asukohas ükskõik millist partiid.

**Hoiata** ja **Sunni**: kui töötaja valib partii, kuvatakse partii juhtelemendi kohal vanima aegumiskuupäevaga partii(de) loend. Kui asukohta juhitakse litsentsiplaadiga, siis kuvatakse litsentsiplaadi juhtelemendi kohal vanima partiiga litsentsiplaatide loend. 
-   **Hoiata**: kui töötaja valib litsentsiplaadi või partii, mida kuvatavas loendis pole, siis muutub juhtelement tühjaks ja kuvatakse hoiatus, et on olemas vanem partii, mida valida. Et saada luba töö jätkamiseks võib töötaja valida uuesti sama litsentsiplaadi või partii.  
-   **Sunni**: töötajad saavad jätkuvalt teate, et komplekteerimiseks on olemas vanem partii.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]