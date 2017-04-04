---
title: Lahendada osalise kliendi makse, mis on mitme allahindluse perioodide
description: "See artikkel näitab, kuidas mitme allahindlusperioodi korral osalisi kliendi makseid tasakaalustatakse."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9da48c7861f48ec2a154ac12616149d1208346cf
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Lahendada osalise kliendi makse, mis on mitme allahindluse perioodide

See artikkel näitab, kuidas mitme allahindlusperioodi korral osalisi kliendi makseid tasakaalustatakse.

Fabrikam pakub kliendile 4031 kahte skontoperioodi. Klient saab 2-protsendilise skonto, kui arve tasutakse viie päeva jooksul ja 1-protsendilise skonto, kui arve tasutakse 14 päeva jooksul. Fabrikam pakub osalistele maksetele ka skontosid. Lahendamise parameetrid asuvad ka **Müügireskontro parameetrid** lehel.

## <a name="invoice"></a>Arve
25. juuni Arnie siseneb ja postitusi arve kliendi 4031 1000.00 dollarit. Kui ta kommentaare selle arve skonto, Arnie näeb kliendi 4031 saab 20.00 hinnaalandit, kui arve on tasutud 30. juuni. Kui arve tasub juuli 9, klient saab 10.00 hinnaalandit.

| Skonto kuupäev | Skonto summa | Summa kandevaluutas |
|--------------------|----------------------|--------------------------------|
| 30.06.2015          | 20,00                | 980,00                         |
| 09.07.2015           | 10,00                | 990,00                         |
| 25.07.2015          | 0,00                 | 1 000,00                       |

Arnie saab vaadata seda kannet lehel** Kliendi kanded**.

| Kanne   | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo  | Valuuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI‑10030 | Arve          | 25.06.2015 | 10030   | 1 000,00                             |                                       | 1 000,00 | USA dollar      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Osaline makse enne skonto kuupäeva
28. juunil teeb klient 4031 osalise makse summas 294,00. Kuna 28. juuni jääb esimesse skontoperioodi, saab klient allahindlust summas 6,00. Lehel **Kannete tasakaalustamine** on suvandi** Skonto summa** väärtus 20,00 ja suvandi **Skonto summa võtmiseks** väärtus on 6,00.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10030 | 4031    | 25.06.2015 | 25.07.2015 | 10030   | 1 000,00                       | USA dollar      | 294,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas. Kui te ei muuda suvandi **Tasakaalustatav summa** väärtuseks **294,00**, erinevad suvandi **Skonto summa** kuvatavad väärtused. Siiski arvestatakse makse sisestamisel skontona 6,00, kuna tasakaalustamine korrigeerib suvandi **Tasakaalustatav summa** väärtust automaatselt teie eest.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 30.06.2015 |
| Skonto summa         | 20,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 6,00      |

Pärast Arnie makse sisestamist on arve saldo 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Osaline makse enne teist skonto kuupäeva
8. juulil maksab klient ülejäänud arve summa. Arvestatakse allahindlusega summas 7,00 (1 protsent), sest makse tehti teisel skontoperioodil.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10030 | 4031    | 25.06.2015 | 25.07.2015 | 10030   | 700,00                               |                                       | USA dollar      | 693,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 30,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 6,00      |
| Skonto summa võtmiseks | 7,00      |

Arve saldo on nüüd 0,00. Arnie vaatab seda teavet lehel **Kliendi kanded**.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI‑10030  | Arve          | 25.06.2015 | 10030   | 1 000,00                             |                                       | 0,00    | USA dollar      |
| ARP‑10030  |  Makse         | 28.06.2015 |         |                                      | 294,00                                | 0,00    | USA dollar      |
| DISC‑10030 |  Skonto   | 28.06.2015 |         |                                      | 6,00                                  | 0,00    | USA dollar      |
| ARP‑10031  |  Makse         | 08.07.2015  |         |                                      | 693,00                                | 0,00    | USA dollar      |
| DISC‑1031  |  Skonto   | 08.07.2015  |         |                                      | 7,00                                  | 0,00    | USA dollar      |




