---
title: Kaal peab olema positiivne
description: Kaal peab olema positiivne
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924299"
---
# <a name="weight-must-be-positive"></a>Kaal peab olema positiivne

Tõrkekood: WeightMustBePositive

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Kaal peab olema positiivne.

## <a name="cause"></a>Põhjus

**Brutokaalu** väli on seatud väärtusele *0* (null) või negatiivsele väärtusele.

## <a name="resolution"></a>Eraldusvõime

Kaalu määratlemiseks järgige ühte järgmistest sammudest.

- Seadke väärtus väljale **Brutokaal**. Siis valige ripploendist ühik.
- Valige **Hangi süsteemi kaal** et arvestada  **Brutokaalu** väärtus.
