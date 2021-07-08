---
title: Kaubal ei saa olla kooslust ega valemit
description: Kui proovite tellimust kinnitada, kuvatakse kauba kinnitamise ajal tõrketeade. See tähendab, et kaubal ei saa olla kooslust (BOM) ega valemit.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294056"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Kaubal ei saa olla kooslust ega valemit

Tõrkekood: PRO2614

## <a name="symptoms"></a>Sümptomid

Kui proovite tellimust kinnitada, kuvatakse kauba kinnitamise ajal järgnev tõrketeade.

> Kaubal ei saa olla kooslust või valemit

## <a name="resolution"></a>Lahendus

Koosluse (BOM) või valemiga kaubad peavad olema *plaanimiskauba*, *koosluse* või *valemi* tüüpi. Kauba tüübi muutmiseks tehke järgmist.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Avage asjakohane toode.
1. Kiirkaardil **Projekteeri** määrake välja **Tootmise tüüp** väärtuseks *Planeeritav kaup*, *kooslus* või *valem*.
