---
title: Plaanitud tellimused võtaksid uuendamiseks kaua aega
description: Plaanitud tellimuse vajaduse koguse ja/või tarnekuupäeva uuendamisel võtab see tavaliselt aega vähemalt 30 sekundit, et värskendust salvestada
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476133"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Plaanitud tellimused võtaksid uuendamiseks kaua aega

## <a name="symptoms"></a>Sümptomid

Plaanitud tellimuse vajaduse koguse ja/või tarnekuupäeva uuendamisel võtab see tavaliselt aega vähemalt 30 sekundit, et värskendust salvestada.

## <a name="resolution"></a>Lahendus

See on teadaolev probleem sisseehitatud koondplaneerimise mootoriga. Selle põhjuseks on aluseks olev automaatne tükeldamine koosluse struktuuri kaudu redigeerimisel. Seda probleemi käsitletakse planeerimise optimeerimisel, kus planeerija saab vastavaid tellimusi värskendada ja kinnitada ning soovi korral käivitab planeerimise käivitamise, et värskendada aluseks oleva koosluse struktuuri jaoks plaanitud tellimusi.

Üks viis jõudluse parandamiseks sisseehitatud koondplaneerimise mootoriga on teha järgmist:

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige plaan.
1. Laiendage **Ajapiir päevades** FastTab.
1. Seadke **Tükeldamine** väärtusele *Jah* ja seadke selle sätte all oleva välja väärtuseks 0 (null).

> [!NOTE]
> See piirab selle koondplaani jaoks teostatavate tükeldamiste perioodi ühele päevale.
