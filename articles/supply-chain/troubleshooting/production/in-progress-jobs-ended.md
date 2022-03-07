---
title: Pooleli olevad tööd lõpevad viimase töö osalise koguse aruandlusega
description: Kui ma kasutan töökaardi seadet, et teatada osalisest kogusest tootmistellimuse viimasel tööl, lõpetatakse automaatselt kõik selle tellimuse varasemad tööd, mille olekuks on seatud pooleli.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476162"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Pooleli olevad tööd lõpevad viimase töö osalise koguse aruandlusega

## <a name="symptoms"></a>Sümptomid

Kui ma kasutan töökaardi seadet, et teatada osalisest kogusest tootmistellimuse viimasel tööl, lõpetatakse automaatselt kõik selle tellimuse varasemad tööd, mille olekuks on seatud pooleli.

## <a name="resolution"></a>Lahendus

Selline käitumine on nii kavandatud. **Tootmistellimuse vaikesätted** lehel **Kinnita lõpetatuks** vahekaardil on suvand nimega **Lõpp-märgistuse protsess**. Kui see teema on seatud väärtusele *Jah*, sisestatakse protsessikaardi tööleht, kui töötaja kasutab viimase operatsiooni kohta töökaardi seadet või töökaardi terminali. See tööleht märgib kõik operatsioonid lõpetatuks ja lõpetab kõik tootmistööd. Kui **Lõpp-märgistamise protsessi** suvandi väärtuseks on seatud *Jah*, ei arvesta süsteem töö olekut, mille töötaja valis viimase operatsiooni käigus. Süsteem ei võta arvesse ka seda, kas töötaja teatab täielikust või osalisest kogusest.
