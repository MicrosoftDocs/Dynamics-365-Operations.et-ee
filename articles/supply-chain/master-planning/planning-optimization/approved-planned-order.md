---
title: Plaanitud tellimuste kuvamine, haldamine ja kinnitamine
description: Käesolevas teemas kirjeldatakse, kuidas planeerimise optimeerimise korral kuvada, hallata ja kinnitada plaanitud tellimusi.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304363"
---
# <a name="view-manage-and-approve-planned-orders"></a>Plaanitud tellimuste kuvamine, haldamine ja kinnitamine

[!include [banner](../../includes/banner.md)]

Käesolevas teemas kirjeldatakse, kuidas planeerimise optimeerimise korral kuvada, hallata ja kinnitada plaanitud tellimusi.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Plaanitud tellimuste kuvamine ja haldamine

Plaanitud tellimusi saate vaadata ja hallata mis tahes plaanitud tellimuste loendilehel. Sõltuvalt plaanitud tellimuste tüübist, mida soovite kasutada, saate minna ühte järgmistest kohtadest.

- Koondplaneerimise \> tööruumide \> koondplaneerimine
- Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused
- Tootmise juhtimine \> Tootmistellimused \> Plaanitud tootmistellimused
- Hanked \> Ostutellimused \> Plaanitud ostutellimused
- Varude haldamine \> Sissetulevad tellimused \> Plaanitud üleviimised
- Varude haldamine \> Väljaminevad tellimused \> Plaanitud üleviimised

## <a name="view-and-edit-the-status-of-planned-orders"></a>Plaanitud tellimuste vaatamine ja redigeerimine

Edenemise jälgimiseks või plaanitud tellimuse töötlemise muutmiseks saate kasutada iga plaanitud tellimuse **olekuvälja**. Saadaval on järgmised suvandi **Olek** väärtused.

- **Töötlemata** – kui koondplaneerimine loob plaanitud tellimused, antakse neile see olek. Selle olekuga plaanitud tellimused kustutatakse järgmise plaanimise käitamisel.
- **Lõpetatud** – see olek näitab, et plaanitud tellimus on lõpetatud. Kui otsustate plaanitud tellimust mitte kinnitada, saate sellele manuaalselt määrata oleku *Lõpule viidud*. Pange tähele, et süsteem käsitleb olekuid *Töötlemata* ja *Lõpetatud* sama moodi.
- **Kinnitatud** – see olek näitab, et plaanitud tellimus on kinnitatud. Kui soovite kinnitada plaanitud tellimuse, saate määrata selle olekuks *Kinnitatud*. Kui soovite säilitada plaanitud tellimusele tehtud muudatusi või kui plaanite plaanitud tellimust kinnitab, muutke selle olekuks *Kinnitatud*. Plaanitud tellimused, mille olek on *Kinnitatud*, loetakse koondplaneerimises fikseerituks ja eeldatavaks tarneks. Seetõttu ei muudeta ega kustutata neid hiljem koondplaneerimise käitamisel. Selle toimimisviisi saavutamiseks kopeerib planeerimisloogika koondplaneerimise ajal *kinnitatud* olekus plaanitud tellimused vana plaani versioonist uude plaani versiooni. Pange tähele, et *Kinnitatud* olekus plaanitud tellimusi loetakse tarnitavateks ainult konkreetse koondplaani korral.

Üksiku plaanitud tellimuse oleku muutmiseks [avage mis tahes plaanitud tellimuste loendileht](#view-planned-orders), avage tellimus ja tehke seejärel üht järgmistest sammudest.

- Kiirkaardil **Üldine** muutke välja **Olek** väärtust.
- Valige toimingupaani vahekaardil **Plaanitud tellimus** grupis **Protsess** suvand **Muuda olekut**.
- Tellimuse kinnitamiseks valige tegumiribal suvand **Kinnita**.

Mitme plaanitud tellimuse oleku ühekorraga muutmiseks [avage mis tahes plaanitud tellimuste loendileht](#view-planned-orders), märkige ruut iga tellimuse puhul, mida soovite muuta, ja seejärel järgige üht järgmistest sammudest.

- Valige toimingupaani vahekaardil **Plaanitud tellimus** grupis **Protsess** suvand **Muuda olekut**.
- Tellimuste kinnitamiseks valige tegumiribal suvand **Kinnita**.

## <a name="approve-planned-orders"></a>Plaanitud tellimuste kinnitamine

Plaanitud tellimuste kinnitamine on valikuline etapp plaanitud tellimuseest kinnitatud tellimuse loomise protsessis.

Järgmine näide näitab, kuidas saate kasutada suvandi **Olek** väärtust, mis on määratud igale plaanitud tellimusele kinnitustöövoogude juurutamiseks. Kinnitusprotsessi juurutamiseks korrigeerige iga plaanitud tellimuse suvandi **Olek** väärtust käsitsi, nagu eelmises jaotises kirjeldatud.

![Plaanitud tellimuse voog](media/approved-planned-orders-1.png)

> [!TIP]
> Soovitame teil kõik muudetud plaanitud tellimused kinnitada. Vastasel korral eiratakse muudatusi ja need kirjutatakse järgmise planeerimise käivitamisel üle.

## <a name="additional-resources"></a>Lisaressursid

- [Kindlad plaanitud tellimused](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
