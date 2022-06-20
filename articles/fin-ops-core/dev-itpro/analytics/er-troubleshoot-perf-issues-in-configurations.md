---
title: Jõudlusprobleemide tõrkeotsing ER-i konfiguratsioonides
description: See artikkel selgitab, kuidas elektroonilise aruandluse (ER) konfiguratsioonides jõudlusprobleeme leida ja parandada.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 28ff68309bad7a6c1b6009ba03ef4b20aceb5194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847336"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>Jõudlusprobleemide tõrkeotsing ER-i konfiguratsioonides

See artikkel selgitab, kuidas elektroonilise aruandluse [(ER) konfiguratsioonides jõudlusprobleeme](general-electronic-reporting.md) leida ja [lahendada](general-electronic-reporting.md#Configuration).

Tavaliselt koosneb toimivuse uurimine mitmest etapist.

1. [Kogu](#collecting-data) andmeid.
2. Analüüsige kogutud andmeid.
3. Analüüsi tulemuste põhjal kasutage ER-konfiguratsioone [muudatuste tegemiseks](#making-changes) või otsustage koguda rohkem andmeid.

## <a name="troubleshooting"></a>Tõrkeotsing

### <a name="analyze-execution-time"></a>Täitmisaja analüüsimine

Täitmisaeg võib sõltuda ettearvamatutest teguritest, näiteks muudest samas keskkonnas töötavatest toimingutest ja vahemällu salvestamisest, mis kasutab andmeid, kui neid esimest korda kutsutakse. Seetõttu peaksite täitmist ja mõõtmist mitu korda kordama.

Mõnikord ei põhjusta jõudlusprobleeme aruandluseks kasutatav ER-vormingu konfiguratsioon. Selle asemel on need põhjustatud X++ koodist, mida kasutatakse selle ER-vormingu konfiguratsiooni avamiseks.

1. Vaadake [tegevuskeskuses](#infolog-time) või [sündmuselogis](#event-log-time) aruande täitmise aega.
2. Saate võrrelda aruande täitmisaega stsenaariumi kogu täitmisajaga.
3. Kui aruande täitmisaeg on palju lühem kui kogu täitmisaeg, kaaluge aruande töödeldavate andmete hulka.

    - Kui aruanne töötleb väikest hulka andmeid, võib probleemiks olla konfiguratsiooni laadimisaeg.
    - Kui aruanne töötleb suurt hulka andmeid, võib probleem hõlmata eeltöötlust X++. Selle juhtumi analüüsimiseks kasutage [trace parserit](#analyze-trace-parser-trace).

    Muudel juhtudel vaadake järgmisi jaotisi.

4. Saate käivitada mitu testi, mis hõlmavad erinevat andmehulka, et määratleda, kuidas täitmisaeg sõltub andmehulgast.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Jälitamised Trace Parseri abil

Valmistage ette väike näide või koguge aruande loomise jaoks juhuslikke osi.

Seejärel tehke [Trace parseeris](#trace-parser) standardne alt üles analüüs ja vastake järgmistele küsimustele:

- Millised on ajatarbimise peamised meetodid?
- Millist osa koguajast need meetodid kasutavad?

Vastake päringute puhul samadele küsimustele.

Kui näete, et meetodite eesliide on "ER", liikuge edasi järgmisse jaotisse.

Kui näete, et meetodid või päringud pärinevad rakendusekomplektist, kaaluge üldisi optimeerimisi (nt registrite loomine).

Saate analüüsida kõnede arvu. Kui arv on oodatust oluliselt suurem, kaaluge konfiguratsiooni vastavate sõlmede vahemällu salvestamist.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Andmebaasikõnede analüüsimine

Valmistage ette näide, millel on väike andmehulk, et saaksite koguda [ER-jälge](#electronic-reporting-traces).

Seejärel avage ER-mudeli vastendamise kujundajas jälitus ja vaadake lehe allserva. Vastake järgmistele küsimustele:

- Kas päringu dubleerimine on olemas? Kui on, kaaluge ühte järgmistest parandustest:

    - [Kasutage vahemällu salvestamist](#use-caching) kui arvate, et ühe emakirje sees on mitu kõnet.
    - [Kasutage vahemällu talletatud, parameetri põhjal arvutatud välja](#cached-parameterized) juhul kui arvate, et erinevates kirjetes on kõnesid samale kirjele.
    - [Kasutage **ÜHENDA** andmeallikat](#use-join-datasource) kui peate lugema andmebaasist mõnda muud kirjet.

- Kas päringute ja toodud kirjete arv vastab andmete koguhulgale? Näiteks kui dokumendil on 10 rida, kas statistika näitab, et aruanne ekstraktib 10 rida või 1000 rida? Kui teil on suur hulk tõmmatud kirjeid, kaaluge ühte järgmistest parandustest:

    - [Kasutage POOLandmete töötlemiseks **FUNKTSIOONI WHERE** **asemel** funktsiooni FILTER](#filter).Microsoft SQL Server
    - Samade andmete toomise vältimiseks kasutage vahemällu salvestamist.
    - [Kogutud andmefunktsioonide abil saate](#collected-data) vältida samade andmete toomist summeerimiseks.

### <a name="analyze-perfview-traces"></a>PerfView jälgede analüüsimine

[PerfView](#perfview) on tööriist kogenud arendajatele. Üksikasjalikumat teavet järgmiste sammude kohta leiate teemast [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Saate lõimeaja abil jälituse koguda.
2. Kaasa ainult virnad, mis kasutavad **käitaSidumata**, et filtreerida ainult lõime, millel on konfiguratsiooni käivitamine. (Lisage **käitaSidumata** sisendvälja **IncPats** ruutu.)
3. Voltige kogu protsessor, võrk ja blokeeritud aeg.
4. [Laadige PerfView jaoks ER-i valmissätted](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).
5. Valige **ER** \> **Muu valmissäte**.
6. Vaata nimesid:

    - Tõenäoliselt näete platvormi koodi, mis tarbib kõige rohkem aega.
    - Võite topeltkoputada (või topeltklõpsata) ja minna üles **helistaja kaudu**.

        Kui leiate klassid, millel on eesliide "ERExpression" ja kui need on valemitega seotud funktsioonid, võite funktsiooni nime klassi nime põhjal ära arvata ja atribuutide vaatamiseks vaadata ER-i repo-d.

### <a name="fixes"></a>Parandused

- Kui näete, et päringud tarbivad suurema osa protsessori ajast, proovige päringute arvu vähendada:

    - [Vaadake ER-i jälitusi](#analyze-database-calls) dubleeritud päringutele.
    - Vaadake, kui palju kirjeid on toodud, ja hinnake, kui palju andmeid tuleks teoreetiliselt tuua.

- Kui näete, et suurema osa protsessori ajast tarbivad kasutatavad funktsioonid, proovige leida koht konfiguratsioonis, mis tarbib kõige rohkem ressursse.
- Kui näete, et suurema osa protsessori ajast tarbivad andmekogumisfunktsioonid, kaaluge nende asendamist *SQL-grupiga* mudeli vastendamise poolel.

### <a name="collecting-data"></a><a name="collecting-data"></a>Andmete kogumine

Sõltuvalt teie keskkonnast on saadaolevate andmete kogumiseks mitu võimalust:

- Hankige kogu käitusaeg:

    - Tegevuskeskusest
    - Sündmuselogist

- Profiili täitmine:

    - ER-tööriistade abil
    - Trace parseri abil
    - PerfView abil

#### <a name="collecting-data-in-a-production-environment"></a>Tootmiskeskkonna andmete kogumine

Mõnikord saab probleeme paljundada ainult tootmiskeskkonnas. Saate andmeid koguda järgmistel viisidel:

- Kasutades [Trace Parser](../perf-test/trace-trace-tutorial.md) jälitamisi
- Kasutades [ER-i täitmise](trace-execution-er-troubleshoot-perf.md) jälgi
- Kogu täitmisaja abil

#### <a name="collecting-data-in-a-development-environment"></a>Arenduskeskkonna andmete kogumine

Lisaks tööriistadele, mida saab kasutada tootmiskeskkonnas, on mitmeid tööriistu, mida saate arenduskeskkonnas kasutada:

- Sündmuselogi (Microsoft-Dynamics-ElectronicReporting). See logi võib anda teile kogu täitmisaja.
- Levinumad .NET-i tööriistad nagu näiteks PerfView.

Lisaks annab arenduskeskkond teile rohkem paindlikkust eksperimenteerimiseks. Näiteks saate aruannete osad välja lülitada, et näha, kuidas täitmisaeg mõjutab.

### <a name="tools"></a><a name="tools"></a>Tööriistad

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Täitmisaeg tegevuskeskuses

ER saab kuvada konfiguratsiooni täitmisaja tegevuskeskuses. See suvand töötab ainult kindla kasutaja ja kindla ettevõtte puhul ning ainult interaktiivsete seansside puhul. Selle funktsiooni kättesaadavaks tegemiseks toimige järgmiselt.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Dialoogiboksis **Kasutaja parameetrid** määrake suvand **Käivita silumisrežiimis** valikule **Jah**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Täitmisaeg sündmuselogis

1. Windows Event Viewer avamine.
2. Jaotises **Rakenduste ja teenuste logid** avage **Microsoft-Dynamics-ElektroonilineAruandlus/Operatsioon**.
3. Otsige **FormatMapingRun** sündmusi, kus **SündmusID=2**, kuna need sündmused sisaldavad teavet möödunud aja kohta.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Jälitamised Trace Parseri abil 

Kuna ER rakendatakse X++-s, saate jõudluse analüüsimiseks kasutada tavalisi X++ tööriistu. Lisateavet leiate teemast [Trace parseri abil jälgede võtmine](../perf-test/trace-trace-tutorial.md).

Sellel lähenemisviisil on mõned piirangud. Kuna osa ER-ist rakendatakse C#-s, pole kõik üksikasjad saadaval. Siiski saate vaadata andmekasutuse üksikasju. Lisaks võivad pikad aruandeajamid ületada jälgimissalvestuse piiranguid.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER jäljed

ER võib koguda oma jälgi ning tal on nende jälgede visualiseerimis- ja analüüsivahendid. Lisateavet leiate teemast [Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Kuna nii X++ kui ka ER on rakendatud .NET-platvormi peale, saate kasutada levinud .NET-i tööriistu. Näiteks saate kasutada tasuta [PerfView](https://github.com/Microsoft/perfview) tööriista.

Andmeid saate koguda ka käsurealt. Näiteks järgmine Windows PowerShell skript kogub täitmisaega, kuni mis tahes vormingu täitmine on arvutis peatatud.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Sellel lähenemisviisil on mõned piirangud. Teil peab olema administratiivne juurdepääs masinale. Lisaks peate olema kogenud arendaja, sest seal on järsk õppimiskõver.

### <a name="making-changes"></a><a name="making-changes"></a>Muudatuste tegemine

#### <a name="use-caching"></a><a name="use-caching"></a>Vahemällu salvestamise kasutamine

Kuigi vahemällu salvestamine vähendab aega, mis kulub andmete uuesti toomiseks, maksab see mälu. Kasutage vahemällu salvestamist juhtudel, kui toodud andmete hulk pole väga suur. Lisateavet ja näiteid vahemällu salvestamise kasutamise kohta leiate teemast [Mudelivastenduse täiustamine täitmisjälitusjälitusteabe põhjal](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="reduce-volume-of-data-fetched"></a><a name="reduce-fetched-data"></a> Vähenda toodavad andmete mahtu

Saate vähendada mälu tarbimist vahemälustusel, piirates väljade arvu rakendustabeli kirjetes, mille käitusajal toodate. Sel juhul toodate ainult neid rakenduse tabeli väljaväärtusi, mida vajate ER-mudeli vastendamiseks. Teisi selle tabeli välju ei tooda. Seetõttu vähendatakse toodavate kirjete vahemällu tallemiseks vajalikku mälumahtu. Lisateavet vt [ER-lahenduste jõudluse parandamiseks, vähendades käitusajal toodud tabeliväljade arvu](er-reduce-fetched-fields-number.md).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Vahemällu talletatud, parameeter arvutatud välja kasutamine

Mõnikord tuleb väärtusi korduvalt uurida. Näited hõlmavad kontonimesid ja kontonumbreid. Aja säästmiseks saate luua arvutatud välja, millel on ülemise taseme parameetrid, ja seejärel lisada välja vahemällu.

Soovitame seda lähenemist kasutada ainult siis, kui vahemällu talletatud andmete maht on väike. Lisateavet vt teemast [ER lahenduste täiustamine arvutatud välja parametriseeritud andmeallika lisamisega](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>Kasutage ÜHILDA andmeallikat

**ÜHILDA** andmeallikas võimaldab ühe päringu abil tuua mitu ühendatud kirjet. Iga ühendatud kirje toomiseks ei pea kasutama eraldi päringut. Näiteks kui teil on 1000 rida ja toote kaubaandmed iga rea kohta seoste kaupa, on teil 1001 päringut (= 1000 + 1). Kui kasutate **ÜHILDA** andmeallikat, saate samade andmete toomiseks kasutada ainult ühte päringut. Vaata lisateavet [Andmeallikate ÜHILDA kasutamine andmete saamiseks mitmest rakendusetabelist elektroonilise aruandluse (ER) mudeli vastendustes](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Kasutage funktsiooni KUS asemel funktsiooni FILTER

**[FILTER](er-functions-list-filter.md)** funktsioon käitab SQL Serveris tingimusi, samas kui **KUS** funktsioon toob kõik andmed loendist, ühe kirje korraga ja rakendab tingimuse iga kirje jaoks. Näiteks soovite valida ühe kirje 1000 kirjest. Kui kasutate **KUS**, tuuakse kõik 1000 kirjet. Kui aga kasutate **FILTRIT**, tuuakse täpselt üks kirje. **FILTRIT** saab kasutada ka indekseid andmebaasi poolel.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Kogutud andmefunktsioonide või akumuleeritud andmeallika kasutamine

Kui teie konfiguratsioonil on *grupeerige* komponentide rühm, mis võtab kokku varem aruande alusel toodud andmed, toob komponent kõik andmed uuesti. Kogutud andmefunktsioonide abil saate lubada ER-l koguda andmeid esimese toomise ajal. Lisateavet vt jaotisest [ER vormingu konfigureerimine inventuuri tegemiseks ja summeerimiseks](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Konfiguratsiooni osade ümberkirjutamine X++

ER toetab tabelite ja klasside helistamismeetodeid, sealhulgas laiendusi. Jõudluse parandamiseks kaaluge x++ mudelivastenduse osade ümberkirjutamist.

ER võib tarbida andmeid järgmistest allikatest:

- Klassid (**objekti** ja **klass** andmeallikad)
- Tabelid (**tabel** ja **tabeli kirjed** andmeallikad)

[ER-i rakenduse programmeerimisliides (API)](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) pakub ka viisi eelarvutatud andmete saatmiseks kutsumiskoodist. Rakenduskomplekt sisaldab arvukalt näiteid selle lähenemisviisi kohta.
