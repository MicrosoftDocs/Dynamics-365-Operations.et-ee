---
title: Topeltaruandlus
description: See teema juhendab teid läbi näite, mis näitab, kuidas saate täita nii rahvusvahelise finantsaruandluse standardi (IFRS) aruandlust kui ka vara rentimise kohustuslikku aruandlust.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229546"
---
# <a name="dual-reporting"></a>Topeltaruandlus

[!include [banner](../includes/banner.md)]

See teema juhendab teid läbi näite, mis näitab, kuidas saate täita nii rahvusvahelise finantsaruandluse standardi (IFRS) aruandlust kui ka vara rentimise kohustuslikku aruandlust. Nõutav on rakenduses Microsoft Dynamics 365 Finance kihtide sisestamise kogemus ja see muudab näitest arusaamise lihtsamaks.

## <a name="example"></a>Näide

Järgmine näide kehtib rentimisele Itaalia seadusliku aruande korral, kasutades nii sularahapõhist meetodit kui ka IFRS-i aruandluse meetodeid. Ettevõte peab looma kolm raamatut, et täita nii Itaalia seadusjärgsed nõuded kui ka IFRS 16 nõuded. Üks raamat on vajalik IFRS 16 jaoks, üks raamat on nõutav kohustuslike nõuete jaoks ja üks raamat on nõutav seaduslike postituste automaatne tagasipööramine. Raamatud häälestatakse, nagu järgmistes tabelites on näidatud.

**IFRS 16 raamat**

IFRS 16 raamat on häälestatud nii, et see vastab IFRS 16 raamatupidamise standardile. Kõik sellesse raamatusse sisestatavad kirjed postitatakse kliendi kihis.

| Nimi                                    | Kirjeldus    |
|-----------------------------------------|----------------|
| Žurnaali tüüp                               | IFRS 16        |
| Raamatu kirjeldus                        | IFRS 16        |
| Sisestamiskiht                           | Kohandatud kiht 1 |
| Rendi tüüp                              | Finance        |
| Raamatupidamisraamistik                    | IFRS 16        |
| Rendiperioodi / kasuliku tööea häälestus         | 0,00           |
| Praeguse väärtuse / vara õiglase väärtuse häälestamine | 0,00           |
| Lühiajaline künnis                    | 12             |
| Väikese väärtuse künnis                     | 5,000.00       |
| Hankijale tasumine                           | Ei             |

**Kohustuslik raamat**

Kohustuslik raamat on sularahal põhinev raamat, kus ettevõte arvestab rendikogemust kui sularaha summat, mis makstakse iga kuu rendiks. See raamat ei tekita õiget kasutamisõiguse esemeks olevat vara või rendikohustist.

| Nimi                                    | Kirjeldus |
|-----------------------------------------|-------------|
| Žurnaali tüüp                               | Seaduslik   |
| Raamatu kirjeldus                        | Kohalik GAAP  |
| Sisestamiskiht                           | Praegune     |
| Rendi tüüp                              | Automaatne   |
| Raamatupidamisraamistik                    | Kassapõhine  |
| Rendiperioodi / kasuliku tööea häälestus         | 0,00        |
| Praeguse väärtuse / vara õiglase väärtuse häälestamine | 0,00        |
| Lühiajaline künnis                    | 0           |
| Väikese väärtuse künnis                     | 0           |
| Hankijale tasumine                           | Ei          |

**Kohustusliku tagasivõtmise raamat**

Kohustuslik tagasivõtmise raamat häälestatakse sarnaselt kohustuslikule raamatule.

| Nimi                                    | Kirjeldus                    |
|-----------------------------------------|--------------------------------|
| Žurnaali tüüp                               | Kohustuslik – tagasivõtmime           |
| Raamatu kirjeldus                        | Kohustustusliku raamatu tagasivõtmise raamat |
| Sisestamiskiht                           | Kohandatud kiht 1                 |
| Rendi tüüp                              | Automaatne                      |
| Raamatupidamisraamistik                    | Kassapõhine                     |
| Rendiperioodi / kasuliku tööea häälestus         | 0,00                           |
| Praeguse väärtuse / vara õiglase väärtuse häälestamine | 0,00                           |
| Lühiajaline künnis                    | 0                              |
| Väikese väärtuse künnis                     | 0                              |
| Hankijale tasumine                           | Ei                             |

