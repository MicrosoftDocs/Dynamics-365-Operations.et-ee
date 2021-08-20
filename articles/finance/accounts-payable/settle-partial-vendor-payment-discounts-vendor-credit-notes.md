---
title: Hankija sellise osalise makse tasumine, mille kreeditarvetel on allahindlusi
description: Selles artiklis läbitakse stsenaarium, kus kreeditarve tasakaalustatakse arvega.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553150a59d132bb1d8b563e03456995cbc8d2be5f36bab0c1fe6b8bbbf77dce1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737109"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-credit-notes"></a>Hankija sellise osalise makse tasumine, mille kreeditarvetel on allahindlusi

[!include [banner](../includes/banner.md)]

Selles artiklis läbitakse stsenaarium, kus kreeditarve tasakaalustatakse arvega.

Fabrikami hankijad annavad kreeditarvetelt skontosid. Hankija 3050 võimaldab Fabrikamil võtta 1% skontot, kui arve tasutakse 14 päeva jooksul.

## <a name="invoice-and-credit-memo"></a>Arve ja kreeditarve
29. juunil loob April hankijale 3050 arve summas 1000,00. 2. juulil loob ta kreeditarve 200,00. Lehelt **Hankijad** avab April lehe **Kannete tasakaalustamine**. Ta saab kasutada lehte **Kannete tasakaalustamine** nii kreeditarve kui ka arve tasakaalustamiseks märkimiseks. Kreeditarvelt arvestatakse allahindlust 2.00. Seega vähendatakse kreeditarve koondväärtust summani 198.00.

| Märge                     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud                 | Tavaline            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070   | –1000.00                      | USA dollar      | –990.00          |
| Valitud ja esile tõstetud | Tavaline            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200,00                         | USA dollar      | 198.00           |

Teave kreeditarve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

| Field                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 7/13/2015 |
| Skonto summa         | 2.00      |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 2.00      |

April klõpsab nuppu **Sisesta**. Seejärel vaatab ta lõpetatud tasakaalustuse üle. Aprillil näeb, et rakendati kreeditarve summat 198.00 ja võeti allahindlust 2.00. Seetõttu on koondsumma 200.00.

| Märge                     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve  | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valitud ja esile tõstetud | Tavaline            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070    | –1000.00                      | USA dollar      | –200.00          |
| Valitud                 | Tavaline            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 | CR-10070 | 200,00                         | USA dollar      | 198.00           |

April saab vaadata üle hankija kanded lehel **Hankija kanded**, valides hankija lehel **Kõik hankijad** ja klõpsates siis tegumiribal nuppu **Kanded**. Sellel lehel näeb April, et arve saldo on –800.00. Ta näeb ka kreeditarvet summaga 198.00 ja allahindlust summas 2.00.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10070  | Arve          | 6/29/2015 | 10070   |                                      | 1 000,00                              | –800.00 | USA dollar      |
| Inv-10071  |                  | 7/2/2015  | CR10071 | 200,00                               |                                       | 0,00    | USA dollar      |
| DISC‑10071 |  Skonto   | 7/2/2015  |         | 2.00                                 |                                       | 0,00    | USA dollar      |
| DISC‑10071 |  Skonto   | 7/2/2015  |         |                                      | 2.00                                  | 0,00    | USA dollar      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]