---
title: Üldkulude arvutus
description: Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 98fd0b4a18b02ed58034ec6e22763ed7c66f567f5c9eeeed124996757470c419
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766285"
---
# <a name="overhead-calculation"></a>Üldkulude arvutus

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.

## <a name="term-definition"></a>Mõiste määratlus

Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega. Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele. Siin on mõned näited üldkuludest.

-   Üür
-   Elektrienergia
-   Haldustasud

## <a name="overhead-calculation-overview"></a>Üldkulude arvutuse ülevaade
Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras. Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked. Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda. Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva. See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale. Kordumatu versiooni-ID koosneb järgmistest elementidest.

-   Versiooni tüüp
-   Kuupäev ja kellaaeg
-   Kuluarvestuse pearaamat
-   Finantsaasta
-   Rahandusperiood

Üldkulude arvutus käivitatakse versioonist sõltumatult. Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni. Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel. Igas etapis luuakse töölehe päis, millel on töölehe kanded. See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta. Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed. Seega on teil alati olemas põhjalik ülevaade. 

[![Üldkulude arvutus.](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Elektri üldkulude arvutamine ja eraldamine
Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana. Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet. Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta. See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel. Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.

<table>
<thead>
<tr>
<th>Aruandluskuupäev</th>
<th colspan="2">Kulukeskus</th>
<th colspan="2">Põhikonto</th>
<th>Summa arvestusvaluutas</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. jaanuar 2017</td>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>1. etapp: kulukäitumise arvutuse töötlemine

Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**. Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.

#### <a name="define-the-cost-behavior-rule"></a>Kulukäitumise reegli määratlemine

Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel. Elektriarved vastavad sageli sellele määratlusele. Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta. Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.

-   Fikseeritud summa: 1000,00
    -   0 &lt;= 1000,00 = fikseeritud
    -   1000,01 &lt; N = muutuja

##### <a name="journal"></a>Tööleht

<table>
<thead>
<tr>
<th>Tööleht</th>
<th>Töölehe tüüp</th>
<th colspan="3">Rahanduskalendri periood</th>
<th>Versioon</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Kulukäitumise arvutamise tööleht</td>
<td>Fiskaalne</td>
<td>2017</td>
<td>Periood 1</td>
<td>Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Töölehe sisestused (kuluobjekti saldo töölehe sisestused)

<table>
<thead>
<tr>
<th>Aruandluskuupäev</th>
<th colspan="2">Kuluobjekt</th>
<th colspan="2">Kuluelement</th>
<th>Kulukäitumine</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. jaanuar 2017</td>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Liigitamata</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kulukirjed

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th colspan="2">Kuluelement</th>
<th>Kulukäitumine</th>
<th>Summa</th>
<th>Aruandluskuupäev</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Liigitamata</td>
<td>10,000.00</td>
<td>3. jaanuar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Liigitamata</td>
<td>–10 000,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>1 000,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>9,000.00</td>
<td>31. jaanuar 2017</td>
</tr>
</tbody>
</table>

Lisateavet vt teemast [Kulukäitumise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).
### <a name="step-2-process-the-cost-distribution-calculation"></a>2. etapp: kulujaotuse arvutuse töötlemine

Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust. Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.

#### <a name="define-the-cost-distribution-rule"></a>Kulujaotuse reegli määratlemine

Finantsaruandluses registreeritakse elektrikulud sageli põhisummana. Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik. Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel. Kõige loogilisem eraldamisalus on elektritarbimine (kWh). Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse. Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>kWh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>1000</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>0</td>
</tr>
</tbody>
</table>

Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Väärtus</th>
<th>Eraldamistegur</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>1000</td>
<td>(1000 ÷ 7000) × 9000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>6,000</td>
<td>(6000 ÷ 7000) × 9000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>0</td>
<td>(0 ÷ 7000) × 9000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit. Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Valem</th>
<th>Väärtus</th>
<th>Eraldamistegur</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>(1000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>(6000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Tööleht

<table>
<thead>
<tr>
<th>Tööleht</th>
<th>Töölehe tüüp</th>
<th colspan="3">Rahanduskalendri periood</th>
<th>Versioon</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Kulujaotuse arvutamise tööleht</td>
<td>Fiskaalne</td>
<td>2017</td>
<td>Periood 1</td>
<td>Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Töölehe sisestused (kuluobjekti saldo töölehe sisestused)

<table>
<thead>
<tr>
<th>Aruandluskuupäev</th>
<th colspan="2">Kuluobjekt</th>
<th colspan="2">Kuluelement</th>
<th>Kulukäitumine</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. jaanuar 2017</td>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>1 000,00</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kulukirjed

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th colspan="2">Kuluelement</th>
<th>Kulukäitumine</th>
<th>Summa</th>
<th>Aruandluskuupäev</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>–1000,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>500,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>500,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Vaike-kulukeskus</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>–9000,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>1,285.71</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>7,714.29</td>
<td>31. jaanuar 2017</td>
</tr>
</tbody>
</table>

Lisateavet vt teemast [Kulujaotise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-distribution-policy-cost-control-unit.md). 

### <a name="step-3-process-the-overhead-rate-calculation"></a>3. etapp: üldkulude määra arvutuse töötlemine

Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks. Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest. 

#### <a name="define-the-overhead-rate"></a>Üldkulu määra määratlemine

Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse. Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Tunnid</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj. 1</td>
<td>Projekt 1</td>
<td>3</td>
</tr>
<tr>
<td>Proj. 2</td>
<td>Projekt 2</td>
<td>1</td>
</tr>
</tbody>
</table>

Määratletud on eelmääratud kulumäär kuluprojektide panusele.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Kuluelement</th>
<th>Kulukäitumine</th>
<th>Ühikud</th>
<th>Kurss</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Muutuv kulu</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Väärtus</th>
<th>Kuluelement</th>
<th>Eraldamistegur</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj. 1</td>
<td>Projekt 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30,00</td>
</tr>
<tr>
<td>Proj. 2</td>
<td>Projekt 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Tööleht

<table>
<thead>
<tr>
<th>Tööleht</th>
<th>Töölehe tüüp</th>
<th colspan="3">Rahanduskalendri periood</th>
<th>Versioon</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Üldkulu määra arvutamise tööleht</td>
<td>Fiskaalne</td>
<td>2017</td>
<td>Periood 1</td>
<td>Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)

<table>
<thead>
<tr>
<th>Aruandluskuupäev</th>
<th colspan="2">Kuluobjekt</th>
<th>Väärtus</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. jaanuar 2017</td>
<td>Proj. 1</td>
<td>Sisemine proj. 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>Proj. 2</td>
<td>Sisemine proj. 2</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kulukirjed

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th colspan="2">Kuluelement</th>
<th>Kulukäitumine</th>
<th>Summa</th>
<th>Aruandluskuupäev</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>–30,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Proj. 1</td>
<td>Sisemine proj. 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>30,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>-10,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Proj. 2</td>
<td>Sisemine proj. 2</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>10.00</td>
<td>31. jaanuar 2017</td>
</tr>
</tbody>
</table>

Lisateavet vt teemast [Üldkulude arvutamine](cost-rollup.md#perform-overhead-calculation).

### <a name="step-4-process-the-cost-allocation-calculation"></a>4. etapp: kulueralduse arvutuse töötlemine

Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust. Finance toetab vastastikuse eraldamise meetodit. Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused. Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra. Kuluobjekti saldo eraldatakse üksiku eraldamisalusena. Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas. Eraldamisjärjekorda reguleerib kulujuhtseade. 

[![Vastastikune meetod.](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Kulueraldamise määratlemine

Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist. Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile. Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Inimressursside teenused</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>10</td>
</tr>
</tbody>
</table>

Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile. Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Rahandusteenused</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>35</td>
</tr>
</tbody>
</table>

Kuluobjekt CC003 assembler panustab mitmele kuluobjektile. Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Assembleriteenused (tundides)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>60</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile. Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Pakendamisteenused (tundides)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>80</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>15</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Statistilised mõõdud, nagu toote tarbitud tootmistunnid, saab tuletada lähteandmetest. Lisateavet vt teemast [Statistiliste mõõtude pakkuja mall](statistical-measure-provider-template.md#statistical-measure-provider-template). Järgmises tabelis on näidatud tulemus, kui HR-teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Väärtus</th>
<th>Eraldamistegur</th>
<th>Summa</th>
<th>Kulukäitumine</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>35</td>
<td>(35 ÷ 100) × 1245,71</td>
<td>436.00</td>
<td>Muutuv kulu</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>55</td>
<td>(55 ÷ 100) × 1.245,71</td>
<td>685.14</td>
<td>Muutuv kulu</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>10</td>
<td>(10 ÷ 100) × 1.245,71</td>
<td>124.57</td>
<td>Muutuv kulu</td>
</tr>
</tbody>
</table>

Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Väärtus</th>
<th>Eraldamistegur</th>
<th>Summa</th>
<th>Kulukäitumine</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>65</td>
<td>(65 ÷ 100) × (7714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Muutuv kulu</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>35</td>
<td>(35 ÷ 100) × (7714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Muutuv kulu</td>
</tr>
</tbody>
</table>

Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Väärtus</th>
<th>Eraldamistegur</th>
<th>Summa</th>
<th>Kulukäitumine</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Muutuv kulu</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Muutuv kulu</td>
</tr>
</tbody>
</table>

Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th>Väärtus</th>
<th>Eraldamistegur</th>
<th>Summa</th>
<th>Kulukäitumine</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Fikseeritud kulu</td>
</tr>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Muutuv kulu</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2852,60 + 124,57)</td>
<td>470.08</td>
<td>Muutuv kulu</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Töölehe sisestused (kuluobjekti saldo töölehe sisestused)

<table>
<thead>
<tr>
<th>Tööleht</th>
<th>Töölehe tüüp</th>
<th colspan="3">Rahanduskalendri periood</th>
<th>Versioon</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Kulueralduse tööleht</td>
<td>Fiskaalne</td>
<td>2017</td>
<td>Periood 1</td>
<td>Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Töölehe read

<table>
<thead>
<tr>
<th>Aruandluskuupäev</th>
<th colspan="2">Kuluobjekt</th>
<th colspan="2">Kuluelement</th>
<th>Kulukäitumine</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. jaanuar 2017</td>
<td>CC001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>500,00</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>CC001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>CC002</td>
<td>Finantsid</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>675.00</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>CC002</td>
<td>Finantsid</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>713.75</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>CC003</td>
<td>Pakendamine</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>286.25</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>CC003</td>
<td>Pakendamine</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>776.36</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>Toode 2</td>
<td>Toode 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>223.64</td>
</tr>
<tr>
<td>31. jaanuar 2017</td>
<td>Toode 2</td>
<td>Toode 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kulukirjed

<table>
<thead>
<tr>
<th colspan="2">Kuluobjekt</th>
<th colspan="2">Kuluelement</th>
<th>Kulukäitumine</th>
<th>Summa</th>
<th>Aruandluskuupäev</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>‑500,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>175.00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>275.00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>50,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personaliosakond</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>–1245,71</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>436.00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>685.14</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>124.57</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>–675,00</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>438.75</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>236.25</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finantsid</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>–8150,29</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>5,297.69</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakendamine</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>2,852.60</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>–713,75</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>535.31</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>178.44</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>–5982,83</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>4,487.12</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>1,495.71</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>–286,25</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>241.05</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Fikseeritud kulu</td>
<td>45.20</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Assembler</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>–2977,17</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Tooe 1</td>
<td>Toode 1</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>2,507.09</td>
<td>31. jaanuar 2017</td>
</tr>
<tr>
<td>Toode 2</td>
<td>Toode 2</td>
<td>10001</td>
<td>Elektrienergia</td>
<td>Muutuv kulu</td>
<td>470.08</td>
<td>31. jaanuar 2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Lõppsõna
Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le. Nii teavad kuluarvestajad, et see kulu tuleb eraldada. Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete. Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">Kuluelement</th>
<th colspan="9">Kuluobjekt</th>
<th rowspan="2">Kokku</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>Proj. 1</th>
<th>Proj. 2</th>
<th>Tooe 1</th>
<th>Toode 2</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 Elekter</td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30,00</strong></td>
<td style="text-align: right;"><strong>10,00</strong></td>
<td style="text-align: right;"><strong>7.770,57</strong></td>
<td style="text-align: right;"><strong>2.189,43</strong></td>
<td style="text-align: right;"><strong>10.000,00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">Liigitamata</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Fikseeritud kulu</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1.000,00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Muutuv kulu</td>
<td style="text-align: right;">000</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">30,00</td>
<td style="text-align: right;">10,00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9.000,00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide. Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele. Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid. Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid. Lisateavet vt teemast [Kulukomplekti poliitika ja üldkulude arvutus](cost-rollup.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]