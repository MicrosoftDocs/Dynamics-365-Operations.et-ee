---
title: Süsteem ei leia mitme tellimuse operatsioonide ajal plaanitud tellimust
description: Tõrge "Plaanitud tellimust pole olemas", kui sooritate toiminguid mitmel plaanitud tellimusel ja vähemalt kaks tellimust kuuluvad samale kauba ID-le.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920850"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Süsteem ei leia mitme tellimuse operatsioonide ajal plaanitud tellimust

Tõrkekood: SYS24774

## <a name="symptoms"></a>Sümptomid

Kui proovite korraga sooritada toimingut mitmel plaanitud tellimusel ja vähemalt kaks tellimust kuuluvad sama kauba ID-sse, saate järgmise tõrketeate. Näiteks võib tõrge ilmneda, kui tellimused on kindlad või nende tellimuse tüüpi muudetakse.

> Plaanitud tellimust %1 pole olemas.

## <a name="cause"></a>Põhjus

Kui süsteem tellimuse tüüpi tagab või muudab, peab see kauba olemasolevad plaanitud tellimused üle vaatama, tagamaks, et plaanitud pakkumine vastaks nõudlusele ja olemasolevale tarnele. Osana sellest protsessist loob süsteem kaubale uuesti plaanitud tellimused. Seetõttu pole teist plaanitud tellimust, mida süsteem eeldab, enam ei töödelda.

## <a name="workaround"></a>Vastukaal

Kinnitage tellimused enne nende töötlemiseks. Sel viisil tellimusi ei kustutata, kui süsteem töötleb kauba esimest tellimust.
