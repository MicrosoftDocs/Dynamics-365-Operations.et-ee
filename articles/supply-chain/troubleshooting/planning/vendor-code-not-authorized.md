---
title: Hankija kood pole kindla toote ja kuupäeva jaoks autoriseeritud
description: Kui proovite plaanitud tellimust kinnitada või ostutellimusele rida lisada, saate tõrketeate, mis kinnitab, et hankija kood pole toote ja kuupäeva jaoks autoriseeritud.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 67cb054a648eac2b9a0e89b5e6a645af3c6142ad25237adb7afbd28f96c7e2eb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777715"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Hankija kood pole kindla toote ja kuupäeva jaoks autoriseeritud

Tõrkekood: SYP4881415

## <a name="symptoms"></a>Sümptomid

Kui proovite plaanitud tellimust kindlustada, kuvatakse järgmine tõrketeade:

> Hankija kood %1 pole autoriseeritud: %2, %3.

## <a name="cause"></a>Põhjus

Tõrge ilmneb, kuna välja **Kinnitatud hankija kontrollmeetod** väärtuseks on määratud toote puhul määratud *ainult Hoiatus* või *Keelatud* ja hankijal pole praegu õigust seda toodet tarnida.

## <a name="resolution"></a>Lahendus

Probleemi lahendamiseks keelake hankijalt vastava toote kontroll või kinnitage hankija.

Hankija tootekontrolli keelamiseks järgige neid samme.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Avage asjakohane toode.
1. Seadke kiirkaardil **Ost** **Kinnitatud hankija kontrollmeetod** välja väärtuseks, mis pole *ainult Hoiatus* või *Pole lubatud*.

Hankija tootekontrolli kinnitamiseks järgige neid samme.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Avage asjakohane kaup.
1. Klõpsake jaotise Tegumiriba vahekaardi **Ost** grupis **Kinnitatud hankija** suvandit **Häälestus**.
1. Valige loendi lehel **Kinnitatud hankijad**, et lisada rida jaotise ruudustikku ja seejärel määrake sellele järgmised väärtused:

    - **Hankija** - valige praeguse toote kinnitamiseks hankija.
    - **Jõustumiskuupäev** - valige hankija kinnitatud esimene kuupäev.
    - **Aegumise kuupäev** - valige hankija kinnitatud viimane kuupäev.

Lisateabe saamiseks vt jaotist [Kindlate toodete hankijate kinnitamine](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).
