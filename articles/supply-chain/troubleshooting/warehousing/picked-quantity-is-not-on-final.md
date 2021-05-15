---
title: Saadetist ei saa kinnitada, kuna kaubad pole komplekteeritud
description: Saadetist ei saa kinnitada, kuna kaubad pole komplekteeritud
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938455"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Saadetist ei saa kinnitada, kuna kaubad pole komplekteeritud

Tõrkekood: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Sümptomid

Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:

> Mõni koorma %1 jaoks vajalik kaup pole veel komplekteeritud ja saadetise lõppsihtkohta teisaldatud.

Seega ei saa te koorma saadetist kinnitada.

## <a name="cause"></a>Põhjus

Koormat või saadetist ei saa praeguses olekus kinnitada, kuna võib esineda üht järgmistest tingimustest:

- Seotud tööd pole veel komplekteeritud ega teisaldatud saadetise lõppsihtkohta.
- Komplekteeritud töö kogus ei vasta loodud töö kogusele koormareal.

## <a name="resolution"></a>Eraldusvõime

Saate kontrollida seotud müügitellimusi või koorma või saadetise üleviimistellimusi. Kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koormaread** koormarida.
1. Tehke märge väärtuse kohta väljal **Loodud töö kogus**.
1. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.
1. Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.
1. Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.
