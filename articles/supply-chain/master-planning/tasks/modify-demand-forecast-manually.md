---
title: 'Juhend: Nõudluse prognoosi käsitsi muutmine'
description: See teema kirjeldab, kuidas kauba prognoosi muuta
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224006"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Juhend: Nõudluse prognoosi käsitsi muutmine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas kauba prognoosi muuta. See protseduur on mõeldud tootmisplaanijale.

## <a name="modify-the-forecast-for-a-selected-item"></a>Valitud kauba prognoosi muutmine

Valitud kauba prognoosi muutmiseks tehke järgmist.

1. Avage **Moodulid \> Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Otsige loendist ja valige soovitud kirje. Valige kaup, mille puhul soovite prognoosi muuta.
1. Avage toimingupaanil vahekaart **Plaan** ja valige **Nõudlusprognoos**.
1. Valige loendist rida. Kui prognoosi read puuduvad, looge uus rida valides toiminguribal nuppu **Uus**.  
1. Väljale **Müügi kogus** sisestage positiivne arv. See number näitab kauba hinnangulist kogust. Negatiivse arvu sisestamisel kuvatakse tõrge.
1. Täitke teised väljad, nagu vaja.
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Ühe või mitme kauba eelarve muutmine rakendusega Microsoft Excel

Ühe või mitme kauba eelarve muutmine rakendusega Microsoft Excel:

1. Tehke üht järgmistest valikutest.
    - Avage leht **Nõudluse prognoosimine** mis tahes kauba jaoks (pole oluline, milline neist), nagu on kirjeldatud eelmises jaotises.
    - Avage K **oondplaneerimine \> Prognoosimine \>Käsitsi proggnoosisisend \> Nõudluse prognoosiread**.
1. Avage toimingupaanil **Ava Microsoft Office \> Nõudlusprognoosi sissekanded**.
1. Valige allalaadimiskoht, salvestage ja avage allalaaditud fail Excelis.
1. Kui näete hoiatust, valige **Luba redigeerimine**.
1. Logige Excelis Microsoft Dynamics tööpaani abil rakendusse Supply Chain Management sisse. Peate sisse logima suvandiga **Hoia mind sisse logitud** ja usaldama andmeühendusrakendust.
1. Exceli arvutustabelis kuvatakse nüüd kõik teie ettevõtte praegused nõudluse prognoosiread.  Vajadusel lisage, kustutage ja muutke nõudluse prognoosi ridu.
1. Muudatuste tagasilaadimiseks rakendusse Supply Chain Management valige Microsoft Dynamics tööpaanil **Avalda**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
