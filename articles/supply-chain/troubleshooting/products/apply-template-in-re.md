---
title: Väljastatud toote loomiseks ei saa malli rakendada
description: Väljastatud toote loomiseks ei saa malli rakendada.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026432"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Väljastatud toote loomiseks ei saa malli rakendada

KB number: 4612097

## <a name="symptoms"></a>Sümptomid

Kui loote uue väljastatud toote dialoogiboksi **Uus väljastatud toode** abil, saate valida malli. Mall peaks tagama uue väljastatud toote mitme välja vaikesätted. Kõiki välju ei seadistata aga pärast malli valimist.

## <a name="cause"></a>Põhjus

Paljud Microsoft Dynamics 365 Supply Chain Management lehed lasevad teil luua malli, mis määrab neile lehtedele näidatavad kirjetele algsätted. Ühe neist mallidest saate luua valides **Kirje info** vahekaardil **Suvandid** vahekaardil tegevuspaanil. Väljastatud tooted on siiski palju keerukamad kui enamike teist tüüpi kirjetest. Kuigi saate malli loomiseks valida **Kirje teabe** **Väljastatud toote** lehel ja saate väljastatud toote loomisel selle malli valida, ei anna mall uue väljastatud toote jaoks oodatud välja väärtusi. Seetõttu ei saa te väljastatud toodete puhul kasutada kirjeteabe malle. Selle asemel peate looma sihtotstarbeline tootemallid.

## <a name="resolution"></a>Eraldusvõime

Tootemalli loomiseks kasutage tegevuspaani toote vahekaardil **Malli** menüüd **Toote** vahekaardil mitte **Kirje info** nuppu **Seaded** vahekaardil.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige tegevuspaani vahekaardi **Toode** jaotises **Uus** grupp, valige **Mall** ja siis valige kas **Loo isiklik mall** või **Loo ühismall** vastavalt vajadusele.
