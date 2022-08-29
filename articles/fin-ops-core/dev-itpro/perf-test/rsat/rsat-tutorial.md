---
title: Regression Suite Automation Tooli õpik
description: See artikkel näitab, kuidas kasutada Regression suite automation tool (RSAT). Selles kirjeldatakse mitmesuguseid funktsioone ja esitatakse näited, kus kasutatakse täpsemat skriptimist.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a270398ddebef0f47a2c31b0ffb022e3df6489c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277400"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Tööriista Regression Suite Automation Tool õpiku kasutamine

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Kasutage Interneti-brauseri tööriistu selle lehe allalaadimiseks ja salvestamiseks PDF-vormingus.

Selles õppetükis tutvustatakse tööriista Regression suite automation tool (RSAT) täpsemaid funktsioone, see hõlmab demomääramist ning kirjeldab strateegiat ja peamisi õppekohti.

## <a name="notable-features-of-rsat-and-task-recorder"></a>RSAT-i ja tegevuse salvestaja olulised funktsioonid

### <a name="validate-a-field-value"></a>Välja väärtuse kinnitamine

RSAT võimaldab teil lisada oma testjuhtumisse kinnitamistoiminguid, et kinnitada eeldatavaid väärtusi. Selle funktsiooni kohta lisateabe saamiseks vaadake artiklit [Eeldatavate väärtuste valideerimine](rsat-validate-expected.md).

Järgmises näites näete, kuidas kasutada seda funktsiooni kinnitamaks, kas vaba kaubavaru väärtus on suurem kui 0 (null).

1. Looge ettevõtte **USMF** demoandmetes tegevuse salvestis, mis sisaldab järgmisi etappe.

    1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
    2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja **Kaubakood** väärtuse **1000** järgi.
    3. Valige **Vaba kaubavaru**.
    4. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja **Tegevuskoht** väärtuse **1** järgi.
    5. Märkige loendis valitud rida.
    6. Kinnitage, et välja **Kokku saadaval** väärtus on **411,0000000000000000**.

2. Salvestage ülesande salvestamine arendaja **salvestusna** ja lisage see oma testjuhtumi juurde Azure DevOps.
3. Lisage testjuhtum katseplaani ja laadige testjuhtum RSAT-sse.
4. Avage Exceli parameetrifail ja minge vahekaardile **TestCaseSteps**.
5. Et kontrollida, kas vaba kaubavaru on alati suurem kui **0**, minge etappi **Kinnita saada saadav kokku** ja muutke selle väärtus väärtuselt **411** väärtusele **0**. Muutke välja **Operaator** väärtust võrdusmärgi (**=**) ja märgiga suurem kui (**\>**).
6. Salvestage ja sulgege Exceli parameetrifail.
7. Valige suvand **Laadi üles**, et salvestada Exceli parameetrifailis tehtud muudatused rakendusse Azure DevOps.

Kui määratud üksuse välja **Kokku saadaval** väärtus varudes on suurem kui 0 (null), siis test läbitakse, olenemata tegelikust vabast kaubavarust.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Salvestatud muutujad ja testjuhtumite aheltöötlus

