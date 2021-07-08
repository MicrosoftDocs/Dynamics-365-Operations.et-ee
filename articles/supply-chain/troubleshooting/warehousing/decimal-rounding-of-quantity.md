---
title: Füüsilise värskenduskoguse ümardamine kümnendkohtade kaupa on vale
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ei vasta ühikus määratletud kümnendtäpsusele.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248777"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Füüsilise värskenduskoguse ümardamine kümnendkohtade kaupa on vale

Tõrkekood: SYS19589

## <a name="symptoms"></a>Sümptomid

Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ei vasta ühikus määratletud kümnendtäpsusele.

Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:

> Füüsilise sisestamiskoguse kümnendkoha ümardamine ühikus %1 on vale.

Seega ei saa te koorma pakendi silti genereerida.

## <a name="cause"></a>Põhjus

Süsteem hindab, kas lähetuskoguse kümnendkohtade ümardamine vastab saatmisühiku jaoks määratletud kümnendtäpsusele. Kui süsteem ümardab lähetuskoguse määratud kümnendkohtade leitud arvuni ja kui ümardatud lähetuskogus ei vasta tegelikule lähetuskogusele, ei saa te saatelehte luua. See probleem võib ilmneda näiteks juhul, kui müügikogus on 1,75 kilogrammi (kg), kuid kümnendtäpsuseks on seatud *1*.

## <a name="resolution"></a>Lahendus

Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub. Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Vaadake üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma kümnendkohtade ja muude ümardamisprobleemideta.
- Vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Vaadake üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma kümnendkohtade ja muude ümardamisprobleemideta

Kasutage järgmist protseduuri, et vaadata üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma kümnendkohtade ja muude ümardamisprobleemideta.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Saate valida koormuse, mille jaoks saatelehte ei saa luua.
1. Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.
1. Vahekaardil  **Koormusread** valige probleemi põhjustava üksuse koormusrida.
1. Komplekteeritud koguse täpsustamiseks valige **Vähenda komplekteeritud kogust**.
1. Vahekaardil  **Liini detailid** valige **Tellimus**.
1. Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** välja väärtusele), et saatelehe loomine saaks toimuda.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega

Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Saate valida koormuse, mille jaoks saatelehte ei saa luua.
1. Kiirkaardil **Koormusread** valige probleemi põhjustava üksuse koormusrida. Tehke märge väärtuse kohta väljadel **Kogus** ja **Ühik**.
1. Avage **Organisatsiooni haldus \> Seadistus \> Ühikud**.
1. Saate valida ühiku, mille jaoks saatelehte ei saa luua.
1. Saate välja **Kümnendtäpsus** väärtust vastavalt vajadusele korrigeerida.
