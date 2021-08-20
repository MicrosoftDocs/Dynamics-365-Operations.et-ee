---
title: Skonto võtmine väljaspool skonto perioodi
description: See artikkel pakub kaht stsenaariumi, mis näitavad, kuidas skontot saab arvestada, isegi kui makse on tehtud väljaspool skontoperioodi.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9ba9c8176571a8b97b43565c89f8614bd828b3d9e1498a248fd896069d5d5c2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736985"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Skonto võtmine väljaspool skonto perioodi

[!include [banner](../includes/banner.md)]

See artikkel pakub kaht stsenaariumi, mis näitavad, kuidas skontot saab arvestada, isegi kui makse on tehtud väljaspool skontoperioodi.

28. juunil loob April arve hankijale 3052 summas 2000,00. Arvel on skonto 1 protsent, kui arve tasutakse 14 päeva jooksul.

## <a name="use-cash-discount-option--always"></a>Suvand Kasuta skontot = Alati
April loob makse 1. juulil, mis on pärast skonto kuupäeva. April avab tasakaalustatavate arvete vaatamiseks lehekülje **Kannete tasakaalustamine**. 

April märgib arve maksmiseks. Skontot ei võeta, kuna makse toimub pärast skonto kuupäeva. Siiski on andnud hankija Aprilile nõusoleku vaatamata sellele skontot võtta. Seega muudab April väljal **Kasuta skontot** väärtuseks **Alati**.

| Märge     | Kasuta skontot | Kanne   | Konto | Skonto kuupäev | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Alati            | Inv-10030 | 3052    | 28.06.2015          | 12.07.2015 | 10030   | ‑2000,00                      | USA dollar      | ‑1980,00        |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas.

| Field                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 12.07.2015 |
| Skonto summa         | ‑20,00    |
| Kasuta skontot            | Alati    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | ‑20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Kuupäev, mida kasutatakse allahindluste arvutamiseks = Valitud kuupäev
Kui mõlemad, nii arve kui ka makse on sisestatud, saab kannete tasakaalustamisel skontot võtta leheküljel **Kannete tasakaalustamine**. April muudab välja **Kuupäev, mida kasutatakse allahindluste arvutamiseks** väärtuseks **Valitud kuupäev**. Seejärel sisestab ta kuupäevaks 28. juuni, mis jääb arvel olnud skonto perioodi. Kande skonto arvutamiseks kasutatakse seda kuupäeva. April näeb, et vaikimisi kuvatakse leheküljel **Avatud kannete tasakaalustamine** kogu skonto summas 20,00. Arve real kuvatakse tasakaalustatavaks summaks 1980,00.

| Märge                     | Kasuta skontot | Kanne   | Konto | Skonto kuupäev | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valitud ja esile tõstetud | Tavaline            | Inv-10030 | 3052    | 28.06.2015          | 12.07.2015 | 10030   | ‑2000,00                      | USA dollar      | ‑1980,00        |
| Valitud                 | Tavaline            | APP‑10030 | 3052    | 15.07.2015          | 15.07.2015 |         | 500,00                         | USA dollar      | 500,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas. Võetakse skonto summas 20,00, kuna tasakaalustatav summa arvel on vaikesumma 1980,00.

| Field                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 12.07.2015 |
| Skonto summa         | ‑20,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | ‑20,00    |

April värskendab välja **Tasakaalustatav summa** väärtuseks **500,00**. Välja **Skonto summa võtmiseks** väärtuseks arvutatakse **5,05**.

| Märge                     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud ja esile tõstetud | Tavaline            | Inv-10030 | 3052    | 28.06.2015 | 12.07.2015 | 10030   | 2000,00                       | USA dollar      | ‑500,00          |
| Valitud                 | Tavaline            | APP‑10030 | 3052    | 15.07.2015 | 15.07.2015 |         | 500,00                         | USA dollar      | 500,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas. Välja **Skonto summa võtmiseks** väärtus on **5,05**, kuna tasakaalustatav summa arvel muudeti maksesummaks 500,00.

| Field                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 12.07.2015 |
| Skonto summa         | ‑20,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | ‑5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]