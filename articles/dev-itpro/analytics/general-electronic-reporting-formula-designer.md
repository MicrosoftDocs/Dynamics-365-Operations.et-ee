---
title: Valemikoostaja elektroonilises aruandluses (ER)
description: Selles teemas selgitatakse, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: d3ac6ea7b104428f364385e1fd3ed221cae8498d
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="formula-designer-in-electronic-reporting-er"></a>Valemikoostaja elektroonilises aruandluses (ER)

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat. ER-is kindla elektroonilise dokumendi vormingu koostamisel saate kasutada valemeid andmete teisendamiseks, et vastata selle dokumendi täitmise ja vormindamise nõuetele. Need valemid sarnanevad Microsoft Exceli valemitega. Valemites toetatakse erinevat tüüpi funktsioone: tekst, kuupäev ja kellaaeg, matemaatiline loogika, teave, andmetüübi teisendamine ja muud (ettevõtte domeenipõhised funktsioonid).

## <a name="formula-designer-overview"></a>Valemikoostaja ülevaade

ER toetab valemikoostajat. Seega saate koostamise ajal konfigureerida avaldisi, misa saab kasutada käitamisel järgmisteks ülesanneteks.

- Microsoft Dynamics 365 for Finance and Operationsi andmebaasist saadud andmete teisendamine. Need peavad olema sisestatud ER-i andmemudelisse, mis on mõeldud ER-vormingute andmeallikaks. (Näiteks võivad need teisendused hõlmata filtreerimist, grupeerimist ja andmetüübi konversiooni.)
- Andmete vormindamine, mis tuleb saata loodavale elektroonilisele dokumendile kindla ER-vormingu paigutuse ja tingimuste järgi. (Näiteks võidakse vormindada kooskõlas nõutava keele, kultuuri või kodeeringuga).
- Elektrooniliste dokumentide loomise protsessi juhtimine. (Näiteks saavad avaldised olenevalt andmete töötlemisest vormingu teatud elementide arvestamist lubada või keelata. Nad saavad ka katkestada dokumentide loomisprotsessi või saata lõppkasutajatele sõnumeid.)

**Valemikoostaja** lehe saate avada järgmiste tegevuste käigus.

- Andmeallika kaupade sidumine andmemudeli komponentidega.
- Andmeallika kaupade sidumine vormingu komponentidega.
- Andmeallikate osana esinevate arvutatud väljade täielik haldamine.
- Kasutaja sisendparameetrite nähtavustingimuste määratlemine.
- Vormingu teisenduste kujundamine.
- Vormingu komponentide lubamistingimuste määratlemine.
- Vormingu failikomponentide failinimede määratlemine.
- Protsessi juhtimise kinnituste tingimuste määratlemine.
- Protsessi juhtimise kinnituste teate tekstide määratlemine.

## <a name="designing-er-formulas"></a>ER-i valemite koostamine

### <a name="data-binding"></a>Andmete sidumine

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis teisendab andmeid, mis saadakse andmeallikatest, nii et käitamisel saab andmeid sisestada andmete tarbijas:

- Dynamics 365 for Finance and Operationsi andmeallikatest ja käitamisaja parameetritest ER-i andmemudelisse;
- ER-i andmemudelist ER-i vormingusse;
- Dynamics 365 for Finance and Operationsi andmeallikatest ja käitamisaja parameetritest ER-i vormingusse.

Järgmisel joonisel on seda tüüpi avaldise kujundus. Selles näites ümardab avaldis Dynamics 365 for Finance and Operationsi tabeli Intrastat välja **Intrastat.AmountMST** väärtuse kahe kümnendkohani ning annab siis ümardatud väärtuse.

