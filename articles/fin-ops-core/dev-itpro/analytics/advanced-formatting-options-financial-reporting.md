---
title: Täpsemad vormingusuvandid finantsaruandluses
description: See artikkel kirjeldab täpsemaid vormindamise funktsioone, sh filtreid, piiranguid, mitteprintimisridasid ja tingimuslauseid arvutustes.
author: panolte
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3ede95ff196abab450a478fef9e024490d22e00f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906664"
---
# <a name="advanced-formatting-options-in-financial-reporting"></a>Täpsemad vormingusuvandid finantsaruandluses

[!include [banner](../includes/banner.md)]

Finantsaruandluses aruannet luues on saadaval täiendavad vormindusfunktsioonid, sealhulgas dimensioonide filtrid, veergude ja aruandlusüksuste piirangud, mitteprinditavad read ja IF-/THEN-/ELSE-laused arvutustes.

Järgmises tabelis selgitatakse täpsemaid vormingufunktsioone, mis on aruannete kujundamisel saadaval.

| Funktsioon                   | Kirjeldus |
|----------------------------|-------------|
| Dimensioonifilter           | Kindlate andmekogumite juurde pääsemiseks saate kasutada readefinitsiooni ja veeru definitsiooni dimensioone. Paljud aruanded kasutavad rea vormingus ainult füüsilist segmenti. Ridu saate siiski nii muuta, et need sisaldaksid dimensiooniväärtusi. Veeru definitsiooni dimensioonifiltreid kasutatakse kindlate dimensiooniväärtuste juurde pääsemiseks. |
| Aruandlusüksuse piirang | Saate seadistada aruande rea nii, et see kuvaks ainult teavet, mis on konkreetse aruandlusüksusega seotud. |
| Mitteprinditavad (NP) read     | Mitteprinditavad read on kasulikud mitmetes aruannetes. Kui väärtuse saamiseks on vaja mitut arvutust, saab neid arvutusi prinditud aruandes peita. Mitteprinditavad read on kasulikud ka aruande kujunduse tõrkeotsinguks ja täpsemaks lahtri paigutuseks. |
| Veeru piirang         | Readefinitsiooni veeru piirang on kasulik väärtuste peitmiseks, mis on asjakohased ainult mõne aruande rea puhul. Rea protsendiarvutuste tegemisel takistab veeru piirang kogusumma veergude või muude veergude printimise, kui need numbrid ei kehti. |
| Veerupiir               | Saate lisada readefinitsiooni veerupiire aruande teabe kõrvuti kuvamiseks. Saate lisada ühte readefinitsiooni mitu veerupiiri ja veerupäised korduvad iga veeru ülaosas pärast veerupiiri. Aruande kommentaarid kuvatakse veerupiiride vahel. |
| Lause IF/THEN/ELSE     | Saate muuta readefinitsiooni või veeru definitsiooni arvutusi. |
| Kasutage ühekordseid jutumärke ('') ning ja-märki (&) dimensiooniväärtuste jaoks | Saate kasutada dimensiooniväärtusi, sh ja-märki ning märki aruande kujunduse jaoks. |

## <a name="advanced-cell-placement"></a>Täpsem lahtri paigutus

Täpsem lahtri paigutus või *sundimine* hõlmab kindlate väärtuste paigutamist kindlatesse lahtritesse. Näiteks kasutatakse sundimist sageli rahavoogude aruande õige saldo teisaldamiseks. Saate kasutada sundimist järgmistel eesmärkidel.

- Väärtuste teisaldamine Microsoft Excelist konkreetsetesse lahtritesse.
- Kindlate väärtuste püsiprogrammeerimine aruandesse.
- Märkide muutmine, kopeerides eelmise lahtri väärtuse ja korrutades selle väärtusega –1.

> [!NOTE]
> Paljudel juhtudel tuleb konfigureerida aruande definitsiooni nii, et veeru arvutused tehtaks enne rea arvutusi. Selle konfiguratsiooni lõpetamiseks järgige järgmisi etappe.
>
> 1. Avage aruande kujundajas aruande definitsioon.
> 2. Valige vahekaardi **Sätted** suvandist **Arvutamise prioriteet** suvand **Tee esmalt veeru ja seejärel rea arvutus**.

