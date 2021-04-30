---
title: Tööriista Regression Suite Automation Tool seadistamise ja installimise õppetükk
description: See teema on õppetükk, milles näidatakse, kuidas seadistada installida tööriista Regression suite automation tool (RSAT).
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7c6e4dcbd854cfadbc34f0040dcffd277d32a8d9
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909030"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="39a44-103">Tööriista Regression Suite Automation Tool seadistamise ja installimise õppetükk</span><span class="sxs-lookup"><span data-stu-id="39a44-103">Set up and install Regression suite automation tool tutorial</span></span>

<span data-ttu-id="39a44-104">See teema on õppetükk, mis aitab seadistada RSAT-d ja selle kasutamisega seotud tööriistu ning alustada nende kasutamist.</span><span class="sxs-lookup"><span data-stu-id="39a44-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="39a44-105">Kasutage Interneti-brauseri tööriistu selle lehe allalaadimiseks ja salvestamiseks PDF-vormingus.</span><span class="sxs-lookup"><span data-stu-id="39a44-105">Use your internet browser tools to download and save this page in PDF format.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="39a44-106">Põhimõisted</span><span class="sxs-lookup"><span data-stu-id="39a44-106">Key concepts</span></span>

- <span data-ttu-id="39a44-107">Mõistate installimise ja eeltingimuste seadistus, mis on vajalik mitmesuguste rakenduste jaoks, mis toetavad tööriista Regression suite automation tool (RSAT).</span><span class="sxs-lookup"><span data-stu-id="39a44-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="39a44-108">Mõistate, kuidas saate tegevuse salvestaja funktsiooniga koos teenustega Microsoft Dynamics Lifecycle Services (LCS) ja Microsoft Azure DevOps luua, konfigureerida, käitada ja uurida testjuhtumeid ning nende kohta aruandeid esitada.</span><span class="sxs-lookup"><span data-stu-id="39a44-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="39a44-109">Volitage funktsiooni kasutajaid kirjendama äriülesandeid, kasutades tegevuse salvestajat, ja seejärel teisendage ülesande salvestised automaatsete katsete komplekti, ilma et peaksite kirjutama lähtekoodi.</span><span class="sxs-lookup"><span data-stu-id="39a44-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="39a44-110">Enne alustamist</span><span class="sxs-lookup"><span data-stu-id="39a44-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="39a44-111">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="39a44-111">Prerequisites</span></span>

- <span data-ttu-id="39a44-112">Selle õppetüki jaoks on vaja keskkonda, kus töötab Microsoft Dynamics 365 for Finance and Operationsi versioon 10.0 (aprill 2019) või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="39a44-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="39a44-113">Klientide jaoks, kes kasutavad Microsoft Dynamics 365 for Finance and Operationsi, Enterprise edition 7.3, toetatakse ka platvormivärskendust 20 (PU20) või uuemat versiooni.</span><span class="sxs-lookup"><span data-stu-id="39a44-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="39a44-114">Kasutajal peavad olema selle keskkonna administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="39a44-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="39a44-115">Teil peab olema juurdepääs kliendi rentniku LCS-ile ja Azure DevOpsile (varem Microsoft Visual Studio Team Services \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="39a44-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="39a44-116">Kasutajal, kes loob ja haldab testkomplekte, peab olema Azure DevOpsi katseplaanide või katsehalduri litsents.</span><span class="sxs-lookup"><span data-stu-id="39a44-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="39a44-117">Katseplaanidele annavad juurdepääsu ka järgmised litsentsid.</span><span class="sxs-lookup"><span data-stu-id="39a44-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="39a44-118">Visual Studio ettevõtte litsents</span><span class="sxs-lookup"><span data-stu-id="39a44-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="39a44-119">Visual Studio Test Professionali litsents</span><span class="sxs-lookup"><span data-stu-id="39a44-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="39a44-120">MSDN-i platvormide tellija litsents</span><span class="sxs-lookup"><span data-stu-id="39a44-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="39a44-121">RSAT-l peab olema juurdepääs katsekeskkonnale veebibrauseri kaudu.</span><span class="sxs-lookup"><span data-stu-id="39a44-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="39a44-122">Katseparameetrite loomiseks ja redigeerimiseks peab olema installitud Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="39a44-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="39a44-123">Teenuse Azure DevOps konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="39a44-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="39a44-124">Kasutaja sobivus</span><span class="sxs-lookup"><span data-stu-id="39a44-124">User eligibility</span></span>

