---
title: Koondplaneerimine loob fiktiivsetele toodetele plaanitud tellimused
description: Koondplaneerimine loob plaanitud tellimused fiktiivsetele toodetele.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026446"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Koondplaneerimine loob fiktiivsetele toodetele plaanitud tellimused

KB number: 4614729

## <a name="symptoms"></a>Sümptomid

Koondplaneerimine loob plaanitud tellimused fiktiivsetele toodetele.

## <a name="resolution"></a>Eraldusvõime

Väljastatud toodete **fiktiivse** valiku säte määrab materjali (BOM) koosluse vaikerea tüübi. Kui **Fiktiivse** suvandi väärtuseks on seatud *Jah* loob süsteem kaubale siiski plaanitud tellimused, kuid iga plaanitud tellimuse valiku **Otse tuletatud vajadus** väärtuseks seatakse *Jah*. Seetõttu ei saa plaanitud tootmistellimust eraldi kinnitada. Selle asemel kaasatakse see alati, kui põhitootmistellimus on kinnitatud. Lisaks kaasatakse plaanitud fiktiivse tellimuse BOM-read algtoodangu tellimusse.
