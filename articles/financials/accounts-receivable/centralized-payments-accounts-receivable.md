---
title: "Müügireskontro tsentraliseeritud maksed"
description: "Organisatsioonid, mis sisaldavad mitut juriidilist isikut, saavad luua ja hallata makseid, kasutades ühte kõigi maksetega tegelevat juriidilist isikut. Seetõttu pole vaja sisestada sama kannet mitmesse juriidilisse isikusse. Selles artiklis tuuakse näiteid, mis näitavad, kuidas tsentraliseeritud maksete sisestamist erinevates stsenaariumides käsitletakse."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6327d9cab1651d22cd411f718f6e3a2f8733e13e
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="centralized-payments-for-accounts-receivable"></a>Müügireskontro tsentraliseeritud maksed

[!include[banner](../includes/banner.md)]


Organisatsioonid, mis sisaldavad mitut juriidilist isikut, saavad luua ja hallata makseid, kasutades ühte kõigi maksetega tegelevat juriidilist isikut. Seetõttu pole vaja sisestada sama kannet mitmesse juriidilisse isikusse. Selles artiklis tuuakse näiteid, mis näitavad, kuidas tsentraliseeritud maksete sisestamist erinevates stsenaariumides käsitletakse.

Organisatsioonid, mis sisaldavad mitut juriidilist isikut, saavad luua ja hallata makseid, kasutades kõigi maksetega tegelevat juriidilist isikut. Seetõttu pole vaja sisestada sama kannet mitmesse juriidilisse isikusse. Lisaks säästab organisatsioon aega, kuna maksesoovituste, tasakaalustuste ja avatud ja suletud kannete redigeerimise protsessid on tsentraliseeritud maksete puhul sujuvamad. 

Tsentraliseeritud maksete organisatsioonis on toimingute jaoks palju juriidilisi isikuid ja iga tegutsev juriidiline isik haldab oma müügireskontro teavet. Maksed kõigi tegutsevate juriidiliste isikute jaoks luuakse ühest juriidilisest isikust, mida nimetatakse makse juriidiliseks isikuks. Tasakaalustusprotsessi ajal luuakse rakendatavad millest milleni kanded. Saate määrata, milline juriidiline isik organisatsioonis võtab vastu realiseeritud kasumi või realiseeritud kahjumi kanded ning kuidas käsitsetakse tsentraliseeritud maksetega seotud allahindluskandeid. 

Järgmised näited illustreerivad sisestamise käsitlust erisugustes stsenaariumides. Kõigi nende näidete puhul eeldatakse järgmist konfiguratsiooni.

-   Juriidilised isikud on Fabrikam, Fabrikam East ja Fabrikam West. Kliendi maksed sisestatakse Fabrikami.
-   Välja **Sularaha allahindluse sisestamine** väärtuseks lehel **Kontserni raamatupidamine** määratakse **Arve juriidiline isik**.
-   Välja **Sisesta valuutavahetusega seotud kasum või kahjum** väärtuseks lehel **Kontserni raamatupidamine** määratakse **Makse juriidiline isik**.
-   Klient Northwind Traders on seadistatud kliendiks igas juriidilises isikus. Kliendid erinevatest juriidilistest isikutest on tuvastatud sama kliendina, kuna neil on ühine globaalse aadressiraamatu ID.

| Aadressiraamatu ID | Kliendi konto | Nimi              | Juriidiline isik  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Ida Fabrikam |
| 4050            | 10000            | Northwind Traders | Lääne Fabrikam |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Näide 1: teise juriidilise isiku arve kliendimakse
Fabrikam võtab Fabrikami kliendi kontole 4000, Northwind Tradersile vastu makse 600,00 ühikut. Makse tasakaalustatakse avatud arvega kliendi kontole 4000 Ida Fabrikamis.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Arve sisestamine Ida Fabrikamis kliendile 4000

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Müügireskontro (Ida Fabrikam) | 600,00       |               |
| Müük (Ida Fabrikam)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Makse saadakse ja sisestatakse Fabrikami all kliendile 4000

