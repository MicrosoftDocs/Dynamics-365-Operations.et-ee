---
title: Osalise makse tasumine enne allahindluse kuupäeva ja lõplik makse pärast allahindluse kuupäeva
description: Selles artiklis läbitakse stsenaarium, kus tehakse mitu osalist makset, mõned skontoperioodil ja teised väljaspool skontoperioodi.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 828c82d88bef1d942af1219505af591d27043fa5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780240"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Osalise makse tasumine enne allahindluse kuupäeva ja lõplik makse pärast allahindluse kuupäeva

[!include [banner](../includes/banner.md)]

Selles artiklis läbitakse stsenaarium, kus tehakse mitu osalist makset, mõned skontoperioodil ja teised väljaspool skontoperioodi.

Fabrikam ostab kaubad hankijalt 3057. Fabrikam saab 1 protsenti skontot, kui arve tasutakse 14 päeva jooksul. Arved tuleb tasuda 30 päeva jooksul. Hankija lubab Fabrikamil kasutada skontosid ka osaliste maksete korral. Tasakaalustamise parameetrid asuvad lehel **Ostureskontro parameetrid**.

## <a name="invoice-on-june-25"></a>Arve 25. juunil
25. juunil sisestab April hankijale 3057 arve summas 1000,00. April saab vaadata seda kannet lehel **Hankija kanded**.

| Kanne   | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo   | Valuuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10020 | Arve          | 6/25/2020 | 10020   |                                      | 1,000.00                              | –1000,00 | USA dollar      |

## <a name="partial-payment-on-july-2"></a>Osaline makse 2. juulil
2. juulil soovib April tasakaalustada sellest arvest 300.00. Makse puhul on õigus arvestada allahindlust, kuna Fabrikam arvestab osalistelt maksetelt allahindlust. Seetõttu maksab April 297.00 ja arvestab allahindlust 3.00. Ta loob maksetöölehe ja sisestab hankijale 3057 rea. Ta avab seejärel lehe **Kannete tasakaalustamine**, et ta saaks arve tasakaalustamiseks märgistada.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | Inv-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | –1000,00                      | USA dollar      | –297.00          |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

| Väli                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 7/09/2020 |
| Skonto summa         | -10,00    |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | –3.00     |

Seejärel sisestab April makse. Arve saldo on nüüd 700.00. April saab vaadata seda kannet lehel **Hankija kanded**.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Arve          | 6/25/2020 | 10020   |                                      | 1,000.00                              | –700.00 | USA dollar      |
| APP‑10020  | Makse          | 7/1/2020  |         | 297.00                               |                                       | 0.00    | USA dollar      |
| DISC‑10020 | Sularahakonto    | 7/1/2020  |         | 3.00                                 |                                       | 0.00    | USA dollar      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Ülejäänud makse 15. juulil, kasuta skontot = tavaline
April maksab ülejäänud arve 15. juulil, mis on pärast allahindluse perioodi. Lehel **Avatud kannete tasakaalustamine** ei kuvata väljal **Eeldatav skonto** allahindluse summat ja välja **Skonto summa** väärtus on **0.00**. Kui April tasub ülejäänud 700.00, siis täiendavat allahindlust ei rakendata.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | Inv-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | –700.00                        | USA dollar      | –700.00          |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas. April näeb, et ta on juba kasutanud allahindlust summas 3.00.

| Väli                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 7/09/2020 |
| Skonto summa         | 0.00      |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | –3.00     |
| Skonto summa võtmiseks | 0,00      |

Seejärel sisestab April makse. Kui ta avab lehe **Hankija kanded**, näeb ta, et arve saldo on 0.00. Samuti näeb ta kaht makset. Üks makse on summas 297.00 allahindlusega 3.00 ja teine makse summas 700.00.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Arve          | 6/25/2020 | 10020   |                                      | 1,000.00                              | 0.00    | USA dollar      |
| APP‑10020  | Makse          | 7/1/2020  |         | 297.00                               |                                       | 0.00    | USA dollar      |
| DISC‑10020 | Sularahakonto    | 7/1/2020  |         | 3.00                                 |                                       | 0.00    | USA dollar      |
| APP‑10021  | Makse          | 7/15/2020 |         | 700,00                               |                                       | 0.00    | USA dollar      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Ülejäänud makse 15. juulil, kasuta skontot = alati
Kui hankija laseb Aprilil võtta soodustust isegi siis, kui April tasub pärast skonto kuupäeva, saab ta muuta välja **Kasuta skontot** väärtuseks **Alati**. Säte **Arvuta skontod osaliste maksete jaoks** kirjutatakse üle ja tehakse allahindlus. Maksesummaks on 693.00 ja allahindluseks on järelejäänud 7.00.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|----------|----------|------|------|-----------|-----------|---------|-----------------------|---------------------------------------|----------|------------------|
| Valitud | Alati            | Inv-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | 700,00                   |                   | USA dollar      | –693.00          |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas.

| Väli                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 7/09/2020 |
| Skonto summa         | 7.00      |
| Kasuta skontot            | Alati    |
| Võetud skonto          | –3.00     |
| Skonto summa võtmiseks | –7.00     |

Seejärel sisestab April makse. Kui ta avab lehe **Hankija kanded**, näeb ta, et arve saldo on 0.00. Samuti näeb ta kaht makset. Üks makse on summas 297.00 allahindlusega 3.00 ja teine makse summas 693.00 allahindlusega 7.00.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Arve          | 6/25/2020 | 10020   |                                      | 1,000.00                              | 0.00    | USA dollar      |
| APP‑10020  | Makse          | 7/1/2020  |         | 297.00                               |                                       | 0.00    | USA dollar      |
| DISC‑10020 | Sularahakonto    | 7/1/2020  |         | 3.00                                 |                                       | 0.00    | USA dollar      |
| APP‑10021  | Makse          | 7/15/2020 |         | 693,00                               |                                       | 0.00    | USA dollar      |
| DISC‑10021 | Sularahakonto    | 7/15/2020 |         | 7.00                                 |                                       | 0.00    | USA dollar      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