## <a name="designing-the-report"></a>Aruande kujundamine

Aruande kujundamisel peaksite esmalt looma kõik üksikasjaread, veendumaks, et kõik väärtused tõmmatakse ootuspäraselt. Seejärel lisage lõplikke väärtusi sisaldava üksikasja peitmiseks vormingu **NP** (mitteprinditav) alistamised.

> [!IMPORTANT]
> Kui kasutate readefinitsioonis vormingukoodi **CAL**, ei saa te kande üksikasjadesse süvitsi minna.

Sundimisel kasutavad valemid järgmist vormingut: &lt;sihtveerg&gt;=&lt;lähteveerg&gt;.&lt;rea kood&gt;. Eraldage rea mis tahes täiendavad paigutused koma ja tühikuga. Näide: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Täiendavate vormingusuvandite näited

Järgmistes näidetes näidatakse, kuidas vormindada readefinitsiooni ja veeru definitsiooni rahavoogude põhiaruande (näide 1) ja statistilise aruande (näide 2) sundimiseks.

### <a name="example-1-basic-forcing"></a>Näide 1: põhisundimine

Järgmises tabelis on toodud põhisundimist kasutava readefinitsiooni näide.

| Reakood |           Kirjeldus            | Vormingukood | Seotud valemid/read/üksused |        Reamuundur        | Link finantsdimensioonidele |
|----------|----------------------------------|-------------|-----------------------------|----------------------------|------------------------------|
| 100      | Kassa perioodi alguses (NP) |             |                             | Konto muutuja = \[/BB\] | +Segment2 = \[1100\]         |
| 130      | Raha perioodi algul      | CAL         | C=C.100,F=D.100             |                            |                              |
| 160      |                                  |             |                             |                            |                              |
| 190      |                                  |             |                             |                            |                              |

> [!NOTE]
> Esitluse huvides eemaldati eelmisest tabelist tühjad veerud: veerge Vormingu alistamine, Tavasaldo, Printimise juhtelement ja Veerupiirang ei kuvata.

Järgmises tabelis on toodud reas põhisundimist kasutava veeru definitsiooni näide.

|           Vorming             | A   | B    | C        | D      | E      | R    |
|------------------------------|-----|------|----------|--------|--------|------|
| Päis 1                     |     |      |          |        |        |      |
| Päis 2                     | A   | B    | C        | D      | E      | R    |
| Päis 3                     |     |      |          |        |        |      |
| Veeru tüüp                  | ROW | DESC | FD       | FD     | FD     | CALC |
| Konteerimiskood/atribuudi kategooria |     |      | ACTUAL   | ACTUAL | ACTUAL |      |
| Finantsaasta                  |     |      | BASE     | BASE   | BASE   |      |
| Periood                       |     |      | BASE     | BASE   | BASE   |      |
| Hõlmatud perioodid              |     |      | PERIODIC | YTD/BB | YTD    |      |
| Valem                      |     |      |          |        |        | E-D  |
| Veeru laius                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Näide 2: statistilised aruanded

Järgmises tabelis on toodud põhisundimist kasutava readefinitsiooni näide statistilise aruande puhul.

| Rea kood | Kirjeldus               | Vormingu kood | Seotud valemid/read/üksused     | Vormingu alistamine      | Tavasaldo | Link finantsdimensioonidele               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|--------------------------------------------|
| 50       | Statistiline teave   | REM         |                                 |                      |                |                                            |
| 100      | Töötajate koguarv – USA            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 115      | Töötajate koguarv – rahvusvaheline | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 130      |                           |             |                                 |                      |                |                                            |
| 190      | Müük USA-s                  |             |                                 |                      | C              | +Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Rahvusvaheline müük       |             |                                 |                      | C              | +Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |                                            |
| 280      |                           |             |                                 |                      |                |                                            |
| 310      | Müük USA-s                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |                                            |
| 340      | Rahvusvaheline müük       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |                                            |

> [!NOTE]
> Esitluse huvides eemaldati eelmisest tabelist tühjad veerud: veerge Printimise juhtelement, Veerupiirang ja Rea muutuja ei kuvata.

