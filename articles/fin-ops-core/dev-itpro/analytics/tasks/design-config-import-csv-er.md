---
title: Elektroonilise aruandluse konfiguratsioonide kujundamine andmete importimiseks välistest CSV-failidest
description: Kasutage seda protseduuri, et kujundada elektroonilise aruandluse konfiguratsioone andmete importimiseks CSV-vormingus välisest failist rakendusse Finance and Operations.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b42f0cf8c7260c85d405a5dfdcd50323ffee4d4528b982997a802b859ab8327b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747267"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>Elektroonilise aruandluse konfiguratsioonide kujundamine andmete importimiseks välistest CSV-failidest

[!include [banner](../../includes/banner.md)]

Kasutage seda protseduuri, et kujundada elektroonilise aruandluse (ER) konfiguratsioone andmete importimiseks CSV-vormingus välisest failist. Protseduuri järgides loote näidisettevõtte Litware, Inc. jaoks vajalikud ER-i konfiguratsioonid. Ülesannete lõpetamiseks peab esmalt täitma protseduuris „ER konfiguratsioonipakkuja loomine ja selle aktiivseks märkimine” toodud toimingud.

Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia USMF-i andmekomplekti abil.

Samuti peate alla laadima ja kohalikult salvestama järgmised failid: [Rakenduse Dynamics 365 Finance elektroonilise aruandluse näited](https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Saate konfigureerida protsessi XML-, TXT- või CSV-vormingus väliste failide tabelitesse importimiseks. Esmalt peate looma abstraktse andmemudeli, mis esindab imporditud andmed ettevõtte seisukohalt – selleks on loodud ER-i andmemudeli konfiguratsioon. Järgmisena määratlege imporditud faili struktuur, mis vastab loodud andmemudelile, et portida andmed failist abstraktsesse andmemudelisse – selleks on loodud ER-vorming konfiguratsioon. Seejärel tuleb ER-i andmemudeli konfiguratsiooni laiendada uue mudeli vastendusega, mis kirjeldab, kuidas imporditud failist pärinevaid andmeid ja abstraktse andmemudeli kinnistatud andmeid kasutatakse rakendusetabelite või andmeüksuste värskendamiseks.
    * Järgmised toimingud näitavad, kuidas väliselt jälgitavate hankijate kanded imporditakse välisest CSV-failist, et neid hiljem kasutada 1099 vormides hankija tasakaalustuses.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” esitatud juhised.
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Rakendage filter „1099 maksete mudel”. Kui olete juba lõpule viinud protseduuri „Vajalike konfiguratsioonide loomine välisest failist andmete importimiseks elektroonilise aruandluse jaoks” ja konfiguratsioon „1099 maksete mudel” on konfiguratsioonipuus saadaval, jätke kõik järgmise alamülesande toimingud vahele.

## <a name="add-a-new-er-model-configuration"></a>Uue elektroonilise aruandluse mudeli konfiguratsiooni lisamine

1. Andmeimpordi toetamiseks uue mudeli loomise asemel laadige varasemalt allalaaditud fail 1099model.xml. See fail sisaldab hankijakannete kohandatud andmemudelit. See andmemudel on juba vastendatud vajalike andmekomponentidega.
2. Klõpsake nuppu Vahetus.
3. Klõpsake nuppu Laadi XML-failist.
4. Klõpsake nuppu Sirvi ja navigeerige varasemalt allalaaditud failini 1099model.xml.
5. Klõpsake nuppu OK.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Uue andmete importimist toetava elektroonilise aruandluse vormingu konfiguratsiooni lisamine

1. Puuvaates valige „1099 maksete mudel”.
2. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
3. Väljale Uus sisestage „Andmemudeli 1099 maksete mudelil põhinev vorming”.
4. Väljal Toetab andmeimporti valige Jah.
5. Selle lehekülje sulgemiseks vajutage klahvi ESC.
    * Andmeimpordi toetamiseks uue ER-i vormingu loomise asemel laadige varasemalt allalaaditud fail 1099formatcsv.xml. See fail sisaldab nõutavat ER-i vormingut, mis määratleb sissetuleva CSV-faili struktuuri ning struktuuri ja hankijakannete andmemudeli vastendamise.
6. Klõpsake nuppu Vahetus.
7. Klõpsake nuppu Laadi XML-failist.
    * Klõpsake nuppu Sirvi ja navigeerige varasemalt allalaaditud failini 1099formatcsv.xml.
8. Klõpsake nuppu OK.
9. Puuvaates laiendage valikut „1099 maksete mudel”.
10. Puuvaates valige „1099 maksete mudel\Hankijakannete importimiseks (CSV)”.

## <a name="review-format-settings"></a>Vormingu sätete ülevaatamine

1. Klõpsake valikut Kujundaja.
2. Klõpsake nuppu Laienda/ahenda.
3. Lülitage nupp Kuva üksikasjad sisse.
    * Kujundatud vorming tähistab CSV-vormingus välise faili eeldatavat struktuuri.
4. Valige puul „Sissetulev: fail\Juur: seeria”.
    * Tüübiga SEQUENCE juurelemendi jaoks on väljal „Erimärgid” valitud suvand „Uus rida – Windows (CR LF)”. Selle sätte alusel tuleb sõelumisfaili iga rida arvestada eraldi kirjena.
5. Valige puul suvand `Incoming: File\Root: Sequence\Line: Sequence 1..*`.
    * Tüübiga SEQUENCE elemendi Juur\Rida jaoks on väljal „Mitmekordsus” valitud suvand „Üks, mitu”. Selle sätte alusel esitatakse sõelumisfailis vähemalt üks rida.
6. Valige puul suvand `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case`.
    * Pange tähele, et tüübiga CASE element Juur\Rida\Tüübid on lisatud seeriasse Juur\Rida pesastatud elemendina. See element CASE sisaldab 3 pesastatud seeriaelementi, mistõttu säte eeldab, et sõelumisfail peaks sisaldama 3 eri tüüpi ridu.
7. Valige puul suvand `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1`.
    * Tüübiga SEERIA element Juur\Rida\Tüübid\Päis sisaldab pesastatud elementi STRING, mille väärtus on määratletud fikseeritud stringiväärtusena. See seeria sõelub sõelumisfaili päiserida.
8. Valige puul suvand `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)`.
    * Tüübiga SEQUENCE element Juur\Rida\Tüübid\Kirje on konfigureeritud sõeluma kanderidu. Pange tähele, et valiku „Kohandatud eraldaja” tähemärgiks on seatud koma. See tähendab, et koma kasutatakse väljade eraldajana sõelumisfaili seda tüüpi rea puhul.
    * Pange tähele, et erinevate andmetüüpide paljud pesastatud elemendid on lisatud elementi Juur\Rida\Tüübid\Kirje, et sõeluda kanderidu eraldi väljadena. Pange tähele, et valik „Pakkumise avaldus” on seatud väärtusele „Puudub”. See tähendab, et sõelumisfailis eeldatakse kõigi seda tüüpi väljade puhul, et need ei sisalda lisatud märke.
9. Valige puul suvand `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime`.
    * Näiteks tüübiga DATETIME element Juur\Rida\Tüübid\Kirje\TransactionDate on konfigureeritud nii, et see hangiks kande kuupäeva ja kellaaja sõelumisfailist vormingus k/p/aaaa.
10. Valige puul suvand `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1`.
    * Pange tähele, et tüübiga STRING element Juur\Rida\Tüübid\Kirje\CountryCode on konfigureeritud nii, et väljal „Mitmekordsus” on valitud „Null, üks”. Säte peab sõelumisrea väljal CountryCode olevat väärtust valikuliseks.
11. Valige puul suvand `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,)`.
    * Pange tähele, et tüübiga SEQUENCE element Juur\Rida\Tüübid\Kirje\Märkus on konfigureeritud nii, et väljal „Pakkumise avaldus” on valitud „Kõik” ja väljal „Jutumärgid” on valitud topeltjutumärgid. See tähendab, et kõik seda tüüpi ridadega väljad sõelumisfailis (mida kirjeldavad pesastatud elemendid: tekst tüübiga STRING) loetakse topeltjutumärkidega ümbritsetuks.
12. Valige puul suvand `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1`.
    * Tüübiga SEQUENCE element Juur\Rida\Tüübid\Sõelumata on konfigureeritud sõeluma selle struktuuri kanderidu, mis ei vasta ülal emaelemendis CASE kirjeldatud struktuurile.

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Vaadake üle vormingu andmemudeliga vastendamise säte

1. Klõpsake nuppu Vormingu vastendamine mudeliga.
    * Mudeli vastendus „CSV-vormingu vastendamine mudeliga” kirjeldab sissetuleva CSV-faili ja andmemudeli vahelise andmeedastuse andmevoogu.
2. Klõpsake valikut Kujundaja.
3. Laiendage puul valikut „format”.
    * Pange tähele, et kujundatud vormingut tähistatakse siin andmeallika komponendina.
4. Laiendage puul valikut „vorming\Sissetulev: fail (sissetulev)”.
5. Laiendage puul jaotist „vorming\Sissetulev: fail (sissetulev)\Juur: seeria (juur)”.
6. Laiendage puul valikut `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)`.
7. Laiendage puul valikut `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)`.
8. Laiendage puul valikut `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)`.
9. Laiendage puul valikut `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data`.
10. Laiendage puul valikut `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode)`.
11. Valige puul suvand `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate)`.
    * Pange tähele, et nõutavad ja valikulised vorminguelemendid, nagu TransactionDate ja CountryCode, näevad eelmääratletud andmeallika komponendis „Vorming” teistsugused välja.
12. Laiendage puul valikut „Kanded = '$both'”.
    * Pange tähele, et imporditud faili struktuuri määratleva vormingu elemendid on seotud andmemudeli elementidega. Nende sidumiste põhjal salvestatakse imporditud CSV-fail käitusajal olemasolevasse andmemudelisse. Pöörake tähelepanu elemendi CountryRegion sidumisele. Sissetulevas failis, milles pole riigikoodi väärtust määratud, täidetakse mis tahes kande elemendi puhul vaikimisi riigikood „USA” andmemudelis.
13. Lülitage nupp „Kuva üksikasjad” sisse.
14. Klõpsake vahekaarti Kinnitused.
15. Klõpsake nuppu Otsing.
16. Väljale Otsi sisestage „vend”.
17. Klõpsake nuppu Otsi järgmine.
    * See vormingu vastendamine võib sisaldada kasutaja määratud loogikat, et kinnitada imporditud andmete täpsust ettevõtte seisukohalt. Näiteks kui imporditava faili struktuuri mõne rea struktuur ei vasta päiserea ega kanderea struktuurile, luuakse sätte alusel teabelogisse hoiatusteade, mis teavitab kasutajat juhtumist ja viitab kande järjekorranumbrile failis.
18. Sulgege leht.

## <a name="run-the-format-mapping"></a>Vormingu vastendamise käitamine

Testimiseks käivitage vorminduse vastendamine varem alla laaditud failiga 1099entriescsv.csv. Loodud väljund esitab andmeid, mis imporditakse valitud CSV-failist ja täidetakse reaalsel importimisel kohandatud andmemudeliga.

1. Klõpsake nuppu Käivita.
    * Klõpsake nuppu Sirvi ja navigeerige varasemalt allalaaditud failini 1099entriescsv.csv.
2. Klõpsake nuppu OK.
    * Pange tähele, et ridadega seotud hoiatusteateid ei võeta vastu. 4. rida sisaldab sissetuleku väärtust, mis on esitatud sobimatus vormingus, samas kui 7. rida ei sisalda kande märkust topeltjutumärkides.
    * Vaadake väljund üle XML-vormingus, mis tähistab valitud failist imporditud ja andmemudelisse porditud andmeid. Pange tähele, et imporditud CSV-faili kõiki 7 rida töödeldi. Sisalduvate väljade pealkirjade rida 1 jäeti vahele, 4 kannet sõeluti õigesti ja 2 kannet osutusid kehtetuks.
3. Sulgege leht.
4. Sulgege leht.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]