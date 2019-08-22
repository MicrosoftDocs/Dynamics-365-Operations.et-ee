---
title: Tööriista Regression suite automation tool kasutamise õppetükk
description: Selles teemas näidatakse, kuidas kasutada tööriista Regression suite automation tool (RSAT). Selles kirjeldatakse mitmesuguseid funktsioone ja esitatakse näited, kus kasutatakse täpsemat skriptimist.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 02933c1649960a4fb58953798799422528d6731d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850823"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Tööriista Regression suite automation tool kasutamise õppetükk

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Kasutage Interneti-brauseri tööriistu selle lehe allalaadimiseks ja salvestamiseks PDF-vormingus. 

Selles õppetükis tutvustatakse tööriista Regression suite automation tool (RSAT) täpsemaid funktsioone, see hõlmab demomääramist ning kirjeldab strateegiat ja peamisi õppekohti.

## <a name="features-of-rsattask-recorder"></a>RSAT / tegevuse salvestaja funktsioonid

### <a name="validate-a-field-value"></a>Välja väärtuse kinnitamine

Teavet selle funktsiooni kohta vaadake teemast [Uue tegevuse salvestise loomine, millel on valideerimise funktsioon](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Salvestatud muutuja

Teavet selle funktsiooni kohta vaadake teemast [Olemasoleva tegevuse salvestise muutmine salvestatud muutuja loomiseks](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Tuletatud testjuhtum

1. Avage Regression suite automation tool (RSAT) ja valige mõlemad loodud testjuhtumid jaotisest [Tööriista Regression suite automation tool seadistamine ja installimine](./hol-set-up-regression-suite-automation-tool.md).
2. Valige suvandid **Uus \> Loo tuletatud testjuhtum**.

    ![Tuletatud testjuhtumi käsu loomine menüüs Uus](./media/use_rsa_tool_01.png)

3. Saate teate, et tuletatud testjuhtum luuakse iga valitud testjuhtumi kohta praeguses testkomplektis ja igal tuletatud testjuhtumil on oma koopia Exceli parameetrifailist. Valige nupp **OK**.

    > [!NOTE]
    > Kui käivitate tuletatud testjuhtumi, kasutab see ülemtestjuhtumi tegevuse salvestist ja oma koopiat Exceli parameetrifailist. Nii saate käivitada sama testi eri parameetritega, ilma et peaksite säilitama rohkem kui ühe tegevuse salvestise. Tuletatud testjuhtum ei pea olema osa samast testkomplektist kui selle ülemtestjuhtum.

    ![Teateaken](./media/use_rsa_tool_02.png)

    Luuakse kaks täiendavat testjuhtumit ja nende jaoks valitakse märkeruut **Tuletatud?**.

    ![Loodud tuletatud testjuhtumid](./media/use_rsa_tool_03.png)

    Tuletatud testjuhtum luuakse automaatselt rakenduses Azure DevOps. See on testjuhtumi **Uue toote loomine** allüksus ja see märgistatakse spetsiaalse märksõnaga: **RSAT:DerivedTestSteps**. Need testjuhtumid lisatakse ka automaatselt katseplaanile rakenduses Azure DevOps.

    ![Märksõna RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Kui tuletatud testjuhtumid pole mingil põhjusel õiges järjekorras, minge rakendusse Azure DevOps ja muutke testjuhtumite järjekorda testkomplektis, et RSAT saaks need käivitada õiges järjekorras.

4. Valige tuletatud testjuhtumid ja seejärel valige nupp **Redigeeri** vastavate Exceli parameetrifailide avamiseks.
5. Redigeerige neid Exceli parameetrifaile samamoodi, nagu redigeerisite ülemfaile. Teisisõnu veenduge, et toote ID oleks seadistatud nii, et see luuakse automaatselt. Peale selle veenduge, et salvestatud muutuja kopeeritakse asjakohastesse väljadesse.
6. Mõlema Exceli parameetrifaili vahekaardil **Üldine** uuendage väli **Ettevõte** väärtusele **USSI**, et tuletatud testjuhtumid käivitatakse muu juriidilise isiku suhtes kui ülemtestjuhtum. Testjuhtumite käivitamiseks konkreetse kasutaja (või konkreetse kasutajaga seotud rolli) suhtes saate uuendada välja **Testkasutaja** väärtust.
7. Valige käsk **Käivita** ja kontrollige, kas toode luuakse nii USMF-i juriidilises isikus kui ka USSI juriidilises isikus.

### <a name="validate-notifications"></a>Teatiste kontrollimine

Seda funktsiooni saab kasutada ka kontrollimaks, kas tegevus toimus. Näiteks kui luuakse tootmistellimus, seda hinnatakse ja see seejärel käivitatakse, kuvab Microsoft Dynamics 365 for Finance and Operations teate „Tootmine – alusta”, mis annab teada, et tootmistellimust on alustatud.

![Teatis Tootmine – alusta](./media/use_rsa_tool_05.png)

Saate selle teate kinnitada läbi RSAT, sisestades teate teksti vastava salvestise Exceli parameetrifaili vahekaardile **Teate kinnitamine**.

![Vahekaart Teate kinnitamine](./media/use_rsa_tool_06.png)

Pärast testjuhtumi käivitamist võrreldakse teadet Exceli parameetrifailis teatega, mis kuvatakse rakenduses Finance and Operations. Kui teated ei kattu, siis testjuhtum nurjub.

> [!NOTE]
> Võite sisestada Exceli parameetrifaili vahekaardile **Teate kinnitamine** rohkem kui ühe teate. Teated võivad olla ka tõrke- või hoiatusteated, mitte teavitavad teated.

### <a name="validate-values-by-using-operators"></a>Väärtuste kinnitamine tehtemärke kasutades

Eelmistes RSAT versioonides saite väärtusi kinnitada ainult siis, kui kontrollväärtus oli võrdne eeldatava väärtusega. Uue funktsiooniga saate kinnitada, kas muutuja ei ole konkreetse väärtusega võrdne, on sellest väiksem või sellest suurem.

- Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    Exceli parameetrifaili ilmub uus väli **Tehtemärk**.

    > [!NOTE]
    > Kui olete kasutanud RSAT vanemat versiooni, peate looma uued Exceli parameetrifailid.

    ![Väli Tehtemärk](./media/use_rsa_tool_07.png)

Järgmises näites näete, kuidas kasutada seda funktsiooni kinnitamaks, kas vaba kaubavaru väärtus on suurem kui 0 (null).

1. Looge ettevõtte **USMF** demoandmetes tegevuse salvestis, mis sisaldab järgmisi etappe.

    1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
    2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja **Kaubakood** väärtuse **1000** järgi.
    3. Valige **Vaba kaubavaru**.
    4. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja **Tegevuskoht** väärtuse **1** järgi.
    5. Märkige loendis valitud rida.
    6. Kinnitage, et välja **Kokku saadaval** väärtus on **411,0000000000000000**.

2. Salvestage tegevuse salvestis LCS-is BPM-i teeki ja sünkroonige see rakendusega Azure DevOps.
3. Lisage testjuhtum katseplaani ja laadige testjuhtum RSAT-sse.
4. Avage Exceli parameetrifail. Vahekaardil **InventOnhandItem** näete jaotist **Kinnita InventOnhandItem**, mis sisaldab välja **Tehtemärk**.

    ![Väli Tehtemärk](./media/use_rsa_tool_08.png)

5. Kinnitamaks, kas vaba kaubavaru on alati rohkem kui 0, muutke välja **Väärtus** väärtuselt **411** väärtusele **0** ja väljal **Tehtemärk** võrdusmärk (**=**) märgiks „suurem kui” (**\>**).

    ![Väljade Väärtus ja Tehtemärk muudetud väärtused](./media/use_rsa_tool_09.png)

6. Salvestage ja sulgege Exceli parameetrifail.
7. Valige suvand **Laadi üles**, et salvestada Exceli parameetrifailis tehtud muudatused rakendusse Azure DevOps.

Kui määratud üksuse välja **Kokku saadaval** väärtus varudes on suurem kui 0 (null), siis test läbitakse, olenemata tegelikust vabast kaubavarust.

### <a name="generator-logs"></a>Koostaja logid

See funktsioon loob kausta, mis sisaldab käivitatud testjuhtumite logisid.

- Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.

    ```
    <add key="LogGeneration" value="false" />
    ```

Pärast testjuhtumite käivitamist leiate logifailid kaustast **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![Kaust GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> Kui enne failis .config väärtuse muutmist olid olemas testjuhtumid, ei looda nende testjuhtumite kohta logisid, kuni loote uue testkäivitusfailid.
> 
> ![Käsk Loo ainult testkäivitusfailid menüüs Uus](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Hetktõmmis

See funktsioon teeb kuvatõmmise etappidest, mis läbiti tegevuse salvestamise ajal.

- Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Kausta **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** luuakse iga käivitatud testjuhtumi kohta eraldi kaust.

![Testjuhtumi hetktõmmise kaust](./media/use_rsa_tool_12.png)

Igast kaustast leiate testjuhtumite käivitamisel läbitud etappide hetktõmmised.

![Hetktõmmiste failid](./media/use_rsa_tool_13.png)

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

Järgmisel joonisel on näha selle stsenaariumi äriprotsessid RSAT-s.

![Demostsenaariumi äriprotsessid](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strateegia – peamised õppepunktid

### <a name="data"></a>Andmed

- Veenduge, et teil oleks olemas esindavad andmemahud (koopia tootmis- / kuldse konfiguratsiooni andmed ja migreeritud andmed).
- Kui loote uued andmed tegevuse salvestaja kaudu, looge katsenimed, mis ei ole vastuolus olemasolevate nimedega (nt kasutage eesliidet nagu **RSATxxx**).
- Kasutage Azure’i ajapunktipõhist taastet, et käivitada uuesti testid muudes kui järgu 1 keskkondades.
- Kuigi võite kasutada kordumatu kombinatsiooni loomiseks Exceli funktsioone **RANDOM** ja **NOW**, on panus arvestatavalt kõrge. Siin on näide.

    ```
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

### <a name="command-line"></a>Käsurida

RSAT-d saab käivitada aknast **Käsuviip**.

> [!NOTE]
> Veenduge, et keskkonnamuutuja **TestRoot** oleks seatud RSAT installiteele. (Avage Microsoft Windowsis suvand **Juhtpaneel**, valige **Süsteem ja turvalisus \> Süsteem \> Täpsemad süsteemisätted** ja seejärel valige suvand **Keskkonnamuutujad**.)

1. Avage administraatorina aken **Käsuviip**.
2. Käivitage tööriist installikaustast.

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Esitage kõik käsud.

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>Windows PowerShelli näited

#### <a name="run-a-test-case-in-a-loop"></a>Testjuhtumi käivitamine tsüklis

Teil on testskript, mis loob uue kliendi. Skriptimise kaudu saab seda testjuhtumis käivitada tsüklis, muutes enne iga iteratsiooni käivitamist järgmised andmed juhuslikuks.

- Kliendi ID
- Kliendi nimi
- Kliendi aadress

Kliendi ID on vormingus *ATCUS\<number\>*, kus \<number\> on väärtus vahemikus **000000001** kuni **999999999**.

Järgmises näites kasutatakse üht parameetrit, **alusta**, esimese kasutatud numbri määramiseks. See kasutab teist parameetrit, **nr**, loodavate klientide arvu määramiseks. Iga iteratsiooni kohta muudetakse Exceli parameetrifailis parameetreid, kasutades funktsiooni UpdateCustomer. Seejärel käivitatakse RSAT käsurida funktsioonis RunTestCase.

Avage Microsoft Windows PowerShell Integrated Scripting Environment (ISE) haldusrežiimis ja kleepige järgmine kood aknasse nimega **Untitled1.ps1**.

```
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
$excelFilename = "full path to excel file parameter file"
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

```
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
