---
title: "Kliendi osalise makse tasakaalustamine enne allahindluse kuupäeva koos lõpliku maksega pärast allahindluse kuupäeva"
description: "See artikkel käsitleb klientidele esitatavate arvete ja maksete tasakaalustamise mõju. Stsenaarium keskendub mõjule alammoodulis, mitte pearaamatus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f3843935cf17aeb0fd358398dccbca4cf494b132
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Kliendi osalise makse tasakaalustamine enne allahindluse kuupäeva koos lõpliku maksega pärast allahindluse kuupäeva

[!include [banner](../includes/banner.md)]

See artikkel käsitleb klientidele esitatavate arvete ja maksete tasakaalustamise mõju. Stsenaarium keskendub mõjule alammoodulis, mitte pearaamatus.

Fabrikam müüb kaupu kliendile 4027. Fabrikam pakub skontot 1%, kui arve tasutakse 14 päeva jooksul. Arved tuleb tasuda 30 päeva jooksul. Fabrikam pakub osalistele maksetele ka skontosid. Tasakaalustamise parameetrid asuvad lehel **Müügireskontro parameetrid**.

## <a name="invoice"></a>Arve
25. juunil sisestab Arnie kliendile 4027 arve summas 1000,00. Arnie saab selle arve vaatamiseks kasutada nuppu **Kanded** lehel **Kliendid**.

| Kanne   | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo  | Valuuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI‑10020 | Arve          | 25.06.2015 | 10020   | 1 000,00                             |                                       | 1 000,00 | USA dollar      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Osaline makse enne skonto kuupäeva
2. juuli tasub klient 4027 arve eest osamakse summas 297,00. Makse on sobilik skonto jaoks, kuna Fabrikam pakub skontosid osalistele maksetele ja osalise makse on tehtud enne skonto kuupäeva. Seetõttu saab klient 4027 skonto 3,00. Arnie registreerib makse kliendi 4027 kohta, kasutades maksetöölehte. Seejärel avab Arnie lehe **Kannete tasakaalustamine**, et ta saaks märkida arve tasakaalustamiseks.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10020 | 4027    | 25.06.2015 | 25.07.2015 | 10020   | 1 000,00                             | USA dollar      | 297.00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas. Kui te ei muuda suvandi **Tasakaalustatav summa** väärtuseks 297,00, erinevad suvandi **Skonto summa** kuvatavad väärtused. Siiski arvestatakse makse sisestamisel skontona 3,00, kuna tasakaalustamine korrigeerib suvandi **Tasakaalustatav summa väärtust** automaatselt teie eest.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 10,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 3,00      |

Arnie sisestab selle makse. Arve saldo on nüüd 700.00. Kliendile on näha järgmised kanded.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI‑10020  | Arve          | 25.06.2015 | 10020   | 1 000,00                             |                                       | 700.00  | USA dollar      |
| ARP‑10020  |  Makse         | 01.07.2015  |         |                                      | 297.00                                | 0,00    | USA dollar      |
| DISC‑10020 |  Skonto   | 01.07.2015  |         |                                      | 3,00                                  | 0,00    | USA dollar      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Maksejääk pärast skonto kuupäeva
11. juulil, mis on pärast allahindluse perioodi, maksab klient 4027 arve ülejäänud summa. Lehel **Kannete tasakaalustamine** ei kuvata väljal **Eeldatav skonto** allahindluse summat ja välja **Skonto summa** väärtus on **0,00**. Kui klient 4027 tasub ülejäänud 700,00, siis täiendavat allahindlust ei rakendata.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10020 | 4027    | 25.06.2015 | 25.07.2015 | 10020   | 700.00                               | USA dollar      | 700.00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 0,00      |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 3,00      |
| Skonto summa võtmiseks | 0,00      |

Kui Arnie muudab välja **Kasuta skontot** sätteks **Alati**, tühistatakse säte **Arvuta skontod osaliste maksete jaoks** ja skonto rakendub. Maksesumma muutub väärtusele 693,00 ja skonto on järelejäänud 7,00.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valitud | Alati            | FTI‑10020 | 4027    | 25.06.2015 | 25.07.2015 | 10020   | 700.00                               |                                       | USA dollar      | 693.00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 7,00      |
| Kasuta skontot            | Alati    |
| Võetud skonto          | 3,00      |
| Skonto summa võtmiseks | 7,00      |

Arnie muudab välja **Kasuta skontot** väärtuseks uuesti **Tavaline**, kuna ta ei lase sellel kliendil kasutada järelejäänud skontot summas 7,00. Seejärel sisestab Arnie makse. Kui Arnie avab lehe**Kliendi kanded**, näeb ta, et arve saldo on 0,00. Samuti näeb ta kaht makset. Üks makse on summas 297,00 skontoga 3,00 skonto ja teine makse summas 700,00.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI‑10020  | Arve          | 25.06.2015 | 10020   | 1 000,00                             |                                       | 0,00    | USA dollar      |
| ARP‑10020  |                  | 01.07.2015  |         |                                      | 297.00                                | 0,00    | USA dollar      |
| DISC‑10020 |                  | 01.07.2015  |         |                                      | 3,00                                  | 0,00    | USA dollar      |
| ARP‑10021  |                  | 7/11/2015 |         |                                      | 700.00                                | 0,00    | USA dollar      |






