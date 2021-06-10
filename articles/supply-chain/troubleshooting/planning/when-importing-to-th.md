---
title: Teil palutakse kauba laovarude sätted salvestada ka siis, kui muudatusi pole tehtud
description: Teil palutakse kauba laovarude sätted salvestada ka siis, kui muudatusi pole tehtud.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049462"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Teil palutakse kauba laovarude sätted salvestada ka siis, kui muudatusi pole tehtud

KB number: 4615588

## <a name="symptoms"></a>Sümptomid

Mõnel juhul võite saada järgmise teate, kui avate **Kauba laovarude** lehe pärast kaupade importimist *Üksuse laovarude V2* kaudu:

> Kas soovite tehtud muudatused enne sulgemist salvestada?

Te saate selle teate ka siis, kui te pole midagi teinud.

## <a name="resolution"></a>Lahendus

**Kauba laovarude** leht hõlmab komplekset vaikeloogikat, mis võib põhjustada teate näitamise pärast andmebaasis otsemuudatuste tegemist, nt üksuse impordi kaudu. Näiteks on `AREGENERALSETTINGSOVERRIDDEN` üksuse välja väärtuseks seatud *Ei*, kuid te impordite faili, mis annab sellistele väljadele uued või muudetud väärtused `PRODUCTCOVERAGEGROUPID` ja/või `VENDORACCOUNTNUMBER`. Sellisel juhul, kuna `AREGENERALSETTINGSOVERRIDDEN` välja väärtuseks on seatud *Ei*, tühjendatakse väärtused automaatselt väljadelt, kui avate **Kauba laovarude lehe** peale importi esimest korda. Kui salvestate muudatused teateakna viipadega, talletatakse need andmebaasi. Vastasel juhul saate sama teate järgmisel korral, kui lehe avate.

Sellise käitumise vältimiseks, kuid ka väljade väärtuste kaasamiseks, nt üksuse `PRODUCTCOVERAGEGROUPID` impordi kaudu, seadke `AREGENERALSETTINGSOVERRIDDEN` importimiseks väärtusele *Jah*.
