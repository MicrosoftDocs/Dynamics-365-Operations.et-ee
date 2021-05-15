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
ms.openlocfilehash: 60e4d69157d7b73bd9e47310adae320687230080
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941222"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="b9251-103">Finantsülevaadete konfigureerimine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="b9251-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b9251-104">Finantsülevaated kombineerivad rakenduse Microsoft Dynamics 365 Finance funktsioonid teenustega Microsoft Dataverse, Azure ja AI Builder, et pakkuda võimsaid prognoosimise tööriistu teie organisatsioonile.</span><span class="sxs-lookup"><span data-stu-id="b9251-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="b9251-105">See teema selgitab konfiguratsiooni samme, mis võimaldavad teie süsteemil kasutada finantsülevaatuses saadaolevaid võimalusi.</span><span class="sxs-lookup"><span data-stu-id="b9251-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="b9251-106">Rakenduse  Dynamics 365 Finance juurutamine</span><span class="sxs-lookup"><span data-stu-id="b9251-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="b9251-107">Keskkonna juurutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b9251-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="b9251-108">Looge teenuses Microsoft Dynamics Lifecycle Services (LCS) või värskendage Dynamics 365 Finance’i keskkonda.</span><span class="sxs-lookup"><span data-stu-id="b9251-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="b9251-109">Keskkond vajab rakenduse versiooni 10.0.11 / Platform värskendust 35 või uuemat.</span><span class="sxs-lookup"><span data-stu-id="b9251-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="b9251-110">Keskkond peab olema hea kättesaadavusega (HA) liivakasti keskkond.</span><span class="sxs-lookup"><span data-stu-id="b9251-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="b9251-111">(Seda tüüpi keskkond on tuntud ka kui järgu 2 keskkond.) Lisateavet vt teemast [Keskkonna kavandamine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="b9251-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="b9251-112">Kui kasutate Contoso demoandmeid, vajate Contoso makse prognoosimise kasutamiseks, rahavoo prognoosimiseks ja eelarve prognoosimise funktsioonideks täiendavaid näidisandmeid.</span><span class="sxs-lookup"><span data-stu-id="b9251-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="b9251-113">Dataverse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b9251-113">Configure Dataverse</span></span>

