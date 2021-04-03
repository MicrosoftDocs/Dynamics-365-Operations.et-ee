---
title: Rea definitsioonide lahtrite muutmine
description: Selles teemas kirjeldatakse teavet, mis on finantsaruandes nõutav readefinitsiooni iga lahtri puhul, ja selgitatakse, kuidas seda teavet sisestada.
author: ShylaThompson
manager: AnnBe
ms.date: 02/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6e1164166ece4df1257ef7300c1c68f4b20ec76c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564587"
---
# <a name="modify-row-definition-cells"></a>Rea definitsioonide lahtrite muutmine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse teavet, mis on finantsaruandes nõutav readefinitsiooni iga lahtri puhul, ja selgitatakse, kuidas seda teavet sisestada.

## <a name="specify-a-row-code-in-a-row-definition"></a>Rea koodi määramine readefinitsioonis

Readefinitsioonides määratlevad lahtri **Rea kood** numbrid või sildid readefinitsiooni igat rida. Andmetele viitamiseks arvutustes ja kogusummades saate määrata rea koodi.

### <a name="row-code-requirements"></a>Rea koodi nõuded

Rea kood on nõutav kõikide ridade puhul. Saate kombineerida readefinitsiooni numbrilisi, tähelisi ja määramata (tühje) rea koode. Rea kood võib olla mis tahes positiivne täisarv (alla 100 000 000) või rida määratlev kirjeldav silt. Kirjeldav silt peab järgima järgmisi reegleid.

- Silt peab algama tähega (a kuni z või A kuni Z) ning võib olla kuni 16 märki pikk kombinatsioon numbritest ja tähtedest.

    > [!NOTE]
    > Silt võib sisaldada allkriipsu (\_), kuid muud erimärgid pole lubatud.

- Silt ei saa kasutada järgmisi kinnissõnu: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO või RPO.

Järgmised näited on kehtivad rea koodid.

- 320
- TL\_NET\_INCOME
- TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Rea koodi muutmine readefinitsioonis

1. Klõpsake aruandekoosturis valikut **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Sisestage sobivale reale veeru **Rea kood** lahtrisse uus väärtus.

### <a name="reset-numeric-row-codes"></a>Numbriliste reakoodide lähtestamine

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Klõpsake menüüs **Redigeerimine** suvandit **Nummerda read ümber**.
3. Määratlege dialoogiboksis **Nummerda read ümber** esimese reakoodi ja reakoodi juurdekasvu uued väärtused. Saate lähtestada numbrilised reakoodid võrdselt jaotatud väärtustele. Aruandekoostur nummerdab ümber siiski ainult reakoodid, mis algavad numbritega (nt 130 või 246). See ei nummerda ümber rea koode, mis algavad tähtedega (nt INCOME\_93 või TP0693).

> [!NOTE]
> Reakoodide ümbernummerdamisel värskendab aruandekoostur viiteid **TOT** ja **CAL** automaatselt. Näiteks kui rida **TOT** viitab vahemikule, mis algab reakoodiga 100 ja nummerdate read ümber, alustades 90-ga, muutub alguse viide **TOT** väärtuselt 100 väärtusele 90.

## <a name="add-a-description"></a>Kirjelduse lisamine
Kirjelduse lahter kirjeldab aruanderea finantsandmeid, nagu Tulu või Netotulu. Lahtri **Kirjeldus** tekst kuvatakse aruandes täpselt nii, nagu selle readefinitsiooni sisestate.

> [!NOTE]
> Aruande kirjelduse veeru laius määratakse veeru definitsioonis. Kui veeru **Kirjeldus** tekst readefinitsioonis on pikk, kontrollige veeru **DESC** laiust. Dialoogiboksi **Sisesta read** kasutamisel on veeru **Kirjeldus** väärtused segmendi väärtused või finantsandmete dimensiooniväärtused. Võite kirjeldava teksti, nagu jaotise päis või kogusumma, ning vormingu, nagu kogusumma reale eelnev rida, lisamiseks ridu sisestada. Kui aruanne sisaldab aruandluspuud, saate kaasata aruandluspuus aruandlusüksuste puhul määratletud lisateksti. Samuti saate piirata konkreetse aruandlusüksuse lisateksti.

### <a name="add-the-description-for-a-line-on-a-report"></a>Aruande rea kirjelduse lisamine

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Valige lahter **Kirjeldus** ja sisestage seejärel aruande rea nimi.
3. Rakendage vormindus.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Lisateksti lisamine kirjelduse aruandluspuult

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Sisestage lisateksti kood ja muu tekst asjakohasesse lahtrisse **Kirjeldus**.
3. Rakendage vormindus.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Konkreetse aruandlusüksuse lisateksti piiramine

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Leidke rida, kuhu tuleks lisatekst luua ja seejärel topeltklõpsake lahtrit veerus **Seotud valemid/read/üksused**.
3. Valige aruandluspuu dialoogiboksi **Aruandlusüksuse valimine** väljalt **Aruandluspuu**.
4. Laiendage või ahendage väljal **Piirangu aruandlusüksuse valimine** aruandluspuud ja seejärel valige aruandlusüksus.

## <a name="add-a-format-code"></a>Vormingu koodi lisamine
Lahter **Vormingu kood** pakub selle rea sisu puhul eelvormindatud valikuid. Kui lahter **Vormingu kood** on tühi, tõlgendatakse rida finantsandmete üksikasjade reana.

> [!NOTE]
> Kui aruanne sisaldab mittesummalisi vorminguridu, mis on seotud peidetud summa ridadega (nt nullsaldode tõttu), saate kasutada veergu **Seotud valemid/read/ühikud** pealkirja ja vormingu ridade printimise vältimiseks.

