---
title: Finance insights`i konfigureerimine avaliku eelvaate (eelvaate) jaoks - versioon 10.0.20 ja uuemad
description: See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada Finance insights`i saadaolevaid võimalusi versioonis 10.0.20 ja uuemates.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222608"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="d7a90-103">Finance insights\`i konfigureerimine avaliku eelvaate (eelvaate) jaoks - versioon 10.0.20 ja uuemad</span><span class="sxs-lookup"><span data-stu-id="d7a90-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d7a90-104">Finantsülevaated kombineerivad rakenduse Microsoft Dynamics 365 Finance funktsioonid teenustega Dataverse, Azure ja AI Builder, et pakkuda võimsaid prognoosimise tööriistu teie organisatsioonile.</span><span class="sxs-lookup"><span data-stu-id="d7a90-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="d7a90-105">See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada Finance insights\`i saadaolevaid võimalusi Dynamics 365 Finance versioonis 10.0.20 ja uuemates.</span><span class="sxs-lookup"><span data-stu-id="d7a90-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="d7a90-106">Selles teemas kirjeldatud konfiguratsiooni etapid kehtivad ainult finantsversiooni 10.0.20 ja uuemate versioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="d7a90-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="d7a90-107">Finance insights\`i seadistamiseks versioonil 10.0.19 ja uuemates versioonides vt [Finance insights vihjete konfigureerimine (eelvaade) – versioonid kuni 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="d7a90-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="d7a90-108">Finantside juurutamine</span><span class="sxs-lookup"><span data-stu-id="d7a90-108">Deploy Finance</span></span>

<span data-ttu-id="d7a90-109">Keskkonna juurutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d7a90-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="d7a90-110">Looge teenuses Microsoft Dynamics Lifecycle Services (LCS) või värskendage ’i keskkonda.</span><span class="sxs-lookup"><span data-stu-id="d7a90-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="d7a90-111">Keskkond vajab rakenduse versiooni 10.0.20 või hilisemat Finance and Operations rakendust.</span><span class="sxs-lookup"><span data-stu-id="d7a90-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="d7a90-112">Keskkond peab olema hea kättesaadavusega (HA) liivakasti keskkond.</span><span class="sxs-lookup"><span data-stu-id="d7a90-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="d7a90-113">(Seda tüüpi keskkond on tuntud ka kui järgu 2 keskkond.) Lisateavet vt teemast [Keskkonna kavandamine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="d7a90-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="d7a90-114">Finance insights\`i konfigureerimisel võib olla peate prognooside tööle kopeerimiseks tootmisandmed sellele keskkonnale kopeerima.</span><span class="sxs-lookup"><span data-stu-id="d7a90-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="d7a90-115">Ennustuse mudel kasutab prognooside koostamiseks mitmeid aastaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="d7a90-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="d7a90-116">Contoso demoandmed ei sisalda piisavalt ajaloolisi andmeid ennustuse mudeli liigenduste jaoks.</span><span class="sxs-lookup"><span data-stu-id="d7a90-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="d7a90-117">Dataverse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d7a90-117">Configure Dataverse</span></span>

<span data-ttu-id="d7a90-118">Kasutage järgmisi samme Finance Insights Dataverse konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d7a90-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="d7a90-119">Avage keskkonnaleht LCS-is ja kontrollige, et **Power Platform integreerimisjaotis** on juba seadistatud.</span><span class="sxs-lookup"><span data-stu-id="d7a90-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="d7a90-120">Kui see on juba seadistatud, tuleks loetleda Dataverse keskkonnaga Finance lingitud keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="d7a90-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="d7a90-121">Kui see ei ole seadistatud, järgige järgmiseid samme:</span><span class="sxs-lookup"><span data-stu-id="d7a90-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="d7a90-122">Valige **Power Platform\`i integratsioon** jaotises nupp **Seadistused**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="d7a90-123">Keskkonna seadistus võib võtta aega kuni tund.</span><span class="sxs-lookup"><span data-stu-id="d7a90-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="d7a90-124">Kui Dataverse keskkond on edukalt seadistatud, tuleb Dataverse keskkonna nimi linkida Finance keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="d7a90-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d7a90-125">Pärast keskkonna seadistuse lõpule viimist **ärge** valige rakenduste jaoks **Lingi rakendus CDS-iga**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="d7a90-126">See nupp pole Finance insights\`i jaoks vajalik.</span><span class="sxs-lookup"><span data-stu-id="d7a90-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="d7a90-127">Selle ruudu valimisel ei saa te konfigureerida LCS-i nõutavaid keskkonna lisandmooduleid.</span><span class="sxs-lookup"><span data-stu-id="d7a90-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="d7a90-128">Azure'i konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d7a90-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="d7a90-129">Kasutage Azure Coud Shelli, et seadistada finantsplevaadete andmejärve ressursid</span><span class="sxs-lookup"><span data-stu-id="d7a90-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="d7a90-130">Windows PowerShelli skripti kasutamine</span><span class="sxs-lookup"><span data-stu-id="d7a90-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="d7a90-131">Windows PowerShell skript on esitatud, seega saate hõlpsalt häälestada Azure’i ressursse, mida kirjeldatakse teemas [Azure Data Lake’i ekspordi konfigureerimine](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="d7a90-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="d7a90-132">Kui eelistate käsitsi häälestust, jätke see protseduur vahele ja jätkake selle asemel protseduuriga jaotises [Käsitsi häälestus](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="d7a90-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="d7a90-133">Kasutage järgmist protseduuri Windows PowerShell\`i skripti käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="d7a90-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="d7a90-134">Häälestus ei pruugi töötada, kui kasutate Azure CLI suvandit **Proovi seda** või kui käivitate skripti oma arvutis.</span><span class="sxs-lookup"><span data-stu-id="d7a90-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="d7a90-135">Järgige neid samme, et konfigureerida Azure Windows PowerShell skripti abil.</span><span class="sxs-lookup"><span data-stu-id="d7a90-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="d7a90-136">Teil peavad olema õigused Azure’i ressursigrupi, Azure’ii ressursside ja Azure AD rakenduse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="d7a90-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="d7a90-137">Lisateavet nõutavate õiguste kohta vt [Azure AD õiguste kontrollimine](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="d7a90-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="d7a90-138">Avage [Azure’i portaalis](https://portal.azure.com) oma sihtkoha Azure’i tellimus.</span><span class="sxs-lookup"><span data-stu-id="d7a90-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="d7a90-139">Valige nupp **Pilve Shell** välja **Otsing** paremalt.</span><span class="sxs-lookup"><span data-stu-id="d7a90-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="d7a90-140">Valige **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="d7a90-141">Looge salvestusruum, kui teil palutakse seda teha.</span><span class="sxs-lookup"><span data-stu-id="d7a90-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="d7a90-142">Minge vahekaardile **Azure CLI** ja valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="d7a90-143">Notepad\`is avage uus fail ja kleepige Windows PowerShell skripti.</span><span class="sxs-lookup"><span data-stu-id="d7a90-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="d7a90-144">Salvestage fail nimega **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="d7a90-145">Laadige Windows PowerShell skript seansile üles, kasutades rakenduses Cloud Shell üleslaadimise menüüsuvandit.</span><span class="sxs-lookup"><span data-stu-id="d7a90-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="d7a90-146">Käivitage skript **.\ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="d7a90-147">Järgige skripti käivitamiseks viipasid.</span><span class="sxs-lookup"><span data-stu-id="d7a90-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="d7a90-148">Kasutage skripti väljundi teavet, et installida LCS-i lisandmoodul Data Lake’i eksportimine.</span><span class="sxs-lookup"><span data-stu-id="d7a90-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="d7a90-149">Käsitsi häälestus</span><span class="sxs-lookup"><span data-stu-id="d7a90-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="d7a90-150">Lisage Azure AD rentnikule rakendused</span><span class="sxs-lookup"><span data-stu-id="d7a90-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="d7a90-151">Avage [Azure’i portaalis](https://portal.azure.com) suvand **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="d7a90-152">Valige käsk **Halda \> Ettevõtte rakendused**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="d7a90-153">Otsige rakenduse ID järgi järgmisi rakendusi.</span><span class="sxs-lookup"><span data-stu-id="d7a90-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="d7a90-154">Avaldus</span><span class="sxs-lookup"><span data-stu-id="d7a90-154">Application</span></span>                              | <span data-ttu-id="d7a90-155">Rakenduse kood</span><span class="sxs-lookup"><span data-stu-id="d7a90-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="d7a90-156">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="d7a90-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="d7a90-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="d7a90-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="d7a90-158">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="d7a90-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="d7a90-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="d7a90-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="d7a90-160">AI Builderi autoriseerimise teenus</span><span class="sxs-lookup"><span data-stu-id="d7a90-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="d7a90-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="d7a90-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="d7a90-162">Kui te ei leia ühtegi eelnevat rakendust, proovige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="d7a90-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="d7a90-163">Oma kohalikus arvutis valige menüü **Käivita** ja otsige suvandit **powershell**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="d7a90-164">Valige ja hoidke (või paremklõpsake) suvandit **Windows PowerShell** ja valige seejärel käsk **Käivita administraatorina**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="d7a90-165">Mooduli **AzureAD** installimiseks käivitage järgmine käsk.</span><span class="sxs-lookup"><span data-stu-id="d7a90-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="d7a90-166">Kui NuGeti pakkuja on kohustatud jätkama, valige selle installimiseks suvand **Y**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="d7a90-167">Kui ilmub teade „Ebausaldusväärne hoidla”, valige jätkamiseks **Y**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="d7a90-168">Iga rakenduse jaoks, mis tuleb lisada, käivitage järgmised käsud rakenduse lisamiseks Azure AD-sse.</span><span class="sxs-lookup"><span data-stu-id="d7a90-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="d7a90-169">Kui teilt küsitakse, logige sisse Azure AD administraatorina.</span><span class="sxs-lookup"><span data-stu-id="d7a90-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="d7a90-170">Azure'i ressursside loomine</span><span class="sxs-lookup"><span data-stu-id="d7a90-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="d7a90-171">Veenduge, et looksite Azure AD eksemplaris ja Dataverse keskkonnas samad ressursid.</span><span class="sxs-lookup"><span data-stu-id="d7a90-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="d7a90-172">Te ei saa kasutada ressursse erinevast Azure AD eksemplarist.</span><span class="sxs-lookup"><span data-stu-id="d7a90-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="d7a90-173">Looge salvestamise konto:</span><span class="sxs-lookup"><span data-stu-id="d7a90-173">Create a storage account:</span></span>

    1. <span data-ttu-id="d7a90-174">Looge [Azure’i portaalis](https://portal.azure.com) salvestamise konto.</span><span class="sxs-lookup"><span data-stu-id="d7a90-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="d7a90-175">Dialoogiboksis **Salvestamise konto loomine** määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="d7a90-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="d7a90-176">**Asukoht** – valige andmekeskuse, kus teie keskkond asub.</span><span class="sxs-lookup"><span data-stu-id="d7a90-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="d7a90-177">**Jõudlus** – soovitame valida suvandi **Standardne**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="d7a90-178">**Konto liik** – peate valima **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="d7a90-179">Dialoogiaknas **Täpsemad suvandid** valige suvandi **Data Lake storage Gen2** valik **Luba** jaotises **Hierarhilised nimeruumide**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="d7a90-180">Kui te selle funktsiooni keelate, ei saa te tarbida andmeid, mida Finance and Operations rakendused kirjutavad, kasutades selliseid teenuseid nagu Power BI andmevoog.</span><span class="sxs-lookup"><span data-stu-id="d7a90-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="d7a90-181">Valige **Läbivaatus ja loomine**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-181">Select **Review and create**.</span></span> <span data-ttu-id="d7a90-182">Kui juurutamine on lõpule viidud, kuvatakse Azure’i portaalis uus ressurss.</span><span class="sxs-lookup"><span data-stu-id="d7a90-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="d7a90-183">Avage loodud salvestusruumi konto.</span><span class="sxs-lookup"><span data-stu-id="d7a90-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="d7a90-184">Valige vasakpoolses menüüs **Juurdepääsuvõtmed**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="d7a90-185">Kopeerige ja salvestage salvestuskonto nimi.</span><span class="sxs-lookup"><span data-stu-id="d7a90-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="d7a90-186">Peate selle väärtuse hiljem sisestama, kui seadistate võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="d7a90-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="d7a90-187">Looge uus võtmehoidla:</span><span class="sxs-lookup"><span data-stu-id="d7a90-187">Create a key vault:</span></span>

    1. <span data-ttu-id="d7a90-188">Looge [Azure’i portaalis](https://portal.azure.com) võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="d7a90-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="d7a90-189">Valige dialoogiboksis **Võtmehoidla** väljal **Asukoht** andmekeskus, kus teie keskkond asub.</span><span class="sxs-lookup"><span data-stu-id="d7a90-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="d7a90-190">Pärast võtme hoidla loomist minge **võtme hoidla ülevaatesse** ja kopeerige ja salvestage DNS-i nimi.</span><span class="sxs-lookup"><span data-stu-id="d7a90-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="d7a90-191">Peate selle väärtuse hiljem sisestama, kui seadistate Data Lake lisandmooduli.</span><span class="sxs-lookup"><span data-stu-id="d7a90-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="d7a90-192">Looge ja registreerige Azure AD rakendus.</span><span class="sxs-lookup"><span data-stu-id="d7a90-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="d7a90-193">Avage [Azure’i portaalis](https://portal.azure.com) suvand **Azure Active Directory** ja valige **Rakenduse registreerimised**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="d7a90-194">Valige **Uus rakenduse registreerimine** ja määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="d7a90-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="d7a90-195">**Nimi** – sisestage rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="d7a90-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="d7a90-196">**Rakenduse tüüp** – valige **Web API**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="d7a90-197">**URI häälestuse ümbersuunamine** – sisestage oma Dynamics 365 eksemplari URL, nt `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="d7a90-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="d7a90-198">Avage äsja loodud rakendus ja kopeerige ja salvestage selle **rakenduse (kliendi) ID** väärtus.</span><span class="sxs-lookup"><span data-stu-id="d7a90-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="d7a90-199">Peate selle väärtuse hiljem sisestama, kui seadistate võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="d7a90-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="d7a90-200">Avage **API load** ja järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="d7a90-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="d7a90-201">Valige **Lisa luba**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="d7a90-202">Valige **Azure võtmehoidla**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="d7a90-203">Kui olete valinud delegeeritud õigused, valige **kasutaja\_isik**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="d7a90-204">Valige **Lisa load**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="d7a90-205">Valige rakenduse menüüs **Serdid \& saladused** ja seejärel järgige võtmehoidla saladuse loomiseks järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="d7a90-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="d7a90-206">Valige **Uus kliendi saladus**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="d7a90-207">Väljale **Võtme kirjeldus** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="d7a90-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="d7a90-208">Valige kestus ja valige seejärel **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="d7a90-209">Väljale **Väärtus** luuakse saladus.</span><span class="sxs-lookup"><span data-stu-id="d7a90-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="d7a90-210">Kopeerige ja salvestage kliendi salajane väärtus.</span><span class="sxs-lookup"><span data-stu-id="d7a90-210">Copy and save the client secret value.</span></span> <span data-ttu-id="d7a90-211">Peate selle väärtuse hiljem sisestama, kui seadistate võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="d7a90-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="d7a90-212">Võtmehoidla saladuste loomine.</span><span class="sxs-lookup"><span data-stu-id="d7a90-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="d7a90-213">Minge võtmehoidla, mille varem lõite, ja valige **Saladused**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="d7a90-214">Järgmise tabeli iga salajase nime puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="d7a90-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="d7a90-215">Valige **Loo/impordi**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="d7a90-216">Valige dialoogiboksis **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="d7a90-217">Looge järgmisest tabelist salajane nimi ja väärtus.</span><span class="sxs-lookup"><span data-stu-id="d7a90-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="d7a90-218">Valige **Luba** ja seejärel **Loo**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="d7a90-219">Saladus on loodud ja lisatud võtmehoidlasse.</span><span class="sxs-lookup"><span data-stu-id="d7a90-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="d7a90-220">Salajane nimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-220">Secret name</span></span>                       | <span data-ttu-id="d7a90-221">Salajane väärtus</span><span class="sxs-lookup"><span data-stu-id="d7a90-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="d7a90-222">app-id</span><span class="sxs-lookup"><span data-stu-id="d7a90-222">app-id</span></span>                            | <span data-ttu-id="d7a90-223">Varasemalt loodud rakenduse ID.</span><span class="sxs-lookup"><span data-stu-id="d7a90-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="d7a90-224">app-secret</span><span class="sxs-lookup"><span data-stu-id="d7a90-224">app-secret</span></span>                        | <span data-ttu-id="d7a90-225">Kliendi saladus, mille varem salvestasite.</span><span class="sxs-lookup"><span data-stu-id="d7a90-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="d7a90-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="d7a90-226">storage-account-name</span></span>              | <span data-ttu-id="d7a90-227">Varem loodud salvestamiskonto nimi, nt **salvestamiskonto1**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="d7a90-228">Andke rakendusele juurdepääs võtmehoidlale.</span><span class="sxs-lookup"><span data-stu-id="d7a90-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="d7a90-229">Avage [Azure’i portaalis](https://portal.azure.com) võtmehoidla, mille varem lõite.</span><span class="sxs-lookup"><span data-stu-id="d7a90-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="d7a90-230">Valige juurdepääsu poliitika.</span><span class="sxs-lookup"><span data-stu-id="d7a90-230">Select the access policies.</span></span>
    3. <span data-ttu-id="d7a90-231">Järgmise tabeli iga rakenduse puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="d7a90-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="d7a90-232">Valige juurdepääsupoliitika loomiseks **Lisa juudepääsupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="d7a90-233">Väljal **Salajased load** valige õigused järgmisest tabelist.</span><span class="sxs-lookup"><span data-stu-id="d7a90-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="d7a90-234">Väljal **Põhimõtte valimine** otsige järgmisest tabelist rakenduse kuvatav nimi.</span><span class="sxs-lookup"><span data-stu-id="d7a90-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="d7a90-235">Valige käsk **Vali**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-235">Select **Select**.</span></span>
        5. <span data-ttu-id="d7a90-236">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-236">Select **Add**.</span></span>
        6. <span data-ttu-id="d7a90-237">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-237">Select **Save**.</span></span>

        | <span data-ttu-id="d7a90-238">Avaldus</span><span class="sxs-lookup"><span data-stu-id="d7a90-238">Application</span></span>                                              | <span data-ttu-id="d7a90-239">Õigused</span><span class="sxs-lookup"><span data-stu-id="d7a90-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="d7a90-240">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-240">The display name of the new application that you created</span></span> | <span data-ttu-id="d7a90-241">Hangi, loend</span><span class="sxs-lookup"><span data-stu-id="d7a90-241">Get, List</span></span>   |
        | <span data-ttu-id="d7a90-242">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="d7a90-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="d7a90-243">Hangi, loend</span><span class="sxs-lookup"><span data-stu-id="d7a90-243">Get, List</span></span>   |

6. <span data-ttu-id="d7a90-244">Määrake rollid salvestamiskontole juurdepääsuks.</span><span class="sxs-lookup"><span data-stu-id="d7a90-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="d7a90-245">Avage [Azure’i portaalis](https://portal.azure.com) salvestamisekonto, mille varem lõite.</span><span class="sxs-lookup"><span data-stu-id="d7a90-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="d7a90-246">Valige **Juurdepääsu juhtimine (iam)** ja seejärel valige **Rolli määramised**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="d7a90-247">Valige **Lisa, rolli määramise lisamine**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="d7a90-248">Järgmise tabeli iga rakenduse puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="d7a90-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="d7a90-249">Valige tabelist roll.</span><span class="sxs-lookup"><span data-stu-id="d7a90-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="d7a90-250">Jätke välja **Määra juurdepääs** väärtuseks **Azure AD kasutaja, grupp või teenusesubjekt**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="d7a90-251">Väljal **Valimine** sisestage järgmisest tabelist rakendused.</span><span class="sxs-lookup"><span data-stu-id="d7a90-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="d7a90-252">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-252">Select **Save**.</span></span>

        | <span data-ttu-id="d7a90-253">Avaldus</span><span class="sxs-lookup"><span data-stu-id="d7a90-253">Application</span></span>                                              | <span data-ttu-id="d7a90-254">Roll</span><span class="sxs-lookup"><span data-stu-id="d7a90-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="d7a90-255">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-255">The display name of the new application that you created</span></span> | <span data-ttu-id="d7a90-256">Omanik</span><span class="sxs-lookup"><span data-stu-id="d7a90-256">Owner</span></span>                       |
        | <span data-ttu-id="d7a90-257">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-257">The display name of the new application that you created</span></span> | <span data-ttu-id="d7a90-258">Kaasautor</span><span class="sxs-lookup"><span data-stu-id="d7a90-258">Contributor</span></span>                 |
        | <span data-ttu-id="d7a90-259">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-259">The display name of the new application that you created</span></span> | <span data-ttu-id="d7a90-260">Salvestamiskonto toetaja</span><span class="sxs-lookup"><span data-stu-id="d7a90-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="d7a90-261">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-261">The display name of the new application that you created</span></span> | <span data-ttu-id="d7a90-262">Salvestamise bloobimälu andmete omanik</span><span class="sxs-lookup"><span data-stu-id="d7a90-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="d7a90-263">**AI Builderi autoriseerimise teenus**</span><span class="sxs-lookup"><span data-stu-id="d7a90-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="d7a90-264">Salvestamise bloobimälu andmete lugeja</span><span class="sxs-lookup"><span data-stu-id="d7a90-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="d7a90-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="d7a90-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="d7a90-266">Eksportimise konfigureerimine Azure Data Lake'i lisandmoodulis</span><span class="sxs-lookup"><span data-stu-id="d7a90-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="d7a90-267">Järgige neid samme, et kasutada LCS-i Azure Data Lake’i lisandmooduli keskkonda eksportimiseks.</span><span class="sxs-lookup"><span data-stu-id="d7a90-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="d7a90-268">Logige LCS–i sisse ja klõpsake seejärel lehe parempoolses servas oleva keskkonna nime all valikul **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="d7a90-269">Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="d7a90-270">Valige lisandmoodul **Data Lake’i eksportimine**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="d7a90-271">Sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d7a90-271">Enter the following values.</span></span>

    | <span data-ttu-id="d7a90-272">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d7a90-272">Value</span></span>                                                              | <span data-ttu-id="d7a90-273">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d7a90-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="d7a90-274">Azure’i tellimuse rentniku ID, kus asub võtmehoidla</span><span class="sxs-lookup"><span data-stu-id="d7a90-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="d7a90-275">Rentniku ID, kus asuvad salvestamiskonto, rakendused ja võtmehoidlad.</span><span class="sxs-lookup"><span data-stu-id="d7a90-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="d7a90-276">Selle väärtuse leidmiseks avage [Azure’i portaal](https://portal.azure.com), minge **Azure Active Directory** ja kopeerige väärtus **Rentniku ID**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="d7a90-277">Sisestage oma võtmehoidla DNS-i nimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="d7a90-278">Võtmehoidla DNS-i nimi, nt `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="d7a90-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="d7a90-279">Esitage saladus, mis sisaldab salvestuskonto nime</span><span class="sxs-lookup"><span data-stu-id="d7a90-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="d7a90-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="d7a90-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="d7a90-281">Data Lake’i juurdepääsuks kasutatava rakenduse ID salajane nimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="d7a90-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="d7a90-282">**app-id**</span></span> |
    | <span data-ttu-id="d7a90-283">Rakenduse kliendi saladuse salanimi</span><span class="sxs-lookup"><span data-stu-id="d7a90-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="d7a90-284">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="d7a90-284">**app-secret**</span></span> |

5. <span data-ttu-id="d7a90-285">Nõustuge tingimustega ja siis valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="d7a90-286">Lisandmoodul installitakse mõne minuti jooksul.</span><span class="sxs-lookup"><span data-stu-id="d7a90-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="d7a90-287">Finance insights lisandmooduli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d7a90-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="d7a90-288">Kui installisite eelnevalt lisandmooduli, desinstallige see enne järgmise protseduuri lõpule viimist.</span><span class="sxs-lookup"><span data-stu-id="d7a90-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="d7a90-289">Järgige neid samme Finance insights lisandmooduli installimiseks.</span><span class="sxs-lookup"><span data-stu-id="d7a90-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="d7a90-290">Logige LCS–i sisse ja klõpsake seejärel lehe parempoolses servas oleva keskkonna nime all valikul **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="d7a90-291">Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="d7a90-292">Valige **Finance insights** lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="d7a90-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="d7a90-293">Nõustuge tingimustega ja siis valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="d7a90-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="d7a90-294">Tagasiside ja tugi</span><span class="sxs-lookup"><span data-stu-id="d7a90-294">Feedback and support</span></span>

<span data-ttu-id="d7a90-295">Kui soovite anda tagasisidet või vajate tuge, saatke meil [Finance insights (eelversioon)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d7a90-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
