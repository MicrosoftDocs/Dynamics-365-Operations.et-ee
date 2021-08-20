---
title: Globaalne kinnipeetav maks
description: Selles teemas antakse teavet globaalsete kinnipeetava maksu funktsionaalsuse ja selle seadistamise kohta. Globaalse kinnipeetava maksu funktsionaalsus on võimendatud hankija ja kliendi tehingute jaoks, nii et kinnipeetav maks arvutatakse kauba tasemel.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c51da1257e11543f025fda76c166301477ef78508caac0451267437e918435eb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727344"
---
# <a name="global-withholding-tax"></a>Globaalne kinnipeetav maks

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet globaalsete kinnipeetava maksu funktsionaalsuse kohta ja selgitatakse selle seadistamist. Uus funktsionaalsus on saadaval versioonis 10.0.17 ja uuemates.

Globaalse kinnipeetava maksu funktsionaalsus on võimendatud hankija ja kliendi tehingute jaoks, nii et kinnipeetav maks arvutatakse kauba tasemel. Ostutehingutest kinnipeetava maksu konto saldot saab tasakaalustada, käitades kinnipeetava maksu töö kinnipeetava maksu tasakaalustuskonto vastu.

> [!NOTE]
> Globaalne kinnipeetav maks ei toeta ostutellimuse, hankija arve ja müügitellimuse lehtede funktsiooni **Tasude haldamine**.

## <a name="turn-on-global-withholding-tax"></a>Globaalse kinnipeetava maksu sisse lülitamine

1. Valige tööruumis **Funktsioonihaldus** suvand **Globaalne kinnipeetav maks** ja seejärel valige **Luba kohe**.
2. Avage **Maks \> Seadistus \> Parameetrid \> Pearaamatu parameetrid** ja seejärel seadistage vahekaardil **Kinnipeetav maks** suvand **Luba globaalne kinnipeetav maks** olekusse **Jah**.
3. Valige käsk **Salvesta**.
4. Värskendage lehekülg oma veebibrauseris.

> [!NOTE]
> Globaalset kinnipeetava maksu funktsiooni ei saa sisse lülitada riikide/regioonide puhul, kus on lokaliseeritud kinnipeetava maksu lahendused juba olemas. Need alad on järgmised (kuid mitte ainult) - India, Brasiilia, Tai, Saudi Araabia, Iirimaa, Suurbritannia ja Ameerika Ühendriikidega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
