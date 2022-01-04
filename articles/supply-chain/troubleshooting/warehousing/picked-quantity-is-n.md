---
title: Komplekteeritud kogus pole saatelehe loomise ajal piisav
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ei ühti koormusjoonel loodud töökogusega.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6febc340f140d0b3a3f08ea32a59d9eb4e6e5204
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920444"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Komplekteeritud kogus pole saatelehe loomise ajal piisav

Tõrkekood: SYS54073

## <a name="symptoms"></a>Sümptomid

Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ei ühti koormusjoonel loodud töökogusega.

Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:

> Kuna %1 on komplekteeritud, ei piisa %2 uuendamisest, kui jääk peab olema %3.

Seega ei saa te koorma pakendi silti genereerida.

## <a name="cause"></a>Põhjus

Saatelehte ei saa praeguses olekus genereerida, kuna võib esineda üht järgmistest tingimustest:

- Seotud tööd pole veel komplekteeritud ega teisaldatud saadetise lõppsihtkohta.
- Komplekteeritud töö kogus ei vasta loodud töö kogusele koormareal.
- Koormusjoone kogus, tööga loodud kogus ja valitud kogus ei ühti.

## <a name="resolution"></a>Lahendus

Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub. Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.
- Muutke laadimisliini kogust.
- Tühistage kõik komplekteerimisregistreerimised ja tehke komplekteerimine uuesti.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid

Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Saate valida koormuse, mille jaoks saatelehte ei saa luua.
1. Valige kiirkaardil **Koormaread** koormarida.
1. Tehke märge väärtuse kohta väljal **Loodud töö kogus**.
1. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.
1. Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.
1. Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.

### <a name="adjust-the-load-line-quantity"></a>Muutke laadimisliini kogust

Koormusrea koguse reguleerimiseks kasutage järgmist toimingut.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Saate valida koormuse, mille jaoks saatelehte ei saa luua.
1. Valige tegevuspaani vahekaardil **Läheta ja võta vastu grupi Tühista** **saadetis** käsku Tühista saadetise **kinnitus**.
1. Valige **vahekaardil Koorma** read väljaminek põhjust põhjus oleva kauba koormarida.
1. Komplekteeritud koguse täpsustamiseks valige **Vähenda komplekteeritud kogust**.
1. Seadistage väli **Koormarea vähendamine**, et kajastada koormusrea korrigeerimisi.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Tühistage kõik komplekteerimisregistreerimised ja tehke komplekteerimine uuesti

Probleem võib ilmneda, sest keegi kasutab koormuse rea sulgemiseks ilma tööta komplekteeritud registreerimist. Sel juhul tuleb käsitsi komplekteerimise registreerimine tühistada ja komplekteerimine tuleb seejärel Warehouse Management laohalduse mobiilirakenduse abil lõpetada.

Kasutage järgmist protseduuri komplekteeritud registreerimise tühistamiseks.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik tellimused**.
1. Valige müügitellimus, millele ei saa koormuse jaoks saatelehte sisestada.
1. Vahekaardil **Müügitellimuse read** valige müügitellimuse rida, mille jaoks registreerimine komplekteeritud oli.
1. Valige suvand **Uuenda rida \> Vali**, et kaupade komplekt eemaldada.