Järgmises tabelis on toodud põhisundimist kasutava veeru definitsiooni näide statistilise aruande puhul.

|    Vorming                    | A   | B    | C      | D            | E     | R            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Päis 1                     | A   | B    | C      | D            | E     | R            |
| Päis 2                     | -   | -    | YTD    | Müük aastas | Personal | $ isiku kohta |
| Päis 3                     |     |      |        |              |       |              |
| Veeru tüüp                  | ROW | DESC | FD     | CALC         | CALC  | CALC         |
| Konteerimiskood/atribuudi kategooria |     |      | ACTUAL |              |       |              |
| Finantsaasta                  |     |      | BASE   |              |       |              |
| Periood                       |     |      | BASE   |              |       |              |
| Hõlmatud perioodid              |     |      | YTD    |              |       |              |
| Valem                      |     |      |        |              |       | E-D          |
| Veeru laius                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Rea piiramine konkreetse aruandlusüksusega

Kui aruande rida on piiratud kindla aruandlusüksusega, kuvatakse sellel real lingitud andmed ainult nimetatud aruandlusüksuse puhul ja eiratakse muude aruandluspuu aruandlusüksuste andmeid. Näiteks saate luua rea, mis sisaldab kindla osakonna tegevuskulude kogusumma üksikasju. Teie aruanne võib sisaldada topeltandmeid, kui aruanne sisaldab nii aruandluspuud kui ka readefinitsiooni, millel on rohkem kui ainult füüsiline konto. Näiteks kui teil on organisatsiooni kuut osakonda loetlev aruandluspuu ja ka readefinitsioon, mis loetleb rea konto ja osakonna kindla kombinatsiooni. Aruande loomisel prinditakse konto ja osakonna kindel kombinatsioon igale aruandluspuu lehele, kuigi see osakond ei pruugi puus olevaga ühtida. Sellise käitumise põhjustab see, et rida alistab selle, mille aruande definitsioon üldjuhul välja filtrib. Üheks andmete dubleerimise vältimise võimaluseks on rea piiramine kindla aruandlusüksusega.

> [!NOTE]
> Kui rida sisaldab dimensioone ja piirate selle rea aruandluse tütarüksusega, kaasatakse rea summa selle tütarüksuse ja selle emaüksuste puhul, kuid dubleerimist ei toimu.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Rea piiramine aruandlusüksusega

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja valige seejärel muutmiseks readefinitsioon.
2. Topeltklõpsake vastavat lahtrit **Seotud valemid/read/üksused**.
3. Valige dialoogiboksi **Aruandlusüksuse valik** väljal **Aruandluspuu** aruandedefinitsioonis määratud aruandluspuu.
4. Valige aruandlusüksus ja seejärel klõpsake nuppu **OK**. Piirang kuvatakse readefinitsiooni lahtris.
5. Topeltklõpsake lahtrit piiratud rea veerus **Link finantsdimensioonidele** ja sisestage seejärel link finantsandmete süsteemile.

## <a name="selecting-print-control-in-a-row-definition"></a>Prindi kontrollkoodi valimine readefinitsioonis

Saate määrata prindi kontrollkoodid iga veeru puhul, kasutades lahtrit **Prindi kontrollkood**.

### <a name="add-print-control-codes-to-a-report-row"></a>Prindi kontrollkoodide lisamine aruande reale

1. Avage aruande kujundajas muudetav readefinitsioon.
2. Topeltklõpsake lahtrit **Prindi kontrollkood**.
3. Valige prindi kontrollkood dialoogiboksist **Prindi kontrollkood** või vajutage ja hoidke mitme koodi valimiseks all klahvi Ctrl. Saate prindi kontrollkoodid sisestada ka otse lahtrisse **Prindi kontrollkood**. Kasutage mitme prindi kontrollkoodi eraldamiseks komasid.
4. Valige mis tahes tingimusliku prindi suvandid.
5. Klõpsake nupul **OK**.

### <a name="regular-print-control-codes"></a>Tavalised prindi kontrollkoodid

Järgmises tabelis kirjeldatakse readefinitsiooni tavalisi printimise kontrollkoode.

