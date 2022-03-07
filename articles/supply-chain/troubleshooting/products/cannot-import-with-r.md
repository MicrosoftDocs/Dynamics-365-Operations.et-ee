---
title: Väljastatud tooted V2 üksuse abil ei saa kaupa importida
description: Üksust Released kasutades välja antud tooted V2 ei saa importida.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764688"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Väljastatud tooted V2 üksuse abil ei saa kaupa importida

KB number: 4611825

## <a name="symptoms"></a>Sümptomid

Kui proovite kaupa importida, kasutades üksust *Väljastatud tooted V2* saate tõrketeate, mis sarnaneb järgmise näitega:

> Kirjeid ei saa luua rakenduses Items – jälgides dimensioonigruppe (EcoResTrackingDimensionGroupItem). Kauba number: 2040663, partii. Kirje on juba olemas.

## <a name="resolution"></a>Eraldusvõime

Uute väljastatud toodete importimiseks peate *Väljastatud toote loomise V2* üksuse kasutama üksuse *Väljastatud tooted V2* asemel.
