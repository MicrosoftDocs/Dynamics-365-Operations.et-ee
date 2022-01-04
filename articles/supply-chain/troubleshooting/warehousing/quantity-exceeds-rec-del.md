---
title: Kogus, mida proovite värskendada, ületab vastuvõetud/tarnitud kogust.
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab müügitellimuse jaoks korjatud ja reserveeritud töökogust.
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
ms.openlocfilehash: ec5e0ac8dd097e5ebf016683fc5c17df7ecb2305
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920394"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Kogus, mida proovite värskendada, ületab vastuvõetud/tarnitud kogust

Tõrkekood: SYS7676

## <a name="symptoms"></a>Sümptomid

Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab müügitellimuse jaoks korjatud ja reserveeritud töökogust.

Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:

> Kogus, mida püüate värskendada, ületab saadud või tarnitud koguse.

Seega ei saa te koorma pakendi silti genereerida.

## <a name="cause"></a>Põhjus

Komplekteeritud töö kogus ei vasta loodud töö kogusele koormareal. Näiteks võib see probleem ilmneda, kui koormarea kogus, tööga loodud kogus või komplekteeritud kogus ei ole täpne.

## <a name="resolution"></a>Lahendus

Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub. Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.
- Muutke laadimisliini kogust.
- Tühistage kõik komplekteerimisregistreerimised ja tehke komplekteerimine uuesti.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid

Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist luua.
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

Kui keegi kasutab registreerimise noppimist koormarea sulgemiseks ilma tööta, võib esineda lahknevust koormarea koguse ja komplekteeritud koguse vahel. Sel juhul tuleb käsitsi komplekteerimise registreerimine tühistada ja komplekteerimine tuleb seejärel Warehouse Management laohalduse mobiilirakenduse abil lõpetada.

Kasutage järgmist protseduuri komplekteeritud registreerimise tühistamiseks.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik tellimused**.
1. Valige müügitellimus, millele ei saa koormuse jaoks saatelehte sisestada.
1. Vahekaardil **Müügitellimuse read** valige müügitellimuse rida, mille jaoks registreerimine komplekteeritud oli.
1. Valige suvand **Uuenda rida \> Vali**, et kaupade komplekt eemaldada.