| Prindi kontrollkood | Prindi kontrollkoodi tõlgendus         | Kirjeldus |
|--------------------|--------------------------------------------------|-------------|
| NP                 | Mitteprinditav rida                                 | Rea summade aruandesse printimise vältimine ja summade välistamine arvutustest. Mitteprinditava veeru kaasamiseks arvutusse viidake veerule otse arvutusvalemis. Näiteks on mitteprinditav rida 240 kaasatud järgmisse arvutusse: **230+240+250**. Mitteprinditav rida 240 pole kaasatud järgmisse arvutusse: **230:250**. |
| CS                 | Valuuta tähis; selle rea valuutavormingu kasutamine | Valuutatähise kaasamine kõigisse mitteprotsentuaalsetesse summadesse. Protsentuaalsetel väärtustel pole kunagi valuutatähist. |
| XD                 | Rea peitmine konto üksikasjade aruandes            | Kontode kuva peitmine konto üksikasjade aruannetes ja kande üksikasjade aruannetes. See prindi kontrollkood on kasulik, kui rida sisaldab mitut kontot, mida ei tohiks konto üksikasjade aruandes või kande üksikasjade aruandes loetleda. |
| X0                 | Rea peitmine kõikide nullide puhul                        | Rea välistamine aruandest, kui kõik selle rea lahtrid on kas tühjad või sisaldavad nulle. See prindi kontrollkood on oluline ainult siis, kui nullsaldo peitmise suvand pole aruande definitsioonis valitud. |
| B0                 | Nullveergude tühjaks jätmine                         | Nullsummasid sisaldavate rea veergude tühjaks jätmine. |
| XR                 | Ümberarvestuse peitmine                                  | Ümberarvestuse peitmine. Kui aruanne kasutab aruandluspuud, ei koondata selle rea summasid järgnevatesse emasõlmedesse. |
| SR                 | Peida ümardamine                                | Selle rea summade ümardamise takistamine. |
| XT                 | Rea peitmine kande üksikasjade aruandes        | Kannete kuva peitmine kande üksikasjade aruannetes. See prindi kontrollkood on kasulik, kui rida sisaldab mitut kontot, mida ei tohiks kande üksikasjade aruandes loetleda. |

### <a name="conditional-print-control-codes"></a>Tingimuslikud prindi kontrollkoodid

Järgmises tabelis kirjeldatakse readefinitsiooni tingimusliku printimise kontrollkoode.

| Prindi kontrollkood | Kirjeldus                                  |
|--------------------|----------------------------------------------|
| (puudub)             | Tingimusliku prindi suvandi tühjendamine.       |
| DR                 | Ainult selle rea deebetsaldode printimine.  |
| CR                 | Ainult selle rea kreeditsaldode printimine. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Readefinitsiooni lahter Veeru piirang

Readefinitsiooni lahtril **Veeru piirangud** on mitu eesmärki. Olenevalt rea tüübist saate kasutada lahtrit **Veeru piirangud** ühe järgmise funktsiooni määramiseks.

- Lahter võib piirata rea summade printimise kindlale veerule. See funktsioon on kasulik tabeli kujul bilansi loomisel.
- Lahter võib määrata sortimiseks summade veeru.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Arvutusvalemi kasutamine readefinitsioonis

Readefinitsiooni arvutusvalem võib sisaldada tehtemärke **+**, **-**, **\**_ ja _*/** ning ka lauseid **IF/THEN/ELSE**. Lisaks võib arvutus sisaldada üksikuid lahtreid ja absoluutsummasid (tegelikud valemisse kaasatud arvud). Valem võib sisaldada kuni 1024 märki. Arvutusi ei saa rakendada ridadele, mis sisaldavad lahtreid tüübiga **Link finantsdimensioonidele** (FD). Siiski saate arvutusi järjestikustele ridadele kaasata, peita nende ridade printimise ja arvutada seejärel arvutusridade kogusumma.

### <a name="operators-in-a-calculation-formula"></a>Arvutusvalemi tehtemärgid

Arvutusvalem kasutab keerukamaid tehtemärke kui rea kogusumma valem. Siiski saate kasutada tehtemärke **\**_ ja _*/** koos täiendavate tehtemärkidega summade korrutamiseks (\*) ja jagamiseks (/). Vahemiku või summa kasutamiseks arvutusvalemis peate kasutama mis tahes rea koodi ees kommertsmärki (@), v.a juhul, kui kasutate readefinitsioonis veergu. Näiteks rea 100 summa liitmiseks rea 330 summale saate kasutada rea kogusumma valemit **100+330** või arvutusvalemit **@100+@330**.

