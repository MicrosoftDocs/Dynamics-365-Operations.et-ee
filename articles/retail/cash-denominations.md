---
title: "Sularaha nimiväärtuste konfigureerimine kassa jaoks"
description: "Poe kassas müüjate, müügiassistentide ja juhatajate poolt kasutatavate rahatähtede ja müntide nimiväärtused saab määratleda kontoris."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: afe7c359f284fde10ada377fb19add9819a8dd21
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="configure-cash-denominations-for-pos"></a>Sularaha nimiväärtuste konfigureerimine kassa jaoks

[!include[banner](includes/banner.md)]

Poe kassas müüjate, müügiassistentide ja juhatajate poolt kasutatavate rahatähtede ja müntide nimiväärtused saab määratleda kontoris. Nimiväärtustest võib olla abi päeva lõpus müügiaruande koostamiseks sularaha lugemisel või maksete kiirel töötlemisel.

## <a name="define-denominations"></a>Määratlege nimiväärtused
Nimiväärtuste seadistamine toimub lehel **Seadistamine** > **Sularaha deklaratsiooni suvand poes**. 

![Sularaha nimiväärtused](./media/image1-denomination.png)

Nimiväärtuse määratlemiseks tehke järgmist.
1. Klõpsake **Uus**.
1. Määrake tüüp (münt või rahatäht).
1. Määrake summa (väärtus).

![sularaha nimiväärtused](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Seadistage funktsiooniprofiil.
Sularahamakse korral saab kassa kasutaja kliendi makstud summa kiireks sisestamiseks kasutada rahatähtede nimiväärtuseid. Funktsiooniprofiilis saate saate seadistada kassas nimiväärtuse kuvamise kaks suvandit.

**Suurem või võrdne summa**: vaikimisi kuvatakse kassas ainult makstavast summast suuremaid nimiväärtuseid, mis võimaldab makseid töödelda ühe puutega. Näiteks kui tasumisele kuuluv summa on 7,50 $,näitab kassa järgmiseid nimiväärtuseid: 10 $, 20 $, 50 $ ja 100 $. Kui puudutada ühte nendest summadest, töödeldakse makse vastavast summast lähtudes. Nimiväärtuseid 1 $ ja 5 $ ei kuvata, sest nende väärtus on maksmisele kuuluvast summast väiksem.

**Kõik nimiväärtused**: maksmisele kuuluvast summast olenemata kassas alati kõikide nimiväärtuste kuvamiseks valige see suvand. See tähendab, et kasutaja saab maksmisele kuuluva summa tasumiseks kasutada rahatähtede kombinatsioone. Näiteks, kui tasumisele kuuluv summa on 25,00 $, saab kasutaja valida müügi lõpetamiseks valikud 20 $ ja 5 $.

