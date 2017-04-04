---
title: Valemikoostaja elektroonilises aruandluses
description: "Selles teemas selgitatakse, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat. ER-is kindla elektroonilise dokumendi vormingu koostamisel saate kasutada Microsoft Exceli sarnaseid valemeid andmete teisendamiseks, et vastata selle dokumendi täitmise ja vormindamise nõuetele. Erinevat tüüpi funktsioone toetatakse -, kuupäev ja kellaaeg, loogiline, matemaatiline teabe, andmete tüübi teisendamise ja teiste (äri domeeni-spetsiifilisi funktsioone)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ac8d6c064ca826cc1c2fed07578ca9ce0c66ef66
ms.lasthandoff: 03/31/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Valemikoostaja elektroonilises aruandluses

Selles teemas selgitatakse, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat. ER-is kindla elektroonilise dokumendi vormingu koostamisel saate kasutada Microsoft Exceli sarnaseid valemeid andmete teisendamiseks, et vastata selle dokumendi täitmise ja vormindamise nõuetele. Erinevat tüüpi funktsioone toetatakse -, kuupäev ja kellaaeg, loogiline, matemaatiline teabe, andmete tüübi teisendamise ja teiste (äri domeeni-spetsiifilisi funktsioone).

<a name="formula-designer-overview"></a>Valemikoostaja ülevaade
-------------------------

Elektrooniline aruandlus (ER) toetab valemikoostajat. Seega saate koostamise ajal konfigureerida avaldisi, misa saab kasutada käitamisel järgmisteks ülesanneteks:

-   teisendada Microsoft Dynamics 365 for Operationsi andmebaasist saadud andmeid. Need peavad olema asustatud ER-i andmemudelisse, mis on mõeldud ER-vormingute andmeallikaks (filtreerimine, grupeerimine, andmetüübi konversioon jne);
-   vormindada andmeid, mis tuleb saata elektroonilisele dokumendile kindla ER-vormingu paigutuse ja tingimuste järgi (kooskõlas nõutava keele või kultuuriga, kodeeringuga jne);
-   juhtida elektroonilise dokumendi loomise protsessi (vormingu teatud elementide arvestamise lubamine/keelamine olenevalt andmete töötlemisest, dokumentide loomise katkestamisest, lõppkasutajatele sõnumite saatmisest jne).

Valemikoostaja lehe saab avada järgmiste tegevuste käigus.

-   Andmeallika kaupade sidumine andmemudeli komponentidega.
-   Andmeallika kaupade sidumine vormingu komponentidega.
-   Arvutatud väljade täielik haldamine andmeallikate osana.
-   Kasutaja sisendparameetrite nähtavustingimuste määratlemine.
-   Vormingu teisenduste kujundamine.
-   Vormingu komponentide lubamistingimuste määratlemine.
-   Vormingu failikomponentide failinimede määratlemine.
-   Protsessi juhtimise kinnituste tingimuste määratlemine.
-   Protsessi juhtimise kinnituste teate tekstide määratlemine.

## <a name="designing-er-formulas"></a>ER-i valemite koostamine
### <a name="data-binding"></a>Andmete sidumine

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis teisendab andmeid, mis saadakse andmeallikatest, nii et käitamisel saab andmeid asustada andmete tarbijas:

-   Dynamics 365 for Operationsi andmeallikatest ja käitamisaja parameetritest ER-i andmemudelisse;
-   ER-i andmemudelist ER-i vormingusse;
-   Dynamics 365 for Operationsi andmeallikatest ja käitamisaja parameetritest ER-i vormingusse.