| Konto                        | Deebetsumma | Kreeditsumma |
|--------------------------------|--------------|---------------|
| Sularaha (Fabrikam)                | 600,00       |               |
| Müügireskontro (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikami makse tasakaalustatakse Ida Fabrikami arvega

**Fabrikami sisestus**

| Konto                         | Deebetsumma | Kreeditsumma |
|---------------------------------|--------------|---------------|
| Müügireskontro (Fabrikam)  | 600,00       |               |
| Võlg Ida Fabrikamile (Fabrikam) |              | 600,00        |

**Ida Fabrikami sisestus**

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Võlg Fabrikamilt (Ida Fabrikam)   | 600,00       |               |
| Müügireskontro (Ida Fabrikam) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Näide 2: arve kliendimakse teisest juriidilisest isikust skontoga
Fabrikam võtab Fabrikami kliendi kontole 4000, Northwind Tradersile vastu makse 580,00 ühikut. Fabrikam Eastil on avatud arve kliendile 4000. Arvele on saadaval skonto 20,00 ühikut. Makse tasakaalustatakse avatud Ida Fabrikami arvetega. Skonto sisestatakse arve juriidilisele isikule, kelleks on Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Arve sisestatakse Ida Fabrikami all Ida Fabrikami kliendile 4000

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Müügireskontro (Ida Fabrikam) | 600,00       |               |
| Müük (Ida Fabrikam)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Makse saadakse ja sisestatakse Fabrikami all Fabrikami kliendile 4000

| Konto                        | Deebetsumma | Kreeditsumma |
|--------------------------------|--------------|---------------|
| Sularaha (Fabrikam)                | 600,00       |               |
| Müügireskontro (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikami makse tasakaalustatakse Ida Fabrikami arvega

**Fabrikami sisestus**

| Konto                         | Deebetsumma | Kreeditsumma |
|---------------------------------|--------------|---------------|
| Müügireskontro (Fabrikam)  | 580,00       |               |
| Võlg Ida Fabrikamile (Fabrikam) |              | 580,00        |

**Ida Fabrikami sisestus**

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Võlg Fabrikamilt (Ida Fabrikam)   | 580,00       |               |
| Müügireskontro (Ida Fabrikam) |              | 580,00        |
| Skonto (Ida Fabrikam)       | 20,00        |               |
| Müügireskontro (Ida Fabrikam) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Näide 3: arve kliendimakse teisest juriidilisest isikust realiseeritud vahetuskursi kasumiga
Fabrikam võtab Fabrikami kliendi kontole 4000, Northwind Tradersile vastu makse 600.00 eurot (EUR). Makse tasakaalustatakse avatud arvega kliendile 4000 Ida Fabrikamis. Tasakaalustusprotsessi käigus luuakse vahetuskursi kasumi kanne.

-   Vahetuskurss eurodest USA dollariteks (USD) arve kuupäeva järgi: 1,2062
-   Vahetuskurss eurodest USA dollariteks vastavalt makse kuupäevale: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Arve sisestatakse Ida Fabrikami all Ida Fabrikami kliendile 4000

| Konto                             | Deebetsumma            | Kreeditsumma           |
|-------------------------------------|-------------------------|-------------------------|
| Müügireskontro (Ida Fabrikam) | 600,00 EUR / 723,72 USD |                         |
| Müük (Ida Fabrikam)               |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Makse saadakse ja sisestatakse Fabrikami all Fabrikami kliendile 4000

| Konto                        | Deebetsumma            | Kreeditsumma           |
|--------------------------------|-------------------------|-------------------------|
| Sularaha (Fabrikam)                | 600,00 EUR / 736,62 USD |                         |
| Müügireskontro (Fabrikam) |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikami makse tasakaalustatakse Ida Fabrikami arvega

**Fabrikami sisestus**

| Konto                         | Deebetsumma            | Kreeditsumma           |
|---------------------------------|-------------------------|-------------------------|
| Müügireskontro (Fabrikam)  | 600,00 EUR / 736,62 USD |                         |
| Võlg Ida Fabrikamile (Fabrikam) |                         | 600,00 EUR / 736,62 USD |
| Võlg Ida Fabrikamile (Fabrikam) | 0,00 EUR / 12,90 USD    |                         |
| Realiseeritud kasum (Fabrikam)        |                         | 0,00 EUR / 12,90 USD    |

**Ida Fabrikami sisestus**

| Konto                             | Deebetsumma            | Kreeditsumma           |
|-------------------------------------|-------------------------|-------------------------|
| Võlg Fabrikamilt (Ida Fabrikam)   | 600,00 EUR / 736,62 USD |                         |
| Müügireskontro (Ida Fabrikam) |                         | 600,00 EUR / 736,62 USD |
| Müügireskontro (Ida Fabrikam) | 0,00 EUR / 12,90 USD    |                         |
| Võlg Fabrikamilt (Ida Fabrikam)   |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Näide 4: kliendi arve makse teisest juriidilisest isikust skonto ja realiseeritud vahetuskursi kasumiga
Fabrikam sisestab makse Fabrikami kliendile 4000, Northwind Traders, avatud arve jaoks Ida Fabrikamis. Arvel on saadaval skonto ja luuakse käibemaksukanne. Makse tasakaalustatakse Ida Fabrikami avatud arvega. Tasakaalustusprotsessi käigus luuakse vahetuskursi kasumi kanne. Skonto sisestatakse arve juriidilisele isikule (Fabrikam East) ja valuutavahetuse kasum sisestatakse makse juriidilisele isikule (Fabrikam).

-   Vahetuskurss eurodest USA dollariteks vastavalt arve kuupäevale: 1,2062
-   Vahetuskurss eurodest USA dollariteks vastavalt makse kuupäevale: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Vabas vormis arve sisestamine ja maksukande loomine Ida Fabrikamis kliendile 4000

| Konto                             | Deebetsumma            | Kreeditsumma           |
|-------------------------------------|-------------------------|-------------------------|
| Müügireskontro (Ida Fabrikam) | 638,22 EUR / 769,82 USD |                         |
| Müük (Ida Fabrikam)               |                         | 600,00 EUR / 723,72 USD |
| Käibemaks (Ida Fabrikam)           |                         | 38,22 EUR / 46,10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Makse saadakse ja sisestatakse Fabrikami all kliendile 4000

| Konto                        | Deebetsumma            | Kreeditsumma           |
|--------------------------------|-------------------------|-------------------------|
| Sularaha (Fabrikam)                | 626,22 EUR / 768,81 USD |                         |
| Müügireskontro (Fabrikam) |                         | 626,22 EUR / 768,81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikami makse tasakaalustatakse Ida Fabrikami arvega

**Fabrikami sisestus**

| Konto                         | Deebetsumma            | Kreeditsumma           |
|---------------------------------|-------------------------|-------------------------|
| Müügireskontro (Fabrikam)  | 626,22 EUR / 768,81 USD |                         |
| Võlg Ida Fabrikamile (Fabrikam) |                         | 626,22 EUR / 768,81 USD |
| Võlg Ida Fabrikamile (Fabrikam) | 0,00 EUR / 13,46 USD    |                         |
| Realiseeritud kasum (Fabrikam)        |                         | 0,00 EUR / 13,46 USD    |

**Ida Fabrikami sisestus**

| Konto                             | Deebetsumma            | Kreeditsumma           |
|-------------------------------------|-------------------------|-------------------------|
| Võlg Fabrikamilt (Ida Fabrikam)   | 626,22 EUR / 768,81 USD |                         |
| Müügireskontro (Ida Fabrikam) |                         | 626,22 EUR / 768,81 USD |
| Müügireskontro (Ida Fabrikam)  | 0,00 EUR / 13,46 USD    |                         |
| Võlg Fabrikamilt (Ida Fabrikam)   |                         | 0,00 EUR / 13,46 USD    |
| Skonto (Ida Fabrikam)       | 12,00 EUR / 14,47 USD   |                         |
| Müügireskontro (Ida Fabrikam) |                         | 12,00 EUR / 14,47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Näide 5: kliendi kreeditarve koos esmase maksega
Fabrikam võtab kliendile 4000, Northwind Traders, vastu makse 75,00 ühikut. Makse tasakaalustatakse avatud arvega Lääne Fabrikami kliendile 10000 ja avatud kreeditarvega Ida Fabrikami kliendile 4000. Makse valitakse esmase maksena avatud lehel **Kannete tasakaalustamine**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Arve sisestatakse Lääne Fabrikami all kliendile 10000

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Müügireskontro (Lääne Fabrikam) | 100,00       |               |
| Müük (Lääne Fabrikam)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kreeditarve sisestatakse Ida Fabrikami all kliendile 4000

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Müügitagastused (Ida Fabrikam)       | 25,00        |               |
| Müügireskontro (Ida Fabrikam) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Makse sisestatakse Fabrikami all kliendile 4000

| Konto                        | Deebetsumma | Kreeditsumma |
|--------------------------------|--------------|---------------|
| Sularaha (Fabrikam)                | 75,00        |               |
| Müügireskontro (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikami makse tasakaalustatakse Lääne Fabrikami arvega ja Ida Fabrikami kreeditarvega

**Fabrikami sisestus**

| Konto                           | Deebetsumma | Kreeditsumma |
|-----------------------------------|--------------|---------------|
| Võlg Ida Fabrikamilt (Fabrikam) | 25,00        |               |
| Müügireskontro (Fabrikam)    |              | 25,00         |
| Müügireskontro (Fabrikam)    | 100,00       |               |
| Võlg Lääne Fabrikamile (Fabrikam)   |              | 100,00        |

**Ida Fabrikami sisestus**

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Müügireskontro (Ida Fabrikam) | 25,00        |               |
| Võlg Fabrikamile (Ida Fabrikam)     |              | 25,00         |

**Lääne Fabrikami sisestus**

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Võlg Fabrikamilt (Lääne Fabrikam)   | 100,00       |               |
| Müügireskontro (Lääne Fabrikam) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Näide 6: kliendi kreeditarve ilma esmase makseta
Fabrikam võtab kliendile 4000, Northwind Traders, vastu makse 75,00 ühikut. Makse tasakaalustatakse avatud arvega Lääne Fabrikami kliendile 10000 ja avatud kreeditarvega Ida Fabrikami kliendile 4000. Makset ei valita esmase maksena avatud lehel **Kannete tasakaalustamine**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Arve sisestatakse Lääne Fabrikami all kliendile 10000

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Müügireskontro (Lääne Fabrikam) | 100,00       |               |
| Müük (Lääne Fabrikam)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kreeditarve sisestatakse Ida Fabrikami all kliendile 4000

| Konto                             | Deebetsumma | Kreeditsumma |
|-------------------------------------|--------------|---------------|
| Müügitagastused (Ida Fabrikam)       | 25,00        |               |
| Müügireskontro (Ida Fabrikam) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Makse sisestatakse Fabrikami all kliendile 4000

| Konto                        | Deebetsumma | Kreeditsumma |
|--------------------------------|--------------|---------------|
| Sularaha (Fabrikam)                | 75,00        |               |
| Müügireskontro (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikami makse tasakaalustatakse Lääne Fabrikami arvega ja Ida Fabrikami kreeditarvega

**Fabrikami sisestus**

| Konto                         | Deebetsumma | Kreeditsumma |
|---------------------------------|--------------|---------------|
| Müügireskontro (Fabrikam)  | 75,00        |               |
| Võlg Lääne Fabrikamile (Fabrikam) |              | 75,00         |

**Ida Fabrikami sisestus**

| Konto                              | Deebetsumma | Kreeditsumma |
|--------------------------------------|--------------|---------------|
| Müügireskontro (Ida Fabrikam)  | 25,00        |               |
| Võlg Lääne Fabrikamile (Ida Fabrikam) |              | 25,00         |

**Lääne Fabrikami sisestus**

| Konto                                | Deebetsumma | Kreeditsumma |
|----------------------------------------|--------------|---------------|
| Võlg Fabrikamilt (Lääne Fabrikam)      | 75,00        |               |
| Müügireskontro (Lääne Fabrikam)    |              | 75,00         |
| Võlg Ida Fabrikamilt (Lääne Fabrikam) | 25,00        |               |
| Müügireskontro (Lääne Fabrikam)    |              | 25,00         |