> [!NOTE]
> Peate kasutama kommertsmärki (@) enne igat arvutusvalemis kasutatavat rea koodi. Vastasel korral loetakse numbrit absoluutsummaks. Näiteks valem **@100+330** lisab real 100 olevale summale 330 USA dollarit. Kui viitate arvutusvalemis veerule, ei ole @-märki vaja.

### <a name="create-a-calculation-formula"></a>Arvutusvalemi loomine

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Topeltklõpsake lahtrit **Vormingu kood** ja seejärel valige **CAL**.
3. Sisestage arvutusvalem lahtrisse **Seotud valemid/read/üksused**.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Kindlate ridade arvutusvalemi näide

Näiteks tähendab arvutusvalem **@100+@330**, et rea 100 summa lisatakse rea 330 summale. Rea koguvalem **@340+370** lisab real 340 oleva summa real 370 olevale summale. (Summa real 370 pärineb arvutusvalemist.)

| Rea kood | Kirjeldus                 | Vormingu kood | Seotud valemid/read/üksus | Printimise juhtelement | Rea muutuja | Link finantsdimensioonidele |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Raha perioodi algul |             |                            | NP            | BB           | +Konto=\[1100:1110\]       |
| 370      | Raha aasta algul   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Raha perioodi algul | TOT         | 340+370                    |               |              |                              |

Kui readefinitsiooni rea vormingu kood on **CAL** ja sisestate matemaatilise arvutuse lahtrisse **Seotud valemid/read/üksused**, peate sisestama ka aruande seotud veeru ja rea tähe. Näiteks veeru A rea 120 kujutamiseks sisestage **A.120**. Samuti on võimalik kõigi veergude tähistamiseks kasutada märki @. Näiteks rea 120 kõigi veergude kujutamiseks sisestage **@120**. Mis tahes arvutust, millel veeru tähte või märki @ pole, peetakse reaalarvuks.

