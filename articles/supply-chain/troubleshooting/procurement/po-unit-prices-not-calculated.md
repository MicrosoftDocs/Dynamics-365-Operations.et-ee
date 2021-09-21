---
title: Ostutellimuste ühiku hindasid ei arvutata ühikuteisenduse alusel
description: Ostutellimuste ühiku hindasid ei arvutata ühikuteisenduse alusel
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476115"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Ostutellimuste ühiku hindasid ei arvutata ühikuteisenduse alusel

## <a name="symptoms"></a>Sümptomid

Kui ostutellimusel muudetakse ühikut, ei arvutata kaubandusleppe hindu ühikuteisenduse määratluste alusel ümber.

## <a name="cause"></a>Põhjus

Hinnad võetakse alati kaubanduslepetest (või muudest süsteemis olevatest hinnasätetest, nt müügilepingutest või kauba hindadest) ja need määratakse ühikule.

Kui ühikut tellimuse real muudetakse, otsib süsteem uue ühiku jaoks üles hinna ja rakendab seda hinda. Kui ühiku jaoks ei leita hinda, ei rakenda süsteem hinda. Ühikuteisendust ei saa kasutada hinna ümberarvutamiseks teiseks ühikuks. Teoreetiliselt ei pruugi ühe kümmet kaupa sisaldava karbi hind võrduda kümne karbi hinnaga.

## <a name="workaround"></a>Vastukaal

Üks viis selle probleemi lahendamiseks on veenduda, et ühikute jaoks, mida hakatakse kauba puhul tellimuse ridadel kasutama, oleks olemas kaubanduslepped.
