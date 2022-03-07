---
title: Erinevad laotüübid laadimisala halduse profiili kasutamisel
description: Selleks, et laadimissildade halduse profiil saaks varude segamist tõhusalt hallata, tuleb seadistada tööpäise piir. See lehekülg selgitab, kuidas seda teha.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476104"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Erinevad varude tüübid segatakse dokihaldusprofiili kasutamisel

## <a name="symptoms"></a>Sümptomid

Kasutate *saadetise konsolideerimispoliitikaid*. Olete seadistanud *dokihaldusprofiili* jaoks *asukoha profiili*, kuid töö loomisel segatakse varude tüübid lõppasukohas.

## <a name="resolution"></a>Lahendus

Laadimissildade halduse profiilid nõuavad töö eelnevat tükeldamist. Teisisõnu eeldab laadimissildade halduse profiil, et tööpäises pole mitut asetamise kohta.

Selleks, et laadimissildade halduse profiil saaks varude segamist tõhusalt hallata, tuleb seadistada tööpäise piir.

Selles näites on meie laadimissildade halduse profiil konfigureeritud nii, et **Varude tüübid, mida ei tohiks segada** on määratud olekusse *Saadetise ID*, ja me seadistame selle jaoks tööpäise piiri:

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Redigeerimiseks valige **Töökäsu tüüp** (nt *Ostutellimused*).
1. Valige redigeeritav töömall.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Avage vahekaart **Sortimine** ja lisage rida järgmiste sätetega.
    - **Tabel** - *Ajutised töökanded*
    - **Tuletatud tabel** - *Ajutised töökanded*
    - **Väli** - *Saadetise ID*
1. Valige nupp **OK**.
1. Naasete lehele **Töömallid**. Valige toimingupaanilt suvand **Tööpäise piirid**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Märkige ruut, mis on seotud **Välja nimi** *Saadetise ID-ga*.
1. Valige toimingupaanil nupp **Salvesta**.
