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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776772"
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