> [!NOTE]
> Kasutades reale viitamiseks sildi reakoodi, peate kasutama veeru tähe ja sildi vahelise eraldajana punkti (.) (nt **A.GROSS\_MARGIN/A.SALES**). @-märgi kasutamisel pole eraldaja nõutav (nt **\@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Kindla veeru arvutusvalemi näide

Selles näites tähendab arvutusvalem **E=C.340** seda, et veeru C rea 340 arvutust tehakse ainult veerus E.

> [!NOTE]
> Kui viitate arvutusvalemis veerule, ei ole @-märki vaja.

| Rea kood | Kirjeldus                 | Vormingu kood | Seotud valemid/read/üksus | Printimise juhtelement | Rea muutuja | Link finantsdimensioonidele |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Kassa perioodi alguses |             |                            | NP            | BB           | +Konto=\[1100:1110\]       |
| 370      | Kassa aasta alguses   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Kassa perioodi alguses | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Numbri muutmine valitud veergudes

Kui muudate numbrit või arvutust kindla rea ühes veerus, kuid ei soovi mõjutada aruande teisi veerge, saate määrata suvandi **CAL** (arvutus) readefinitsiooni veerus **Vormingu kood**.

- Arvutuse tegemiseks kõigis aruande veergudes (**FD**) ärge sisestage veeru määramist.
- Valemi piiramiseks kindlate veergudega sisestage veeru täht, võrdusmärk (**=**) ja seejärel valem.
- Saate määrata mitu veergu. Kui kasutate kommertsmärki (@) kindlas veeru paigutuses, seotakse kommertsmärk (@) reaga.
- Saate ühele reale sisestada mitu veeru valemit. Eraldage valemid komadega.

### <a name="calculation-examples"></a>Arvutusnäited

| Kalkulatsioon            | Loodud tegevus                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Iga veeru puhul korrutatakse rea 130 väärtus arvuga 0,75. Tulemus pannakse seejärel iga veeru aktiivsele reale. |
| B=@130\*.75            | Sama arvutust tehakse ainult veerus B.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>Readefinitsiooni laused IF/THEN/ELSE

Lauseid **IF/THEN/ELSE** saab lisada mis tahes kehtivasse arvutusse ja kasutada vorminguga **CAL**. Saate sisestada arvutusvalemeid **IF/THEN/ELSE** veeru **Seotud valemid/read/üksused** lahtrisse. Arvutusvalemid **IF/THEN/ELSE** kasutavad järgmist valemit: IF &lt;lause tõene/väär&gt; THEN &lt;valem&gt; ELSE &lt;valem&gt; Lause **ELSE &lt;valem&gt;** osa on valikuline.

#### <a name="if-statements"></a>IF-laused

Lausele **IF** järgnevaks lauseks võib olla mis tahes lause, mida saab hinnata tõese või väärana. Lausele **IF** järgnev lause võib hõlmata lihtsat hindamist või olla mitut avaldist sisaldav keerukas lause. Järgmisena on toodud mõned näited.

- **IF A.200&gt;0** (lihtne hindamine)
- **IF A.200&gt;0 AND A.200&lt;10,000** (keerukas lause)
- **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (mitut avaldist sisaldav keerukas lause)

Mõiste **Perioodid** lauses **IF** näitab aruande perioodide arvu. Seda mõistet kasutatakse üldjuhul kumulatiivse keskmise arvutamiseks. Näiteks kui käivitate aruande perioodiks 7 YTD, tähendab lause **B.150/Periods**, et veeru B rea 150 väärtus jagatakse 7-ga.

#### <a name="then-and-else-formulas"></a>Valemid THEN ja ELSE

Valemiks **THEN** ja **ELSE** võib olla mis tahes kehtiv arvutus alates väga lihtsatest väärtuse määramistest kuni keerukate valemiteni. Näiteks lause **IF A.200 &gt;0 THEN A=B.200** tähendab järgmist: kui veeru A rea 200 lahtri väärtus on suurem kui 0 (null), pange veeru B rea 200 lahtris olev väärtus veeru A aktiivse rea lahtrisse. Eelnev lause **IF/THEN** paneb väärtuse aktiivse rea ühte veergu. Siiski saate kasutada kommertsmärki (@) kas tõene/väär hindamistes või valemit kõigi veergude tähistamiseks. Järgmiselt on toodud mõned järgmistes jaotistes kirjeldatud näited.

- **IF A.200 &gt;0 THEN B.200**: kui lahtri A.200 väärtus on positiivne, pannakse lahtri B.200 väärtus aktiivse rea igasse veergu.
- **IF A.200 &gt;0 THEN @200**: kui lahtri A.200 väärtus on positiivne, pannakse rea 200 iga veeru väärtus aktiivse rea asjakohasesse veergu.
- **IF @200 &gt;0 THEN @200**: kui aktiivse veeru rea 200 väärtus on positiivne, pannakse rea 200 väärtus aktiivse rea samasse veergu.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Arvutuse piiramine readefinitsiooni aruandlusüksusega

Arvutuse piiramiseks aruandluspuu ühe aruandlusüksusega nii, et saadavat summat ei koondataks kõrgema taseme üksusesse, saate kasutada koodi **\@Unit** readefinitsiooni lahtris **Seotud valemid/read/üksused**. Kood **\@Unit** loetletakse aruandluspuu veerus B **Üksuse nimi**. Koodi **\@Unit** kasutamisel väärtusi ei koondata, kuid arvutust hinnatakse aruandluspuu igal tasandil.

> [!NOTE]
> Selle funktsiooni kasutamiseks peab aruandluspuu olema readefinitsiooniga seostatud.

Arvutusrida võib viidata arvutusreale või finantsandmete reale. Arvutus registreeritakse readefinitsiooni lahtrisse **Seotud valemid/read/üksused** ja finantsandmete tüübi piirangusse. Arvutus peab kasutama tingimuslikku arvutust, mis algab **Kui \@Ühik** konstruktsiooniga. Näide: IF @Unit(SALES) THEN @100 ELSE 0 See arvutus hõlmab rea 100 summa igasse aruande veergu, kuid ainult üksuse SALES (Müük) puhul. Kui SALES (Müük) on mitme üksuse nimeks, kuvatakse summa kõigis neis üksustes. Lisaks võib rida 100 olla finantsandmete rida ja määratletud mitteprinditavana. Sellisel juhul takistatakse summa kuvamist puu kõigis üksustes. Samuti saate piirata summa aruande ühe veeruga, näiteks veeruga H, kasutades ainult selle aruande veeru väärtuse printimiseks veeru piirangut. Saate kaasata **OR** kombinatsioone lauses **IF**. Siin on näide: **KUI @Unit(SALES) VÕI @Unit(SALESWEST) SIIS 5 ELSE @100**. Saate arvutuse tüüpi piirangus määrata ühiku järgmisel moel:

- Sobivate üksuste kaasamiseks sisestage üksuse nimi. Näiteks **Kui \@Üksus(SALES)** võimaldab arvutuse mis tahes üksuse puhul, mille nimi on SALES (Müük), seda isegi juhul, kui aruandluspuus on mitu müügiüksust.
- Sisestage ettevõtte ja üksuse nimi arvutuse piiramiseks kindla ettevõtte kindlate üksustega. Näiteks sisestage **IF @Unit(ACME:SALES)** arvutuse piiramiseks müügiüksustega ettevõttes ACME.
- Sisestage aruandluspuust täielik hierarhia kood arvutuse piiramiseks kindla üksusega. Näiteks sisestage **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)**.

