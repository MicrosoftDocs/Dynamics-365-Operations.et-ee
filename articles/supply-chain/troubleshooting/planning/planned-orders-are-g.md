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
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742000"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Koondplaneerimine loob fiktiivsetele toodetele plaanitud tellimused

KB number: 4614729

## <a name="symptoms"></a>Sümptomid

Koondplaneerimine loob plaanitud tellimused fiktiivsetele toodetele.

## <a name="resolution"></a>Eraldusvõime

Väljastatud toodete **fiktiivse** valiku säte määrab materjali (BOM) koosluse vaikerea tüübi. Kui **Fiktiivse** suvandi väärtuseks on seatud *Jah* loob süsteem kaubale siiski plaanitud tellimused, kuid iga plaanitud tellimuse valiku **Otse tuletatud vajadus** väärtuseks seatakse *Jah*. Seetõttu ei saa plaanitud tootmistellimust eraldi kinnitada. Selle asemel kaasatakse see alati, kui põhitootmistellimus on kinnitatud. Lisaks kaasatakse plaanitud fiktiivse tellimuse BOM-read algtoodangu tellimusse.
