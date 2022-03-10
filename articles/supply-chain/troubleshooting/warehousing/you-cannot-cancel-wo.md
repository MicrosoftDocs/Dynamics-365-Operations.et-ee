---
title: Kasutajale määratud tööd ei saa tühistada
description: Kasutajale määratud tööd ei saa tühistada
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748687"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Kasutajale määratud tööd ei saa tühistada

Tõrkekood: WAX708

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Kasutajale määratud tööd ei saa tühistada.

## <a name="cause"></a>Põhjus

Töö on blokeeritud ja seda ei saa tühistada. Selle kinnitamiseks avage töö ID ja seejärel avage **Üldine** vahekaart. Kui töö on lukustatud, seatakse välja **Töö olek** *Pooleli* ja väljale **Lukustus** seatakse kasutaja ID.

## <a name="resolution"></a>Eraldusvõime

Loa tühistamiseks tehke järgmist.

1. Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.
1. Väljal **Töö ID** määrake töö ID, mida soovite tühistada.
1. Valige nupp **OK**.
1. Valige **Jah**, et kinnitada, et soovite töö tühistada.

Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).