Üks RSAT põhifunktsioone on testjuhtumite aheltöötlus (test suudab edastada muutujaid teistele testidele). Lisateabe saamiseks vt artiklit [Muutujate kopeerimine keti testjuhtumitele](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Tuletatud testjuhtum

RSAT võimaldab kasutada sama tegevuse salvestist mitme testjuhtumi korral, võimaldades ülesandel töötada erinevate andmete konfiguratsioonidega. Lisateabe saamiseks vt artiklit [Tuletatud testjuhtumid](rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Teatiste ja sõnumite kinnitamine

Seda funktsiooni saab kasutada ka kontrollimaks, kas tegevus toimus. Näiteks kui luuakse tootmistellimus, seda hinnatakse ja see seejärel käivitatakse, kuvab rakendus teate „Tootmine – alusta”, mis annab teada, et tootmistellimust on alustatud.

![Tootmine – alustamise teatis.](./media/use_rsa_tool_05.png)

Saate selle teate kinnitada läbi RSAT, sisestades teate teksti vastava salvestise Exceli parameetrifaili vahekaardile **Teate kinnitamine**.

![Vahekaart Teate kinnitamine.](./media/use_rsa_tool_06.png)

Pärast testjuhtumi käivitamist võrreldakse teadet Exceli parameetrifailis kuvatava teatega. Kui teated ei kattu, siis testjuhtum nurjub.

> [!NOTE]
> Võite sisestada Exceli parameetrifaili vahekaardile **Teate kinnitamine** rohkem kui ühe teate. Teated võivad olla ka tõrke- või hoiatusteated, mitte teavitavad teated.

### <a name="snapshot"></a>Hetktõmmis

See funktsioon teeb kuvatõmmise etappidest, mis läbiti tegevuse salvestamise ajal. See on kasulik auditeerimiseks või silumiseks.

- Selle funktsiooni kasutamiseks RSAT-i kasutajaliidesega töötamise ajal avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Selle funktsiooni kasutamiseks RSAT-i kasutajaliidesega CLI poolt (näiteks Azure DevOps), avage töötamise ajal fail **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Testjuhtumite käivitamisel loob RSAT sammude hetktõmmised (pildid) ja salvestab need töökausta testjuhtumite kausta. Soovitud kaustas luuakse eraldi alamkaust nimega **StepSnapshots**. See kaust sisaldab hetketõmmiseid käitatud testjuhtumite jaoks.

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

![Demostsenaariumi voog.](./media/use_rsa_tool_14.png)

Järgmisel joonisel on kujutatud LCS-i äriprotsesside modelleerija selle stsenaariumi äriprotsesside hierarhia.

![Demostsenaariumi äriprotsessid.](./media/use_rsa_tool_15.png)

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Loetleb kõik käsud või kuvab konkreetse käsu spikri koos saadaval parameetritega.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Valikulised parameetrid

`command`– koht ``[command]``, kus on üks eelnevas loendis nimetatud käskudest.

#### <a name="about"></a>teave

Kuvab installitud RSAT-i versiooni.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Tühjendab ekraani.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>laadi alla

Laadib määratud testjuhtumi manused (salvestamine, käivitamine ja parameetrifailid) väljundkaustast Azure DevOps alla. Käsu abil saate ``list`` saada kõik saadaolevad testjuhtumid ja kasutada **parameetrina mis tahes esimese test_case_id** väärtust.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>allalaadimine: valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab allalaadimisprotsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.

##### <a name="download-required-parameters"></a>download: nõutavad parameetrid

+ `test_case_id`: tähistab testjuhtumi ID-d.

##### <a name="download-optional-parameters"></a>allalaadimine: valikulised parameetrid

+ `output_dir`– näitab väljundi töökausta. Kaust peab olemas olema. Kui seda parameetrit ei määrata, kasutatakse sätetest pärit töökausta.

##### <a name="download-examples"></a>download: näited

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>Laadi alla

Laadib alla manused (salvestamise, käivitamise ja parameetrifailid) kõigi määratud testsviite Azure DevOps korral väljundkaustast. Käsu abil saate ``listtestsuitenames`` saada kõik saadaolevad test ja kasutada iga väärtust **test_suite_name parameetrina**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadlüliti: valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab allalaadimisprotsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.
+ `/byid`: see lüliti näitab, et soovitud test komplekt tuvastatakse Azure DevOps test komplekt nime asemel selle ID-ga.

##### <a name="downloadsuite-required-parameters"></a>downloadmeeter: nõutavad parameetrid

+ `test_suite_name`: tähistab testkomplekti nime. Kui /byid-lülitit pole määratud, on see parameeter **vajalik**. See nimi on testsviidi Azure DevOps nimi.
+ `test_suite_id`: tähistab testkomplekti ID-d. Kui /byid-lüliti on määratud, on see **parameeter** vajalik. See ID on testsviidi Azure DevOps ID.

##### <a name="downloadsuite-optional-parameters"></a>downloadmeeter: valikulised parameetrid

+ `output_dir`– näitab väljundi töökausta. Kaust peab olemas olema. Kui seda parameetrit ei määrata, kasutatakse sätetest pärit töökausta.

##### <a name="downloadsuite-examples"></a>Download tõmbamine: näited

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>redigeeri

Võimaldab teil avada parameetrite faili Exceli programmis ja seda redigeerida.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: nõutud parameetrid

+ `excel_file`: peab sisaldama olemasoleva Exceli faili täielikku teed.

##### <a name="edit-examples"></a>edit: näited

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Loob testkäivitamise ja parameetrifailid väljundkataloogi määratud testjuhtumi jaoks. Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid. Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>loomine: valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab loomisprotsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.
+ `/dllonly`– saate luua ainult testkäivitamisfaile. Ärge looge Uuesti Exceli parameetrifaili.
+ `/keepcustomexcel`: täiendage olemasolevaid parameetrite faili. Saate käivitamisfailid ka uuesti käivitada.

##### <a name="generate-required-parameters"></a>generate: nõutavad parameetrid

+ `test_case_id`: tähistab testjuhtumi ID-d.

##### <a name="generate-optional-parameters"></a>loomine: valikulised parameetrid

+ `output_dir`– näitab väljundi töökausta. Kaust peab olemas olema. Kui seda parameetrit ei määrata, kasutatakse sätetest pärit töökausta.

##### <a name="generate-examples"></a>generate: näited

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Loob esitatud katsejuhtumi uue tuletatud katsejuhtumi (alamtesti juhtumi). Määratud testsviiti lisatakse ka uus katsejuhtum. Käsu abil saate ``list`` saada kõik saadaolevad testjuhtumid ja kasutada **parameetrina mis tahes esimese test_case_id** väärtust.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>genereeritud: valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab loomisprotsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.

##### <a name="generatederived-required-parameters"></a>generatederived: nõutavad parameetrid

+ `parent_test_case_id`: tähistab ülemtestjuhtumi ID-d.
+ `test_plan_id`: tähistab katseplaani ID-d.
+ `test_suite_id`: tähistab testkomplekti ID-d.

##### <a name="generatederived-examples"></a>generatederived: näited

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Loob ainult määratud testjuhtumi testkäivitamisfailid See ei loo Exceli parameetrifaili. Failid luuakse määratud väljundkaustas. Käsu abil saate ``list`` saada kõik saadaolevad testjuhtumid ja kasutada **parameetrina mis tahes esimese test_case_id** väärtust.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab loomisprotsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: nõutavad parameetrid

+ `test_case_id`: tähistab testjuhtumi ID-d.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: valikulised parameetrid

+ `output_dir`– näitab väljundi töökausta. Kaust peab olemas olema. Kui seda parameetrit ei määrata, kasutatakse sätetest pärit töökausta.

##### <a name="generatetestonly-examples"></a>generatetestonly: näited

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Loob testautomatiseeritud failid kõigile määratud test komplekt testjuhtumitele. Käsu abil saate ``listtestsuitenames`` saada kõik saadaolevad test ja kasutada iga väärtust **test_suite_name parameetrina**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>Generatetest nii: valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab loomisprotsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.
+ `/dllonly`– saate luua ainult testkäivitamisfaile. Ärge looge Uuesti Exceli parameetrifaili.
+ `/keepcustomexcel`: täiendage olemasolevate parameetrite faili. Saate käivitamisfailid ka uuesti käivitada.
+ `/byid`: see lüliti näitab, et soovitud test komplekt tuvastatakse Azure DevOps test komplekt nime asemel selle ID-ga.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: nõutavad parameetrid

+ `test_suite_name`: tähistab testkomplekti nime. Kui /byid-lülitit pole määratud, on see parameeter **vajalik**. See nimi on testsviidi Azure DevOps nimi.
+ `test_suite_id`: tähistab testkomplekti ID-d. Kui /byid-lüliti on määratud, on see **parameeter** vajalik. See ID on testsviidi Azure DevOps ID.

##### <a name="generatetestsuite-optional-parameters"></a>Generatetest nii: valikulised parameetrid

+ `output_dir`– näitab väljundi töökausta. Kaust peab olemas olema. Kui seda parameetrit ei määrata, kasutatakse sätetest pärit töökausta.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: näited

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>spikker

Identne [?](#section) käsk.

#### <a name="list"></a>loend

Loetleb kõik praeguse katseplaani saadaolevad katsejuhtumid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Loetleb kõik saadaolevad katseplaanid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Loetleb määratud testkomplekti testjuhtumid. Selle käsu abil ``listtestsuitenames`` saate saada kogu saadaoleva testnime ning kasutada loendis salvestatud parameetrina **suite_name** väärtust.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: nõutavad parameetrid

+ `test_suite_name`: soovitud komplekti nimi.

##### <a name="listtestsuite-examples"></a>listtestsuite: näited

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestrnobyid

Loetleb määratud testkomplekti testjuhtumid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestrnobyid: nõutavad parameetrid

+ `test_suite_id`– soovitud komplekti ID.

##### <a name="listtestsuitebyid-examples"></a>listtestrnobyid: näited

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Loetleb kõik praeguse katseplaani saadaolevad testplaanid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Esitatakse tagasi määratud Exceli parameetrifailiga seotud katsejuhtumi. See käsk kasutab olemasolevaid kohaliku automatiseeritud faile ja ei laadi faile alla asukohast Azure DevOps. Seda käsku ei toetata kassa äri testijuhtumite puhul.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>Valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab protsessi protsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.
+ `/comments[="comment"]`: sisestage kohandatud teabestring, mis kaasatakse **katsejuhtumi** käitamisel kokkuvõtte ja katsetulemuse lehtede kommentaaride Azure DevOps väljale.

##### <a name="playback-required-parameters"></a>playback: nõutavad parameetrid

+ `excel_parameter_file`: Exceli parameetrifaili täielik tee. Fail peab olemas olema.

##### <a name="playback-examples"></a>playback: näited

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Esitab korraga mitu katsejuhtumi tagasi. Katsejuhtumid tuvastatakse nende ID järgi. See käsk laadib alla failid asukohast Azure DevOps. Käsu abil saate ``list`` saada kõik saadaolevad testjuhtumid ja kasutada mis tahes esimese veeru väärtuseid test_case_id **parameetrina**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>Parameetrid <a0/&; – valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab protsessi protsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.
+ `/comments[="comment"]`: sisestage kohandatud teabestring, mis kaasatakse **katsejuhtumi** käitamisel kokkuvõtte ja katsetulemuse lehtede kommentaaride Azure DevOps väljale.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: nõutavad parameetrid

+ `test_case_id1`: olemasoleva katsejuhtumi ID.
+ `test_case_id2`: olemasoleva katsejuhtumi ID.
+ `test_case_idN`: olemasoleva katsejuhtumi ID.

##### <a name="playbackbyid-examples"></a>playbackbyid: näited

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Esitab korraga mitu katsejuhtumi tagasi. Testjuhtumid on identifitseeritud Exceli parameetrifailidega. See käsk kasutab olemasolevaid kohaliku automatiseeritud faile ja ei laadi faile alla asukohast Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>Rõhk <a0/&: valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab protsessi protsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.
+ `/comments[="comment"]`: sisestage kohandatud teabestring, mis kaasatakse **katsejuhtumi** käitamisel kokkuvõtte ja katsetulemuse lehtede kommentaaride Azure DevOps väljale.

##### <a name="playbackmany-required-parameters"></a>playbackmany: nõutavad parameetrid

+ `excel_parameter_file1`: Exceli parameetrifaili täielik tee. Fail peab olemas olema.
+ `excel_parameter_file2`: Exceli parameetrifaili täielik tee. Fail peab olemas olema.
+ `excel_parameter_fileN`: Exceli parameetrifaili täielik tee. Fail peab olemas olema.

##### <a name="playbackmany-examples"></a>playbackmany: näited

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Esitab tagasi ühe või mitme määratud testjuhtumi kõik katsejuhtumid. Kui /local lüliti on määratud, kasutatakse manus korral kohalikke manuseid. Vastasel juhul laaditakse manused alla asukohast Azure DevOps. Selle käsu abil ``listtestsuitenames`` saate saada kogu saadaoleva testdiagrammi ning **kasutada parameetrina mis tahes esimese suite_name** väärtust.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>lisalüliti: valikulised lülitid

+ `/updatedriver`: kui see lüliti on määratud, uuendatakse veebibrauseri veebiaadressi enne protsessi käivitamist vastavalt vajadusele.
+ `/local`: see lüliti näitab, et manusfailide allalaadimise asemel asukohast tuleks kasutada kohalikke manuseid Azure DevOps.
+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab protsessi protsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.
+ `/comments[="comment"]`: sisestage kohandatud teabestring, mis kaasatakse **katsejuhtumi** käitamisel kokkuvõtte ja katsetulemuse lehtede kommentaaride Azure DevOps väljale.
+ `/byid`: see lüliti näitab, et soovitud test komplekt tuvastatakse Azure DevOps test komplekt nime asemel selle ID-ga.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: nõutavad parameetrid

+ `test_suite_name1`: tähistab testkomplekti nime. Kui /byid-lülitit pole määratud, on see parameeter **vajalik**. See nimi on testsviidi Azure DevOps nimi.
+ `test_suite_nameN`: tähistab testkomplekti nime. Kui /byid-lülitit pole määratud, on see parameeter **vajalik**. See nimi on testsviidi Azure DevOps nimi.
+ `test_suite_id1`: tähistab testkomplekti ID-d. Kui /byid-lüliti on määratud, on see **parameeter** vajalik. See ID on testsviidi Azure DevOps ID.
+ `test_suite_idN`: tähistab testkomplekti ID-d. Kui /byid-lüliti on määratud, on see **parameeter** vajalik. See ID on testsviidi Azure DevOps ID.

##### <a name="playbacksuite-examples"></a>playbacksuite: näited

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>Tema kood <a0/&;

Käivitab määratud testsviite kõik Azure DevOps testjuhtumid.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>Valikulised lülitid

+ `/retry[=seconds]`: kui see lüliti on määratud ja kui mõni muu RSAT-i eksemplar on testjuhtumid blokeerinud, ootab protsessi protsess määratud sekundite arvu ja proovib siis veel ühte sekundit. Sekundite vaikeväärtus \[on\] 120 sekundit. Ilma selle lülitita tühistatakse protsess kohe, kui katsejuhtumid on blokeeritud.
+ `/comments[="comment"]`: sisestage kohandatud teabestring, mis kaasatakse **katsejuhtumi** käitamisel kokkuvõtte ja katsetulemuse lehtede kommentaaride Azure DevOps väljale.
+ `/byid`: see lüliti näitab, et soovitud test komplekt tuvastatakse Azure DevOps test komplekt nime asemel selle ID-ga.

##### <a name="playbacksuitebyid-required-parameters"></a>Parameetrid <a0/&;

+ `test_suite_id`: näitab test komplekt ID-d, nagu see on olemas Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>rnobaid: näited

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>quit

Sulgeb rakenduse. See käsk on kasulik ainult siis, kui rakendused töötavad interaktiivses režiimis.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>lahku: näited

`quit`

#### <a name="upload"></a>upload

Laadib üles manusfailid (salvestamine, käivitamine ja parameetrifailid), mis kuuluvad määratud test komplekt või testjuhtumid.Azure DevOps

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: nõutavad parameetrid

+ `test_suite_name`: üles laaditakse kõik määratud test komplekti kuuluvad failid.
+ `test_case_id1`: näitab esimest testjuhtumi ID-d, mis tuleb üles laadida. Kasutage seda parameetrit ainult juhul, kui test komplekt nime pole antud.
+ `test_case_idN`: näitab viimast testjuhtumi ID-d, mis tuleb üles laadida. Kasutage seda parameetrit ainult juhul, kui test komplekt nime pole antud.

##### <a name="upload-examples"></a>upload: näited

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Laadib üles ainult salvestusfaili, mis kuulub ühte või mitmesse määratud testjuhtumi Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: nõutavad parameetrid

+ `test_case_id1`– näitab esimese testjuhtumi ID-d salvestuse jaoks, mis tuleb üles laadida Azure DevOps.
+ `test_case_idN`– näitab viimase katsejuhtumi ID-d salvestuse jaoks, mis tuleb üles laadida Azure DevOps.

##### <a name="uploadrecording-examples"></a>uploadrecording: näited

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Sellel väljal kuvatakse rakenduse kolm kasutusviisi.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Rakenduse käivitamine interaktiivselt:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Rakenduse käivitamine, määrates käsu:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Rakenduse käivitamine sätetefailiga:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

### <a name="windows-powershell-examples"></a>Windows PowerShelli näited

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

```powershell
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
