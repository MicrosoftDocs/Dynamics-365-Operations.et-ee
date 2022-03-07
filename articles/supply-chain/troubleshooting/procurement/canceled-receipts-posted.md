---
title: Pange tähele, et peatatud pearaamatukontodele saab kandeid sisestada
description: Kui toote sissetulek tühistatakse, lubab süsteem sisestada kandeid peatatud pearaamatukontodele, kuigi põhikontod on peatatud
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476168"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Pange tähele, et peatatud pearaamatukontodele saab kandeid sisestada

## <a name="symptoms"></a>Sümptomid

Kui toote sissetulek tühistatakse, lubab süsteem sisestada kandeid peatatud pearaamatukontodele, kuigi põhikontod on peatatud.

## <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Veenduge, et lehe **Ostureskontro parameetrid** vahekaardil **Üldine** oleks suvandi **Sisesta toote sissetulek pearaamatusse** väärtuseks seatud *Jah*.
1. Looge ostutellimus ja lisage tellimuse rida, mille toote kogus on *1000*.
1. Kinnitage ostutellimus.
1. Sisestage toote sissetulek ja kontrollige kandeid.
1. Peatage asjakohased põhikontod *200140* ja *140200*.
1. Tühistage sisestatud toote sissetulek.
1. Pange tähele, et peatatud pearaamatukontodele saab kandeid sisestada.

## <a name="resolution"></a>Lahendus

Kandeid saab toote sissetulekute tühistamise korral peatatud pearaamatukontodele sisestada, kuna selline olukord lubab teha õigeid sisestusi.