Selle näite puhul on loodud rendikirje, millel on vahekaartidel **Üldine** ja **Maksegraafiku read** järgmised sätted.

**Vahekaart Üldine**

| Field                      | Väärtus            |
|----------------------------|------------------|
| Alternatiivne laenuintressimäär | 5%               |
| Alguskuupäev          | 1.1.2020         |
| Rendigrupp                | Hooned        |
| Tarnija                     | 1001             |
| Vara õiglane väärtus    | 245,000          |
| Vara kasulik tööiga          | 120              |
| Annuiteedi tüüp               | Harilik annuiteet |
| Liitmisintervall       | Kord kuus          |

**Maksegraafiku ridade vahekaart**

| Field             | Väärtus      |
|-------------------|------------|
| Alguskuupäev        | 1.1.2020   |
| Perioodi intervall   | Kuud     |
| Perioodid           | 24         |
| Lõppkuupäev          | 31.12.2020 |
| Makse sagedus | Kord kuus    |
| Maksesumma    | 1000      |

Selle rendikirje kahe raamistiku põhjal arvestamiseks kasutate praegust sisestamiskihti ja kohandatud sisestamiskihti. Järgmises tabelis on toodud iga töölehe kirje näide, mis on nõutavad rahandusasjade õiglaseks kajastamiseks iga aruandlusstandardi põhjal. Hiljem lisatakse rendiperioodi esimese kuu jaoks iga töölehe kirje üksikasjalik kirjeldus.

<table>
<thead>
<tr>
<th rowspan='3'>Konto number</th>
<th rowspan='3'>Kirjeldus</th>
<th colspan='3'>Kohustuslik raamat (praegune kiht)</th>
<th rowspan='3'>Praeguse kihi kogusumma</th>
<th>Tühistamise raamat (kohandatud kiht)</th>
<th colspan='4'>IFRS 16 raamat (kohandatud kiht)</th>
<th rowspan='3'>Praeguse kihi + kohandatud kiht kokku</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Rendikulu</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>–1000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Pangatasu</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>KM-kulu</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Kliiringukonto</td>
<td>–1000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>–1000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Ostureskontro</td>
<td></td>
<td>–1008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Kasutamisõiguse esemeks olev vara</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Kapitalirendi kohustus</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>–22 794,00</td>
<td>1,000.00</td>
<td>–94,97</td>
<td></td>
<td>–21 888,87</td>
</tr>
<tr>
<td>8</td>
<td>Intressikulu</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Sularaha</td>
<td></td>
<td></td>
<td>–1008,00</td>
<td>–1008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>–1008,00</td>
</tr>
<tr>
<td>10</td>
<td>Kulumi kulu</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Akumuleeritud kulum</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>–949,75</td>
<td>–949,75</td>
</tr>
</tbody>
</table>

Nagu eelnev tabel näitab, tuleb nii kohustusliku aruandluse kui ka IFRS-i aruandluse põhjal esitada kolm raamatut.

- Kohustuslik raamat kirjendab rendimaksed vastavalt sularahapõhise raamatupidamise praeguse kihi reeglitele.
- Kohustuslik tagasivõtmise raamat pöörab kohustuslikud töölehe kanded ümber.
- IFRS 16 raamat loob töölehe kirjed, mida nõutakse IFRS 16 alusel.

Peate sisestama rendi ainult üks kord. Seejärel saate avada lehe **Raamatud**, et näha kõiki üürilepinguga seotud raamatuid.

> [!NOTE]
> Kui loote raamatud, peavad kõik kolm olema seotud sama rendikirjega.

Esimese töölehe kirje talletab kohustuslikku raamatusse rendikogemuse. Makseid saate luua kas partiina või valides kohustuslikus raamatus maksegraafiku.

Käesolevas näites luuakse kohustusliku raamatu jaoks maksegraafikust järgmine töölehe kirje.

### <a name="lease-payment--1312020--je-100"></a>Rendimakse – 31.1.2020 – JE 100

| Konto tüüp | Konto number | Kiht   | Konto kirjeldus | Debiteeri    | Krediit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 1              | Praegune | Rendikulu       | 1,000.00 |          |
| Ledger       | 4              | Praegune | Kliiringukonto    |          | 1,000.00 |

Ostureskontro ametnik kasutab standardset Dynamics 365 funktsiooni, et luua arve rendi eest maksmiseks väljaspool vara rentimist. Kuid selle asemel, et valida deebeti kontona **Rendikulu**, valib ostureskontro ametnik konto, et luua järgmine kirje.

