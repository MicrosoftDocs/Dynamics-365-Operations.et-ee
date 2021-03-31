---
title: Finantsülevaadete konfigureerimine (eelversioon)
description: See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cf29e3c05f9fdcc685017a4c640ef32c40989c73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208553"
---
# <a name="configuration-for-finance-insights-preview"></a>Finantsülevaadete konfigureerimine (eelversioon)

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finantsülevaated kombineerivad rakenduse Microsoft Dynamics 365 Finance funktsioonid teenustega Microsoft Dataverse, Azure ja AI Builder, et pakkuda võimsaid prognoosimise tööriistu teie organisatsioonile. See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi.

## <a name="deploy-dynamics-365-finance"></a>Rakenduse  Dynamics 365 Finance juurutamine

Keskkonna juurutamiseks tehke järgmist.

1. Looge teenuses Microsoft Dynamics Lifecycle Services (LCS) või värskendage Dynamics 365 Finance’i keskkonda. Keskkond vajab rakenduse versiooni 10.0.11 / Platform värskendust 35 või uuemat.
2. Keskkond peab olema hea kättesaadavusega (HA) liivakasti keskkond. (Seda tüüpi keskkond on tuntud ka kui järgu 2 keskkond.) Lisateavet vt teemast [Keskkonna kavandamine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Kui kasutate Contoso demoandmeid, vajate Contoso makse prognoosimise kasutamiseks, rahavoo prognoosimiseks ja eelarve prognoosimise funktsioonideks täiendavaid näidisandmeid. 

## <a name="configure-dataverse"></a>Dataverse konfigureerimine

Saate lõpetada järgmised konfigureerimise etapid käsitsi või saate kiirendada konfigureerimisprotsessi, kasutades esitatud Windows PowerShelli skripti. Kui PowerShelli skript on töötamise lõpetanud, annab see teile väärtused, mida kasutada finantsülevaadete konfigureerimiseks. 

> [!NOTE]
> Skripti käivitamiseks avage arvutis PowerShell. Võite vajada PowerShelli versiooni 5. Microsoft Azure CLI valik „Proovi seda” ei pruugi töötada.

# <a name="manual-configuration-steps"></a>[Käsitsi konfigureerimise etapid](#tab/configuration-steps)

1. Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com/) ja järgige neid samme, et luua uus Dataverse’i keskkond samas Active Directory rentnikus.

    1. Avage leht **Keskkonnad**.

        [![Keskkondade leht](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Valige **Uus keskkond**.
    3. Väljal **Tüüp** valige **Liivakast**.
    4. Määrake suvand **Andmebaas** valikule **Jah**.
    5. Valige **Edasi**.
    6. Valige oma organisatsiooni keel ja valuuta.
    7. Võtke vastu teiste väljade vaikeväärtused.
    8. Valige käsk **Salvesta**.
    9. Värskendage lehte **Keskkonnad**.
    10. Oodake, kuni välja **Olek** väärtus uuendatakse olekuks **Valmis**.
    11. Märkige üles rakenduse Dataverse organsisatsiooni ID.
    12. Valige uus keskkond ja seejärel valige suvand **Sätted**.
    13. Valige **Ressursid \> Kõik pärandsätted**.
    14. Ülemisel navigeerimisribal valige **Sätted** ja valige seejärel **Kohandamised**.
    15. Valige **Arendaja ressursid**.
    16. Määrake välja **Eksemplari viiteteabe ID** rakenduse Dataverse organisatsiooni ID väärtus, mille varem kirja panite.
    17. Märkige üles brauseri aadressiribal olev Dataverse’i organisatsiooni URL. Näiteks URL võib olla `https://org42b2b3d3.crm.dynamics.com`.

2. Kui kavatsete kasutada rahavoo prognoosimise või eelarve prognoosimise funktsiooni, toimige järgmiselt, et värskendada oma organisatsiooni marginaali limiiti vähemalt 50 megabaidini (MB).

    1. Avage [Power Apps'i portaal](https://make.powerapps.com).
    2. Valige vastloodud keskkond ja seejärel valige **Täpsemad sätted**.
    3. Valige **Sätted \>Meili konfiguratsioon**.
    4. Muute välja **Maksimaalne faili suurus** väärtuseks **51 200**. (Väärtus on väljendatud kilobaitides \[KB\].)
    5. Muudatuste salvestamiseks klõpsake nuppu **OK**.

# <a name="windows-powershell-configuration-script"></a>[Windows PowerShelli konfiguratsiooni skript](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a>Azure'i häälestamise konfigureerimine

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>Sisestage Dataverse’i kausta ID ja kasutaja Azure AD objekti ID

1. Sisestage Dataverse’i kausta ID.

    1. Avage [Azure portaal](https://portal.azure.com).
    2. Logige sisse, kasutades kasutaja ID-d, mida kasutati Dataverse’i keskkonna loomiseks.
    3. Avage **Azure Active Directory**.
    4. Kopeerige väärtus **Rentniku ID**.

2. Sisestage kasutaja Azure Active Directory (Azure AD) objekti ID.

    1. [Azure portaalis](https://portal.azure.com) avage suvand **Kasutajad** ja otsige kasutajat meiliaadressi järgi.
    2. Valige kasutajanimi.
    3. Kopeerige väärtus **Objekti ID**.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Kasutage Azure Coud Shelli, et seadistada finantsplevaadete andmejärve ressursid

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShelli skripti kasutamine](#tab/use-a-powershell-script)

Windows PowerShelli skript on esitatud, seega saate hõlpsalt häälestada Azure’i ressursse, mida kirjeldatakse teemas [Azure Data Lake’i ekspordi konfigureerimine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake). Kui eelistate käsitsi häälestust, jätke see protseduur vahele ja jätkake protseduuriga jaotises [Käsitsi häälestus](#manual-setup).

> [!NOTE]
> PowerShelli skripti käitamiseks järgige allolevaid samme. Azure CLI valik „Proovi seda” või arvutis skripti käitamine ei pruugi töötada.

Järgige neid samme, et konfigureerida Azure Windows PowerShelli skripti abil. Teil peavad olema õigused Azure’i ressursigrupi, Azure’ii ressursside ja Azure AD rakenduse loomiseks. Lisateavet nõutavate õiguste kohta vt [Azure AD õiguste kontrollimine](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Avage [Azure’i portaalis](https://portal.azure.com) oma sihtkoha Azure’i tellimus. Valige nupp **Cloud Shell** väljast **Otsing** paremal.
2. Valige **PowerShell**.
3. Looge salvestusruum, kui teil palutakse seda teha. Seejärel laadige Windows PowerShelli skript seansile.
4. Käivitage skript.
5. Järgige skripti käivitamiseks viipasid.
6. Kasutage skripti väljundi teavet, et installida LCS-i lisandmoodul **Data Lake’i eksportimine**.
7. Kasutage skripti väljundi teavet, et lubada üksuse salvestusruum rakenduse Finance lehel **Andmeühendused** (**Süsteemi haldus \> Süsteemi parameetrid \> Andmeühendused**).

### <a name="manual-setup"></a>Käsitsi häälestus

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Lisage Azure AD rentnikule rakendused

1. Avage [Azure’i portaalis](https://portal.azure.com) suvand **Azure Active Directory**.
2. Valige käsk **Halda \> Ettevõtte rakendused**.
3. Otsige rakenduse ID järgi järgmisi rakendusi.

    | Avaldus                              | Rakenduse kood                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builderi autoriseerimise teenus         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Kui te ei leia ühtegi eelnevat rakendust, proovige järgmisi samme.

1. Oma kohalikus arvutis valige menüü **Start** ja otsige suvandit **PowerShell**.
2. Valige ja hoidke (või paremklõpsake) suvandit **Windows PowerShell** ja valige seejärel käsk **Käivita administraatorina**.
3. Mooduli **AzureAD** installimiseks käivitage järgmine käsk.

    `Install-Module -Name AzureAD`

4. Kui NuGeti pakkuja on kohustatud jätkama, valige selle installimiseks suvand **Y**.
5. Kui ilmub teade „Ebausaldusväärne hoidla”, valige jätkamiseks **Y**.
6. Iga rakenduse jaoks, mis tuleb lisada, käivitage järgmised käsud rakenduse lisamiseks Azure AD-sse. Kui teilt küsitakse, logige sisse Azure AD administraatorina.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure'i ressursside loomine

> [!NOTE]
> Veenduge, et looksite Azure AD eksemplaris ja Dataverse’i keskkonnas samad ressursid. Te ei saa kasutada ressursse erinevast Azure AD eksemplarist.

1. Looge uus salvestamise konto.

    1. Looge [Azure’i portaalis](https://portal.azure.com) salvestamise konto.
    2. Dialoogiboksis **Salvestamise konto loomine** määrake järgmised väljad.

        - **Asukoht** – valige andmekeskuse, kus teie keskkond asub.
        - **Jõudlus** – soovitame valida suvandi **Standardne**.
        - **Konto liik** – peate valima **StorageV2**.

    3. Dialoogiaknas **Täpsemad suvandid** valige suvandi **Data Lake storage Gen2** valik **Luba** jaotises **Hierarhilised nimeruumide**. Kui te selle funktsiooni keelate, ei saa te tarbida andmeid, mida Finance and Operationsi rakendused kirjutavad, kasutades selliseid teenuseid nagu Power BI andmevoog.
    4. Valige **Läbivaatus ja loomine**. Kui juurutamine on lõpule viidud, kuvatakse Azure’i portaalis uus ressurss.
    5. Avage loodud salvestusruumi konto.
    6. Valige vasakpoolses menüüs **Juurdepääsuvõtmed**.
    7. Kopeerige ja salvestage ühenduse string kas **Võti1** või **Võti2** jaoks.
    8. Kopeerige ja salvestage salvestuskonto nimi.

2. Looge uus võtmehoidla.

    1. Looge [Azure’i portaalis](https://portal.azure.com) võtmehoidla.
    2. Valige dialoogiboksis **Võtmehoidla** väljal **Asukoht** andmekeskus, kus teie keskkond asub.
    3. Kui võtmehoidla on loodud, valige see loendist ja seejärel valige suvand **Saladused**.
    4. Valige **Loo/impordi**.
    5. Valige dialoogiboksis **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.
    6. Sisestage saladuse nimi. Märkige üles nimi, sest peate selle hiljem esitama.
    7. Sisestage väljale **Väärtus** ühenduse string, mille olete eelmise protseduuri savestamisekontolt saanud.
    8. Valige **Luba** ja seejärel **Loo**. Saladus on loodud ja lisatud võtmehoidlasse.
    9. Avage suvand **Võtmehoidla ülevaade** ja märkige üles DNS-i nimi.

3. Looge ja registreerige Azure AD rakendus.

    1. Avage [Azure’i portaalis](https://portal.azure.com) suvand **Azure Active Directory** ja valige **Rakenduse registreerimised**.
    2. Valige **Uus rakenduse registreerimine** ja määrake järgmised väljad.

        - **Nimi** – sisestage rakenduse nimi.
        - **Rakenduse tüüp** – valige **Web API**.
        - **URI häälestuse ümbersuunamine** – sisestage oma Dynamics 365 eksemplari URL, nt `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Avage äsja loodud rakendus ja kopeerige ja salvestage selle **rakenduse (kliendi) ID** väärtus. Peate selle väärtuse hiljem sisestama, kui seadistate võtmehoidla.
    4. Avage **API load** ja järgige järgmisi samme.

        1. Valige **Lisa luba**.
        2. Valige **Azure võtmehoidla**.
        3. Kui olete valinud delegeeritud õigused, valige **kasutaja\_isik**.
        4. Valige **Lisa load**.

    5. Valige rakenduse menüüs **Serdid \& saladused** ja seejärel järgige võtmehoidla saladuse loomiseks järgmisi samme.

        1. Valige **Uus kliendi saladus**.
        2. Väljale **Võtme kirjeldus** sisestage nimi.
        3. Valige kestus ja valige seejärel **Lisa**. Väljale **Väärtus** luuakse saladus.
        4. Kopeerige ja salvestage salajane väärtus.

4. Võtmehoidla saladuste loomine.

    1. Minge võtmehoidla, mille varem lõite, ja valige **Saladused**.
    2. Järgmise tabeli iga salajase nime puhul järgige neid samme.

        1. Valige **Loo/impordi**.
        2. Valige dialoogiboksis **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.
        3. Looge järgmisest tabelist salajane nimi ja väärtus.
        4. Valige **Luba** ja seejärel **Loo**. Saladus on loodud ja lisatud võtmehoidlasse.

        | Salajane nimi                       | Salajane väärtus                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | Varasemalt loodud rakenduse ID                                      |
        | app-secret                        | Kliendi saladus, mille varem salvestasite                                                    |
        | storage-account-name              | Varem loodud salvestamiskonto nimi, nt **storageaccount1**       |
        | storage-account-connection-string | Ühenduse string, mille kopeerisite lehelt **Juurdepääsuvõtmed** salvestuskonto jaoks |

5. Andke rakendusele juurdepääs võtmehoidlale.

    1. Avage [Azure’i portaalis](https://portal.azure.com) võtmehoidla, mille varem lõite.
    2. Valige juurdepääsu poliitika.
    3. Järgmise tabeli iga rakenduse puhul järgige neid samme.

        1. Valige juurdepääsupoliitika loomiseks **Lisa juudepääsupoliitika**.
        2. Väljal **Salajased load** valige õigused järgmisest tabelist.
        3. Väljal **Põhimõtte valimine** otsige järgmisest tabelist rakenduse kuvatav nimi.
        4. Valige käsk **Vali**.
        5. Valige **Lisa**.
        6. Valige käsk **Salvesta**.

        | Avaldus                                              | Õigused |
        |----------------------------------------------------------|-------------|
        | Teie loodud uue rakenduse kuvatav nimi | Hangi, loend   |
        | **Microsoft Dynamics ERP Microservices**                 | Hangi, loend   |

6. Määrake rollid salvestamiskontole juurdepääsuks.

    1. Avage [Azure’i portaalis](https://portal.azure.com) salvestamisekonto, mille varem lõite.
    2. Valige **Juurdepääsu juhtimine (iam)** ja seejärel valige **Rolli määramised**.
    3. Valige **Lisa, rolli määramise lisamine**.
    4. Järgmise tabeli iga rakenduse puhul järgige neid samme.

        1. Valige järgmisest tabelist roll.
        2. Jätke välja **Määra juurdepääs** väärtuseks **Azure AD kasutaja, grupp või teenusesubjekt**.
        3. Väljal **Valimine** sisestage järgmisest tabelist rakendused.
        4. Valige käsk **Salvesta**.

        | Avaldus                                              | Roll                        |
        |----------------------------------------------------------|-----------------------------|
        | Teie loodud uue rakenduse kuvatav nimi | Omanik                       |
        | Teie loodud uue rakenduse kuvatav nimi | Kaasautor                 |
        | Teie loodud uue rakenduse kuvatav nimi | Salvestamiskonto toetaja |
        | Teie loodud uue rakenduse kuvatav nimi | Salvestamise bloobimälu andmete omanik     |
        | **AI Builderi autoriseerimise teenus**                     | Salvestamise bloobimälu andmete lugeja    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---

## <a name="configure-the-entity-store"></a>Üksuse salvestamise konfigureerimine

Järgige neid samme, et seadistada üksuse salvestamine oma Finance’i keskkonnas.

1. Minge jaotisse **Süsteemihaldus \> Seadistus \> Süsteemi parameetrid \>Andmeühendused**.
2. Määrake suvandi **Luba Data Lake’i integratsioon** väärtuseks **Jah**.
3. Seadke järgmised võtmehoidja väljad.

    - **Rakenduse (klient) ID** – sisestage eelnevalt loodud rakenduse kliendi ID.
    - **Avalduse saladus** – sisestage saladus, mille salvestasite varem loodud rakenduse jaoks.
    - **DNS-i nimi** – domeeninime süsteemi (DNS) nime leiate varem loodud rakenduse üksikasjade lehelt.
    - **Salajane nimi** – sisestage **storage-account-connection-string**.

## <a name="configure-the-data-lake"></a>Andmejärve konfigureerimine

Järgige neid samme, et kasutada LCS-i Azure Data Lake’i lisandmooduli keskkonda lisamiseks.

1. Logige LCS–i sisse ja klõpsake seejärel lehe parempoolses servas oleva keskkonna nime all valikul **Kõik üksikasjad**.
2. Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
3. Valige lisandmoodul **Data Lake’i eksportimine**.
4. Sisestage järgmised väärtused.

    | Väärtus                                                              | Kirjeldus |
    |--------------------------------------------------------------------|-------------|
    | Azure’i tellimuse rentniku ID, kus asub võtmehoidla | Rentniku ID, kus asuvad salvestamiskonto, rakendused ja võtmehoidlad. Selle väärtuse leidmiseks avage [Azure’i portaal](https://portal.azure.com), avage **Azure Active Directory** ja kopeerige väärtus **Rentniku ID**. |
    | Sisestage oma võtmehoidla DNS-i nimi                             | Võtmehoidla DNS-i nimi, nt `https://customkeyvault.vault.azure.net/`. (See väärtus vastab üksuse salvestamisel kasutatavale DNS-i nimele.) |
    | Esitage saladus, mis sisaldab salvestuskonto nime   | **storage-account-name** |
    | Data Lake’i juurdepääsuks kasutatava rakenduse ID salajane nimi          | **app-id** |
    | Rakenduse ID-ga kasutatav salajane nimi                                 | **app-secret** |

5. Nõustuge tingimustega ja valige **Installi**.

Lisandmoodul installitakse mõne minuti jooksul.

## <a name="configure-ai-builder"></a>AI Builderi konfigureerimine

1. Logige LCS-i sisse ja avage leht **Keskkonna üksikasjad**.
2. Kerige alla jaotiseni **Keskkonna lisandmoodulid**. Peaksite nägema lisandmooduleid, mis on juba sellesse keskkonda installitud. Kui Lisandmoodulit **Data Lake’i eksportimine** nende seas ei ole, konfigureerige see lisandmoodul.
3. Valige lisandmoodul **Ülevaadete hankimine**.
4. Lisandmooduli **Ülevaadete hankimine** üksikasjade lehel sisestage järgmised väärtused.

    | Väärtus                                                    | Kirjeldus |
    |----------------------------------------------------------|-------------|
    | CDS-i organisatsiooni URL                                     | Dataverse’i organisatsiooni URL Dataverse’i eksemplari jaoks. Selle väärtuse leidmiseks avage [Power Appsi portaal](https://make.powerapps.com), valige ülemises parempoolses nurgas nupp **Sätted** (hammasratta sümbol), valige **Täpsemad sätted** ja kopeerige URL. (URL lõpeb liitega dynamics.com.) |
    | CDS-i organisatsiooni ID                                               | Dataverse’i eksemplari keskkonna ID. Selle väärtuse leidmiseks avage [Power Appsi portaal](https://make.powerapps.com), valige ülemises parempoolses nurgas nupp **Sätted** (hammasratta sümbol), valige **Kohandamised \> Arendaja ressursid \>Eksemplari viitamise teave** ja kopeerige väärtus **ID**. |
    | CDS-i rentniku ID (kataloogi ID AAD-st)               | Dataverse’i eksemplari rentniku ID. Selle väärtuse leidmiseks avage [Azure’i portaal](https://portal.azure.com), avage **Azure Active Directory** ja kopeerige väärtus **Rentniku ID**. |
    | Esitage kasutaja objekti ID, kellel on süsteemi administraatori roll | Azure AD kasutaja objekti ID teenuses Dataverse. See kasutaja peab olema Dataverse’i eksemplari süsteemiadministraator. Selle väärtuse leidmiseks avage [Azure’i portaal](https://portal.azure.com), avage **Azure Active Directory \> Kasutajad**, valige kasutaja ja seejärel kopeerige jaotises **Identiteet** väärtus **Objekti ID**. |
    | Kas see on rentniku vaikimisi CDS-i keskkond?      | Kui Dataverse’i eksemplar oli esimene loodud tootmiseksemplar, märkige see märkeruut. Kui Dataverse’i eksemplar on käsitsi loodud, tühjendage see märkeruut. |

## <a name="feedback-and-support"></a>Tagasiside ja tugi

Kui soovite anda tagasisidet või vajate tuge, saatke meil [kliendimaksete ülevaadetele (eelversioon)](mailto:fiap@microsoft.com).

## <a name="privacy-notice"></a>Privaatsusavaldus

Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]