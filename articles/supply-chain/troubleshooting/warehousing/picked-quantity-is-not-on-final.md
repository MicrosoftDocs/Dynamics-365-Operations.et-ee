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
ms.openlocfilehash: 7b57d3151852c9a2880185b7d9414e4246b7efb6429fcfce04c7cdae4ee00e37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760920"
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
- Asukoha direktiiv on konfigureeritud pakkimisasukohaga kui saadetise lõppsihtkohaks, kasutades voomalli konteinerit.

## <a name="resolution"></a>Lahendus

Koorem või saadetis on praegu olekus, kus saadetise kinnitamine nurjub. Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.
- Tühistage pakkimisasukohaga loodud töö ID-d saadetise lõppsihtkohana, konfigureerige asukohadirektiivi ümber ja väljastage koorem uuesti.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid

Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koormaread** koormarida.
1. Tehke märge väärtuse kohta väljal **Loodud töö kogus**.
1. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.
1. Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.
1. Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Tühistage pakkimisasukohaga loodud töö ID-d saadetise lõppsihtkohana, konfigureerige asukohadirektiivi ümber ja väljastage koorem uuesti

Kasutage järgmist protseduuri, et tühistada töö ID-d, mille pakkimise asukoht on lõplik maha panemise asukoht koos automaatse konteinerite paigutamisega.

1. Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.
1. Avaneb dialoog **Tühista töö**. Väljal **Töö ID** määrake töö ID, mida soovite tühistada. Valitud töö ID **töö oleku** väärtus peab olema *Avatud*, *Pooleli*, *Tühistatud*, *Kombineeritud* või *Suletud*.
1. Valige nupp **OK**.
1. Valige **Jah**, et kinnitada, et soovite töö tühistada.
1. Korrake seda protseduuri muude töö ID-de puhul vastavalt vajadusele.

Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).

Kasutage asukohadirektiivi ümber konfigureerimiseks järgmist protseduuri, et see ei kasutaks voomalli automatiseeritud konteinerite konfigureerimise korral pakkimisasukohta lõppsihtkohana.

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.
1. Valige asukohadirektiivid, mida kasutate konteinerite määratlemiseks.
1. Valige kiirkaardi tööriistaribal **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.
1. Päringu redaktori dialoogis leidke vahekaardil **Vahemik** rida, kus **Väli** on seatud *asukohaprofiilile*, ja veenduge, et rea väli **Kriteerium** ei ole seadistatud asukohaprofiilile, mille **asukohatüüp** on *Pakkimine*. Korrigeerige välja **Kriteerium**, et parandada lõplik maha panemise asukoht.

Kasutage järgmist protseduuri, et taas väljastada koorem ja luua õige saadetise sihtkohaga töö ID-d.

1. Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.
1. Leidke jaotises **Koormad** koorem, mis tuleb vabastada.
1. Valige jaotise **Koormused** tööriistaribal koormuse lattu väljastamiseks **Väljasta \> Lattu väljastamine**.
1. Korrake seda protseduuri muude koormuste puhul vastavalt vajadusele.
