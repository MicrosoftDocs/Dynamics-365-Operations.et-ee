---
title: Osaliste ja lõplike maksete täielik tasakaalustamine enne allahindluse kuupäeva
description: See artikkel pakub stsenaariume näitamiseks, kuidas kirjendada kliendi osalisi makseid ja võtta skonto perioodil skontosid.
author: abruer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7d13b533cda70dba432b2de20a65d6dcedb6863
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028079"
---
# <a name="settle-partial-and-final-payments-in-full-before-the-discount-date"></a>Osaliste ja lõplike maksete täielik tasakaalustamine enne allahindluse kuupäeva

[!include [banner](../includes/banner.md)]

See artikkel pakub stsenaariume näitamiseks, kuidas kirjendada kliendi osalisi makseid ja võtta skonto perioodil skontosid.

Fabrikam müüb kaupu kliendile 4028. Fabrikam pakub skontot 1%, kui arve tasutakse 14 päeva jooksul. Arved tuleb tasuda 30 päeva jooksul. Fabrikam pakub osalistele maksetele ka skontosid. Tasakaalustamise parameetrid asuvad lehel **Müügireskontro parameetrid**.

## <a name="customer-invoice"></a>Kliendiarve
25. juunil sisestab Arnie kliendile 4028 arve summas 1000,00. Arnie saab vaadata seda kannet lehel **Kliendi kanded**.

| Kanne   | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo  | Valuuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI‑10010 | Arve          | 25.06.2015 | 10010   | 1 000,00                             |                                       | 1 000,00 | USA dollar      |

Arnie saab arve kuupäevi ja skontode summasid vaadata leheküljel **Klient** või **Kliendi kanded**, avades seal lehekülje **Kannete tasakaalustamine**. Tähtaeg on 25. juulil ja kui arve on tasutud 9. juuliks, on saadaval skonto summas 10,00.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1 000,00                       | USA dollar      | 990,00           |

Teave märgitud arve skonto kohta kuvatakse lehekülje **Kannete tasakaalustamine** allosas.

|    &nbsp;                    |  &nbsp;   |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 10,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 10,00     |

Skonto summa vaatamiseks klõpsab Arnie vahekaarti **Skonto**.

