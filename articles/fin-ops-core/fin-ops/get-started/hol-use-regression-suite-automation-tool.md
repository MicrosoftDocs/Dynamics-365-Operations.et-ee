---
title: Tööriista Regression Suite Automation Tool õppetüki kasutamine
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
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070816"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="d911e-104">Tööriista Regression suite automation tool kasutamise õppetükk</span><span class="sxs-lookup"><span data-stu-id="d911e-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="d911e-105">Kasutage Interneti-brauseri tööriistu selle lehe allalaadimiseks ja salvestamiseks PDF-vormingus.</span><span class="sxs-lookup"><span data-stu-id="d911e-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="d911e-106">Selles õppetükis tutvustatakse tööriista Regression suite automation tool (RSAT) täpsemaid funktsioone, see hõlmab demomääramist ning kirjeldab strateegiat ja peamisi õppekohti.</span><span class="sxs-lookup"><span data-stu-id="d911e-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="d911e-107">RSAT / tegevuse salvestaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="d911e-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="d911e-108">Välja väärtuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="d911e-108">Validate a field value</span></span>

<span data-ttu-id="d911e-109">Teavet selle funktsiooni kohta vaadake teemast [Uue tegevuse salvestise loomine, millel on valideerimise funktsioon](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="d911e-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="d911e-110">Salvestatud muutuja</span><span class="sxs-lookup"><span data-stu-id="d911e-110">Saved variable</span></span>

<span data-ttu-id="d911e-111">Teavet selle funktsiooni kohta vaadake teemast [Olemasoleva tegevuse salvestise muutmine salvestatud muutuja loomiseks](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="d911e-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="d911e-112">Tuletatud testjuhtum</span><span class="sxs-lookup"><span data-stu-id="d911e-112">Derived test case</span></span>

1. <span data-ttu-id="d911e-113">Avage Regression Suite Automation Tool (RSAT) ja valige mõlemad loodud testjuhtumid jaotisest [Tööriista Regression Suite Automation tool seadistamise ja installimise õpetus](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="d911e-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="d911e-114">Valige suvandid **Uus \> Loo tuletatud testjuhtum**.</span><span class="sxs-lookup"><span data-stu-id="d911e-114">Select **New \> Create derived test case**.</span></span>

    ![Tuletatud testjuhtumi käsu loomine menüüs Uus](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="d911e-116">Saate teate, et tuletatud testjuhtum luuakse iga valitud testjuhtumi kohta praeguses testkomplektis ja igal tuletatud testjuhtumil on oma koopia Exceli parameetrifailist.</span><span class="sxs-lookup"><span data-stu-id="d911e-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="d911e-117">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d911e-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d911e-118">Kui käivitate tuletatud testjuhtumi, kasutab see ülemtestjuhtumi tegevuse salvestist ja oma koopiat Exceli parameetrifailist.</span><span class="sxs-lookup"><span data-stu-id="d911e-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="d911e-119">Nii saate käivitada sama testi eri parameetritega, ilma et peaksite säilitama rohkem kui ühe tegevuse salvestise.</span><span class="sxs-lookup"><span data-stu-id="d911e-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="d911e-120">Tuletatud testjuhtum ei pea olema osa samast testkomplektist kui selle ülemtestjuhtum.</span><span class="sxs-lookup"><span data-stu-id="d911e-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Teateaken](./media/use_rsa_tool_02.png)

    <span data-ttu-id="d911e-122">Luuakse kaks täiendavat testjuhtumit ja nende jaoks valitakse märkeruut **Tuletatud?**.</span><span class="sxs-lookup"><span data-stu-id="d911e-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Loodud tuletatud testjuhtumid](./media/use_rsa_tool_03.png)

    <span data-ttu-id="d911e-124">Tuletatud testjuhtum luuakse automaatselt rakenduses Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="d911e-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="d911e-125">See on testjuhtumi **Uue toote loomine** allüksus ja see märgistatakse spetsiaalse märksõnaga: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="d911e-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="d911e-126">Need testjuhtumid lisatakse ka automaatselt katseplaanile rakenduses Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="d911e-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Märksõna RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="d911e-128">Kui tuletatud testjuhtumid pole mingil põhjusel õiges järjekorras, minge rakendusse Azure DevOps ja muutke testjuhtumite järjekorda testkomplektis, et RSAT saaks need käivitada õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="d911e-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="d911e-129">Valige tuletatud testjuhtumid ja seejärel valige nupp **Redigeeri** vastavate Exceli parameetrifailide avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d911e-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="d911e-130">Redigeerige neid Exceli parameetrifaile samamoodi, nagu redigeerisite ülemfaile.</span><span class="sxs-lookup"><span data-stu-id="d911e-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="d911e-131">Teisisõnu veenduge, et toote ID oleks seadistatud nii, et see luuakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d911e-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="d911e-132">Peale selle veenduge, et salvestatud muutuja kopeeritakse asjakohastesse väljadesse.</span><span class="sxs-lookup"><span data-stu-id="d911e-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="d911e-133">Mõlema Exceli parameetrifaili vahekaardil **Üldine** uuendage väli **Ettevõte** väärtusele **USSI**, et tuletatud testjuhtumid käivitatakse muu juriidilise isiku suhtes kui ülemtestjuhtum.</span><span class="sxs-lookup"><span data-stu-id="d911e-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="d911e-134">Testjuhtumite käivitamiseks konkreetse kasutaja (või konkreetse kasutajaga seotud rolli) suhtes saate uuendada välja **Testkasutaja** väärtust.</span><span class="sxs-lookup"><span data-stu-id="d911e-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="d911e-135">Valige käsk **Käivita** ja kontrollige, kas toode luuakse nii USMF-i juriidilises isikus kui ka USSI juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="d911e-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="d911e-136">Teatiste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="d911e-136">Validate notifications</span></span>

<span data-ttu-id="d911e-137">Seda funktsiooni saab kasutada ka kontrollimaks, kas tegevus toimus.</span><span class="sxs-lookup"><span data-stu-id="d911e-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="d911e-138">Näiteks kui luuakse tootmistellimus, seda hinnatakse ja see seejärel käivitatakse, kuvab rakendus teate „Tootmine – alusta”, mis annab teada, et tootmistellimust on alustatud.</span><span class="sxs-lookup"><span data-stu-id="d911e-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Teatis Tootmine – alusta](./media/use_rsa_tool_05.png)

<span data-ttu-id="d911e-140">Saate selle teate kinnitada läbi RSAT, sisestades teate teksti vastava salvestise Exceli parameetrifaili vahekaardile **Teate kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="d911e-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Vahekaart Teate kinnitamine](./media/use_rsa_tool_06.png)

<span data-ttu-id="d911e-142">Pärast testjuhtumi käivitamist võrreldakse teadet Exceli parameetrifailis kuvatava teatega.</span><span class="sxs-lookup"><span data-stu-id="d911e-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="d911e-143">Kui teated ei kattu, siis testjuhtum nurjub.</span><span class="sxs-lookup"><span data-stu-id="d911e-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="d911e-144">Võite sisestada Exceli parameetrifaili vahekaardile **Teate kinnitamine** rohkem kui ühe teate.</span><span class="sxs-lookup"><span data-stu-id="d911e-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="d911e-145">Teated võivad olla ka tõrke- või hoiatusteated, mitte teavitavad teated.</span><span class="sxs-lookup"><span data-stu-id="d911e-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="d911e-146">Väärtuste kinnitamine tehtemärke kasutades</span><span class="sxs-lookup"><span data-stu-id="d911e-146">Validate values by using operators</span></span>

<span data-ttu-id="d911e-147">Eelmistes RSAT versioonides saite väärtusi kinnitada ainult siis, kui kontrollväärtus oli võrdne eeldatava väärtusega.</span><span class="sxs-lookup"><span data-stu-id="d911e-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="d911e-148">Uue funktsiooniga saate kinnitada, kas muutuja ei ole konkreetse väärtusega võrdne, on sellest väiksem või sellest suurem.</span><span class="sxs-lookup"><span data-stu-id="d911e-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="d911e-149">Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.</span><span class="sxs-lookup"><span data-stu-id="d911e-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="d911e-150">Exceli parameetrifaili ilmub uus väli **Tehtemärk**.</span><span class="sxs-lookup"><span data-stu-id="d911e-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d911e-151">Kui olete kasutanud RSAT vanemat versiooni, peate looma uued Exceli parameetrifailid.</span><span class="sxs-lookup"><span data-stu-id="d911e-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Väli Tehtemärk](./media/use_rsa_tool_07.png)

<span data-ttu-id="d911e-153">Järgmises näites näete, kuidas kasutada seda funktsiooni kinnitamaks, kas vaba kaubavaru väärtus on suurem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d911e-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="d911e-154">Looge ettevõtte **USMF** demoandmetes tegevuse salvestis, mis sisaldab järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="d911e-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="d911e-155">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="d911e-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="d911e-156">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="d911e-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d911e-157">Näiteks filtreerige välja **Kaubakood** väärtuse **1000** järgi.</span><span class="sxs-lookup"><span data-stu-id="d911e-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="d911e-158">Valige **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="d911e-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="d911e-159">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="d911e-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d911e-160">Näiteks filtreerige välja **Tegevuskoht** väärtuse **1** järgi.</span><span class="sxs-lookup"><span data-stu-id="d911e-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="d911e-161">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d911e-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="d911e-162">Kinnitage, et välja **Kokku saadaval** väärtus on **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="d911e-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="d911e-163">Salvestage tegevuse salvestis LCS-is BPM-i teeki ja sünkroonige see rakendusega Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="d911e-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="d911e-164">Lisage testjuhtum katseplaani ja laadige testjuhtum RSAT-sse.</span><span class="sxs-lookup"><span data-stu-id="d911e-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="d911e-165">Avage Exceli parameetrifail.</span><span class="sxs-lookup"><span data-stu-id="d911e-165">Open the Excel parameter file.</span></span> <span data-ttu-id="d911e-166">Vahekaardil **InventOnhandItem** näete jaotist **Kinnita InventOnhandItem**, mis sisaldab välja **Tehtemärk**.</span><span class="sxs-lookup"><span data-stu-id="d911e-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Väli Tehtemärk](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="d911e-168">Kinnitamaks, kas vaba kaubavaru on alati rohkem kui 0, muutke välja **Väärtus** väärtuselt **411** väärtusele **0** ja väljal **Tehtemärk** võrdusmärk (**=**) märgiks „suurem kui” (**\>**).</span><span class="sxs-lookup"><span data-stu-id="d911e-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Väljade Väärtus ja Tehtemärk muudetud väärtused](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="d911e-170">Salvestage ja sulgege Exceli parameetrifail.</span><span class="sxs-lookup"><span data-stu-id="d911e-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="d911e-171">Valige suvand **Laadi üles**, et salvestada Exceli parameetrifailis tehtud muudatused rakendusse Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="d911e-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="d911e-172">Kui määratud üksuse välja **Kokku saadaval** väärtus varudes on suurem kui 0 (null), siis test läbitakse, olenemata tegelikust vabast kaubavarust.</span><span class="sxs-lookup"><span data-stu-id="d911e-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="d911e-173">Koostaja logid</span><span class="sxs-lookup"><span data-stu-id="d911e-173">Generator logs</span></span>

<span data-ttu-id="d911e-174">See funktsioon loob kausta, mis sisaldab käivitatud testjuhtumite logisid.</span><span class="sxs-lookup"><span data-stu-id="d911e-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="d911e-175">Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.</span><span class="sxs-lookup"><span data-stu-id="d911e-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="d911e-176">Pärast testjuhtumite käivitamist leiate logifailid kaustast **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="d911e-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Kaust GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="d911e-178">Kui enne failis .config väärtuse muutmist olid olemas testjuhtumid, ei looda nende testjuhtumite kohta logisid, kuni loote uue testkäivitusfailid.</span><span class="sxs-lookup"><span data-stu-id="d911e-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Käsk Loo ainult testkäivitusfailid menüüs Uus](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="d911e-180">Hetktõmmis</span><span class="sxs-lookup"><span data-stu-id="d911e-180">Snapshot</span></span>

<span data-ttu-id="d911e-181">See funktsioon teeb kuvatõmmise etappidest, mis läbiti tegevuse salvestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="d911e-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="d911e-182">Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.</span><span class="sxs-lookup"><span data-stu-id="d911e-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="d911e-183">Kausta **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** luuakse iga käivitatud testjuhtumi kohta eraldi kaust.</span><span class="sxs-lookup"><span data-stu-id="d911e-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Testjuhtumi hetktõmmise kaust](./media/use_rsa_tool_12.png)

<span data-ttu-id="d911e-185">Igast kaustast leiate testjuhtumite käivitamisel läbitud etappide hetktõmmised.</span><span class="sxs-lookup"><span data-stu-id="d911e-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Hetktõmmiste failid](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="d911e-187">Määramine</span><span class="sxs-lookup"><span data-stu-id="d911e-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="d911e-188">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="d911e-188">Scenario</span></span>

1. <span data-ttu-id="d911e-189">Toote koostaja loob uue väljastatud toote.</span><span class="sxs-lookup"><span data-stu-id="d911e-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="d911e-190">Tootmisjuht käivitab tootmistellimuse, et jagada toote varud kaheks.</span><span class="sxs-lookup"><span data-stu-id="d911e-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="d911e-191">Tootmine alustab ja lõpetab tootmistellimuse ning kontrollib, kas vaba kaubavaru kogus on kaks tükki.</span><span class="sxs-lookup"><span data-stu-id="d911e-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="d911e-192">Müügimeeskond saab tellimuse neljale tükile uuele tootele.</span><span class="sxs-lookup"><span data-stu-id="d911e-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="d911e-193">Seega uuendab müügimeeskond netonõudeid dünaamilise plaani kaudu.</span><span class="sxs-lookup"><span data-stu-id="d911e-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="d911e-194">Kuna täiendav maht pole saadaval, määratakse tellimuse vaikepoliitika väärtusele „tegemise asemel osta”.</span><span class="sxs-lookup"><span data-stu-id="d911e-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="d911e-195">Seega luuakse plaanitud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="d911e-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="d911e-196">Ostja lisab hankija, kinnitab plaanitud ostutellimuse ja seejärel kinnitab ostutellimuse.</span><span class="sxs-lookup"><span data-stu-id="d911e-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="d911e-197">Kui ostetud kaubad saabuvad kauplusesse, otsib kaupluse töötaja välja seotud ostutellimuse ja võtab kaubad vastu.</span><span class="sxs-lookup"><span data-stu-id="d911e-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="d911e-198">Kuna tellimus on nüüd lõpule viidud, võib kaubad müügitellimuse suhtes komplekteerida ja pakkida.</span><span class="sxs-lookup"><span data-stu-id="d911e-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="d911e-199">Finantsosakond sisestab ostuarve ja müügiarve.</span><span class="sxs-lookup"><span data-stu-id="d911e-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="d911e-200">Järgmisel joonisel on näha selle stsenaariumi voog.</span><span class="sxs-lookup"><span data-stu-id="d911e-200">The following illustration shows the flow for this scenario.</span></span>

![Demostsenaariumi voog](./media/use_rsa_tool_14.png)

<span data-ttu-id="d911e-202">Järgmisel joonisel on näha selle stsenaariumi äriprotsessid RSAT-s.</span><span class="sxs-lookup"><span data-stu-id="d911e-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Demostsenaariumi äriprotsessid](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="d911e-204">Strateegia – peamised õppepunktid</span><span class="sxs-lookup"><span data-stu-id="d911e-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="d911e-205">Andmed</span><span class="sxs-lookup"><span data-stu-id="d911e-205">Data</span></span>

- <span data-ttu-id="d911e-206">Veenduge, et teil oleks olemas esindavad andmemahud (koopia tootmis- / kuldse konfiguratsiooni andmed ja migreeritud andmed).</span><span class="sxs-lookup"><span data-stu-id="d911e-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="d911e-207">Kui loote uued andmed tegevuse salvestaja kaudu, looge katsenimed, mis ei ole vastuolus olemasolevate nimedega (nt kasutage eesliidet nagu **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="d911e-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="d911e-208">Kasutage Azure’i ajapunktipõhist taastet, et käivitada uuesti testid muudes kui järgu 1 keskkondades.</span><span class="sxs-lookup"><span data-stu-id="d911e-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="d911e-209">Kuigi võite kasutada kordumatu kombinatsiooni loomiseks Exceli funktsioone **RANDOM** ja **NOW**, on panus arvestatavalt kõrge.</span><span class="sxs-lookup"><span data-stu-id="d911e-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="d911e-210">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="d911e-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="d911e-211">Ülesande salvestaja</span><span class="sxs-lookup"><span data-stu-id="d911e-211">Task recorder</span></span>

- <span data-ttu-id="d911e-212">Enne salvestamise alustamist määratlege stsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="d911e-213">Hästi hallatud projektil on eelmääratletud teststsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="d911e-214">Testjuhtumi loomiseks võtke arvesse, kui ennustatav on nende teststsenaariumite tulemus.</span><span class="sxs-lookup"><span data-stu-id="d911e-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="d911e-215">Tükeldage salvestisi, kui need tehakse eri rollides või kui enne järgmist etappi on ooteaeg või väline sündmus.</span><span class="sxs-lookup"><span data-stu-id="d911e-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="d911e-216">Vältige väärtuste valimist loendites.</span><span class="sxs-lookup"><span data-stu-id="d911e-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="d911e-217">Selle asemel kasutage tekstivorminguid, nt **FIFO**, **AudioRM** ja **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="d911e-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="d911e-218">Kui valite loendis, salvestatakse väärtuse asukoht loendis, mitte väärtus ise.</span><span class="sxs-lookup"><span data-stu-id="d911e-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="d911e-219">Kui sellele loendile üksuseid lisatakse, võib väärtuse asukoht muutuda.</span><span class="sxs-lookup"><span data-stu-id="d911e-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="d911e-220">Seega kasutab salvestus muud parameetrit ja see võib mõjutada ülejäänud stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="d911e-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="d911e-221">Mõelge mitme kasutaja käitumisele.</span><span class="sxs-lookup"><span data-stu-id="d911e-221">Think about multi-user behavior.</span></span> <span data-ttu-id="d911e-222">Näiteks ärge eeldage, et alati valitakse automaatselt teie äsja loodud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="d911e-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="d911e-223">Selle asemel kasutage filtrit õige tellimuse leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="d911e-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="d911e-224">Kasutage tegevuse salvestajas funktsiooni Kopeeri äsja loodud toote nime salvestamiseks, et seda saaks kasutada ühendatud testjuhtumites.</span><span class="sxs-lookup"><span data-stu-id="d911e-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="d911e-225">Kasutage tegevuse salvestajad funktsiooni Kinnita kontrollpunktide määramiseks, mis kontrollivad, kas etapid on käivitatud õigesti.</span><span class="sxs-lookup"><span data-stu-id="d911e-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="d911e-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="d911e-226">RSAT</span></span>

- <span data-ttu-id="d911e-227">Testi käivitamiseks teises ettevõttes saate muuta ettevõtte nime Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="d911e-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="d911e-228">Veenduge, et sätted ja andmed oleksid äsja valitud ettevõttes saadaval.</span><span class="sxs-lookup"><span data-stu-id="d911e-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="d911e-229">Saate muuta testkasutajat Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="d911e-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="d911e-230">Määrake testjuhtumit käivitava kasutaja meili ID.</span><span class="sxs-lookup"><span data-stu-id="d911e-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="d911e-231">Sellisel juhul saab testjuhtumit käivitada, kasutades määratud kasutaja turbeõigus.</span><span class="sxs-lookup"><span data-stu-id="d911e-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="d911e-232">Ootamiseks enne testi käivitamist saate määrata pausi Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="d911e-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="d911e-233">Seda pausi saab kasutada pakett-töös (nt kui töövoog tuleb käivitada enne, kui järgmist etappi saab läbida).</span><span class="sxs-lookup"><span data-stu-id="d911e-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="d911e-234">Täpsem skriptimine</span><span class="sxs-lookup"><span data-stu-id="d911e-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="d911e-235">CLI</span><span class="sxs-lookup"><span data-stu-id="d911e-235">CLI</span></span>

<span data-ttu-id="d911e-236">RSAT saab käivitada aknast **Käsuviip** või **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="d911e-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="d911e-237">Veenduge, et keskkonnamuutuja **TestRoot** oleks seatud RSAT installiteele.</span><span class="sxs-lookup"><span data-stu-id="d911e-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="d911e-238">(Avage Microsoft Windowsis suvand **Juhtpaneel**, valige **Süsteem ja turvalisus \> Süsteem \> Täpsemad süsteemisätted** ja seejärel valige suvand **Keskkonnamuutujad**.)</span><span class="sxs-lookup"><span data-stu-id="d911e-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="d911e-239">Avage administraatorina aken **Käsuviip** või **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="d911e-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="d911e-240">Navigeerige RSAT-i installikausta.</span><span class="sxs-lookup"><span data-stu-id="d911e-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="d911e-241">Esitage kõik käsud.</span><span class="sxs-lookup"><span data-stu-id="d911e-241">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="d911e-242">?</span><span class="sxs-lookup"><span data-stu-id="d911e-242">?</span></span> 
<span data-ttu-id="d911e-243">Kuvab kõigi saadaolevate käskude ja nende parameetrite spikri.</span><span class="sxs-lookup"><span data-stu-id="d911e-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="d911e-244">Valikulised parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="d911e-245">Kus ``[command]`` on üks allpool määratud käskudest.</span><span class="sxs-lookup"><span data-stu-id="d911e-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="d911e-246">about</span><span class="sxs-lookup"><span data-stu-id="d911e-246">about</span></span>
<span data-ttu-id="d911e-247">Kuvab praeguse versiooni.</span><span class="sxs-lookup"><span data-stu-id="d911e-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="d911e-248">cls</span><span class="sxs-lookup"><span data-stu-id="d911e-248">cls</span></span>
<span data-ttu-id="d911e-249">Tühjendab ekraani.</span><span class="sxs-lookup"><span data-stu-id="d911e-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="d911e-250">laadi alla</span><span class="sxs-lookup"><span data-stu-id="d911e-250">download</span></span>
<span data-ttu-id="d911e-251">Laadib alla määratud testjuhtumi manused väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="d911e-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="d911e-252">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d911e-253">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="d911e-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-254">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-254">Required parameters</span></span>
<span data-ttu-id="d911e-255">**``test_case_id``** Tähistab testjuhtumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="d911e-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="d911e-256">**``output_dir``** Tähistab väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="d911e-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="d911e-257">Kaust peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="d911e-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-258">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="d911e-259">redigeeri</span><span class="sxs-lookup"><span data-stu-id="d911e-259">edit</span></span>
<span data-ttu-id="d911e-260">Võimaldab teil avada parameetrite faili Exceli programmis ja seda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="d911e-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-261">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-261">Required parameters</span></span>
<span data-ttu-id="d911e-262">**``excel_file``** Peab sisaldama olemasoleva Exceli faili täielikku teed.</span><span class="sxs-lookup"><span data-stu-id="d911e-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-263">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="d911e-264">generate</span><span class="sxs-lookup"><span data-stu-id="d911e-264">generate</span></span>
<span data-ttu-id="d911e-265">Loob testkäivitamise ja parameetrifailid väljundkataloogi määratud testjuhtumi jaoks.</span><span class="sxs-lookup"><span data-stu-id="d911e-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="d911e-266">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d911e-267">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="d911e-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-268">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-268">Required parameters</span></span>
<span data-ttu-id="d911e-269">**``test_case_id``** Tähistab testjuhtumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="d911e-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="d911e-270">**``output_dir``** Tähistab väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="d911e-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="d911e-271">Kaust peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="d911e-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-272">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="d911e-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="d911e-273">generatederived</span></span>
<span data-ttu-id="d911e-274">Loob uue testjuhtumi, mis tulenevad esitatud testjuhtumist.</span><span class="sxs-lookup"><span data-stu-id="d911e-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="d911e-275">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d911e-276">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="d911e-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-277">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-277">Required parameters</span></span>
<span data-ttu-id="d911e-278">**``parent_test_case_id``** Tähistab ülemtestjuhtumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="d911e-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="d911e-279">**``test_plan_id``** Tähistab katseplaani ID-d.</span><span class="sxs-lookup"><span data-stu-id="d911e-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="d911e-280">**``test_suite_id``** Tähistab testkomplekti ID-d.</span><span class="sxs-lookup"><span data-stu-id="d911e-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-281">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="d911e-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="d911e-282">generatetestonly</span></span>
<span data-ttu-id="d911e-283">Loob väljundkataloogi määratud testjuhtumi jaoks ainult testkäivitamise faili.</span><span class="sxs-lookup"><span data-stu-id="d911e-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="d911e-284">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d911e-285">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="d911e-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-286">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-286">Required parameters</span></span>
<span data-ttu-id="d911e-287">**``test_case_id``** Tähistab testjuhtumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="d911e-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="d911e-288">**``output_dir``** Tähistab väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="d911e-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="d911e-289">Kaust peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="d911e-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-290">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="d911e-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="d911e-291">generatetestsuite</span></span>
<span data-ttu-id="d911e-292">Loob kõik väljundkataloogi määratud komplekti testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="d911e-293">Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid.</span><span class="sxs-lookup"><span data-stu-id="d911e-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="d911e-294">Kasutage veeru mis tahes väärtust parameetrina **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="d911e-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-295">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-295">Required parameters</span></span>
<span data-ttu-id="d911e-296">**``test_suite_name``** Tähistab testkomplekti nime.</span><span class="sxs-lookup"><span data-stu-id="d911e-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="d911e-297">**``output_dir``** Tähistab väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="d911e-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="d911e-298">Kaust peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="d911e-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-299">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="d911e-300">spikker</span><span class="sxs-lookup"><span data-stu-id="d911e-300">help</span></span>
<span data-ttu-id="d911e-301">Identne [?](####?)</span><span class="sxs-lookup"><span data-stu-id="d911e-301">Identical to the [?](####?)</span></span> <span data-ttu-id="d911e-302">käsuga</span><span class="sxs-lookup"><span data-stu-id="d911e-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="d911e-303">loend</span><span class="sxs-lookup"><span data-stu-id="d911e-303">list</span></span>
<span data-ttu-id="d911e-304">Loetleb kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="d911e-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="d911e-305">listtestplans</span></span>
<span data-ttu-id="d911e-306">Loetleb kõik saadaolevad katseplaanid.</span><span class="sxs-lookup"><span data-stu-id="d911e-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="d911e-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="d911e-307">listtestsuite</span></span>
<span data-ttu-id="d911e-308">Loetleb määratud testkomplekti testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="d911e-309">Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid.</span><span class="sxs-lookup"><span data-stu-id="d911e-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="d911e-310">Kasutage esimese veeru mis tahes väärtust parameetrina **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="d911e-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-311">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-311">Required parameters</span></span>
<span data-ttu-id="d911e-312">**``suite_name``** Soovitud komplekti nimi.</span><span class="sxs-lookup"><span data-stu-id="d911e-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-313">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="d911e-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="d911e-314">listtestsuitenames</span></span>
<span data-ttu-id="d911e-315">Loetleb kõik saadaolevad testkomplektid.</span><span class="sxs-lookup"><span data-stu-id="d911e-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="d911e-316">playback</span><span class="sxs-lookup"><span data-stu-id="d911e-316">playback</span></span>
<span data-ttu-id="d911e-317">Taasesitab Exceli faili abil testjuhtumi.</span><span class="sxs-lookup"><span data-stu-id="d911e-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-318">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-318">Required parameters</span></span>
<span data-ttu-id="d911e-319">**``excel_file``** Exceli faili täielik tee.</span><span class="sxs-lookup"><span data-stu-id="d911e-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="d911e-320">Fail peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="d911e-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="d911e-321">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="d911e-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="d911e-322">playbackbyid</span></span>
<span data-ttu-id="d911e-323">Taasesitab korraga mitu testjuhtumit.</span><span class="sxs-lookup"><span data-stu-id="d911e-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="d911e-324">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="d911e-325">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="d911e-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-326">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-326">Required parameters</span></span>
<span data-ttu-id="d911e-327">**``test_case_id1``** Olemasoleva testjuhtumi ID.</span><span class="sxs-lookup"><span data-stu-id="d911e-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="d911e-328">**``test_case_id2``** Olemasoleva testjuhtumi ID.</span><span class="sxs-lookup"><span data-stu-id="d911e-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="d911e-329">**``test_case_idN``** Olemasoleva testjuhtumi ID.</span><span class="sxs-lookup"><span data-stu-id="d911e-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="d911e-330">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="d911e-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="d911e-331">playbackmany</span></span>
<span data-ttu-id="d911e-332">Taasesitab korraga mitu testjuhtumit, kasutades Exceli faile.</span><span class="sxs-lookup"><span data-stu-id="d911e-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-333">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-333">Required parameters</span></span>
<span data-ttu-id="d911e-334">**``excel_file1``** Exceli faili täielik tee.</span><span class="sxs-lookup"><span data-stu-id="d911e-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="d911e-335">Fail peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="d911e-335">File must exist.</span></span>  
<span data-ttu-id="d911e-336">**``excel_file2``** Exceli faili täielik tee.</span><span class="sxs-lookup"><span data-stu-id="d911e-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="d911e-337">Fail peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="d911e-337">File must exist.</span></span>  
<span data-ttu-id="d911e-338">**``excel_fileN``** Exceli faili täielik tee.</span><span class="sxs-lookup"><span data-stu-id="d911e-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="d911e-339">Fail peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="d911e-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="d911e-340">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="d911e-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="d911e-341">playbacksuite</span></span>
<span data-ttu-id="d911e-342">Taasesitab konkreetse testkomplekti kõik testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="d911e-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="d911e-343">Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid.</span><span class="sxs-lookup"><span data-stu-id="d911e-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="d911e-344">Kasutage esimese veeru mis tahes väärtust parameetrina **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="d911e-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-345">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-345">Required parameters</span></span>
<span data-ttu-id="d911e-346">**``suite_name``** Soovitud komplekti nimi.</span><span class="sxs-lookup"><span data-stu-id="d911e-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-347">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="d911e-348">quit</span><span class="sxs-lookup"><span data-stu-id="d911e-348">quit</span></span>
<span data-ttu-id="d911e-349">Sulgeb rakenduse.</span><span class="sxs-lookup"><span data-stu-id="d911e-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="d911e-350">upload</span><span class="sxs-lookup"><span data-stu-id="d911e-350">upload</span></span>
<span data-ttu-id="d911e-351">Laadib üles kõik määratud testkomplekti või testjuhtumitesse kuuluvad failid.</span><span class="sxs-lookup"><span data-stu-id="d911e-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="d911e-352">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-352">Required parameters</span></span>
<span data-ttu-id="d911e-353">**``suite_name``** Kõik määratud testkomplekti kuuluvad failid laaditakse üles.</span><span class="sxs-lookup"><span data-stu-id="d911e-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="d911e-354">**``testcase_id``** Kõik määratud testjuhtumi(te)sse kuuluvad failid laaditakse üles.</span><span class="sxs-lookup"><span data-stu-id="d911e-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-355">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="d911e-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="d911e-356">uploadrecording</span></span>
<span data-ttu-id="d911e-357">Laadib üles ainult määratud testjuhtumitesse kuuluva salvestamisfaili.</span><span class="sxs-lookup"><span data-stu-id="d911e-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="d911e-358">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="d911e-358">Required parameters</span></span>
<span data-ttu-id="d911e-359">**``testcase_id``** Määratud testjuhtumitesse kuuluv salvestamisfail laaditakse üles.</span><span class="sxs-lookup"><span data-stu-id="d911e-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="d911e-360">Näited</span><span class="sxs-lookup"><span data-stu-id="d911e-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="d911e-361">usage</span><span class="sxs-lookup"><span data-stu-id="d911e-361">usage</span></span>
<span data-ttu-id="d911e-362">Näitab selle rakenduse kahte käivitamisviisi: üks kasutab vaikimisi seadistusfaili, teine esitab seadistusfaili.</span><span class="sxs-lookup"><span data-stu-id="d911e-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="d911e-363">Windows PowerShelli näited</span><span class="sxs-lookup"><span data-stu-id="d911e-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="d911e-364">Testjuhtumi käivitamine tsüklis</span><span class="sxs-lookup"><span data-stu-id="d911e-364">Run a test case in a loop</span></span>

<span data-ttu-id="d911e-365">Teil on testskript, mis loob uue kliendi.</span><span class="sxs-lookup"><span data-stu-id="d911e-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="d911e-366">Skriptimise kaudu saab seda testjuhtumis käivitada tsüklis, muutes enne iga iteratsiooni käivitamist järgmised andmed juhuslikuks.</span><span class="sxs-lookup"><span data-stu-id="d911e-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="d911e-367">Kliendi ID</span><span class="sxs-lookup"><span data-stu-id="d911e-367">Customer ID</span></span>
- <span data-ttu-id="d911e-368">Kliendi nimi</span><span class="sxs-lookup"><span data-stu-id="d911e-368">Customer name</span></span>
- <span data-ttu-id="d911e-369">Kliendi aadress</span><span class="sxs-lookup"><span data-stu-id="d911e-369">Customer address</span></span>

<span data-ttu-id="d911e-370">Kliendi ID on vormingus *ATCUS\<number\>*, kus \<number\> on väärtus vahemikus **000000001** kuni **999999999**.</span><span class="sxs-lookup"><span data-stu-id="d911e-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="d911e-371">Järgmises näites kasutatakse üht parameetrit, **alusta**, esimese kasutatud numbri määramiseks.</span><span class="sxs-lookup"><span data-stu-id="d911e-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="d911e-372">See kasutab teist parameetrit, **nr**, loodavate klientide arvu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="d911e-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="d911e-373">Iga iteratsiooni kohta muudetakse Exceli parameetrifailis parameetreid, kasutades funktsiooni UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="d911e-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="d911e-374">Seejärel käivitatakse RSAT käsurida funktsioonis RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="d911e-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="d911e-375">Avage Microsoft Windows PowerShell Integrated Scripting Environment (ISE) haldusrežiimis ja kleepige järgmine kood aknasse nimega **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="d911e-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="d911e-376">Microsoft Dynamics 365 andmetest sõltuva skripti käivitamine</span><span class="sxs-lookup"><span data-stu-id="d911e-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="d911e-377">Järgmises näites kasutatakse kutset Open Data Protocol (OData) ostutellimuse tellimuse oleku leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="d911e-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="d911e-378">Kui olek ei ole **arveldatud**, võite näiteks käivitada RSAT testjuhtumi, mis arve sisestab.</span><span class="sxs-lookup"><span data-stu-id="d911e-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
