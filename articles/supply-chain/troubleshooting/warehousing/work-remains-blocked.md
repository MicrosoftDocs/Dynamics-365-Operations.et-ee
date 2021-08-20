---
title: Töö jääb blokeerituks
description: Töö jääb blokeerituks
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 898390c78bb26fb8a44f77a10ad27a00720f7d1a3396cec5fff10e9d6b93364d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768566"
---
# <a name="work-remains-blocked"></a>Töö jääb blokeerituks

Tõrkekood: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Töö %1 jääb blokeerituks, kuna seotud voo %2 olek on %3.

## <a name="cause"></a>Põhjus

Tööd töödeldakse voos ja sellelt ei saa blokeeringut eemaldada nagu on näidatud ühes järgnevast tingimustest:

- Vahekaardil **Blokeerimise põhjused** väli **Töö blokeerimise põhjused** on ühe või mitme rea väärtuseks seatud *Voo töötlemine*.
- Kui valite **Voog**  **Seotud teabe** grupist **Seostuva teabe** Tegevuspaani vahekaardil, on **Voo oleku** väli seatud suvandile *Töös*.

## <a name="resolution"></a>Eraldusvõime

Tegevuspaani vahekaardil **Seotud teave** grupis **Seotud teave** valige **Voog**. Siis valige **Voo** lehel, Tegevuspaanil, **Voo** vahekaardil **Voo** grupis **Vooandmete puhastamine**.

## <a name="workaround"></a>Vastukaal

Kui eelmised sammud probleemi ei lahendanud, saate töö järgmiste sammude abil tühistada.

1. Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.
1. Väljal **Töö ID** määrake töö ID, mida soovite tühistada ja millel on **Töö oleku** väärtuseks kas *Ava*, *Pooleli*, *Tühistatud*, *Kombineeritud* või *Suletud*.
1. Valige nupp **OK**.
1. Valige **Jah**, et kinnitada, et soovite töö tühistada.

Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).
