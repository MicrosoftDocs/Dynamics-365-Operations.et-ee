---
title: Kaudsed kulud protsessiaruandes sisaldab kustutatud tootmist
description: Protsessi kaudsete kulude aruanne sisaldab teavet tootmistellimuste kohta, mis on osaliselt töödeldud ja hiljem kustutatud.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026440"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Kaudsed kulud protsessiaruandes sisaldab kustutatud tootmist

KB number: 4612748

## <a name="symptoms"></a>Sümptomid

**Protsessi kaudsete kulude aruanne** sisaldab teavet tootmistellimuste kohta, mis on osaliselt töödeldud ja hiljem kustutatud.

## <a name="resolution"></a>Eraldusvõime

Tootmistellimuse tühistamisel tühistate ka selle tootmistellimuse kõik kanded. Kui kustutate tootmistellimuse, jäävad alles alammooduli tabelid ja pearaamat ning kõik sellega seotud kanded. Aruannetes kuvatakse tehingud alamraamatu tabelites. Kindla tootmistellimuse netoväärtus peaks olema 0.00.
