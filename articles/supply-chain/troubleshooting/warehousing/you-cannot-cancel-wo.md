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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924397"
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
