---
title: Mitme allahindlusperioodiga osalise hankijamakse tasakaalustamine
description: See artikkel käsitleb stsenaariumi, kus mitut skontot pakkuvale hankijale tehakse mitu osalist makset.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da69d61c657ddc168a27a97fe16909d5f60eb4fd
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778033"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Mitme allahindlusperioodiga osalise hankijamakse tasakaalustamine

[!include [banner](../includes/banner.md)]

See artikkel käsitleb stsenaariumi, kus mitut skontot pakkuvale hankijale tehakse mitu osalist makset. 

Hankija 3054 pakub Fabrikamile 2-protsendist skontot, kui arve tasutakse viie päeva jooksul ja 1-protsendist skontot, kui arve tasutakse 14 päeva jooksul.

## <a name="invoice"></a>Arve
28. juunil loob April hankijale 3054 arve summas 1000,00. April saab vaadata seda kannet lehel **Hankija kanded**.

| Kanne   | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo   | Valuuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10060 | 6/28/2020 | 10060   |                                      | 1,000.00                              | –1000,00 | USA dollar      |

Selle arve jaoks on saadaval järgmised skonto kuupäevad ja summad.

| Skonto kuupäev | Skonto summa | Summa kandevaluutas |
|--------------------|----------------------|--------------------------------|
| 7/3/2020           | 20.00                | 980,00                         |
| 7/12/2020          | 10.00                | 990.00                         |
| 7/25/2020          | 0.00                 | 1,000.00                       |

## <a name="payment-on-july-2"></a>Makse 2. juulil
2. juulil soovib April tasuda arve suhtes 300,00. Ta loob ühekordse makse, kasutades ostureskontro lehte **Maksetööleht**. Ta lisab rea hankijale 3054 ja sisestab maksesumma **300,00**. Seejärel avab April lehe **Kannete tasakaalustamine**, et ta saaks märkida arve tasakaalustamiseks. Ta värskendab välja **Tasakaalustatav summa** väärtusele **300,00** ja näeb, et välja **Arvestatav skonto summa** väärtus on nüüd **6,12**. Kuna see makse on tehtud esimesel allahindlusperioodil, arvestatakse 2-protsendist allahindlust.

| Märge | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Tavaline            | Inv-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USA dollar      | 300.00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

| Väli                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 7/02/2020 |
| Skonto summa         | ‑20,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | –6,12     |

Kuna skonto on saadaval, soovib April muuta maksesummat nii, et kogu tasakaalustatud summa oleks nii makse kui ka skonto puhul 300,00. Ta muudab välja **Tasakaalustatav summa** väärtuseks **294,00** ja näeb, et välja **Arvestatav skonto summa** väärtus on nüüd **6,00**.

| Märge | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Tavaline            | Inv-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USA dollar      | 294,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

| Väli                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 7/02/2020 |
| Skonto summa         | ‑20,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | –6,00     |

April sisestab makse. April saab vaadata kandeid lehel **Hankija kanded**. Ta näeb, et arvele on rakendatud 300,00. See summa sisaldab allahindlust 6,00. Seetõttu on jääksaldo 700,00.

| Kanne    | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | –700.00 | USA dollar      |
| APP‑10060  | 7/2/2020  |         | 294,00                               |                                       | 0.00    | USA dollar      |
| DISC‑10060 | 7/2/2020  |         | 6,00                                 |                                       | 0.00    | USA dollar      |

## <a name="payment-on-july-8"></a>Makse 8. juulil
8. juulil teeb April arve arve eest täiendava makse. Summa sisestamiseks avab ta lehe **Kannete tasakaalustamine** ja seejärel klõpsab vahekaarti **Skonto**. Ta näeb kahe saadaoleva skonto kuupäevi ja summasid. Kuna see makse on tehtud teisel allahindlusperioodil, on saadaval 1-protsendine allahindlus (või summas 5,00) See summa arvutatakse poolena 1-protsendisest allahindlusest summalt 1000,00 või poolena summast 10,00.

| Skonto kuupäev | Skonto summa | Summa kandevaluutas |
|--------------------|----------------------|--------------------------------|
| 7/3/2020           | 20.00                | 680.00                         |
| 7/12/2020          | 10.00                | 690.00                         |
| 7/25/2020          | 0.00                 | 700,00                         |

April otsustab tasuda 495,00 ja saab skonto 5,00. Seetõttu on tasakaalustatav kogusumma 500,00.

| Märge | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Tavaline            | Inv-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USA dollar      | 495.00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

| Väli                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 7/12/2020 |
| Skonto summa         | -10,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | –6,00     |
| Skonto summa võtmiseks | –5,00     |

Lehel **Hankija kanded** näeb April, et uus saldo on 200,00.

| Kanne    | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | –200.00 | USA dollar      |
| APP‑10060  | 7/2/2020  |         | 294,00                               |                                       | 0.00    | USA dollar      |
| DISC‑10060 | 7/2/2020  |         | 6,00                                 |                                       | 0.00    | USA dollar      |
| APP‑10061  | 7/12/2020 |         | 495.00                               |                                       | 0.00    | USA dollar      |
| DISC‑10061 | 7/12/2020 |         | 5.00                                 |                                       | 0.00    | USA dollar      |

## <a name="payment-on-july-20"></a>Makse 20. juulil
20. juulil loob April lõpliku makse summale 200,00. Skontot ei arvestata, kuna makse tehakse pärast mõlemat allahindlusperioodi. Arve saldo on 0,00 eurot.

| Kanne    | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | –200.00 | USA dollar      |
| APP‑10060  | 7/2/2020  |         | 294,00                               |                                       | 0.00    | USA dollar      |
| DISC‑10060 | 7/2/2020  |         | 6,00                                 |                                       | 0.00    | USA dollar      |
| APP‑10061  | 7/12/2020 |         | 495.00                               |                                       | 0.00    | USA dollar      |
| DISC‑10061 | 7/12/2020 |         | 5.00                                 |                                       | 0.00    | USA dollar      |
| APP‑10062  | 7/20/2020 |         | 200,00                               |                                       | 0.00    | USA dollar      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