Järgmisel joonisel on seda tüüpi avaldise kujundus. Selles näites annab avaldis Dynamics 365 for Operationsi tabeli **Intrastat** välja **Intrastat.AmountMST** väärtuse pärast selle väärtuse ümardamist kahe kümnendkohani. [![pilt-sõna-siduv](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) järgmine joonis kujutab selline väljendus kasutamise. Selles näites on kujundatud Avaldise tulemus asustatud linnas on **Transaction.InvoicedAmount** osa ning **maksude aruandluse mudel** andmemudel. [![pilt-sõna-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) käivitamise ajal loodud valem **ÜMMARGUNE (Intrastat.AmountMST, 2)**, ümardab väärtuse ning **AmountMST** välja iga kirje kohta on **Intrastat** sajandikkohani tabel ja asustada ümardatud väärtus on **Transaction.InvoicedAmount** osa ning **maksuaruandluse** andmemudel.

### <a name="data-formatting"></a>Andmete vormindamine

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis vormindab andmeid, mis saadakse andmeallikatest, nii et andmeid saab saata elektroonilise dokumendi loomise osana. Kui teil on vorming, mida tuleb rakendada tüüpilise reeglina, mida tuleb vormingu puhul taaskasutada, saate kasutada seda vormingut ühe korra vormingu konfiguratsioonis nimega teisendusena, millel on vormindamisavaldis. Selle nimelise teisenduse saab siduda paljude vormingu komponentidega, mille väljund peab olema vormindatud vastavalt loodud avaldisele. Järgmisel joonisel on seda tüüpi teisenduse kujundus. Selles näites võtab teisendus **TrimmedString** andmetüübi **String** sissetulevad andmed ning kärbib stringi väärtuse andmisel algus- ja lõputühikud. [![pilt-ümberkujundamine-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) järgmine joonis kujutab selline määramist kasutamise. Selles näites viitavad mitu vormingu komponenti, mis saadavad teksti käitusajal väljundina elektroonilise dokumendi loomisel, teisendusele **TrimmedString** nime järgi. [![pilt, ümberkujundamise ja kasutamine](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Kuna formaat komponentide viitavad selle ** TrimmedString ** ümberkujundamine (näiteks on **partyName** osa eelmisel pildil) see saadab teksti kui teeniva dokumendi. Tekst ei sisalda algus- ega lõputühikuid. Kui teil on vorming, mida tuleb rakendada eraldi, saab selle kasutusele võtta kindla vormingu komponendi sidumise üksiku avaldisena. Järgmisel joonisel on seda tüüpi avaldis. Selles näites on vormingu komponent **partyType** seotud andmeallikaga avaldise kaudu, mis teisendab sissetulevad andmeallika andmed väljalt **Model.Company.RegistrationType** suurtäheliseks tekstiks ja saadab selle teksti väljundina elektroonilisse dokumenti. [![pilt-Köitmine-koos-valem](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Protsessi voo juhtimine

ER-i valemikoostajat saab kasutada dokumentide loomise protsessivoo juhtimiseks kasutatavate avaldiste määratlemiseks. Saate:

-   Määratlege tingimused, mis määravad, millal tuleb dokumendi loomise protsess peatada.
-   Määrake avaldised, mis loovad lõppkasutajale sõnumeid peatatud protsesside kohta või heidavad käivitamislogi sõnumeid aruande loomise protsessi jätkamise kohta.
-   Määrake loodavate dokumentide failinimed ja juhtige nende loomise tingimusi.

Iga protsessi voo juhtimise reegel on koostatud üksiku kinnitusena. Järgmisel joonisel on seda tüüpi kinnitus. Siin on selles näites oleva konfiguratsiooni selgitus.

-   Kinnitamine on hinnatud, kui loodavas XML-failis luuakse **INSTAT**-sõlm.
-   Kui kannete loend on tühi, lõpetab kinnitamine käivitamisprotsessi ja tagastab väärtuse **FALSE**.
-   Kinnitamine annab tõrketeate, mis sisaldab SYS70894 teksti kasutaja eelistatud keeles.

[![pilt-valideerimise](./media/picture-validation.jpg)](./media/picture-validation.jpg) The ER valemi disainer saab ka määrama teeniva elektroonilise dokumendi nime ja faili loomise protsessi. Järgmisel joonisel on seda tüüpi protsessi voo juhtimise kujundus. Siin on selles näites oleva konfiguratsiooni selgitus.

-   Andmeallika **model.Intrastat** kirjete loend on jagatud partiideks, millest iga sisaldab kuni 1000 kirjet.
-   Väljund loob zip-faili, mis sisaldab ühte XML-vormingus faili iga loodud partii kohta.
-   Avaldis tagastab failinime loodavatele elektroonilistele dokumentidele, liites faili nime ja laiendi. Teise partii ja kõikide järgnevate partiide puhul sisaldab faili nimi järelliitena partii ID-d.
-   Avaldis lubab (andes vatuseks väärtuse **TRUE**) faili loomise protsessi partiidele, mis sisaldavad vähemalt ühte kirjet.

[![faili-juhtelemendi](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Põhisüntaks

ER-i avaldised võivad sisaldada mõnd või kõiki järgmistest elementidest.

-   Konstandid
-   Operaatorid
-   Viited
-   Teed
-   Funktsioonid

#### <a name="constants"></a>Konstandid

Avaldiste koostamisel saate kasutada tekstilisi ja arvulisi konstante (väärtused, mida ei arvutata). Näiteks avaldis ** väärtus ("100") + 20 ** kasutab arv pidevalt 20- ja string pidev "100" ja tagastab arvulise väärtuse **120**. ER-i valemikoostaja toetab paoseeriaid, mis tähendab, et saate määrata avaldise stringi, mida tuleb teisiti käsitleda. Näiteks avaldis **Lev Tolstoi „„Sõda ja rahu”” 1. osa** tagastab tekstistringi **Lev Tolstoi „Sõda ja rahu” 1. osa**.

#### <a name="operators"></a>Operaatorid

Järgmises tabelis on aritmeetilised tehtemärgid, mida saate kasutada põhiliste matemaatiliste tehete puhul, nagu liitmine, lahutamine, jagamine ja korrutamine.

| Operaator | Tähendus              | Näide |
|----------|----------------------|---------|
| +        | Lisa             | 1 + 2     |
| -        | Lahutamise eitus | 5–2 –1  |
| \*       | Korrutamine       | 7\*8    |
| /        | Jaotus             | 9 / 3     |

Järgmises tabelis on võrdlemise tehtemärgid, mida toetatakse ning mida saate kasutada kahe väärtuse võrdlemiseks.

| Operaator | Tähendus                  | Näide    |
|----------|--------------------------|------------|
| =        | Võrdne                    | X = Y        |
| &gt;     | Suurem kui             | X&gt;Y     |
| &lt;     | Väiksem kui                | X&lt;Y     |
| &gt;=    | Suurem kui või võrdne | X&gt;=Y    |
| &lt;=    | Väiksem kui või võrdne    | X&lt;=Y    |
| &lt;&gt; | Pole võrdne             | X&lt;&gt;Y |

Lisaks saate kasutada ja-märki (&) teksti liitmise tehtemärgina, et ühendada või liita üks või mitu tekstistringi üheks tekstiks.

| Operaator | Tähendus     | Näide                                        |
|----------|-------------|------------------------------------------------|
| &        | Ühenda | „Midagi pole printida” & „: ” & „kirjeid ei leitud” |

#### <a name="operator-precedence"></a>Tehete järjestus

Liitavaldise osade arvutamise järjekord on oluline. Näiteks tulemus väljend ** 1 + 4 / 2 ** erineb sõltuvalt sellest, kas selle lisamine ega osakonna tööd tehakse esimest. Saate kasutada sulge, et selgelt määratleda, kuidas avaldise väärtust leida. Näiteks näitamaks, et esimesena tuleb teha liitmistoiming, saate muuta eelnevat avaldis järgmiselt: **(1 + 4) / 2**. Kui avaldise tehted ei ole selgelt määratletud, põhineb järjekord vaikimisi järjestusel, mis on määratud toetatud tehtemärkidele. Järgmistes tabelites on tehted ja igale tehtele määratud järjestus. Kõrgema prioriteediga tehted (nt 7) arvutatakse enne madalama prioriteediga tehteid (nt 1).

| Tehtejärjestus | Operaatorid      | Süntaks                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Grupeerimine       | ( … )                                                    |
| 6          | Liikme juurdepääs  | … . …                                                    |
| 5          | Funktsioonikutse  | … ( … )                                                  |
| 4          | Korrutamine | … \* … … / …                                             |
| 3          | Täiend       | … + … … - …                                              |
| 2          | Võrdlus     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Lahutamine     | … , …                                                    |

Samal real olevatel tehetel on võrdne prioriteet. Kui avaldis sisaldab mitut sellist tehet, arvutatakse avaldist vasakult paremale. Nt avaldis **1 + 6 / 2 \*3 &gt;5** tagastab **true**. Soovitame kasutada sulge näitamaks selgelt avaldise arvutamise soovitud järjestust, et avaldisi oleks lihtsam lugeda ja hallata.

#### <a name="references"></a>Viited

Kõiki praeguse ER-i komponendi (mudel või vorming) andmeallikaid, mis on avalduse koostamise ajal saadaval, saab kasutada nimega viidetena. Näiteks praegune ER-i andmemudel sisaldab andmeallikat **ReportingDate**, mis tagastab andmetüübi **DATETIME** väärtuse. Õigesti vormingus teeniva dokumendi väärtust, saate otsida andmeallikas väljendamisel järgmine: **DATETIMEFORMAT (ReportingDate, "päev-kuu-aasta")** kõik märgid viitamisteenuse andmeallika nime, mis ei esinda kirja tähestiku ette ülakoma ('). Kui viitamisteenuse andmeallika nimi sisaldab vähemalt üks sümbol, mis ei Näita kirja tähestiku (nt kirjavahemärgid või sümbolid kirjaliku), tuleb nimi panna ülakomade. Järgmisena on toodud mõned näited.

-   Andmeallikale **Tänane kuupäev ja kellaaeg** tuleb viidata ER-i avaldises järgmiselt: **'Tänane kuupäev ja kellaaeg'**
-   ER-i avaldises tuleb viidata andmeallika **Kliendid** meetodile **nimi()** järgmiselt: **Kliendi.'nimi()'**

#### <a name="path"></a>Tee

Kui avaldis viitab struktureeritud andmeallikale, saate kasutada tee määratlemist, et valida selle andmeallika kindel primitiivne element. Punkti (.) kasutatakse struktureeritud andmeallika üksikute elementide eraldamiseks. Näiteks praegune ER-i andmemudel sisaldab andmeallikat **InvoiceTransactions**, mis tagastab kirjete loendi. Kirje struktuur** InvoiceTransactions** sisaldab välju **AmountDebit** ja **AmountCredit**, mis tagastavad arvulisi väärtusi. Seega saate arveldatud summa arvutamiseks koostada järgmise avaldise: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funktsioonid

Järgmises jaotises kirjeldatakse funktsioone, mida saab kasutada ER-i avaldistes. Kõiki avaldise konteksti (praegune ER-i andmemudel või ER-i vorming) andmeallikaid ja ka konstante saab kasutada helistamisfunktsioonide parameetritena vastavalt helistamisfunktsiooni argumentide loendile. Näiteks praegune ER-i andmemudel sisaldab andmeallikat **InvoiceTransactions**, mis tagastab kirjete loendi. Kirje struktuur** InvoiceTransactions** sisaldab välju **AmountDebit** ja **AmountCredit**, mis tagastavad arvulisi väärtusi. Seega saate arveldatud summa arvutamiseks koostada järgmise avaldise, mis kasutab sisseehitatud ER-i ümardamisfunktsiooni: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Toetatud funktsioonid
Järgmistes tabelites kirjeldatakse andmete manipuleerimise funktsioone, mida saate kasutada ER-i andmemudelite ja ER-i aruannete koostamiseks. Funktsioonide loend ei ole fikseeritud ja arendajad saavad seda laiendada. Võimalike funktsioonide loendi nägemiseks minge ER-i valemikoostaja funktsioonide paanile.

### <a name="date-and-time-functions"></a>Kuupäeva ja kellaaja funktsioonid

| Funktsioon                                   | Kirjeldus                                                                                                                                                                                                                                                                                                                                                      | Näide                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (kuupäev, kellaaeg, päevad)                   | Lisage määratud kuupäeva ja kellaaja väärtusele määratud päevade arv.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** tagastab kuupäeva ja kellaaja seitsme päeva pärast.                                                                                                                                                                                                                            |
| DATETODATETIME (kuupäev)                      | Teisendage määratud kuupäeva väärtus kuupäeva ja kellaaja väärtuseks.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. "getCurrentDate()')** käib praeguse Dynamics 365 operatsioonide istungi kuupäev, 12/24/2015 **12/24/2015 12:00:00 EL**. Selles näites on **CompInfo** tüübi **Dynamics 365 for Operations / tabel** ER-i andmeallikas, mis viitab tabelile CompanyInfo. |
| NOW ()                                     | Tagastab Dynamics 365 for Operationsi rakenduseserveri praeguse kuupäeva ja kellaaja kuupäeva- ja kellaajaväärtusena.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Tagastab Dynamics 365 for Operationsi rakenduseserveri praeguse kuupäeva kuupäevaväärtusena.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Tagastab kuupäeva väärtuse **null**.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Tagastab kuupäeva ja kellaaja väärtuse **null**.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (kuupäev ja kellaaeg, vorming)          | Teisendage määratud kuupäeva ja kellaaja väärtus määratud vormingus stringiks. (Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), „pp-KK-aaaa”)** tagastab Dynamics 365 for Operationsi rakenduseserveri praeguse kuupäeva, 12/24/2015, kujul **„24-12-2015”** vastavalt määratud kohandatud vormingule.                                                                                                          |
| DATETIMEFORMAT (kuupäev ja kelaaeg, vorming, kultuur) | Teisendage määratud kuupäeva ja kellaaja väärtus määratud vormingus ja [kultuuris](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx) stringiks. (Teavet toetatud vormingute kohta vt jaotistest [standardne](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** tagastab Dynamics 365 for Operationsi rakenduseserveri praeguse kuupäeva, 12/24/2015, kujul **„24.12.2015”** vastavalt valitud saksa kultuurile.                                                                                                             |
| SESSIONTODAY ()                            | Tagastab Dynamics 365 for Operationsi seansi praeguse kuupäeva kuupäevaväärtusena.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Tagastab Dynamics 365 for Operationsi seansi praeguse kuupäeva ja kellaaja kuupäeva- ja kellaajaväärtusena.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (kuupäev, vorming)                  | Annab stringi kujul esitatud kuupäeva, kasutades määratud vormingut.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "pp-KK-aaaa")** tagastab Dynamics 365 for Operationsi rakenduseserveri praeguse kuupäeva, 12/24/2015, kujul **„24-12-2015”** vastavalt määratud kohandatud vormingule.                                                                                                                      |
| DATEFORMAT (kuupäev, vorming, kultuur)         | Teisendage määratud kuupäevaväärtus määratud vormingus ja [kultuuris](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx) stringiks. (Teavet toetatud vormingute kohta vt jaotistest [standardne](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** tagastab Dynamics 365 for Operationsi seansi praeguse kuupäeva, 12/24/2015, kujul **„24.12.2015”** vastavalt valitud saksa kultuurile.                                                                                                                       |

### <a name="list-functions"></a>Loendi funktsioonid

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktsioon</th>
<th>Kirjeldus</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (sisend, pikkus)</td>
<td>Jaotage määratud sisendstring alamstringideks, millest igaühel on määratud pikkus. Tagastab tulemi uue loendina.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> tagastab uue loendi, mis koosneb kahe kirje, mis on saanud <strong>STRINGI</strong> välja. Esimese kirje väli sisaldab teksti <strong>&quot;abc&quot;</strong>, ja teine kirje väli sisaldab teksti <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (loend, number)</td>
<td>Jaotatage määratud loend partiideks, millest igaüks sisaldab määratud kirjete arvu. Tagastab tulemi uue partiide loendina, mis sisaldab järgmisi elemente.
<ul>
<li>Partiid regulaarsete loenditena (komponent <strong>Väärtus</strong>)</li>
<li>Praegune partiinumber (komponent <strong>BatchNumber</strong>)</li>
</ul></td>
<td>Järgmises näites luuakse andmeallikas <strong>Read</strong> kolme kirje kirjeloendina, mis on jaotatud partiideks, millest igaüks sisaldab kuni kahte kirjet. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>See näitab kujundatud vormi paigutust, kui sidemed on <strong>read</strong> andmeallika loomisel XML-vormingus, mis esitab see üksikute keskuste iga partii ja kirjete loomiseks. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>Järgnev on tingitud kujundatud formaat töötab. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (kirje 1 [, kirje 2, ...])</td>
<td>Tagastab uue loendi, mis luuakse määratud argumentidest.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> tagastab tühja kirje, kus väljade loend sisaldab kõiki kirjeloendite <strong>MainData</strong> ja <strong>OtherData</strong> välju.</td>
</tr>
<tr class="even">
<td>LISTJOIN (loend 1, loend 2, ...)</td>
<td>Tagastab ühendatud loendi, mis luuakse määratud argumentide loenditest.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1) tükeldada (&quot;def&quot;, 1))</strong> tagastab kuus kirjete loend, kus üks valdkonnas on <strong>STRINGI</strong> andmetüüp sisaldab üksik.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (loend)</td>
<td>Tagastab väärtuse <strong>TRUE</strong>, kui määratud loend ei sisalda ühtki elementi. Muidu tagastatakse väärtus <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (loend)</td>
<td>Tagastab tühja loendi, kasutades määratud loendit loendi struktuuri allikana.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> tagastab uus tühi loend, mis on sama struktuuriga loendi, mis tagastatakse <strong>jagada</strong> funktsiooni.</td>
</tr>
<tr class="odd">
<td>FIRST (loend)</td>
<td>Tagastab määratud loendi esimese kirje, kui see kirje pole tühi. Muidu ilmneb erand.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (loend)</td>
<td>Tagastab määratud loendi esimese kirje, kui see kirje pole tühi. Muidu tagastatakse kirje <strong>null</strong>.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (loend)</td>
<td>Tagastab loendi, mis sisaldab ainult määratud loendi esimest üksust.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (tee)</td>
<td>Tagastab uue lameloendi, mis kajastab kõiki konkreetsele teele vastavaid üksusi. Tee peab olema määratletud kehtiva andmeallika teena kirjeloendi andmetüübi andmeallika elemendini. Tee stringi, kuupäeva jm andmeelemendini peaks ER-i avaldisekoostajas andma kujundusajal tõrke.</td>
<td>Kui sisestate <strong>tükeldada (&quot;abcdef&quot;, 2)</strong> andmeallikana (DS), <strong>arv (ALLITEMS (DS. Väärtus))</strong> tagastab <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (loend [, avaldis 1, avaldis 2, …])</td>
<td>Tagastab määratud loendi, mis on sorditud vastavalt määratud argumentidele, mida saab määratleda avaldistena.</td>
<td>Kui <strong>Hankija </strong>on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, tagastab<strong> ORDERBY (Vendors, Vendors.'name()')</strong> hankijate loendi, mis on sorditud nimede järgi kasvavas järjestuses.</td>
</tr>
<tr class="even">
<td>REVERSE (loend)</td>
<td>Tagastab määratud loendi vastupidises sortimisjärjestuses.</td>
<td>Kui <strong>Hankija </strong>on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, tagastab <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> hankijate loendi, mis on sorditud nimede järgi kahanevas järjestuses.</td>
</tr>
<tr class="odd">
<td>WHERE (loend, tingimus)</td>
<td>Tagastab määratud loendi, mida on filtreeritud vastavalt määratud tingimusele. Erinevalt funktsioonist <strong>FILTER</strong> rakendatakse määratud tingimus mälus olevale loendile.</td>
<td>Kui <strong>hankija</strong> on konfigureeritud ER andmeallikas, mis viitab tabeli VendTable <strong>kus (müüjad, Vendors.VendGroup = &quot;40&quot;)</strong> tagastab hankijagrupi 40 kuuluvad hankijate nimekirja.</td>
</tr>
<tr class="even">
<td>ENUMERATE (loend)</td>
<td>Tagastab uue loendi, mis koosneb määratud loendi nummerdatud kirjetest ja mis avaldab järgmised elemendid.
<ul>
<li>Määratud loendikirjed regulaarsete loenditena (komponent <strong>Väärtus</strong>)</li>
<li>Praegune kirje indeks (komponent <strong>Number</strong>)</li>
</ul></td>
<td>Järgmises näites on andmeallikas <strong>Nummerdatud</strong> loodud andmeallika <strong>Hankijad</strong> hankijate kirjete nummerdatud loendina, mis viitab tabelile <strong>VendTable</strong>. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Siin on vorm, kus luuakse andmete loomiseks XML-vormingus, mis esitab erinevate hankijate nummerdatud sõlmedena. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>See tuleneb kavandatud formaat töötab. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (loend)</td>
<td>Tagastab määratud loendi kirjete arvu, kui loend pole tühi. Muidu tagastatakse väärtus <strong>0</strong> (null).</td>
<td><strong>ARV (SPLIT (&quot;abcd&quot;, 3))</strong> tagastab <strong>2</strong>, sest selle <strong>jagada</strong> funktsioon loob nimekirja, mis koosneb kahe.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (tee)</td>
<td>Tagastab üht järgmist tüüpi argumentidest loodud kirjete loendi.
<ul>
<li>Mudeli loetelu</li>
<li>Vormingu loetelu</li>
<li>Konteiner</li>
</ul>
Loodud loend koosneb järgmiste väljadega kirjetest.
<ul>
<li>Nimi</li>
<li>Silt</li>
<li>Kirjeldus</li>
</ul>
Väljad Silt ja Kirjeldus tagastatakse käitusaja väärtuste juures põhinevalt vormingu keelesätetest.</td>
<td>Järgmises näites kirjeldatakse andmemudelis kasutusele võetud loetelu. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Järgmine näide:
<ul>
<li>aruandesse andmeallikana sisestatud mudeli loetelu;</li>
<li>mudeliloetelu selle funktsiooni parameetrina kasutamiseks kujundatud ER-i avaldist;</li>
<li>loodud ER-i avaldise abil aruandesse sisestatud kirjeloendi tüübi andmeallikas.</li>
</ul><ph id="t1">
< a href="./media/ger-listoffields-function-in-format-expression.png" ></ph><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> järgmine näide ER vormi elemente, mis on seotud andmeallika kirje tüüp, mis on loodud, kasutades LISTOFFIELDS funktsiooni. <a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>See on kujundatud vormi täitmise tulemusena. <a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Märkus:</strong> tõlgitud tekst sildid ja kirjeldused on asustatud ER formaadis väljund vastavalt konfigureeritud vanema faili ja kausta formaadis elemendid keelesätteid.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (loend, välja nimi, eraldaja)</td>
<td>Tagastab loendist välja liitväärtuste stringi valitud eraldajaga.</td>
<td>Kui sisestasite andmeallikana DS väärtuse SPLIT("abc" , 1), tagastab avaldis STRINGJOIN (DS, DS.Value, ":") tulemi „a:b:c”</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (loend, piirväärtus, piirallikas)</td>
<td>Tükeldab loendi uueks alamloenditest koosnevaks loendiks ja tagastab tulemuse kirjeloendi sisus. Piirväärtuse parameeter määrab algse loendi tükeldamise piirväärtuse. Piirallika parameeter määrab etapi, milles kogusumma suureneb. Piirangut ei rakendata antud loendi üksikule üksusele, kui piirallikas ületab määratud piirangut.</td>
<td>Järgmises näites kirjeldatakse näidisvormingut, kasutades andmeallikaid. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>See on tulemus vormi täitmine, mis esitab kindla nimekirja, kauba. <a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>Järgmine näide samalaadne täpsustas esitada kaupade nimekirja, töölehed, kui ühe partii peab sisaldama kaupade kogukaal, mis ei tohiks ületada piiri 9. <a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>See on korrigeeritud kujul täitmise tulemustest. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Märkus:</strong> piirmäära ei kohaldata päritolu loendi viimasele üksusele väärtus (11) selle piiri allikas (kaal) on üle kindlaks määratud piirmäära (9). Kasutage kas funktsiooni <strong>KUS</strong> või vastava vorminguelemendi avaldist <strong>Lubatud</strong>, et alamloendeid aruande loomisel vajaduse korral eirata (jätta vahele).</td>
</tr>
<tr class="odd">
<td>FILTER (loend, tingimus)</td>
<td>Tagastab antud loendi, mida on filtreeritud määratud tingimuse jaoks, muutes päringut. Erinevalt funktsioonist <strong>KUS</strong> rakendatakse määratud tingimust andmebaasi tasemel kõigile tabelikirje tüüpi ER-i andmeallikatele.</td>
<td>FILTER (müüjad, Vendors.VendGroup = &quot;40&quot;) tagastab ainult need hankijad, hankijate grupi "40" loetelu kui <strong>hankija</strong> konfigureeritakse ER andmeallikana, viidates selle <strong>VendTable</strong> tabel</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loogilised funktsioonid

| Funktsioon                                                                                | Kirjeldus                                                                                                                                                                                                                                                                     | Näide                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| JUHUL (väljend, variant 1, kaasa 1 \[, 2. valik, kaasa 2\] ... \[, vaikimisi tulemus\]) | Arvutab määratud avaldise väärtuse määratud teise suvandi suhtes. Tagastab suvandi tulemi, mis on võrdne avaldise väärtusega. Muidu tagastatakse valikuliselt sisestatud vaiketulem (viimane parameeter, millele ei eelne suvand). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** tagastab stringi **"WINTER"**, kui praeguse Dynamics 365 for Operations seansi kuupäev jääb vahemikku oktoober kuni detsember. Muidu tagastatakse tühi string. |
| IF (tingimus, väärtus 1, väärtus 2)                                                        | Tagastab määratud väärtuse 1, kui antud tingimus on täidetud. Muul juhul tagastab väärtuse 2. Kui 1 ja 2 on kirjete või kirjete loendid, tulemus on ainult need väljad, mis on olemas mõlemas nimekirjas.                                                                     | **IF (1=2, "condition is met", "condition is not met")** tagastab stringi **"condition is not met"**.                                                                                                                                                      |
| NOT (tingimus)                                                                         | Tagastab määratud tingimuse tühistatud loogilise väärtuse.                                                                                                                                                                                                                   | **NOT (TRUE)** tagastab väärtuse **FALSE**.                                                                                                                                                                                                                            |
| JA (tingimusel, et 1\[, tingimusel, et 2... \])                                                 | Tagastab väärtuse **TRUE**, kui *kõik *määratud tingimused on tõesed. Muidu tagastatakse väärtus **FALSE**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** tagastab väärtuse **TRUE**. **AND (1=2, "a"="a")** tagastab väärtuse **FALSE**.                                                                                                                                                                           |
| VÕI (tingimusel, et 1\[, tingimusel, et 2... \])                                                  | Tagastab väärtuse **FALSE**, kui *kõik *määratud tingimused on väärad. Tagastab väärtuse **TRUE**, kui *mõni *määratud tingimustest on tõene.                                                                                                                                                                 | **OR (1=2, "a"="a")** tagastab väärtuse **TRUE**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Matemaatilised funktsioonid

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktsioon</th>
<th>Kirjeldus</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (number)</td>
<td>Tagastab määratud arvu (arv ilma märgita) absoluutväärtuse.</td>
<td><strong>ABS (–1)</strong> tagastab väärtuse <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (number, aste)</td>
<td>Tagastab määratud astmele määratud positiivse numbri tõstmise tulemi.</td>
<td><strong>POWER (10, 2)</strong> tagastab väärtuse <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (string, kümnendkohaeraldaja, arvu rühmitamise eraldaja)</td>
<td>Teisendab määratud stringi numbriks. Määratud sümbolit kasutatakse kümnendarvu täisarvu ja murdosa eraldamiseks ja kasutatakse ka määratud tuhandete erldajat.</td>
<td><strong>NUMBERVALUE (&quot;1 234,56&quot;, &quot;,&quot;, &quot;&quot;)</strong> tagastab väärtuse <strong>1234.56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (string)</td>
<td>Teisendab määratud stringi numbriks. Komasid ja punkte (.), loetakse komakohtade eraldajateks ning miinusmärki (–) kasutatakse negatiivse märgina. Ilmneb erand, kui määratud stringis on muid mittenumbrilisi märke.</td>
<td><strong>VÄÄRTUS (&quot;1 234,56&quot;)</strong> põhjustab erandi.</td>
</tr>
<tr class="odd">
<td>ROUND (number, kümnendkohad)</td>
<td>Tagastab määratud numbri, mis on ümardatud määratud komakohtadeni.
<ul>
<li>Kui määratud kümnendkohtade väärtus on suurem kui 0 (null), ümardatakse määratud number määratud komakohtadeni.</li>
<li>Kui määratud kümnendkohtade väärtus on 0 (null), ümardatakse määratud number lähima täisarvuni.</li>
<li>Kui määratud kümnendkohtade väärtus on väiksem kui 0 (null), ümardatakse määratud number komakohast vasakule.</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> ümardab kahe komakohani ja tagastab väärtuse <strong>1200,77</strong>. <strong>ROUND (1200,767, –3)</strong> ümardab lähima 1000 kordseni ja tagastab väärtuse <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (number, kümnendkohad)</td>
<td>Tagastab määratud numbri, mis on ümardatud allapoole (nulli poole) määratud komakohtadeni. <strong>Märkus.</strong> See funktsioon toimib nagu <strong>ROUND</strong>, kuid see ümardab alati määratud numbrit allapoole.</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> ümardab allapoole kahe komakohani ja tagastab väärtuse <strong>1200,76</strong>. <strong>ROUNDDOWN (1700.767, -3)</strong> ümardab allapoole lähima 1000 kordseni ja tagastab väärtuse <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (number, kümnendkohad)</td>
<td>Tagastab määratud numbri, mis on ümardatud ülespoole (nullist eemale) määratud komakohtadeni. <strong>Märkus.</strong> See funktsioon toimib nagu <strong>ROUND</strong>, kuid see ümardab alati määratud numbrit ülespoole.</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> ümardab ülespoole kahe komakohani ja tagastab väärtuse <strong>1200,77</strong>. <strong>ROUNDUP (1200.767, -3)</strong> ümardab ülespoole lähima 1000 kordseni ja tagastab väärtuse <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

### <a name="record-functions"></a>Kirje funktsioonid

| Funktsioon             | Kirjeldus                                                                                                                                                                                                                                     | Näide                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (loend) | Tagastab kirje **null**, millel on sama struktuur kui määratud kirjeloendil või kirjel. **Märkus. **See funktsioon on aegunud. Kasutage selle asemel funktsiooni **EMPTYRECORD**.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille tagastab funktsioon **SPLIT**. |
| EMPTYRECORD (kirje) | Tagastab kirje **null**, millel on sama struktuur kui määratud kirjeloendil või kirjel. **Märkus:** A **null** kirje on kirje, kus kõik väljad on tühi väärtus (**0**\[0\] numbrid, tühi string stringid ja nii edasi). | **EMPTYRECORD (SPLIT ("abc", 1))** tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille tagastab funktsioon **SPLIT**.   |

### <a name="text-functions"></a>Tekstifunktsioonid

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktsioon</th>
<th>Kirjeldus</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (string)</td>
<td>Tagastab määratud stringi, mis on teisendatud suurtäheliseks.</td>
<td><strong>ÜLEMINE (&quot;proovi&quot;)</strong> tagastab <strong>&quot;proovi&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (string)</td>
<td>Tagastab määratud stringi, mis on teisendatud väiketäheliseks.</td>
<td><strong>MADALAM (&quot;proovi&quot;)</strong> tagastab <strong>&quot;proovi&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (string, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringi algusest.</td>
<td><strong>VASAKULE (&quot;proovi&quot;, 3)</strong> tagastab <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (string, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringi lõpust.</td>
<td><strong>PAREMALE (&quot;proovi&quot;, 3)</strong> tagastab <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (string, alguspositsioon, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringist, alustades määratust kohas.</td>
<td><strong>MID (&quot;proovi&quot;, 2, 3)</strong> tagastab <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (string)</td>
<td>Tagastab tähemärkide arvu määratud stringis.</td>
<td><strong>LEN (&quot;proovi&quot;)</strong> tagastab <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (number)</td>
<td>Tagastab tähemärke stringi, millele viitab määratud Unicode'i number.</td>
<td><strong>CHAR (255)</strong> tagastab <strong>&quot;ÿ&quot;</strong>. <strong>Märkus.</strong> Tagastatud string sõltub failivormingu ülemelemendis valitud kodeeringust. Toetatud kodeeringute loendi leiate teemast <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodeeringuklass</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (string 1 [, string 2, …])</td>
<td>Tagastab kõik määratud tekstistringid, mis on ühendatud üheks stringiks.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> tagastab <strong>&quot;abcdef&quot;</strong>. <strong>Märkus:</strong> väljend <strong>&quot;abc&quot;&amp;&quot;def&quot;</strong> ka <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (string, muster, asendus)</td>
<td>Tagastab määratud stringi, mille puhul kõik määratud mustri stringi märgid asendatakse määratud asendusstringis olevate vastavas kohas olevate tähemärkidega.</td>
<td><strong>TÕLGI (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> asendab muster <strong>&quot;cd&quot;</strong> string <strong>&quot;GH&quot;</strong> ja <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (string, muster, asendus, regulaaravaldise lipp)</td>
<td>Kui määratud regulaaravaldise lipp on <strong>tõene</strong>, tagastatakse määratud string, mida on muudetud, rakendades regulaaravaldist, mis on määratud selle funktsiooni musterargumendina. Seda avaldist kasutatakse asendatavate tähemärkide otsimiseks. Määratud asendusargumendi tähemärke kasutatakse leitud tähemärkide asendamiseks. Kui määratud regulaaravaldise lipp on <strong>väär</strong>, toimib see funktsioon nagu väärtus <strong>TRANSLATE</strong>.</td>
<td>  <strong>ASENDADA (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, tõsi)</strong> kehtib regulaaravaldise, mis eemaldab kõik arvväärtus sümbolid ja tagastab <strong>&quot;19234564971&quot;</strong>. <strong>ASENDADA (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> asendab muster <strong>&quot;cd&quot;</strong> string <strong>&quot;GH&quot;</strong> ja <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (sisend)</td>
<td>Tagastab määratud sisendi, mis on teisendatud tekstistringiks, mis on vormindatud vastavalt praeguse Dynamics 365 for Operationsi eksemplari serverilokaadi sätetele. <strong>Tõelist</strong> tüüpi väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.</td>
<td>Kui Dynamics 365 toimingute astme serveri asukoha määratletakse <strong>EN-US</strong>, <strong>teksti (nüüd ())</strong> tagastab praeguse Dynamics 365 operatsioonide istungi kuupäev, 12/17/2015 tekstistring nagu <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEKST (1/3)</strong> tagastab <strong>&quot;0,33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (string 1, string 2[, string 3, ...])</td>
<td>Tagastab määratud stringi, mida vormindatakse, asendades kõik argumendi <strong>%N</strong> esinemised argumendiga <em>n</em>. Argumendid on stringid. Kui parameeter ei ole argument, tagastatakse parameeter <strong>&quot;%N&quot;</strong> string. <strong>Tõelist</strong> tüüpi väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.</td>
<td>Selles näites tagastab andmeallikas <strong>PaymentModel</strong> komponendi <strong>Klient</strong> kaudu kliendikirjete loendi ja välja <strong>ProcessingDate</strong> kaudu töötlemise kuupäeva väärtuse. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>Eesmärk on luua elektroonilise faili valitud klientide, ER-vormingus <strong>PaymentModel</strong> on valitud andmeallika ja kontrollib menetluse kulgemine. Lõppkasutajatele tehakse erand, kui valitud klient on peatatud kuupäeval, millal aruannet töödeldakse. Seda tüüpi töötlemise juhtimiseks koostatud valem saab kasutada järgmisi ressursse.
<ul>
<li>Dynamics 365 for Operationsi silt SYS70894, millel on järgmine tekst.
<ul>
<li><strong>EN-US keeles:</strong>&quot;pole midagi printida&quot;</li>
<li><strong>DE keeles:</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operationsi silt SYS18389, millel on järgmine tekst.
<ul>
<li><strong>EN-US keeles:</strong>&quot;lõpetatakse kliendi %1% 2.&quot;</li>
<li><strong>DE keeles:</strong>&quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Siin on valem, mis võib olla ette: formaat (CONCATENATE (@&quot;SYS70894&quot;,&quot;. &quot;@&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (mudel. ProcessingDate, &quot;d&quot;)) kui aruanne on selle <strong>Litware jaetarbijale</strong> 17 Detsember 2015 aastal on <strong>EN-US</strong> kultuuri ja <strong>EN-US</strong> keel, see valem tagastab järgmine tekst, mida saab esitada erand sõnum lõppkasutajale: &quot;pole midagi printida. Kliendi Litware jaemüügi lõppu 12/17/2015.&quot; Kui aruandes on selle<strong> Litware jaetarbijale</strong> 17 Detsember 2015 ja selle <strong>DE</strong> kultuuri ja <strong>DE</strong> keel, see valem tagastab järgmine tekst, mis kasutab erinevat kuupäeva vormingut: &quot;Nichts zu drucken. Debitor 'Litware jaemüügi' wird für 17.12.2015 gesperrt.&quot; <strong>Märkus. </strong>Siltidele mõeldud ER-i valemites rakendatakse järgmist süntaksit.
<ul>
<li><strong>Siltide Dynamics 365 toimingute ressursside:</strong> <strong>@&quot;X&quot;</strong>, kus X on sildi ID rakendusobjektide puu (AOT)</li>
<li><strong>Etiketid, millel asuvad ER koosseisus:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, kus X on sildi ID ER konfiguratsiooni</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (number, vorming)</td>
<td>Tagastab määratud vormingus määratud numbri stringiesituse. (Toetatud vormingute kohta leiate teemast <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standard</a> ja <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">kohandatud</a>.) See funktsioon on sisse sõidetud raames määrab kultuur, mida kasutatakse arvude vormindamiseks.</td>
<td>EN-US kultuuri-, <strong>NUMBERFORMAT (0,45, &quot;p&quot;)</strong> tagastab <strong>&quot;45,00%&quot;</strong>. <strong>NUMBERFORMAT (10,45, &quot;#&quot;)</strong> tagastab <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (number, keel, valuuta, prindi valuuta nime lipp, kümnendkohad)</td>
<td>Tagastab sõnadena kirjutatud (tekstistringiks teisendatud) numbri määratud keeles. Keelekood ei ole kohustuslik: kui see on määratletud tühja stringina, kasutatakse selle asemel käitatava konteksti keelekoodi (määratletud kausta või faili loomiseks). Valuutakood ei ole kohustuslik. Kui see on määratletud tühja stringina, kasutatakse ettevõtte valuutat. Pange tähele, et parameetreid <strong>Prindi valuuta nimi</strong> ja <strong>Kümnendkohad</strong> analüüsitakse ainult järgmiste keelekoodide puhul: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Pange tähele, et parameetrit <strong>Prindi valuuta nimi</strong> analüüsitakse ainult nende Dynamics 365 for Operationsi ettevõtete puhul, mille riigikontekst toetab valuuta käänamist.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, vale, 2) tagastab "Tuhande kaks saja kolmekümne neljandal ja 56" NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, vale, 0) tagastab "Sto dwadzieścia" NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;euro&quot;, tõsi, 2) tagastab "Сто двадцать евро 21 евроцент"</td>
</tr>
<tr class="odd">
<td>PADLEFT (string, pikkus, täidismärgid)</td>
<td>Tagastab määratud pikkusega stringi, milles praeguse stringi algusele on lisatud määratud märkidest koosnevad täidismärgid.</td>
<td>PADLEFT („1234”, 10, „ ”) tagastab tekstistringi „      1234”</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Andmete kogumise funktsioonid

Funktsioon

Kirjeldus

Näide

FORMATELEMENTNAME ()

Toob praeguse vormingu elemendi nime. Tagastab tühja stringi, kui praeguste failide lipp **Kogu väljundi üksikasjad** on välja lülitatud.

Lisateavet nende funktsioonide kasutamise kohta vaadake tegevusjuhisest **ER-i loendamise ja liitmise vormingu väljundi kasutusandmed** (äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa).

SUMIFS (peamised liitmist, kriteeriumid range1 string, kriteeriumid väärtus1 string string \[, kriteeriumid range2 string, kriteeriumid väärtus2 string,... \])

Tagastab XML-i sõlmede väärtuste summa (koos võtmena määratletud nimega), mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimusi (vahemiku ja väärtuse paarid). Tagastab nullväärtuse, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

SUMIF (liitmise võtmestring, kriteeriumivahemiku string, kriteeriumiväärtuse string)

Tagastab XML-i sõlmede väärtuste summa (koos võtmena määratletud nimega), mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimuse (vahemik ja väärtus). Tagastab nullväärtuse, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

COUNTIFS (kriteeriumid range1 string, kriteeriumid väärtus1 string \[, kriteeriumid range2 string, kriteeriumid väärtus2 string,... \])

Tagastab XML-i sõlmede arvu, mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimusi (vahemiku ja väärtuse paarid). Tagastab nullväärtuse, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

COUNTIF (kriteeriumivahemiku string, kriteeriumiväärtuse string)

Tagastab XML-i sõlmede arvu, mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimuse (vahemik ja väärtus). Tagastab nullväärtuse, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

COLLECTEDLIST (kriteeriumid range1 string, kriteeriumid väärtus1 string \[, kriteeriumid range2 string, kriteeriumid väärtus2 string,... \])

Tagastab XML-i sõlmede väärtuste loendi, mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimusi (vahemiku ja väärtuse paarid). Tagastab tühja loendi, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

### <a name="other-business-domainspecific-functions"></a>Muud (ettevõtte domeenipõhised) funktsioonid

| Funktsioon                                                                         | Kirjeldus                                                                                                                                                                                                                                                        | Näide                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (summa, lähtekoha valuuta, sihtkoha valuuta, kuupäev, ettevõte)        | Teisendab määratud rahasumma lähtekoha valuutast sihtkoha valuutaks, kasutades määratud kuupäeval määratud Dynamics 365 for Operationsi ettevõtte sätteid.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** tagastab ühe euroga võrdse väärtuse USA dollarites praeguse seansi kuupäeval DEMF-i ettevõtte sätete alusel.                                                                                                                                  |
| ROUNDAMOUNT (number, kümnendkohad, ümardamisreegel)                                       | Ümardab määratus summa vastavalt määratud ümardamisreeglile ja määratud kümnendkohtade arvule. **Märkus.** Ümardamisreegel peab olema määratud Dynamics 365 for Operationsi nummerdamise **RoundOffType** väärtusena.                          | Kui on **mudel. Ümardamine** parameeter on seatud *** allapoole ***, **ROUNDAMOUNT (1000.787, 2, mudel. Ümardamine)** tagastab väärtuse **1000.78**. Kui parameeter **model.RoundOff** on seatud väärtusele **Normaalne** või **Ülespoole ümardamine**, tagastab **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** väärtuse **1000,79**. |
| CURCredRef (arvud)                                                              | Tagastab kreeditori viite määratud arve numbri arvude alusel.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** tagastab väärtuse **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (numbrit)                                                                 | Tagastab kreeditori viite MOD97 avaldisena määratud arve numbri arvude alusel.                                                                                                                                                            | **MOD\_97 ("VEND 200002")** tagastab **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (arvud)                                                              | Tagastab ISO kreeditori viite määratud arve numbri arvude ja tähestikus olevate sümbolite alusel. **Märkus. **ISO-ga ühildumatute sümbolite tähestikust eemaldamiseks tuleb sisendparameeter enne sellele funktsioonile edastamist tõlkida. | **ISOCredRef ("VEND-200002")** tagastab väärtuse **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (string, number)                                  | Hankige täiendav finantsdimensiooni ID. Dimensioonid on esindatud selles stringis komadega eraldatud ID-dena. Numbrid määratlevad taotletud dimensioonide seeriakoodi selles stringis.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA, BB, CC, DD, EE, FF, GG, HH", 3) tagastab "CC"                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Tagastab praegu logitud ettevõtte koodi.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_panga\_MOD\_10 (numbrit)                                                       | Tagastab kreeditori viite MOD10 avaldisena antud arve numbri numbrite alusel.                                                                                                                                                                      | CH\_panga\_MOD\_10 ("VEND 200002") tagastab 3                                                                                                                                                                                                                                                                   |
| FA\_SUM (fikseeritud vara kood, mudel tähis, alguskuupäev, lõppkuupäev)               | Tagastab ettevalmistatud andmekonteineri põhivarasummadega perioodi kohta.                                                                                                                                                                                         | FA\_("COMP-000001", "Vool", Date1, kuupäev2) summa tagastab ettevalmistatud andmed mahuti põhivara "COMP-000001" väärtusmudeliga "Voolu" jooksul Date1 kuni kuupäev2.                                                                                                                        |
| FA\_SALDOGA (põhivara kood, mudel tähis, aruandeaastaga, Narva mnt) | Tagastab ettevalmistatud andmekonteineri põhivarasaldodega. Aruandlusaasta peab olema määratud Dynamics 365 for Operationsi nummerduse **AssetYear** väärtusena.                                                                                           | FA\_summa ("COMP-000001", "Vool", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) tagastab ettevalmistatud andmed mahuti põhivara saldode "COMP-000001" väärtusmudeliga "Voolu" praeguse 365 operatsioonide istungi kuupäeva.                                                                |

### <a name="functions-list-extension"></a>Funktsioonide loendi laiend

ER laseb laiendada nende funktsioonide loendit, mida kasutatakse ER-i avaldistes. Nõutavad on mõned projekteerimise panused. Üksikasjalikuma teabe saamiseks vt jaotist [Elektroonilise aruandluse funktsioonide loendi laiendamine](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Vt ka
--------

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) funktsioonide loendi laiendamine](general-electronic-reporting-formulas-list-extension.md)


