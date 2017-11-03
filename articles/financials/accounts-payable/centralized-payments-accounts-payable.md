---
title: Ostureskontro tsentraliseeritud maksed
description: "Organisatsioonid, mis sisaldavad mitut juriidilist isikut, saavad luua ja hallata makseid, kasutades ühte kõigi maksetega tegelevat juriidilist isikut. Seetõttu pole vaja sisestada samu makseid mitmesse juriidilisse isikusse, Selles artiklis tuuakse näiteid, mis näitavad, kuidas tsentraliseeritud maksete sisestamist erinevates stsenaariumides käsitletakse."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 49d5242168cd43e78dd4b0c63da363f91f680904
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="centralized-payments-for-accounts-payable"></a>Ostureskontro tsentraliseeritud maksed

[!include[banner](../includes/banner.md)]


Organisatsioonid, mis sisaldavad mitut juriidilist isikut, saavad luua ja hallata makseid, kasutades ühte kõigi maksetega tegelevat juriidilist isikut. Seetõttu pole vaja sisestada samu makseid mitmesse juriidilisse isikusse, Selles artiklis tuuakse näiteid, mis näitavad, kuidas tsentraliseeritud maksete sisestamist erinevates stsenaariumides käsitletakse.

Organisatsioonid, mis sisaldavad mitut juriidilist isikut, saavad luua ja hallata makseid, kasutades kõigi maksetega tegelevat juriidilist isikut. Seetõttu pole vaja sisestada samu makseid mitmesse juriidilisse isikusse, Peale selle säästab organisatsioon aega, kuna makseprotsess on sujuv.

Tsentraliseeritud maksete organisatsioonis on toimingute jaoks palju juriidilisi isikuid ja iga tegutsev juriidiline isik haldab oma hankijaarveid. Maksed kõigi juriidiliste isikute jaoks luuakse ühest juriidilisest isikust, mida nimetatakse makse juriidiliseks isikuks. Tasakaalustusprotsessi ajal luuakse rakendatavad millest milleni kanded. Saate määrata, milline juriidiline isik organisatsioonis võtab vastu realiseeritud kasumi või realiseeritud kahjumi kanded ning kuidas käsitsetakse ettevõtetevaheliste maksetega seotud allahindluskandeid. 

Järgmised näited illustreerivad sisestamise käsitlust erisugustes stsenaariumides. Kõigi nende näidete puhul eeldatakse järgmist konfiguratsiooni.

-   Juriidilised isikud on Fabrikam, Fabrikam East ja Fabrikam West. Maksed on tehtud Fabrikamist.
-   Välja **Sularaha allahindluse sisestamine** väärtuseks lehel **Kontserni raamatupidamine** määratakse **Arve juriidiline isik**.
-   Välja **Sisesta valuutavahetusega seotud kasum või kahjum** väärtuseks lehel **Kontserni raamatupidamine** määratakse **Makse juriidiline isik**.
-   Hankija Fourth Coffee on seadistatud iga juriidilise isiku hankijana. Hankijad erinevatest juriidilistest isikutest on tuvastatud sama hankijana, kuna neil on ühine globaalse aadressiraamatu ID.

| Kausta ID | Hankija konto | Nimi          | Juriidiline isik  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Ida Fabrikam |
| 1050         | 3004           | Fourth Coffee | Lääne Fabrikam |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Näide 1: teise juriidilise isiku hankija makse arve
Fabrikam Eastil on avatud arve hankija kontole 100, Fourth Coffee. Fabrikam määrab ja sisestab makse Fabrikami hankija kontole 3004, Fourth Coffee. Makse tasakaalustatakse avatud arvega.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Arve sisestatakse Fabrikam Easti hankijale 100

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Kulu (Ida Fabrikam)          | 600,00       |               |
| Ostureskontro (Ida Fabrikam) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Fabrikamis luuakse ja sisestatakse makse tarnijale 3004

