---
title: Plaanitud tellimused luuakse laos koos tootmistellimustega
description: Plaanitud tellimused luuakse ka siis, kui teil on laos ja tootmistellimustes kaubad juba olemas
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
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476169"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Plaanitud tellimused luuakse laos koos tootmistellimustega

## <a name="symptoms"></a>Sümptomid

Plaanitud tellimused luuakse ka siis, kui teil on laos ja tootmistellimustes kaubad juba olemas.

## <a name="resolution"></a>Lahendus

Võimalik, et saate selle probleemi lahendada, suurendades vastavate gruppide **Positiivsete päevade** väärtust **Laovarude grupi** lehel. See muudatus paneb süsteemi määratlema, kas vaba kaubavaru saab nõudluse jaoks kasutada. Seejärel ei looda laos olevate kaupade jaoks uut plaanitud tellimust.