[![Andmete sidumine](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Järgmine joonis näitab, kuidas seda tüüpi avaldist saab kasutada. Selles näites on koostatud avaldise tulem sisestatud andmemudeli **Maksu aruandluse mudel** komponendile **Transaction.InvoicedAmount**.

[![Kasutatav andmete sidumine](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Käitusajal ümardab koostatud valem **ROUND (Intrastat.AmountMST, 2)** välja **AmountMST** väärtuse tabeli Intrastat iga kirje puhul kahe kümnendkohani. Seejärel sisestab see ümardatud väärtuse andmemudeli **Maksu aruandlus** komponenti **Transaction.InvoicedAmount**.

### <a name="data-formatting"></a>Andmete vormindamine

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis vormindab andmeid, mis saadakse andmeallikatest, nii et andmeid saab saata elektroonilise dokumendi loomise osana. Teil võib olla vorming, mida tuleb rakendada tüüpilise reeglina, mida tuleb vormingu puhul taaskasutada. Sel juhul saate seda vormingut kasutada ühe korra vormingu konfiguratsioonis nimega teisendusena, millel on vormindamisavaldis. Selle nimelise teisenduse saab siduda paljude vormingu komponentidega, mille väljund peab olema vormindatud loodud vormindamisavaldise järgi.

Järgmisel joonisel on seda tüüpi teisenduse kujundus. Selles näites kärbib teisendus **TrimmedString** andmetüübi **String** sissetulevad andmed, eemaldades algus- ja lõputühikud. Seejärel tagastab see kärbitud stringiväärtuse.

[![Teisendus](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Järgmine joonis näitab, kuidas seda tüüpi teisendust saab kasutada. Selles näites saadavad mitu vormingu komponenti teksti käitusajal väljundina loodavale elektroonilisele dokumendile. Kõik need vormingukomponendid viitavad teisendusele **TrimmedString** nime järgi.

[![Kasutatav teisendamine](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kui vormingu komponendid (näiteks komponendi **partyName** puhul eelmises näites) viitavad teisendusele **TrimmedString**, saadab teisendus teksti väljundina loodavasse elektroonilisse dokumenti. See tekst ei sisalda algus- ega lõputühikuid.

Kui teil on vorming, mida tuleb rakendada eraldi, saab selle kasutusele võtta kindla vormingu komponendi sidumise üksiku avaldisena. Järgmisel joonisel on seda tüüpi avaldis. Selles näites on vormingu komponent **partyType** seotud andmeallikaga avaldise kaudu, mis teisendab sissetulevad andmeallika andmed väljalt **Model.Company.RegistrationType** suurtäheliseks tekstiks. Seejärel saadab avaldis selle teksti väljundina elektroonilisse dokumenti.

[![Vorminduse rakendamine üksikule komponendile](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Protsessi voo juhtimine

ER-i valemikoostajat saab kasutada elektrooniliste dokumentide loomise protsessivoo juhtimiseks kasutatavate avaldiste määratlemiseks. Saate teha järgmisi toiminguid.

- Määratlege tingimused, mis määravad, millal tuleb dokumendi loomise protsess peatada.
- Määrake avaldised, mis loovad kasutajale sõnumeid peatatud protsesside kohta või heidavad käivitamislogi sõnumeid aruande loomise protsessi jätkamise kohta.
- Määrake loodavate elektrooniliste dokumentide failinimed ja juhtige nende loomise tingimusi.

Iga protsessi voo juhtimise reegel on koostatud üksiku kinnitusena. Järgmisel joonisel on seda tüüpi kinnitus. Siin on selles näites oleva konfiguratsiooni selgitus.

- Kinnitamist hinnatakse, kui XML-faili loomisel luuakse **INSTAT**-sõlm.
- Kui kannete loend on tühi, lõpetab kinnitamine käivitamisprotsessi ja tagastab väärtuse **FALSE**.
- Kinnitamine annab tõrketeate, mis sisaldab Finance and Operationsi sildi SYS70894 teksti kasutaja eelistatud keeles.

[![Kinnitamine](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER-i valemikoostajat saab kasutada ka failinime loomiseks loodavale elektroonilisele dokumendile ja faili loomise protsessi juhtimiseks. Järgmisel joonisel on seda tüüpi protsessi voo juhtimise kujundus. Siin on selles näites oleva konfiguratsiooni selgitus.

- Andmeallika **model.Intrastat** kirjete loend on jagatud partiideks. Iga partii sisaldab 1000 kirjet.
- Väljund loob zip-faili, mis sisaldab ühte XML-vormingus faili iga loodud partii kohta.
- Avaldis annab vastuseks failinime loodavatele elektroonilistele dokumentidele, liites faili nime ja failinime laiendi. Teise partii ja kõikide järgnevate partiide puhul sisaldab faili nimi järelliitena partii ID-d.
- Avaldis lubab (andes vatuseks väärtuse **TRUE**) faili loomise protsessi partiidele, mis sisaldavad vähemalt ühte kirjet.

[![Faili juhtimine](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Põhisüntaks

ER-i avaldised võivad sisaldada mõnd või kõiki järgmistest elementidest.

- Konstandid
- Tehtemärgid
- Viited
- Teed
- Funktsioonid

#### <a name="constants"></a>Konstandid

Avaldiste koostamisel saate kasutada tekstilisi ja arvulisi konstante (st väärtused, mida ei arvutata). Näiteks kasutab avaldis **VALUE ("100") + 20** arvulist konstanti **20** ja stringi konstanti **100** ning annab vastuseks arvulise väärtuse **120**. ER-i valemikoostaja toetab paoseeriaid. Seega saate määrata avaldise stringi, mida tuleb teisiti käsitleda. Näiteks avaldis **Lev Tolstoi „„Sõda ja rahu”” 1. osa** tagastab tekstistringi **Lev Tolstoi „Sõda ja rahu” 1. osa**.

#### <a name="operators"></a>Operaatorid

Järgmises tabelis on aritmeetilised tehtemärgid, mida saate kasutada põhiliste matemaatiliste tehete puhul, nagu liitmine, lahutamine, korrutamine ja jagamine.

| Operaator | Tähendus               | Näide |
|----------|-----------------------|---------|
| +        | Lisa              | 1 + 2     |
| -        | Lahutamine, negatiivsus | 5-2, -1 |
| \*       | Korrutamine        | 7\*8    |
| /        | Jaotus              | 9 / 3     |

Järgmises tabelis kuvatakse toetatud võrdlemise tehtemärgid. Neid tehtemärke saate kasutada kahe väärtuse võrdlemiseks.

| Operaator | Tähendus                  | Näide    |
|----------|--------------------------|------------|
| =        | Võrdne                    | X = Y        |
| &gt;     | Suurem kui             | X&gt;Y     |
| &lt;     | Väiksem kui                | X&lt;Y     |
| &gt;=    | Suurem kui või võrdne | X&gt;=Y    |
| &lt;=    | Väiksem kui või võrdne    | X&lt;=Y    |
| &lt;&gt; | Pole võrdne             | X&lt;&gt;Y |

Peale selle saate kasutada ja-märki (&) teksti liitmise tehtemärgina. Nii saate ühe või mitu tekstistringi üheks tekstiks ühendada või liita.

| Operaator | Tähendus     | Näide                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Ühenda | "Midagi pole printida" & "&nbsp;" & "kirjeid ei leitud" |

##### <a name="operator-precedence"></a>Tehete järjestus

Liitavaldise osade arvutamise järjekord on oluline. Näiteks avaldise **1 + 4 / 2** tulemid erinevad olenevalt sellest, kas esimesena tehakse liitmis- või jagamistoiming. Saate kasutada sulge, et selgelt määratleda, kuidas avaldise väärtust leida. Näiteks näitamaks, et esimesena tuleb teha liitmistoiming, saate muuta eelnevat avaldis järgmiselt: **(1 + 4) / 2**. Kui avaldise tehete järjekord ei ole selgelt määratletud, põhineb see vaikejärjestusel, mis on määratud toetatud tehtemärkidele. Järgmises tabelis on toodud igale tehtemärgile määratud järjestus. Kõrgema prioriteediga tehted (nt 7) arvutatakse enne madalama prioriteediga tehteid (nt 1).

| Tehtejärjestus | Tehtemärgid      | Süntaks                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Grupeerimine       | ( … )                                                                   |
| 6          | Liikme juurdepääs  | … . …                                                                   |
| 5          | Funktsioonikutse  | … ( … )                                                                 |
| 4          | Korrutamine | … \* …<br>… / …                                                         |
| 3          | Täiend       | … + …<br>… - …                                                          |
| 2          | Võrdlus     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Lahutamine     | … , …                                                                   |

Kui avaldis sisaldab mitut järjestikust sama järjestusega tehet, tehakse neid tehteid vasakult paremale. Näiteks avaldis **1 + 6 / 2 \* 3 &gt; 5** tagastab väärtuse **tõene**. Soovitame avaldise tehete soovitud järjestuse selgeks näitamiseks kasutada sulge, et avaldisi oleks lihtsam lugeda ja hallata.

#### <a name="references"></a>Viited

Kõiki praeguse ER-i komponendi andmeallikaid, mis on avalduse koostamise ajal saadaval, saab kasutada nimega viidetena. (Praegune ER-i komponent saab olla kas mudel või vorming.) Näiteks sisaldab praegune ER-i andmemudel andmeallikat **ReportingDate**, mis annab vastuseks andmetüübi **DATETIME** väärtuse. Loodavas dokumendis väärtuse õigesti vormindamiseks saate viidata avaldises andmeallikale järgmiselt: **DATETIMEFORMAT (ReportingDate, "pp-KK-aaaa")**.

Kõikidele viidatava andmeallika nimes olevatele tähemärkidele, mis ei kuulu tähestikku, peab eelnema ühekordne jutumärk ('). Kui viidatava andmeallika nimi sisaldab vähemalt ühte sümbolit, mis ei kuulu tähestikku, tuleb nimi panna ühekordsetesse jutumärkidesse. (Näiteks võivad need tähestikku mittekuuluvad sümbolid olla kirjavahemärgid või mis tahes muud kirjalikud sümbolid.) Järgmisena on toodud mõned näited.

- Andmeallikale **Tänane kuupäev ja kellaaeg** tuleb viidata ER-i avaldises järgmiselt: **'Tänane kuupäev ja kellaaeg'**.
- ER-i avaldises tuleb viidata andmeallika **Kliendid** meetodile **nimi()** järgmiselt: **Kliendi.'nimi()'**.

Kui Dynamics 365 for Finance and Operationsi andmeallikate meetoditel on parameetrid, kasutatakse järgmist süntaksit.

- Kui andmeallika **System** meetodi **isLanguageRTL** andmetüübil **String** on parameeter **EN-US**, peab see meetod olema ER-avaldises viidatud järgmisel viisil: **System.'isLanguageRTL'("EN-US")**.
- Kui meetodi nimi sisaldab ainult tähti ja numbreid, siis ei ole jutumärgid vajalikud. Need on aga vajalikud sulgusid sisaldava tabelimeetodi puhul.

Kui andmeallikas **System** lisatakse ER-vastendusele, mis viitab rakenduse Finance and Operations rakendusklassile **Üldine**, siis annab avaldis kahendmuutuja väärtuse **FALSE**. Muudetud avaldis **System.' isLanguageRTL'("AR")** annab vastuseks kahendmuutuja väärtuse **TRUE**.

Saate piirata, kuidas väärtusi selle meetoditüübi parameetritele edastatakse.

- Seda tüüpi meetoditele saab edastada ainult konstante. Konstantide väärtused määratakse koostamisajal.
- Seda tüüpi parameetrite puhul toetatakse ainult primitiivseid (põhilisi) andmetüüpe. (Primitiivsed andmetüübid on täisarv, reaalarv, kahendmuutuja, string jne).

#### <a name="paths"></a>Teed

Kui avaldis viitab struktureeritud andmeallikale, saate kasutada tee määratlemist, et valida selle andmeallika kindel primitiivne element. Punkti (.) kasutatakse struktureeritud andmeallika üksikute elementide eraldamiseks. Näiteks praegune ER-i andmemudel sisaldab andmeallikat **InvoiceTransactions**, mis annab vastuseks kirjete loendi. Kirje struktuur **InvoiceTransactions** sisaldab välju **AmountDebit** ja **AmountCredit**, mis mõlemad tagastavad arvulisi väärtusi. Seega saate arveldatud summa arvutamiseks koostada järgmise avaldise: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Funktsioonid

Järgmises jaotises kirjeldatakse funktsioone, mida saab kasutada ER-i avaldistes. Kõiki avaldise konteksti (praegune ER-i andmemudel või ER-i vorming) andmeallikaid saab kasutada helistamisfunktsioonide parameetritena vastavalt funktsioonide käivitamine argumentide loendile. Konstante saab kasutada ka funktsioonide käivitamise parameetritena. Näiteks praegune ER-i andmemudel sisaldab andmeallikat **InvoiceTransactions**, mis annab vastuseks kirjete loendi. Kirje struktuur **InvoiceTransactions** sisaldab välju **AmountDebit** ja **AmountCredit**, mis mõlemad tagastavad arvulisi väärtusi. Seega saate arveldatud summa arvutamiseks koostada järgmise avaldise, mis kasutab sisseehitatud ER-i ümardamisfunktsiooni: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Toetatud funktsioonid

Järgmistes tabelites kirjeldatakse andmete manipuleerimise funktsioone, mida saate kasutada ER-i andmemudelite ja ER-i aruannete koostamiseks. Funktsioonide loend ei ole fikseeritud. Arendajad saavad seda laiendada. Võimalike funktsioonide loendi nägemiseks avage ER-i valemikoostaja funktsioonide paan.

### <a name="date-and-time-functions"></a>Kuupäeva ja kellaaja funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| ADDDAYS (kuupäev, kellaaeg, päevad) | Lisage määratud kuupäeva ja kellaaja väärtusele määratud päevade arv. | **ADDDAYS (NOW(), 7)** tagastab kuupäeva ja kellaaja seitsme päeva pärast. |
| DATETODATETIME (kuupäev) | Teisendage määratud kuupäeva väärtus kuupäeva ja kellaaja väärtuseks. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** annab vastuseks praeguse Finance and Operationsi seansi kuupäeva 24. detsember 2015 kujul **12/24/2015 12:00:00 AM**. Selles näites on **CompInfo** tüübi **Finance and Operations / tabel** ER-i andmeallikas ja viitab tabelile CompanyInfo. |
| NOW () | Annab vastuseks Finance and Operationsi rakenduseserveri praeguse kuupäeva ja kellaaja kuupäeva- ja kellaaja väärtusena. | |
| TODAY () | Tagastab Finance and Operationsi rakenduseserveri kuupäeva kuupäevaväärtusena. | |
| NULLDATE () | Tagastab kuupäeva väärtuse **null**. | |
| NULLDATETIME () | Annab vastuseks kuupäeva ja kellaaja väärtuse **null**. | |
| DATETIMEFORMAT (kuupäev ja kellaaeg, vorming) | Teisendage määratud kuupäeva ja kellaaja väärtus määratud vormingus stringiks. (Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), „pp-KK-aaaa”)** annab vastuseks praeguse Finance and Operationsi rakenduseserveri kuupäeva 24. detsember 2015 kujul **"24-12-2015"** määratud kohandatud vormingu kohaselt. |
| DATETIMEFORMAT (kuupäev ja kelaaeg, vorming, kultuur) | Teisendage määratud kuupäeva ja kellaaja väärtus määratud vormingus ja [kultuuris](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx) stringiks. (Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** annab vastuseks Finance and Operationsi rakenduseserveri praeguse kuupäeva 24. detsember 2015 kujul **"24.12.2015"** valitud saksa kultuuri kohaselt. |
| SESSIONTODAY () | Annab vastuseks Finance and Operationsi seansi kuupäeva kuupäevaväärtusena. | |
| SESSIONNOW () | Annab vastuseks Finance and Operationsi seansi praeguse kuupäeva ja kellaaja kuupäeva- ja kellaaja väärtusena. | |
| DATEFORMAT (kuupäev, vorming) | Annab vastuseks määratud kuupäeva määratud vormingus stringi kujul. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** annab vastuseks praeguse Finance and Operationsi seansi kuupäeva 24. detsember 2015 kujul **"24-12-2015"** määratud kohandatud vormingu kohaselt. |
| DATEFORMAT (kuupäev, vorming, kultuur) | Teisendage määratud kuupäevaväärtus määratud vormingus ja [kultuuris](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx) stringiks. (Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** annab vastuseks Finance and Operationsi seansi praeguse kuupäeva 24. detsember 2015 kujul **"24.12.2015"** valitud saksa kultuuri kohaselt. |
| DAYOFYEAR (kuupäev) | Annab vastuseks 1. jaanuari ja määratud kuupäeva vahelise päevade arvu täisarvuna. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** annab vastuseks **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** annab vastuseks **1**. |
| DAYS (kuupäev 1, kuupäev 2) | Annab vastuseks esimese määratud kuupäeva ja teise määratud kuupäeva vahele jäävate päevade arvu. Annab vastuseks positiivse väärtuse, kui esimene kuupäev on hilisem kui teine kuupäev, annab vastuseks **0** (nulli), kui esimene kuupäev võrdub teise kuupäevaga, või annab vastuseks negatiivse väärtuse, kui esimene kuupäev on varasem kui teine kuupäev. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** annab vastuseks **-1**. |

### <a name="data-conversion-functions"></a>Andmete teisendamise funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| DATETODATETIME (kuupäev) | Teisendage määratud kuupäeva väärtus kuupäeva ja kellaaja väärtuseks. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** annab vastuseks praeguse Finance and Operationsi seansi kuupäeva 24. detsember 2015 kujul **12/24/2015 12:00:00 AM**. Selles näites on **CompInfo** tüübi **Finance and Operations / tabel** ER-i andmeallikas ja viitab tabelile CompanyInfo. |
| DATEVALUE (string, vorming) | Annab vastuseks määratud stringi määratud vormingus kuupäeva kujul. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** annab vastuseks kuupäeva 21. detsember 2016 määratud kohandatud vormingu ja rakenduse vaikekultuuri **EN-US** kohaselt. |
| DATEVALUE (string, vorming, kultuur) | Annab vastuseks määratud stringi määratud vormingus ja kultuuris kuupäeva kujul. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** annab vastuseks kuupäeva 21. jaanuar 2016 määratud kohandatud vormingu ja kultuuri kohaselt. Stringiga **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** ilmneb aga erand, mis teavitab kasutajat sellest, et seda stringi ei tuvastata kehtiva kuupäevana. |
| DATETIMEVALUE (string, vorming) | Annab vastuseks määratud stringi määratud vormingus kuupäeva ja kellaaja kujul. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** annab vastuseks kellaaja 2:55:00 21. detsembril 2016, määratud kohandatud vormingu ja rakenduse vaikekultuuri **EN-US** kohaselt. |
| DATETIMEVALUE (string, vorming, kultuur) | Annab vastuseks määratud stringi määratud vormingus ja kultuuris kuupäeva ja kellaaja kujul. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** annab vastuseks kellaaja 2:55:00 21. detsembril 2016, määratud kohandatud vormingu ja kultuuri kohaselt. Stringiga **DATETIMEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** ilmneb aga erand, mis teavitab kasutajat sellest, et seda stringi ei tuvastata kehtiva kuupäeva ja kellaajana. |

### <a name="list-functions"></a>Loendi funktsioonid

<table>
<thead>
<tr>
<th>Funktsioon</th>
<th>Kirjeldus</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (sisend, pikkus)</td>
<td>Jaotage määratud sisendstring alamstringideks, millest igaühel on määratud pikkus. Tagastab tulemi uue loendina.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> tagastab uue loendi, mis koosneb kahest kirjest, millel on väli <strong>STRING</strong>. Esimese kirje väli sisaldab teksti <strong>&quot;abc&quot;</strong> ja teise kirje väli sisaldab teksti <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr>
<td>SPLITLIST (loend, number)</td>
<td>Jaotatage määratud loend partiideks, millest igaüks sisaldab määratud kirjete arvu. Tagastab tulemi uue partiide loendina, mis sisaldab järgmisi elemente.
<ul>
<li>Partiid regulaarsete loenditena (komponent <strong>Väärtus</strong>)</li>
<li>Praegune partiinumber (komponent <strong>BatchNumber</strong>)</li>
</ul>
</td>
<td>Järgmisel joonisel luuakse andmeallikas <strong>Read</strong> kolme kirje kirjeloendina. See loend on jaotatud partiideks, millest igaüks sisaldab kuni kahte kirjet.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Järgmisel joonisel on näidatud koostatud vormingu paigutus. Selles vormi paigutuses luuakse andmeallika <strong>Read</strong> sidemed, et luua XML-vormingus väljund. See väljund esitab üksikuid sõlmi igale partiile ja selles olevale kirjele.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (kirje 1 [, kirje 2, …])</td>
<td>Tagastab uue loendi, mis luuakse määratud argumentidest.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> tagastab tühja kirje, kus väljade loend sisaldab kõiki kirjeloendite <strong>MainData</strong> ja <strong>OtherData</strong> välju.</td>
</tr>
<tr>
<td>LISTJOIN (loend 1, loend 2, …)</td>
<td>Tagastab ühendatud loendi, mis luuakse määratud argumentide loenditest.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> annab vastuseks kuue kirje loendi, kus andmetüübi <strong>STRING</strong> üks väli sisaldab üksikuid tähti.</td>
</tr>
<tr>
<td>ISEMPTY (loend)</td>
<td>Annab vastuseks väärtuse <strong>TRUE</strong>, kui määratud loend ei sisalda ühtki elementi. Muidu tagastatakse väärtus <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (loend)</td>
<td>Tagastab tühja loendi, kasutades määratud loendit loendi struktuuri allikana.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> annab vastuseks uue tühja loendi, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon <strong>SPLIT</strong>.</td>
</tr>
<tr>
<td>FIRST (loend)</td>
<td>Tagastab määratud loendi esimese kirje, kui see kirje pole tühi. Muidu ilmneb erand.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (loend)</td>
<td>Tagastab määratud loendi esimese kirje, kui see kirje pole tühi. Muidu tagastatakse kirje <strong>null</strong>.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (loend)</td>
<td>Tagastab loendi, mis sisaldab ainult määratud loendi esimest üksust.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (tee)</td>
<td>See funktsioon töötab mälusisese valikuna. See tagastab uue lameloendi, mis kajastab kõiki konkreetsele teele vastavaid üksusi. Tee peab olema määratletud kirjeloendi andmetüübi andmeallika elemendi kehtiva andmeallika teena. Andmeelemendid, nagu tee stingi või kuupäevani, peaks ER-i avaldisekoostajas andma koostamise ajal tõrke.</td>
<td>Kui sisestate andmeallikaks <strong>SPLIT(&quot;abcdef&quot; , 2)</strong>, tagastab <strong>COUNT( ALLITEMS (DS.Value))</strong> väärtuse <strong>3</strong>.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (tee)</td>
<td>See funktsioon töötab liidetud SQL-päringuna. See tagastab uue lameloendi, mis kajastab kõiki konkreetsele teele vastavaid üksusi. Määratud tee peab olema määratletud kirjeloendi andmetüübiga andmeallika elemendi kehtiva andmeallika teena ja sisaldama vähemalt üht seost. Andmeelemendid, nagu tee stingi või kuupäevani, peaks ER-i avaldisekoostajas andma koostamise ajal tõrke.</td>
<td>Määratlege oma mudelivastenduses järgmised andmeallikad.
<ul>
<li><strong>CustInv</strong> (tüüp <strong>Tabelikirjed</strong>), mis viitab tabelile CustInvoiceTable</li> 
<li><strong>FilteredInv</strong> (tüüp <strong>Arvutatud väli</strong>), mis sisaldab avaldist <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong></li>
<li><strong>JourLines</strong> (tüüp <strong>Arvutatud väli</strong>), mis sisaldab avaldist <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong></li>
</ul>
<p>Kui käitate mudelivastenduse andmeallika <strong>JourLines</strong> poole pöördumiseks, käivitatakse järgmine SQL-avaldis.</p>
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3 WHERE...
</td>
</tr>
<tr>
<td>ORDERBY (loend [, avaldis 1, avaldis 2, …])</td>
<td>Annab vastuseks määratud loendi pärast seda, kui seda on sorditud määratud argumentide kohaselt. Neid argumente saab määratleda avaldistena.</td>
<td>Kui <strong>Hankija</strong> on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, annab <strong>ORDERBY (Vendors, Vendors.&#39;name()&#39;)</strong> vastuseks hankijate loendi, mis on sorditud nimede järgi kasvavas järjestuses.</td>
</tr>
<tr>
<td>REVERSE (loend)</td>
<td>Tagastab määratud loendi vastupidises sortimisjärjestuses.</td>
<td>Kui <strong>Hankija</strong> on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, annab <strong>REVERSE (ORDERBY (Vendors, Vendors.&#39;name()&#39;)) )</strong> vastuseks hankijate loendi, mis on sorditud nimede järgi kahanevas järjestuses.</td>
</tr>
<tr>
<td>WHERE (loend, tingimus)</td>
<td>Annab vastuseks määratud loendi pärast seda, kui seda on filtreeritud määratud tingimuse kohaselt. Määratud tingimust rakendatakse mälus olevale loendile. Nii erineb funktsioon <strong>WHERE</strong> funktsioonist <strong>FILTER</strong>.</td>
<td>Kui <strong>Hankija</strong> on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, annab vastuseks <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> hankijate loendi, mis kuulub hankijate gruppi 40.</td>
</tr>
<tr>
<td>ENUMERATE (loend)</td>
<td>Tagastab uue loendi, mis koosneb määratud loendi nummerdatud kirjetest ja mis avaldab järgmised elemendid.
<ul>
<li>Määratud loendikirjed regulaarsete loenditena (komponent <strong>Väärtus</strong>)</li>
<li>Praegune kirje indeks (komponent <strong>Number</strong>)</li>
</ul>
</td>
<td>Järgmises näites on andmeallikas <strong>Nummerdatud</strong> loodud andmeallika <strong>Hankijad hankijate</strong> kirjete nummerdatud loendina, mis viitab tabelile VendTable.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Järgmine illustratsioon näitab seda vormingut. Selles vormingus luuakse andmesidemed, et luua XML-vormingus väljund. Selle väljund esitab üksikuid hankijaid nummerdatud sõlmedena.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (loend)</td>
<td>Tagastab määratud loendi kirjete arvu, kui loend pole tühi. Muidu tagastatakse väärtus <strong>0</strong> (null).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> tagastab väärtuse <strong>2</strong>, sest funktsioon <strong>SPLIT</strong> loob loendi, mis koosneb kahest kirjest.</td>
</tr>
<tr>
<td>LISTOFFIELDS (tee)</td>
<td>Annab vastuseks üht järgmist tüüpi argumentidest loodud kirjete loendi.
<ul>
<li>Mudeli loetelu</li>
<li>Vormingu loetelu</li>
<li>Konteiner</li>
</ul>
<p>Loodud loend koosneb järgmiste väljadega kirjetest:</p>
<ul>
<li>Nimi</li>
<li>Silt</li>
<li>Kirjeldus</li>
</ul>
Käitusajal annavad väljad <strong>Silt</strong> ja <strong>Kirjeldus</strong> vastuseks väärtused, mis põhinevad vormingu keelesätetest.
</td>
<td>Järgmises näites on andmemudelis kasutusele võetud loetelu.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Järgmises näites on toodud järgmised üksikasjad:</p>
<ul>
<li>mudeli loetelu on aruandesse sisestatud andmeallikana;</li>
<li>ER-i avaldis kasutab mudeli loetelu funktsiooni <strong>LISTOFFIELDS</strong> parameetrina;</li>
<li>kirjeloendi tüübi andmeallikas on sisestatud aruandesse loodud ER-i avaldise abil.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Järgmises näites kirjeldatakse elektroonilise aruandluse vormingu elemente, mis on seotud funktsiooniga <strong>LISTOFFIELDS</strong> loodud kirjeloendi tüübi andmeallikaga.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Siltide ja kirjelduste tõlgitud tekst sisestatakse ER-i vormingu väljundis vormingu peaelementide FAIL ja KAUST jaoks konfigureeritud keelesätete kohaselt.</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (tee, keel)</td>
<td>Annab vastuseks üht järgmist tüüpi argumentidest loodud kirjete loendi: mudeli loetelu, vormingu loetelu või konteiner. Loodud loend koosneb järgmiste väljadega kirjetest:
<ul>
<li>Nimi</li>
<li>Silt</li>
<li>Kirjeldus</li>
<li>IsTranslated</li>
</ul>
Käitusajal annavad väljad <strong>Silt</strong> ja <strong>Kirjeldus</strong> vastuseks väärtused, mis põhinevad vormingu keelesätetel ja määratud keelel. Väli <strong>Is translated</strong> näitab, et väli <strong>Silt</strong> on tõlgitud määratud keelde.
</td>
<td>Näiteks saate andmeallika tüüpi <strong>Arvutatud väli</strong> kasutada andmeallikate <strong>enumType_de</strong> ja <strong>enumType_deCH</strong> konfigureerimiseks andmemudeli loetelu <strong>enumType</strong> jaoks:
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
Sel juhul saate järgmist avaldist kasutada Šveitsi saksa keele loeteluväärtuse sildi saamiseks, kui selle tõlge on olemas. Kui Šveitsi saksa keele tõlget pole saadaval, on silt saksa keeles: <strong>IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)</strong>.
</td>
</tr>
<tr>
<td>STRINGJOIN (loend, välja nimi, eraldaja)</td>
<td>Annab vastuseks stringi, mis koosneb määratud loendi määratud väärtuse liitväärtustest. Väärtused on eraldatud määratud eraldajaga.</td>
<td>Kui sisestate andmeallikana (DS) väärtuse <strong>SPLIT(&quot;abc&quot; , 1)</strong>, annab avaldis <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> vastuseks <strong>&quot;a-b-c&quot;</strong>.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (loend, piirväärtus, piirallikas)</td>
<td>Tükeldab määratud loendi uueks alamloenditest koosnevaks loendiks ja annab vastuseks tulemi kirjeloendi sisus. <strong>Piirväärtuse</strong> parameeter määratleb algse loendi tükeldamise piirväärtuse. <strong>Piirallika</strong> parameeter määratleb etapi, milles kogusumma suureneb. Piirangut ei rakendata algse loendi üksikule üksusele, kui piirallikas ületab määratud piirangut.</td>
<td>Järgmisel joonisel on näidatud vorming. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>Järgmisel joonisel on näidatud vormingu puhul kasutatud andmeallikad.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Järgmisel joonisel on näidatud vormingu käitamise tulemus. Sel juhul on väljund tarbekaupade lame loend.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>Järgmistes näidetes on sama vormingut kohandatud nii, et see esitab tarbekaupade loendi partiidena, kus üksik partii peab sisaldama tarbekaupu ning kogukaal ei tohi ületada piirangut 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Järgmisel joonisel on näidatud kohandatud vormingu käitamise tulemus.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] Piirangut ei rakendata algse loendi viimasele üksusele, kuna selle piirangu allika (mass) väärtus (11) ületab määratletud piirangut (9). Kasutage kas funktsiooni <strong>KUS</strong> või vastava vorminguelemendi avaldist <strong>Lubatud</strong>, et alamloendeid aruande loomisel vajaduse korral eirata (jätta vahele).</blockquote>
</td>
</tr>
<tr>
<td>FILTER (loend, tingimus)</td>
<td>Annab vastuseks määratud loendi pärast seda, kui päringut on muudetud filtreerima määratud tingimuse kohaselt. Erinevalt funktsioonist <strong>WHERE</strong> rakendatakse määratud tingimust andmebaasi tasemel kõigile tüübi <strong>Tabeli kirjed</strong> ER-i andmeallikatele. Loendi ja tingimuse saab määrata tabelite ja seoste abil.</td>
<td>Kui <strong>Hankija</strong> on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, annab vastuseks <strong>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> hankijate loendi, mis kuulub hankijate gruppi 40. Kui <strong>Hankija</strong> on konfigureeritud elektroonilise aruandluse andmeallikana, mis viitab tabelile <strong>VendTable</strong>, ja kui <strong>parmVendorBankGroup</strong> on konfigureeritud elektroonilise aruandluse andmeallikana, mis tagastab väärtuse andmetüübiga <strong>String</strong>, tagastab avaldis <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> loendi ainult nende hankijakontodega, mis kuuluvad kindlasse pangarühma.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loogilised funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| CASE (avaldis, suvand 1, tulem 1 \[, suvand 2, tulem 2\] … \[, vaiketulem\]) | Arvutab määratud avaldise väärtuse määratud teise suvandi suhtes. Annab vastuseks suvandi tulemi, mis on võrdne avaldise väärtusega. Muul juhul annab vastuseks valikulise vaiketulemi, kui see on määratud. (Vaiketulem on viimane parameeter, millele ei eelne suvand). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** tagastab stringi **"WINTER"**, kui praeguse Finance and Operationsi seansi kuupäev jääb vahemikku oktoober kuni detsember. Muidu tagastatakse tühi string. |
| IF (tingimus, väärtus 1, väärtus 2) | Annab vastuseks esimese määratud väärtuse, kui määratud tingimus on täidetud. Muul juhul annab vastuseks teise määratud väärtuse. Kui väärtus 1 ja väärtus 2 on kirjed või kirjeloendid, on tulemil ainult väljad, mis on olemas mõlemas loendis. | **IF (1=2, "condition is met", "condition is not met")** tagastab stringi **"condition is not met"**. |
| NOT (tingimus) | Tagastab määratud tingimuse tühistatud loogilise väärtuse. | **NOT (TRUE)** tagastab väärtuse **FALSE**. |
| AND (tingimus 1\[, tingimus 2, …\]) | Tagastab väärtuse **TRUE**, kui *kõik* määratud tingimused on tõesed. Muidu tagastatakse väärtus **FALSE**. | **AND (1=1, "a"="a")** tagastab väärtuse **TRUE**. **AND (1=2, "a"="a")** tagastab väärtuse **FALSE**. |
| OR (tingimus 1\[, tingimus 2, …\]) | Tagastab väärtuse **FALSE**, kui *kõik* määratud tingimused on väärad. Tagastab väärtuse **TRUE**, kui *mõni* määratud tingimustest on tõene. | **OR (1=2, "a"="a")** tagastab väärtuse **TRUE**. |

### <a name="mathematical-functions"></a>Matemaatilised funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| ABS (number) | Annab vastuseks määratud arvu absoluutväärtuse. (Teiste sõnadega annab vastuseks ilma märgita arvu). | **ABS (–1)** tagastab väärtuse **1**. |
| POWER (number, aste) | Tagastab määratud astmele määratud positiivse numbri tõstmise tulemi. | **POWER (10, 2)** tagastab väärtuse **100**. |
| NUMBERVALUE (string, kümnendkohaeraldaja, arvu rühmitamise eraldaja) | Teisendab määratud stringi numbriks. Määratud kümnendkoha eraldajat kasutatakse kümnendarvu täisarvu ja murdosa eraldamiseks. Määratud numbrikohtade rühmitamise eraldajat kasutatakse tuhandeliste eraldajana. | **NUMBERVALUE("1 234,56", ",", " ")** tagastab väärtuse **1234,56**. |
| VALUE (string) | Teisendab määratud stringi numbriks. Komasid ja punkte (.), loetakse komakohtade eraldajateks ning miinusmärki (–) kasutatakse negatiivse märgina. Ilmneb erand, kui määratud stringis on muid mittenumbrilisi märke. | **VALUE ("1 234,56")** annab erandi. |
| ROUND (number, kümnendkohad) | Annab vastuseks määratud numbri pärast selle ümardamist määratud arvu komakohtadeni.<ul><li>Kui **kümnendkohtade** parameetri väärtus on suurem kui 0 (null), ümardatakse määratud number nii paljude komakohtadeni.</li><li>Kui **kümnendkohtade** parameetri väärtus on **0** (null), ümardatakse määratud number lähima täisarvuni.</li><li>Kui **kümnendkohtade** parameetri väärtus on väiksem kui 0 (null), ümardatakse määratud number komakohast vasakule.</li></ul> | **ROUND (1200.767, 2)** ümardab kahe komakohani ja tagastab väärtuse **1200,77**. **ROUND (1200,767, –3)** ümardab lähima 1000 kordseni ja tagastab väärtuse **1000**. |
| ROUNDDOWN (number, kümnendkohad) | Annab vastuseks määratud numbri pärast selle allapoole ümardamist määratud arvu komakohtadeni.<blockquote>[!NOTE] See funktsioon toimib nagu **ROUND**, kuid see ümardab alati määratud numbrit allapoole (nulli poole).</blockquote> | **ROUNDDOWN (1200.767, 2)** ümardab allapoole kahe komakohani ja tagastab väärtuse **1200,76**. **ROUNDDOWN (1700.767, -3)** ümardab allapoole lähima 1000 kordseni ja tagastab väärtuse **1000**. |
| ROUNDUP (number, kümnendkohad) | Annab vastuseks määratud numbri pärast selle ülespoole ümardamist määratud arvu komakohtadeni.<blockquote>[!NOTE] See funktsioon toimib nagu **ROUND**, kuid see ümardab alati määratud numbrit ülespoole (nullist kaugemale).</blockquote> | **ROUNDUP (1200.763, 2)** ümardab ülespoole kahe komakohani ja tagastab väärtuse **1200,77**. **ROUNDUP (1200.767, -3)** ümardab ülespoole lähima 1000 kordseni ja tagastab väärtuse **2000**. |

### <a name="data-conversion-functions"></a>Andmete teisendamise funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| VALUE (string) | Teisendab määratud stringi numbriks. Komasid ja punkte (.), loetakse komakohtade eraldajateks ning miinusmärki (–) kasutatakse negatiivse märgina. Ilmneb erand, kui määratud stringis on muid mittenumbrilisi märke. | **VALUE ("1 234,56")** annab erandi. |
| NUMBERVALUE (string, kümnendkohaeraldaja, arvu rühmitamise eraldaja) | Teisendab määratud stringi numbriks. Määratud kümnendkoha eraldajat kasutatakse kümnendarvu täisarvu ja murdosa eraldamiseks. Määratud numbrikohtade rühmitamise eraldajat kasutatakse tuhandeliste eraldajana. | **NUMBERVALUE("1 234,56", ",", " ")** annab vastuseks tulemi **1234.56**. |
| INTVALUE (string) | Annab vastuseks määratud stringi täisarvu kujul. Kümnendkohad kärbitakse. | **INTVALUE ("100.77")** annab vastuseks **100**. |
| INTVALUE (number) | Annab vastuseks määratud arvu täisarvu kujul. Kümnendkohad kärbitakse. | **INTVALUE (-100.77)** annab vastuseks **–100**. |
| INT64VALUE (string) | Annab vastuseks määratud stringi kujul int64. Kümnendkohad kärbitakse. | **INT64VALUE ("22565422744")** annab vastuseks tulemi **22565422744**. |
| INT64VALUE (number) | Annab vastuseks määratud arvu kujul int64. Kümnendkohad kärbitakse. | **INT64VALUE (22565422744.00)** annab vastuseks **22565422744**. |

### <a name="record-functions"></a>Kirje funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| NULLCONTAINER (loend) | Tagastab kirje **null**, millel on sama struktuur kui määratud kirjeloendil või kirjel.<blockquote>[!NOTE] See funktsioon on aegunud. Kasutage selle asemel funktsiooni **EMPTYRECORD**.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille tagastab funktsioon **SPLIT**. |
| EMPTYRECORD (kirje) | Tagastab kirje **null**, millel on sama struktuur kui määratud kirjeloendil või kirjel.<blockquote>[!NOTE] **Nullkirje** on kirje, mille kõikidel väljadel on tühi väärtus. Tühi väärtus on arvude puhul **0** (null), stringide puhul tühi string jne.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille tagastab funktsioon **SPLIT**. |

### <a name="text-functions"></a>Tekstifunktsioonid

<table>
<thead>
<tr>
<th>Funktsioon</th>
<th>Kirjeldus</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (string)</td>
<td>Annab vastuseks määratud stringi pärast selle teisendamist suurtäheliseks.</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> tagastab väärtuse <strong>&quot;SAMPLE&quot;</strong>.</td>
</tr>
<tr>
<td>LOWER (string)</td>
<td>Annab vastuseks määratud stringi pärast selle teisendamist väiketäheliseks.</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> tagastab väärtuse <strong>&quot;sample&quot;</strong>.</td>
</tr>
<tr>
<td>LEFT (string, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringi algusest.</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> tagastab väärtuse <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr>
<td>RIGHT (string, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringi lõpust.</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> tagastab väärtuse <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr>
<td>MID (string, alguspositsioon, tähemärkide arv)</td>
<td>Tagastab määratud tähemärkide arvu määratud stringist, alustades määratust kohas.</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> tagastab väärtuse <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr>
<td>LEN (string)</td>
<td>Tagastab tähemärkide arvu määratud stringis.</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> tagastab väärtuse <strong>6</strong>.</td>
</tr>
<tr>
<td>CHAR (number)</td>
<td>Tagastab tähemärke stringi, millele viitab määratud Unicode'i number.</td>
<td><strong>CHAR (255)</strong> tagastab väärtuse <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE] Selle funktsiooni tagastatud string sõltub failivormingu ülemelemendis valitud kodeeringust. Toetatud kodeeringute loendi leiate teemast <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodeeringuklass</a>.</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (string 1 [, string 2, …])</td>
<td>Annab vastuseks kõik määratud tekstistringid pärast nende ühendamist üheks stringiks.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> tagastab väärtuse <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE] Avaldis <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> annab vastuseks samuti väärtuse <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (string, muster, asendus)</td>
<td>Annab vastuseks määratud stringi pärast kõigi määratud mustri stringi märkide asendamist määratud asendusstringis olevate vastavas kohas olevate tähemärkidega.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> asendab mustri <strong>&quot;cd&quot;</strong> stringiga <strong>&quot;GH&quot;</strong> ja tagastab väärtuse <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>REPLACE (string, muster, asendus, regulaaravaldise lipp)</td>
<td>Kui määratud regulaaravaldise lipp on <strong>tõene</strong>, tagastatakse määratud string, mida on muudetud, rakendades regulaaravaldist, mis on määratud selle funktsiooni musterargumendina. Seda avaldist kasutatakse asendatavate tähemärkide otsimiseks. Määratud asendusargumendi tähemärke kasutatakse leitud tähemärkide asendamiseks. Kui määratud regulaaravaldise lipp on <strong>väär</strong>, toimib see funktsioon nagu väärtus <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> rakendab regulaaravaldist, mis eemaldab kõik mittearvulised sümbolid ja tagastab väärtuse <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> asendab mustri <strong>&quot;cd&quot;</strong> stringiga <strong>&quot;GH&quot;</strong> ja tagastab väärtuse <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>TEXT (sisend)</td>
<td>Annab vastuseks määratud sisendi, mis on teisendatud tekstistringiks, mis on vormindatud praeguse Finance and Operationsi eksemplari serverilokaadi sätete kohaselt. <strong>Tõelist</strong> tüüpi väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.</td>
<td>Kui Finance and Operationsi eksemplari serverilokaat on määratletud kui <strong>EN-US</strong>, <strong>TEXT (NOW ())</strong>, siis annab vastuseks praeguse Finance and Operationsi seansi kuupäeva 17. detsember 2015 tekstistringina <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> tagastab väärtuse <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr>
<td>FORMAT (string 1, string 2[, string 3, …])</td>
<td>Annab määratud stringi, mille vormindamisel asendati <strong>%N</strong> esinemiskorrad <em>n</em>. argumendiga. Argumendid on stringid. Kui parameetril ei ole argumenti, tagastatakse parameeter stringis kui <strong>&quot;%N&quot;</strong>. <strong>Tõelist</strong> tüüpi väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.</td>
<td>Järgmises näites annab vastuseks andmeallikas <strong>PaymentModel</strong> komponendi <strong>Klient</strong> kaudu kliendikirjete loendi ja välja <strong>ProcessingDate</strong> kaudu töötlemise kuupäeva väärtuse.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>ER-i vormingus, mis on mõeldud looma valitud klientidele elektroonilist faili, valitakse <strong>PaymentModel</strong> andmeallikana ja see juhib protsessi voogu. Ilmneb erand, mis teavitab kasutajat sellest, kui valitud klient on peatatud kuupäeval, millal aruannet töödeldakse. Seda tüüpi töötlemise juhtimiseks koostatud valem saab kasutada järgmisi ressursse.</p>
<ul>
<li>Finance and Operationsi silt SYS70894, millel on järgmine tekst.
<ul>
<li><strong>Inglise keeles:</strong> &quot;Nothing to print&quot;</li>
<li><strong>Saksa keeles:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Finance and Operationsi silt SYS18389, millel on järgmine tekst.
<ul>
<li><strong>Inglise keeles:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>Saksa keeles:</strong> &quot;Debitor &#39;%1&#39; wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Koostada saab järgmise valemi.</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Kui töödeldakse kliendi <strong>Litware Retaili</strong> aruannet 17. detsembril 2015 kultuuris <strong>ET-EE</strong> ja keeles <strong>ET-EE</strong>, annab vastuseks see valem järgmise teksti, mida saab esitada erandliku teatena kasutajale:</p>
<p>&quot;Midagi pole printida. Customer Litware Retail is stopped for 12/17/2015.&quot;</p>
<p>Kui sama aruannet töödeldakse kliendi <strong> Litware Retail</strong> jaoks 17. detsembril 2015 kultuuris <strong>DE</strong> ja keeles <strong>DE</strong>, tagastab valem järgmise teksti, mis kasutab erinevat andmevormingut:</p>
<p>&quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE] Siltidele mõeldud ER-i valemites rakendatakse järgmist süntaksit.
<ul>
<li><strong>Finance and Operationsi ressursside siltide puhul:</strong> <strong>@&quot;X&quot;</strong>, kus X on sildi ID rakendusobjektide puus (AOT)</li>
<li><strong>ER-i konfiguratsioonides asuvate siltide puhul:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, kus X on sildi ID ER-i konfiguratsioonis</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (number, vorming)</td>
<td>Annab vastuseks määratud vormingus määratud numbri stringiesituse. (Teavet toetatud vormingute kohta vt jaotistest <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standardne</a> ja <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">kohandatud</a>.) Selle funktsiooni käitamise kontekst määrab kultuuri, mida kasutatakse numbrite vormindamiseks.</td>
<td>Ingliskeelses kultuuris tagastab <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> väärtuse <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> tagastab väärtuse <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (number, keel, valuuta, prindi valuuta nime lipp, kümnendkohad)</td>
<td>Tagastab määratud numbri pärast selle määratud keeles tekstistringideks kirjutamist (teisendamist). Keelekood ei ole kohustuslik. Kui see on määratletud tühja stringina, kasutatakse käitatava konteksti keelekoodi. (Käitatava konteksti keelekood määratletakse kausta või faili loomiseks). Valuutakood on samuti valikuline. Kui see on määratletud tühja stringina, kasutatakse ettevõtte valuutat.
<blockquote>[!NOTE] <strong>Valuuta nime printimise lipu</strong> ja <strong>kümnendkohtade</strong> parameetreid analüüsitakse ainult järgmiste keelekoodide puhul: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> ja <strong>RU</strong>. Peale selle analüüsitakse <strong>valuuta nime printimise lipu</strong> parameetrit ainult nende Finance and Operationsi ettevõtete puhul, mille riigi või piirkonna kontekst toetab valuuta nimede käänamist.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> annab vastuseks stringi <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, väär, 0)</strong> annab vastuseks stringi <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, tõene, 2)</strong> annab vastuseks stringi <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr>
<td>PADLEFT (string, pikkus, täidismärgid)</td>
<td>Annab vastuseks määratud pikkusega stringi, milles määratud stringi algusele on lisatud määratud märkidest koosnevad täidismärgid.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> annab vastuseks tekstistringi <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr>
<td>TRIM (string)</td>
<td>Annab vastuseks määratud tekstistringi pärast algus- ja lõputühikute kärpimist ning sõnade vahel olevate mitmekordsete tühikute eemaldamist.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Näidis&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;tekst&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> annab vastuse <strong>&quot;Näidistekst&quot;</strong>.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (loetelu andmeallika tee, loetelu väärtuse sildi tekst)</td>
<td>Annab vastuseks määratud loetelu andmeallika väärtuse selle loetelu sildi määratud teksti põhjal.</td>
<td>Järgmises näites on andmemudelis kasutusele võetud loetelu <strong>ReportDirection</strong>. Pange tähele, et loetelu väärtuste puhul on määratletud sildid.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Järgmises näites on toodud järgmised üksikasjad:</p>
<ul>
<li>Mudeli loetelu <strong>ReportDirection</strong> on lisatud aruandesse andmeallikana <strong>$Direction</strong>.</li>
<li>ER-i avaldis <strong>$IsArrivals</strong> on mõeldud kasutama mudeli loetelu selle funktsiooni parameetrina. Avaldise väärtus on <strong>TRUE</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (sisend)</td>
<td>Saate määratud sisendi andmetüübiga <strong>String</strong> teisendada andmeüksuseks andmetüübiga <strong>GUID</strong>.</td>
<td>Määratlege oma mudelivastenduses järgmised andmeallikad.
<ul>
<li><strong>myID</strong> (tüüp <strong>Arvutatud väli</strong>), mis sisaldab avaldist <strong>GUIDVALUE(&quot;AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0&quot;)</strong></li>
<li><strong>Kasutajad</strong> (tüüp <strong>Tabelikirjed</strong>), mis viitab tabelile UserInfo</li>
</ul>
Kui need andmeallikad on määratletud, saate kasutada avaldist, nt <strong>FILTER (Users, Users.objectId = myID)</strong>, et filtreerida tabel UserInfo andmetüübiga <strong>GUID</strong> välja <strong>objectId</strong> järgi.
</td>
</tr>
<tr>
<td>JSONVALUE (id, tee)</td>
<td>Saate andmeid sõeluda vormingus JavaScript Object Notation (JSON), millele pääseb juurde määratud tee kaudu ekstraktimaks määratud ID-l põhineva skalaarväärtuse.</td>
<td>Andmeallikas <strong>$JsonField</strong> sisaldab JSON-vormingus järgmisi andmeid: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. Selle andmeallika puhul tagastab avaldis </strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong> väärtuse <strong>7.3.1234.1</strong> andmetüübiga <strong>String</strong>.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Andmete teisendamise funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| TEXT (sisend) | Annab vastuseks määratud sisendi, mis on teisendatud tekstistringiks, mis on vormindatud praeguse Finance and Operationsi eksemplari serverilokaadi sätete kohaselt. **Tõelist** tüüpi väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga. | Kui Finance and Operationsi eksemplari serverilokaat on määratletud kui **EN-US**, annab **TEXT (NOW ())** vastuseks praeguse Finance and Operationsi seansi kuupäeva 17. detsember 2015 tekstistringina **"12/17/2015 07:59:23 AM"**. **TEXT (1/3)** tagastab väärtuse **"0,33"**. |
| QRCODE (string) | Tagastab määratud stringi puhul ruutkoodi (QR-koodi) pildi base64-binaarvormingus. | **QRCODE ("Näidistekst")** annab vastuse **U2FtcGxlIHRleHQ=**. |

### <a name="data-collection-functions"></a>Andmete kogumise funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Annab vastuseks praeguse vormingu elemendi nime. Annab vastuseks tühja stringi, kui praeguste failide lipp **Kogu väljundi üksikasjad** on välja lülitatud. | Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest **ER-i loendamise ja liitmise vormingu väljundi kasutusandmed**, mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa. |
| SUMIFS (liitmise võtmestring, kriteeriumivahemiku 1 string, kriteeriumiväärtuse 1 string \[, kriteeriumivahemiku2 string, kriteeriumiväärtuse2 string, …\]) | Annab vastuseks XML-i sõlmede väärtuste summa (koos võtmena määratletud nimega), mis on kogutud selle vormi käivitamise ajal ja mis täidab määratud tingimusi (vahemike ja väärtuste paarid). Annab vastuseks väärtuse **0** (null), kui praeguste failide lipp **Kogu väljundi üksikasjad** on välja lülitatud. | |
| SUMIF (liitmise võtmestring, kriteeriumivahemiku string, kriteeriumiväärtuse string) | Annab vastuseks XML-i sõlmede väärtuste summa (koos võtmena määratletud nimega), mis on kogutud selle vormi käivitamise ajal ja mis täidab määratud tingimust (vahemik ja väärtus). Annab vastuseks väärtuse **0** (null), kui praeguste failide lipp **Kogu väljundi üksikasjad** on välja lülitatud. | |
| COUNTIFS (kriteeriumivahemiku 1 string, kriteeriumiväärtuse 1 string \[, kriteeriumivahemiku2 string, kriteeriumiväärtuse2 string, …\]) | Annab vastuseks XML-i sõlmede arvu, mis on kogutud selle vormi käivitamise ajal ja mis täidab määratud tingimusi (vahemike ja väärtuste paarid). Annab vastuseks väärtuse **0** (null), kui praeguste failide lipp **Kogu väljundi üksikasjad** on välja lülitatud. | |
| COUNTIF (kriteeriumivahemiku string, kriteeriumiväärtuse string) | Annab vastuseks XML-i sõlmede arvu, mis on kogutud selle vormi käivitamise ajal ja mis täidab määratud tingimust (vahemik ning väärtus). Annab vastuseks väärtuse **0** (null), kui praeguste failide lipp **Kogu väljundi üksikasjad** on välja lülitatud. | |
| COLLECTEDLIST (kriteeriumivahemiku 1 string, kriteeriumiväärtuse 1 string \[, kriteeriumivahemiku2 string, kriteeriumiväärtuse2 string, …\]) | Annab vastuseks XML-i sõlmede väärtuste loendi, mis on kogutud selle vormi käivitamise ajal ja mis täidab määratud tingimusi (vahemik ning väärtus). Annab vastuseks tühja loendi, kui praeguste failide lipp **Kogu väljundi üksikasjad** on välja lülitatud. | |

### <a name="other-business-domainspecific-functions"></a>Muud (ettevõtte domeenipõhised) funktsioonid

| Funktsioon | Kirjeldus | Näide |
|----------|-------------|---------|
| CONVERTCURRENCY (summa, lähtekoha valuuta, sihtkoha valuuta, kuupäev, ettevõte) | Teisendab määratud rahasumma määratud lähtekoha valuutast määratud sihtkoha valuutaks, kasutades määratud kuupäeval määratud Finance and Operationsi ettevõtte sätteid. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** tagastab ühe euroga võrdse väärtuse USA dollarites praeguse seansi kuupäeval DEMF-i ettevõtte sätete alusel. |
| ROUNDAMOUNT (number, kümnendkohad, ümardamisreegel) | Ümardab määratus summa määratud kümnendkohtade arvule määratud ümardamisreegli kohaselt.<blockquote>[!NOTE] Ümardamisreegel peab olema määratud Finance and Operationsi loetelu **RoundOffType** väärtusena.</blockquote> | Kui parameeter **model.RoundOff** on seatud väärtusele **Allapoole**, annab vastuseks **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** väärtuse **1000.78**. Kui parameeter **model.RoundOff** on seatud väärtusele **Normaalne** või **Ülespoole ümardamine**, tagastab **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** väärtuse **1000,79**. |
| CURCredRef (arvud) | Tagastab kreeditori viite määratud arve numbri arvude alusel. | **CURCredRef ("VEND-200002")** tagastab väärtuse **"2200002"**. |
| MOD\_97 (arvud) | Tagastab kreeditori viite MOD97 avaldisena määratud arve numbri arvude alusel. | **MOD\_97 ("VEND-200002")** tagastab väärtuse **"20000285"**. |
| ISOCredRef (arvud) | Annab vastuseks Rahvusvahelise Standardiorganisatsiooni (ISO) kreeditori viite määratud arve numbri arvude ja tähestikus olevate sümbolite alusel.<blockquote>[!NOTE] ISO-ga ühildumatute sümbolite tähestikust eemaldamiseks tuleb sisendparameeter enne sellele funktsioonile edastamist tõlkida.</blockquote> | **ISOCredRef ("VEND-200002")** tagastab väärtuse **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (string, number) | Saate hankida määratud täiendav finantsdimensiooni ID. Parameetris **string** on dimensioonid esitatud komadega eraldatud ID-dena. Parameeter **number** määratleb taotletud dimensiooni seeriakoodi stringis. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** annab vastuseks stringi **"CC"**. |
| GetCurrentCompany () | Annab vastuseks selle juriidilise isiku (ettevõtte) koodi tekstkuju, kuhu kasutaja on praegu sisse loginud. | **GETCURRENTCOMPANY ()** annab vastuse **USMF** kasutaja puhul, kes on logitud sisse Finance and Operationsi ettevõttesse **Contoso Entertainment System USA**. |
| CH\_BANK\_MOD\_10 (numbrid) | Annab vastuseks kreeditori viite MOD10 avaldisena määratud arve numbri arvude alusel. | **CH\_BANK\_MOD\_10 ("VEND-200002")** annab vastuseks väärtuse **3**. |
| FA\_SUM (põhivara kood, väärtusmudeli kood, alguskuupäev, lõppkuupäev) | Annab vastuseks põhivarasumma ettevalmistatud andmekonteineri määratud perioodi kohta. | **FA\_SUM ("COMP-000001", "Praegune", Kuupäev1, Kuupäev2)** annab vastuseks põhivara **"COMP-000001"** ettevalmistatud andmekonteineri koos väärtusmudeliga **"Praegune"** perioodi **Kuupäev1** kuni **Kuupäev2** kohta. |
| FA\_BALANCE (põhivara kood, väärtusmudeli kood, aruandlusaasta, aruande kuupäev) | Annab vastuseks põhivarasaldo ettevalmistatud andmekonteineri. Aruandlusaasta peab olema määratud Finance and Operationsi loetelu **AssetYear** väärtusena. | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** annab vastuseks põhivara **"COMP-000001"** väärtusmudeliga **"Praegune"** saldode ettevalmistatud andmekonteineri praegusel 365 for Finance and Operationsi seansi kuupäeval. |
| TABLENAME2ID (string) | Annab vastuseks antud tabelinime tabeli ID täisarvu kujul. | **TABLENAME2ID ("Intrastat")** annab vastuse **1510**. |
| ISVALIDCHARACTERISO7064 (string) | Annab vastuseks kahendmuutuja **TRUE**, kui määratud string on kehtiv rahvusvaheline pangakonto number (IBAN). Muul juhul annab vastuseks kahendmuutuja väärtuse **FALSE**. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** annab vastuse **TRUE**. **ISVALIDCHARACTERISO7064 ("AT61")** annab vastuse **FALSE**. |

### <a name="functions-list-extension"></a>Funktsioonide loendi laiend

ER laseb laiendada nende funktsioonide loendit, mida kasutatakse ER-i avaldistes. Nõutav on mõni projekteerimise panus. Üksikasjalikuma teabe saamiseks vt jaotist [Elektroonilise aruandluse funktsioonide loendi laiendamine](general-electronic-reporting-formulas-list-extension.md).

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) funktsioonide loendi laiendamine](general-electronic-reporting-formulas-list-extension.md)

