---
title: Nullväärtusega toote kviitungi jaoks postitatakse ostu kogunemine, mille summa on null
description: Kui sisestatakse nullväärtusega toote kviitung, loob süsteem ostu laekumise jaoks postituse, kus summa on 0 (null).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026455"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Nullväärtusega toote kviitungi jaoks postitatakse ostu kogunemine, mille summa on null

KB number: 4612588

## <a name="symptoms"></a>Sümptomid

Kui sisestatakse nullväärtusega toote kviitung, loob süsteem ostu laekumise jaoks postituse, kus summa on 0 (null).

## <a name="resolution"></a>Eraldusvõime

Vaikimisi on ostu pearaamatu sisestuste *Kviitung, lisanduv* tüüp `IsTransferredIndetail` väljal seatud *Kokkuvõtteks* alammooduli kannetes. Seetõttu loob süsteem seotud kandekirje ka juhul, kui summa on 0 (null).

Kui summa on 0 (null), jäetakse see sisestamistüüp vahele, kui laiendage `subledgerJournalizer.markDoNotTransferEntries` meetodit nii, et see hõlmaks `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, nagu näha järgmises näites.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