| Skonto kuupäev | Skonto summa | Summa kandevaluutas |
|--------------------|----------------------|--------------------------------|
| 09.07.2015           | 10,00                | 990,00                         |
| 25.07.2015          | 0,00                 | 1 000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Osalise makse tegemine kasutades lehekülge Kliendimaksete sisestamine
Klient 4028 saadab makse 500,00 1. juulil. Selle makse sisestamiseks ei klõpsa Arnie nuppu **Read**. Selle asemel salvestab Arnie makse, luues uue maksetöölehe ja avades seejärel lehekülje **Kliendimaksete sisestamine**. Arnie sisestab makseteabe ja märgib sisestatud arve. Kui Arnie sisestab summaks **500.00**, sisestavad nad ka **500.00** ruudustiku **Makstav summa** väljale. Kuna Fabrikam võimaldab osaliste maksete sularaha konto soodustust, näeb Arnie et arvesse võetakse ka osalist sularahasoodustust 5.05. Seda skontot arvutatakse järgmiselt: 500,00 ÷ 0,99 × 0,01 = 5,05. (Summa 500,00 jagatakse selles arvutuses 0,99-ga, kuna skonto on 1 protsent. Seetõttu tasub klient 99% arvest. Seejärel korrutatakse tulemus skonto protsendiga, mis on 1% ehk 0,01. Kui klient võtab täieliku allahindluse 10,00, peab tasakaalustatav summa olema 990,00. Allahindluse teave kuvatakse lehe **Sisesta kliendimaksed** lehe allservas olevas ruudustikus.

| Skonto summa võtmiseks | Võetud skonto | Makstav summa |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Osalise makse tegemine töölehe ridu kasutades
Arve sisestamiseks saab Arnie maksetöölehe lehekülje **Kliendimaksete sisestamine** asemel kasutada valikut **Read**. Kuvatakse maksetööleht, kuhu Arnie saab sisestada rea kliendile 4028. Seejärel avab Arnie lehe **Kannete tasakaalustamine**, et ta saaks märkida arve tasakaalustamiseks. Arnie märgib arve ja muudab välja **Tasakaalustatav summa** väärtuseks **500,00**. Jällegi, Arnie näeb väljal **Sularaha konto summa** väljal **10.00** täieliku arve jaoks ja summa väljal **Sularaha konto summa võtmiseks** on **5.05**. Seetõttu tasakaalustab Arnie arve summas 505,05.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1 000,00                       | USA dollar      | 500,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|        &nbsp;                | &nbsp;    |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 10,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 5,05      |

Kui klient soovib tasakaalustada täpselt poole arvest, saadab ta makse summas 495,00. Sel juhul sisestab Arnie väljale **Tasakaalustatav summa** **495,00**. Arvesse võetakse skontot summas 5,00, seega on tasakaalustuse kogusumma 500,00.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1 000,00                       | USA dollar      | 495,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|     &nbsp;                   | &nbsp;    |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 10,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 5,00      |

Arnie sulgeb lehekülje **Kannete tasakaalustamine**. Töölehel luuakse makserida summas 495,00 ja Arnie sisestab töölehe. Ta saab kliendi kanded üle vaadata leheküljel **Kliendikanded**. Sellel lehel näeb Arnie, et arve saldo on 500,00. Samuti näeb ta makset summas 495.00 ja sularahakontot summas 5.00.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI‑10010  | Arve          | 25.06.2015 | 10010   | 1 000,00                             |                                       | 500,00  | USA dollar      |
| ARP‑10010  |  Makse         | 01.07.2015  |         |                                      | 495,00                                | 0,00    | USA dollar      |
| DISC‑10010 |  Skonto   | 01.07.2015  |         |                                      | 5,00                                  | 0,00    | USA dollar      |

## <a name="payment-for-the-remaining-amount"></a>Makse järelejäänud summas
Klient 4028 maksab 8. juulil järelejäänud summa 495,00, seega jääb makse skonto perioodi. Arnie loob 8. juulil maksetöölehe ja märgib kande tasakaalustamiseks. Arnie näeb, et tasakaalustatav summa on 495.00. Välja **Eeldatav skonto** väärtus on **5,00**, kuna skonto summas 5,00 oli juba varem arvestatud.

|   &nbsp;                | &nbsp; |
|-------------------------|--------|
| Kokku märgitud            | 495,00 |
| Eeldatav skonto | 5,00   |

Teave märgitud kande kohta ilmub lehe **Avatud kannete tasakaalustamine** ruudustikule.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10010 | 4028    | 25.06.2015 | 25.07.2015 | 10010   | 1 000,00                       | USA dollar      | 495,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Skonto kuupäev           | 09.07.2015 |
| Skonto summa         | 10,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 5,00      |
| Skonto summa võtmiseks | 5,00      |

Arnie sisestab töölehe ja vaatab üle kliendi kanded leheküljel **Kliendikanded**. Arve saldo on nüüd 0,00 ja Arnie näeb kaht makset ja kaht skontot.

| Kanne    | Kande tüüp | Kuupäev      | Arve | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo | Valuuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI‑10010  | Arve          | 25.06.2015 | 10010   | 1 000,00                             |                                       | 0,00    | USA dollar      |
| ARP‑10010  | Makse          | 01.07.2015  |         |                                      | 495,00                                | 0,00    | USA dollar      |
| DISC‑10010 | Skonto    | 01.07.2015  |         |                                      | 5,00                                  | 0,00    | USA dollar      |
| ARP‑10011  | Makse          | 08.07.2015  |         |                                      | 495,00                                | 0,00    | USA dollar      |
| DISC‑10011 | Skonto    | 08.07.2015  |         |                                      | 5,00                                  | 0,00    | USA dollar      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]