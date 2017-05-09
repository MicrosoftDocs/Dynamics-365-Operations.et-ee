---
title: Valemikoostaja elektroonilises aruandluses
description: "Selles teemas selgitatakse, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat. ER-is kindla elektroonilise dokumendi vormingu koostamisel saate kasutada Microsoft Exceli sarnaseid valemeid andmete teisendamiseks, et vastata selle dokumendi täitmise ja vormindamise nõuetele. Toetatakse erinevat tüüpi funktsioone: tekst, kuupäev ja kellaaeg, matemaatiline loogika, teave, andmetüübi teisendamine ja muud (ettevõtte domeenipõhised funktsioonid)."
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

[!include[banner](../includes/banner.md)]


Selles teemas selgitatakse, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat. ER-is kindla elektroonilise dokumendi vormingu koostamisel saate kasutada Microsoft Exceli sarnaseid valemeid andmete teisendamiseks, et vastata selle dokumendi täitmise ja vormindamise nõuetele. Toetatakse erinevat tüüpi funktsioone: tekst, kuupäev ja kellaaeg, matemaatiline loogika, teave, andmetüübi teisendamine ja muud (ettevõtte domeenipõhised funktsioonid).

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

Järgmisel joonisel on seda tüüpi avaldise kujundus. Selles näites annab avaldis Dynamics 365 for Operationsi tabeli **Intrastat** välja **Intrastat.AmountMST** väärtuse pärast selle väärtuse ümardamist kahe kümnendkohani. [![picture-expression-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) Järgmisel joonisel on näidatud, kuidas saab seda tüüpi avaldist kasutada. Selles näites on koostatud avaldise tulem lisatud andmemudeli **Maksu aruandluse mudel** komponendile **Transaction.InvoicedAmount**. [![picture-expression-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) Käitusajal ümardab koostatud valem (**ROUND (Intrastat.AmountMST, 2)**) välja **AmountMST** väärtuse tabeli **Intrastat** iga kirje puhul kahe kümnendkohani ja sisestab ümardatud väärtuse andmemudeli **Maksu aruandlus** komponenti **Transaction.InvoicedAmount**.

### <a name="data-formatting"></a>Andmete vormindamine

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis vormindab andmeid, mis saadakse andmeallikatest, nii et andmeid saab saata elektroonilise dokumendi loomise osana. Kui teil on vorming, mida tuleb rakendada tüüpilise reeglina, mida tuleb vormingu puhul taaskasutada, saate kasutada seda vormingut ühe korra vormingu konfiguratsioonis nimega teisendusena, millel on vormindamisavaldis. Selle nimelise teisenduse saab siduda paljude vormingu komponentidega, mille väljund peab olema vormindatud vastavalt loodud avaldisele. Järgmisel joonisel on seda tüüpi teisenduse kujundus. Selles näites võtab teisendus **TrimmedString** andmetüübi **String** sissetulevad andmed ning kärbib stringi väärtuse andmisel algus- ja lõputühikud. [![picture-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) Järgmine joonis näitab, kuidas seda tüüpi teisendust saab kasutada. Selles näites viitavad mitu vormingu komponenti, mis saadavad teksti käitusajal väljundina elektroonilise dokumendi loomisel, teisendusele **TrimmedString** nime järgi. [![picture-transformation-usage](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Kui vormingu komponendid viitavad teisendusele **TrimmedString**(näiteks komponendi **partyName** puhul eelmises näites), saadab see teksti väljundina loodavasse dokumenti. Tekst ei sisalda algus- ega lõputühikuid. Kui teil on vorming, mida tuleb rakendada eraldi, saab selle kasutusele võtta kindla vormingu komponendi sidumise üksiku avaldisena. Järgmisel joonisel on seda tüüpi avaldis. Selles näites on vormingu komponent **partyType** seotud andmeallikaga avaldise kaudu, mis teisendab sissetulevad andmeallika andmed väljalt **Model.Company.RegistrationType** suurtäheliseks tekstiks ja saadab selle teksti väljundina elektroonilisse dokumenti. [![picture-binding-with-formula](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Protsessi voo juhtimine

ER-i valemikoostajat saab kasutada dokumentide loomise protsessivoo juhtimiseks kasutatavate avaldiste määratlemiseks. Saate:

-   Määratlege tingimused, mis määravad, millal tuleb dokumendi loomise protsess peatada.
-   Määrake avaldised, mis loovad lõppkasutajale sõnumeid peatatud protsesside kohta või heidavad käivitamislogi sõnumeid aruande loomise protsessi jätkamise kohta.
-   Määrake loodavate dokumentide failinimed ja juhtige nende loomise tingimusi.

Iga protsessi voo juhtimise reegel on koostatud üksiku kinnitusena. Järgmisel joonisel on seda tüüpi kinnitus. Siin on selles näites oleva konfiguratsiooni selgitus.

-   Kinnitamine on hinnatud, kui loodavas XML-failis luuakse **INSTAT**-sõlm.
-   Kui kannete loend on tühi, lõpetab kinnitamine käivitamisprotsessi ja tagastab väärtuse **FALSE**.
-   Kinnitamine annab tõrketeate, mis sisaldab SYS70894 teksti kasutaja eelistatud keeles.

[![picture-validation](./media/picture-validation.jpg)](./media/picture-validation.jpg) ER-i valemi koostajat saab kasutada ka failinime määramiseks loodavale elektroonilisele dokumendile ja faili loomise protsessi juhtimiseks. Järgmisel joonisel on seda tüüpi protsessi voo juhtimise kujundus. Siin on selles näites oleva konfiguratsiooni selgitus.

-   Andmeallika **model.Intrastat** kirjete loend on jagatud partiideks, millest iga sisaldab kuni 1000 kirjet.
-   Väljund loob zip-faili, mis sisaldab ühte XML-vormingus faili iga loodud partii kohta.
-   Avaldis tagastab failinime loodavatele elektroonilistele dokumentidele, liites faili nime ja laiendi. Teise partii ja kõikide järgnevate partiide puhul sisaldab faili nimi järelliitena partii ID-d.
-   Avaldis lubab (andes vatuseks väärtuse **TRUE**) faili loomise protsessi partiidele, mis sisaldavad vähemalt ühte kirjet.

[![picture-file-control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Põhisüntaks

ER-i avaldised võivad sisaldada mõnd või kõiki järgmistest elementidest.

-   Konstandid
-   Operaatorid
-   Viited
-   Teed
-   Funktsioonid

#### <a name="constants"></a>Konstandid

Avaldiste koostamisel saate kasutada tekstilisi ja arvulisi konstante (väärtused, mida ei arvutata). Näiteks avaldis **VALUE („100”) + 20 **kasutab arvulist konstanti 20 ja stringi konstanti 100 ning tagastab arvulise väärtuse **120**. ER-i valemikoostaja toetab paoseeriaid, mis tähendab, et saate määrata avaldise stringi, mida tuleb teisiti käsitleda. Näiteks avaldis **Lev Tolstoi „„Sõda ja rahu”” 1. osa** tagastab tekstistringi **Lev Tolstoi „Sõda ja rahu” 1. osa**.

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

Liitavaldise osade arvutamise järjekord on oluline. Näiteks avaldise**1 + 4 / 2** tulemid erinevad olenevalt sellest, kas esimesena tehakse liitmis- või jagamistoiming. Saate kasutada sulge, et selgelt määratleda, kuidas avaldise väärtust leida. Näiteks näitamaks, et esimesena tuleb teha liitmistoiming, saate muuta eelnevat avaldis järgmiselt: **(1 + 4) / 2**. Kui avaldise tehted ei ole selgelt määratletud, põhineb järjekord vaikimisi järjestusel, mis on määratud toetatud tehtemärkidele. Järgmistes tabelites on tehted ja igale tehtele määratud järjestus. Kõrgema prioriteediga tehted (nt 7) arvutatakse enne madalama prioriteediga tehteid (nt 1).

| Tehtejärjestus | Operaatorid      | Süntaks                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Grupeerimine       | ( … )                                                    |
| 6          | Liikme juurdepääs  | … . …                                                    |
| 5          | Funktsioonikutse  | … ( … )                                                  |
| 4          | Korrutamine | … \* … … / …                                             |
| 3          | Täiend       | … + … … - …                                              |
| 2          | Võrdlus     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Lahutamine     | … , …                                                    |

Samal real olevatel tehetel on võrdne prioriteet. Kui avaldis sisaldab mitut sellist tehet, arvutatakse avaldist vasakult paremale. Näiteks avaldis **1 + 6 / 2 \* 3 &gt; 5** tagastab väärtuse **tõene**. Soovitame kasutada sulge näitamaks selgelt avaldise arvutamise soovitud järjestust, et avaldisi oleks lihtsam lugeda ja hallata.

#### <a name="references"></a>Viited

Kõiki praeguse ER-i komponendi (mudel või vorming) andmeallikaid, mis on avalduse koostamise ajal saadaval, saab kasutada nimega viidetena. Näiteks praegune ER-i andmemudel sisaldab andmeallikat **ReportingDate**, mis tagastab andmetüübi **DATETIME** väärtuse. Loodavas dokumendis väärtuse õigesti vormindamiseks saate viidata avaldises andmeallikale järgmiselt: **DATETIMEFORMAT (ReportingDate, "pp-KK-aaaa")** Kõikidele viidatava andmeallika nimes olevatele tähemärkidele, mis ei kuulu tähestikku, peab eelnema ühekordne jutumärk ('). Kui viidatava andmeallika nimi sisaldab vähemalt ühte sümbolit, mis ei kuulu tähestikku (nt kirjavahemärgid või muu kirjalik sümbol), tuleb nimi panna ühekordsetesse jutumärkidesse. Järgmisena on toodud mõned näited.

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
| DATETODATETIME (kuupäev)                      | Teisendage määratud kuupäeva väärtus kuupäeva ja kellaaja väärtuseks.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. 'getCurrentDate()')** tagastab Dynamics 365 for Operationsi seansi praeguse kuupäeva, 12/24/2015 kujul **12/24/2015 12:00:00**. Selles näites on **CompInfo** tüübi **Dynamics 365 for Operations / tabel** ER-i andmeallikas, mis viitab tabelile CompanyInfo. |
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
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> tagastab uue loendi, mis koosneb kahest kirjest, millel on väli <strong>STRING</strong>. Esimese kirje väli sisaldab teksti <strong>&quot;abc&quot;</strong> ja teise kirje väli sisaldab teksti <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (loend, number)</td>
<td>Jaotatage määratud loend partiideks, millest igaüks sisaldab määratud kirjete arvu. Tagastab tulemi uue partiide loendina, mis sisaldab järgmisi elemente.
<ul>
<li>Partiid regulaarsete loenditena (komponent <strong>Väärtus</strong>)</li>
<li>Praegune partiinumber (komponent <strong>BatchNumber</strong>)</li>
</ul></td>
<td>Järgmises näites luuakse andmeallikas <strong>Read</strong> kolme kirje kirjeloendina, mis on jaotatud partiideks, millest igaüks sisaldab kuni kahte kirjet. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> Siin on koostatud vormi paigutus, kus luuakse andmeallika <strong>Read</strong> sidemed, et luua XML-vormingus väljund, mis esitab üksikuid sõlmi igale partiile ja selles olevale kirjele. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> Siin on kujundatud vormingu käitamise tulem. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (kirje 1 [, kirje 2, ...])</td>
<td>Tagastab uue loendi, mis luuakse määratud argumentidest.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> tagastab tühja kirje, kus väljade loend sisaldab kõiki kirjeloendite <strong>MainData</strong> ja <strong>OtherData</strong> välju.</td>
</tr>
<tr class="even">
<td>LISTJOIN (loend 1, loend 2, ...)</td>
<td>Tagastab ühendatud loendi, mis luuakse määratud argumentide loenditest.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> tagastab kuue kirje loendi, kus andmetüübi <strong>STRING</strong> üks väli sisaldab üksikuid tähti.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (loend)</td>
<td>Tagastab väärtuse <strong>TRUE</strong>, kui määratud loend ei sisalda ühtki elementi. Muidu tagastatakse väärtus <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (loend)</td>
<td>Tagastab tühja loendi, kasutades määratud loendit loendi struktuuri allikana.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> tagastab uue tühja loendi, millel on sama struktuur nagu loendil, mille tagastab funktsioon <strong>SPLIT</strong>.</td>
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
<td>Kui sisestate andmeallikaks <strong>SPLIT(&quot;abcdef&quot; , 2)</strong>, tagastab <strong>COUNT( ALLITEMS (DS.Value))</strong> väärtuse <strong>3</strong>.</td>
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
<td>Kui <strong>Hankija</strong> on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, tagastab <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> hankijate loendi, mis kuulub hankijate gruppi 40.</td>
</tr>
<tr class="even">
<td>ENUMERATE (loend)</td>
<td>Tagastab uue loendi, mis koosneb määratud loendi nummerdatud kirjetest ja mis avaldab järgmised elemendid.
<ul>
<li>Määratud loendikirjed regulaarsete loenditena (komponent <strong>Väärtus</strong>)</li>
<li>Praegune kirje indeks (komponent <strong>Number</strong>)</li>
</ul></td>
<td>Järgmises näites on andmeallikas <strong>Nummerdatud</strong> loodud andmeallika <strong>Hankijad</strong> hankijate kirjete nummerdatud loendina, mis viitab tabelile <strong>VendTable</strong>. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Siin on vorming, kus luuakse andmete sidumised, et luua XML-vormingus väljund, mis esitab üksikuid hankijaid nummerdatud sõlmedena. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> Siin on kujundatud vormingu käitamise tulem. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (loend)</td>
<td>Tagastab määratud loendi kirjete arvu, kui loend pole tühi. Muidu tagastatakse väärtus <strong>0</strong> (null).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> tagastab väärtuse <strong>2</strong>, sest funktsioon <strong>SPLIT</strong> loob loendi, mis koosneb kahest kirjest.</td>
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
<td>Järgmises näites kirjeldatakse andmemudelis kasutusele võetud loetelu. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Järgmises näites on toodud:
<ul>
<li>aruandesse andmeallikana sisestatud mudeli loetelu;</li>
<li>mudeliloetelu selle funktsiooni parameetrina kasutamiseks kujundatud ER-i avaldist;</li>
<li>loodud ER-i avaldise abil aruandesse sisestatud kirjeloendi tüübi andmeallikas.</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> Järgmises näites on toodud ER-vorming elemendid, mis on seotud funktsiooniga LISTOFFIELDS loodud kirjeloendi tüübi andmeallikaga.<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>See on kujundatud vormingu käivitamise tulem.<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Märkus.</strong> Siltide ja kirjelduste tõlgitud tekst asustatakse ER-vormingu väljundisse vastavalt faili- ja kaustavormingu ülemelementidele konfigureeritud keelesätetele.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (loend, välja nimi, eraldaja)</td>
<td>Tagastab loendist välja liitväärtuste stringi valitud eraldajaga.</td>
<td>Kui sisestasite andmeallikana DS väärtuse SPLIT("abc" , 1), tagastab avaldis STRINGJOIN (DS, DS.Value, ":") tulemi „a:b:c”</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (loend, piirväärtus, piirallikas)</td>
<td>Tükeldab loendi uueks alamloenditest koosnevaks loendiks ja tagastab tulemuse kirjeloendi sisus. Piirväärtuse parameeter määrab algse loendi tükeldamise piirväärtuse. Piirallika parameeter määrab etapi, milles kogusumma suureneb. Piirangut ei rakendata antud loendi üksikule üksusele, kui piirallikas ületab määratud piirangut.</td>
<td>Järgmises näites kirjeldatakse näidisvormingut, kasutades andmeallikaid. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>See on vormingu käivitamise tulemus, mis kujutab tarbekaupade lamedat loendit.<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>Järgmises näites on toodud sama vorming, mida on kohandatud, et esitada tarbekaupade loend partiidena, kus üksik partii peab sisaldama tarbekaupu kogukaaluga, mis ei tohi ületada piirangut 9.<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>See on kohandatud vormingu käivitamise tulemus. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Märkus.</strong> Piirangut ei rakendata algse loendi viimasele üksusele, kuna selle piirangu allika (mass) väärtus (11) ületab määratletud piirangut (9). Kasutage kas funktsiooni <strong>KUS</strong> või vastava vorminguelemendi avaldist <strong>Lubatud</strong>, et alamloendeid aruande loomisel vajaduse korral eirata (jätta vahele).</td>
</tr>
<tr class="odd">
<td>FILTER (loend, tingimus)</td>
<td>Tagastab antud loendi, mida on filtreeritud määratud tingimuse jaoks, muutes päringut. Erinevalt funktsioonist <strong>KUS</strong> rakendatakse määratud tingimust andmebaasi tasemel kõigile tabelikirje tüüpi ER-i andmeallikatele.</td>
<td>FILTER (hankijad, Vendors.VendGroup = &quot;40&quot;) tagastab ainult hankijate gruppi „40” kuuluvate hankijate loendi, kui <strong>Hankija</strong> on konfigureeritud tabelile <strong>VendTable</strong> viitava ER-i andmeallikana.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loogilised funktsioonid

| Funktsioon                                                                                | Kirjeldus                                                                                                                                                                                                                                                                     | Näide                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CASE (avaldis, suvand 1, tulem 1 \[, suvand 2, tulem 2\] ... \[, vaiketulem\]) | Arvutab määratud avaldise väärtuse määratud teise suvandi suhtes. Tagastab suvandi tulemi, mis on võrdne avaldise väärtusega. Muidu tagastatakse valikuliselt sisestatud vaiketulem (viimane parameeter, millele ei eelne suvand). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** tagastab stringi **"WINTER"**, kui praeguse Dynamics 365 for Operations seansi kuupäev jääb vahemikku oktoober kuni detsember. Muidu tagastatakse tühi string. |
| IF (tingimus, väärtus 1, väärtus 2)                                                        | Tagastab määratud väärtuse 1, kui antud tingimus on täidetud. Muidu tagastatakse väärtus 2. Kui väärtus 1 ja väärtus 2 on kirjed või kirjeloendid, on tulemil ainult väljad, mis on olemas mõlemas loendis.                                                                     | **IF (1=2, "condition is met", "condition is not met")** tagastab stringi **"condition is not met"**.                                                                                                                                                      |
| NOT (tingimus)                                                                         | Tagastab määratud tingimuse tühistatud loogilise väärtuse.                                                                                                                                                                                                                   | **NOT (TRUE)** tagastab väärtuse **FALSE**.                                                                                                                                                                                                                            |
| AND (tingimus 1\[, tingimus 2, ...\])                                                 | Tagastab väärtuse **TRUE**, kui *kõik *määratud tingimused on tõesed. Muidu tagastatakse väärtus **FALSE**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** tagastab väärtuse **TRUE**. **AND (1=2, "a"="a")** tagastab väärtuse **FALSE**.                                                                                                                                                                           |
| OR (tingimus 1\[, tingimus 2, ...\])                                                  | Tagastab väärtuse **FALSE**, kui *kõik *määratud tingimused on väärad. Tagastab väärtuse **TRUE**, kui *mõni *määratud tingimustest on tõene.                                                                                                                                                                 | **OR (1=2, "a"="a")** tagastab väärtuse **TRUE**.                                                                                                                                                                                                                      |

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
<td><strong>NUMBERVALUE(&quot;1 234,56&quot;, &quot;,&quot;, &quot; &quot;)</strong> tagastab väärtuse <strong>1234.56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (string)</td>
<td>Teisendab määratud stringi numbriks. Komasid ja punkte (.), loetakse komakohtade eraldajateks ning miinusmärki (–) kasutatakse negatiivse märgina. Ilmneb erand, kui määratud stringis on muid mittenumbrilisi märke.</td>
<td><strong>VALUE (&quot;1 234,56&quot;)</strong> annab erandi.</td>
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
| EMPTYRECORD (kirje) | Tagastab kirje **null**, millel on sama struktuur kui määratud kirjeloendil või kirjel. **Märkus.** Kirje **null** on kirje, mille kõikidel väljadel on tühi väärtus (**0** \[null\] numbrite puhul, tühi string stringide puhul jne). | **EMPTYRECORD (SPLIT ("abc", 1))** tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille tagastab funktsioon **SPLIT**.   |

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
<td><strong>UPPER(&quot;Sample&quot;)</strong> tagastab väärtuse <strong>&quot;SAMPLE&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (string)</td>
<td>Tagastab määratud stringi, mis on teisendatud väiketäheliseks.</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> tagastab väärtuse <strong>&quot;sample&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (string, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringi algusest.</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> tagastab väärtuse <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (string, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringi lõpust.</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> tagastab väärtuse <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (string, alguspositsioon, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringist, alustades määratust kohas.</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> tagastab väärtuse <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (string)</td>
<td>Tagastab tähemärkide arvu määratud stringis.</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> tagastab väärtuse <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (number)</td>
<td>Tagastab tähemärke stringi, millele viitab määratud Unicode'i number.</td>
<td><strong>CHAR (255)</strong> tagastab väärtuse <strong>&quot;ÿ&quot;</strong>. <strong>Märkus.</strong> Tagastatud string sõltub failivormingu ülemelemendis valitud kodeeringust. Toetatud kodeeringute loendi leiate teemast <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodeeringuklass</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (string 1 [, string 2, …])</td>
<td>Tagastab kõik määratud tekstistringid, mis on ühendatud üheks stringiks.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> tagastab väärtuse <strong>&quot;abcdef&quot;</strong>. <strong>Märkus.</strong> Avaldis <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> tagastab samuti väärtuse <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (string, muster, asendus)</td>
<td>Tagastab määratud stringi, mille puhul kõik määratud mustri stringi märgid asendatakse määratud asendusstringis olevate vastavas kohas olevate tähemärkidega.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> asendab mustri <strong>&quot;cd&quot;</strong> stringiga <strong>&quot;GH&quot;</strong> ja tagastab väärtuse <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (string, muster, asendus, regulaaravaldise lipp)</td>
<td>Kui määratud regulaaravaldise lipp on <strong>tõene</strong>, tagastatakse määratud string, mida on muudetud, rakendades regulaaravaldist, mis on määratud selle funktsiooni musterargumendina. Seda avaldist kasutatakse asendatavate tähemärkide otsimiseks. Määratud asendusargumendi tähemärke kasutatakse leitud tähemärkide asendamiseks. Kui määratud regulaaravaldise lipp on <strong>väär</strong>, toimib see funktsioon nagu väärtus <strong>TRANSLATE</strong>.</td>
<td>  <strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> rakendab regulaaravaldist, mis eemaldab kõik mittearvulised sümbolid ja tagastab väärtuse <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> asendab mustri <strong>&quot;cd&quot;</strong> stringiga <strong>&quot;GH&quot;</strong> ja tagastab väärtuse <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (sisend)</td>
<td>Tagastab määratud sisendi, mis on teisendatud tekstistringiks, mis on vormindatud vastavalt praeguse Dynamics 365 for Operationsi eksemplari serverilokaadi sätetele. <strong>Tõelist</strong> tüüpi väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.</td>
<td>Kui Dynamics 365 for Operationsi serverilokaat on määratletud kui <strong>EN-US</strong>, tagastab <strong>TEXT (NOW ())</strong> Dynamics 365 for Operations seansi praeguse kuupäeva, 12/17/2015, tekstistringina <strong>&quot;12/17/2015 07:59:23&quot;</strong>. <strong>TEXT (1/3)</strong> tagastab väärtuse <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (string 1, string 2[, string 3, ...])</td>
<td>Tagastab määratud stringi, mida vormindatakse, asendades kõik argumendi <strong>%N</strong> esinemised argumendiga <em>n</em>. Argumendid on stringid. Kui parameetril ei ole argumenti, tagastatakse parameeter stringis kui <strong>&quot;%N&quot;</strong>. <strong>Tõelist</strong> tüüpi väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.</td>
<td>Selles näites tagastab andmeallikas <strong>PaymentModel</strong> komponendi <strong>Klient</strong> kaudu kliendikirjete loendi ja välja <strong>ProcessingDate</strong> kaudu töötlemise kuupäeva väärtuse. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a> ER-i vormingus, mis on mõeldud looma valitud klientidele elektroonilist faili, valitakse <strong>PaymentModel</strong> andmeallikana ja see juhib protsessi voogu. Lõppkasutajatele tehakse erand, kui valitud klient on peatatud kuupäeval, millal aruannet töödeldakse. Seda tüüpi töötlemise juhtimiseks koostatud valem saab kasutada järgmisi ressursse.
<ul>
<li>Dynamics 365 for Operationsi silt SYS70894, millel on järgmine tekst.
<ul>
<li><strong>Inglise keeles:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Saksa keeles:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operationsi silt SYS18389, millel on järgmine tekst.
<ul>
<li><strong>Inglise keeles:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>Saksa keeles:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Siin on valem, mida saab koostada: FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;)) Kui töödeldakse <strong>Litware Retaili kliendi</strong> aruannet 17. detsembril 2015 <strong>ameerika</strong> kultuuris ja <strong>inglise</strong> keeles, tagastab see valem järgmise teksti, mida saab esitada erandliku teatena lõppkasutajale: &quot;Nothing to print. Customer Litware Retail is stopped for 12/17/2015.&quot; Kui sama aruannet töödeldakse<strong> Litware Retaili kliendi</strong> jaoks 17. detsembril 2015 <strong>saksa</strong> kultuuris ja <strong>saksa</strong> keeles, tagastab see valem järgmise teksti, mis kasutab erinevat andmevormingut: &quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot; <strong>Märkus. </strong>Siltidele mõeldud ER-i valemites rakendatakse järgmist süntaksit.
<ul>
<li><strong>Dynamics 365 for Operationsi ressursside siltide puhul:</strong> <strong>@&quot;X&quot;</strong>, kus X on sildi ID rakendusobjektide puus (AOT)</li>
<li><strong>ER-i konfiguratsioonides asuvate siltide puhul:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, kus X on sildi ID ER-i konfiguratsioonis</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (number, vorming)</td>
<td>Tagastab määratud vormingus määratud numbri stringiesituse. (Teavet toetatud vormingute kohta vt jaotistest <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standardne</a> ja <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">kohandatud</a>.) Selle funktsiooni käitamise kontekst määrab kultuuri, mida kasutatakse numbrite vormindamiseks.</td>
<td>Ingliskeelses kultuuris tagastab <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> väärtuse <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> tagastab väärtuse <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (number, keel, valuuta, prindi valuuta nime lipp, kümnendkohad)</td>
<td>Tagastab sõnadena kirjutatud (tekstistringiks teisendatud) numbri määratud keeles. Keelekood ei ole kohustuslik: kui see on määratletud tühja stringina, kasutatakse selle asemel käitatava konteksti keelekoodi (määratletud kausta või faili loomiseks). Valuutakood ei ole kohustuslik. Kui see on määratletud tühja stringina, kasutatakse ettevõtte valuutat. Pange tähele, et parameetreid <strong>Prindi valuuta nimi</strong> ja <strong>Kümnendkohad</strong> analüüsitakse ainult järgmiste keelekoodide puhul: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Pange tähele, et parameetrit <strong>Prindi valuuta nimi</strong> analüüsitakse ainult nende Dynamics 365 for Operationsi ettevõtete puhul, mille riigikontekst toetab valuuta käänamist.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2) tagastab stringi „One Thousand Two Hundred Thirty Four and 56” NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) tagastab stringi „Sto dwadzieścia” NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2) tagastab stringi „Сто двадцать евро 21 евроцент”</td>
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

SUMIFS (liitmise võtmestring, kriteeriumivahemiku 1 string, kriteeriumiväärtuse 1 string \[, kriteeriumivahemiku2 string, kriteeriumiväärtuse2 string, …\])

Tagastab XML-i sõlmede väärtuste summa (koos võtmena määratletud nimega), mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimusi (vahemiku ja väärtuse paarid). Tagastab nullväärtuse, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

SUMIF (liitmise võtmestring, kriteeriumivahemiku string, kriteeriumiväärtuse string)

Tagastab XML-i sõlmede väärtuste summa (koos võtmena määratletud nimega), mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimuse (vahemik ja väärtus). Tagastab nullväärtuse, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

COUNTIFS (kriteeriumivahemiku 1 string, kriteeriumiväärtuse 1 string \[, kriteeriumivahemiku2 string, kriteeriumiväärtuse2 string, …\])

Tagastab XML-i sõlmede arvu, mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimusi (vahemiku ja väärtuse paarid). Tagastab nullväärtuse, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

COUNTIF (kriteeriumivahemiku string, kriteeriumiväärtuse string)

Tagastab XML-i sõlmede arvu, mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimuse (vahemik ja väärtus). Tagastab nullväärtuse, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

COLLECTEDLIST (kriteeriumivahemiku 1 string, kriteeriumiväärtuse 1 string \[, kriteeriumivahemiku2 string, kriteeriumiväärtuse2 string, …\])

Tagastab XML-i sõlmede väärtuste loendi, mis on kogutud selle vormi käivitamise ajal ja mis täidab sisestatud tingimusi (vahemiku ja väärtuse paarid). Tagastab tühja loendi, kui praeguste failide lipp **Kogu väljundi üksikasjad **on välja lülitatud.

### <a name="other-business-domainspecific-functions"></a>Muud (ettevõtte domeenipõhised) funktsioonid

| Funktsioon                                                                         | Kirjeldus                                                                                                                                                                                                                                                        | Näide                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (summa, lähtekoha valuuta, sihtkoha valuuta, kuupäev, ettevõte)        | Teisendab määratud rahasumma lähtekoha valuutast sihtkoha valuutaks, kasutades määratud kuupäeval määratud Dynamics 365 for Operationsi ettevõtte sätteid.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** tagastab ühe euroga võrdse väärtuse USA dollarites praeguse seansi kuupäeval DEMF-i ettevõtte sätete alusel.                                                                                                                                  |
| ROUNDAMOUNT (number, kümnendkohad, ümardamisreegel)                                       | Ümardab määratus summa vastavalt määratud ümardamisreeglile ja määratud kümnendkohtade arvule. **Märkus.** Ümardamisreegel peab olema määratud Dynamics 365 for Operationsi nummerdamise **RoundOffType** väärtusena.                          | Kui parameeter **model.RoundOff** on seatud väärtusele ****Allapoole****, tagastab **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** väärtuse **1000.78**. Kui parameeter **model.RoundOff** on seatud väärtusele **Normaalne** või **Ülespoole ümardamine**, tagastab **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** väärtuse **1000,79**. |
| CURCredRef (arvud)                                                              | Tagastab kreeditori viite määratud arve numbri arvude alusel.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** tagastab väärtuse **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (arvud)                                                                 | Tagastab kreeditori viite MOD97 avaldisena määratud arve numbri arvude alusel.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** tagastab väärtuse **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (arvud)                                                              | Tagastab ISO kreeditori viite määratud arve numbri arvude ja tähestikus olevate sümbolite alusel. **Märkus. **ISO-ga ühildumatute sümbolite tähestikust eemaldamiseks tuleb sisendparameeter enne sellele funktsioonile edastamist tõlkida. | **ISOCredRef ("VEND-200002")** tagastab väärtuse **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (string, number)                                  | Hankige täiendav finantsdimensiooni ID. Dimensioonid on esindatud selles stringis komadega eraldatud ID-dena. Numbrid määratlevad taotletud dimensioonide seeriakoodi selles stringis.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3) tagastab stringi „CC”                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Tagastab praegu logitud ettevõtte koodi.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_BANK\_MOD\_10 (numbrid)                                                       | Tagastab kreeditori viite MOD10 avaldisena antud arve numbri numbrite alusel.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") tagastab väärtuse 3                                                                                                                                                                                                                                                                   |
| FA\_SUM (põhivara kood, väärtusmudeli kood, alguskuupäev, lõppkuupäev)               | Tagastab ettevalmistatud andmekonteineri põhivarasummadega perioodi kohta.                                                                                                                                                                                         | FA\_SUM ("COMP-000001", „Praegune”, Kuupäev1, Kuupäev2) tagastab põhivara „COMP-000001” ettevalmistatud andmekonteineri koos väärtusmudeliga „Praegune” perioodi Kuupäev1 kuni Kuupäev2 kohta.                                                                                                                        |
| FA\_BALANCE (põhivara kood, väärtusmudeli kood, aruandlusaasta, aruande kuupäev) | Tagastab ettevalmistatud andmekonteineri põhivarasaldodega. Aruandlusaasta peab olema määratud Dynamics 365 for Operationsi nummerduse **AssetYear** väärtusena.                                                                                           | FA\_SUM ("COMP-000001", „Praegune”, AxEnumAssetYear.ThisYear, SESSIONTODAY ()) tagastab põhivara ettevalmistatud saldode andmekonteineri „COMP-000001” koos väärtusmudeliga „Praegune” 365 for Operationsi seansi praegusel kuupäeval.                                                                |

### <a name="functions-list-extension"></a>Funktsioonide loendi laiend

ER laseb laiendada nende funktsioonide loendit, mida kasutatakse ER-i avaldistes. Nõutavad on mõned projekteerimise panused. Üksikasjalikuma teabe saamiseks vt jaotist [Elektroonilise aruandluse funktsioonide loendi laiendamine](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Vt ka
--------

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) funktsioonide loendi laiendamine](general-electronic-reporting-formulas-list-extension.md)



