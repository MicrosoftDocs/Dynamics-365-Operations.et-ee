---
title: Kogus ületab saatelehe loomise ajal ületarne protsendi
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab ületarne protsendi.
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
ms.openlocfilehash: 00e3da7767b80e16f9351f59b109765bffc0128fe149cefafc1edda3a6cbcb96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781341"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Kogus ületab saatelehe loomise ajal ületarne protsendi

Tõrkekood: SYS24920

## <a name="symptoms"></a>Sümptomid

Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab ületarne protsendi.

Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:

> Rea ületarne on %1 protsenti, kuid lubatud ületarne on ainult %2 protsenti.

Seega ei saa te koorma pakendi silti genereerida.

## <a name="cause"></a>Põhjus

Koormuse või saadetise komplekteeritud kogus on tellitud kogusest suurem ja ei kuulu ületarne protsendi vahemikku.

## <a name="resolution"></a>Lahendus

Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub. Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Muutke laadimisliini kogust.
- Muutke ületarne protsendi.
- Pöörake ümber ja tehke kohandusi.

### <a name="adjust-the-load-line-quantity"></a>Muutke laadimisliini kogust

Koormusrea koguse reguleerimiseks kasutage järgmist toimingut.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Saate valida koormuse, mille jaoks saatelehte ei saa luua.
1. Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.
1. Valige vahekaardil  **Koormaread** koorma rida kauba jaoks, mis ületab ületarne protsent.
1. Komplekteeritud koguse täpsustamiseks valige **Vähenda komplekteeritud kogust**.
1. Vahekaardil  **Liini detailid** valige **Tellimus**.
1. Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** välja väärtusele), et saatelehe loomine saaks toimuda.

### <a name="adjust-the-over-delivery-percentage"></a>Muutke ületarne protsendi

Ületarne protsendi reguleerimiseks kasutage järgmist toimingut.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik tellimused**.
1. Valige müügitellimus, millele ei saa koormuse jaoks saatelehte sisestada.
1. Valige vahekaardil  **Müügitellimused** müügitellimuse rida kauba jaoks, mis ületab ületarne protsent.
1. Vahekaardil  **Liini detailid** valige **Kohaletoimetamine**.
1. Seadke **Ületarne** väljal väärtus suuremale protsendile, mis rahuldab koorma koguse suhtes komplekteeritud kogust, nii et saatelehe loomine on võimalik.

### <a name="reverse-and-make-adjustments"></a>Pöörake ümber ja tehke kohandusi

Tühistage kõik koormuse jaoks sisestatud asjad (nt saateleht, lähetuskinnitus ja töö), tehke müügitellimuse täpsustused, väljastage tellimus uuesti lattu ja viige saatmisprotseduur lõpule.

Saatelehe tühistamiseks kasutage järgmist toimingut.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Tühista saatelehed**.

Saadetise kinnituse tühistamiseks kasutage järgmist toimingut.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.

Töö pööramiseks tehke järgmised toimingud:

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige toimingupaani vahekaardil  **Koormused** grupis  **Töö** üksus  **Pöördtöö**.
