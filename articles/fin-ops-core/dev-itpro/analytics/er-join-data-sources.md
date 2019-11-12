---
title: Andmeallikate JOIN kasutamine elektroonilises aruandluse (ER) mudeli vastendustes, et saada andmeid mitmest rakendusetabelist
description: Selles teema selgitatakse, kuidas saate kasutada elektroonilises aruandluses andmeallikaid JOIN.
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667950"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Andmeallikate JOIN kasutamine andmete saamiseks mitmest rakendusetabelist elektroonilise aruandluse (ER) mudeli vastendustes

[!include[banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) mudeli vastenduste või vormingute konfigureerimisel saate [lisada](#review) vajalikud andmeallikad, mille tüüp on **Ühendamine**. Koostamisajal on **ühendamise** andmeallikas konfigureeritud mitme andmeallika kogumina, millest igaüks tagastab kirjete loendi. Iga andmeallika puhul, välja arvatud esimene, tuleb määratleda vajalikud tingimused praeguste ja eelmiste andmeallikate kirjete ühendamiseks. Käitusajal [tagastab](#executeERformat) konfigureeritud andmeallikas tüübiga **Ühendamine** ühe ühendatud kirjete loendi, mis sisaldab pesastatud andmeallikate kirjete välju.

Praegu toetatakse järgmisi ühendamise tüüpe.

- Välimine (vasakpoolne) ühendamine:
    - Ühendage kõik esimese (kõige vasakpoolsema) andmeallika kirjed ja seejärel teise (kõige parempoolsema) andmeallika kirjed, mis on vastavalt konfigureeritud tingimustele sobivad.
- Sisemine (parempoolne) ühendamine:
    - Ühendage ainult esimese (kõige vasakpoolsema) andmeallika kirjed ja seejärel ainult teise (kõige parempoolsema) andmeallika kirjed, mis sobivad üksteisega vastavalt konfigureeritud tingimustele.

Konfigureeritud **ühendamise** andmeallikas, kui kõigi andmeallikate tüüp on **Tabeli kirjed**, saab ühendamise andmeallika käivitamise [teha andmebaasi tasandil](#analyze), kasutades selleks ühte SQL-lauset. See vähendab andmebaasikutsete arvu, mis omakorda suurendab mudelivastenduse jõudlust. Vastasel juhul toimub **ühendamise** andmeallika käivitamine mälus.

> [!NOTE]
> Funktsiooni **VALUEIN** kasutamist elektroonilise aruandluse avaldistes, mis määravad tingimused kirjete ühendamiseks andmeallikates, mille tüüp on Ühendamine, ei toetata veel. Üksikasjalikumat teavet selle funktsiooni kohta leiate lehelt [Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md).

Lisateabe saamiseks selle funktsiooni kohta läbige siinse teema näide.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Näide: andmeallikate JOIN kasutamine ER-i mudelivastendustes

Järgmistes toimingutes selgitatakse, kuidas süsteemiadministraator või elektroonilise aruandluse arendaja saab konfigureerida elektroonilise aruandluse (ER) mudelivastenduse, et saada andmeid mitmest rakendusetabelist korraga, kasutades andmeallikaid tüübiga **Ühendamine**, et suurendada andmejuurdepääsu jõudlust. Neid toiminguid saab teha mis tahes ettevõte, mis kasutab tarkvara Dynamics 365 Finance või Regulatory Configuration Services (RCS).

### <a name="prerequisites"></a>Eeltingimused

Selle teema näides kirjeldatud toimingute tegemiseks peab teil olema juurdepääs ühele järgmistest, sõltuvalt sellest, millist teenust kasutatakse nende toimingute tegemiseks.

**Juurdepääs Rahanduse keskkonda ühe järgmise rolli jaoks:**

- Elektroonilise aruandluse arendaja
- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

**Juurdepääs RCS-keskonda ühe järgmise rolli jaoks:**

- Elektroonilise aruandluse arendaja
- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

Samuti peate esmalt läbima protseduuri [Konfiguratsiooni pakkuja loomine ning aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md) etapid.

Eelnevalt peate lisaks [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=000000) alla laadima ja lokaalselt salvestama järgmised proovi ER-i konfiguratsioonifailide näidised:

| **Sisu kirjeldus**  | **Faili nimi**   |
|--------------------------|-----------------|
| **ER-i andmemudeli** konfiguratsioonifaili näidis, mida kasutatakse näidete andmeallikana.| [Model to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| **ER-i mudelivastenduse** konfiguratsioonifaili näidis, mis kasutab näidete jaoks ER-i andmemudelit. | [Mapping to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| **ER-i vormingu** konfiguratsioonifaili näidis. See fail kirjeldab andmeid, millega asustatakse näidistes ER-i vormingu komponent. | [Format to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>Konfiguratsioonide pakkuja aktiveerimine

1. Saate oma veebibrauseri esimesel seansil kasutada kas Finance'i või RCS-i.
2. Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.
3. Veenduge lehe **Lokalisatsiooni konfiguratsioonid** jaotises **Konfiguratsiooni pakkujad**, et näidisettevõtte Litware, Inc. (http://www.litware.com) konfiguratsiooni pakkuja oleks loendis ja tähistatud märkega **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, järgige teemas [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md) kirjeldatud toiminguid.

    ![Elektroonilise aruandluse tööruum](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>ER-i konfiguratsioonifaili näidise importimine

1. Valige **Aruandluse konfiguratsioonid**.
2. Saate importida ER-i andmemudeli konfiguratsioonifaili.
    1. Valige **Exchange**.
    2. Valige **Laadi XML-failist**.
    3. Valige **Sirvi**, et leida fail **Model to learn JOIN data sources.version.1.1.xml**.
    4. Valige nupp **OK**.
3. Saate importida ER-i mudelivastenduse konfiguratsioonifaili.
    1. Valige **Exchange**.
    2. Valige **Laadi XML-failist**.
    3. Valige **Sirvi**, et leida fail **Mapping to learn JOIN data sources.version.1.1.xml**.
    4. Valige nupp **OK**.
4.  Saate importida ER‑i vormingu konfiguratsioonifaili.
    1. Valige **Exchange**.
    2. Valige **Laadi XML-failist**.
    3. Valige **Sirvi**, et leida fail **Format to learn JOIN data sources.version.1.1.xml**.
    4. Valige nupp **OK**.
5.  Laiendage konfiguratsioonide puus üksust **Mudel andmeallikate JOIN õppimiseks**, samuti muid mudeliüksusi (kui on saadaval).
6.  Jälgige ER‑i konfiguratsioonide loendit puus kui ka versiooni üksikasju kiirkaardil **Versioonid** – neid kasutatakse teie näidisaruande andmete allikana.

    ![Elektroonilise aruandluse konfiguratsioonide leht](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Käivitamise jälituse valikute sisselülitamine
1.  Valige **KONFIGURATSIOONID**.
2.  Valige **Kasutaja parameetrid**.
3.  Määrake käivitamise jälitamise parameetrid, nagu näidatud alloleval kuvatõmmisel.

    ![Elektroonilise aruandluse kasutaja parameetrite leht](./media/GER-JoinDS-Parameters.PNG)

    Kui need parameetrid on sisse lülitatud, luuakse igal imporditud ER-i vormingus faili käivitamisel käivitamise jälitus. Loodud käivitamise jälituse üksikasjade abil saate analüüsida ER-i vormingu ja ER‑i mudelivastenduse komponentide käivitamist. Lisateavet ER-i käivitamise jälituse funktsiooni kohta leiate lehelt [ER-i vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsingu tegemiseks](trace-execution-er-troubleshoot-perf.md).

### <a name="review-er-model-mapping-part-1"></a>ER-i mudelivastenduse ülevaade (1. osa)

Vaadake üle ER-i mudelivastenduse komponendi sätted. Komponent on konfigureeritud kasutama teavet ER-i konfiguratsiooni versioonide, konfiguratsioonide ja konfiguratsiooni pakkujate üksikasjade kohta ilma andmeallikaid kasutamata, mille tüüp on **Ühendamine**.

1.  Valige konfiguratsioon **Vastendamine andmeallikate JOIN õppimiseks**.
2.  Valige **Koostaja**, et avada vastenduste loend.
3.  Valige **Koostaja**, et vaadata üle vastendamise üksikasjad. 
4.  Valige **Üksikasjade näitamine**.
5.  Laiendage konfiguratsioonide puus andmemudeli üksusi **Set1** ja **Set1.Details**:

    1. Sidumine **Details: Record list = Versions** näitab, et üksus **Set1.Details** on seotud andmeallikaga **Versioonid**, mis tagastab tabeli **ERSolutionVersionTable** kirjed. Selle tabeli iga kirje kajastab ER-i konfiguratsiooni ühte versiooni. Selle tabeli sisu on esitatud lehe **Konfiguratsioonid** kiirkaardil **Versioonid**.
    2. Sidumine **ConfigurationVersion: String = @.PublicVersionNumber** tähendab, et iga ER-i konfiguratsiooni versiooni avaliku versiooni väärtus võetakse tabeli **ERSolutionVersionTable** väljalt **PublicVersionNumber** ja paigutatakse üksusesse **ConfigurationVersion**.
    3. Sidumine **ConfigurationTitle: String = @.'>Relations'.Solution.Name** näitab, et ER-i konfiguratsiooni nimi võetakse tabeli **ERSolutionTable** väljalt **Nimi**, hinnates tabelite **ERSolutionVersionTable** ja **ERSolutionTable** vahelist mitu-ühele seost (**'>Seosed**). Praeguse rakenduse eksemplari ER-i konfiguratsioonide nimed esitatakse konfiguratsioonide puus lehel **Konfiguratsioonid**.
    4. Sidumine **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** näitab, et praegust konfiguratsiooni omava konfiguratsiooni pakkuja nimi võetakse tabeli **ERVendorTable** väljalt **Nimi**, hinnates tabelite **ERSolutionTable** ja **ERVendorTable** vahelist mitu-ühele seost. ER-i konfiguratsiooni pakkujate nimed esitatakse konfiguratsioonide puus lehel **Konfiguratsioonid** iga konfiguratsiooni lehepäises. Kogu ER-i konfiguratsiooni pakkujate kogu loendi leiate tabelilehelt **Organisatsiooni haldus \> Elektrooniline aruandlus \> Konfiguratsiooni pakkuja** tabeli lehelt.

    ![ER-i mudelivastenduse koostaja leht](./media/GER-JoinDS-Set1Review.PNG)

6.  Laiendage konfiguratsioonide puus andmemudeli üksust **Set1.Summary**:

    1. Sidumine **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** näitab, et üksus **Set1.Summary.VersionsNumber** on seotud andmeallika **VersionsSummary** (tüüp **GroupBy**) kogumi väljaga **VersionsNumber**, mis oli konfigureeritud tagastama tabeli **ERSolutionVersionTable** kirjete arvu andmeallika **Versioonid** kaudu.

    ![Andmeallika GROUPBY parameetrite leht](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  Sulgege leht.

### <a name="review"></a> ER-i mudelivastenduse ülevaade (2. osa)

Vaadake üle ER-i mudelivastenduse komponendi sätted. Komponent on konfigureeritud kasutama teavet ER-i konfiguratsiooni versioonide, konfiguratsioonide ja konfiguratsiooni pakkujate üksikasjade kohta koos andmeallika kasutamisega, mille tüüp on **Ühendamine**.

1.  Laiendage konfiguratsioonide puus andmemudeli üksusi **Set2** ja **Set2.Details**: Võtke arvesse, et sidumine **Details: Record list = Details** näitab, et üksus **Set2.Details** on seotud andmeallikaga **Üksikasjad**, mis on konfigureeritud andmeallikana, mille tüüp on **Ühendamine**.

    ![ER-i mudelivastenduse koostaja leht](./media/GER-JoinDS-Set2Review.PNG)

    Andmeallika **Ühendamine** saab lisada, valides andmeallika **Functions\Join**:

    ![ER-i mudelivastenduse koostaja leht](./media/GER-JoinDS-AddJoinDS.PNG)

2.  Valige andmeallikas **Üksikasjad**:
3.  Valige paanil **Andmeallikad** käsk **Redigeeri**.
4.  Valige **Redigeeri ühendamist**.
5.  Valige **Üksikasjade näitamine**.

    ![Andmeallika JOIN parameetrite leht](./media/GER-JoinDS-JoinDSEditor.PNG)

    Seda lehte kasutatakse andmeallika kujundamiseks, mille tüüp on **Ühendamine**. Käitusajal loob see andmeallikas ühe ühendatud loendi andmeallikatest , mis kuuluvad ruudustikku **Ühendatud loend**. Kirjete ühendamine algab andmeallikast **ConfigurationProviders**, mis on ruudustikus esimene (veerg **Tüüp** on selle jaoks tühi). Kõigi muude andmeallikate kirjed ühendatakse sellest tulenevalt ema-andmeallika kirjetega selle ruudustiku tellimuse alusel. Iga ühendatav andmeallikas peab olema konfigureeritud andmeallikana, mis on pesastatud sihtandmeallika alla (andmeallikas **1Versions** on pesastatud andmeallika **1Configurations** all; **1Configurations** on pesastatud andmeallika **ConfigurationProviders** all). Iga konfigureeritud andmeallikas peab sisaldama ühendamise tingimusi. Selle konkreetse **ühendamise**andmeallikas määratletakse järgmised ühendused:

    - Andmeallika **ConfigurationProviders** iga kirje (viide tabelile **ERVendorTable**) ühendatakse ainult andmeallika **1Configurations** kirjetega (sellele viidatakse tabelis **ERSolutionTable**), millel on sama väärtus kui väljadel **SolutionVendor** ja **RecId**. Tüüpi **Sisemine ühendamine** kasutatakse selle ühendamise puhul ja järgmiste kirjete vastendamise tingimuste puhul: 

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Andmeallika **1Configurations** iga kirje (viide tabelile **ERSolutionTable**) ühendatakse ainult andmeallika **1Versions** kirjetega (sellele viidatakse tabelis **ERSolutionVersionTable**), millel on sama väärtus kui väljadel **Solution** ja **RecId**. Tüüpi **Sisemine ühendamine** kasutatakse selle ühendamise puhul ja järgmiste kirjete vastendamise tingimuste puhul:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - Valik **Käivita** on konfigureeritud **päringuna**, mis tähendab, et see ühendamise andmeallikas käivitatakse käitusajal andmebaasi tasandil otsese SQL-kutsena.

    Pidage meeles, et rakendustabeleid esindavate andmeallikate kirjete ühendamiseks saate määrata ühendamistingimused, kasutades nende tabelite vahelistes AOT-suhetes olevatest väljapaaridest erinevaid väljapaare. Seda tüüpi ühendamise saab konfigureerida käivituma ka andmebaasi tasandil.

6.  Sulgege leht.
7.  Valige **Tühista**.
8.  Laiendage konfiguratsioonide puus andmemudeli üksust **Set2.Summary**:

    - Sidumine **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** näitab, et üksus **Set2.Summary.VersionsNumber** on seotud andmeallika **DetailsSummary** (tüüp **GroupBy**) kogumi väljaga **VersionsNumber**, mis oli konfigureeritud tagastama andmeallika **Üksikasjad** (tüüp **Ühendamine**) ühendatud kirjete arvu.
    - Võtke arvesse, et asukohavalik **Käivitamine** on konfigureeritud **päringuna**, mis tähendab, et see **GroupBy** andmeallikas käivitatakse käitusajal andmebaasi tasandil otsese SQL-kutsena. See on võimalik, kuna alusandmeallikas **Üksikasjad** tüübiga **Ühendamine** on konfigureeritud käivitamiseks andmebaasi tasandil.

    ![Andmeallika GROUPBY parameetrite leht](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  Sulgege leht.
10. Valige **Tühista**.

### <a name="executeERformat"></a> Käivitage ER-i vorming

1.  Finance'ile või RCS‑ile saate juurdepääsu veebibrauseri teisel seansil, kasutades sama mandaati ja ettevõtet nagu esimesel seansil.
2.  Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
3.  Laiendage konfiguratsiooni **Vastendamine andmeallikate JOIN õppimiseks**.
4.  Valige konfiguratsioon **Vormindamine andmeallikate JOIN õppimiseks**.
5.  Valige **Kujundaja**.
6.  Valige **Üksikasjade näitamine**.
7.  Valige **Vastendamine**.
8.  Valige **Laienda/ahenda**.

    Pange tähele, et see vorming on loodud genereeritud tekstifaili asustamiseks uue reaga ER-i konfiguratsiooni iga versiooni (**Versiooni** järjestus) jaoks. Iga loodud rida sisaldab konfiguratsiooni pakkuja nime, kes omab praegust konfiguratsiooni, konfiguratsiooni nime ja konfiguratsiooni versiooni, mis on eraldatud semikooloniga. Loodud faili viimane rida sisaldab ER-i konfiguratsioonide (**Kokkuvõtte** järjestus) avastatud versioonide arvu.

    ![ER-i vormingu koostaja leht](./media/GER-JoinDS-FormatReview.PNG)

    Andmeallikaid **Andmed** ja **Kokkuvõte** kasutatakse konfiguratsiooni versiooni üksikasjade asustamiseks loodud faili:

    - Andmemudelist **Set1** saadud teavet kasutatakse siis, kui valite käitusajal ER-i vormingu kasutamisel kasutajadialoogi lehel andmeallika **Valija** väärtuseks **Ei**.
    - Andmemudelist **Set2** saadud teavet kasutatakse siis, kui valite käitusajal kasutajadialoogi lehel andmeallika **Valija** väärtuseks **Jah**.

    ![ER-i vormingu koostaja leht](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  Valige käsk **Käitus**.
10. Valige dialoogilehe väljal **Kasuta andmeallikat JOIN** väärtus **Ei**.
11. Valige nupp **OK**.
12. Vaadake loodud fail üle.

    ![ER-i kasutajadialoogi leht](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>ER-i vormingu käivitamise jälituse analüüsimine

1.  Valige Finance'i või RCS-i esimesel seansil **Koostaja**.
2.  Valige **Jõudluse jälitus**.
3.  Valige ruudustikus **Jõudluse jälitus** praegust mudelivastenduse komponenti kasutanud ER-i vormingu viimase käivitamise jälituse kõige ülemine kirje.
4.  Valige nupp **OK**.

    Arvestage, et käivitamise statistika teavitab teid rakendusetabelite dubleeritud kutsetest:

    - **ERSolutionTable** on kutsutud nii mitu korda, kui teil on tabelis **ERSolutionVersionTable** konfiguratsiooni versiooni kirjeid, samas kui selliste kutsete arv võib jõudluse suurenemisel väheneda.
    - **ERVendorTable** on kutsutud kaks korda iga tabelis **ERSolutionVersionTable** avastatud konfiguratsiooni versiooni kirje kohta, samas võib selliste kutsete arv samuti väheneda.

    ![ER-i mudelivastenduse koostaja leht](./media/GER-JoinDS-Set1Run2.PNG)

5.  Sulgege leht.

### <a name="execute-er-format"></a>Käivitage ER-i vorming

1.  Lülituge Finance'i või RCS-i teisel seansil ümber oma veebibrauseri vahekaardile.
2.  Valige käsk **Käitus**.
3.  Valige dialoogilehe väljal **Kasuta andmeallikat JOIN** väärtus **Jah**.
4.  Valige nupp **OK**.
5.  Vaadake loodud fail üle.

    ![ER-i kasutajadialoogi leht](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> ER-i vormingu käivitamise jälituse analüüsimine

1.  Valige Finance'i või RCS-i esimesel seansil **Koostaja**.
2.  Valige **Jõudluse jälitus**.
3.  Valige ruudustikus **Jõudluse jälitus** kõige ülemine kirje, mis käsitleb praegust mudelivastenduse komponenti kasutanud ER-i vormingu viimase käivitamise jälitust.
4.  Valige nupp **OK**.

    Võtke arvesse, et käivitamise statistika teavitab teid järgmisest:

    - Rakenduse andmebaas on kutsutud ühe korra, et saada tabelitest **ERVendorTable**, **ERSolutionTable** ja **ERSolutionVersionTable** kirjed nõutavatele väljadele pääsemiseks.

    ![ER-i mudelivastenduse koostaja leht](./media/GER-JoinDS-Set2Run2.PNG)

    - Rakenduse andmebaas on kutsutud ühe korra, et arvutada konfiguratsiooni versioonide arv, kasutades ühendamisi, mis olid konfigureeritud andmeallikas **Üksikasjad**.

    ![ER-i mudelivastenduse koostaja leht](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a>Lisaressursid

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[ER-vormingu täitmise jälitus jõudluse probleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md)

