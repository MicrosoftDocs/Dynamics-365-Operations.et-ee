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
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777739"
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