<span data-ttu-id="b9251-114">Kasutage järgmisi samme Finance Insights'i Dataverse konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b9251-114">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="b9251-115">Avage keskkonnaleht LCS-is ja kontrollige, et **Power Platform integreerimisjaotis** on juba seadistatud.</span><span class="sxs-lookup"><span data-stu-id="b9251-115">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="b9251-116">Kui see on juba seadistatud, tuleks loetleda Dataverse keskkonnaga Dynamics 365 Finance lingitud keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-116">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="b9251-117">Kopeerige Dataverse keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-117">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="b9251-118">Kui see ei ole seadistatud, järgige järgmiseid samme.</span><span class="sxs-lookup"><span data-stu-id="b9251-118">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="b9251-119">Valige nupp **Seadistused** jaotises Power Platform Integratsioon.</span><span class="sxs-lookup"><span data-stu-id="b9251-119">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="b9251-120">Keskkonna häälestamine võib võtta kuni tunni.</span><span class="sxs-lookup"><span data-stu-id="b9251-120">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="b9251-121">Kui Dataverse keskkond on edukalt seadistatud, tuleb Dataverse keskkonna nimilinkida Dynamics 365 Finance keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="b9251-121">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="b9251-122">Kopeerige Dataverse keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-122">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="b9251-123">Pärast keskkonna häälestamise lõpetamist **ÄRGE** valige nuppu **Link CDS rakendustele**.</span><span class="sxs-lookup"><span data-stu-id="b9251-123">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="b9251-124">See ei ole rakenduse Finance Insights jaoks vajalik ja keelab nõutavate keskkonna lisandmoodulite lõpuleviimise LCS-is.</span><span class="sxs-lookup"><span data-stu-id="b9251-124">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="b9251-125">Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com/) ja järgige neid samme, et luua uus Dataverse’i keskkond samas Active Directory rentnikus.</span><span class="sxs-lookup"><span data-stu-id="b9251-125">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="b9251-126">Avage leht **Keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="b9251-126">Open the **Environments** page.</span></span>

        <span data-ttu-id="b9251-127">[![Keskkondade leht](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="b9251-127">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="b9251-128">Valige ülalpool loodud Dataverse keskkond ja seejärel valige **suvand Sätted**.</span><span class="sxs-lookup"><span data-stu-id="b9251-128">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="b9251-129">Valige **Ressursid \> Kõik pärandsätted**.</span><span class="sxs-lookup"><span data-stu-id="b9251-129">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="b9251-130">Ülemisel navigeerimisribal valige **Sätted** ja valige seejärel **Kohandamised**.</span><span class="sxs-lookup"><span data-stu-id="b9251-130">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="b9251-131">Valige **Arendaja ressursid**.</span><span class="sxs-lookup"><span data-stu-id="b9251-131">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="b9251-132">Kopeerige väärtus **Dataverse organisatsiooni ID**.</span><span class="sxs-lookup"><span data-stu-id="b9251-132">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="b9251-133">Märkige üles brauseri aadressiribal olev Dataverse’i organisatsiooni URL.</span><span class="sxs-lookup"><span data-stu-id="b9251-133">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="b9251-134">Näiteks URL võib olla `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="b9251-134">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="b9251-135">Kui kavatsete kasutada rahavoo prognoosimise või eelarve prognoosimise funktsiooni, toimige järgmiselt, et värskendada oma organisatsiooni marginaali limiiti vähemalt 50 megabaidini (MB).</span><span class="sxs-lookup"><span data-stu-id="b9251-135">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="b9251-136">Avage [Power Apps'i portaal](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="b9251-136">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="b9251-137">Valige vastloodud keskkond ja seejärel valige **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="b9251-137">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="b9251-138">Valige **Sätted \>Meili konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="b9251-138">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="b9251-139">Muute välja **Maksimaalne faili suurus** väärtuseks **51 200**.</span><span class="sxs-lookup"><span data-stu-id="b9251-139">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="b9251-140">(Väärtus on väljendatud kilobaitides \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="b9251-140">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="b9251-141">Muudatuste salvestamiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9251-141">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="b9251-142">Azure'i häälestamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b9251-142">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="b9251-143">Sisestage Dataverse’i kausta ID ja kasutaja Azure AD objekti ID</span><span class="sxs-lookup"><span data-stu-id="b9251-143">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="b9251-144">Sisestage Dataverse’i kausta ID.</span><span class="sxs-lookup"><span data-stu-id="b9251-144">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="b9251-145">Avage [Azure portaal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="b9251-145">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="b9251-146">Logige sisse, kasutades kasutaja ID-d, mida kasutati Dataverse’i keskkonna loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b9251-146">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="b9251-147">Avage **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="b9251-147">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="b9251-148">Kopeerige väärtus **Rentniku ID**.</span><span class="sxs-lookup"><span data-stu-id="b9251-148">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="b9251-149">Sisestage kasutaja Azure Active Directory (Azure AD) objekti ID.</span><span class="sxs-lookup"><span data-stu-id="b9251-149">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="b9251-150">[Azure portaalis](https://portal.azure.com) avage suvand **Kasutajad** ja otsige kasutajat meiliaadressi järgi.</span><span class="sxs-lookup"><span data-stu-id="b9251-150">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="b9251-151">Valige kasutajanimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-151">Select the user's name.</span></span>
    3. <span data-ttu-id="b9251-152">Kopeerige väärtus **Objekti ID**.</span><span class="sxs-lookup"><span data-stu-id="b9251-152">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="b9251-153">Kasutage Azure Coud Shelli, et seadistada finantsplevaadete andmejärve ressursid</span><span class="sxs-lookup"><span data-stu-id="b9251-153">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="b9251-154">Windows PowerShelli skripti kasutamine</span><span class="sxs-lookup"><span data-stu-id="b9251-154">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="b9251-155">Windows PowerShelli skript on esitatud, seega saate hõlpsalt häälestada Azure’i ressursse, mida kirjeldatakse teemas [Azure Data Lake’i ekspordi konfigureerimine](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="b9251-155">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="b9251-156">Kui eelistate käsitsi häälestust, jätke see protseduur vahele ja jätkake protseduuriga jaotises [Käsitsi häälestus](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="b9251-156">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="b9251-157">PowerShelli skripti käitamiseks järgige allolevaid samme.</span><span class="sxs-lookup"><span data-stu-id="b9251-157">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="b9251-158">Azure CLI valik „Proovi seda” või arvutis skripti käitamine ei pruugi töötada.</span><span class="sxs-lookup"><span data-stu-id="b9251-158">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="b9251-159">Järgige neid samme, et konfigureerida Azure Windows PowerShelli skripti abil.</span><span class="sxs-lookup"><span data-stu-id="b9251-159">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="b9251-160">Teil peavad olema õigused Azure’i ressursigrupi, Azure’ii ressursside ja Azure AD rakenduse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b9251-160">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="b9251-161">Lisateavet nõutavate õiguste kohta vt [Azure AD õiguste kontrollimine](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="b9251-161">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="b9251-162">Avage [Azure’i portaalis](https://portal.azure.com) oma sihtkoha Azure’i tellimus.</span><span class="sxs-lookup"><span data-stu-id="b9251-162">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="b9251-163">Valige nupp **Cloud Shell** väljast **Otsing** paremal.</span><span class="sxs-lookup"><span data-stu-id="b9251-163">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="b9251-164">Valige **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="b9251-164">Select **PowerShell**.</span></span>
3. <span data-ttu-id="b9251-165">Looge salvestusruum, kui teil palutakse seda teha.</span><span class="sxs-lookup"><span data-stu-id="b9251-165">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="b9251-166">Minge vahekaardile **Azure CLI** ja valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="b9251-166">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="b9251-167">Avage Notepad ja kleepige PowerShelli skript sellesse.</span><span class="sxs-lookup"><span data-stu-id="b9251-167">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="b9251-168">Salvestage fail nimega ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="b9251-168">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="b9251-169">Laadige Windows PowerShelli skript seansile üles, kasutades rakenduses Cloud Shell üleslaadimise menüüsuvandit.</span><span class="sxs-lookup"><span data-stu-id="b9251-169">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="b9251-170">Käivitage skript .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="b9251-170">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="b9251-171">Järgige skripti käivitamiseks viipasid.</span><span class="sxs-lookup"><span data-stu-id="b9251-171">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="b9251-172">Kasutage skripti väljundi teavet, et installida LCS-i lisandmoodul **Data Lake’i eksportimine**.</span><span class="sxs-lookup"><span data-stu-id="b9251-172">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="b9251-173">Kasutage skripti väljundi teavet, et lubada üksuse salvestusruum rakenduse Finance lehel **Andmeühendused** (**Süsteemi haldus \> Süsteemi parameetrid \> Andmeühendused**).</span><span class="sxs-lookup"><span data-stu-id="b9251-173">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="b9251-174">Käsitsi häälestus</span><span class="sxs-lookup"><span data-stu-id="b9251-174">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="b9251-175">Lisage Azure AD rentnikule rakendused</span><span class="sxs-lookup"><span data-stu-id="b9251-175">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="b9251-176">Avage [Azure’i portaalis](https://portal.azure.com) suvand **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="b9251-176">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="b9251-177">Valige käsk **Halda \> Ettevõtte rakendused**.</span><span class="sxs-lookup"><span data-stu-id="b9251-177">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="b9251-178">Otsige rakenduse ID järgi järgmisi rakendusi.</span><span class="sxs-lookup"><span data-stu-id="b9251-178">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="b9251-179">Avaldus</span><span class="sxs-lookup"><span data-stu-id="b9251-179">Application</span></span>                              | <span data-ttu-id="b9251-180">Rakenduse kood</span><span class="sxs-lookup"><span data-stu-id="b9251-180">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="b9251-181">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="b9251-181">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="b9251-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="b9251-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="b9251-183">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="b9251-183">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="b9251-184">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="b9251-184">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="b9251-185">AI Builderi autoriseerimise teenus</span><span class="sxs-lookup"><span data-stu-id="b9251-185">AI Builder Authorization Service</span></span>         | <span data-ttu-id="b9251-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="b9251-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="b9251-187">Kui te ei leia ühtegi eelnevat rakendust, proovige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="b9251-187">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="b9251-188">Oma kohalikus arvutis valige menüü **Start** ja otsige suvandit **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="b9251-188">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="b9251-189">Valige ja hoidke (või paremklõpsake) suvandit **Windows PowerShell** ja valige seejärel käsk **Käivita administraatorina**.</span><span class="sxs-lookup"><span data-stu-id="b9251-189">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="b9251-190">Mooduli **AzureAD** installimiseks käivitage järgmine käsk.</span><span class="sxs-lookup"><span data-stu-id="b9251-190">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="b9251-191">Kui NuGeti pakkuja on kohustatud jätkama, valige selle installimiseks suvand **Y**.</span><span class="sxs-lookup"><span data-stu-id="b9251-191">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="b9251-192">Kui ilmub teade „Ebausaldusväärne hoidla”, valige jätkamiseks **Y**.</span><span class="sxs-lookup"><span data-stu-id="b9251-192">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="b9251-193">Iga rakenduse jaoks, mis tuleb lisada, käivitage järgmised käsud rakenduse lisamiseks Azure AD-sse.</span><span class="sxs-lookup"><span data-stu-id="b9251-193">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="b9251-194">Kui teilt küsitakse, logige sisse Azure AD administraatorina.</span><span class="sxs-lookup"><span data-stu-id="b9251-194">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="b9251-195">Azure'i ressursside loomine</span><span class="sxs-lookup"><span data-stu-id="b9251-195">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="b9251-196">Veenduge, et looksite Azure AD eksemplaris ja Dataverse’i keskkonnas samad ressursid.</span><span class="sxs-lookup"><span data-stu-id="b9251-196">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="b9251-197">Te ei saa kasutada ressursse erinevast Azure AD eksemplarist.</span><span class="sxs-lookup"><span data-stu-id="b9251-197">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="b9251-198">Looge uus salvestamise konto.</span><span class="sxs-lookup"><span data-stu-id="b9251-198">Create a new storage account:</span></span>

    1. <span data-ttu-id="b9251-199">Looge [Azure’i portaalis](https://portal.azure.com) salvestamise konto.</span><span class="sxs-lookup"><span data-stu-id="b9251-199">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="b9251-200">Dialoogiboksis **Salvestamise konto loomine** määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="b9251-200">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="b9251-201">**Asukoht** – valige andmekeskuse, kus teie keskkond asub.</span><span class="sxs-lookup"><span data-stu-id="b9251-201">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="b9251-202">**Jõudlus** – soovitame valida suvandi **Standardne**.</span><span class="sxs-lookup"><span data-stu-id="b9251-202">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="b9251-203">**Konto liik** – peate valima **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="b9251-203">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="b9251-204">Dialoogiaknas **Täpsemad suvandid** valige suvandi **Data Lake storage Gen2** valik **Luba** jaotises **Hierarhilised nimeruumide**.</span><span class="sxs-lookup"><span data-stu-id="b9251-204">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="b9251-205">Kui te selle funktsiooni keelate, ei saa te tarbida andmeid, mida Finance and Operationsi rakendused kirjutavad, kasutades selliseid teenuseid nagu Power BI andmevoog.</span><span class="sxs-lookup"><span data-stu-id="b9251-205">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="b9251-206">Valige **Läbivaatus ja loomine**.</span><span class="sxs-lookup"><span data-stu-id="b9251-206">Select **Review and create**.</span></span> <span data-ttu-id="b9251-207">Kui juurutamine on lõpule viidud, kuvatakse Azure’i portaalis uus ressurss.</span><span class="sxs-lookup"><span data-stu-id="b9251-207">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="b9251-208">Avage loodud salvestusruumi konto.</span><span class="sxs-lookup"><span data-stu-id="b9251-208">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="b9251-209">Valige vasakpoolses menüüs **Juurdepääsuvõtmed**.</span><span class="sxs-lookup"><span data-stu-id="b9251-209">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="b9251-210">Kopeerige ja salvestage ühenduse string kas **Võti1** või **Võti2** jaoks.</span><span class="sxs-lookup"><span data-stu-id="b9251-210">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="b9251-211">Kopeerige ja salvestage salvestuskonto nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-211">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="b9251-212">Looge uus võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="b9251-212">Create a new key vault:</span></span>

    1. <span data-ttu-id="b9251-213">Looge [Azure’i portaalis](https://portal.azure.com) võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="b9251-213">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="b9251-214">Valige dialoogiboksis **Võtmehoidla** väljal **Asukoht** andmekeskus, kus teie keskkond asub.</span><span class="sxs-lookup"><span data-stu-id="b9251-214">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="b9251-215">Kui võtmehoidla on loodud, valige see loendist ja seejärel valige suvand **Saladused**.</span><span class="sxs-lookup"><span data-stu-id="b9251-215">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="b9251-216">Valige **Loo/impordi**.</span><span class="sxs-lookup"><span data-stu-id="b9251-216">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="b9251-217">Valige dialoogiboksis **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="b9251-217">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="b9251-218">Sisestage saladuse nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-218">Enter a name for the secret.</span></span> <span data-ttu-id="b9251-219">Märkige üles nimi, sest peate selle hiljem esitama.</span><span class="sxs-lookup"><span data-stu-id="b9251-219">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="b9251-220">Sisestage väljale **Väärtus** ühenduse string, mille olete eelmise protseduuri savestamisekontolt saanud.</span><span class="sxs-lookup"><span data-stu-id="b9251-220">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="b9251-221">Valige **Luba** ja seejärel **Loo**.</span><span class="sxs-lookup"><span data-stu-id="b9251-221">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="b9251-222">Saladus on loodud ja lisatud võtmehoidlasse.</span><span class="sxs-lookup"><span data-stu-id="b9251-222">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="b9251-223">Avage suvand **Võtmehoidla ülevaade** ja märkige üles DNS-i nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-223">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="b9251-224">Looge ja registreerige Azure AD rakendus.</span><span class="sxs-lookup"><span data-stu-id="b9251-224">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="b9251-225">Avage [Azure’i portaalis](https://portal.azure.com) suvand **Azure Active Directory** ja valige **Rakenduse registreerimised**.</span><span class="sxs-lookup"><span data-stu-id="b9251-225">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="b9251-226">Valige **Uus rakenduse registreerimine** ja määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="b9251-226">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="b9251-227">**Nimi** – sisestage rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-227">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="b9251-228">**Rakenduse tüüp** – valige **Web API**.</span><span class="sxs-lookup"><span data-stu-id="b9251-228">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="b9251-229">**URI häälestuse ümbersuunamine** – sisestage oma Dynamics 365 eksemplari URL, nt `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="b9251-229">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="b9251-230">Avage äsja loodud rakendus ja kopeerige ja salvestage selle **rakenduse (kliendi) ID** väärtus.</span><span class="sxs-lookup"><span data-stu-id="b9251-230">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="b9251-231">Peate selle väärtuse hiljem sisestama, kui seadistate võtmehoidla.</span><span class="sxs-lookup"><span data-stu-id="b9251-231">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="b9251-232">Avage **API load** ja järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="b9251-232">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="b9251-233">Valige **Lisa luba**.</span><span class="sxs-lookup"><span data-stu-id="b9251-233">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="b9251-234">Valige **Azure võtmehoidla**.</span><span class="sxs-lookup"><span data-stu-id="b9251-234">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="b9251-235">Kui olete valinud delegeeritud õigused, valige **kasutaja\_isik**.</span><span class="sxs-lookup"><span data-stu-id="b9251-235">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="b9251-236">Valige **Lisa load**.</span><span class="sxs-lookup"><span data-stu-id="b9251-236">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="b9251-237">Valige rakenduse menüüs **Serdid \& saladused** ja seejärel järgige võtmehoidla saladuse loomiseks järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="b9251-237">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="b9251-238">Valige **Uus kliendi saladus**.</span><span class="sxs-lookup"><span data-stu-id="b9251-238">Select **New client secret**.</span></span>
        2. <span data-ttu-id="b9251-239">Väljale **Võtme kirjeldus** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-239">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="b9251-240">Valige kestus ja valige seejärel **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="b9251-240">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="b9251-241">Väljale **Väärtus** luuakse saladus.</span><span class="sxs-lookup"><span data-stu-id="b9251-241">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="b9251-242">Kopeerige ja salvestage salajane väärtus.</span><span class="sxs-lookup"><span data-stu-id="b9251-242">Copy and save the secret value.</span></span>

4. <span data-ttu-id="b9251-243">Võtmehoidla saladuste loomine.</span><span class="sxs-lookup"><span data-stu-id="b9251-243">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="b9251-244">Minge võtmehoidla, mille varem lõite, ja valige **Saladused**.</span><span class="sxs-lookup"><span data-stu-id="b9251-244">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="b9251-245">Järgmise tabeli iga salajase nime puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="b9251-245">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b9251-246">Valige **Loo/impordi**.</span><span class="sxs-lookup"><span data-stu-id="b9251-246">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="b9251-247">Valige dialoogiboksis **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="b9251-247">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="b9251-248">Looge järgmisest tabelist salajane nimi ja väärtus.</span><span class="sxs-lookup"><span data-stu-id="b9251-248">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="b9251-249">Valige **Luba** ja seejärel **Loo**.</span><span class="sxs-lookup"><span data-stu-id="b9251-249">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="b9251-250">Saladus on loodud ja lisatud võtmehoidlasse.</span><span class="sxs-lookup"><span data-stu-id="b9251-250">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="b9251-251">Salajane nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-251">Secret name</span></span>                       | <span data-ttu-id="b9251-252">Salajane väärtus</span><span class="sxs-lookup"><span data-stu-id="b9251-252">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="b9251-253">app-id</span><span class="sxs-lookup"><span data-stu-id="b9251-253">app-id</span></span>                            | <span data-ttu-id="b9251-254">Varasemalt loodud rakenduse ID</span><span class="sxs-lookup"><span data-stu-id="b9251-254">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="b9251-255">app-secret</span><span class="sxs-lookup"><span data-stu-id="b9251-255">app-secret</span></span>                        | <span data-ttu-id="b9251-256">Kliendi saladus, mille varem salvestasite</span><span class="sxs-lookup"><span data-stu-id="b9251-256">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="b9251-257">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="b9251-257">storage-account-name</span></span>              | <span data-ttu-id="b9251-258">Varem loodud salvestamiskonto nimi, nt **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="b9251-258">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="b9251-259">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="b9251-259">storage-account-connection-string</span></span> | <span data-ttu-id="b9251-260">Ühenduse string, mille kopeerisite lehelt **Juurdepääsuvõtmed** salvestuskonto jaoks</span><span class="sxs-lookup"><span data-stu-id="b9251-260">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="b9251-261">Andke rakendusele juurdepääs võtmehoidlale.</span><span class="sxs-lookup"><span data-stu-id="b9251-261">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="b9251-262">Avage [Azure’i portaalis](https://portal.azure.com) võtmehoidla, mille varem lõite.</span><span class="sxs-lookup"><span data-stu-id="b9251-262">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="b9251-263">Valige juurdepääsu poliitika.</span><span class="sxs-lookup"><span data-stu-id="b9251-263">Select the access policies.</span></span>
    3. <span data-ttu-id="b9251-264">Järgmise tabeli iga rakenduse puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="b9251-264">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b9251-265">Valige juurdepääsupoliitika loomiseks **Lisa juudepääsupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="b9251-265">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="b9251-266">Väljal **Salajased load** valige õigused järgmisest tabelist.</span><span class="sxs-lookup"><span data-stu-id="b9251-266">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="b9251-267">Väljal **Põhimõtte valimine** otsige järgmisest tabelist rakenduse kuvatav nimi.</span><span class="sxs-lookup"><span data-stu-id="b9251-267">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="b9251-268">Valige käsk **Vali**.</span><span class="sxs-lookup"><span data-stu-id="b9251-268">Select **Select**.</span></span>
        5. <span data-ttu-id="b9251-269">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="b9251-269">Select **Add**.</span></span>
        6. <span data-ttu-id="b9251-270">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b9251-270">Select **Save**.</span></span>

        | <span data-ttu-id="b9251-271">Avaldus</span><span class="sxs-lookup"><span data-stu-id="b9251-271">Application</span></span>                                              | <span data-ttu-id="b9251-272">Õigused</span><span class="sxs-lookup"><span data-stu-id="b9251-272">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="b9251-273">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-273">The display name of the new application that you created</span></span> | <span data-ttu-id="b9251-274">Hangi, loend</span><span class="sxs-lookup"><span data-stu-id="b9251-274">Get, List</span></span>   |
        | <span data-ttu-id="b9251-275">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="b9251-275">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="b9251-276">Hangi, loend</span><span class="sxs-lookup"><span data-stu-id="b9251-276">Get, List</span></span>   |

6. <span data-ttu-id="b9251-277">Määrake rollid salvestamiskontole juurdepääsuks.</span><span class="sxs-lookup"><span data-stu-id="b9251-277">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="b9251-278">Avage [Azure’i portaalis](https://portal.azure.com) salvestamisekonto, mille varem lõite.</span><span class="sxs-lookup"><span data-stu-id="b9251-278">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="b9251-279">Valige **Juurdepääsu juhtimine (iam)** ja seejärel valige **Rolli määramised**.</span><span class="sxs-lookup"><span data-stu-id="b9251-279">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="b9251-280">Valige **Lisa, rolli määramise lisamine**.</span><span class="sxs-lookup"><span data-stu-id="b9251-280">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="b9251-281">Järgmise tabeli iga rakenduse puhul järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="b9251-281">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b9251-282">Valige järgmisest tabelist roll.</span><span class="sxs-lookup"><span data-stu-id="b9251-282">Select the role from the following table.</span></span>
        2. <span data-ttu-id="b9251-283">Jätke välja **Määra juurdepääs** väärtuseks **Azure AD kasutaja, grupp või teenusesubjekt**.</span><span class="sxs-lookup"><span data-stu-id="b9251-283">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="b9251-284">Väljal **Valimine** sisestage järgmisest tabelist rakendused.</span><span class="sxs-lookup"><span data-stu-id="b9251-284">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="b9251-285">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b9251-285">Select **Save**.</span></span>

        | <span data-ttu-id="b9251-286">Avaldus</span><span class="sxs-lookup"><span data-stu-id="b9251-286">Application</span></span>                                              | <span data-ttu-id="b9251-287">Roll</span><span class="sxs-lookup"><span data-stu-id="b9251-287">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="b9251-288">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-288">The display name of the new application that you created</span></span> | <span data-ttu-id="b9251-289">Omanik</span><span class="sxs-lookup"><span data-stu-id="b9251-289">Owner</span></span>                       |
        | <span data-ttu-id="b9251-290">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-290">The display name of the new application that you created</span></span> | <span data-ttu-id="b9251-291">Kaasautor</span><span class="sxs-lookup"><span data-stu-id="b9251-291">Contributor</span></span>                 |
        | <span data-ttu-id="b9251-292">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-292">The display name of the new application that you created</span></span> | <span data-ttu-id="b9251-293">Salvestamiskonto toetaja</span><span class="sxs-lookup"><span data-stu-id="b9251-293">Storage Account Contributor</span></span> |
        | <span data-ttu-id="b9251-294">Teie loodud uue rakenduse kuvatav nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-294">The display name of the new application that you created</span></span> | <span data-ttu-id="b9251-295">Salvestamise bloobimälu andmete omanik</span><span class="sxs-lookup"><span data-stu-id="b9251-295">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="b9251-296">**AI Builderi autoriseerimise teenus**</span><span class="sxs-lookup"><span data-stu-id="b9251-296">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="b9251-297">Salvestamise bloobimälu andmete lugeja</span><span class="sxs-lookup"><span data-stu-id="b9251-297">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="b9251-298">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="b9251-298">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="b9251-299">Andmejärve konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b9251-299">Configure the data lake</span></span>

<span data-ttu-id="b9251-300">Järgige neid samme, et kasutada LCS-i Azure Data Lake’i lisandmooduli keskkonda lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="b9251-300">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="b9251-301">Logige LCS–i sisse ja klõpsake seejärel lehe parempoolses servas oleva keskkonna nime all valikul **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b9251-301">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="b9251-302">Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="b9251-302">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="b9251-303">Valige lisandmoodul **Data Lake’i eksportimine**.</span><span class="sxs-lookup"><span data-stu-id="b9251-303">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="b9251-304">Sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b9251-304">Enter the following values.</span></span>

    | <span data-ttu-id="b9251-305">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b9251-305">Value</span></span>                                                              | <span data-ttu-id="b9251-306">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b9251-306">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="b9251-307">Azure’i tellimuse rentniku ID, kus asub võtmehoidla</span><span class="sxs-lookup"><span data-stu-id="b9251-307">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="b9251-308">Rentniku ID, kus asuvad salvestamiskonto, rakendused ja võtmehoidlad.</span><span class="sxs-lookup"><span data-stu-id="b9251-308">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="b9251-309">Selle väärtuse leidmiseks avage [Azure’i portaal](https://portal.azure.com), avage **Azure Active Directory** ja kopeerige väärtus **Rentniku ID**.</span><span class="sxs-lookup"><span data-stu-id="b9251-309">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="b9251-310">Sisestage oma võtmehoidla DNS-i nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-310">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="b9251-311">Võtmehoidla DNS-i nimi, nt `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="b9251-311">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="b9251-312">(See väärtus vastab üksuse salvestamisel kasutatavale DNS-i nimele.)</span><span class="sxs-lookup"><span data-stu-id="b9251-312">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="b9251-313">Esitage saladus, mis sisaldab salvestuskonto nime</span><span class="sxs-lookup"><span data-stu-id="b9251-313">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="b9251-314">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="b9251-314">**storage-account-name**</span></span> |
    | <span data-ttu-id="b9251-315">Data Lake’i juurdepääsuks kasutatava rakenduse ID salajane nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-315">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="b9251-316">**app-id**</span><span class="sxs-lookup"><span data-stu-id="b9251-316">**app-id**</span></span> |
    | <span data-ttu-id="b9251-317">Rakenduse ID-ga kasutatav salajane nimi</span><span class="sxs-lookup"><span data-stu-id="b9251-317">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="b9251-318">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="b9251-318">**app-secret**</span></span> |

5. <span data-ttu-id="b9251-319">Nõustuge tingimustega ja valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="b9251-319">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="b9251-320">Lisandmoodul installitakse mõne minuti jooksul.</span><span class="sxs-lookup"><span data-stu-id="b9251-320">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="b9251-321">AI Builderi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b9251-321">Configure AI Builder</span></span>

1. <span data-ttu-id="b9251-322">Logige LCS-i sisse ja avage leht **Keskkonna üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b9251-322">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="b9251-323">Kerige alla jaotiseni **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="b9251-323">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="b9251-324">Peaksite nägema lisandmooduleid, mis on juba sellesse keskkonda installitud.</span><span class="sxs-lookup"><span data-stu-id="b9251-324">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="b9251-325">Kui Lisandmoodulit **Data Lake’i eksportimine** nende seas ei ole, konfigureerige see lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="b9251-325">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="b9251-326">Valige lisandmoodul **Ülevaadete hankimine**.</span><span class="sxs-lookup"><span data-stu-id="b9251-326">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="b9251-327">Lisandmooduli **Ülevaadete hankimine** üksikasjade lehel sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b9251-327">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="b9251-328">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b9251-328">Value</span></span>                                                    | <span data-ttu-id="b9251-329">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b9251-329">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="b9251-330">CDS-i organisatsiooni URL</span><span class="sxs-lookup"><span data-stu-id="b9251-330">CDS Organization URL</span></span>                                     | <span data-ttu-id="b9251-331">Ülalpool kopeeritud Dataverse organisatsiooni URL.</span><span class="sxs-lookup"><span data-stu-id="b9251-331">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="b9251-332">CDS-i organisatsiooni ID</span><span class="sxs-lookup"><span data-stu-id="b9251-332">CDS Org ID</span></span>                                               | <span data-ttu-id="b9251-333">Ülalpool kopeeritud Dataverse organisatsiooni ID.</span><span class="sxs-lookup"><span data-stu-id="b9251-333">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="b9251-334">Lubage suvand **Kas see on rentniku CDS-i vaikekeskkond**.</span><span class="sxs-lookup"><span data-stu-id="b9251-334">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="b9251-335">Üksuse salvestamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b9251-335">Configure the entity store</span></span>

<span data-ttu-id="b9251-336">Järgige neid samme, et seadistada üksuse salvestamine oma Finance’i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="b9251-336">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="b9251-337">Minge jaotisse **Süsteemihaldus \> Seadistus \> Süsteemi parameetrid \>Andmeühendused**.</span><span class="sxs-lookup"><span data-stu-id="b9251-337">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="b9251-338">Seadke järgmised võtmehoidja väljad.</span><span class="sxs-lookup"><span data-stu-id="b9251-338">Set the following key vault fields:</span></span>

    - <span data-ttu-id="b9251-339">**Rakenduse (klient) ID** – sisestage eelnevalt loodud rakenduse kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="b9251-339">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="b9251-340">**Avalduse saladus** – sisestage saladus, mille salvestasite varem loodud rakenduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="b9251-340">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="b9251-341">**DNS-i nimi** – domeeninime süsteemi (DNS) nime leiate varem loodud rakenduse üksikasjade lehelt.</span><span class="sxs-lookup"><span data-stu-id="b9251-341">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="b9251-342">**Salajane nimi** – sisestage **storage-account-connection-string**.</span><span class="sxs-lookup"><span data-stu-id="b9251-342">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="b9251-343">Lubage **Luba Data Lake'i integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="b9251-343">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="b9251-344">Valige suvand **Testi rakendust Azure Key Vault** ja veenduge, et tõrkeid ei ole.</span><span class="sxs-lookup"><span data-stu-id="b9251-344">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="b9251-345">Valige suvand **Testi Azure'i andmemahtu** ja veenduge, et tõrkeid ei ole.</span><span class="sxs-lookup"><span data-stu-id="b9251-345">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="b9251-346">Tagasiside ja tugi</span><span class="sxs-lookup"><span data-stu-id="b9251-346">Feedback and support</span></span>

<span data-ttu-id="b9251-347">Kui soovite anda tagasisidet või vajate tuge, saatke meil [kliendimaksete ülevaadetele (eelversioon)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b9251-347">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="b9251-348">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="b9251-348">Privacy notice</span></span>

<span data-ttu-id="b9251-349">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="b9251-349">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
