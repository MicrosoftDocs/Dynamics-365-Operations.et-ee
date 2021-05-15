---
title: Tööd ei saa tühistada, kuna see on blokeeritud
description: Tööd ei saa tühistada, kuna see on blokeeritud
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924275"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Tööd ei saa tühistada, kuna see on blokeeritud

Tõrkekood: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Tööd %1 ei saa tühistada, kuna see on põhjuse tüübi %2tõttu blokeeritud. Tööl peab olema blokeering tühistatud enne kui selle saab tühistada.

## <a name="cause"></a>Põhjus

Töö on blokeeritud ja seda ei saa tühistada.

**Töö** lehel, vahekaardil **Üldine** on suvand **Blokeeritud** seatud väärtusele *Jah*. See säte näitab, et töö on blokeeritud. Vahekaart **Blokeerimise põhjused** näitab, miks töö blokeeriti.

## <a name="resolution"></a>Eraldusvõime

Töö blokeerimise tühistamiseks valige vahekaart **Blokeerimise põhjused** ja järgige seejärel üht järgmistest sammudest:

- Kui **Töö blokeerimise põhjuse** välja väärtuseks on seatud *Määratlemata põhjus*: Valige Tegevuspaanil vahekaardil **Töö** grupis **Töö** suvand **Tühista töö blokeering**.
- Kui **Töö blokeerimise põhjuse** välja väärtuseks on seatud *Voo töötlemine*: valige Tegevuspaanil vahekaardil **Seostuv teabe** jaotises **Seotud teabe** grupis suvand **Voog**. Siis valige **Voo** lehel, Tegevuspaanil, **Voo** vahekaardil **Voo** grupis **Vooandmete puhastamine**.

## <a name="workaround"></a>Vastukaal

Kui eelmised sammud probleemi ei lahendanud, saate töö järgmiste sammude abil tühistada.

1. Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.
1. Väljal **Töö ID** määrake töö ID, mida soovite tühistada ja millel on **Töö oleku** väärtuseks kas *Ava*, *Pooleli*, *Tühistatud*, *Kombineeritud* või *Suletud*.
1. Valige nupp **OK**.
1. Valige **Jah**, et kinnitada, et soovite töö tühistada.

Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).