> [!NOTE]
> Täieliku hierarhiakoodi leidmiseks paremklõpsake aruandluspuu definitsioonis ja valige seejärel suvand **Aruandlusüksuse identifikaatori kopeerimine (H-kood)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Arvutuse piiramine aruandlusüksusega

1. Klõpsake aruandekoosturis suvandit **Readefinitsioonid** ja avage seejärel muudetav readefinitsioon.
2. Topeltklõpsake lahtrit **Vormingu kood** ja seejärel valige **CAL**.
3. Klõpsake **Seotud valemid/read/üksused** lahtrit ja seejärel sisestage tingimuslik arvutus, mis algab **Kui \@Üksus** konstruktsiooniga.

### <a name="ifthenelse-statements-in-a-column-definition"></a>Veeru definitsiooni laused IF/THEN/ELSE

Lause **IF/THEN/ELSE** võimaldab mis tahes arvutuse sõltumise teiste veergude tulemustest. Saate teistele veergudele viidata, kuid te ei saa viidata aruande lahtrile lauses **IF**. Arvutus tuleb rakendada kogu veerule. Näiteks lause **IF B&gt;100 THEN B ELSE C\*1.25** tähendab järgmist: kui veeru B summa on üle 100, pange veeru B väärtus veergu **CALC**. Kui veeru B summa pole üle 100, korrutage veeru C väärtus 1,25-ga ja pange tulemus veergu **CALC**. Pange lause **IF** järele alati loogikalause, mida saab hinnata tõese või väärana. Nii lause **THEN** kui ka **ELSE** puhul kasutatavad valemid võivad sisaldada viiteid mis tahes arvule veergudele ja need valemid võivad olla nii keerukad, kui soovite.

> [!NOTE]
> Arvutuse tulemusi ei saa panna muusse veergu. Tulemused peavad olema valemit sisaldavas veerus.

#### <a name="use-single-quotes-and-an-ampersand-for-dimension-values-in-a-row-column-or-tree"></a>Kasutage ühekordseid jutumärke ('') ning ja-märki (&) dimensiooniväärtusi reas, veerus või aruandluspuul

Saate koostada aruandeid, kasutades dimensiooniväärtusi, mis sisaldavad ja-märki (&).

Mis tahes väljal **Link finantsdimensioonidele** saate sisestada väärtuse nagu **"P & L"**. Ühekordsete jutumärkide (' ') kasutamine dimensiooniväärtuse mõlemal küljel näitab, et kasutate literaalväärtust, sh ja-märk (&).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
