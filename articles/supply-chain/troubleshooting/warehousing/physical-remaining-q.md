---
title: Ühikus olev füüsiline jääkkogus ei tohi olla null
description: Saatelehe loomisel on sellele esitatud andmete laokogus nullist erinev, kuid müügikogus null.
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
ms.openlocfilehash: 187363db3030ee0741f0c7e7746295b88320162c156120112332bb78593bb673
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744650"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Ühikus olev füüsiline jääkkogus ei tohi olla null

Tõrkekood: SYS19591

## <a name="symptoms"></a>Sümptomid

Saatelehe loomisel on sellele esitatud andmete laokogus nullist erinev, kuid müügikogus null.

Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:

> Füüsiliselt järelejääv kogus ühikus %1 peab nullist erinema.

Seega ei saa te koorma pakendi silti genereerida.

## <a name="cause"></a>Põhjus

Süsteem hindab inventuuriühiku füüsilist jääkkogust ja saatmisühikus järelejäänud füüsilist kogust. Kui süsteem leiab, et saatmisühiku füüsiline jääkkogus on 0 (null), kuid füüsiline jääk laoühikus pole 0, ei saa te saatelehte luua. See probleem võib ilmneda näiteks juhul, kui kauba müügiühik ja laoühik erinevad ning ühikutevaheline teisendamine pole täpne.

## <a name="resolution"></a>Lahendus

Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub. Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.
- Vaadake üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma ümardamisprobleemideta.
- Vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega.
- Veenduge, et lao mõõtühik oleks müügi mõõtühikust väiksem.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid

Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koormaread** koormarida.
1. Tehke märge väärtuse kohta väljal **Loodud töö kogus**.
1. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.
1. Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.
1. Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Vaadake üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma ümardamisprobleemideta

Kasutage järgmist protseduuri, et vaadata üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma ümardamisprobleemideta.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Saate valida koormuse, mille jaoks saatelehte ei saa luua.
1. Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.
1. Valige vahekaardil  **Koormaread** koorma rida kauba jaoks, mis ületab ületarnet.
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

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Veenduge, et lao mõõtühik oleks müügi mõõtühikust väiksem

Veenduge, et lao mõõtühik oleks müügi mõõtühikust väiksem. Kaaluge kauba mõõtühiku ümberkonfigureerimine vastavalt vajadusele.
