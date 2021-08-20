---
title: Viimane suletud töörida peab olema pane
description: Viimane suletud töörida peab olema pane
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bbc5797df2b7465b36ec5ea546a67441626daeb1c72f82dfca4eb7db3503b713
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760270"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Viimane suletud töörida peab olema pane

Tõrkekood: WAX1285

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Viimane suletud töörida peab olema pane.

## <a name="cause"></a>Põhjus

Tööd ei saa praeguses olekus tühistada.

Viimasel tööreal on väli **Töö olek** seatud *Suletud*, kuid välja **Töö tüüp** väärtuseks pole seatud *Pane*.

## <a name="resolution"></a>Eraldusvõime

Loa tühistamiseks tehke järgmist.

1. Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.
1. Väljal **Töö ID** määrake töö ID, mida soovite tühistada.
1. Valige nupp **OK**.
1. Valige **Jah**, et kinnitada, et soovite töö tühistada.

Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).
