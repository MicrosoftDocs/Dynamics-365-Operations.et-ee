---
title: "Võtta väljaspool skonto skonto"
description: "See artikkel pakub kaht stsenaariumi, mis näitavad, kuidas skontot saab arvestada, isegi kui makse on tehtud väljaspool skontoperioodi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: bea9565f488c01e5e6aede8cabe73ac13b75dacb
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Võtta väljaspool skonto skonto

See artikkel pakub kaht stsenaariumi, mis näitavad, kuidas skontot saab arvestada, isegi kui makse on tehtud väljaspool skontoperioodi.

28. juuni aprill loob 2,000.00 3052 hankija arve. Arve on 1 protsenti allahindlust, kui arve on tasutud 14 päeva jooksul.

## <a name="use-cash-discount-option--always"></a>Suvand Kasuta skontot = Alati
April loob makse 1. juulil, mis on pärast skonto kuupäeva. April avab tasakaalustatavate arvete vaatamiseks lehekülje **Kannete tasakaalustamine**. 

April märgib arve maksmiseks. Skontot ei võeta, kuna makse toimub pärast skonto kuupäeva. Siiski on Hankija skonto niikuinii võtta aprillis heakskiidu andnud. Seega aprillis muudab väärtust ning **Kasuta skontot** välja **alati**.

| Märge     | Kasuta skontot | Kanne   | Konto | Skonto kuupäev | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Alati            | Inv-10030 | 3052    | 28.06.2015          | 12.07.2015 | 10030   | ‑2000,00                      | USA dollar      | ‑1980,00        |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas.

|                              |           |
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

|                              |           |
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

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 12.07.2015 |
| Skonto summa         | ‑20,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | ‑5,05     |




