---
title: Töö pole blokeeritud
description: Töö pole blokeeritud
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924200"
---
# <a name="work-isnt-blocked"></a>Töö pole blokeeritud

Tõrkekood: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Töö ID-ga %1 pole blokeeritud.

## <a name="cause"></a>Põhjus

**Blokeeritud voo** suvand on seatud väärtusele *Ei*. Töö blokeeringut ei saa eemaldada, kuna see pole praegu blokeeritud.

## <a name="resolution"></a>Eraldusvõime

 Ainult tööl, mille **Blokeeritud voo** suvand on seatud valikule *Jah* saab blokeeringu eemaldada.
