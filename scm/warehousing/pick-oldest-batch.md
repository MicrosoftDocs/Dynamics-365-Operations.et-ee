---
title: Vanima partii komplekteerimine mobiilsel seadmel
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada mobiilselt seadmelt vanima partii komplekteerimise valikuid.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: ee45fed40b10dbe913c73e1186b726a39831816d
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017


---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>Vanima partii komplekteerimine mobiilsel seadmel

[!include[banner](../includes/banner.md)]

Konfiguratsioonile **Komplekteeri vanim partii** pääseb juurde mobiilse seadme menüü kaudu ja see võimaldab sundida laotöötajaid või hoiatada neid, et nad komplekteeriksid oma praeguses asukohas vanima partii.  

## <a name="where-it-applies"></a>Kus see kehtib
Vanima partii komplekteerimine on konfigureeritud mobiilse seadme menüüelementides ja see käivitab allpool nimetatud kaupade partii komplekteerimise.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Vanima partii komplekteerimise konfiguratsiooni seadistamine 
Kaupade puhul, mis on seadistatud kasutama olemasolevat tööd, saab valiku **Komplekteeri vanim partii** olekuks määrata mobiilse seadme menüüst **Pole**, **Hoiata** või **Sunni**.

**Pole**: töötajad ei saa ühtegi teadet ja neil lubatakse komplekteerida nende asukohas ükskõik millist partiid.

**Hoiata** ja **Sunni**: kui töötaja valib partii, kuvatakse partii juhtelemendi kohal vanima aegumiskuupäevaga partii(de) loend. Kui asukohta juhitakse litsentsiplaadiga, siis kuvatakse litsentsiplaadi juhtelemendi kohal vanima partiiga litsentsiplaatide loend. 
-   **Hoiata**: kui töötaja valib litsentsiplaadi või partii, mida kuvatavas loendis pole, siis muutub juhtelement tühjaks ja kuvatakse hoiatus, et on olemas vanem partii, mida valida. Et saada luba töö jätkamiseks võib töötaja valida uuesti sama litsentsiplaadi või partii.  
-   **Sunni**: töötajad saavad jätkuvalt teate, et komplekteerimiseks on olemas vanem partii.

