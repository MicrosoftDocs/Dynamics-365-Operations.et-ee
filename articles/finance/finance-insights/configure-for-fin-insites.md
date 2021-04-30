---
title: Finantsülevaadete konfigureerimine (eelversioon)
description: See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi.
author: ShivamPandey-msft
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 54117c009cfeb7307938cc6bd43e774ccfedcfb1
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908826"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="69ad8-103">Finantsülevaadete konfigureerimine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="69ad8-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="69ad8-104">Finantsülevaated kombineerivad rakenduse Microsoft Dynamics 365 Finance funktsioonid teenustega Microsoft Dataverse, Azure ja AI Builder, et pakkuda võimsaid prognoosimise tööriistu teie organisatsioonile.</span><span class="sxs-lookup"><span data-stu-id="69ad8-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="69ad8-105">See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="69ad8-106">Rakenduse  Dynamics 365 Finance juurutamine</span><span class="sxs-lookup"><span data-stu-id="69ad8-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="69ad8-107">Keskkonna juurutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="69ad8-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="69ad8-108">Looge teenuses Microsoft Dynamics Lifecycle Services (LCS) või värskendage Dynamics 365 Finance’i keskkonda.</span><span class="sxs-lookup"><span data-stu-id="69ad8-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="69ad8-109">Keskkond vajab rakenduse versiooni 10.0.11 / Platform värskendust 35 või uuemat.</span><span class="sxs-lookup"><span data-stu-id="69ad8-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="69ad8-110">Keskkond peab olema hea kättesaadavusega (HA) liivakasti keskkond.</span><span class="sxs-lookup"><span data-stu-id="69ad8-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="69ad8-111">(Seda tüüpi keskkond on tuntud ka kui järgu 2 keskkond.) Lisateavet vt teemast [Keskkonna kavandamine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="69ad8-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="69ad8-112">Kui kasutate Contoso demoandmeid, vajate Contoso makse prognoosimise kasutamiseks, rahavoo prognoosimiseks ja eelarve prognoosimise funktsioonideks täiendavaid näidisandmeid.</span><span class="sxs-lookup"><span data-stu-id="69ad8-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="69ad8-113">Dataverse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="69ad8-113">Configure Dataverse</span></span>

<span data-ttu-id="69ad8-114">Saate lõpetada järgmised konfigureerimise etapid käsitsi või saate kiirendada konfigureerimisprotsessi, kasutades esitatud Windows PowerShelli skripti.</span><span class="sxs-lookup"><span data-stu-id="69ad8-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="69ad8-115">Kui PowerShelli skript on töötamise lõpetanud, annab see teile väärtused, mida kasutada finantsülevaadete konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="69ad8-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="69ad8-116">Skripti käivitamiseks avage arvutis PowerShell.</span><span class="sxs-lookup"><span data-stu-id="69ad8-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="69ad8-117">Võite vajada PowerShelli versiooni 5.</span><span class="sxs-lookup"><span data-stu-id="69ad8-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="69ad8-118">Microsoft Azure CLI valik „Proovi seda” ei pruugi töötada.</span><span class="sxs-lookup"><span data-stu-id="69ad8-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="69ad8-119">Käsitsi konfigureerimise etapid</span><span class="sxs-lookup"><span data-stu-id="69ad8-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="69ad8-120">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com/) ja järgige neid samme, et luua uus Dataverse’i keskkond samas Active Directory rentnikus.</span><span class="sxs-lookup"><span data-stu-id="69ad8-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="69ad8-121">Avage leht **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="69ad8-122">[![Keskkondade leht](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="69ad8-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="69ad8-123">Valige **Uus keskkond**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="69ad8-124">Väljal **Tüüp** valige **Liivakast**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="69ad8-125">Määrake suvand **Andmebaas** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="69ad8-126">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-126">Select **Next**.</span></span>
    6. <span data-ttu-id="69ad8-127">Valige oma organisatsiooni keel ja valuuta.</span><span class="sxs-lookup"><span data-stu-id="69ad8-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="69ad8-128">Võtke vastu teiste väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="69ad8-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="69ad8-129">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-129">Select **Save**.</span></span>
    9. <span data-ttu-id="69ad8-130">Värskendage lehte **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="69ad8-131">Oodake, kuni välja **Olek** väärtus uuendatakse olekuks **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="69ad8-132">Märkige üles rakenduse Dataverse organsisatsiooni ID.</span><span class="sxs-lookup"><span data-stu-id="69ad8-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="69ad8-133">Valige uus keskkond ja seejärel valige suvand **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="69ad8-134">Valige **Ressursid \> Kõik pärandsätted**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="69ad8-135">Ülemisel navigeerimisribal valige **Sätted** ja valige seejärel **Kohandamised**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="69ad8-136">Valige **Arendaja ressursid**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="69ad8-137">Kopeerige väärtus **Dataverse organisatsiooni ID**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-137">Copy the **Dataverse organization ID** value.</span></span>
    17. <span data-ttu-id="69ad8-138">Märkige üles brauseri aadressiribal olev Dataverse’i organisatsiooni URL.</span><span class="sxs-lookup"><span data-stu-id="69ad8-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="69ad8-139">Näiteks URL võib olla `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="69ad8-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="69ad8-140">Kui kavatsete kasutada rahavoo prognoosimise või eelarve prognoosimise funktsiooni, toimige järgmiselt, et värskendada oma organisatsiooni marginaali limiiti vähemalt 50 megabaidini (MB).</span><span class="sxs-lookup"><span data-stu-id="69ad8-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="69ad8-141">Avage [Power Apps'i portaal](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="69ad8-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="69ad8-142">Valige vastloodud keskkond ja seejärel valige **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="69ad8-143">Valige **Sätted \>Meili konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="69ad8-144">Muute välja **Maksimaalne faili suurus** väärtuseks **51 200**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="69ad8-145">(Väärtus on väljendatud kilobaitides \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="69ad8-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="69ad8-146">Muudatuste salvestamiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="69ad8-147">Windows PowerShelli konfiguratsiooni skript</span><span class="sxs-lookup"><span data-stu-id="69ad8-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a><span data-ttu-id="69ad8-148">Azure'i häälestamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="69ad8-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="69ad8-149">Sisestage Dataverse’i kausta ID ja kasutaja Azure AD objekti ID</span><span class="sxs-lookup"><span data-stu-id="69ad8-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="69ad8-150">Sisestage Dataverse’i kausta ID.</span><span class="sxs-lookup"><span data-stu-id="69ad8-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="69ad8-151">Avage [Azure portaal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="69ad8-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="69ad8-152">Logige sisse, kasutades kasutaja ID-d, mida kasutati Dataverse’i keskkonna loomiseks.</span><span class="sxs-lookup"><span data-stu-id="69ad8-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="69ad8-153">Avage **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="69ad8-154">Kopeerige väärtus **Rentniku ID**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="69ad8-155">Sisestage kasutaja Azure Active Directory (Azure AD) objekti ID.</span><span class="sxs-lookup"><span data-stu-id="69ad8-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="69ad8-156">[Azure portaalis](https://portal.azure.com) avage suvand **Kasutajad** ja otsige kasutajat meiliaadressi järgi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="69ad8-157">Valige kasutajanimi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-157">Select the user's name.</span></span>
    3. <span data-ttu-id="69ad8-158">Kopeerige väärtus **Objekti ID**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="69ad8-159">Kasutage Azure Coud Shelli, et seadistada finantsplevaadete andmejärve ressursid</span><span class="sxs-lookup"><span data-stu-id="69ad8-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="69ad8-160">Windows PowerShelli skripti kasutamine</span><span class="sxs-lookup"><span data-stu-id="69ad8-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="69ad8-161">Windows PowerShelli skript on esitatud, seega saate hõlpsalt häälestada Azure’i ressursse, mida kirjeldatakse teemas [Azure Data Lake’i ekspordi konfigureerimine](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="69ad8-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="69ad8-162">Kui eelistate käsitsi häälestust, jätke see protseduur vahele ja jätkake protseduuriga jaotises [Käsitsi häälestus](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="69ad8-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="69ad8-163">PowerShelli skripti käitamiseks järgige allolevaid samme.</span><span class="sxs-lookup"><span data-stu-id="69ad8-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="69ad8-164">Azure CLI valik „Proovi seda” või arvutis skripti käitamine ei pruugi töötada.</span><span class="sxs-lookup"><span data-stu-id="69ad8-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="69ad8-165">Järgige neid samme, et konfigureerida Azure Windows PowerShelli skripti abil.</span><span class="sxs-lookup"><span data-stu-id="69ad8-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="69ad8-166">Teil peavad olema õigused Azure’i ressursigrupi, Azure’ii ressursside ja Azure AD rakenduse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="69ad8-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="69ad8-167">Lisateavet nõutavate õiguste kohta vt [Azure AD õiguste kontrollimine](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="69ad8-167">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="69ad8-168">Avage [Azure’i portaalis](https://portal.azure.com) oma sihtkoha Azure’i tellimus.</span><span class="sxs-lookup"><span data-stu-id="69ad8-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="69ad8-169">Valige nupp **Cloud Shell** väljast **Otsing** paremal.</span><span class="sxs-lookup"><span data-stu-id="69ad8-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="69ad8-170">Valige **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="69ad8-171">Looge salvestusruum, kui teil palutakse seda teha.</span><span class="sxs-lookup"><span data-stu-id="69ad8-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="69ad8-172">Seejärel laadige Windows PowerShelli skript seansile.</span><span class="sxs-lookup"><span data-stu-id="69ad8-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="69ad8-173">Käivitage skript.</span><span class="sxs-lookup"><span data-stu-id="69ad8-173">Run the script.</span></span>
5. <span data-ttu-id="69ad8-174">Järgige skripti käivitamiseks viipasid.</span><span class="sxs-lookup"><span data-stu-id="69ad8-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="69ad8-175">Kasutage skripti väljundi teavet, et installida LCS-i lisandmoodul **Data Lake’i eksportimine**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="69ad8-176">Kasutage skripti väljundi teavet, et lubada üksuse salvestusruum rakenduse Finance lehel **Andmeühendused** (**Süsteemi haldus \> Süsteemi parameetrid \> Andmeühendused**).</span><span class="sxs-lookup"><span data-stu-id="69ad8-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="69ad8-177">Käsitsi häälestus</span><span class="sxs-lookup"><span data-stu-id="69ad8-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="69ad8-178">Lisage Azure AD rentnikule rakendused</span><span class="sxs-lookup"><span data-stu-id="69ad8-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="69ad8-179">Avage [Azure’i portaalis](https://portal.azure.com) suvand **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="69ad8-180">Valige käsk **Halda \> Ettevõtte rakendused**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="69ad8-181">Otsige rakenduse ID järgi järgmisi rakendusi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="69ad8-182">Avaldus</span><span class="sxs-lookup"><span data-stu-id="69ad8-182">Application</span></span>                              | <span data-ttu-id="69ad8-183">Rakenduse kood</span><span class="sxs-lookup"><span data-stu-id="69ad8-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="69ad8-184">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="69ad8-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="69ad8-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="69ad8-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="69ad8-186">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="69ad8-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="69ad8-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="69ad8-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="69ad8-188">AI Builderi autoriseerimise teenus</span><span class="sxs-lookup"><span data-stu-id="69ad8-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="69ad8-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="69ad8-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="69ad8-190">Kui te ei leia ühtegi eelnevat rakendust, proovige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="69ad8-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="69ad8-191">Oma kohalikus arvutis valige menüü **Start** ja otsige suvandit **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="69ad8-192">Valige ja hoidke (või paremklõpsake) suvandit **Windows PowerShell** ja valige seejärel käsk **Käivita administraatorina**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="69ad8-193">Mooduli **AzureAD** installimiseks käivitage järgmine käsk.</span><span class="sxs-lookup"><span data-stu-id="69ad8-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="69ad8-194">Kui NuGeti pakkuja on kohustatud jätkama, valige selle installimiseks suvand **Y**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="69ad8-195">Kui ilmub teade „Ebausaldusväärne hoidla”, valige jätkamiseks **Y**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="69ad8-196">Iga rakenduse jaoks, mis tuleb lisada, käivitage järgmised käsud rakenduse lisamiseks Azure AD-sse.</span><span class="sxs-lookup"><span data-stu-id="69ad8-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="69ad8-197">Kui teilt küsitakse, logige sisse Azure AD administraatorina.</span><span class="sxs-lookup"><span data-stu-id="69ad8-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="69ad8-198">Azure'i ressursside loomine</span><span class="sxs-lookup"><span data-stu-id="69ad8-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="69ad8-199">Veenduge, et looksite Azure AD eksemplaris ja Dataverse’i keskkonnas samad ressursid.</span><span class="sxs-lookup"><span data-stu-id="69ad8-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="69ad8-200">Te ei saa kasutada ressursse erinevast Azure AD eksemplarist.</span><span class="sxs-lookup"><span data-stu-id="69ad8-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="69ad8-201">Looge uus salvestamise konto.</span><span class="sxs-lookup"><span data-stu-id="69ad8-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="69ad8-202">Looge [Azure’i portaalis](https://portal.azure.com) salvestamise konto.</span><span class="sxs-lookup"><span data-stu-id="69ad8-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="69ad8-203">Dialoogiboksis **Salvestamise konto loomine** määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="69ad8-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="69ad8-204">**Asukoht** – valige andmekeskuse, kus teie keskkond asub.</span><span class="sxs-lookup"><span data-stu-id="69ad8-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="69ad8-205">**Jõudlus** – soovitame valida suvandi **Standardne**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="69ad8-206">**Konto liik** – peate valima **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="69ad8-207">Dialoogiaknas **Täpsemad suvandid** valige suvandi **Data Lake storage Gen2** valik **Luba** jaotises **Hierarhilised nimeruumide**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="69ad8-208">Kui te selle funktsiooni keelate, ei saa te tarbida andmeid, mida Finance and Operationsi rakendused kirjutavad, kasutades selliseid teenuseid nagu Power BI andmevoog.</span><span class="sxs-lookup"><span data-stu-id="69ad8-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="69ad8-209">Valige **Läbivaatus ja loomine**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-209">Select **Review and create**.</span></span> <span data-ttu-id="69ad8-210">Kui juurutamine on lõpule viidud, kuvatakse Azure’i portaalis uus ressurss.</span><span class="sxs-lookup"><span data-stu-id="69ad8-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="69ad8-211">Avage loodud salvestusruumi konto.</span><span class="sxs-lookup"><span data-stu-id="69ad8-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="69ad8-212">Valige vasakpoolses menüüs **Juurdepääsuvõtmed**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="69ad8-213">Kopeerige ja salvestage ühenduse string kas **Võti1** või **Võti2** jaoks.</span><span class="sxs-lookup"><span data-stu-id="69ad8-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="69ad8-214">Kopeerige ja salvestage salvestuskonto nimi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="69ad8-215">Looge uus võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="69ad8-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="69ad8-216">Looge [Azure’i portaalis](https://portal.azure.com) võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="69ad8-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="69ad8-217">Valige dialoogiboksis **Võtmehoidla** väljal **Asukoht** andmekeskus, kus teie keskkond asub.</span><span class="sxs-lookup"><span data-stu-id="69ad8-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="69ad8-218">Kui võtmehoidla on loodud, valige see loendist ja seejärel valige suvand **Saladused**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="69ad8-219">Valige **Loo/impordi**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="69ad8-220">Valige dialoogiboksis **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="69ad8-221">Sisestage saladuse nimi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-221">Enter a name for the secret.</span></span> <span data-ttu-id="69ad8-222">Märkige üles nimi, sest peate selle hiljem esitama.</span><span class="sxs-lookup"><span data-stu-id="69ad8-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="69ad8-223">Sisestage väljale **Väärtus** ühenduse string, mille olete eelmise protseduuri savestamisekontolt saanud.</span><span class="sxs-lookup"><span data-stu-id="69ad8-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="69ad8-224">Valige **Luba** ja seejärel **Loo**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="69ad8-225">Saladus on loodud ja lisatud võtmehoidlasse.</span><span class="sxs-lookup"><span data-stu-id="69ad8-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="69ad8-226">Avage suvand **Võtmehoidla ülevaade** ja märkige üles DNS-i nimi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="69ad8-227">Looge ja registreerige Azure AD rakendus.</span><span class="sxs-lookup"><span data-stu-id="69ad8-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="69ad8-228">Avage [Azure’i portaalis](https://portal.azure.com) suvand **Azure Active Directory** ja valige **Rakenduse registreerimised**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="69ad8-229">Valige **Uus rakenduse registreerimine** ja määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="69ad8-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="69ad8-230">**Nimi** – sisestage rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="69ad8-231">**Rakenduse tüüp** – valige **Web API**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="69ad8-232">**URI häälestuse ümbersuunamine** – sisestage oma Dynamics 365 eksemplari URL, nt `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="69ad8-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="69ad8-233">Avage äsja loodud rakendus ja kopeerige ja salvestage selle **rakenduse (kliendi) ID** väärtus.</span><span class="sxs-lookup"><span data-stu-id="69ad8-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="69ad8-234">Peate selle väärtuse hiljem sisestama, kui seadistate võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="69ad8-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="69ad8-235">Avage **API load** ja järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="69ad8-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="69ad8-236">Valige **Lisa luba**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="69ad8-237">Valige **Azure võtmehoidla**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="69ad8-238">Kui olete valinud delegeeritud õigused, valige **kasutaja\_isik**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="69ad8-239">Valige **Lisa load**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="69ad8-240">Valige rakenduse menüüs **Serdid \& saladused** ja seejärel järgige võtmehoidla saladuse loomiseks järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="69ad8-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="69ad8-241">Valige **Uus kliendi saladus**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="69ad8-242">Väljale **Võtme kirjeldus** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="69ad8-243">Valige kestus ja valige seejärel **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="69ad8-244">Väljale **Väärtus** luuakse saladus.</span><span class="sxs-lookup"><span data-stu-id="69ad8-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="69ad8-245">Kopeerige ja salvestage salajane väärtus.</span><span class="sxs-lookup"><span data-stu-id="69ad8-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="69ad8-246">Võtmehoidla saladuste loomine.</span><span class="sxs-lookup"><span data-stu-id="69ad8-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="69ad8-247">Minge võtmehoidla, mille varem lõite, ja valige **Saladused**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="69ad8-248">Järgmise tabeli iga salajase nime puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="69ad8-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="69ad8-249">Valige **Loo/impordi**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="69ad8-250">Valige dialoogiboksis **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="69ad8-251">Looge järgmisest tabelist salajane nimi ja väärtus.</span><span class="sxs-lookup"><span data-stu-id="69ad8-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="69ad8-252">Valige **Luba** ja seejärel **Loo**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="69ad8-253">Saladus on loodud ja lisatud võtmehoidlasse.</span><span class="sxs-lookup"><span data-stu-id="69ad8-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="69ad8-254">Salajane nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-254">Secret name</span></span>                       | <span data-ttu-id="69ad8-255">Salajane väärtus</span><span class="sxs-lookup"><span data-stu-id="69ad8-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="69ad8-256">app-id</span><span class="sxs-lookup"><span data-stu-id="69ad8-256">app-id</span></span>                            | <span data-ttu-id="69ad8-257">Varasemalt loodud rakenduse ID</span><span class="sxs-lookup"><span data-stu-id="69ad8-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="69ad8-258">app-secret</span><span class="sxs-lookup"><span data-stu-id="69ad8-258">app-secret</span></span>                        | <span data-ttu-id="69ad8-259">Kliendi saladus, mille varem salvestasite</span><span class="sxs-lookup"><span data-stu-id="69ad8-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="69ad8-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="69ad8-260">storage-account-name</span></span>              | <span data-ttu-id="69ad8-261">Varem loodud salvestamiskonto nimi, nt **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="69ad8-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="69ad8-262">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="69ad8-262">storage-account-connection-string</span></span> | <span data-ttu-id="69ad8-263">Ühenduse string, mille kopeerisite lehelt **Juurdepääsuvõtmed** salvestuskonto jaoks</span><span class="sxs-lookup"><span data-stu-id="69ad8-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="69ad8-264">Andke rakendusele juurdepääs võtmehoidlale.</span><span class="sxs-lookup"><span data-stu-id="69ad8-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="69ad8-265">Avage [Azure’i portaalis](https://portal.azure.com) võtmehoidla, mille varem lõite.</span><span class="sxs-lookup"><span data-stu-id="69ad8-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="69ad8-266">Valige juurdepääsu poliitika.</span><span class="sxs-lookup"><span data-stu-id="69ad8-266">Select the access policies.</span></span>
    3. <span data-ttu-id="69ad8-267">Järgmise tabeli iga rakenduse puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="69ad8-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="69ad8-268">Valige juurdepääsupoliitika loomiseks **Lisa juudepääsupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="69ad8-269">Väljal **Salajased load** valige õigused järgmisest tabelist.</span><span class="sxs-lookup"><span data-stu-id="69ad8-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="69ad8-270">Väljal **Põhimõtte valimine** otsige järgmisest tabelist rakenduse kuvatav nimi.</span><span class="sxs-lookup"><span data-stu-id="69ad8-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="69ad8-271">Valige käsk **Vali**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-271">Select **Select**.</span></span>
        5. <span data-ttu-id="69ad8-272">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-272">Select **Add**.</span></span>
        6. <span data-ttu-id="69ad8-273">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-273">Select **Save**.</span></span>

        | <span data-ttu-id="69ad8-274">Avaldus</span><span class="sxs-lookup"><span data-stu-id="69ad8-274">Application</span></span>                                              | <span data-ttu-id="69ad8-275">Õigused</span><span class="sxs-lookup"><span data-stu-id="69ad8-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="69ad8-276">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-276">The display name of the new application that you created</span></span> | <span data-ttu-id="69ad8-277">Hangi, loend</span><span class="sxs-lookup"><span data-stu-id="69ad8-277">Get, List</span></span>   |
        | <span data-ttu-id="69ad8-278">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="69ad8-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="69ad8-279">Hangi, loend</span><span class="sxs-lookup"><span data-stu-id="69ad8-279">Get, List</span></span>   |

6. <span data-ttu-id="69ad8-280">Määrake rollid salvestamiskontole juurdepääsuks.</span><span class="sxs-lookup"><span data-stu-id="69ad8-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="69ad8-281">Avage [Azure’i portaalis](https://portal.azure.com) salvestamisekonto, mille varem lõite.</span><span class="sxs-lookup"><span data-stu-id="69ad8-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="69ad8-282">Valige **Juurdepääsu juhtimine (iam)** ja seejärel valige **Rolli määramised**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="69ad8-283">Valige **Lisa, rolli määramise lisamine**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="69ad8-284">Järgmise tabeli iga rakenduse puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="69ad8-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="69ad8-285">Valige järgmisest tabelist roll.</span><span class="sxs-lookup"><span data-stu-id="69ad8-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="69ad8-286">Jätke välja **Määra juurdepääs** väärtuseks **Azure AD kasutaja, grupp või teenusesubjekt**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="69ad8-287">Väljal **Valimine** sisestage järgmisest tabelist rakendused.</span><span class="sxs-lookup"><span data-stu-id="69ad8-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="69ad8-288">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-288">Select **Save**.</span></span>

        | <span data-ttu-id="69ad8-289">Avaldus</span><span class="sxs-lookup"><span data-stu-id="69ad8-289">Application</span></span>                                              | <span data-ttu-id="69ad8-290">Roll</span><span class="sxs-lookup"><span data-stu-id="69ad8-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="69ad8-291">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-291">The display name of the new application that you created</span></span> | <span data-ttu-id="69ad8-292">Omanik</span><span class="sxs-lookup"><span data-stu-id="69ad8-292">Owner</span></span>                       |
        | <span data-ttu-id="69ad8-293">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-293">The display name of the new application that you created</span></span> | <span data-ttu-id="69ad8-294">Kaasautor</span><span class="sxs-lookup"><span data-stu-id="69ad8-294">Contributor</span></span>                 |
        | <span data-ttu-id="69ad8-295">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-295">The display name of the new application that you created</span></span> | <span data-ttu-id="69ad8-296">Salvestamiskonto toetaja</span><span class="sxs-lookup"><span data-stu-id="69ad8-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="69ad8-297">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-297">The display name of the new application that you created</span></span> | <span data-ttu-id="69ad8-298">Salvestamise bloobimälu andmete omanik</span><span class="sxs-lookup"><span data-stu-id="69ad8-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="69ad8-299">**AI Builderi autoriseerimise teenus**</span><span class="sxs-lookup"><span data-stu-id="69ad8-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="69ad8-300">Salvestamise bloobimälu andmete lugeja</span><span class="sxs-lookup"><span data-stu-id="69ad8-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="69ad8-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="69ad8-301">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="69ad8-302">Andmejärve konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="69ad8-302">Configure the data lake</span></span>

<span data-ttu-id="69ad8-303">Järgige neid samme, et kasutada LCS-i Azure Data Lake’i lisandmooduli keskkonda lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="69ad8-303">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="69ad8-304">Logige LCS–i sisse ja klõpsake seejärel lehe parempoolses servas oleva keskkonna nime all valikul **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-304">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="69ad8-305">Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-305">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="69ad8-306">Valige lisandmoodul **Data Lake’i eksportimine**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-306">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="69ad8-307">Sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="69ad8-307">Enter the following values.</span></span>

    | <span data-ttu-id="69ad8-308">Väärtus</span><span class="sxs-lookup"><span data-stu-id="69ad8-308">Value</span></span>                                                              | <span data-ttu-id="69ad8-309">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="69ad8-309">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="69ad8-310">Azure’i tellimuse rentniku ID, kus asub võtmehoidla</span><span class="sxs-lookup"><span data-stu-id="69ad8-310">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="69ad8-311">Rentniku ID, kus asuvad salvestamiskonto, rakendused ja võtmehoidlad.</span><span class="sxs-lookup"><span data-stu-id="69ad8-311">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="69ad8-312">Selle väärtuse leidmiseks avage [Azure’i portaal](https://portal.azure.com), avage **Azure Active Directory** ja kopeerige väärtus **Rentniku ID**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-312">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="69ad8-313">Sisestage oma võtmehoidla DNS-i nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-313">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="69ad8-314">Võtmehoidla DNS-i nimi, nt `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="69ad8-314">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="69ad8-315">(See väärtus vastab üksuse salvestamisel kasutatavale DNS-i nimele.)</span><span class="sxs-lookup"><span data-stu-id="69ad8-315">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="69ad8-316">Esitage saladus, mis sisaldab salvestuskonto nime</span><span class="sxs-lookup"><span data-stu-id="69ad8-316">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="69ad8-317">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="69ad8-317">**storage-account-name**</span></span> |
    | <span data-ttu-id="69ad8-318">Data Lake’i juurdepääsuks kasutatava rakenduse ID salajane nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-318">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="69ad8-319">**app-id**</span><span class="sxs-lookup"><span data-stu-id="69ad8-319">**app-id**</span></span> |
    | <span data-ttu-id="69ad8-320">Rakenduse ID-ga kasutatav salajane nimi</span><span class="sxs-lookup"><span data-stu-id="69ad8-320">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="69ad8-321">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="69ad8-321">**app-secret**</span></span> |

5. <span data-ttu-id="69ad8-322">Nõustuge tingimustega ja valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-322">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="69ad8-323">Lisandmoodul installitakse mõne minuti jooksul.</span><span class="sxs-lookup"><span data-stu-id="69ad8-323">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="69ad8-324">AI Builderi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="69ad8-324">Configure AI Builder</span></span>

1. <span data-ttu-id="69ad8-325">Logige LCS-i sisse ja avage leht **Keskkonna üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-325">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="69ad8-326">Kerige alla jaotiseni **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-326">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="69ad8-327">Peaksite nägema lisandmooduleid, mis on juba sellesse keskkonda installitud.</span><span class="sxs-lookup"><span data-stu-id="69ad8-327">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="69ad8-328">Kui Lisandmoodulit **Data Lake’i eksportimine** nende seas ei ole, konfigureerige see lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="69ad8-328">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="69ad8-329">Valige lisandmoodul **Ülevaadete hankimine**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-329">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="69ad8-330">Lisandmooduli **Ülevaadete hankimine** üksikasjade lehel sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="69ad8-330">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="69ad8-331">Väärtus</span><span class="sxs-lookup"><span data-stu-id="69ad8-331">Value</span></span>                                                    | <span data-ttu-id="69ad8-332">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="69ad8-332">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="69ad8-333">CDS-i organisatsiooni URL</span><span class="sxs-lookup"><span data-stu-id="69ad8-333">CDS Organization URL</span></span>                                     | <span data-ttu-id="69ad8-334">Dataverse’i organisatsiooni URL Dataverse’i eksemplari jaoks.</span><span class="sxs-lookup"><span data-stu-id="69ad8-334">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="69ad8-335">Selle väärtuse leidmiseks avage [Power Appsi portaal](https://make.powerapps.com), valige ülemises parempoolses nurgas nupp **Sätted** (hammasratta sümbol), valige **Täpsemad sätted** ja kopeerige URL.</span><span class="sxs-lookup"><span data-stu-id="69ad8-335">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="69ad8-336">(URL lõpeb liitega dynamics.com.)</span><span class="sxs-lookup"><span data-stu-id="69ad8-336">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="69ad8-337">CDS-i organisatsiooni ID</span><span class="sxs-lookup"><span data-stu-id="69ad8-337">CDS Org ID</span></span>                                               | <span data-ttu-id="69ad8-338">Dataverse’i eksemplari keskkonna ID.</span><span class="sxs-lookup"><span data-stu-id="69ad8-338">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="69ad8-339">Selle väärtuse leidmiseks avage [Power Appsi portaal](https://make.powerapps.com), valige ülemises parempoolses nurgas nupp **Sätted** (hammasratta sümbol), valige **Kohandamised \> Arendaja ressursid \>Eksemplari viitamise teave** ja kopeerige väärtus **ID**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-339">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="69ad8-340">CDS-i rentniku ID (kataloogi ID AAD-st)</span><span class="sxs-lookup"><span data-stu-id="69ad8-340">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="69ad8-341">Dataverse’i eksemplari rentniku ID.</span><span class="sxs-lookup"><span data-stu-id="69ad8-341">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="69ad8-342">Selle väärtuse leidmiseks avage [Azure’i portaal](https://portal.azure.com), avage **Azure Active Directory** ja kopeerige väärtus **Rentniku ID**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-342">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="69ad8-343">Esitage kasutaja objekti ID, kellel on süsteemi administraatori roll</span><span class="sxs-lookup"><span data-stu-id="69ad8-343">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="69ad8-344">Azure AD kasutaja objekti ID teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="69ad8-344">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="69ad8-345">See kasutaja peab olema Dataverse’i eksemplari süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="69ad8-345">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="69ad8-346">Selle väärtuse leidmiseks avage [Azure’i portaal](https://portal.azure.com), avage **Azure Active Directory \> Kasutajad**, valige kasutaja ja seejärel kopeerige jaotises **Identiteet** väärtus **Objekti ID**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-346">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="69ad8-347">Kas see on rentniku vaikimisi CDS-i keskkond?</span><span class="sxs-lookup"><span data-stu-id="69ad8-347">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="69ad8-348">Kui Dataverse’i eksemplar oli esimene loodud tootmiseksemplar, märkige see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="69ad8-348">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="69ad8-349">Kui Dataverse’i eksemplar on käsitsi loodud, tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="69ad8-349">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="configure-the-entity-store"></a><span data-ttu-id="69ad8-350">Üksuse salvestamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="69ad8-350">Configure the entity store</span></span>

<span data-ttu-id="69ad8-351">Järgige neid samme, et seadistada üksuse salvestamine oma Finance’i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="69ad8-351">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="69ad8-352">Minge jaotisse **Süsteemihaldus \> Seadistus \> Süsteemi parameetrid \>Andmeühendused**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-352">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="69ad8-353">Määrake suvandi **Luba Data Lake’i integratsioon** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-353">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="69ad8-354">Seadke järgmised võtmehoidja väljad.</span><span class="sxs-lookup"><span data-stu-id="69ad8-354">Set the following key vault fields:</span></span>

    - <span data-ttu-id="69ad8-355">**Rakenduse (klient) ID** – sisestage eelnevalt loodud rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="69ad8-355">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="69ad8-356">**Avalduse saladus** – sisestage saladus, mille salvestasite varem loodud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="69ad8-356">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="69ad8-357">**DNS-i nimi** – domeeninime süsteemi (DNS) nime leiate varem loodud rakenduse üksikasjade lehelt.</span><span class="sxs-lookup"><span data-stu-id="69ad8-357">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="69ad8-358">**Salajane nimi** – sisestage **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="69ad8-358">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="69ad8-359">Tagasiside ja tugi</span><span class="sxs-lookup"><span data-stu-id="69ad8-359">Feedback and support</span></span>

<span data-ttu-id="69ad8-360">Kui soovite anda tagasisidet või vajate tuge, saatke meil [kliendimaksete ülevaadetele (eelversioon)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="69ad8-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="69ad8-361">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="69ad8-361">Privacy notice</span></span>

<span data-ttu-id="69ad8-362">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="69ad8-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
