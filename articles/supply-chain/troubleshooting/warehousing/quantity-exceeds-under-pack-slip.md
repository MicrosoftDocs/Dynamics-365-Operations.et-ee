---
title: Kogus ületab saatelehe loomise ajal alatarne protsendi
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab alatarne protsendi.
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
ms.openlocfilehash: ae02846c0ec937ebaff440dc5272a135e16c8aa7355ecc303929e760a54b6627
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760294"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Kogus ületab saatelehe loomise ajal alatarne protsendi

Tõrkekood: SYS24921

## <a name="symptoms"></a>Sümptomid

Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab alatarne protsendi.

Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:

> Rea alatarne on %1 protsenti, kuid lubatud alatarne on ainult %2 protsenti.

Seega ei saa te koorma pakendi silti genereerida.

## <a name="cause"></a>Põhjus

Koormuse või saadetise komplekteeritud kogus on tellitud kogusest väiksem ja ei kuulu alatarne protsendi vahemikku.

## <a name="resolution"></a>Lahendus

Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub. Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Muutke alatarne protsenti.
- Pöörake ümber ja tehke kohandusi.

### <a name="adjust-the-under-delivery-percentage"></a>Muutke alatarne protsenti

Alatarne protsendi reguleerimiseks kasutage järgmist toimingut.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik tellimused**.
1. Valige müügitellimus, millele ei saa koormuse jaoks saatelehte sisestada.
1. Valige vahekaardil  **Müügitellimused** müügitellimuse rida kauba jaoks, mis ületab alatarne protsent.
1. Vahekaardil  **Liini detailid** valige **Kohaletoimetamine**.
1. Seadke **Alatarne** väljal väärtus suuremale protsendile, mis rahuldab koorma koguse suhtes komplekteeritud kogust, nii et saatelehe loomine on võimalik.

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
