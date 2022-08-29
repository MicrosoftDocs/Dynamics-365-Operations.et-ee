---
title: Sularaha nimiväärtuste konfigureerimine kassa jaoks
description: Poe kassas müüjate, müügiassistentide ja juhatajate poolt kasutatavate rahatähtede ja müntide nimiväärtused saab määratleda kontoris.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.industry: Retail
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
ms.openlocfilehash: c61cde76bf2bfe3ff48b306a8a161fa27f50ac41
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273689"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Sularaha nimiväärtuste konfigureerimine kassa jaoks

[!include [banner](includes/banner.md)]

Poe kassas müüjate, müügiassistentide ja juhatajate poolt kasutatavate rahatähtede ja müntide nimiväärtused saab määratleda kontoris. Nimiväärtustest võib olla abi päeva lõpus müügiaruande koostamiseks sularaha lugemisel või maksete kiirel töötlemisel.

## <a name="define-denominations"></a>Määratlege nimiväärtused

Nimiväärtuste seadistamine iga poe kohta toimub lehel **Seadistamine** \> **Sularaha deklaratsiooni suvand**.

![Sularaha deklaratsiooni suvand.](./media/image1-denomination.png)

Nimiväärtuse määratlemiseks tehke järgmist.

1. Klõpsake valikut **Uus**.
1. Määrake tüüp (münt või rahatäht).
1. Määrake summa (väärtus).

![Sularahadeklaratsiooni põhivaluutade leht.](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Seadistage funktsiooniprofiil.

Sularahamakse korral saab kassa kasutaja kliendi makstud summa kiireks sisestamiseks kasutada rahatähtede nimiväärtuseid. Funktsiooniprofiilis saate saate seadistada kassas nimiväärtuse kuvamise kaks suvandit.

- **Suurem või võrdne summa**: vaikimisi kuvatakse kassas ainult makstavast summast suuremaid nimiväärtuseid, mis võimaldab makseid töödelda ühe puutega. Näiteks kui tasumisele kuuluv summa on 7,50 $,näitab kassa järgmiseid nimiväärtuseid: 10 $, 20 $, 50 $ ja 100 $. Kui puudutada ühte nendest summadest, töödeldakse makse vastavast summast lähtudes. Nimiväärtuseid 1 $ ja 5 $ ei kuvata, sest nende väärtus on maksmisele kuuluvast summast väiksem.
- **Kõik nimiväärtused**: maksmisele kuuluvast summast olenemata kassas alati kõikide nimiväärtuste kuvamiseks valige see suvand. See tähendab, et kasutaja saab maksmisele kuuluva summa tasumiseks kasutada rahatähtede kombinatsioone. Näiteks, kui tasumisele kuuluv summa on 25,00 $, saab kasutaja valida müügi lõpetamiseks valikud 20 $ ja 5 $.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
