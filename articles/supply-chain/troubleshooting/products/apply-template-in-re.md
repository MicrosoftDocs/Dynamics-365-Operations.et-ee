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
ms.openlocfilehash: 566686b6a86e67c87f75f9f2e397592174d3d749034f18997ca8ce651c2594a2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760390"
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
