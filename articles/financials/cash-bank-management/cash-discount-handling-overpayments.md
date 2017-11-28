---
title: "Skonto töötlemine ülemaksete korral"
description: "Selles artiklis on stsenaariumid, mis nöitavad, kuidas makset käsitletakse, kui klient võtab skonto, kuid maksab üle."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b664ad6d084c5437111149266a859d7157b22ee9
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="handling-cash-discounts-for-overpayments"></a>Skonto töötlemine ülemaksete korral

[!include[banner](../includes/banner.md)]


Selles artiklis on stsenaariumid, mis nöitavad, kuidas makset käsitletakse, kui klient võtab skonto, kuid maksab üle. 

Arve loetakse ülemakstuks, kui maksesumma on suurem kui arve summa, millest on maha arvestatud skonto. Määramaks, kuidas saadavat skonto erinevust ülemaksete korral käsitletakse, kasutage välju **Skonto haldamine** ja **Suurim üle- või alamakse** lehel **Müügireskontro parameetrid**. Järgmises näites on klient arve üle maksnud 0,50 võrra.

| Arve summa | Saadaolev skonto | Makstav summa, mis hõlmab skontot | Kliendi tegelikult makstav summa |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Skonto haldamine = spetsiifiline
Kui lehe **Automaatsete kannete kontod** väljal **Skonto haldamine** valitakse suvand **Spetsiifiline**, vetakse täielik skonto. Ülemakse summa sisestatakse skonto erinevuse pearaamatukontole või jäetakse saldona kliendi kontole. Käitumine oleneb sellest, kas ülemakse summa on 0,00 ja väljale**Suurim üle- või alamakse** sisestatud summa vahel või kas ülemakse summa on suurem kui summa väljal **Suurim üle- või alamakse**.

### <a name="scenario-1"></a>1. stsenaarium

Selles stsenaariumis on ülemakse summa 0,00 ja maksimaalse üle- või alamakse vahemikus. Arve on sisestatud summas 105,00 ja skonto on saadaval, kui arve makstakse seitsme päeva jooksul.

| Arve summa | Saadaolev skonto | Makstav summa, mis hõlmab skontot |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Klient edastab makse 95,00 skontoperioodil. Makse tasakaalustatakse arve alusel, mille summa on 105,00. Kui arve ja makse on tasakaalustatud, luuakse kliendi ostureskontrosse järgmised kanded.

| Kanne   | Summa | Saldo |
|---------------|--------|---------|
| Arve       | 105,00 | 0,00    |
| Makse       | -95,00 | 0,00    |
| Skonto | -10,50 | 0,00    |

Makse ja tasakaalustuse kohta luuakse järgmised raamatupidamiskirjed. **Makse**

| Konto             | Deebetsumma | Kreeditsumma |
|---------------------|--------------|---------------|
| Sularaha                | 95,00        |               |
| Müügireskontro |              | 95,00         |

**Tasakaalustus**

| Konto                                                                                                          | Deebetsumma | Kreeditsumma |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Skonto (väli **Kliendi allahindluste põhikonto** lehel **Skontod**)                 | 10,50        |               |
| Müügireskontro                                                                                              |              | 10,50         |
| Kliendi skonto (väli **Kliendi skonto** lehel **Automaatsete kannete konto**) |              | 0,50          |
| Müügireskontro                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>2. stsenaarium

Selles stsenaariumis on ülemakse summa suurem kui maksimaalne üle- või alamakse. Arve on sisestatud summas 105,00 ja skonto on saadaval, kui arve makstakse seitsme päeva jooksul.

| Arve summa | Saadaolev skonto | Makstav summa, mis hõlmab skontot |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Klient edastab makse 95,00 skontoperioodil. Makse tasakaalustatakse arve alusel, mille summa on 105,00. Kui arve ja makse on tasakaalustatud, luuakse kliendi ostureskontrosse järgmised kanded.

| Kanne   | Summa | Saldo |
|---------------|--------|---------|
| Arve       | 105,00 | 0,00    |
| Makse       | -95,00 | -0,50   |
| Skonto | -10,50 | 0,00    |

Ülemakse summa 0,50 jääb makse avatud saldoks ning selle saab muu arvega tasakaalustada. Makse ja tasakaalustuse kohta luuakse järgmised raamatupidamiskirjed. **Makse**

| Konto             | Deebetsumma | Kreeditsumma |
|---------------------|--------------|---------------|
| Sularaha                | 95,00        |               |
| Müügireskontro |              | 95,00         |

**Tasakaalustus**

| Konto                                                                                          | Deebetsumma | Kreeditsumma |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Skonto (väli **Kliendi allahindluste põhikonto** lehel **Skontod**) | 10,50        |               |
| Müügireskontro                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Skonto haldamine = määramata
Kui lehe **Automaatsete kannete kontod** väljal **Skonto haldamine** valitakse suvand **Määramata**, vähendatakse skonto summat ülemakse summa võrra. Seda kasutatakse alati, olenemata sellest, kas ülemakse summa on suurem või väiksem kui summa, mis on sisestatud väljale **Suurim üle- või alamakse**.

### <a name="scenario-3"></a>3. stsenaarium

Selles stsenaariumis on arve sisestatud summas 105,00 ja skonto on saadaval, kui arve makstakse seitsme päeva jooksul.

| Arve summa | Saadaolev skonto | Makstav summa, mis hõlmab skontot |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Klient edastab makse 95,00 skonto kuupäevaks. Makse tasakaalustatakse arve alusel, mille summa on 105,00. Kui arve ja makse on tasakaalustatud, luuakse kliendi ostureskontrosse järgmised kanded.

| Kanne   | Summa | Saldo |
|---------------|--------|---------|
| Arve       | 105,00 | 0,00    |
| Makse       | -95,00 | -0,00   |
| Skonto | -10,00 | 0,00    |

Skonto summat 10,50 vähendatakse 10,00-ni. Makse ja arve loetakse tasakaalustatuks. **Makse**

| Konto             | Deebetsumma | Kreeditsumma |
|---------------------|--------------|---------------|
| Sularaha                | 95,00        |               |
| Müügireskontro |              | 95,00         |

**Tasakaalustus**

| Konto                                                                                          | Deebetsumma | Kreeditsumma |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Skonto (väli **Kliendi allahindluste põhikonto** lehel **Skontod**) | 10,50        |               |
| Müügireskontro                                                                              |              | 10,50         |






