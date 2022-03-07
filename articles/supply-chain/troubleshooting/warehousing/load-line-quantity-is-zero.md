---
title: Saadetist ei saa kinnitada, kuna koormusridadel on null kogust
description: Saadetist ei saa kinnitada, kuna koormusridadel on null kogust.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5dc5f8962ba37d21d7ef505fea940dc8767a9d9295588cb0e12e9eebe379a35c
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012159"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Saadetist ei saa kinnitada, kuna koormusridadel on null kogust

Tõrkekood: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Sümptomid

Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:

> Kõigi koorma %1 ridade kogus on null.  
> Koorma %1 saatmist ei saanud kinnitada.

Seega ei saa te koorma saadetist kinnitada.

## <a name="cause"></a>Põhjus

Süsteem hindab, kas koormarida saab lähetada, võttes aluseks loodud töö ID-d, koormarea koguse ja alatarne protsendi. Kui süsteem leiab, et töö ID-d pole ja kui alatarne protsendiks on seatud 100 protsenti, ei saa saadetist kinnitada.

Näiteks võib see probleem ilmneda, kui töö on tühistatud ja koormarea alatarne protsent on 100 protsenti.

## <a name="resolution"></a>Lahendus

Koorem või saadetis on praegu olekus, kus saadetise kinnitamine nurjub. Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.
- Vaadake üle koorma read veendumaks, et alatarnete protsent ja kogused on joondatud komplekteeritud tööga.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid

Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Avage koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koormaread** koormarida.
1. Tehke märge väärtuse kohta väljal **Loodud töö kogus**.
1. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.
1. Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.
1. Kui leiate lahknevuse, tühistage vastav töö, konfigureerige asukohadirektiivi ümber ja vabastage koormus uuesti. Juhisteks vt [Saadetist ei saa kinnitada, kuna kaubad pole komplekteeritud](picked-quantity-is-not-on-final.md).
1. Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Vaadake üle koorma read veendumaks, et alatarnete protsent ja kogused on joondatud komplekteeritud tööga

Kasutage järgmist protseduuri, et vaadata üle koorma read veendumaks, et alatarnete protsent ja kogused on joondatud komplekteeritud tööga.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Avage koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab alatarne protsendi.
1. Korrigeerige välja **Alatarne** väärtust või välja **Kogus** vastavalt vajadusele.

> [!TIP]
> Kui probleem pole ikka veel lahendatud, peate lõpule viima rohkem komplekteerimistööd seotud müügitellimustes või üleviimistellimustes kuni saadav kogus on koorma või saadetisega joondatud.
