---
title: Tööriista Regression Suite Automation Tool õppetüki kasutamine
description: Selles teemas näidatakse, kuidas kasutada tööriista Regression suite automation tool (RSAT). Selles kirjeldatakse mitmesuguseid funktsioone ja esitatakse näited, kus kasutatakse täpsemat skriptimist.
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 2d3dde69b102ce161e5c1f1dd393ffceca608bcb
ms.sourcegitcommit: 4fdee254649a751d46632fb4d0d48698e112fa72
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248732"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Tööriista Regression suite automation tool kasutamise õppetükk

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Kasutage Interneti-brauseri tööriistu selle lehe allalaadimiseks ja salvestamiseks PDF-vormingus. 

Selles õppetükis tutvustatakse tööriista Regression suite automation tool (RSAT) täpsemaid funktsioone, see hõlmab demomääramist ning kirjeldab strateegiat ja peamisi õppekohti. 

## <a name="notable-features-of-rsat-and-task-recorder"></a>RSAT-i ja tegevuse salvestaja olulised funktsioonid

### <a name="validate-a-field-value"></a>Välja väärtuse kinnitamine

RSAT võimaldab teil lisada oma testjuhtumisse kinnitamistoiminguid, et kinnitada eeldatavaid väärtusi. Selle funktsiooni kohta lisateabe saamiseks vaadake artiklit [Eeldatavate väärtuste valideerimine](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).

Järgmises näites näete, kuidas kasutada seda funktsiooni kinnitamaks, kas vaba kaubavaru väärtus on suurem kui 0 (null).

1. Looge ettevõtte **USMF** demoandmetes tegevuse salvestis, mis sisaldab järgmisi etappe.

    1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
    2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja **Kaubakood** väärtuse **1000** järgi.
    3. Valige **Vaba kaubavaru**.
    4. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja **Tegevuskoht** väärtuse **1** järgi.
    5. Märkige loendis valitud rida.
    6. Kinnitage, et välja **Kokku saadaval** väärtus on **411,0000000000000000**.

2. Salvestage tegevuse salvestis ja lisage see oma testi juhtumile Azure DevOpsis.
3. Lisage testjuhtum katseplaani ja laadige testjuhtum RSAT-sse.
4. Avage Exceli parameetrifail. Vahekaardil **InventOnhandItem** näete jaotist **Kinnita InventOnhandItem**, mis sisaldab välja **Tehtemärk**.

    ![Väli Tehtemärk](./media/use_rsa_tool_08.png)

5. Kinnitamaks, kas vaba kaubavaru on alati rohkem kui 0, muutke välja **Väärtus** väärtuselt **411** väärtusele **0** ja väljal **Tehtemärk** võrdusmärk (**=**) märgiks „suurem kui” (**\>**).

    ![Väljade Väärtus ja Tehtemärk muudetud väärtused](./media/use_rsa_tool_09.png)

6. Salvestage ja sulgege Exceli parameetrifail.
7. Valige suvand **Laadi üles**, et salvestada Exceli parameetrifailis tehtud muudatused rakendusse Azure DevOps.

Kui määratud üksuse välja **Kokku saadaval** väärtus varudes on suurem kui 0 (null), siis test läbitakse, olenemata tegelikust vabast kaubavarust.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Salvestatud muutujad ja testjuhtumite aheltöötlus