### <a name="ap-process--1312020--je-110"></a>AP protsess – 31.1./2020 – JE 110

| Konto tüüp | Konto number | Kiht   | Konto kirjeldus | Debiteeri    | Krediit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 4              | Praegune | Kliiringukonto    | 1,000.00 |          |
| Ledger       | 2              | Praegune | Pangatasu            | 3.00     |          |
| Ledger       | 3              | Praegune | KM-kulu         | 5.00     |          |
| Tarnija       | 5              | Praegune | Ostureskontro    |          | 1,008.00 |

Kui hankijale edastatakse arve, järgite tavalist maksetoimingut. Selle toimingu käigus luuakse järgmine töölehe kirje.

### <a name="cash-payment--1312020--je-120"></a>Sularahamakse – 31/1/2020 – JE 120

| Konto tüüp | Konto number | Kiht   | Konto kirjeldus | Debiteeri    | Krediit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Tarnija       | 5              | Praegune | Ostureskontro    | 1,008.00 |          |
| Pank         | 9              | Praegune | Sularaha                |          | 1,008.00 |

Selleks hetkeks on teil antud rendikirje kohustusliku aruandlusnõude alusel kõik raamatupidamistoimingud tehtud ja saate luua praegust kihti kasutades proovibilansi. Süsteem tagastab proovibilansi, millel on järgmised arvud.

<table>
<thead>
<tr>
<th rowspan='3'>Konto number</th>
<th rowspan='3'>Kirjeldus</th>
<th colspan='3'>Kohustuslik raamat (praegune kiht)</th>
<th rowspan='3'>Praeguse kihi kogusumma</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Rendikulu</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Pangatasu</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>KM-kulu</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Kliiringukonto</td>
<td>–1000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Ostureskontro</td>
<td></td>
<td>–1008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Kasutamisõiguse esemeks olev vara</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Kapitalirendi kohustus</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Intressikulu</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Sularaha</td>
<td></td>
<td></td>
<td>–1008,00</td>
<td>–1008,00</td>
</tr>
<tr>
<td>10</td>
<td>Kulumi kulu</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Akumuleeritud kulum</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Kui soovite kasutada sama proovibilansi käitamiseks kasutada IFRS 16 andmeid, tuleb kohustusliku raamatupidamise töölehe kanded tagasi võtta ja IFRS 16 töölehe kanded tuleb sisestada. Kohustusliku töölehe kirjete tühistamiseks sisaldab see näide seadusjärgset tagasivõtmise raamatut, millel on sama seadistus kui kohustuslik raamat, kuid vastupidine sisestusreegel. Näiteks, kohustuslik raamat *debiteerib* rendikulu kontot, kuid tagasivõtmise konto *krediteerib* seda kontot. Need seosed on lihtne määratleda vara rentimise sisestamise kontol lehel **Vara rentimise parameetrid**(**Vara rentimine \> Seadistus \> Vara rentimise parameetrid**).

Kui tagasivõtmise raamatu puhul kasutataks kohustusliku raamatuga sama protsessi, loodaks järgmine töölehe kirje. Erinevus seisneb selles, et tagasivõtmise raamat kirjendab kohustusliku raamatu tagastamise kirjed. Tagasivõtmise kirjed tehakse ka kliendi kihis. Kui proovibilanssi käitatakse praeguses kihis, siis tagasivõtmise töölehe kirjeid ei kaasataks.

### <a name="lease-payment--1312020--je-130"></a>Rendimakse – 31.1.2020 – JE 130

| Konto tüüp | Konto number | Kiht  | Konto kirjeldus | Debiteeri    | Krediit   |
|--------------|----------------|--------|---------------------|----------|----------|
| Ledger       | 4              | Kohandatud | Kliiringukonto    | 1,000.00 |          |
| Ledger       | 1              | Kohandatud | Rendikulu       |          | 1,000.00 |

Nüüd kui olete kohustusliku töölehe sisestused eemaldanud, kirjendate kõik töölehe kirjed, mida IFRS 16 nõuab, IFRS 16 raamatus. Need kanded hõlmavad kasutamisõiguse esemeks oleva vara esialgset tunnustamist ning intressikirjet ja kulumi arvestust.