| Konto                     | Deebetsumma | Kreeditsumma |
|-----------------------------|--------------|---------------|
| Ostureskontro (Fabrikam) | 600,00       |               |
| Sularaha (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikami makse tasakaalustatakse Ida Fabrikami arvega

**Fabrikami sisestus**

| Konto                           | Deebetsumma | Kreeditsumma |
|-----------------------------------|--------------|---------------|
| Võlg Ida Fabrikamilt (Fabrikam) | 600,00       |               |
| Ostureskontro (Fabrikam)       |              | 600,00        |

**Ida Fabrikami sisestus**

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Ostureskontro (Ida Fabrikam) | 600,00       |               |
| Võlg Fabrikamile (Ida Fabrikam)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Näide 2: teise juriidilise isiku arve hankijamakse skontoga
Fabrikam Eastil on avatud arve hankijale 100, Fourth Coffee. Arvel on 20,00 sularaha allahindluse võimalus. Fabrikam määrab ja sisestab 580,00 suuruse makse Fabrikami hankijale 3004, Fourth Coffee. Makse tasakaalustatakse avatud Ida Fabrikami arvetega. Skonto sisestatakse arve juriidilisele isikule, kelleks on Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Arve on sisestatud Ida Fabrikamis Ida Fabrikami tarnijale 100

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Kulu (Ida Fabrikam)          | 600,00       |               |
| Ostureskontro (Ida Fabrikam) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Makse luuakse ja sisestatakse Fabrikamis Fabrikami tarnijale 3004

| Konto                     | Deebetsumma | Kreeditsumma |
|-----------------------------|--------------|---------------|
| Ostureskontro (Fabrikam) | 580,00       |               |
| Sularaha (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikami makse tasakaalustatakse Ida Fabrikami arvega

**Fabrikami sisestus**

| Konto                           | Deebetsumma | Kreeditsumma |
|-----------------------------------|--------------|---------------|
| Võlg Ida Fabrikamilt (Fabrikam) | 580,00       |               |
| Ostureskontro (Fabrikam)       |              | 580,00        |

**Ida Fabrikami sisestus**

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Ostureskontro (Ida Fabrikam) | 580,00       |               |
| Võlg Fabrikamile (Ida Fabrikam)  |              | 580,00        |
| Ostureskontro (Ida Fabrikam) | 20,00        |               |
| Skonto (Ida Fabrikam)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Näide 3: teise juriidilise isiku arve hankijamakse realiseeritud vahetuskursi kahjumiga
Fabrikam Eastil on avatud arve hankijale 100, Fourth Coffee. Fabrikam määrab ja sisestab makse Fabrikami hankijale 3004, Fourth Coffee. See makse tasakaalustatakse Fabrikam Easti avatud maksega. Valuutavahetuse kahjumikanne luuakse tasakaalustusprotsessi ajal.

-   Vahetuskurss eurodest (EUR) USA dollariteks (USD) arve kuupäeva järgi: 1,2062
-   Vahetuskurss eurodest USA dollariteks vastavalt makse kuupäevale: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Arve on sisestatud Ida Fabrikamis Ida Fabrikami tarnijale 100

| Konto                          | Deebetsumma            | Kreeditsumma           |
|----------------------------------|-------------------------|-------------------------|
| Kulu (Ida Fabrikam)          | 600,00 EUR / 723,72 USD |                         |
| Ostureskontro (Ida Fabrikam) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Makse luuakse ja sisestatakse Fabrikamis Fabrikami tarnijale 3004

| Konto                     | Deebetsumma            | Kreeditsumma           |
|-----------------------------|-------------------------|-------------------------|
| Ostureskontro (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Sularaha (Fabrikam)             |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikami makse tasakaalustatakse Ida Fabrikami arvega

**Fabrikami sisestus**

| Konto                           | Deebetsumma            | Kreeditsumma           |
|-----------------------------------|-------------------------|-------------------------|
| Võlg Ida Fabrikamilt (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Ostureskontro (Fabrikam)       |                         | 600,00 EUR / 736,62 USD |
| Realiseeritud kahjum (Fabrikam)          | 0,00 EUR / 12,90 USD    |                         |
| Võlg Ida Fabrikamilt (Fabrikam) |                         | 0,00 EUR / 12,90 USD    |

**Ida Fabrikami sisestus**

| Konto                          | Deebetsumma            | Kreeditsumma           |
|----------------------------------|-------------------------|-------------------------|
| Ostureskontro (Ida Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Võlg Fabrikamile (Ida Fabrikam)  |                         | 600,00 EUR / 736,62 USD |
| Võlg Fabrikamile (Ida Fabrikam)  | 0,00 EUR / 12,90 USD    |                         |
| Ostureskontro (Ida Fabrikam) |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Näide 4: teise juriidilise isiku arve hankijamakse skonto ja realiseeritud vahetuskursi kahjumiga
Fabrikam Eastil on avatud arve hankijale 100, Fourth Coffee. Arvel on saadaval skonto ja luuakse käibemaksukanne. Fabrikam sisestab makse Fabrikami hankijale 3004, Fourth Coffee. Makse tasakaalustatakse avatud Fabrikam Easti arvega. Valuutavahetuse kahjumikanne luuakse tasakaalustusprotsessi ajal. Skonto sisestatakse arve juriidilisele isikule (Fabrikam East) ja valuutavahetuse kahjum sisestatakse makse juriidilisele isikule (Fabrikam).

-   Vahetuskurss eurodest USA dollariteks vastavalt arve kuupäevale: 1,2062
-   Vahetuskurss eurodest USA dollariteks vastavalt makse kuupäevale: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Arve sisestatakse ja käibemaksukanne luuakse Fabrikam Eastis hankijale 100

| Konto                          | Deebetsumma            | Kreeditsumma           |
|----------------------------------|-------------------------|-------------------------|
| Kulu (Ida Fabrikam)          | 564,07 EUR / 680,38 USD |                         |
| Käibemaks (Ida Fabrikam)        | 35,93 EUR / 43,34 USD   |                         |
| Ostureskontro (Ida Fabrikam) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Fabrikamis luuakse ja sisestatakse makse tarnijale 3004

| Konto                     | Deebetsumma            | Kreeditsumma           |
|-----------------------------|-------------------------|-------------------------|
| Ostureskontro (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Sularaha (Fabrikam East)        |                         | 588,72 EUR / 722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikami makse tasakaalustatakse Ida Fabrikami arvega

**Fabrikami sisestus**

| Konto                           | Deebetsumma            | Kreeditsumma           |
|-----------------------------------|-------------------------|-------------------------|
| Võlg Ida Fabrikamilt (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Ostureskontro (Fabrikam)       |                         | 588,72 EUR / 722,77 USD |
| Realiseeritud kahjum (Fabrikam)          | 0,00 EUR / 12,66 USD    |                         |
| Võlg Ida Fabrikamilt (Fabrikam) |                         | 0,00 EUR / 12,66 USD    |

**Ida Fabrikami sisestus**

| Konto                          | Deebetsumma            | Kreeditsumma           |
|----------------------------------|-------------------------|-------------------------|
| Ostureskontro (Ida Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Võlg Fabrikamile (Ida Fabrikam)  |                         | 588,72 EUR / 722,77 USD |
| Võlg Fabrikamile (Fabrikam East   | 0,00 EUR / 12,66 USD    |                         |
| Ostureskontro (Ida Fabrikam) |                         | 0,00 EUR / 12,66 USD    |
| Ostureskontro (Ida Fabrikam) | 11,28 EUR / 13,61 USD   |                         |
| Skonto (Ida Fabrikam)    |                         | 11,28 EUR / 13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Näide 5: hankija kreeditarve esmase maksega
Fabrikam loob 75,00 summa suuruse makse hankijale 3004, Fourth Coffee. See makse tasakaalustatakse Fabrikam Westi hankijale 3004 avatud arvega ja avatud kreeditarvega Fabrikam Easti hankijale 100. Makse valitakse esmase maksena avatud lehel **Kannete tasakaalustamine**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Arve sisestatakse Lääne Fabrikami tarnijale 3004

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Kulu (Lääne Fabrikam)          | 100,00       |               |
| Ostureskontro (Lääne Fabrikam) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kreeditarve sisestatakse Ida Fabrikami tarnijale 100

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Ostureskontro (Ida Fabrikam) | 25,00        |               |
| Ostu tagastused (Ida Fabrikam) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Makse sisestatakse Fabrikami tarnijale 3004

| Konto                     | Deebetsumma | Kreeditsumma |
|-----------------------------|--------------|---------------|
| Ostureskontro (Fabrikam) | 75,00        |               |
| Sularaha (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikami makse tasakaalustatakse Lääne Fabrikami arvega ja Ida Fabrikami kreeditarvega

**Fabrikami sisestus**

| Konto                           | Deebetsumma | Kreeditsumma |
|-----------------------------------|--------------|---------------|
| Ostureskontro (Fabrikam)       | 25,00        |               |
| Võlg Ida Fabrikamile (Fabrikam)   |              | 25,00         |
| Võlg Lääne Fabrikamilt (Fabrikam) | 100,00       |               |
| Ostureskontro (Fabrikam)       |              | 100,00        |

**Ida Fabrikami sisestus**

| Konto                           | Deebetsumma | Kreeditsumma |
|-----------------------------------|--------------|---------------|
| Võlg Fabrikamilt (Ida Fabrikam) | 25,00        |               |
| Ostureskontro (Ida Fabrikam)  |              | 25,00         |

**Lääne Fabrikami sisestus**

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Ostureskontro (Lääne Fabrikam) | 100,00       |               |
| Võlg Fabrikamile (Lääne Fabrikam)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Näide 6: hankija kreeditarve esmase makseta
Fabrikam loob 75,00 summa suuruse makse hankijale 3004, Fourth Coffee. See makse tasakaalustatakse Fabrikam Westi hankijale 3004 avatud arvega ja avatud kreeditarvega Fabrikam Easti hankijale 100. Makset ei valita esmase maksena avatud lehel **Kannete tasakaalustamine**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Arve sisestatakse Lääne Fabrikami tarnijale 3004

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Kulu (Lääne Fabrikam)          | 100,00       |               |
| Ostureskontro (Lääne Fabrikam) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kreeditarve sisestatakse Ida Fabrikami tarnijale 100

| Konto                          | Deebetsumma | Kreeditsumma |
|----------------------------------|--------------|---------------|
| Ostureskontro (Ida Fabrikam) | 25,00        |               |
| Ostu tagastused (Ida Fabrikam) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Makse sisestatakse Fabrikami tarnijale 3004

| Konto                     | Deebetsumma | Kreeditsumma |
|-----------------------------|--------------|---------------|
| Ostureskontro (Fabrikam) | 75,00        |               |
| Sularaha (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikami makse tasakaalustatakse Lääne Fabrikami arvega ja Ida Fabrikami kreeditarvega

**Fabrikami sisestus**

| Konto                           | Deebetsumma | Kreeditsumma |
|-----------------------------------|--------------|---------------|
| Võlg Lääne Fabrikamilt (Fabrikam) | 75,00        |               |
| Ostureskontro (Fabrikam)       |              | 75,00         |

**Ida Fabrikami sisestus**

| Konto                                | Deebetsumma | Kreeditsumma |
|----------------------------------------|--------------|---------------|
| Võlg Fabrikam Westilt (Fabrikam East) | 25,00        |               |
| Ostureskontro (Ida Fabrikam)       |              | 25,00         |

**Lääne Fabrikami sisestus**

| Konto                              | Deebetsumma | Kreeditsumma |
|--------------------------------------|--------------|---------------|
| Ostureskontro (Lääne Fabrikam)     | 75,00        |               |
| Võlg Fabrikamile (Lääne Fabrikam)      |              | 75,00         |
| Ostureskontro (Lääne Fabrikam)     | 25,00        |               |
| Võlg Fabrikam Eastilt (Fabrikam West) |              | 25,00         |






