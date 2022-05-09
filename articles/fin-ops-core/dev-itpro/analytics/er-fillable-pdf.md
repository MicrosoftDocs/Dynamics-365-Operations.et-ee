---
title: ER-i konfiguratsioonide koostamine PDF-mallide täitmiseks
description: Selles teemas antakse teavet selle kohta, kuidas kujundada elektroonilise aruandluse (ER) vormingut PDF-malli täitmiseks.
author: NickSelin
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 706256300cf0b64bc5b5e1e7adb77c1da500d16f
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645103"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>ER-i konfiguratsioonide koostamine PDF-mallide täitmiseks

[!include[banner](../includes/banner.md)]

Selle teemas esitatud protseduurid on näited, mis näitavad, kuidas kasutaja kas **Süsteemiadministraatori** või **Elektroonilise aruandluse arendaja** rollis saab konfigureerida elektroonilise aruandluse (ER) vormingu, mis loob aruandeid PDF-failidena, kasutades täidetavaid PDF-dokumente aruandemallidena. Neid samme saab teha mis tahes Dynamics 365 Finance või Regulatory Configuration Services (RCS) ettevõttes.

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist peab teil olema üks järgmistest juurdepääsu tüüpidest, sõltuvalt teenusest, mida kasutate selle teema protseduuride lõpetamiseks.

- Juurdepääs Rahanduse keskkonda ühe järgmise rolli jaoks:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Juurdepääs RCS-keskonda ühe järgmise rolli jaoks:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