### <a name="initial-recognition--112020--je-140"></a>Esialgne tunnustamine – 1.1.2020 – JE 140

| Konto tüüp | Konto number | Kiht  | Konto kirjeldus      | Debiteeri     | Krediit    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Ledger       | 6              | Kohandatud | Kasutamisõiguse esemeks olev vara                | 22,793.90 |           |
| Ledger       | 7              | Kohandatud | Kapitalirendi kohustus |           | 22,793.90 |

Rendimakse sisestatakse sarnaselt teistele rendimaksetele. Tühjendamise konto kasutamise põhjus on tagada, et sularaha krediteeritakse ainult üks kord.

### <a name="lease-payment--1312020--je-150"></a>Rendimakse – 31.1.2020 – JE 150

| Konto tüüp | Konto number | Kiht  | Konto kirjeldus      | Debiteeri    | Krediit   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Ledger       | 7              | Kohandatud | Kapitalirendi kohustus | 1,000.00 |          |
| Ledger       | 4              | Kohandatud | Kliiringukonto         |          | 1,000.00 |

Intressikulu töölehe kirje luuakse kohustise amortiseerimise graafikust.

### <a name="interest-expense--1312020--je-160"></a>Intressikulu – 31.1.2020 – JE 160

| Konto tüüp | Konto number | Kiht  | Konto kirjeldus      | Debiteeri | Krediit |
|--------------|----------------|--------|--------------------------|-------|--------|
| Ledger       | 8              | Kohandatud | Intressikulu         | 94.97 |        |
| Ledger       | 7              | Kohandatud | Kapitalirendi kohustus |       | 94.97  |

Kulumi kulu töölehe kirje luuakse vara kulumi graafikust.

### <a name="depreciation-expense--1312020--je-170"></a>Kulumi kulu – 31.1.2020 – JE 170

| Konto tüüp | Konto number | Kiht  | Konto kirjeldus      | Debiteeri  | Krediit |
|--------------|----------------|--------|--------------------------|--------|--------|
| Ledger       | 10             | Kohandatud | Kulumi kulu     | 949.75 |        |
| Ledger       | 11             | Kohandatud | Akumuleeritud kulum |        | 949.75 |

Pärast kõikide nende töölehe kirjete loomist ja sisestamist näete järgmist „kohandatud kiht 1” väärtuseid. Pange tähele, et viimane veerg sisaldab pangatasu, käibemaksu (KM) kulu ja eelmise kihi sularaha vähendamist, kuid see ei sisalda kohustusliku aruandluse töölehe kandeid. Seega saavutate tõelise topeltaruandluse võimalused. Sel hetkel peab ettevõte lihtsalt käivitama oma proovibilansi ja kombineerima praeguse kihi ja kohandatud kihi, et luua IFRS-i prooviversioon.

| Konto nr | Kirjeldus              | Kohustuslik raamat\-Praegune tase\-JE\-100\-Dr \(Cr\) | Kohustuslik raamat\-Praegune tase\-JE\-110\-Dr \(Cr\) | Kohustuslik raamat\-Praegune tase\-JE\-120\-Dr \(Cr\) | Praegune kiht \- kogusummad | - | Tühistamise raamat\-Kohandatud kiht\-JE\-130\-Dr \(Cr\) | IFRS 16 raamat\-kohandatud kiht \-JE\-140\-Dr \(Cr\) | IFRS 16 raamat\-kohandatud kiht \-JE\-150\-Dr \(Cr\) | IFRS 16 raamat\-kohandatud kiht \-JE\-160\-Dr \(Cr\) | IFRS 16 raamat\-kohandatud kiht \-JE\-170\-Dr \(Cr\) | Kohandatud kiht \+ Praegune kiht \- Tööriistad |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Rendikulu            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Pangatasu                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | KM-kulu              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Kliiringukonto         | \-1000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1000                                           |                                                | \-1000                                        |                                                |                                                | 0\.00                                   |
| 5          | Ostureskontro         |                                                   | \-1008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | Kasutamisõiguse esemeks olev vara                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Kapitalirendi kohustus |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22 794                                       | 1000                                          | \-94\.97                                       |                                                | \-21 888\.87                            |
| 8          | Intressikulu         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Sularaha                     |                                                   |                                                   | \-1008\.00                                       | \-1008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1008\.00                             |
| 10         | Kulumi kulu     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Akumuleeritud kulum |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]