### <a name="add-a-format-code-to-a-report-row"></a>Vormingu koodi lisamine aruande reale

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja valige seejärel muutmiseks readefinitsioon.
2. Topeltklõpsake lahtrit **Vormingu kood**.
3. Valige vormingu kood loendist. Järgmises tabelis kirjeldatakse vormingu koode ja nende toiminguid.

    | Vormingu kood                   | Vormingukoodi tõlgendus | Tegevus |
    |-------------------------------|-----------------------------------|--------|
    | (Pole)                        |                                   | Tühjendab lahtri **Vormingu kood**. |
    | TOT                           | Kokku                             | Tuvastab matemaatilisi tehtemärke kasutava rea veerus **Seotud valemid/read/üksused**. Kogusummad sisaldavad lihtsaid tehtemärke, nagu **+** või **-**. |
    | CAL                           | Kalkulatsioon                       | Tuvastab matemaatilisi tehtemärke kasutava rea veerus **Seotud valemid/read/üksused**. Arvutused sisaldavad keerukaid tehtemärke, nagu **+**, **-**, **\**_, _*/**, ja lauseid **IF/THEN/ELSE**. |
    | DES                           | Kirjeldus                       | Tuvastab aruande pealkirja rea või tühja rea. |
    | LFT RGT CEN                   | Vasakul, keskel, paremal                 | Joondab aruande lehel rea kirjelduse teksti olenemata teksti paigutusest veeru definitsioonis. |
    | CBR                           | Baasrea muutmine                   | Määrab veeru arvutuste puhul baasrea määrava rea. |
    | COLUMN                        | Veerupiir                      | Alustab aruandes uut veergu. |
    | PAGE                          | Lehepiir                        | Alustab aruandes uut lehte. |
    | \---                          | Üks allakriipsutus                  | Paneb aruande kõigi summa veergude alla ühe joone. |
    | ===                           | Kahekordne allakriipsutus                  | Paneb aruande kõigi summa veergude alla topeltjoone. |
    | LINE1                         | Peen joon                         | Joonistab üle lehe ühe peene joone. |
    | RIDA2                         | Paks joon                        | Tõmbab üle lehe ühe paksu joone. |
    | RIDA3                         | Punktiirjoon                       | Joonistab üle lehe ühe punktiiri. |
    | LINE4                         | Jäme ja peen joon          | Joonistab üle lehe topeltjoone. Ülemine joon on jäme ja alumine peen. |
    | LINE5                         | Peen ja jäme joon          | Joonistab üle lehe topeltjoone. Ülemine joon on peen ja alumine jäme. |
    | BXB BXC                       | Kastis rida                         | Joonistab kasti ümber aruande ridade, mis algavad reaga **BXB** ja lõppevad reaga **BXC**. |
    | REM                           | Märkus                            | Määratleb rea, mis on kommentaaririda ja mida ei tuleks aruandele printida. Näiteks võib märkuserida selgitada teie vormistamismeetodeid. |
    | SORT ASORT SORTDESC ASORTDESC | Sortimine                              | Sordib tulud või kulud, tegeliku või eelarve hälbe aruande suurima hälbe järgi või sordib rea kirjeldused tähestikuliselt. |

## <a name="specify-related-formulasrowsunits"></a>Seotud valemite/ridade/üksuste määramine
Lahtril **Seotud valemid/read/üksused** on mitu eesmärki. Olenevalt rea tüübist saab lahter **Seotud valemid/read/üksused** täita üht järgmistest funktsioonidest.

- Arvutusse kaasatavate ridade määratlemine, kui kasutate vormingu koodi **TOT** või **CAL**.
- Vormingu rea sidumine summa reaga nii, et vorming prinditakse ainult seotud summa printimisel.
- Rea piiramine konkreetse aruandlusüksusega.
- Baasrea määratlemine arvutuste puhul, kui kasutate vormingu koodi **BASEROW**.
- Sorditavate ridade määratlemine, kui kasutate mõnd järgmist vormingu koodi.

### <a name="use-a-row-total-in-a-row-definition"></a>Rea kogusumma kasutamine readefinitsioonis

Kasutage rea kogusumma valemit muude ridade summade liitmiseks või lahutamiseks. Rea kogusumma loomise valem võib sisaldada üksikute reakoodide ja vahemike kombineerimiseks tehtemärke + ja -. Vahemikke tähistab koolon (:). Valem võib sisaldada kuni 1024 märki. Järgmiselt on toodud standardne summeerimisvalem: 400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Rea kogusumma valemi komponendid

Rea kogusumma valemi loomisel peate kasutama reakoode, et määrata, milliseid ridu praeguses reamääratluses liita või lahutada, ning kasutama tehtemärke, et määrata ridade ühendamise viis. Kogusumma ridu ja summaridu saab kasutada mis tahes kombinatsioonides.

> [!NOTE]
> Kõik vahemikus olevad kogusummade read jäetakse välja. Lõppsumma loomiseks saate määrata ridade vahemiku. Kui vahemiku esimene rida on kogusumma rida, kaasatakse see rida uude kogusummasse. Järgmises tabelis kirjeldatakse tehtemärkide kasutamist rea kogusumma valemites.

| Operaator | Näidisvalem | Kirjeldus                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Lisab real 100 oleva summa real 330 olevale summale.        |
| :        | 100:330         | Lisab ridade 100 ja 330 vahel olevate kõigi ridade kogusummad.    |
| -        | 100-330         | Lahutab real 100 oleva summa real 330 olevast summast. |

### <a name="create-a-row-total"></a>Rea kogusumma loomine

1. Klõpsake aruandekoosturis suvandit **Readefinitsioonid** ja avage seejärel muudetav readefinitsioon.
2. Topeltklõpsake readefinitsioonis lahtrit **Vormingu kood** ja valige **TOT**.
3. Sisestage kogusumma valem lahtrisse **Seotud valemid/read/üksused**.

### <a name="relate-a-format-row-to-an-amount-row"></a>Vormingu rea sidumine summa reaga

Readefinitsiooni veerus **Vormingu kood** rakendavad vormingu koodid **DES**, **LFT**, **RGT**, **CEN**, **---** ja **===** vorminduse mittesumma ridadele. Selle vormingu printimise vältimiseks seotud summa ridade peitmisel (näiteks summa ridadel olevate nullväärtuste või perioodi aktiivsuse puudumise tõttu) peate seostama vormingu read asjakohaste summa ridadega. See funktsioon on kasulik, kui soovite takistada kogusummadega seotud päiste või vormingu printimise, kui perioodi puhul prinditavad üksikasjad puuduvad.

> [!NOTE]
> Saate takistada ka üksikasjaliku summa ridade printimise, tühjendades summadeta ridade kuvamise suvandi. See suvand asub aruande definitsiooni vahekaardil **Sätted**. Vaikimisi on nullsaldo või perioodi aktiivsuseta kande üksikasjade kontod aruannetes peidetud. Nende kande üksikasjade kontode kuvamiseks valige märkeruut **Kuva summadeta read** aruande definitsiooni vahekaardil **Sätted**.

### <a name="relate-a-format-row-to-an-amount-row"></a>Vormingu rea sidumine summa reaga

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja valige seejärel muutmiseks readefinitsioon.
2. Sisestage vormindamise rea lahtrisse **Seotud valemid/read/üksused** peidetava summa rea kood.

    > [!NOTE]
    > Summarea peitmiseks peab rea saldo olema 0 (null). Saldoga summa rida ei peideta.

3. Klõpsake menüüs **Fail** käsku **Salvesta**.

### <a name="example-of-preventing-printing-of-rows"></a>Ridade printimise vältimise näide

Järgmises näites soovib kasutaja vältida oma aruande rea **Sularahas kokku** pealkirja ja allkriipsude printimist, kuna tegevus mõlemal sularahakontol puudus. Seetõttu sisestab kasutaja reale 220 (mis, nagu vormingu kood **---** viitab, on vormindamise rida) lahtrisse **Seotud valemid/read/üksused** väärtuse **250**, mis on rea kood summa rea puhul, mille kasutaja soovib peita.

[![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Baasrea valimine veeru arvutamiseks
Suhtelises aruandluses määrate readefinitsioonis ühe või mitu baasrida, kasutades vormingu koodi **CBR** (baasrea muutmine). Baasreale viidatakse seejärel veeru definitsioonis arvutusega. Järgmiselt on toodud mõni tüüpiline näide CBR-arvutuste kohta.

- Tulu üksikute üksustega seotud kogutulu protsent
- Kulu üksikute üksustega seotud kogukulu protsent
- Allüksuse või osakonna üksikasjadega seotud kogutulu protsent.

Readefinitsioonis määratletakse üks või mitu baasrida ja seejärel määratleb veeru definitsioon seose, mille alusel baasrida esitatakse. Veeru valemis kasutatud kood on **BASEROW**. Suvandiga **BASEROW** kasutatakse järgmisi peamisi matemaatilisi tehtemärke: jagamine, korrutamine, liitmine või lahutamine. Kõige sagedamini kasutatav tehtemärk on jagamine suvandiga **BASEROW**, kus tulemus kuvatakse protsendina. Veeru arvutused, mis kasutavad valemis suvandit **BASEROW**, kasutavad seotud baasrea koodide puhul readefinitsiooni. Ridadel **CBR** on järgmised omadused.

- **CBR**-ridu lõpetatud aruandele ei prindita.
- Vormingu kood **CBR** ja sellega seotud rea kood asuvad seotud arvutusi kuvava rea või jaotise kohal.

Veerudefinitsioonis tähistab veeru tüüp **CALC** veergu, mis määrab real **Valem** valemi. See valem toimib aruande selle veeru andmetel ja kasutab märksõna Baserow arvutuste rajamiseks rea vormingu koodidele **CBR**. Readefinitsioonis määratleb vormingu kood **CBR** baasrea veergude puhul, mis arvutavad aruande iga rea puhul protsendi või korrutavad baasreaga. Teil võib olla rea vormingus mitu vormingu koodi **CBR**, näiteks üks netomüügi, üks brutomüügi ja üks kogukulude jaoks. Tavaliselt kasutatakse vormingu koodi **CBR** protsendi loomiseks kontode puhul, mida võrreldakse kogusumma reaga. Baasrida kasutatakse kõigi arvutuste puhul kuni teise baasrea määratlemiseni. Peate määrama alguse vormingu koodi **CBR** ja lõpu vormingu koodi **CBR**. Näiteks kulude määramiseks netomüügi protsendina saate jagada iga kulu rea väärtuse netomüügi rea väärtusega. Sellisel juhul on netomüügi rida baasrida. Saate määrata veeru definitsiooni, mis esitab tulemused aasta puhul ja aasta algusest praeguse kuupäevani koos iga tulemuse baasprotsendiga, nagu on näidatud järgmises näites. Alustage üksikasjaliku kasumiaruandega.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Baasrea valimine readefinitsioonis veeru arvutuse puhul

1. Klõpsake aruande kujundajas suvandit **Veeru definitsioonid** ja seejärel avage kasumiaruande veeru definitsioon.
2. Lisage veeru definitsiooni uus veerg ja seadke veeru tüübiks **CALC**.
3. Protsendi nägemiseks sisestage uue veeru lahtrisse **Valem** valem **X/BASEROW**, kus **X** on veeru tüüp **FD**.
4. Topeltklõpsake lahtrit **Vormingu/valuuta alistamine**.
5. Valige dialoogiboksi **Vormingu alistamine** loendist **Vormingu kategooria** suvand **Protsent** ja seejärel klõpsake nuppu **OK**.
6. Veeru definitsiooni salvestamiseks uue nimega klõpsake menüüs **Fail** käsku **Salvesta nimega**. Lisage **CBR** praeguse faili nimele (nt **CUR\_YTD\_CBR**). See veeru definitsioon on teie baasrea veeru definitsioon.
7. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon, kasutades baasrea arvutust.
8. Lisage uus rida rea kohale, kust baasrea arvutamine peaks algama.
9. Topeltklõpsake readefinitsiooni lahtrit **Vormingu kood** ja seejärel valige **CBR**.
10. Sisestage lahtrisse **Seotud valemid/read/üksused** baasrea rea koodi number.

### <a name="example-of-base-row-calculation"></a>Baasrea arvutamise näide

Järgmises readefinitsiooni näites näitab rida 100, et arvutuste baasreaks on rida 280.

[![Baasrea arvutamise näide.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png)

Järgmises veeru definitsiooni näites kasutavad arvutused vormingu koodi **CBR**. Arvutus veerus C jagab aruande veeru B väärtuse veeru B real 280 oleva väärtusega. Vormingu alistamine veerus B prindib arvutuse tulemuse protsendina. Samamoodi on iga veeru E summa veeru D summa netomüügi protsendina.

[![Veeru definitsiooni näide.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png)

Järgmises näites näidatakse aruannet, mis võidakse luua eelmiste arvutuste põhjal.

[![Eelmistel näidisarvutustel põhinev näidisaruanne.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Readefinitsiooni sortimiskoodi valimine
Sortimiskoodid sordivad kontod või väärtused, tegeliku või eelarve hälbe aruande suurima hälbe järgi või rea kirjeldused tähestikuliselt. Saadaval on järgmised sortimiskoodid:

- **SORT** – sordib aruande tõusvas järjestuses määratud veeru väärtuste põhjal.
- **ASORT** – sordib aruande tõusvas järjestuses määratud veeru väärtuste absoluutväärtuse põhjal. Teisisõnu ignoreeritakse väärtuste sortimisel iga väärtuse märki. See vormingu kood järjestab väärtused hälbe väärtuse järgi, olenemata sellest, kas hälve on positiivne või negatiivne.
- **SORTDESC** – sordib aruande laskuvas järjestuses määratud veeru väärtuste põhjal.
- **ASORTDESC** – sordib aruande laskuvas järjestuses määratud veeru väärtuste absoluutväärtuse põhjal.

### <a name="select-a-sorting-code"></a>Sortimiskoodi valimine

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Topeltklõpsake lahtrit **Vormingu kood** ja seejärel valige sortimiskood.
3. Määrake lahtris **Seotud valemid/read/üksused** sorditavate reakoodide vahemik. Vahemiku määramiseks sisestage esimene rea kood, koolon (:) ja seejärel viimane rea kood. Näiteks sisestage **160:490** määramaks, et vahemik on rida 160 kuni rida 490.
4. Sisestage lahtrisse **Veeru piirang** sortimisel kasutatava aruande veeru täht.

    > [!NOTE]
    > Kaasake sortimise arvutusse ainult summa read.

### <a name="examples-of-ascending-and-descending-column-values"></a>Tõusvate ja laskuvate veeru väärtuste näited

Järgmises näites sorditakse aruande veeru D väärtused tõusvas järjestuses ridade 160 kuni 490 puhul. Lisaks sorditakse aruande veeru G absoluutväärtused laskuvas järjestuses ridade 610 kuni 940 puhul.

| Rea kood | Kirjeldus                                         | Vormingu kood | Seotud valemid/read/üksused | Tavasaldo | Veerupiirang | Link finantsdimensioonidele |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Sorditud igakuise hälbe järgi tõusvas järjestuses       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Müük                                               |             |                             | C              |                    | 4100                         |
| 190      | Müügitagastused                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Intressitulu                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Sorditud YTD absoluuthälbe järgi laskuvas järjestuses | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Müük                                               |             |                             | C              |                    | 4100                         |
| 640      | Müügitagastused                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Intressitulu                                     |             |                             | C              |                    | 7000                         |


## <a name="specify-a-format-override-cell"></a>Vormingu alistamise lahtri määramine
Lahter **Vormingu alistamine** määrab aruande printimisel rea puhul kasutatava vormingu. Selline vorming alistab veeru definitsioonis ja aruande definitsioonis määratud vormingu. Vaikimisi on neis definitsioonides määratud vorminguks valuuta. Kui ühel aruande real loetletakse varade arv, nt ehitiste arv ja teisel real loetletakse nende varade rahaline väärtus, saate alistada valuuta vormingu ja sisestada numbrivormingu rea puhul, mis määrab ehitiste arvu. Saate selle teabe määrata dialoogiboksis **Vormingu alistamine**. Saadaolevad suvandid olenevad valitud vormingu kategooriast. Dialoogiboksi alal **Näidis** kuvatakse näidisvormingud. Saadaval on järgmised vormingu kategooriad.

- Valuuta vorming
- Arvuvorming
- Protsendivorming
- Kohandatud vorming

### <a name="override-cell-formatting"></a>Lahtri vormingu alistamine

1. Avage aruande kujundajas muudetav readefinitsioon.
2. Topeltklõpsake reas, mille puhul vorming alistada, lahtrit veerus **Vormingu alistamine**.
3. Valige dialoogiboksis **Vormingu alistamine** aruande selle rea puhul kasutatavad vormingusuvandid.
4. Klõpsake nupul **OK**.

### <a name="currency-formatting"></a>Valuuta vorming

Valuuta vorming rakendub eelarve summale ja sisaldab valuuta tähist. Valikud on järgmised:

- **Valuuta sümbol** aruandes kasutatav valuuta sümbol. See väärtus alistab ettevõtte teabe sätte **Piirkonnavalikud**.
- **Negatiivsed arvud** – negatiivsetel arvudel võib olla miinusmärk (–), need võivad olla sulgudes või kolmnurgaga (∆).
- **Kümnendkohad** – pärast kümnendkohta näidatavate numbrikohtade arv.
- **Nullväärtuse alistamise tekst** – aruandesse kaasatav tekst, kui summa on 0 (null). See tekst kuvatakse ala **Näidis** viimase reana.

    > [!NOTE]
    > Kui printimine on nullväärtuste või perioodi aktiivsuse puudumise puhul tõkestatud, on see tekst peidetud.

### <a name="numeric-formatting"></a>Arvuvorming

Arvuvorming rakendub mis tahes summale, mis ei sisalda valuuta tähist. Valikud on järgmised:

- **Negatiivsed arvud** – negatiivsetel arvudel võib olla miinusmärk (–), need võivad olla sulgudes või kolmnurgaga (∆).
- **Kümnendkohad** – pärast kümnendkohta näidatavate numbrikohtade arv.
- **Nullväärtuse alistamise tekst** – aruandesse kaasatav tekst, kui summa on 0 (null). See tekst kuvatakse ala **Näidis** viimase reana.

    > [!NOTE]
    > Kui printimine on nullväärtuste või perioodi aktiivsuse puudumise puhul tõkestatud, on see tekst peidetud.

### <a name="percentage-formatting"></a>Protsendivorming

Protsendivorming sisaldab protsendimärki (%). Valikud on järgmised:

- **Negatiivsed arvud** – negatiivsetel arvudel võib olla miinusmärk (–), need võivad olla sulgudes või kolmnurgaga (∆).
- **Kümnendkohad** – pärast kümnendkohta kuvatavate numbrikohtade arv.
- **Nullväärtuse alistamise tekst** – aruandesse kaasatav tekst, kui summa on 0 (null). See tekst kuvatakse ala **Näidis** viimase reana.

    > [!NOTE]
    > Kui printimine on nullväärtuste või perioodi aktiivsuse puudumise puhul tõkestatud, on see tekst peidetud.

### <a name="custom-formatting"></a>Kohandatud vorming

Kasutage kohandatud vormingu alistamise loomiseks kohandatud vormingu kategooriat. Valikud on järgmised:

- **Tüüp**: kohandatud vorming.
- **Nullväärtuse alistamise tekst** – aruandesse kaasatav tekst, kui summa on 0 (null). See tekst kuvatakse ala **Näidis** viimase reana.

    > [!NOTE]
    > Kui printimine on nullväärtuste või perioodi aktiivsuse puudumise puhul tõkestatud, on see tekst peidetud.

Tüüp peaks tähistama positiivset väärtust ja seejärel negatiivset väärtust. Üldjuhul sisestate sarnase vormingu, mis eristab positiivset ja negatiivset väärtust. Näiteks määramaks, et nii positiivsetel kui ka negatiivsetel väärtustel on kaks kümnendkohta, kuid negatiivsed väärtused kuvatakse sulgudes, sisestage **0.00;(0.00)**. Järgmises tabelis näidatakse kohandatud vorminguid, mida saate kasutada oma väärtuste vormingu juhtimiseks. Kõik näited algavad väärtusest 1234.56.

| Vorming                         | Positiivne   | Negatiivne     | Null    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);""       | 1,235      | (1,235)      | (tühi) |
| \#,\#\#0.00;(\#,\#\#0.00);null | 1,234.56   | (1,234.56)   | null    |
| 0.00%;(0.00%)                  | 123456.00% | (123456.00%) | 0.00%   |

## <a name="specify-a-normal-balance-cell"></a>Lahtri Normaalsaldo määramine
Readefinitsiooni lahter **Normaalsaldo** kontrollib rea summade märki. Rea märgi muutmiseks või juhul, kui konto normaalsaldo on krediit, sisestage selle rea puhul **C** lahtrisse **Normaalsaldo**. Aruandekoostur tühistab märgi kõigil selle rea krediidi bilansikontodel. Kui aruandekoostur neid kontosid teisendab, eemaldatakse kõikidelt kontodelt deebeti/kreediti näitaja ja seega muutub summeerimine lihtsamaks. Näiteks netotulu arvutamiseks lahutate kulud tulust. Üldjuhul kood **C** summeeritud ja arvutatud ridu ei mõjuta. Sellegipoolest muudab veeru definitsiooni prindi kontrollkood **XCR** märgi mis tahes rea puhul, mis sisaldab koodi **C** veerus **Normaalsaldo**. Selline vorming on eriti oluline, kui soovite kuvada kõik soovimatud hälbed negatiivsete summadena. Kui summeeritud või arvutatud arvul on vale märk, sisestage **C** lahtrisse **Normaalsaldo** muudetava märgiga rea puhul.

## <a name="specify-a-row-modifier-cell"></a>Lahtri Rea muutuja määramine
Readefinitsiooni lahtri **Rea muutuja** sisu alistab rahandusaastad, perioodid ja muu selle rea veeru definitsioonis määratud teabe. Valitud muutuja rakendub rea igale kontole. Saate muuta iga rida, kasutades ühte või mitut järgmist tüüpi muutujat.

- Konto muutujad
- Konteerimiskoodi muutujad
- Konto ja kande atribuudid

### <a name="override-a-column-definition"></a>Veeru definitsiooni alistamine

1. Avage aruande kujundajas muudetav readefinitsioon.
2. Topeltklõpsake reas, milles soovite veeru definitsiooni alistada, lahtrit **Rea muutuja**.
3. Valige suvand dialoogiboksi **Rea muutuja** väljalt **Konto muutuja**. Suvandite kirjelduse saamiseks vt jaotist Konto muutujad.
4. Valige väljalt **Konteerimiskoodi muutuja** rea puhul kasutatav konteerimiskood.
5. Järgige suvandis **Atribuudid** järgmisi etappe, et lisada kirje iga atribuudi puhul, mis tuleks reakoodi kaasata.

    1. Topeltklõpsake lahtrit **Atribuut** ja valige atribuudi nimi.

        > [!IMPORTANT]
        > Asendage numbrimärk (\#) arvväärtusega.

    2. Topeltklõpsake lahtrit **Alates** ja sisestage vahemiku esimene väärtus.
    3. Topeltklõpsake lahtrit **Kuni** ja sisestage vahemiku viimane väärtus.

6. Klõpsake nupul **OK**.

### <a name="account-modifiers"></a>Konto muutujad

Kindla konto valimisel kombineerib aruandekoostur üldjuhul konto ja rahandusaastad, perioodid ja muu veeru definitsioonis määratud teabe. Saate kindlate ridade puhul kasutada erinevaid andmeid, nt erinevaid rahandusperioode. Järgmises tabelis kuvatakse saadaolevad konto muutujad. Asendage numbrimärk (\#) väärtusega, mis on võrdne rahandusaasta perioodide arvuga või sellest väiksem.

| Konto muutuja | Print                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Konto algsaldo.                                                     |
| /\#              | Määratud perioodi saldo.                                                     |
| /-\#             | Saldo perioodi puhul, mis on \# perioodi enne praegust perioodi.                  |
| /+\#             | Saldo perioodi puhul, mis on \# perioodi pärast praegust perioodi.                   |
| /C               | Praeguse perioodi saldo.                                                       |
| /C-\#            | Saldo perioodi puhul, mis on \# perioodi enne praegust perioodi.                  |
| /C+\#            | Saldo perioodi puhul, mis on \# perioodi pärast praegust perioodi.                   |
| /Y               | Praeguse perioodi saldo kuni tänase kuupäevani.                                      |
| /Y-\#            | Kumulatiivne saldo kuni perioodini, mis on \# perioodi enne praegust perioodi. |
| /Y+\#            | Kumulatiivne saldo kuni perioodini, mis on \# perioodi pärast praegust perioodi.  |

### <a name="book-code-modifiers"></a>Konteerimiskoodi muutujad

Saate piirata rida olemasoleva konteerimiskoodiga. Veeru definitsioon peab sisaldama vähemalt ühte konteerimiskoodiga veergu **FD**.

> [!NOTE]
> Rea konteerimiskoodi piirang alistab selle rea veeru definitsiooni konteerimiskoodi piirangud.

### <a name="account-and-transaction-attributes"></a>konto- ja kandeatribuudid

Mõned raamatupidamissüsteemid toetavad finantsandmetes konto atribuute ja kande atribuute. Need atribuudid toimivad virtuaalsete kontosegmentidena ja võivad sisaldada lisateavet konto või kande kohta. Selleks lisateabeks võivad olla konto ID-d, partii ID-d, sihtnumbrid või muud atribuudid. Kui teie raamatupidamissüsteem toetab atribuute, saate kasutada konto atribuute või kande atribuute readefinitsioonis rea muutujatena. Lisateabe saamiseks rea teabe alistamise kohta vt selles artiklis varem toodud jaotist Veeru definitsiooni alistamine.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Lahtri Link finantsdimensioonidele määramine
Lahter **Link finantsdimensioonidele** sisaldab linke finantsandmetele, mis tuleks aruande igale reale lisada. See lahter sisaldab dimensiooniväärtusi. Dialoogiboksi **Dimensioonid** avamiseks topeltklõpsake lahtrit **Link finantsdimensioonidele**.

> [!NOTE]
> Aruande kujundaja ei saa valida kontosid, dimensioone ega välju Microsoft Dynamics ERP süsteemist, mis sisaldavad järgmisi kinnismärke: &, \*, \[, \], { või }. Readefinitsioonis juba olemasoleva rea teabe määratlemiseks lisage teave lahtrisse **Link finantsdimensioonidele**. Finantsandmetega seotavate uute ridade lisamiseks kasutage aruande definitsioonis uute ridade loomiseks dialoogiboksi **Sisesta read**. Veeru pealkiri muutub veeru konfiguratsioonist olenevalt, nagu on näidatud järgmises tabelis.

| Valitud seose tüüp       | Lingi veeru kirjeldus muutub järgmiseks |
|----------------------------------|----------------------------------------------------|
| Finantsdimensioonid             | Link finantsdimensioonidele                       |
| Aruande tööleht                 | Finantsaruandluse aruanne                         |

### <a name="specify-a-dimension-or-range"></a>Dimensiooni või vahemiku määramine

1. Avage aruandekoosturis muudetav readefinitsioon.
2. Topeltklõpsake veerus **Link finantsdimensioonidele** olevat lahtrit.
3. Topeltklõpsake dialoogiboksis **Dimensioonid** dimensiooni nime all olevat lahtrit.
4. Valige dimensiooni dialoogiaknas suvand **Üksik või vahemik**.
5. Sisestage väljale **Alates** algusdimensioon või klõpsake saadaolevate dimensioonide otsimiseks ikooni ![Sirvi](media/browse.gif "Sirvimine"). Dimensioonide vahemiku sisestamiseks sisestage lõppdimensioon väljale **Kuni**.
6. Dimensiooni dialoogiboksi sulgemiseks klõpsake nuppu **OK**. Dialoogiboksis **Dimensioonid** kuvatakse värskendatud dimensioon või vahemik.
7. Klõpsake nuppu **OK** dialoogiboksi **Dimensioonid** sulgemiseks.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Nullsaldo kontode kuvamine readefinitsioonis
Vaikimisi ei prindi aruandekoostur ridu, mille finantsandmetes pole asjakohast saldot. Seetõttu saate luua ühe readefinitsiooni, mis sisaldab kõiki füüsilise segmendi väärtusi või kõiki dimensiooniväärtusi ja kasutada seejärel seda readefinitsiooni mis tahes osakondade puhul.

### <a name="modify-zero-balance-settings"></a>Nullsaldo sätete muutmine

1. Avage aruande kujundajas muudetav aruande definitsioon.
2. Valige vahekaardi **Sätted** suvandi **Muu vorming** alt aruande definitsioonis kasutatavad readefinitsiooni suvandid.
3. Muudatuste salvestamiseks klõpsake menüü **Fail** käsku **Salvesta**.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Metamärkide ja vahemike kasutamine readefinitsioonis
Füüsilise segmendi väärtuse sisestamisel dialoogiboksi **Dimensioonid** saate panna metamärgi (? või \*) segmendi mis tahes kohta. Aruandekoostur ekstraktib kõik määratud asukohtade väärtused metamärke arvestamata. Näiteks sisaldab readefinitsioon ainult füüsilise segmendi väärtusi ja füüsilistel segmentidel on neli tähemärki. Sisestades reale **6???**, juhendate aruandekoosturit kaasama kõiki kontosid, mille füüsilise segmendi väärtus algab 6-ga. Kui sisestate **6\**_, saadakse samad tulemused, kuid tulemused sisaldavad ka muutuva laiusega väärtusi, nagu _* 60** ja **600000**. Aruandekoostur asendab iga metamärgi (?) võimalikud väärtuste vahemikuga, mis hõlmavad tähti ja erimärke. Näiteks vahemikus **12?0** kuni **12?4** asendatakse **12?0** metamärk märgistiku madalaima väärtusega ja **12?4** metamärk asendatakse märgistiku kõrgeima väärtusega.

> [!NOTE]
> Peaksite vältima metamärkide kasutamist vahemike algus- ja lõppkontode puhul. Algus- või lõppkontol metamärkide kasutamisel võite saada ootamatuid tulemusi.

### <a name="single-segment-or-single-dimension-ranges"></a>Ühe segmendi või ühe dimensiooni vahemikud

Saate määrata segmendiväärtuste või dimensiooniväärtuste vahemiku. Vahemiku määramise kasu seisneb selles, et te ei pea värskendama readefinitsiooni iga kord, kui uus segmendiväärtus või dimensiooniväärtus finantsandmetesse lisatakse. Näiteks vahemik **+Konto=\[6100:6900\]** tõmbab rea summasse väärtusi kontodelt 6100 kuni 6900. Kui vahemik sisaldab metamärki (?), ei hinda aruandekoostur vahemikku märgiti. Selle asemel määratakse vahemiku alam- ja ülempiirid ja seejärel kaasatakse piirväärtused ja kõik nendevahelised väärtused.

> [!NOTE]
> Aruande kujundaja ei saa valida kontosid, dimensioone ega välju Microsoft Dynamics ERP süsteemist, mis sisaldavad järgmisi kinnismärke: &, \*, \[, \], { või }. Saate ampersandi (&) lisada ainult juhul, kui loote readefinitsioone automaatselt, kasutades dialoogiboksi **Sisesta read dimensioonidest**.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Mitme segmendi või mitme dimensiooni vahemikud

Vahemiku sisestamisel mitme dimensiooniväärtuse kombinatsioone kasutades võrreldakse vahemikku ..\\finantsdimensioonid\\dimensioonipõhiselt. Vahemiku võrdlust ei saa teha märgiti või osalise segmendi alusel. Näiteks vahemik **+Konto=\[5000:6000\], Osakond=\[1000:2000\], Kulukeskus=\[00\]** hõlmab ainult iga segmendiga ühtivaid kontosid. Selles stsenaariumis peab esimene dimensioon olema vahemikus 5000 kuni 6000, teine dimensioon peab olema vahemikus 1000 kuni 2000 ja viimane dimensioon peab olema 00. Näiteks **+Konto=\[5100\], Osakond=\[1100\], Kulukeskus=\[01\]** ei kaasata aruandesse, kuna viimane segment jääb määratud vahemikust välja. Kui segmendi väärtus sisaldab tühikuid, pange see väärtus nurksulgudesse (\[ \]). Neljakohalise segmendi puhul kehtivad järgmised väärtused: **\[ 234\], \[123 \], \[1 34\]**. Dimensiooniväärtused peaks olema nurksulgudes (\[ \]) ja aruandekoostur lisab need sulud teie eest. Kui mitme segmendi või mitme dimensiooni vahemik sisaldab metamärke (? või \*), määratakse mitme segmendi või mitme dimensiooni vahemiku alam- ja ülempiirid ja seejärel kaasatakse piirväärtused ja kõik nendevahelised väärtused. Laia vahemiku soovimisel, nagu näiteks kogu kontode vahemiku 40 000 kuni 99 999 puhul peaksite võimaluse korral määrama kehtiva algus- ja lõppkonto.

> [!NOTE] 
> Aruande kujundaja ei saa valida kontosid, dimensioone ega välju Microsoft Dynamics ERP süsteemist, mis sisaldavad järgmisi kinnismärke: &, \*, \[, \], { või }. Saate ampersandi (&) lisada ainult juhul, kui loote readefinitsioone automaatselt, kasutades dialoogiboksi **Sisesta read dimensioonidest**.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Readefinitsiooni muude kontode liitmine või lahutamine
Ühe konto rahasummade liitmiseks teise konto rahasummadele või neist lahutamiseks saate kasutada plussmärki (+) ja miinusmärk (–) lahtris **Link finantsdimensioonidele**. Järgmises tabelis kuvatakse linkide finantsandmetele liitmise ja lahutamise puhul lubatud vormingud.

| Toiming                                                                               | Kasutatav vorming                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Kahe täielikult kvalifitseeritud konto liitmine.                                                       | +Divisjon=\[000\], Konto=\[1205\], Osakond=\[00\]+Divisjon=\[100\], Konto=\[1205\], Osakond=\[00\] |
| Kahe segmendiväärtuse liitmine.                                                                 | +Konto=\[1205\]+Konto=\[1210\]                                                                           |
| Metamärke sisaldavate segmendiväärtuste liitmine.                                    | +Konto=\[120?+Konto=\[11??\]                                                                             |
| Täielikult kvalifitseeritud kontode vahemiku liitmine.                                                | +Divisjon=\[000:100\], Konto=\[1205\], Osakond=\[00\]                                                   |
| Segmendiväärtuste vahemiku liitmine.                                                          | +Konto=\[1200:1205\]                                                                                       |
| Metamärke sisaldavate segmendiväärtuste vahemiku liitmine.                         | +Konto=\[120?:130?\]                                                                                       |
| Ühe täielikult kvalifitseeritud konto lahutamine teiselt täielikult kvalifitseeritud kontolt.              | +Divisjon=\[000\], Konto=\[1205\], Osakond=\[00\]-Divisjon=\[100\], Konto=\[1205\], Osakond=\[00\] |
| Ühe segmendiväärtuse lahutamine teiselt segmendiväärtuselt.                                  | +Konto=\[1205\]-Konto=\[1210\]                                                                           |
| Metamärki sisaldava segmendiväärtuse lahutamine teiselt segmendiväärtuselt. | +Konto=\[1200\]-Konto=\[11??\]                                                                           |
| Täielikult kvalifitseeritud kontode vahemiku lahutamine.                                           | -Divisjon=\[000:100\], Konto=\[1200:1205\], Osakond=\[00:01\]                                           |
| Segmendiväärtuste vahemiku lahutamine.                                                     | -Konto=\[1200:1205\]                                                                                       |
| Metamärke sisaldavate segmendiväärtuste vahemiku lahutamine.                    | -Konto=\[120?:130?\]                                                                                       |

Ehkki saate kontosid otse muuta, saate finantsandmete linkidele õige vormingu rakendamiseks kasutada ka dialoogiboksi **Dimensioonid**. Väärtused võivad sisaldada metamärke (? või \*). Aruande kujundaja ei saa aga valida kontosid, dimensioone ega välju Microsoft Dynamics ERP süsteemist, mis sisaldavad järgmisi kinnismärke: &, \*, \[, \], { või }.

> [!NOTE]
> Väärtuste lahutamiseks peate need väärtused sulgudesse panema. Näiteks kui sisestate **450?-(4509)**, kuvatakse see kui **+Konto=\[4509\]-Konto=\[450?\]** ja juhendate aruandekoosturit lahutama konto segmendi 4509 summat mis tahes konto segmendi summast, mis algab 450-ga.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Kontode liitmine muudele kontodele või neist lahutamine

1. Avage aruande kujundajas muudetav readefinitsioon.
2. Topeltklõpsake asjakohasel real veeru **Link finantsdimensioonidele** lahtrit.
3. Järgige dialoogiboksi **Dimensioonid** esimeses reas järgmisi etappe.

    1. Valige esimesel väljal kõik dimensioonid (vaikimisi) või klõpsake dialoogiboksi **Dimensioonikogumite haldamine** avamiseks, milles saate kogumi luua, seda muuta, kopeerida või kustutada.
    2. Topeltklõpsake lahtrit **Tehtemärk +/-** ja valige tehtemärk pluss (**+**) või miinus (**-**), mis rakendub rea ühele või enamale dimensiooniväärtusele või kogumile.
    3. Topeltklõpsake sobiva dimensiooniväärtuse veerus lahtrit dialoogiboksi **Dimensioonid** avamiseks ja valige, kas see dimensiooniväärtus on üksiku või vahemiku, dimensiooniväärtuste kogumi või kontode summeerimise jaoks. Dialoogiboksi **Dimensioonid** väljade kirjelduste saamiseks vt jaotist Dimensiooni dialoogiboksi kirjeldus.
    4. Sisestage segmendi väärtused veergu **Alates** ja veergu **Kuni**.

4. Tehete lisamiseks korrake etappe 2 kuni 3.

> [!NOTE]
> Tehtemärk rakendub rea kõigile dimensioonidele.

## <a name="description-of-the-dimensions-dialog-box"></a>Dialoogiboksi Dimensioonid kirjeldus
Järgmises tabelis kirjeldatakse dialoogiboksi **Dimensioonid** välju.

| Kaup                | Kirjeldus |
|---------------------|-------------|
| Üksik või vahemik | Sisestage väljale **Alates** konto nimi või klõpsake nuppu **Sirvi** ![Sirvi](media/browse.gif "Sirvimine") konto sirvimiseks. Vahemiku valimiseks sisestage väärtus või sirvige seda väljal **Kuni**. |
| Dimensiooniväärtuste kogum | Sisestage dimensiooniväärtuste kogumi nimi väljale **Nimi**. Kogumi loomiseks, muutmiseks, kopeerimiseks või kustutamiseks klõpsake suvandit **Dimensiooniväärtuste kogumite haldamine**. Väli **Valem** täidetakse valemiga lahtrist **Link finantsdimensioonidele** readefinitsioonis määratud dimensiooniväärtuse puhul. |
| Kontode summeerimine   | Sisestage kontode summeerimise dimensioon väljale **Nimi** või sirvige seda sellel väljal. Väli **Vorming** asustatakse valemiga lahtris **Link finantsdimensioonidele** aruande definitsiooni selle konto summeerimise puhul. |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Dimensiooniväärtuste kogumite lisamine readefinitsioonis
Dimensiooniväärtuste kogum on dimensiooniväärtuste nimega grupp. Dimensiooniväärtuste kogum võib sisaldada väärtusi ainult ühes dimensioonis, kuid dimensiooniväärtuste kogumit saate kasutada mitmes readefinitsioonis, veeru definitsioonis, aruandluspuu definitsioonis ja aruande definitsioonis. Ühtlasi saate dimensiooniväärtuste kogumeid aruande definitsioonis kombineerida. Kui teie finantsandmete muutmine nõuab, et muudaksite dimensiooniväärtuste kogumit, saate dimensiooniväärtuste kogumi definitsiooni värskendada ja see värskendus rakendub kõigile seda dimensiooniväärtuste kogumit kasutavatele aladele. Näiteks kui viitate tihti oma finantsandmetega seotavatele väärtuste vahemikule, nagu väärtused 5100 kuni 5600, saate määrata selle vahemiku kontode kogumile nimega Müük. Pärast dimensiooniväärtuste kogumi loomist võite selle kogumi oma finantsandmete lingiks valida. Teine näide: kui kontokogumisse Müük on määratud väärtuste vahemik 5100 kuni 5600 ning kontokogumisse Allahindlused on määratud 4175, saate müügi kogusumma määratleda, lahutades kogumist Müük kogumi Allahindlused. Sellele tehtele viidatakse järgmiselt: **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Dimensiooniväärtuste kogumi loomine

1. Avage aruande kujundajas muudetav rea, veeru või puu definitsioon.
2. Klõpsake menüüs **Redigeeri** suvandit **Dimensiooniväärtuste kogumite haldamine**.
3. Valige dialoogiboksi **Dimensiooniväärtuste kogumite haldamine** väljal **Dimensioon** loodava dimensiooniväärtuste kogumi tüüp ja klõpsake seejärel suvandit **Uus**.
4. Sisestage kogumi nimi ja kirjeldus dialoogiboksi **Uus**.
5. Topeltklõpsake lahtrit veerus **Alates**.
6. Valige dialoogiboksi **Konto** loendist konto nimi või otsige kirjet väljalt **Otsing**. Seejärel klõpsake nuppu **OK**.
7. Selle tehtemärgi puhul valemi loomiseks korrake veerus **Kuni** etappe 5 kuni 6.
8. Kui valem on lõpetatud, klõpsake nuppu **OK**.
9. Klõpsake dialoogiboksis **Dimensioonikogumite haldamine** käsku **Sulge**.

### <a name="update-a-set-of-dimension-values"></a>Dimensiooniväärtuste kogumi värskendamine

1. Avage aruandekoosturis muudetav rea-, veeru- või aruandluspuu definitsioon.
2. Klõpsake menüüs **Redigeeri** suvandit **Dimensiooniväärtuste kogumite haldamine**.
3. Valige dimensiooni tüüp dialoogiboksi **Dimensiooniväärtuste kogumite haldamine** väljalt **Dimensioon**.
4. Valige loendist värskendatav dimensiooniväärtuste kogum ja seejärel klõpsake käsku **Muuda**.
5. Muutke dialoogiboksis **Muutmine** kogumisse kaasatava valemi väärtusi.

    > [!NOTE]
    > Uute kontode või dimensioonide lisamisel veenduge, et muudaksite muudatuste kaasamiseks olemasolevaid dimensiooniväärtuse kogumeid.

6. Topeltklõpsake lahtrit ja valige sobiv tehtemärk, konto **Alates** ja konto **Kuni**.
7. Klõpsake nuppu **OK** dialoogiboksi **Muutmine** sulgemiseks ja muudatuste salvestamiseks.

### <a name="copy-a-dimension-set"></a>Dimensioonikogumi kopeerimine

1. Avage aruande kujundajas muudetav rea, veeru või puu definitsioon.
2. Klõpsake menüüs **Redigeeri** suvandit **Dimensiooniväärtuste kogumite haldamine**.
3. Valige dimensiooni tüüp dialoogiboksi **Dimensiooniväärtuste kogumite haldamine** väljalt **Dimensioon**.
4. Valige loendist kopeeritav kogum ja klõpsake seejärel käsku **Salvesta nimega**.
5. Sisestage kopeeritud kogumi uus nimi ja seejärel klõpsake nuppu **OK**.

### <a name="delete-a-dimension-set"></a>Dimensioonikogumi kustutamine

1. Avage aruandekoosturis muudetav rea-, veeru- või aruandluspuu definitsioon.
2. Klõpsake menüüs **Redigeeri** suvandit **Dimensiooniväärtuste kogumite haldamine**.
3. Valige dimensiooni tüüp dialoogiboksi **Dimensiooniväärtuste kogumite haldamine** väljalt **Dimensioon**.
4. Valige kustutatav kogum ja klõpsake seejärel käsku **Kustuta**. Dimensiooniväärtuste kogumi jäädavaks kustutamiseks klõpsake suvandit **Jah**.

## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandlus](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]