Üks RSAT põhifunktsioone on testjuhtumite aheltöötlus (test suudab edastada muutujaid teistele testidele). Lisateabe saamiseks vt artiklit [Muutujate kopeerimine keti testjuhtumitele](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Tuletatud testjuhtum

RSAT võimaldab kasutada sama tegevuse salvestist mitme testjuhtumi korral, võimaldades ülesandel töötada erinevate andmete konfiguratsioonidega. Lisateabe saamiseks vt artiklit [Tuletatud testjuhtumid](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Teatiste ja sõnumite kinnitamine

Seda funktsiooni saab kasutada ka kontrollimaks, kas tegevus toimus. Näiteks kui luuakse tootmistellimus, seda hinnatakse ja see seejärel käivitatakse, kuvab rakendus teate „Tootmine – alusta”, mis annab teada, et tootmistellimust on alustatud.

![Teatis Tootmine – alusta](./media/use_rsa_tool_05.png)

Saate selle teate kinnitada läbi RSAT, sisestades teate teksti vastava salvestise Exceli parameetrifaili vahekaardile **Teate kinnitamine**.

![Vahekaart Teate kinnitamine](./media/use_rsa_tool_06.png)

Pärast testjuhtumi käivitamist võrreldakse teadet Exceli parameetrifailis kuvatava teatega. Kui teated ei kattu, siis testjuhtum nurjub.

> [!NOTE]
> Võite sisestada Exceli parameetrifaili vahekaardile **Teate kinnitamine** rohkem kui ühe teate. Teated võivad olla ka tõrke- või hoiatusteated, mitte teavitavad teated.

### <a name="snapshot"></a>Hetktõmmis

See funktsioon teeb kuvatõmmise etappidest, mis läbiti tegevuse salvestamise ajal. See on kasulik auditeerimiseks või silumiseks.

- Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Kui käivitate testjuhtumi, teeb RSAT hetktõmmised (pildid) töökaustas oleva testjuhtumite taasesitusekausta etappidest. Kui kasutate RSAT-i vanemat versiooni, salvestatakse pildid kausta **C:\\Kasutajad\\\<Kasutajanimi\>\\AppData\\Roaming\\regressionTool\\playback**, iga käitatud testjuhtumi korral luuakse eraldi kaust.

## <a name="assignment"></a>Määramine

### <a name="scenario"></a>Stsenaarium

1. Toote koostaja loob uue väljastatud toote.
2. Tootmisjuht käivitab tootmistellimuse, et jagada toote varud kaheks.
3. Tootmine alustab ja lõpetab tootmistellimuse ning kontrollib, kas vaba kaubavaru kogus on kaks tükki.
4. Müügimeeskond saab tellimuse neljale tükile uuele tootele. Seega uuendab müügimeeskond netonõudeid dünaamilise plaani kaudu. Kuna täiendav maht pole saadaval, määratakse tellimuse vaikepoliitika väärtusele „tegemise asemel osta”. Seega luuakse plaanitud ostutellimus.
5. Ostja lisab hankija, kinnitab plaanitud ostutellimuse ja seejärel kinnitab ostutellimuse.
6. Kui ostetud kaubad saabuvad kauplusesse, otsib kaupluse töötaja välja seotud ostutellimuse ja võtab kaubad vastu. Kuna tellimus on nüüd lõpule viidud, võib kaubad müügitellimuse suhtes komplekteerida ja pakkida.
7. Finantsosakond sisestab ostuarve ja müügiarve.

Järgmisel joonisel on näha selle stsenaariumi voog.

![Demostsenaariumi voog](./media/use_rsa_tool_14.png)

Järgmisel joonisel on kujutatud LCS-i äriprotsesside modelleerija selle stsenaariumi äriprotsesside hierarhia.

![Demostsenaariumi äriprotsessid](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strateegia – peamised õppepunktid

### <a name="data"></a>Andmed

- Veenduge, et teil oleks olemas esindavad andmemahud (koopia tootmis- / kuldse konfiguratsiooni andmed ja migreeritud andmed).
- Kui loote uued andmed tegevuse salvestaja kaudu, looge katsenimed, mis ei ole vastuolus olemasolevate nimedega (nt kasutage eesliidet nagu **RSATxxx**).
- Kasutage Azure’i ajapunktipõhist taastet, et käivitada uuesti testid muudes kui järgu 1 keskkondades.
- Kuigi võite kasutada kordumatu kombinatsiooni loomiseks Exceli funktsioone **RANDOM** ja **NOW**, on panus arvestatavalt kõrge. Siin on näide.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Ülesande salvestaja

- Enne salvestamise alustamist määratlege stsenaariumid. Hästi hallatud projektil on eelmääratletud teststsenaariumid. Testjuhtumi loomiseks võtke arvesse, kui ennustatav on nende teststsenaariumite tulemus.
- Tükeldage salvestisi, kui need tehakse eri rollides või kui enne järgmist etappi on ooteaeg või väline sündmus.
- Vältige väärtuste valimist loendites. Selle asemel kasutage tekstivorminguid, nt **FIFO**, **AudioRM** ja **SiteWH**. Kui valite loendis, salvestatakse väärtuse asukoht loendis, mitte väärtus ise. Kui sellele loendile üksuseid lisatakse, võib väärtuse asukoht muutuda. Seega kasutab salvestus muud parameetrit ja see võib mõjutada ülejäänud stsenaariumi.
- Mõelge mitme kasutaja käitumisele. Näiteks ärge eeldage, et alati valitakse automaatselt teie äsja loodud müügitellimus. Selle asemel kasutage filtrit õige tellimuse leidmiseks.
- Kasutage tegevuse salvestajas funktsiooni Kopeeri äsja loodud toote nime salvestamiseks, et seda saaks kasutada ühendatud testjuhtumites.
- Kasutage tegevuse salvestajad funktsiooni Kinnita kontrollpunktide määramiseks, mis kontrollivad, kas etapid on käivitatud õigesti.

### <a name="rsat"></a>RSAT

- Testi käivitamiseks teises ettevõttes saate muuta ettevõtte nime Exceli parameetrifaili vahekaardil **Üldine**. Veenduge, et sätted ja andmed oleksid äsja valitud ettevõttes saadaval.
- Saate muuta testkasutajat Exceli parameetrifaili vahekaardil **Üldine**. Määrake testjuhtumit käivitava kasutaja meili ID. Sellisel juhul saab testjuhtumit käivitada, kasutades määratud kasutaja turbeõigus.
- Ootamiseks enne testi käivitamist saate määrata pausi Exceli parameetrifaili vahekaardil **Üldine**. Seda pausi saab kasutada pakett-töös (nt kui töövoog tuleb käivitada enne, kui järgmist etappi saab läbida).

## <a name="advanced-scripting"></a>Täpsem skriptimine

### <a name="cli"></a>CLI

RSAT saab käivitada aknast **Käsuviip** või **PowerShell**.

> [!NOTE]
> Veenduge, et keskkonnamuutuja **TestRoot** oleks seatud RSAT installiteele. (Avage Microsoft Windowsis suvand **Juhtpaneel**, valige **Süsteem ja turvalisus \> Süsteem \> Täpsemad süsteemisätted** ja seejärel valige suvand **Keskkonnamuutujad**.)

1. Avage administraatorina aken **Käsuviip** või **PowerShell**.
2. Navigeerige RSAT-i installikausta.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Esitage kõik käsud.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>? 
Kuvab kõigi saadaolevate käskude ja nende parameetrite spikri.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a>Valikulised parameetrid

**``command``**


Kus ``[command]`` on üks allpool määratud käskudest.


#### <a name="about"></a>about
Kuvab praeguse versiooni.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls
Tühjendab ekraani.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a>laadi alla
Laadib alla määratud testjuhtumi manused väljundkausta. Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid. Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``test_case_id``** Tähistab testjuhtumi ID-d.  
**``output_dir``** Tähistab väljundkausta. Kaust peab olemas olema.

##### <a name="examples"></a>Näited

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a>redigeeri
Võimaldab teil avada parameetrite faili Exceli programmis ja seda redigeerida.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``excel_file``** Peab sisaldama olemasoleva Exceli faili täielikku teed.

##### <a name="examples"></a>Näited
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a>generate
Loob testkäivitamise ja parameetrifailid väljundkataloogi määratud testjuhtumi jaoks.
Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid. Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``test_case_id``** Tähistab testjuhtumi ID-d.  
**``output_dir``** Tähistab väljundkausta. Kaust peab olemas olema.

##### <a name="examples"></a>Näited
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a>generatederived
Loob uue testjuhtumi, mis tulenevad esitatud testjuhtumist. Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid. Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``parent_test_case_id``** Tähistab ülemtestjuhtumi ID-d.  
**``test_plan_id``** Tähistab katseplaani ID-d.  
**``test_suite_id``** Tähistab testkomplekti ID-d.

##### <a name="examples"></a>Näited
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a>generatetestonly
Loob väljundkataloogi määratud testjuhtumi jaoks ainult testkäivitamise faili. Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid. Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``test_case_id``** Tähistab testjuhtumi ID-d.  
**``output_dir``** Tähistab väljundkausta. Kaust peab olemas olema.

##### <a name="examples"></a>Näited
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a>generatetestsuite
Loob kõik väljundkataloogi määratud komplekti testjuhtumid.
Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid. Kasutage veeru mis tahes väärtust parameetrina **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``test_suite_name``** Tähistab testkomplekti nime.  
**``output_dir``** Tähistab väljundkausta. Kaust peab olemas olema.

##### <a name="examples"></a>Näited
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a>spikker
Identne [?](#section) käsuga


#### <a name="list"></a>loend
Loetleb kõik saadaolevad testjuhtumid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a>listtestplans
Loetleb kõik saadaolevad katseplaanid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a>listtestsuite
Loetleb määratud testkomplekti testjuhtumid. Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid. Kasutage esimese veeru mis tahes väärtust parameetrina **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``suite_name``** Soovitud komplekti nimi.

##### <a name="examples"></a>Näited
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a>listtestsuitenames
Loetleb kõik saadaolevad testkomplektid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a>playback
Taasesitab Exceli faili abil testjuhtumi.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``excel_file``** Exceli faili täielik tee. Fail peab olemas olema. 

##### <a name="examples"></a>Näited
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a>playbackbyid
Taasesitab korraga mitu testjuhtumit.
Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid. Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``test_case_id1``** Olemasoleva testjuhtumi ID.  
**``test_case_id2``** Olemasoleva testjuhtumi ID.  
**``test_case_idN``** Olemasoleva testjuhtumi ID.  

##### <a name="examples"></a>Näited
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a>playbackmany
Taasesitab korraga mitu testjuhtumit, kasutades Exceli faile.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``excel_file1``** Exceli faili täielik tee. Fail peab olemas olema.  
**``excel_file2``** Exceli faili täielik tee. Fail peab olemas olema.  
**``excel_fileN``** Exceli faili täielik tee. Fail peab olemas olema.  

##### <a name="examples"></a>Näited
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a>playbacksuite
Taasesitab konkreetse testkomplekti kõik testjuhtumid. Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid. Kasutage esimese veeru mis tahes väärtust parameetrina **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``suite_name``** Soovitud komplekti nimi.

##### <a name="examples"></a>Näited
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a>quit
Sulgeb rakenduse.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a>upload
Laadib üles kõik määratud testkomplekti või testjuhtumitesse kuuluvad failid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a>Nõutud parameetrid
**``suite_name``** Kõik määratud testkomplekti kuuluvad failid laaditakse üles.
**``testcase_id``** Kõik määratud testjuhtumi(te)sse kuuluvad failid laaditakse üles.

##### <a name="examples"></a>Näited
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a>uploadrecording
Laadib üles ainult määratud testjuhtumitesse kuuluva salvestamisfaili.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a>Nõutud parameetrid
**``testcase_id``** Määratud testjuhtumitesse kuuluv salvestamisfail laaditakse üles.

##### <a name="examples"></a>Näited
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a>usage
Näitab selle rakenduse kahte käivitamisviisi: üks kasutab vaikimisi seadistusfaili, teine esitab seadistusfaili.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a>Windows PowerShelli näited

[!IMPORTANT] Allolevad näidisskriptid on esitatud olemasoleval kujul ja need on illustratiivsed ning Microsoft ei toeta neid.

#### <a name="run-a-test-case-in-a-loop"></a>Testjuhtumi käivitamine tsüklis

Teil on testskript, mis loob uue kliendi. Skriptimise kaudu saab seda testjuhtumis käivitada tsüklis, muutes enne iga iteratsiooni käivitamist järgmised andmed juhuslikuks.

- Kliendi ID
- Kliendi nimi
- Kliendi aadress

Kliendi ID on vormingus *ATCUS\<number\>*, kus \<number\> on väärtus vahemikus **000000001** kuni **999999999**.

Järgmises näites kasutatakse üht parameetrit, **alusta**, esimese kasutatud numbri määramiseks. See kasutab teist parameetrit, **nr**, loodavate klientide arvu määramiseks. Iga iteratsiooni kohta muudetakse Exceli parameetrifailis parameetreid, kasutades funktsiooni UpdateCustomer. Seejärel käivitatakse RSAT käsurida funktsioonis RunTestCase.

Avage Microsoft Windows PowerShell Integrated Scripting Environment (ISE) haldusrežiimis ja kleepige järgmine kood aknasse nimega **Untitled1.ps1**.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Microsoft Dynamics 365 andmetest sõltuva skripti käivitamine

Järgmises näites kasutatakse kutset Open Data Protocol (OData) ostutellimuse tellimuse oleku leidmiseks. Kui olek ei ole **arveldatud**, võite näiteks käivitada RSAT testjuhtumi, mis arve sisestab.

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
