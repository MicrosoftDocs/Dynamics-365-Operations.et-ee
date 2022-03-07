---
title: Müügitellimust ei saanud väljastada väljaminevate laotoimingutega
description: On mitu põhjust, miks võite saada tõrketeate, et müügitellimust ei saanud välja lasta. See lehekülg selgitab, miks ja kuidas probleemi lahendada.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476135"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Müügitellimust ei saanud väljastada väljaminevate laotoimingutega

## <a name="symptoms"></a>Sümptomid

Väljaminevate laotoimingutega töötamisel võite saada järgmise tõrketeate:

> Müügitellimust ei saanud väljastada.

## <a name="cause"></a>Põhjus

See probleem võib ilmneda mitmel põhjusel. Näiteks on tellimus krediidihalduses ja ühtegi saadetist ei saa luua enne, kui kõigi müügitellimusega seotud müügiridade jaoks on sisestatud kehtiv postiaadress. Teise võimalusena võib olla ootel tellimus, millega tuleb tegeleda enne, kui tellimuse saab lattu väljastada. See ootele panemine võib olla seotud tellimusega või see võib olla tingitud kliendi kontost.

## <a name="resolution"></a>Lahendus

Lisage või värskendage aadressi müügitellimuse ja tellimuse ridadel ning seejärel väljastage tellimus lattu. Tellimusi saab lattu väljastada ainult siis, kui neil on kehtiv tarneaadress (iga **Organisatsiooni halduse** moodulis oleva aadressi vormingu seadistuse kohta).

Uurige tellimuse ootelepanekut ja lahendage probleemid. Seejärel eemaldage ootele panemine tellimuselt või kliendilt ja väljastage tellimus lattu.
