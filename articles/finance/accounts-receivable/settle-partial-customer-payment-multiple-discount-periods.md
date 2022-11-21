---
title: Mitme allahindlusperioodiga osalise kliendimakse tasakaalustamine
description: See artikkel näitab, kuidas mitme allahindlusperioodi korral osalisi kliendi makseid tasakaalustatakse.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62defda8831d2915050fc6822f60a905f067fe88
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778435"
---
# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Mitme allahindlusperioodiga osalise kliendimakse tasakaalustamine

[!include [banner](../includes/banner.md)]

See artikkel näitab, kuidas mitme allahindlusperioodi korral osalisi kliendi makseid tasakaalustatakse.

Fabrikam pakub kliendile 4031 kahte skontoperioodi. Klient saab 2-protsendilise skonto, kui arve tasutakse viie päeva jooksul ja 1-protsendilise skonto, kui arve tasutakse 14 päeva jooksul. Fabrikam pakub osalistele maksetele ka skontosid. Tasakaalustamise parameetrid asuvad lehel **Müügireskontro parameetrid**.

## <a name="invoice"></a>Arve
25. juunil sisestab Arnie kliendile 4031 arve summas 1000,00. Selle arve sularahakontode ülevaatamisel näeb Arnie, et klient 4031 saab allahindlust 20.00, kui ta tasub arve 30. juuniks. Kui arve tasutakse 9. juuliks, saab klient 10,00 allahindlust.

| Skonto kuupäev | Skonto summa | Summa kandevaluutas |
|--------------------|----------------------|--------------------------------|
| 30.6.2020          | 20.00                | 980,00                         |
| 7/9/2020           | 10.00                | 990.00                         |
| 7/25/2020          | 0.00                 | 1,000.00                       |

Arnie saab vaadata seda kannet lehel **Kliendi kanded**.

| Kanne   | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo  | Valuuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI‑10030 | Arve          | 6/25/2020 | 10030   | 1,000.00                             |                                       | 1,000.00 | USA dollar      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Osaline makse enne skonto kuupäeva
28. juunil teeb klient 4031 osalise makse summas 294,00. Kuna 28. juuni jääb esimesse skontoperioodi, saab klient allahindlust summas 6,00. Lehel **Kannete tasakaalustamine** on suvandi **Skonto summa** väärtus 20,00 ja suvandi **Skonto summa võtmiseks** väärtus on 6,00.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10030 | 4031    | 6/25/2020 | 7/25/2020 | 10030   | 1,000.00                       | USA dollar      | 294,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas. Kui te ei muuda suvandi **Tasakaalustatav summa** väärtuseks **294,00**, erinevad suvandi **Skonto summa** kuvatavad väärtused. Siiski arvestatakse makse sisestamisel skontona 6,00, kuna tasakaalustamine korrigeerib suvandi **Tasakaalustatav summa** väärtust automaatselt teie eest.

| &nbsp;                       | &nbsp;    |
|------------------------------|-----------|
| Skonto kuupäev           | 30.6.2020 |
| Skonto summa         | 20.00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 6,00      |

Pärast Arnie makse sisestamist on arve saldo 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Osaline makse enne teist skonto kuupäeva
8. juulil maksab klient ülejäänud arve summa. Arvestatakse allahindlusega summas 7,00 (1 protsent), sest makse tehti teisel skontoperioodil.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------|-----------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10030 | 4031    | 6/25/2020 | 7/25/2020 | 10030   | 700,00       |            | USA dollar      | 693,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

| &nbsp;                       | &nbsp;    |
|------------------------------|-----------|
| Skonto kuupäev           | 7/09/2020 |
| Skonto summa         | 30.00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 6,00      |
| Skonto summa võtmiseks | 7,00      |

Arve saldo on nüüd 0,00. Arnie vaatab seda teavet lehel **Kliendi kanded**.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI‑10030  | Arve          | 6/25/2020 | 10030   | 1,000.00                             |                                       | 0.00    | USA dollar      |
| ARP‑10030  |  Makse         | 6/28/2020 |         |                                      | 294,00                                | 0.00    | USA dollar      |
| DISC‑10030 |  Sularahakonto   | 6/28/2020 |         |                                      | 6,00                                  | 0.00    | USA dollar      |
| ARP‑10031  |  Makse         | 7/8/2020  |         |                                      | 693,00                                | 0.00    | USA dollar      |
| DISC‑1031  |  Sularahakonto   | 7/8/2020  |         |                                      | 7.00                                  | 0.00    | USA dollar      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
