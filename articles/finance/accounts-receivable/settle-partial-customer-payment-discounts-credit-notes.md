---
title: Kliendi osalise makse, millel on kliendi kreeditarvetel allahindlusi, tasakaalustamine
description: See artikkel tutvustab stsenaariumi, kus kreeditarvelt arvestatakse skontot, samas kui algsel arvel oli samuti skonto.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f64b9b9cd4fa65d17ba30fb87a688411becd5a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780220"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Kliendi osalise makse, millel on kliendi kreeditarvetel allahindlusi, tasakaalustamine

[!include [banner](../includes/banner.md)]

See artikkel tutvustab stsenaariumi, kus kreeditarvelt arvestatakse skontot, samas kui algsel arvel oli samuti skonto. 

Fabrikam võimaldab klientidel kasutada osalistel maksetel ja ka kreeditarvetel skontosid. Skontot saab arvestada kreeditarvel, kui see on väljastatud arve kohta, mille puhul kasutas klient skontot. Täissummas krediidi pakkumisel saate krediteerida kliendi saldo summas, mis jätab välja kliendi kasutatud skonto protsendi. Tasakaalustamise parameetrid asuvad lehel **Müügireskontro parameetrid**.

## <a name="invoice-and-credit-note"></a>Arve ja kreeditarve
Kliendil 4035 on arve summale 1000,00 ja kreeditarve summale 100,00. Igal dokumendil on 1% allahindlust, kui see tasutakse 14 päeva jooksul. Arnie saab vaadata seda teavet lehel **Kliendi kanded**.

| Kanne    | Kande tüüp | Kuupäev      | Arve  | Deebeti summa kande valuutas | Kreediti summa kande valuutas | Saldo  | Valuuta |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI‑10050  | Arve          | 6/28/2020 | 10050    | 1,000.00                             |                                       | 1,000.00 | USA dollar      |
| CCRN-10050 | Kreeditarve      | 6/28/2020 | CR-10050 |                                      | 100.00                                | -100,00  | USA dollar      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Kreeditarve tasakaalustamine arvega
Arnie avab lehel **Kliendi kanded** lehe **Kannete tasakaalustamine**. Arnie saab kasutada lehte **Kannete tasakaalustamine** arve ja kreeditarve tasakaalustamiseks. Tasakaalustusprotsessi osana näeb Arnie sularahakonto kuupäevi ja summasid. Arnie märgib kaks dokumenti ja klõpsab seejärel kannete tasakaalustamiseks käsku **Sisesta**. Kreeditarvel on allahindlus –1,00, kuna Fabrikam lubab kreeditarvete puhul allahindlusi.

| Märge     | Kasuta skontot | Kanne    | Konto | Kuupäev      | Tähtaeg  | Arve  | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | FTI‑10050  | 4035    | 6/28/2020 | 7/28/2020 | 10050    | 1,000.00                       | USA dollar      | 990.00           |
| Valitud | Tavaline            | CCRN-10050 | 4035    | 6/28/2020 | 7/28/2020 | CR-10050 | -100,00                        | USA dollar      | –99,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas.

- **Skonto kuupäev**: 12.07.2020 
- **Skonto summa**: –1,00     
- **Kasuta skontot**: Tavaline    
- **Võetud skonto**: 0,00      
- **Skonto summa võtmiseks**: –1,00     

Tasakaalustus on 100,00 ning sisaldab makset summas 99,00 ja allahindlust summas 1,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