Samuti peate lõpetama protseduuri teemas [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Lõpuks laadige alla järgmised failid .

| Sisu kirjeldus                       | Faili nimi                                     |
|-------------------------------------------|-----------------------------------------------|
| Aruande esimese lehekülje mall | [IntrastatReportTemplate1. pdf](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| Aruande teiste lehekülgede mall    | [IntrastatReportTemplate2. pdf](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| ER-vormingu näidis – PDF                          | [Intrastat report (PDF).version.1.1.xml](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| ER-vormingu näidis – Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| Näidisandmekogu                            | [Intrastat sample data.xlsx](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>Vormingu konfiguratsiooni kujundamine

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Juurdepääsu saamine Microsofti pakutavale konfiguratsioonide loendile

1. Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.
2. Veenduge, et pakkuja **Litware, Inc.** on olemas ja märgitud aktiivseks.
3. Paanil **Microsoft** i pakkuja jaoks valige **Hoidlad**.

    > [!NOTE]
    > Kui **LCS**-tüüpi hoidla on juba olemas, jätke selle protseduuri ülejäänud etapid vahele.

4. Valige **Lisa**.
5. Dialoogiakna ripploendis **Hoidla tüübi konfiguratsioon** valige suvand **LCS**.
6. Valige käsk **Loo hoidla**.
7. Valige nupp **OK**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Microsofti pakutavate mudeli konfiguratsioonide saamine

1. Lehe **Hoidlate konfiguratsioon** vasakul küljel valige nupp **Filtrite kuvamine** (lehtri sümbol).
2. Lisage filter **LCS**-väärtuse jaoks väljale **Tüüp** ja kasutage tehtemärki **algab väärtusega**.
3. Valige **Rakendamine**.
4. Valige **Avamine**.
5. Tehke puul valik **Intrastati mudel**.
6. Kiirkaardil **Versioonid** valige versioon **1**.

    > [!NOTE]
    > Kui nupp **Import** ei ole kiirkaardil **Versioonid** saadaval, jätke selle protseduuri ülejäänud etapid vahele.

7. Valige **Impordi**.
8. Valige **Jah**, et kinnitada **Intrastati mudeli** valitud versiooni mudeli konfiguratsiooni importimist.

### <a name="create-a-new-format-configuration"></a>Uue vormingu konfiguratsiooni loomine

1. Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.
2. Tehke puul valik **Intrastati mudel**.
3. Valige **Konfiguratsiooni loomine**.

    > [!NOTE]
    > Kui nupp **Konfiguratsiooni loomine** ei ole saadaval, peate lülitama sisse kujunduse režiimi lehel **Elektroonilise aruandluse parameetrid**, mida saab avada tööruumis **Elektrooniline aruandlus**.

4. Dialoogiakna rippmenüüs, väljagrupil **Uus** valige suvand **Intrastati andmemudelil põhinev vorming**.
5. Väljale **Nimi** sisestage **Intrastati aruanne (PDF)**.
6. Väljale **Kirjeldus** sisestage **Intrastati aruanne PDF-vormingus**.

    > [!NOTE]
    > Aktiivne konfiguratsiooni pakkuja sisestatakse automaatselt. See pakkuja saab seda konfiguratsiooni hallata. Kuigi teised pakkujad saavad seda konfiguratsiooni kasutada, ei saa nad seda hallata.

7. Valikuline: väljal **Vormingu tüüp** saate valida elektroonilise dokumendi kindla vormingu. Kui valite **PDF**-i kujunduse ajal, siis pakub ER-i operatsioonide kujundaja ainult vorminguelemente, mis on kohaldatavad ainult PDF-vormingus loodud dokumentidele (**PDF\fail**, **PDF\PDF-i liitmine** jne). Kui jätate selle välja tühjaks, määratakse elektroonilise dokumendi vorming ER operatsioonide kujundamise ajal, kui lisatakse esimene vorminguelement. Näiteks kui lisate **Excel\File** esimese vorminguelemendina, pakub ER-i operatsioonide kujundaja just vormingu elemente, mis on kohaldatavad ainult Exceli vormingus loodud dokumentidele (**Excel\Cell**, **Excel\Range**, jne). Vorming.
8. Valige **Konfiguratsiooni loomine**.

Uus ER-i vormingu konfiguratsioon on loodud. Saate kasutada selle konfiguratsiooni mustandversiooni, et talletada ER-i vormingu komponenti, mille eesmärk on luua elektroonilisi dokumente PDF-vormingus.

### <a name="design-the-format-of-an-electronic-document"></a>Elektroonilise dokumendi vormingu kujundus

Järgmisena saate luua loodud ER-i vormingu konfiguratsiooni alusel luua ER-i vormingu, mis loob PDF-vormingus **Intrastati kontroll**-aruande. Aruande esimesel leheküljel näidatakse aruande kokkuvõtet ja väliskaubanduse kannete üksikasju, millest on teatatud. Teised leheküljed peavad näitama ainult üksikasju väliskaubanduse kannete kohta, millest on teatatud. Kuna loodud aruande lehtedel, peavad olema erinevad paigutused, kasutatakse ER-i vormingus kahte erinevat PDF-vormingu malli.

Avage mis tahes PDF-i vaaturis allalaaditud PDF-mallid. Pange tähele, et iga mall sisaldab mitut välja, mis peavad olema täidetud. Igas mallis esitatakse väliskaubanduse kannete üksikasjad 42 reana, millest igaühes on üheksa välja. Rea number kuvatakse iga välja nime lõpus (nt **kuupäev 1**...**Kuupäev 42** ja **Kaup 1**...**Kaup 42**).

Järgmisel joonisel on kujutatud aruande esimese lehekülje PDF-malli.

![Mall 1.](media/rcs-ger-filloutpdf-template1.png)

Järgmisel joonisel on kujutatud aruande teiste lehekülgede PDF-malli.

![Mall 2.](media/rcs-ger-filloutpdf-template2.png)

1. Lehel **Konfiguratsioonid** valige suvand **Kujundaja**.
2. Valige **Lisa juur**.
3. Dialoogiakna ripploendi puul valige **PDF \> -PDF-i liitmine.**

    Kui valite elemendi **PDF-i liitmine** vormingu juurelemendina, ühendatakse kõik PDF-dokumendid, mis on loodud käitamise ajal, üheks lõplikuks PDF-dokumendiks. Kui teil on vaja ainult ühte PDF-malli, et luua kõik vajalikud dokumendid, siis kasutades teie disainitud ER-i vormingut, saate valida **PDF-faili** juurelemendina.

4. Väljale **Nimi** sisestage **Väljund**.
5. Väljal **Keele-eelistus** valige **Kasutaja eelistus**. Aruanne luuakse käitava kasutaja eelistatud keeles.
6. Väljal **Kultuuri eelistus** valige **Kasutaja eelistus**. Aruande lehtedel esitatud väärtused ja kuupäevad vormindatakse aruande käitanud kasutaja kohalike eelistuste alusel.
7. Valige nupp **OK**.
8. Toimingupaani vahekaardil **Import** valige suvand **PDF-st importimine**.

    Kui täidetav PDF-dokument imporditakse selle ER-i vormingu mallina, luuakse kõik nõutavad ER-i vormingu elemendid (**PDF-faili**, **Väljagrupi** ja **Välja** elemendid) automaatselt vormingus, mis on loodud imporditud PDF-dokumendi struktuuri põhjal.

9. Valige **Sirvimine**. Navigeerige faili juurde ja valige fail **IntrastatReportTemplate1. pdf-**, mille te varem eeltingimusena laadisite.
10. Valige nupp **OK**.

    Valitud fail on laaditud ja väli **Mall** dialoogiaknas **PDF-st importimine** on täidetud.

11. Määrake suvand **Grupiväljad** valikuga **Jah**. Kui valitud PDF-dokument sisaldab mis tahes väljagruppe, kasutatakse neid loodud ER-i vormingu elementide grupeerimiseks. Sellel eesmärgil luuakse **Väljagrupi** vormingu element.

    Kui see suvand on seatud väärtusega **Ei**, luuakse nõutavad ER-i vormingu elemendid kindla loendina elementidest, mis on pesastatud **PDF-faili** vormingu elemendi alusel.

12. Valige nupp **OK**.

    ![Importimine PDF-i dialoogiaknast.](media/rcs-ger-filloutpdf-importtemplate.png)

13. Laiendage puul valikut **Väljund**.

    Pange tähele, et **PDF-faili** komponent on loodud automaatselt, et hallata käitamise ajal loodava aruande esimese lehekülje loomist.

14. Laiendage puul valikut **Väljund \> PDF-fail**.

    Pange tähele, et vormindamise elementide struktureeritud loend on automaatselt loodud ER-i vormingus, mis põhineb täidetava PDF-dokumendi struktuuril, mille varem importisite.

15. Puul valige **Väljund \> PDF-fail**.
16. Väljale **Nimi** sisestage **Lehekülg 1**.

    Selle vormingu elementi kasutatakse **Intrastati kontroll**-aruande esimese lehekülje loomiseks. Sellel lehel kuvatakse aruande kokkuvõte ja väliskaubanduse kannete üksikasjad.

    Kui jätate välja **Keele-eelistused** tühjaks, määratakse säte **Keele-eelistus** **PDF-i liitmise** emaelemendi poolt, mis määrab loodava aruande keele, kasutades seda vormingu elementi. Saate valida teise väärtuse, et alistada emaelemendi säte.

    Kui jätate välja **Kultuuri eelistused** tühjaks, määratakse säte **Kultuuri eelistused** **PDF-i liitmise** emaelemendi poolt, mis määrab loodava aruande lokaadi, kasutades seda vormingu elementi. Lokaat määrab aruande lehekülgedel olevate väärtuste ja kuupäevade vormingu. Saate valida teise väärtuse, et alistada emaelemendi säte.

17. Toimingupaanil valige vahekaart **import**. Pange tähele, et nupp **PDF-i värskendamine** on muutunud kättesaadavaks valitava **PDF-faili** vormingu elemendi jaoks.

    Selle nupu abil saate importida värskendatud PDF-malli redigeeritud vormingusse. Värskendatud PDF-malli importimisel muudetakse vastavalt ka vormingu elementide loendit:

    - Värskendatud PDF-malli uute väljade jaoks luuakse muudetud ER-i vormingus uued vormingud.
    - Kui värskendatud PDF-mall ei sisalda enam välju, mis vastavad mis tahes olemasoleva vormingu elementidele redigeeritud ER-i vormingus, kustutatakse need vormingu elemendid ER-i vormingust.

18. Vahekaardil **Vorming** valige **Manused**.

    Pange tähele, et imporditud PDF-dokument on lisatud muudetud ER-i vormingule.

    ![PDF-i manuse eelvaade.](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Jätkake selle vormingu kujundamist, importides teise PDF-malli, lisades vajalikud sidumised andmeallikatega jne.
20. Valige käsk **Salvesta**.
21. Sulgege leht.
22. Valige **Kustuta**.
23. Valige **Jah**.

Lisateavet, kuidas uusi **PDF-i liitmise**, **PDF-faili**, **Väljagrupi** ja **Välja** vormingu elemente kasutada PDF-vormingus dokumentide loomiseks, saate importides ja analüüsides ER-i vormingu näidist.

### <a name="import-the-format-configuration"></a>Vormingu konfiguratsiooni importimine

Järgmisena impordite ER-i vormingu näidise, mille eelnevalt laadiste alla, et luua **Intrastati kontroll**-aruannet PDF-vormingus. Aruande esimesel leheküljel näidatakse aruande kokkuvõtet ja väliskaubanduse kannete üksikasju, millest on teatatud. Teised leheküljed peavad näitama ainult üksikasju väliskaubanduse kannete kohta, millest on teatatud.

1. Lehel **Konfiguratsioonid** valige suvand **Vahetuskursi \> laadimine XML-failist.**
2. Valige **Sirvimine**. Navigeerige faili juurde ja valige fail **IntrastatReport(PDF).version.1.1.xml**, mille te varem eeltingimusena laadisite.
3. Valige nupp **OK**.

## <a name="analyze-the-format-configuration"></a>Vormingu konfiguratsiooni analüüsimine

### <a name="format-layout"></a>Vormingu paigutus

1. Valige lehel **Konfiguratsioonid** puul **Intrastati mudeli \> Intrastati aruanne (PDF).**
2. Valige **Kujundaja**.
3. Valige **Üksikasjade näitamine**.
4. Laiendage puul valikut **Väljund: PDF-i liitmine**.

    Pange tähele, et see ER-i vorming sisaldab kaht **PDF-faili** elementi, millest kumbki kasutab erinevat PDF-malli. Ühte malli kasutatakse aruande esimese lehekülje loomiseks PDF-vormingus ja teist malli kasutatakse teiste lehtede loomiseks.

5. Puul laiendage **Väljund: PDF-i liitmine \>, lehekülg 1: PDF-fail (IntrastatReportTemplate1)**.
6. Puul laiendage **Väljund: PDF-i liitmine \>, lehekülg N: PDF-fail (IntrastatReportTemplate2)**.

    Pange tähele, et kuna kahe PDF-malli sisu erineb, erineb ka kahe **PDF-faili** elemendi pesastatud vormingu elementide struktuur.

### <a name="format-mapping"></a>Vormingu vastendamine

1. Valige lehel **Vormingu kujundaja** vahekaart **Vastendamine**.
2. Laiendage puul suvandit **Saalimine \> Lehed**.

    ![Valemi kujundaja lehekülg, kus on laiendatud mudelipuu.](media/rcs-ger-filloutpdf-reviewformat.png)

    Arvestage järgmist.

    - **Väljundi \> Leht 1** **PDF-faili** tüübi vormingu element ei ole seotud ühegi andmeallikaga ja selle vormingu elemendi **Lubatud** avaldis on tühi. Seetõttu täidetakse käitamise ajal **IntrastatReportTemplate1** PDF-mall ainult üks kord, siis, kui luuakse individuaalne PDF-dokument.
    - **Väljundi \> Leht N** **PDF-faili** tüübi vormingu element on seotud andmeallikaga **Saalimine.lehtN** tüübiga **Kirjete loend** ja selle vormingu elemendi **Lubatud** avaldis on tühi. Seetõttu täidetakse käitamise ajal **IntrastatReportTemplate2** PDF-mall iga seotud kirje loendist pärit kirje korral, kui luuakse individuaalne PDF-dokument.
    - Kuna **lehekülg 1: PDF-fail** ja **leht N: PDF-** vormingu elemendid on lapsed **Väljund: PDF-i liitmine** vormingu elemendst,liidetakse kõik täidetud PDF-dokumendid ühte lõplikku PDF-dokumenti.
    - **Saalimine.Leht1** ja **Saalimine.LehtN** andmeallikad on konfigureeritud andmeallika **Saalimine.Lehed** kirjete filtritena. See andmeallikas on konfigureeritud tükeldama kogu väliskaubanduse kannete kogumi partiideks. Iga partii sisaldab 42 kirjet. Kannete tükeldamiseks partiideks kasutatakse järgmist ER-i avaldist:

        SPLITLIST (Kogusummad.CommodityRecord, 42)

    - **Saalimine. Lehted** andmeallikas sisaldab **Saalimine.Lehed. Loendatud** elementi, mis tagastab iga partiisse kaasatud kirje üksikasjad. Need üksikasjad hõlmavad kirje seeriat praeguses partiis ( väli **Saalimine.Lehed.Nummerdatud.Number**). Välja **Saalimine.Lehed.Nummerdatud.Number** kasutatakse **PDF-välja** vormingu elementide **nime** avaldises, et luua välja nimi dünaamiliselt, mis põhineb kande numbril partiis. Loodud välja nime kasutatakse seejärel õige PDF-i välja täitmiseks kasutatavas PDF-mallis.
    - **PDF-grupi** tüübi elemendi **väljund \>leht N \> üksikasjad 2** vorming on seotud andmeallikaga **Saalimine. LehtN.Loendatud** (või **\@.Loendamine**, kui on kasutatud **suhtelise tee** vaate režiimi) **kirjeloendi** tüübiga. Seetõttu täidetakse selle PDF-grupi pesastatud elemendid iga kirje puhul seotud kirjeloendist. Sel viisil luuakse eraldi PDF-read, kus igas N-is on 42 loendi **Saalimine.LehtN.Loendatud** kirjet.ja järgmised PDF-väljad on täidetud: kuupäev N, suund N, kaup N jne. Seetõttu meenutab selle **Väljagrupi** vormingu element käitumine **XML \> Seeria** ja **Teksti \> Seeria** vormingu elementide käitumist.

3. Puul laiendage **Väljundi \> Leht N \> Üksikasjad2**.
4. Puul valige **Väljund \> Leht N \> Üksikasjad2 \> LeheJalus**.

    Pange tähele , et selle vormingu elemendi **Nimi** on määratletud kui **LeheJalus**. Samuti pange tähele, et , vormingu elemendi avaldis **Nimi** on tühi.

5. Puul valige **Väljund \> Leht N \> Üksikasjad2 \> Parandus 1**.

    Pange tähele , et selle vormingu elemendi **Nimi** on määratletud kui **Parandus 1**. Samuti pange tähele, et vormingu elemendi avaldis **Nimi** on määratletud kui **Saalimine.FldNimi („Parandus",\@.Number)**.

![Vormingu kujundaja, kus vastendamine on valitud.](media/rcs-ger-filloutpdf-reviewformat2.png)

Arvestage, vormingu elementi **Väli** kasutatakse täidetava PDF-dokumendi üksiku välja täitmiseks, mis on määratud **PDF-faili** emavormingu elemendi mallina. **PDF-faili** vormingu elemendi sidumine või pesastatud elemendid, kui on pesastatud elemente, määrab vastavatele PDF-väljadele sisestatavad väärtused. **Välja** vormingu elemendi erinevaid atribuute saab kasutada, et määrata, milline PDF-väli täidetakse üksiku vormingu elemendiga:

- Klõpsake vahekaardil **Vorming** elemendi vormingu atribuuti **Nimi**
- Klõpsake vahekaardil **Vastendamine** elemendi vormingu avaldist **Nimi**

Kuna mõlemad atribuudid on vormingu elemendi **Väli** puhul kohustuslikud, rakendatakse siht-PDF-välja määramiseks järgmisi reegleid:

- Kui atribuut **Nimi** on tühi ja avaldis **Nimi** tagastab tühja stringi käituse ajal, tehakse käitusaja erand, et teavitada kasutajat sellest, et PDF-i välja ei leita PDF-mallis, mida kasutatakse PDF-dokumendi täitmiseks.
- Kui atribuut **Nimi** on määratud ja avaldis **Nimi** on tühi, siis täidetakse PDF-i väli, millel on sama vormingu elemendi atribuudi **Nimi**.
- Kui atribuut **Nimi** on määratud ja avaldis **Nimi** on konfigureeritud, siis täidetakse PDF-i väli, millel on sama vormingu elemendi avaldise **Nime** tagastatud väärtus.

> [!NOTE]
> Kui PDF-malli märkeruut ei kuulu märkeruutede gruppi, on see esitatud redigeeritavas ER-vormingus **·** **PDF-faili elemendi alla pesastatud väljaelemendina**. Seda tüüpi PDF-märkeruutu saab valida järgmistel viisidel:
>
> - Vastav väljavormingu **element** on seotud andmeallika väljaga *[boole'i](er-formula-supported-data-types-primitive.md#boolean)* andmetüübis, mille väärtus on **Tõene**.
> - Vastav välja **vorminguelement** sisaldab pesastatud **stringivormingu** elementi **, mis on seotud andmeallika väljaga, mille tekstiväärtus on 1**, Tõene **või** **Jah**.
>
> Teie mall võib sisaldada märkeruute, kus korraga saab valida ainult ühe märkeruudu. Need märkeruudud on esitatud PDF-mallis mitme ruudutüüpi *vormiväljana*. Igal väljal on sama nimi, kuid erinev ekspordiväärtus. Kui impordite malli redigeeritavasse ER-vormingusse, **tähistab** iga märkeruutu vormingu hierarhilises struktuuris märkeruudugrupi kaubaelement **, mis on pesastatud sama märkeruudugrupi elemendi** alla. Märkeruudugrupi **elemendi** nimi võrdub PDF-malli märkeruuduväljade nimega. Iga märkeruudugrupi **kaubaelemendi** nimi võrdub vastava märkeruudu välja ekspordiväärtusega PDF-mallis.
>
> Saate siduda märkeruudu **grupi kauba** elemendi ainult Kahendmuutuja *andmetüübi* andmeallika väljaga.

## <a name="run-the-format-configuration"></a>Vormingu konfiguratsiooni käitamine

### <a name="import-the-format-configuration"></a>Vormingu konfiguratsiooni importimine

Järgmisena laadige **Intrastati (Impordi Excelist)** ER-i vormingu näidis. See vorming on mõeldud kasutaja valitud Microsoft Exceli töövihiku sõelumiseks, mis simuleerib väliskaubanduse kandeid.

1. Lehel **Konfiguratsioonid** valige suvand **Vahetuskursi \> laadimine XML-failist.**
2. Valige **Sirvimine**. Navigeerige faili juurde ja valige fail **(import from Excel).version.1.1.xml**, mille te varem eeltingimusena laadisite.
3. Valige nupp **OK**.
4. Tehke puul valik **Intrastati mudel \> Intrastat (impordi Excelist)**.
5. Valige suvand **Redigeeri**.
6. Seadistage **Vaikimisi mudeli vastendamise** suvand väärtusele **Jah**.

    > [!NOTE]
    > Kui olete eelnevalt seadistanud **Vaikimisi mudeli vastendamise** suvandi väärtusega **Jah** **Intrastati mudeli** konfiguratsiooni jaoks või mõne muu konfiguratsiooniga, mis on pesastatud konfiguratsiooniga **Intrastati mudeli** alusel, siis määrake see suvand väärtusele **Ei**.

    Kui suvand **Mudeli vaikimisi vastendamine** on vaikimisi seatud väärtusele **Jah**, siis määratakse imporditud **Intrastati (imporditud Excelist)** ERi vormingule vaikimisi andmeallika **Intrastati aruande (PDF)** vormingu konfiguratsioon. Siis, kui **Intrastati aruande (PDF)** vormingu konfigureerimine on käivitatud, simuleerib Exceli töövihiku sisu, mis on sõelutud **Intrastati (importud Excelist)** ER-i vormingus, väliskaubanduse kandeid, millest tuleb teatada. Järgmisel joonisel on toodud Exceli töövihiku näide.

    ![Exceli töövihik, millel on näidisandmed.](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>Vormingu konfiguratsiooni käitamine

1. Valige lehel **Konfiguratsioonid** puul **Intrastati mudeli \> Intrastati aruanne (PDF).**
2. Valige käsk **Käitus**.
3. Valige **Sirvimine**. Navigeerige faili juurde ja valige fail **Intrastat sample data.xlsx**, mille te varem eeltingimusena laadisite.
4. Valige nupp **OK**.
5. Väljal **Aruande suund** valige **Mõlemad**, et täita kõik Exceli töövihikust imporditud kanded loodud PDF-aruandes.
6. Valige nupp **OK**.
7. Vaadake üle loodav PDF-dkoument.

Järgnev illustratsioon näitab aruande esimesest leheküljest loodud näidet.

![Loodud aruande esimene lehekülg.](media/rcs-ger-filloutpdf-generatedreport.png)

Järgnev illustratsioon näitab aruande teistest lehekügedest loodud näidet.

![Loodud aruande muu lehekülg.](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="limitations"></a>Kitsendused

Täitmisväljade nimed peaksid olema kordumatud PDF-vormingus, mida plaanite aruandemallina kasutada. Igale sellisele väljale luuakse PDF-vormi importimisel vastava nimega üksikvormingu element redigeeritavas ER-vormingus. Kui PDF-vorm sisaldab mitut sama nimega välja, luuakse üks vorminguelement väljadele, mis ei luba neid käitusajal eraldi täita.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="when-i-run-the-er-format-to-generate-a-report-in-pdf-format-why-do-i-get-the-following-errors--cannot-handle-iref-streams-the-current-implementation-of-pdfsharp-cannot-handle-this-pdf-feature-introduced-with-acrobat-6-and-a-pdf-name-must-start-with-a-slash-"></a>Pdf-vormingus aruande loomiseks käivitades ER-vormingu, siis kuvatakse järgmised tõrked: **ei saa käsitseda tagasijaotatud vooge. PDFSharpi praegune juurutamine ei suuda käsitseda seda Pdf-funktsiooni, mis käivitati koos Acrobat 6-ga.** Ja **PDF-nimi peavad algma kaldkriipsuga (/).**

ER-raamistik kasutab nende PDF-aruannete loomiseks PDF-aruannete loomiseks PDF-teeki 1.5. Mõningaid PDF 1.5 (Adobe Reader 6.0) funktsioone ei ole selles teegis veel rakendatud. Seetõttu ei saa PDFSharp veel **avada faile, mis on märgitud pdf-vormingus 1.5** või uuem ja mille puhul võivad ilmneda tõrked. Probleemi lahendamiseks kasutage üht järgmistest lahendustest:

-   Kui kasutate oma PDF-malli: alandate Adobe malli varasemasse versiooni ja alustate uue malli kasutamist ER-vormingus.
-   Kui kasutate ER-i vormingu malli, mille teine konfiguratsioonipakkuja teile ER-lahenduse osana jagas: võtke ühendust selle ER-lahenduse omanikuga ja esitage probleemi kirjeldus.
-   Kui kasutate ISV lahendust, mis sisaldab PDFSharpi teeki varasemat versiooni: võtke ühendust lahenduse omanikuga ja soovitage uuendada uuemat PDFSharpi versiooni.

## <a name="additional-resources"></a>Lisaressursid

- [Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [Elektroonilise aruandluse konfiguratsioonide kujundamine Wordi vormingus aruannete loomiseks](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
