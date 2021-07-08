---
title: Plaanitud tootmistellimus tuleb enne kinnitamist planeerida
description: Kui proovite plaanitud tellimust kinnitada, kuvatakse tõrketeade, mis ütleb, et tellimus tuleb enne kinnitamist ajastada.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294060"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Plaanitud tootmistellimus tuleb enne kinnitamist planeerida

Tõrkekood: SYS309802

## <a name="symptoms"></a>Sümptomid

Kui proovite plaanitud tellimust kindlustada, kuvatakse järgmine tõrketeade:

> Plaanitud tootmistellimus peab olema plaanitud enne, kui seda saab kinnitada.

## <a name="cause"></a>Põhjus

Ajastatud algus- ja lõppkuupäevad ei tohi olla tühjad.

## <a name="resolution"></a>Lahendus

Plaanitud tellimuse algus- ja lõppkuupäevade määramiseks toimige järgmiselt.

1. Avage **Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused**.
1. Avage asjakohane plaanitud tellimus.
1. Määrake kiirkaardi **Üldine** jaotises **Ajastatud** kuupäevad väljadel **Alguskuupäev** ja **Lõppkuupäev**.
