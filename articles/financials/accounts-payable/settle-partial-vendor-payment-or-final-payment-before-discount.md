---
title: "Hankija osalise makse ja lõpliku makse tasakaalustamine enne allahindluse kuupäeva."
description: "Selles artiklis käsitletakse stsenaariumi, kus osalised maksed tehakse hankija arvele ja võetakse skonto."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bfa93961e4e3a7c1c68494ffae94c877aa466183
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Hankija osalise makse ja lõpliku makse tasakaalustamine enne allahindluse kuupäeva.

[!include [banner](../includes/banner.md)]

Selles artiklis käsitletakse stsenaariumi, kus osalised maksed tehakse hankija arvele ja võetakse skonto.

Fabrikam ostab kaupu hankijalt 3064. Hankija annab Fabrikamile 1 protsenti skontot, kui arve tasutakse 14 päeva jooksul. Arved tuleb tasuda 30 päeva jooksul. Hankija lubab Fabrikamil kasutada skontosid ka osaliste maksete korral. Tasakaalustamise parameetrid asuvad lehel **Ostureskontro parameetrid**. April sisestab 25. juunil arve hankijale 3064 summas 1000,00.

## <a name="vendor-invoice-on-june-25"></a>Hankija arve 25. juunil
25. juunil sisestab April hankijale 3064 arve summas 1000,00. April saab vaadata seda kannet lehel **Hankija kanded**.

| Kanne   | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo   | Valuuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10010 | 25.06.2015 | 10010   |                                      | 1 000,00                              | –1000,00 | USA dollar      |

Lehelt **Hankijad** avab April lehe **Kannete tasakaalustamine**. Ta saab kasutada lehte **Kannete tasakaalustamine**, et vaadata skonto kuupäevi ja summasid. Tähtaeg on 25. juulil ja kui arve on tasutud 9. juuliks, on saadaval skonto summas –10,00.

| Märge | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Tavaline            | Inv-10010 | 3064    | 25.06.2015 | 25.07.2015 | 10010   | 1 000,00                       | USA dollar      | 990,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine**allosas.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | -10,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | -10,00    |

Skonto summa vaatamiseks klõpsab April vahekaarti **Skonto**.

| Skonto kuupäev | Skonto summa | Summa kandevaluutas |
|--------------------|----------------------|--------------------------------|
| 09.07.2015           | 10,00                | 990,00                         |
| 25.07.2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Osaline makse 1. juulil, kasutades lehte Kannete tasakaalustamine
April saab luua sellele maksele maksetöölehe, avades jaotises Ostureskontro lehe **Maksetööleht**. Ta loob uue töölehe ja sisestab hankijale 3064 rea. Ta avab seejärel lehe **Kannete tasakaalustamine**, et ta saaks arve tasakaalustamiseks märgistada. April märgib arve ja muudab välja **Tasakaalustatav summa** väärtuseks **–500,00**. Väljal **Skonto summa** näeb ta, et täieliku arve skonto summa on **–10,00** ja skonto summa väljal **Skonto summa võtmiseks** on **–5,05**. Seetõttu tasakaalustab April arve summas –505,05.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1 000,00                       | USA dollar      | ‑500,00          |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | -10,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | ‑5,05     |

April soovib tasakaalustada täpselt poole arvest. Seega muudab ta välja **Tasakaalustatav summa** väärtuseks **–495,00**. Tasakaalustatav kogusumma on nüüd 500,00. See summa sisaldab skontot –5,00.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1 000,00                       | USA dollar      | –495,00          |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | -10,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | –5,00     |

April sulgeb lehe **Kannete tasakaalustamine**. Töölehel luuakse makserida summas 495,00 ja April sisestab töölehe. April saab hankija kandeid lehel **Hankija kanded** üle vaadata. Ta näeb, et arve saldo on –500,00. Samuti näeb ta makset summas 495,00 ja skontot summas 5,00.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Arve          | 25.06.2015 | 10010   |                                      | 1 000,00                              | ‑500,00 | USA dollar      |
| APP‑10010  | Makse          | 01.07.2015  |         | 495,00                               |                                       | 0,00    | USA dollar      |
| DISC‑10010 | Skonto    | 01.07.2015  |         | 5,00                                 |                                       | 0,00    | USA dollar      |

## <a name="remaining-amount-paid-on-july-8"></a>Ülejäänud summa on makstud 8. juulil
April maksab ülejäänud arve hankijale 3064 8. juulil, mis on allahindluse perioodil. April loob 8. juulil maksetöölehe ja märgib kande tasakaalustamiseks. Ta näeb, et tasakaalustatav summa on 495,00. Välja **Eeldatav skonto** väärtus on **–5,00**, sest skonto summas 5,00 oli juba varem arvestatud.

|                         |        |
|-------------------------|--------|
| Kokku märgitud            | 495,00 |
| Eeldatav skonto | –5,00  |

Teave märgitud kande kohta ilmub lehe **Avatud kannete tasakaalustamine** ruudustikule.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1 000,00                       | USA dollar      | 495,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 10,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 5,00      |
| Skonto summa võtmiseks | 5,00      |

April sisestab maksetöölehe ja vaatab üle hankija kanded lehel **Hankija kanded**. Arve saldo on nüüd 0,00 ning April näeb kaht makset ja kaht skontot.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Arve          | 25.06.2015 | 10010   |                                      | 1 000,00                              | 0,00    | USA dollar      |
| APP‑10010  |  Makse         | 01.07.2015  |         | 495,00                               |                                       | 0,00    | USA dollar      |
| DISC‑10010 | Skonto    | 01.07.2015  |         | 5,00                                 |                                       | 0,00    | USA dollar      |
| APP‑10011  | Makse          | 08.07.2015  |         | 495,00                               |                                       | 0,00    | USA dollar      |
| DISC‑10011 | Skonto    | 08.07.2015  |         | 5,00                                 |                                       | 0,00    | USA dollar      |