<span data-ttu-id="39a44-125">Veenduge, et kasutaja oleks loodud Azure DevOpsis ja tal oleks tellimustase, mis annab juurdepääsu Azure’i katseplaanidele.</span><span class="sxs-lookup"><span data-stu-id="39a44-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="39a44-126">Azure DevOpsi katseplaanide litsentsi on vaja vaid siis, kui kasutaja loob ja haldab katsejuhtumeid (ehk kõikidel RSAT kasutajatel seda litsentsi vaja pole).</span><span class="sxs-lookup"><span data-stu-id="39a44-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="39a44-127">Teavet litsentsi nõudmiste kohta vt teemast [Litsentsi nõudmised](/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="39a44-127">For information about the license requirements, see [License requirements](/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="39a44-128">Uue Azure DevOpsi projekti loomine</span><span class="sxs-lookup"><span data-stu-id="39a44-128">Create a new Azure DevOps project</span></span>

<span data-ttu-id="39a44-129">RSAT kasutab Azure DevOpsi testjuhtumi ja testkomplekti halduseks, aruandluseks ja testkäivituse tulemuste uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span>

> [!NOTE]
> <span data-ttu-id="39a44-130">Võite kasutada olemasolevat Azure DevOpsi projekti.</span><span class="sxs-lookup"><span data-stu-id="39a44-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="39a44-131">Kuid kui olemasolev Azure DevOpsi projekt on seadistatud nii, et sellel on kohandatud mall, saate tõrke „VSTS-i sünkroonimistõrge”, kui sünkroonite testjuhtumeid äriprotsesside modelleerijast (BPM) Azure DevOpsi (vt jaotist [BPM-st Azure DevOpsi sünkroonimise testimine](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="39a44-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="39a44-132">Kui kohandatud malli korral on järgitud järgmisi parimaid tavasid, saate sünkroonida testjuhtumid Azure DevOpsi.</span><span class="sxs-lookup"><span data-stu-id="39a44-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="39a44-133">(Parimad tavad on loendatud tõrketeates.)</span><span class="sxs-lookup"><span data-stu-id="39a44-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="39a44-134">Ärge kustutage ühtegi tööüksuse tüüpi või valmiskujul välja.</span><span class="sxs-lookup"><span data-stu-id="39a44-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="39a44-135">Ärge kustutage ühtegi tööüksuse tüübi olekut.</span><span class="sxs-lookup"><span data-stu-id="39a44-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="39a44-136">Ärge lisage tööüksuse tüübile ühtegi kohustuslikku välja.</span><span class="sxs-lookup"><span data-stu-id="39a44-136">Do not add any required fields to a work item type.</span></span>

![Tõrketeade parimate tavade loendiga](./media/setup_rsa_tool_02.png)

<span data-ttu-id="39a44-138">Muidu soovitame selle õppetüki jaoks luua uue Azure DevOpsi projekti.</span><span class="sxs-lookup"><span data-stu-id="39a44-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="39a44-139">Lisateavet vt teemast [Probleemid BPM-i sünkroonimisel kohandatud Azure DevOpsi (VSTS) protsessimalliga](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="39a44-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="39a44-140">Avage Azure DevOpsi URL (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="39a44-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="39a44-141">Valige suvand **Projekti loomine** Azure DevOpsi lehelt ülevalt paremalt nurgast.</span><span class="sxs-lookup"><span data-stu-id="39a44-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Projekti loomise nupp](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="39a44-143">Täitke järgmise väljad ja valige käsk **Loo**.</span><span class="sxs-lookup"><span data-stu-id="39a44-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="39a44-144">**Projekti nimi**</span><span class="sxs-lookup"><span data-stu-id="39a44-144">**Project name**</span></span>
    - <span data-ttu-id="39a44-145">**Versiooni kontroll** – valige suvand **Team Foundationi versioonikontroll**.</span><span class="sxs-lookup"><span data-stu-id="39a44-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="39a44-146">Pange tähele, et vaikesuvandit **Git** ei toetata.</span><span class="sxs-lookup"><span data-stu-id="39a44-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="39a44-147">**Tööüksuse protsess**</span><span class="sxs-lookup"><span data-stu-id="39a44-147">**Work item process**</span></span>

    ![Uue projekti loomise dialoogiaken](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="39a44-149">Isikliku pääsutõendi loomine</span><span class="sxs-lookup"><span data-stu-id="39a44-149">Create a personal access token</span></span>

<span data-ttu-id="39a44-150">Selles õppetükis kasutate LCS-i äriprotsessi modelleerijat (BPM) testjuhtumi teegi loomiseks ja testjuhtumite loomiseks Azure DevOpsiga.</span><span class="sxs-lookup"><span data-stu-id="39a44-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="39a44-151">Vajate isiklikku pääsutõendit BPM-i sünkroonimiseks Azure DevOpsiga.</span><span class="sxs-lookup"><span data-stu-id="39a44-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="39a44-152">Valige profiili ikoon Azure DevOpsi projekti lehe ülevalt paremalt nurgast ja seejärel valige suvand **Turve**.</span><span class="sxs-lookup"><span data-stu-id="39a44-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Turbe käsk](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="39a44-154">Vasakul paanil jaotisest **Turve** valige suvand **Isiklikud pääsutõendid**.</span><span class="sxs-lookup"><span data-stu-id="39a44-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="39a44-155">Seejärel valige suvand **Uus tõend**.</span><span class="sxs-lookup"><span data-stu-id="39a44-155">Then select **New Token**.</span></span>

    ![Nupp Uus tõend isiklike pääsutõendite vahekaardil kasutajasätetes](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="39a44-157">Täitke järgmise väljad ja valige käsk **Loo**.</span><span class="sxs-lookup"><span data-stu-id="39a44-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="39a44-158">**Nimi**</span><span class="sxs-lookup"><span data-stu-id="39a44-158">**Name**</span></span>
    - <span data-ttu-id="39a44-159">**Aegumine (UTC)** – valige suvand **Määratletud kohandatud** ja seejärel kasutage kuupäevavalijat viimase saadavuskuupäeva valimiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="39a44-160">**Ulatused** – valige suvand **Täielik juurdepääs**.</span><span class="sxs-lookup"><span data-stu-id="39a44-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Isiklik pääsutõendi loomise dialoogiaken](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="39a44-162">Märkige loodud isiklik pääsutõend üles.</span><span class="sxs-lookup"><span data-stu-id="39a44-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="39a44-163">Seda läheb vaja hiljem, kui seadistate RSAT konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="39a44-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Isiklik pääsutõend](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="39a44-165">LCS-i projekti konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="39a44-165">Configure the LCS project</span></span>

<span data-ttu-id="39a44-166">Testide ülemteegi jaoks on vaja teenuse Lifecycle Services (LCS) projekti.</span><span class="sxs-lookup"><span data-stu-id="39a44-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="39a44-167">LCS äriprotsesside modelleerijat (BPM) kasutatakse testjuhtumite ülemteegina.</span><span class="sxs-lookup"><span data-stu-id="39a44-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="39a44-168">BPM-i kasutatakse testteekide haldamiseks ja jaotamiseks LCS-i projektides.</span><span class="sxs-lookup"><span data-stu-id="39a44-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="39a44-169">Näiteks testteeke loov Microsofti partner või sõltumatu tarkvarahankija (ISV) väljastab testteegid BPM-i teekidena.</span><span class="sxs-lookup"><span data-stu-id="39a44-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="39a44-170">BPM-is on testjuhtumid korraldatud äriprotsessi järgi.</span><span class="sxs-lookup"><span data-stu-id="39a44-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="39a44-171">BPM ei määratle testi läbimise täitmisjärjestust või -sagedust.</span><span class="sxs-lookup"><span data-stu-id="39a44-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="39a44-172">Neid üksikasju hallatakse Azure DevOpsi, nagu on kirjeldatud selles teemas allpool.</span><span class="sxs-lookup"><span data-stu-id="39a44-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="39a44-173">LCS-i projekti jaoks saate kasutada olemasolevat kliendi juurutus- või partneriprojekti.</span><span class="sxs-lookup"><span data-stu-id="39a44-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="39a44-174">LCS-i keele värskendamine</span><span class="sxs-lookup"><span data-stu-id="39a44-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="39a44-175">Selleks et kasutajaliides (UI) kuvaks äriprotsesse õigesti, peab LCS-i eelistatud keel olema määratud valikule **Inglise (USA)**.</span><span class="sxs-lookup"><span data-stu-id="39a44-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="39a44-176">Minge LCS-i juurutusprojekti.</span><span class="sxs-lookup"><span data-stu-id="39a44-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="39a44-177">Valige paremast ülanurgast nupp **Sätted** (hammasrattasümbol) ja seejärel valige **Keele-eelistus**.</span><span class="sxs-lookup"><span data-stu-id="39a44-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Keele-eelistuse värskendamine](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="39a44-179">Valige väljast **Eelistatud keel** suvand **Inglise (USA)** ja seejärel valige nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="39a44-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Keele-eelistuse vahekaart kasutajasätetes](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="39a44-181">LCS-i konfigureerimine ühenduse loomiseks Azure DevOpsi projektiga</span><span class="sxs-lookup"><span data-stu-id="39a44-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="39a44-182">Kui lõite varem uue Azure DevOpsi projekti, konfigureerige LCS-i projekt sellega ühendumiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="39a44-183">Kui LCS-i projekt on juba Azure DevOpsi projekti ühendatud, võite minna edasi järgmisse jaotisesse.</span><span class="sxs-lookup"><span data-stu-id="39a44-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="39a44-184">Minge LCS-i juurutusprojekti.</span><span class="sxs-lookup"><span data-stu-id="39a44-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="39a44-185">Valige nupp **Menüü** ja seejärel suvand **Projekti sätted**.</span><span class="sxs-lookup"><span data-stu-id="39a44-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Projekti sätete käsk](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="39a44-187">Valige vasakult paanilt **Visual Studio Team Services** ja seejärel suvand **Teenuse Visual Studio Team Services seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Teenuse Visual Studio Team Services vahekaart projekti sätetes](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="39a44-189">Välja **Azure DevOpsi saidi URL** sisestage Azure DevOpsi saidi URL.</span><span class="sxs-lookup"><span data-stu-id="39a44-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="39a44-190">Välja **Isiklik pääsutõend** sisestage varem loodud isiklik pääsutõend.</span><span class="sxs-lookup"><span data-stu-id="39a44-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-191">Kuigi VSTS kannab nüüd nime Azure DevOps, kasutage LCS-i ühendamiseks Azure DevOpsi projektiga vana URL-i.</span><span class="sxs-lookup"><span data-stu-id="39a44-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="39a44-192">Näiteks selles õppetükis kasutatud Azure DevOpsi URL on `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="39a44-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="39a44-193">Kuid järgmisel joonisel on see sisestatud kujul `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="39a44-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Teenuse Visual Studio Team Services seadistamise 1. etapp](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="39a44-195">Valige nupp **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="39a44-195">Select **Continue**.</span></span>
6. <span data-ttu-id="39a44-196">Väljas **Teenuse Visual Studio Team Services projekt** valige valitud saidi VSTS-i projekt, mille soovite siduda LCS projektiga.</span><span class="sxs-lookup"><span data-stu-id="39a44-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="39a44-197">Väli **Protsessimall** seatakse vaikimisi väärtusele **Kiire**.</span><span class="sxs-lookup"><span data-stu-id="39a44-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="39a44-198">Kohandatud malli jaoks vaadake üle heade tavade juhised jaotises [Uue Azure DevOpsi projekti loomine](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="39a44-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="39a44-199">Seejärel valige nupp **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="39a44-199">Then select **Continue**.</span></span>

    ![Teenuse Visual Studio Team Services seadistamise 2. etapp](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="39a44-201">Vaadake sätted üle ja valige nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="39a44-201">Review your settings, and then select **Save**.</span></span>

    ![Teenuse Visual Studio Team Services seadistamise 3. etapp](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="39a44-203">Valige nupp **Autoriseerimine**, et anda LCS-ile volitus juurdepääsuks konfigureeritud Azure DevOpsi saidile teie nimel ja VSTS-iga integreeritavate funktsioonide sisse lülitamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Nupp Autoriseerimine](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="39a44-205">Kuvatakse teateaken tekstiga „Teid suunatakse ümber välisele saidile, et lubaksite LCS-il teie nimel teenusega Visual Studio Team Services ühenduse luua.</span><span class="sxs-lookup"><span data-stu-id="39a44-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="39a44-206">Kas soovite jätkata?”</span><span class="sxs-lookup"><span data-stu-id="39a44-206">Proceed?"</span></span> <span data-ttu-id="39a44-207">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="39a44-207">Select **Yes**.</span></span>

    ![Teateaken](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="39a44-209">Valige **Aktsepteerimine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-209">Select **Accept**.</span></span>

    ![Juurdepääsu autoriseerimine](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="39a44-211">Kui olete autoriseeritud kasutajana, peaks kasutajaliides viima teid tagasi LCS-i projekti sätete lehele.</span><span class="sxs-lookup"><span data-stu-id="39a44-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Autoriseeritud kasutaja](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="39a44-213">Uue BPM-i teegi loomine</span><span class="sxs-lookup"><span data-stu-id="39a44-213">Create a new BPM library</span></span>

1. <span data-ttu-id="39a44-214">Minge LCS-i juurutusprojekti.</span><span class="sxs-lookup"><span data-stu-id="39a44-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="39a44-215">Valige nupp **Menüü** ja seejärel suvand **Äriprotsesside modelleerija**.</span><span class="sxs-lookup"><span data-stu-id="39a44-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Äriprotsesside modelleerija käsk](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="39a44-217">Valige suvand **Uus teek**.</span><span class="sxs-lookup"><span data-stu-id="39a44-217">Select **New library**.</span></span>

    ![Uue teegi nupp](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="39a44-219">Välja **Teegi nimi** sisestage nimi ja seejärel valige nupp **Loo**.</span><span class="sxs-lookup"><span data-stu-id="39a44-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="39a44-220">Selle õppetüki käigus pange BPM-i teegi nimeks **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="39a44-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Uue teegi loomise dialoogiaken](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="39a44-222">Avage uus **RSAT** BPM-i teek.</span><span class="sxs-lookup"><span data-stu-id="39a44-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="39a44-223">Valige protsess **Peamise äriprotsessi näidis** ja seejärel valige paremalt suvand **Redigeerimisrežiim**.</span><span class="sxs-lookup"><span data-stu-id="39a44-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Redigeerimisrežiimi nupp](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="39a44-225">Muutke väljade **Nimi** ja **Kirjeldus** väärtus valikule **Toote loomine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="39a44-226">Seejärel valige nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="39a44-226">Then select **Save**.</span></span>

    ![Väljad Nimi ja Kirjeldus](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="39a44-228">Keskkond</span><span class="sxs-lookup"><span data-stu-id="39a44-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="39a44-229">Nõudmised versioonile</span><span class="sxs-lookup"><span data-stu-id="39a44-229">Version requirement</span></span>

<span data-ttu-id="39a44-230">Vajalik on katse- või liivakastikeskkond versiooniga 10.</span><span class="sxs-lookup"><span data-stu-id="39a44-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="39a44-231">Klienride jaoks, kes kasutavad versiooni 7.3, toetatakse ka platvormivärskendust 20 või uuemat versiooni.</span><span class="sxs-lookup"><span data-stu-id="39a44-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="39a44-232">RSAT-il peab olema juurdepääs teie katsekeskkonnale veebibrauseri kaudu.</span><span class="sxs-lookup"><span data-stu-id="39a44-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="39a44-233">Kasutaja kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="39a44-233">User criteria</span></span>

<span data-ttu-id="39a44-234">Kasutajal peavad olema selle keskkonna administraatoriõigused.</span><span class="sxs-lookup"><span data-stu-id="39a44-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="39a44-235">Spikri sätete seadistamine ühenduse loomiseks LCS-iga</span><span class="sxs-lookup"><span data-stu-id="39a44-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="39a44-236">See etapp on vajalik ühenduse loomiseks LCS-iga, et tegevuse salvestisi saaks salvestada vastavasse BPM-i teeki LCS-is kliendi kaudu.</span><span class="sxs-lookup"><span data-stu-id="39a44-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="39a44-237">Avage klient.</span><span class="sxs-lookup"><span data-stu-id="39a44-237">Open the client.</span></span>
2. <span data-ttu-id="39a44-238">Minge jaotisse **Süsteemihaldus \> Seadistus \> Süsteemi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="39a44-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="39a44-239">Vahekaardil **Spikker** väljas **Teenuse Lifecycle Services spikri konfiguratsioon** valige vastav LCS-i projekt (selles õppetükis **RSAT**).</span><span class="sxs-lookup"><span data-stu-id="39a44-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Teenuse Lifecycle Services spikri konfiguratsiooni väli vahekaardil Spikker](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="39a44-241">BPM-i teegid täidetakse vastavas LCS-i projektis.</span><span class="sxs-lookup"><span data-stu-id="39a44-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="39a44-242">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="39a44-242">Select **Save**.</span></span>
5. <span data-ttu-id="39a44-243">Spikri uuendatud sisu nägemiseks peate võib-olla brauserit värskendama.</span><span class="sxs-lookup"><span data-stu-id="39a44-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Teatis brauseri värskendamise kohta](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="39a44-245">Tegevuse salvestised</span><span class="sxs-lookup"><span data-stu-id="39a44-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="39a44-246">Veenduge, et kõik tegevuse salvestised algaksid peamiselt armatuurlaualt.</span><span class="sxs-lookup"><span data-stu-id="39a44-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="39a44-247">Hoidke üksikud salvestised lühikesed ja keskenduge ühele äriülesandele, näiteks müügitellimuse loomisele.</span><span class="sxs-lookup"><span data-stu-id="39a44-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="39a44-248">Tegevuse salvestise loomine ja salvestamine BPM-i teeki</span><span class="sxs-lookup"><span data-stu-id="39a44-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="39a44-249">Looge vastav tegevuse salvestis, mida saate manustada uues BPM-i teegis loodud lihtsa äriprotsessi juurde.</span><span class="sxs-lookup"><span data-stu-id="39a44-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="39a44-250">Avage klient.</span><span class="sxs-lookup"><span data-stu-id="39a44-250">Open the client.</span></span>
2. <span data-ttu-id="39a44-251">Valige peamiselt armatuurlaualt nupp **Sätted** (hammasratta sümbol) ja seejärel valige suvand **Tegevuse salvestaja**.</span><span class="sxs-lookup"><span data-stu-id="39a44-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Valige menüüs Sätted suvand Tegevuse salvestaja](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="39a44-253">Valige nupp **Salvestise loomine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-253">Select **Create recording**.</span></span>

    ![Salvestise loomise nupp](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="39a44-255">Täitke väljad **Salvestise nimi** ja **Salvestise kirjeldus** ja seejärel valige nupp **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="39a44-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Salvestise nime ja salvestise kirjelduse väljad](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="39a44-257">Salvestage toote loomise etapid.</span><span class="sxs-lookup"><span data-stu-id="39a44-257">Record the steps for creating a product.</span></span> <span data-ttu-id="39a44-258">Kui olete lõpetanud, valige nupp **Peata** salvestamise lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Toote loomise etapid](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="39a44-260">Valige suvand **Salvesta teenustesse Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="39a44-260">Select **Save to Lifecycle Services**.</span></span>

    ![Tegevuse salvestise salvestamine teenusesse Lifecycle Services](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="39a44-262">Teegi teave laaditakse LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="39a44-262">Library information is loaded from LCS.</span></span>

    ![Teegi teabe laadimine](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="39a44-264">Valige tegevuse salvestisega seostamiseks BPM-i teek.</span><span class="sxs-lookup"><span data-stu-id="39a44-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="39a44-265">Selles õppetükis valige varem loodud BPM-i teek **RSAT** ja selle all äriprotsess **Toote loomine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="39a44-266">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="39a44-266">Then select **OK**.</span></span>

    ![Tegevuse salvestise seostamine BPM-i teegi ja äriprotsessiga](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="39a44-268">Ilmub teade „Salvestamine teenusesse Lifecycle Services õnnestus”.</span><span class="sxs-lookup"><span data-stu-id="39a44-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Teade õnnestunud salvestamisest LCS-i](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="39a44-270">Kui soovite salvestada tegevuse salvestise lokaalselt ja seejärel laadida selle üles BPM-i LCS-i, järgige alltoodud etappe.</span><span class="sxs-lookup"><span data-stu-id="39a44-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="39a44-271">Kui salvestamine on lõpule viidud, valige suvand **Salvesta sellesse arvutisse**.</span><span class="sxs-lookup"><span data-stu-id="39a44-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Salvesta sellesse arvutisse](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="39a44-273">Brauseri teavitusribalt valige nupp **Salvesta** või **Salvesta nimega**, et salvestada fail kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="39a44-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Teavitusriba](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="39a44-275">Valige BPM-i teek **RSAT** ja seejärel äriprotsess tegevuse salvestise salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="39a44-276">Vahekaardil **Ülevaade** valige nupp **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="39a44-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Nupp Laadi üles](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="39a44-278">Valige nupp **Sirvi** ja seejärel valige varem salvestatud fail .axtr.</span><span class="sxs-lookup"><span data-stu-id="39a44-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="39a44-279">Seejärel valige nupp **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="39a44-279">Then select **Upload**.</span></span>

        ![Üleslaadimiseks faili .axtr valimine](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="39a44-281">BPM-ist Azure DevOpsi sünkroonimise testimine</span><span class="sxs-lookup"><span data-stu-id="39a44-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="39a44-282">Kui tegevuse salvestis on äriprotsessi juurde manustatud, peate kinnitama, et äriprotsessi ja seotud tegevuse salvestist saab sünkroonida Azure DevOpsi funktsioonina ja testjuhtumina (vastavalt), kasutades LCS-is VSTS-i sünkroonimise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="39a44-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="39a44-283">Vastav tööüksuse tüüp, mis Azure DevOpsis luuakse, on erinev, olenevalt protsessimallist, mille valisite LCS-i projekti konfigureerimisel Azure DevOpsiga, nagu on kirjeldatud jaotises [Uue Azure DevOpsi projekti loomine](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="39a44-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="39a44-284">Minge BPM-i teeki ja avage varem loodud **RSAT** teek.</span><span class="sxs-lookup"><span data-stu-id="39a44-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="39a44-285">Valige kolmikpunkti nupp (**...**) ja seejärel suvand **VSTS-i sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![VSTS-i sünkroonimise käsk kolmikpunkti menüüs](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="39a44-287">Kui VSTS-i sünkroonimine on lõpule viidud, ilmub vasakule vahekaart **Nõuded**, mis sisaldab vastavat Azure DevOpsi tööüksust.</span><span class="sxs-lookup"><span data-stu-id="39a44-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-288">Azure DevOpsis loodud tööüksusel on pealkirja eesliiteks BPM-i teegi nimi.</span><span class="sxs-lookup"><span data-stu-id="39a44-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Vahekaart Nõuded](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="39a44-290">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="39a44-290">Refresh the page.</span></span>
4. <span data-ttu-id="39a44-291">Valige kolmikpunkti nupp (**...**). Näete lisasuvandit, **Testjuhtumite sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="39a44-292">Valige see suvand.</span><span class="sxs-lookup"><span data-stu-id="39a44-292">Select this option.</span></span>

    ![Testjuhtumite sünkroonimise käsk kolmikpunkti menüüs](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="39a44-294">Kui suvand **Testjuhtumite sünkroonimine** ei ole pärast lehe värskendamist saadaval, minge BPM-i pealehele ja valige suvand **Testjuhtumite sünkroonimine** kogu teegile.</span><span class="sxs-lookup"><span data-stu-id="39a44-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="39a44-295">Seda saate tõhusalt sundkäivitada kogu teegi sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="39a44-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    >
    > ![Suvandi Testjuhtumite sünkroonimine kogu teegi jaoks](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="39a44-297">Kui testjuhtumite sünkroonimine on lõpule viidud, luuakse vahekaardil **Nõuded** uus testjuhtum.</span><span class="sxs-lookup"><span data-stu-id="39a44-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Uus testjuhtum vahekaardil Nõuded](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="39a44-299">Avage Azure DevOpsi projekt ja valige suvandid **Tahvlid \> Tööüksused**.</span><span class="sxs-lookup"><span data-stu-id="39a44-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Tööüksuste käsk jaotises Tahvlid](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="39a44-301">Kinnitage, et BPM-i sünkroonimise kaudu loodud tööüksus ja testjuhtum on olemas.</span><span class="sxs-lookup"><span data-stu-id="39a44-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Tööüksus ja testjuhtum](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="39a44-303">RSAT installimine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="39a44-303">Install and Configure RSAT</span></span>

<span data-ttu-id="39a44-304">RSAT-d saab installida igasse arvutisse, kus töötab Windows 10 ja mille saab ühendada veebibrauseri kaudu (Internet Explorer või Google Chrome) keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="39a44-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="39a44-305">Enne tööriista uue versiooni installimist soovitame varasema versiooni desinstallida.</span><span class="sxs-lookup"><span data-stu-id="39a44-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="39a44-306">Autentimisserdi installimine</span><span class="sxs-lookup"><span data-stu-id="39a44-306">Install an authentication certificate</span></span>

<span data-ttu-id="39a44-307">Autentimise lubamiseks peate looma ja installima serdi samasse arvutisse, kus töötab RSAT.</span><span class="sxs-lookup"><span data-stu-id="39a44-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="39a44-308">Serdi loomine</span><span class="sxs-lookup"><span data-stu-id="39a44-308">Generate a certificate</span></span>

1. <span data-ttu-id="39a44-309">Serdifaili loomiseks avage administraatorina Microsoft Windows PowerShelli aken ja käivitage järgmine käsk.</span><span class="sxs-lookup"><span data-stu-id="39a44-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="39a44-310">Avage serdihaldus, sisestades käsu **certlm.msc** dialoogiaknasse **Käivita**, ja kinnitage, et sert **D365 automaattestimise sert** luuakse jaotisesse **Isiklik \> Serdid**.</span><span class="sxs-lookup"><span data-stu-id="39a44-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-311">Sisestage kindlasti **certlm.msc**, mitte **certmgr.msc**, sest serte salvestatakse kohalikus arvutis.</span><span class="sxs-lookup"><span data-stu-id="39a44-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![D365 automaattestimise sert](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="39a44-313">Tehke serdil paremklõps ja valige käsk **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="39a44-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="39a44-314">Valige suvandid **Usaldusväärsed juurserdi haldurid \> Serdid**.</span><span class="sxs-lookup"><span data-stu-id="39a44-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Sertide kaust kaustas Usaldusväärsed juurserdi haldurid](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="39a44-316">Valige menüüst **Tegevus** käsk **Kleebi**, et kopeerida sert asukohta **Usaldusväärsed juurserdi haldurid**.</span><span class="sxs-lookup"><span data-stu-id="39a44-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Kleepimise käsk menüüs Tegevus](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="39a44-318">Installitud serdi sõrmejälje saamiseks (ilma tühikute ja erimärkideta) avage administraatorina Windows PowerShelli aken ja käivitage järgmised käsud.</span><span class="sxs-lookup"><span data-stu-id="39a44-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="39a44-319">Salvestage sõrmejälg, kuna vajate seda hiljem wif-failide värskendamisel rakendusobjekti serveri (AOS) jaoks ja RSAT konfiguratsiooni seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="39a44-320">AOS-i arvuti konfigureerimine ühenduse usaldamiseks</span><span class="sxs-lookup"><span data-stu-id="39a44-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="39a44-321">Kui keskkond on järgu 2+ keskkond, tuleb serdi sõrmejälge värskendada failis wif.config keskkonna **kõikide** AOS-i arvutite jaoks.</span><span class="sxs-lookup"><span data-stu-id="39a44-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="39a44-322">Looge AOS-i arvutiga Remote Desktop Protocoli (RDP) ühendus.</span><span class="sxs-lookup"><span data-stu-id="39a44-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="39a44-323">Sisselogimise üksikasjad on saadaval LCS-is keskkonna üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="39a44-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="39a44-324">Avage teenus Microsoft Internet Information Services (IIS) ja otsige saitide loendist üles **AOSService**.</span><span class="sxs-lookup"><span data-stu-id="39a44-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService saitide loendis](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="39a44-326">Tehke paremklõps valikul **Uuri**, et avada kaust **\<Drive\>: \\AosService\\WebRoot**.</span><span class="sxs-lookup"><span data-stu-id="39a44-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="39a44-327">Otsige üles fail **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="39a44-327">Find the **wif.config** file.</span></span>

    ![File wif.config kaustas WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="39a44-329">Värskendage faili **wif.config**, lisades serdile ja ameti nimele uus asutuse kirje, nagu on näidatud järgmises näites.</span><span class="sxs-lookup"><span data-stu-id="39a44-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="39a44-330">Kui mitu kasutajat kasutab sama rakendust, peab iga kasutaja looma eraldi sõrmejäljed, mis tuleb kõik lisada jaotisesse **\<keys\>**.</span><span class="sxs-lookup"><span data-stu-id="39a44-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="39a44-331">Kui AOS-i arvuteid on rohkem kui üks, korrake etappe 3 kuni 4 iga lisaarvuti jaoks.</span><span class="sxs-lookup"><span data-stu-id="39a44-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-332">Erineval vanematest järgu 2 keskkondadest juurutatakse uued järgu 2 keskkonnad kahe AOS-i juhtumiga.</span><span class="sxs-lookup"><span data-stu-id="39a44-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="39a44-333">Käivitage **iisreset** kõikides AOS-i arvutites.</span><span class="sxs-lookup"><span data-stu-id="39a44-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-334">Kui teil pole administraatoriõigusi käsu **iisreset** käivitamiseks järgu 1 arvutis, valige LCS-is keskkonna üksikasjade lehelt suvandid Hooldamine > Teenuste taaskäivitamine.</span><span class="sxs-lookup"><span data-stu-id="39a44-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="39a44-335">Järgu 2+ keskkond</span><span class="sxs-lookup"><span data-stu-id="39a44-335">Tier 2+ environment</span></span>

<span data-ttu-id="39a44-336">Kui kasutatakse järgu 2+ (standardse vastuvõtutesti liivakast või uuem versioon) keskkonda, siis kontrollige järgmist registri sätet või seadistage see arvutis, kuhu on installitud RSAT.</span><span class="sxs-lookup"><span data-stu-id="39a44-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="39a44-337">See etapp on vajalik, kuna see aitab vältida autentimise või RSAT ühenduse tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="39a44-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="39a44-338">RSAT installimine</span><span class="sxs-lookup"><span data-stu-id="39a44-338">Install RSAT</span></span>

1. <span data-ttu-id="39a44-339">Minge lehele <https://www.microsoft.com/download/details.aspx?id=57357> ja valige käsk **Laadi alla**.</span><span class="sxs-lookup"><span data-stu-id="39a44-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="39a44-340">Valige kõik failid ja seejärel valige nupp **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="39a44-340">Select all the files, and then select **Next**.</span></span>

    ![Kõikide failide valimine](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="39a44-342">Tehke topeltklõps .msi paketil installeri käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="39a44-343">Kui installimine on lõpule viidud, valige nupp **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="39a44-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT installeri fail](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="39a44-345">Selenium ja brauseri draiverite installimine</span><span class="sxs-lookup"><span data-stu-id="39a44-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="39a44-346">RSAT vanemates versioonides pidite installima Seleniumi ja brauseri draiverid.</span><span class="sxs-lookup"><span data-stu-id="39a44-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="39a44-347">Nüüd pole neid draivereid enam vaja installida, kuna need installitakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="39a44-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="39a44-348">Esimene kord, kui RSAT avate, palutakse teil Selenium automaatselt alla laadida ja installida.</span><span class="sxs-lookup"><span data-stu-id="39a44-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="39a44-349">Lisateavet vt jaotisest [RSAT konfigureerimine](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="39a44-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="39a44-350">Enne kui saate testjuhtumi käivitada, palutakse teil automaatselt alla laadida ja installida brauseri draiver, mis vastab vaikebrauserile, mis valitakse RSAT konfiguratsioonis.</span><span class="sxs-lookup"><span data-stu-id="39a44-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="39a44-351">Lisateavet vt jaotisest [Testjuhtumite laadimine ja käivitamine](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="39a44-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="39a44-352">RSAT kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="39a44-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="39a44-353">Katseplaani ja testkomplektide loomine</span><span class="sxs-lookup"><span data-stu-id="39a44-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="39a44-354">Avage Azure DevOpsi projekt ja valige suvand **Katseplaanid**.</span><span class="sxs-lookup"><span data-stu-id="39a44-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Katseplaanide käsk](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="39a44-356">Valige suvand **Uus katseplaan**.</span><span class="sxs-lookup"><span data-stu-id="39a44-356">Select **New Test Plan**.</span></span>

    ![Uue katseplaani nupp](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="39a44-358">Täitke väli **Nimi** ja seejärel valige käsk **Loo**.</span><span class="sxs-lookup"><span data-stu-id="39a44-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="39a44-359">Selles õppetükis pange katseplaani nimeks **RSAT katseplaan**.</span><span class="sxs-lookup"><span data-stu-id="39a44-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Uue katseplaani dialoogiaken](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="39a44-361">Valige plussmärk (**+**) ja seejärel valige suvand **Staatiline komplekt**, et luua uue katseplaani alla staatiline komplekt.</span><span class="sxs-lookup"><span data-stu-id="39a44-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="39a44-362">Pange uue testkomplekti nimeks **T01 – valmistamine lattu**.</span><span class="sxs-lookup"><span data-stu-id="39a44-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-363">Võite ka luua päringul põhineva komplekti, kui soovite, et uued testjuhtumid automaatselt BPM-ist RSAT testkomplekti tõmmataks.</span><span class="sxs-lookup"><span data-stu-id="39a44-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Staatilise komplekti loomine](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="39a44-365">Testjuhtumite manustamine testkomplektide juurde</span><span class="sxs-lookup"><span data-stu-id="39a44-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="39a44-366">Olemasolevate testjuhtumite lisamiseks testkomplekti valige paremalt käsk **Lisa olemasolev**.</span><span class="sxs-lookup"><span data-stu-id="39a44-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Nupp Lisa olemasolev](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="39a44-368">Valige lehel **Testjuhtumite lisamine komplekti** käsk **Käivita päring** ja seejärel valige testjuhtum testkomplekti lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="39a44-369">Selles õppetükis valige testjuhtum **Uue toote loomine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="39a44-370">Seejärel valige lehel alt paremast nurgast suvand **Testjuhtumite lisamine** (seda nuppu pole järgmisel joonisel).</span><span class="sxs-lookup"><span data-stu-id="39a44-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Nupp Käivita päring](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="39a44-372">Testjuhtum lisatakse testkomplekti **T01 – valmistamine lattu**.</span><span class="sxs-lookup"><span data-stu-id="39a44-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testkomplekti lisatud testjuhtum](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="39a44-374">Konfigureeri RSAT</span><span class="sxs-lookup"><span data-stu-id="39a44-374">Configure RSAT</span></span>

1. <span data-ttu-id="39a44-375">Avage RSAT.</span><span class="sxs-lookup"><span data-stu-id="39a44-375">Open RSAT.</span></span>

    ![RSAT ikoon](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="39a44-377">Saate hoiatusteate tekstiga „Tööriista Regression Suite Automation Tool jaoks on vaja aSeleniumi, kas soovite selle kohe automaatselt alla laadida ja installida?”</span><span class="sxs-lookup"><span data-stu-id="39a44-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="39a44-378">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="39a44-378">Select **Yes**.</span></span>

    ![Hoiatusteade, et Regression Suite Automation Tool nõuab Seleniumit](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="39a44-380">Valige nupp **Sätted** (hammasratta sümbol) ja seejärel täitke ilmuvas dialoogiaknas järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="39a44-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="39a44-381">**Azure DevOpsi URL** – sisestage Azure DevOpsi projekti URL, näiteks `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="39a44-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="39a44-382">**Pääsutõend** – sisestage pääsutõend, millega saab tööriist luua ühenduse Azure DevOpsiga.</span><span class="sxs-lookup"><span data-stu-id="39a44-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="39a44-383">Kasutage isiklikku pääsutõendit, mille lõite varem selles õppetükis.</span><span class="sxs-lookup"><span data-stu-id="39a44-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="39a44-384">Lisateavet vt teemast [Juurdepääsu autentimine isiklike pääsutõenditega](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="39a44-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="39a44-385">**Projekti nimi** – valige oma Azure DevOpsi projekti nimi.</span><span class="sxs-lookup"><span data-stu-id="39a44-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="39a44-386">**Katseplaan** – valige Azure DevOpsi katseplaan, mis sisaldab teie testjuhtumeid.</span><span class="sxs-lookup"><span data-stu-id="39a44-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="39a44-387">Lisateavet vt teemast [Katseplaanide ja testkomplektide loomine](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="39a44-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="39a44-388">Pärast katseplaani valimist valige suvand **Ühenduse test**, et kontrollida ühendust Azure DevOpsiga.</span><span class="sxs-lookup"><span data-stu-id="39a44-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="39a44-389">**Hosti nimi** – sisestage katsekeskkonna hosti nimi, näiteks **\<myaos\>.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="39a44-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="39a44-390">Ärge lisage eesliidet **https://** või **http://**.</span><span class="sxs-lookup"><span data-stu-id="39a44-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="39a44-391">**SOAP-i hosti nimi** – sisestage katsekeskkonna SOAP-i hosti nimi.</span><span class="sxs-lookup"><span data-stu-id="39a44-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="39a44-392">Tavaliselt on SOAP-i hosti nimi sama kui hosti nimi, aga sellel on järelliide **soap**.</span><span class="sxs-lookup"><span data-stu-id="39a44-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="39a44-393">Siin on näide: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="39a44-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="39a44-394">Ärge lisage eesliidet **https://** või **http://**.</span><span class="sxs-lookup"><span data-stu-id="39a44-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="39a44-395">Hosti nime ja SOAP-i hosti nime leidmiseks avage IIS-i haldur, tehke paremklõps suvanditel **Saidid \> AOSService** ja seejärel valige suvand **Sidumiste redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="39a44-396">Väärtused veerus **Hosti nimi** annavad hosti nime ja SOAP-i hosti nime (SOAP-i hosti nimel on URL-ist järelliide **soap**).</span><span class="sxs-lookup"><span data-stu-id="39a44-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Hosti nimi ja SOAP-i hosti nimi hosti nime veerus](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="39a44-398">**Administraatori kasutajanimi** – sisestage katsekeskkonda administraatori meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="39a44-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="39a44-399">**Sõrmejälg** – sisestage autentimisserdi sõrmejälg, nagu on kirjeldatud selles õppetükis eespool.</span><span class="sxs-lookup"><span data-stu-id="39a44-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="39a44-400">**Töökaust** – määrake kausta asukoht, kuhu salvestatakse automatiseerimise testfailid, nt Exceli andmete testfailid.</span><span class="sxs-lookup"><span data-stu-id="39a44-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="39a44-401">Näiteks sisestage või valige **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="39a44-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="39a44-402">Kui kausta nimes on tühikud, siis käivitamine nurjub, sest kausta ei leita.</span><span class="sxs-lookup"><span data-stu-id="39a44-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="39a44-403">See on teadaolev probleem ja see peaks olema tööriista uusimas versioonis lahendatud.</span><span class="sxs-lookup"><span data-stu-id="39a44-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="39a44-404">**Vaikebrauser** – valige kas **Internet Explorer** või **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="39a44-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="39a44-405">Veenduge, et installitud oleks sobivad brauseri draiverid.</span><span class="sxs-lookup"><span data-stu-id="39a44-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="39a44-406">**Testkäivituse ajalõpp** – määrake testkäivituste ajalõpu periood minutites.</span><span class="sxs-lookup"><span data-stu-id="39a44-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="39a44-407">Kui ajalõpu periood möödub, siis kõik aktiivsed aknad suletakse ja ootel olevad testjuhtumid nurjuvad.</span><span class="sxs-lookup"><span data-stu-id="39a44-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="39a44-408">**Testtegevuse ajalõpp** – see väli reguleerib Finance and Operationsi keskkonna serveri päringute ajalõpu perioodi minutites.</span><span class="sxs-lookup"><span data-stu-id="39a44-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="39a44-409">Tavaliselt piisab vaikeväärtusest (2 minutit).</span><span class="sxs-lookup"><span data-stu-id="39a44-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="39a44-410">Kuid aeglasemate keskkondade korral võite seda pikendada, kui tekivad ajalõppudega seotud tõrked.</span><span class="sxs-lookup"><span data-stu-id="39a44-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="39a44-411">**Ettevõtte nimi** – sisestage ettevõtte nimi, mida kasutatakse Exceli parameetri faili loomisel vaikimisi ettevõttena.</span><span class="sxs-lookup"><span data-stu-id="39a44-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="39a44-412">Saate ettevõtet hiljem muuta, redigeerides Exceli parameetrifaili.</span><span class="sxs-lookup"><span data-stu-id="39a44-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Sätete dialoogiaken](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="39a44-414">Sätete rakendamiseks ja salvestamiseks valige käsk **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="39a44-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="39a44-415">Praeguste sätete salvestamiseks arvutisse konfiguratsioonifaili valige käsk **Salvesta nimega**.</span><span class="sxs-lookup"><span data-stu-id="39a44-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="39a44-416">Sätete taastamiseks arvutis olevast konfiguratsioonifailist valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="39a44-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="39a44-417">Valige dialoogiboksi sulgemiseks suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="39a44-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="39a44-418">Testjuhtumite laadimine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="39a44-418">Load and run test cases</span></span>

1. <span data-ttu-id="39a44-419">Valige nupp **Laadi**, et laadida katseplaan **RSAT katseplaan** Azure DevOpsi projektist.</span><span class="sxs-lookup"><span data-stu-id="39a44-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Nupp Laadi](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="39a44-421">Valige testkomplektist testjuhtum **Uue toote loomine** ja seejärel valige suvandid **Uus \> Testikäivitus- ja parameetrifailide loomine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Käsk Testkäivitus- ja parameetrifailide loomine menüüs Uus](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="39a44-423">Exceli parameetrifail luuakse kohalikku kausta, mille määratlesite RSAT konfiguratsioonis (nt **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="39a44-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Loodud Exceli parameetrifail](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="39a44-425">Kui soovite parameetrifailid salvestada, valige nupp **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="39a44-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="39a44-426">Kõikide valitud testjuhtumite automatiseerimise testfailid laaditakse hiljem kasutamiseks üles Azure DevOpsi.</span><span class="sxs-lookup"><span data-stu-id="39a44-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="39a44-427">(Need failid hõlmavad Exceli testparameetrifaile.)</span><span class="sxs-lookup"><span data-stu-id="39a44-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="39a44-428">Nii saate valida nupu **Laadi** parameetrifailide (ja automatiseerimise failide) laadimiseks testjuhtumist otse Azure DevOpsist.</span><span class="sxs-lookup"><span data-stu-id="39a44-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="39a44-429">Parameetrifaile pole vaja uuesti luua.</span><span class="sxs-lookup"><span data-stu-id="39a44-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="39a44-430">See lähenemine muutub oluliseks hiljem, kui soovite säilitada muudatusi parameetrifailis ega taha, et need üle kirjutataks.</span><span class="sxs-lookup"><span data-stu-id="39a44-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="39a44-431">Veendumaks, et automatiseerimise ja parameetrifailid salvestatakse Azure DevOpsi, avage Azure DevOpsi projekt, valige suvandid **Tahvlid \> Tööüksused** ja valige testjuhtum **Uue toote loomine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="39a44-432">Vahekaardil **Manused** peaksite nägema nelja faili.</span><span class="sxs-lookup"><span data-stu-id="39a44-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="39a44-433">**.cs** – C\# automatiseerimise fail</span><span class="sxs-lookup"><span data-stu-id="39a44-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="39a44-434">**.dll** – kompileeritud automatiseerimise fail komplektina</span><span class="sxs-lookup"><span data-stu-id="39a44-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="39a44-435">**.xlsx** – Exceli parameetrifail</span><span class="sxs-lookup"><span data-stu-id="39a44-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="39a44-436">**.xml** – salvestusfail</span><span class="sxs-lookup"><span data-stu-id="39a44-436">**.xml** – Recording file</span></span>

    ![Failid vahekaardil Manused](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="39a44-438">Valige käivitamiseks testjuhtum ja seejärel käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="39a44-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-439">Kui kasutate brauserina Internet Explorerit, siis veenduge enne testjuhtumi käivitamist, et teie töölaua eraldusvõime oleks seatud väärtusele **100%** suvandites **Windowsi kuvasätted \> Mõõtkava ja paigutus**.</span><span class="sxs-lookup"><span data-stu-id="39a44-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="39a44-440">Kui te seda sätet virtuaalarvutis muuta ei saa, muutke seda kliendis (sülearvutis), mille kaudu üritate virtuaalarvutile ligi pääseda.</span><span class="sxs-lookup"><span data-stu-id="39a44-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="39a44-441">Eraldusvõime sätted rakenduvad virtuaalarvuti kuvasätetele.</span><span class="sxs-lookup"><span data-stu-id="39a44-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Töölaua eraldusvõime on seatud väärtusele 100%](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="39a44-443">Kui brauseri draivereid pole süsteemi installitud, kuvatakse hoiatusteade „Selleks toiminguks on vaja brauseri \<browser name\> draiverit.</span><span class="sxs-lookup"><span data-stu-id="39a44-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="39a44-444">Kas soovite selle kohe automaatselt alla laadida ja installida?”</span><span class="sxs-lookup"><span data-stu-id="39a44-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="39a44-445">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="39a44-445">Select **Yes**.</span></span>

    ![Internet Exploreri hoiatusteade](./media/setup_rsa_tool_69.png)

    ![Chrome’i hoiatusteade](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="39a44-448">Kui kasutate brauserina Chrome’i ja saate tõrketeate, et seanssi ei loodud, kuna Chrome’i versioon pole õige, siis laadige alla uusim Chrome’i draiver lehelt <http://chromedriver.chromium.org/downloads> kausta **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="39a44-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Chrome’i tõrketeade](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="39a44-450">Käivitatakse testjuhtum ja värskendatakse välja **Tulemus**.</span><span class="sxs-lookup"><span data-stu-id="39a44-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Uuendatud tulemiväli](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="39a44-452">Kui olete õppetükki järginud nii, nagu see on kirjutatud, siis testjuhtum **Uue toote loomine** nurjub, kuna toote loomise tegevuse salvestamine salvestas toote nime püsiprogrammeeritud väärtusena.</span><span class="sxs-lookup"><span data-stu-id="39a44-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="39a44-453">Kui sama testjuhtumi uuesti käivitate, saate tõrketeate, kuna toode on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="39a44-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Nurjunuks määratud väli Tulemus](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="39a44-455">Testi tulemuste kuvamine</span><span class="sxs-lookup"><span data-stu-id="39a44-455">View the test results</span></span>

1. <span data-ttu-id="39a44-456">Tehke topeltklõps nurjunud testjuhtumil.</span><span class="sxs-lookup"><span data-stu-id="39a44-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="39a44-457">Kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="39a44-457">You receive an error message.</span></span>

    ![Tõrketeade](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="39a44-459">Kogu tõrketeate nägemiseks valige nupp **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="39a44-459">Select **Details** to view the whole error message.</span></span>

    ![Kogu tõrketeade](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="39a44-461">Tõrketeate üksikasjaliku versiooni vaatamiseks Azure DevOpsis valige käsk **Ava Azure DevOpsis**.</span><span class="sxs-lookup"><span data-stu-id="39a44-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="39a44-462">Azure DevOpsis saate vaadata testjuhtumi olekut ja üksikasjalikku tõrketeadet.</span><span class="sxs-lookup"><span data-stu-id="39a44-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Üksikasjalik tõrketeade Azure DevOpsis](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="39a44-464">Testi tulemuste vaatamiseks otse Azure DevOpsi projektis valige suvandid **Katseplaanid \> Katseplaanid \> Käivitused**.</span><span class="sxs-lookup"><span data-stu-id="39a44-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="39a44-465">Tehke topeltklõps testkäivitusel, mille üksikasju soovite näha.</span><span class="sxs-lookup"><span data-stu-id="39a44-465">Double-click the test run that you want to see more details for.</span></span>

    ![Testkäivituste loend Azure DevOpsis](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="39a44-467">Vahekaart **Käivituse kokkuvõte** näitab, et testjuhtum nurjus, aga tegelikku tõrketeadet ei esitata.</span><span class="sxs-lookup"><span data-stu-id="39a44-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="39a44-468">Üksikasjaliku tõrketeate vaatamiseks valige vahekaart **Testi tulemused**.</span><span class="sxs-lookup"><span data-stu-id="39a44-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Vahekaart Käivituse kokkuvõte](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="39a44-470">Vahekaardil **Testi tulemused** leiate testjuhtumi teabe koos tulemuse ja tõrketeatega.</span><span class="sxs-lookup"><span data-stu-id="39a44-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Vahekaart testi tulemused](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="39a44-472">Üksikasjaliku tõrketeate nägemiseks tehke topeltklõps vastaval kirjel.</span><span class="sxs-lookup"><span data-stu-id="39a44-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Üksikasjalik tõrketeade](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="39a44-474">Kõik tõrketeated on saadaval ka lokaalselt failis **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="39a44-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="39a44-475">Saate eksportida testkäivituse tulemused katseplaani tasemest, valides nupu **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="39a44-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Katseplaani eksportimine](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="39a44-477">Exceli parameetrifaili muutmine</span><span class="sxs-lookup"><span data-stu-id="39a44-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="39a44-478">Avage RSAT.</span><span class="sxs-lookup"><span data-stu-id="39a44-478">Open RSAT.</span></span>
2. <span data-ttu-id="39a44-479">Valige testjuhtum ja seejärel nupp **Redigeeri** Exceli parameetrifaili avamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="39a44-480">Lehel **EcoResProductCreate** pange tähele, et väli **Tootenumber** on püsiprogrammeeritud.</span><span class="sxs-lookup"><span data-stu-id="39a44-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="39a44-481">Peate värskendama selle välja uuele tootenumbrile, enne kui testjuhtumi uuesti käivitate.</span><span class="sxs-lookup"><span data-stu-id="39a44-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="39a44-482">Iga käivituse jaoks kordumatu tootenumbri loomiseks Exceli parameetrifaili uuesti avamata ja tootenumbrit iga kord käsitsi värskendamata kasutage järgmist Exceli valemit.</span><span class="sxs-lookup"><span data-stu-id="39a44-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="39a44-483">Lisaks vahekaardile **Üldine** sisaldab Exceli parameetrifail andmete vahekaarti iga vormi lehe kohta, mida testjuhtum külastab.</span><span class="sxs-lookup"><span data-stu-id="39a44-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Tootenumbri väli](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="39a44-485">Valige **Salvesta** ja sulgege seejärel Exceli tööraamat.</span><span class="sxs-lookup"><span data-stu-id="39a44-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="39a44-486">Valige nupp **Laadi üles** Exceli parameetrifaili salvestamiseks Azure DevOpsi.</span><span class="sxs-lookup"><span data-stu-id="39a44-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Teade üleslaadimise õnnestumise kohta](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="39a44-488">Testjuhtumite käivitamiseks konkreetses kasutaja kontekstist sisestage kasutaja meiliaadressi ID välja **Testkasutaja** Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="39a44-489">RSAT uusimas versioonis on Exceli parameetrifaili väljade paigutust värskendatud, aga põhimõte on sama.</span><span class="sxs-lookup"><span data-stu-id="39a44-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Väli Testkasutaja](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="39a44-491">Tulemuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="39a44-491">Validate the results</span></span>

- <span data-ttu-id="39a44-492">Testjuhtumi uuesti käivitamiseks valige nupp **Käivita** ja veenduge, et testjuhtum on läbitud.</span><span class="sxs-lookup"><span data-stu-id="39a44-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="39a44-493">Testi tulemusi saate vaadata, nagu on kirjeldatud jaotises [Testi tulemuste vaatamine](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="39a44-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Läbituks määratud väli Tulemus](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="39a44-495">Testjuhtumite aheltöötlus</span><span class="sxs-lookup"><span data-stu-id="39a44-495">Chaining of test cases</span></span>

<span data-ttu-id="39a44-496">Üks RSAT põhifunktsioone on testjuhtumite aheltöötlus (test suudab edastada väärtusi teistele testidele).</span><span class="sxs-lookup"><span data-stu-id="39a44-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="39a44-497">Testjuhtumid käivitatakse Azure DevOpsi katseplaanis määratud järjekorra järgi.</span><span class="sxs-lookup"><span data-stu-id="39a44-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="39a44-498">(Seda järjekorda saab värskendada ka testtööriistas.) Seega kui soovite edastada muutujaid ühest testjuhtumist teise, on väga oluline, et testid oleksid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="39a44-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="39a44-499">Selles jaotises loote salvestatud muutuja esimeses testjuhtumis, loote teise testjuhtumi ja edastate salvestatud muutuja esimesest testjuhtumist teise testjuhtumisse.</span><span class="sxs-lookup"><span data-stu-id="39a44-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="39a44-500">Seejärel käivitate testjuhtumid RSAT-s testjuhtumi ahelana.</span><span class="sxs-lookup"><span data-stu-id="39a44-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="39a44-501">Olemasoleva tegevuse salvestise muutmine salvestatud muutuja loomiseks</span><span class="sxs-lookup"><span data-stu-id="39a44-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="39a44-502">Avage klient.</span><span class="sxs-lookup"><span data-stu-id="39a44-502">Open the client.</span></span>
2. <span data-ttu-id="39a44-503">Valige nupp **Sätted** (hammasratta sümbol) ja seejärel valige suvand **Tegevuse salvestaja**.</span><span class="sxs-lookup"><span data-stu-id="39a44-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="39a44-504">Valige nupp **Salvestise redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-504">Select **Edit Recording**.</span></span>

    ![Salvestise redigeerimise nupp](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="39a44-506">Valige nupp **Ava teenusest Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="39a44-506">Select **Open from Lifecycle Services**.</span></span>

    ![Nupp Ava teenusest Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="39a44-508">Valige nupp **Vali teenuse Lifecycle Services teek**.</span><span class="sxs-lookup"><span data-stu-id="39a44-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Nupp Vali teenuse Lifecycle Services teek](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="39a44-510">BPM-i teegid laaditakse LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="39a44-510">BPM libraries are loaded from LCS.</span></span>

    ![BPM-i teekide laadimine](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="39a44-512">Pärast BPM-i teekide laadimist LCS-ist valige BPM-i teek **RSAT** ja äriprotsess **Uue toote loomine**, millega tegevuse salvestis on seotud.</span><span class="sxs-lookup"><span data-stu-id="39a44-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="39a44-513">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="39a44-513">Then select **OK**.</span></span>

    ![BPM-i teegi ja äpriprotsessi valimine](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="39a44-515">Vastava tegevuse salvestise nimi sisestatakse välja **Salvestise nimi**.</span><span class="sxs-lookup"><span data-stu-id="39a44-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="39a44-516">Valige nupp **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="39a44-516">Select **Start**.</span></span>

    ![Tegevuse salvestise nimi väljal Salvestise nimi](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="39a44-518">Valige suvandid **Tooteteabe haldus \> Tooted** ja valige nupp **Uus**, et avada leht, kus salvestati algne tegevuse salvestis, **Toote loomine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="39a44-519">Valige nupp **Sisesta etapp**.</span><span class="sxs-lookup"><span data-stu-id="39a44-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-520">Uus etapp sisestatakse **pärast** paanilt valitud etappi.</span><span class="sxs-lookup"><span data-stu-id="39a44-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Nupp Sisesta etapp](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="39a44-522">Tehke paremklõps väljal **Tootenumber** ja seejärel valige suvandid **Tegevuse salvestaja \> Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="39a44-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Käsk Kopeeri](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="39a44-524">Paanile lisatakse uus etapp.</span><span class="sxs-lookup"><span data-stu-id="39a44-524">A new step is added in the pane.</span></span> <span data-ttu-id="39a44-525">Märkige välja **Tootenumber** väärtus üles, seda läheb hiljem vaja.</span><span class="sxs-lookup"><span data-stu-id="39a44-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Lisatud uus etapp](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="39a44-527">Valige nupp **Muutmine on lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="39a44-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="39a44-528">Valige nupp **Salvesta teenusesse Lifecycle Services** ja seostage uus tegevuse salvestis sama BPM-i teegi ja äriprotsessiga, millega oli seotud algne tegevuse salvestis.</span><span class="sxs-lookup"><span data-stu-id="39a44-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="39a44-529">Lisateavet vt jaotisest [Tegevuse salvestise loomine ja salvestamine BPM-i teeki](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="39a44-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="39a44-530">Minge BPM-i teeki ja valige suvand **Testjuhtumite sünkroonimine**, et kirjutada üle tegevuse salvestis, mis on seotud testjuhtumiga Azure DevOpsis, nagu on kirjeldatud jaotises [BPM-ist Azure DevOpsi sünkroonimise testimine](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="39a44-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="39a44-531">Avage RSAT ja valige nupp **Laadi**, et laadida uuesti kõik testjuhtumid testkomplektis.</span><span class="sxs-lookup"><span data-stu-id="39a44-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="39a44-532">Peate looma uuesti automatiseerimise ja parameetrifaili vastava testjuhtumi jaoks, valides testjuhtumi ja seejärel suvandid **Uus \> Testkäivitus- ja parameetrifailide loomine**, nagu on kirjeldatud jaotises [Testjuhtumite laadimine ja käivitamine](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="39a44-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-533">Kui Exceli parameetrifail jäeti lahti, siis uuesti loomine nurjub.</span><span class="sxs-lookup"><span data-stu-id="39a44-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="39a44-534">Seetõttu olge kindel, et testjuhtumi Exceli parameetrifail suletakse enne uue Exceli parameetrifaili loomist.</span><span class="sxs-lookup"><span data-stu-id="39a44-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="39a44-535">Valige nupp **Redigeeri**, et avada uus Exceli parameetrifail.</span><span class="sxs-lookup"><span data-stu-id="39a44-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="39a44-536">Näete uut kannet **Salvestatud muutuja** real 9.</span><span class="sxs-lookup"><span data-stu-id="39a44-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="39a44-537">See muutuja, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, salvestatakse tegevuse salvestise XML-faili ja seda saab kasutada edaspidistes testides.</span><span class="sxs-lookup"><span data-stu-id="39a44-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Salvestatud muutuja kanne](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="39a44-539">Uue testjuhtumi loomine</span><span class="sxs-lookup"><span data-stu-id="39a44-539">Create a new test case</span></span>

1. <span data-ttu-id="39a44-540">Minge BPM-i teeki **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="39a44-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="39a44-541">Valige protsess **Tugiäriprotsessi näidis** ja seejärel valige paremalt suvand **Redigeerimisrežiim**.</span><span class="sxs-lookup"><span data-stu-id="39a44-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="39a44-542">Muutke väljade **Nimi** ja **Kirjeldus** väärtus valikule **Toote väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="39a44-543">Seejärel valige nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="39a44-543">Then select **Save**.</span></span>

    ![Väärtusele Toote väljastamine muudetud nimi ja kirjeldus](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="39a44-545">Uue kinnitamise funktsiooniga tegevuse salvestise loomine</span><span class="sxs-lookup"><span data-stu-id="39a44-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="39a44-546">Looge tegevuse salvestis, et väljastada varem loodud toode USRT juriidilisse isikusse.</span><span class="sxs-lookup"><span data-stu-id="39a44-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="39a44-547">Lisateavet vt jaotisest [Tegevuse salvestise loomine ja salvestamine BPM-i teeki](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="39a44-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39a44-548">Testjuhtumite ahela jaoks soovite alati otsida või filtreerida vajalikku kirjet, *sisestades välja väärtuse käsitsi*.</span><span class="sxs-lookup"><span data-stu-id="39a44-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="39a44-549">Nii saab tööriist määrata kirje, mille suhtes järgmises testjuhtumis tuleb tegevus teha.</span><span class="sxs-lookup"><span data-stu-id="39a44-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Uus kinnitamise funktsiooniga tegevuse salvestis](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="39a44-551">Nagu eelmisel joonisel näha, siis pärast toote leidmist kiirfiltriga, aga enne nupu **Väljasta tooted** valimist kinnitate välja **Tootenumber** väärtuse veendumaks, et toote ID on varem loodud toote ID.</span><span class="sxs-lookup"><span data-stu-id="39a44-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="39a44-552">Väärtuse kinnitamiseks tehke paremklõps väljal **Tootenumber** ja seejärel valige suvandid **Tegevuse salvestaja \> Kinnita \> Praegune väärtus**.</span><span class="sxs-lookup"><span data-stu-id="39a44-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Praeguse väärtuse kinnitamine](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="39a44-554">Tegevuse salvestise salvestamine BPM-i</span><span class="sxs-lookup"><span data-stu-id="39a44-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="39a44-555">Kui tegevuse salvestamine on lõpule viidud, valige suvand **Salvesta teenusesse Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="39a44-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Lõpetatud tegevuse salvestise salvestamine teenusesse Lifecycle Services](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="39a44-557">Teegi teave laaditakse LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="39a44-557">Library information is loaded from LCS.</span></span>

    ![Teegi teabe laadimine LCS-ist](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="39a44-559">Valige tegevuse salvestisega seostamiseks BPM-i teek.</span><span class="sxs-lookup"><span data-stu-id="39a44-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="39a44-560">Selles õppetükis valige varem loodud BPM-i teek **RSAT** ja selle all äriprotsess **Toote väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="39a44-561">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="39a44-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="39a44-562">BPM-i sünkroonimine Azure DevOpsiga</span><span class="sxs-lookup"><span data-stu-id="39a44-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="39a44-563">Minge BPM-i teeki ja avage teek **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="39a44-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="39a44-564">Valige suvand **VSTS-i sünkroonimine** ja seejärel suvand **Testjuhtumite sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="39a44-565">Lisateavet vt jaotisest [BPM-ist Azure DevOpsi sünkroonimise testimine](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="39a44-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="39a44-566">Kui sünkroonimine on lõpule viidud, kuvatakse äriprotsessi **Toote väljastamine** uus tööüksus ja vastav testjuhtum Azure DevOpsis jaotises **Tahvlid \> Tööüksused**.</span><span class="sxs-lookup"><span data-stu-id="39a44-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="39a44-567">Uue testjuhtumi lisamine olemasolevasse testkomplekti</span><span class="sxs-lookup"><span data-stu-id="39a44-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="39a44-568">Valige suvandid **Katseplaanid \> Katseplaanid** ja valige plaan **RSAT katseplaan**.</span><span class="sxs-lookup"><span data-stu-id="39a44-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="39a44-569">Valige nupp **Lisa olemasolev**.</span><span class="sxs-lookup"><span data-stu-id="39a44-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="39a44-570">Lehel **Testjuhtumite lisamine komplekti** valige käsk **Käivita päring**.</span><span class="sxs-lookup"><span data-stu-id="39a44-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="39a44-571">Valige uus testjuhtum, mis loodi suvandi **Toote väljastamine** jaoks, ja seejärel valige lehel alt paremalt nurgast nupp **Testjuhtumite lisamine** (seda nuppu pole järgmisel joonisel).</span><span class="sxs-lookup"><span data-stu-id="39a44-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Leht Testjuhtumite lisamine komplekti](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="39a44-573">Testkomplektil on nüüd kaks testjuhtumit.</span><span class="sxs-lookup"><span data-stu-id="39a44-573">The test suite now has two test cases.</span></span>

    ![Kaks testjuhtumit testkomplektis](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="39a44-575">Testjuhtumite laadimine RSAT-sse</span><span class="sxs-lookup"><span data-stu-id="39a44-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="39a44-576">Avage RSAT ja valige nupp **Laadi**.</span><span class="sxs-lookup"><span data-stu-id="39a44-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="39a44-577">Testjuhtumid laaditakse ja kuvatakse hoiatus tekstiga „See tegevus kirjutab üle Exceli testandmefailid, kohalikud muudatused lähevad kaduma.</span><span class="sxs-lookup"><span data-stu-id="39a44-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="39a44-578">Kas soovite jätkata?”</span><span class="sxs-lookup"><span data-stu-id="39a44-578">Do you want to proceed?"</span></span> <span data-ttu-id="39a44-579">Valige nupp **Jah** Exceli parameetrifailide värskendamiseks kohalikus süsteemis, aga mitte Azure DevOpsi üles laaditud Exceli parameetrifailide värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![See toiming kirjutab Exceli testandmefailid üle](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="39a44-581">Mõlemad testjuhtumid on laaditud koos Exceli parameetrifailiga esimese testjuhtumi jaoks.</span><span class="sxs-lookup"><span data-stu-id="39a44-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="39a44-582">Kuna valisite viimasel käitusel nupu **Laadi**, tõmmatakse parameetrifailid Azure DevOpsist.</span><span class="sxs-lookup"><span data-stu-id="39a44-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Laaditud testjuhtumid](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="39a44-584">Valige ainult teine testjuhtum ja seejärel suvandid **Uus \> Testkäivitus- ja parameetrifailide loomine**.</span><span class="sxs-lookup"><span data-stu-id="39a44-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="39a44-585">Exceli parameetrifaili redigeerimine</span><span class="sxs-lookup"><span data-stu-id="39a44-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="39a44-586">Valige ainult teine testjuhtum ja seejärel valige nupp **Redigeeri** vastava Exceli parameetrifaili avamiseks.</span><span class="sxs-lookup"><span data-stu-id="39a44-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="39a44-587">Kopeerige salvestatud muutuja **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (vt jaotist [Olemasoleva tegevuse salvestise muutmine salvestatud muutuja loomiseks](#modify-an-existing-task-recording-to-create-a-saved-variable)) esimesest testjuhtumist kõikidesse väljadesse, kus kasutatakse tootenumbrit.</span><span class="sxs-lookup"><span data-stu-id="39a44-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="39a44-588">Kopeerige selles juhtumis muutuja väljadesse **Tootenumber** ja **Tootenumbri kinnitus** lehel **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="39a44-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Tootenumbri ja tootenumbri kinnituse väljad](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="39a44-590">Muutujaid saab edastada testide vahel ainult sama testkäivituse ajal.</span><span class="sxs-lookup"><span data-stu-id="39a44-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="39a44-591">Muutujate nimed peavad täpselt kattuma.</span><span class="sxs-lookup"><span data-stu-id="39a44-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="39a44-592">Valige **Salvesta** ja sulgege seejärel Exceli tööraamat.</span><span class="sxs-lookup"><span data-stu-id="39a44-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="39a44-593">Valige suvand **Laadi üles**, et salvestada Exceli parameetrifailis tehtud muudatused.</span><span class="sxs-lookup"><span data-stu-id="39a44-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="39a44-594">Testjuhtumite ahela käivitamine</span><span class="sxs-lookup"><span data-stu-id="39a44-594">Run the chained test cases</span></span>

1. <span data-ttu-id="39a44-595">Valige mõlemad testjuhtumid ja seejärel käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="39a44-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="39a44-596">Kontrollige, kas mõlemad testjuhtumid on läbitud.</span><span class="sxs-lookup"><span data-stu-id="39a44-596">Verify that both test cases have passed.</span></span>

    ![Väli Tulemus, mis on seatud väärtusele Läbitud mõlema testjuhtumi korral](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]