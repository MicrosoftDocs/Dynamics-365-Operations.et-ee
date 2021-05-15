---
title: Tööd ei saa tema oleku tõttu tühistada
description: Tööd ei saa tema oleku tõttu tühistada
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924251"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Tööd ei saa tema oleku tõttu tühistada

Tõrkekood: WAX2190

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Tööd %1 ei saa tühistada, sest selle olek on %2.

## <a name="cause"></a>Põhjus

Tööd ei saa praeguses olekus tühistada.

Töö päisel või töö ridadel ei ole eeldatavat **Töö oleku** väärtust. **Töö oleku** väli pole tööpäises seatud *Avatud* või *Pooleli*.

## <a name="resolution"></a>Eraldusvõime

Loa tühistamiseks tehke järgmist.

1. Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.
1. Väljal **Töö ID** määrake töö ID, mida soovite tühistada.
1. Valige nupp **OK**.
1. Valige **Jah**, et kinnitada, et soovite töö tühistada.

Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).
