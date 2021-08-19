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
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730102"
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
