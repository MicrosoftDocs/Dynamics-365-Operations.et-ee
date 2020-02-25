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
ms.openlocfilehash: 026d1d743b5150f152ef70aa642dcf6841a4e398
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025800"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="01ad3-104">Tööriista Regression suite automation tool kasutamise õppetükk</span><span class="sxs-lookup"><span data-stu-id="01ad3-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="01ad3-105">Kasutage Interneti-brauseri tööriistu selle lehe allalaadimiseks ja salvestamiseks PDF-vormingus.</span><span class="sxs-lookup"><span data-stu-id="01ad3-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="01ad3-106">Selles õppetükis tutvustatakse tööriista Regression suite automation tool (RSAT) täpsemaid funktsioone, see hõlmab demomääramist ning kirjeldab strateegiat ja peamisi õppekohti.</span><span class="sxs-lookup"><span data-stu-id="01ad3-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="01ad3-107">RSAT / tegevuse salvestaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="01ad3-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="01ad3-108">Välja väärtuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="01ad3-108">Validate a field value</span></span>

<span data-ttu-id="01ad3-109">Teavet selle funktsiooni kohta vaadake teemast [Uue tegevuse salvestise loomine, millel on valideerimise funktsioon](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="01ad3-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="01ad3-110">Salvestatud muutuja</span><span class="sxs-lookup"><span data-stu-id="01ad3-110">Saved variable</span></span>

<span data-ttu-id="01ad3-111">Teavet selle funktsiooni kohta vaadake teemast [Olemasoleva tegevuse salvestise muutmine salvestatud muutuja loomiseks](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="01ad3-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="01ad3-112">Tuletatud testjuhtum</span><span class="sxs-lookup"><span data-stu-id="01ad3-112">Derived test case</span></span>

1. <span data-ttu-id="01ad3-113">Avage Regression Suite Automation Tool (RSAT) ja valige mõlemad loodud testjuhtumid jaotisest [Tööriista Regression Suite Automation tool seadistamise ja installimise õpetus](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="01ad3-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="01ad3-114">Valige suvandid **Uus \> Loo tuletatud testjuhtum**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-114">Select **New \> Create derived test case**.</span></span>

    ![Tuletatud testjuhtumi käsu loomine menüüs Uus](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="01ad3-116">Saate teate, et tuletatud testjuhtum luuakse iga valitud testjuhtumi kohta praeguses testkomplektis ja igal tuletatud testjuhtumil on oma koopia Exceli parameetrifailist.</span><span class="sxs-lookup"><span data-stu-id="01ad3-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="01ad3-117">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="01ad3-118">Kui käivitate tuletatud testjuhtumi, kasutab see ülemtestjuhtumi tegevuse salvestist ja oma koopiat Exceli parameetrifailist.</span><span class="sxs-lookup"><span data-stu-id="01ad3-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="01ad3-119">Nii saate käivitada sama testi eri parameetritega, ilma et peaksite säilitama rohkem kui ühe tegevuse salvestise.</span><span class="sxs-lookup"><span data-stu-id="01ad3-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="01ad3-120">Tuletatud testjuhtum ei pea olema osa samast testkomplektist kui selle ülemtestjuhtum.</span><span class="sxs-lookup"><span data-stu-id="01ad3-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Teateaken](./media/use_rsa_tool_02.png)

    <span data-ttu-id="01ad3-122">Luuakse kaks täiendavat testjuhtumit ja nende jaoks valitakse märkeruut **Tuletatud?**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Loodud tuletatud testjuhtumid](./media/use_rsa_tool_03.png)

    <span data-ttu-id="01ad3-124">Tuletatud testjuhtum luuakse automaatselt rakenduses Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="01ad3-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="01ad3-125">See on testjuhtumi **Uue toote loomine** allüksus ja see märgistatakse spetsiaalse märksõnaga: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="01ad3-126">Need testjuhtumid lisatakse ka automaatselt katseplaanile rakenduses Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="01ad3-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Märksõna RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="01ad3-128">Kui tuletatud testjuhtumid pole mingil põhjusel õiges järjekorras, minge rakendusse Azure DevOps ja muutke testjuhtumite järjekorda testkomplektis, et RSAT saaks need käivitada õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="01ad3-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="01ad3-129">Valige tuletatud testjuhtumid ja seejärel valige nupp **Redigeeri** vastavate Exceli parameetrifailide avamiseks.</span><span class="sxs-lookup"><span data-stu-id="01ad3-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="01ad3-130">Redigeerige neid Exceli parameetrifaile samamoodi, nagu redigeerisite ülemfaile.</span><span class="sxs-lookup"><span data-stu-id="01ad3-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="01ad3-131">Teisisõnu veenduge, et toote ID oleks seadistatud nii, et see luuakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="01ad3-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="01ad3-132">Peale selle veenduge, et salvestatud muutuja kopeeritakse asjakohastesse väljadesse.</span><span class="sxs-lookup"><span data-stu-id="01ad3-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="01ad3-133">Mõlema Exceli parameetrifaili vahekaardil **Üldine** uuendage väli **Ettevõte** väärtusele **USSI**, et tuletatud testjuhtumid käivitatakse muu juriidilise isiku suhtes kui ülemtestjuhtum.</span><span class="sxs-lookup"><span data-stu-id="01ad3-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="01ad3-134">Testjuhtumite käivitamiseks konkreetse kasutaja (või konkreetse kasutajaga seotud rolli) suhtes saate uuendada välja **Testkasutaja** väärtust.</span><span class="sxs-lookup"><span data-stu-id="01ad3-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="01ad3-135">Valige käsk **Käivita** ja kontrollige, kas toode luuakse nii USMF-i juriidilises isikus kui ka USSI juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="01ad3-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="01ad3-136">Teatiste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="01ad3-136">Validate notifications</span></span>

<span data-ttu-id="01ad3-137">Seda funktsiooni saab kasutada ka kontrollimaks, kas tegevus toimus.</span><span class="sxs-lookup"><span data-stu-id="01ad3-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="01ad3-138">Näiteks kui luuakse tootmistellimus, seda hinnatakse ja see seejärel käivitatakse, kuvab rakendus teate „Tootmine – alusta”, mis annab teada, et tootmistellimust on alustatud.</span><span class="sxs-lookup"><span data-stu-id="01ad3-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Teatis Tootmine – alusta](./media/use_rsa_tool_05.png)

<span data-ttu-id="01ad3-140">Saate selle teate kinnitada läbi RSAT, sisestades teate teksti vastava salvestise Exceli parameetrifaili vahekaardile **Teate kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Vahekaart Teate kinnitamine](./media/use_rsa_tool_06.png)

<span data-ttu-id="01ad3-142">Pärast testjuhtumi käivitamist võrreldakse teadet Exceli parameetrifailis kuvatava teatega.</span><span class="sxs-lookup"><span data-stu-id="01ad3-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="01ad3-143">Kui teated ei kattu, siis testjuhtum nurjub.</span><span class="sxs-lookup"><span data-stu-id="01ad3-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="01ad3-144">Võite sisestada Exceli parameetrifaili vahekaardile **Teate kinnitamine** rohkem kui ühe teate.</span><span class="sxs-lookup"><span data-stu-id="01ad3-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="01ad3-145">Teated võivad olla ka tõrke- või hoiatusteated, mitte teavitavad teated.</span><span class="sxs-lookup"><span data-stu-id="01ad3-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="01ad3-146">Väärtuste kinnitamine tehtemärke kasutades</span><span class="sxs-lookup"><span data-stu-id="01ad3-146">Validate values by using operators</span></span>

<span data-ttu-id="01ad3-147">Eelmistes RSAT versioonides saite väärtusi kinnitada ainult siis, kui kontrollväärtus oli võrdne eeldatava väärtusega.</span><span class="sxs-lookup"><span data-stu-id="01ad3-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="01ad3-148">Uue funktsiooniga saate kinnitada, kas muutuja ei ole konkreetse väärtusega võrdne, on sellest väiksem või sellest suurem.</span><span class="sxs-lookup"><span data-stu-id="01ad3-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="01ad3-149">Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="01ad3-150">Exceli parameetrifaili ilmub uus väli **Tehtemärk**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="01ad3-151">Kui olete kasutanud RSAT vanemat versiooni, peate looma uued Exceli parameetrifailid.</span><span class="sxs-lookup"><span data-stu-id="01ad3-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Väli Tehtemärk](./media/use_rsa_tool_07.png)

<span data-ttu-id="01ad3-153">Järgmises näites näete, kuidas kasutada seda funktsiooni kinnitamaks, kas vaba kaubavaru väärtus on suurem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="01ad3-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="01ad3-154">Looge ettevõtte **USMF** demoandmetes tegevuse salvestis, mis sisaldab järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="01ad3-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="01ad3-155">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="01ad3-156">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="01ad3-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="01ad3-157">Näiteks filtreerige välja **Kaubakood** väärtuse **1000** järgi.</span><span class="sxs-lookup"><span data-stu-id="01ad3-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="01ad3-158">Valige **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="01ad3-159">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="01ad3-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="01ad3-160">Näiteks filtreerige välja **Tegevuskoht** väärtuse **1** järgi.</span><span class="sxs-lookup"><span data-stu-id="01ad3-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="01ad3-161">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="01ad3-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="01ad3-162">Kinnitage, et välja **Kokku saadaval** väärtus on **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="01ad3-163">Salvestage tegevuse salvestis LCS-is BPM-i teeki ja sünkroonige see rakendusega Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="01ad3-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="01ad3-164">Lisage testjuhtum katseplaani ja laadige testjuhtum RSAT-sse.</span><span class="sxs-lookup"><span data-stu-id="01ad3-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="01ad3-165">Avage Exceli parameetrifail.</span><span class="sxs-lookup"><span data-stu-id="01ad3-165">Open the Excel parameter file.</span></span> <span data-ttu-id="01ad3-166">Vahekaardil **InventOnhandItem** näete jaotist **Kinnita InventOnhandItem**, mis sisaldab välja **Tehtemärk**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Väli Tehtemärk](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="01ad3-168">Kinnitamaks, kas vaba kaubavaru on alati rohkem kui 0, muutke välja **Väärtus** väärtuselt **411** väärtusele **0** ja väljal **Tehtemärk** võrdusmärk (**=**) märgiks „suurem kui” (**\>**).</span><span class="sxs-lookup"><span data-stu-id="01ad3-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Väljade Väärtus ja Tehtemärk muudetud väärtused](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="01ad3-170">Salvestage ja sulgege Exceli parameetrifail.</span><span class="sxs-lookup"><span data-stu-id="01ad3-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="01ad3-171">Valige suvand **Laadi üles**, et salvestada Exceli parameetrifailis tehtud muudatused rakendusse Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="01ad3-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="01ad3-172">Kui määratud üksuse välja **Kokku saadaval** väärtus varudes on suurem kui 0 (null), siis test läbitakse, olenemata tegelikust vabast kaubavarust.</span><span class="sxs-lookup"><span data-stu-id="01ad3-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="01ad3-173">Koostaja logid</span><span class="sxs-lookup"><span data-stu-id="01ad3-173">Generator logs</span></span>

<span data-ttu-id="01ad3-174">See funktsioon loob kausta, mis sisaldab käivitatud testjuhtumite logisid.</span><span class="sxs-lookup"><span data-stu-id="01ad3-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="01ad3-175">Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="01ad3-176">Pärast testjuhtumite käivitamist leiate logifailid kaustast **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Kaust GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="01ad3-178">Kui enne failis .config väärtuse muutmist olid olemas testjuhtumid, ei looda nende testjuhtumite kohta logisid, kuni loote uue testkäivitusfailid.</span><span class="sxs-lookup"><span data-stu-id="01ad3-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Käsk Loo ainult testkäivitusfailid menüüs Uus](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="01ad3-180">Hetktõmmis</span><span class="sxs-lookup"><span data-stu-id="01ad3-180">Snapshot</span></span>

<span data-ttu-id="01ad3-181">See funktsioon teeb kuvatõmmise etappidest, mis läbiti tegevuse salvestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="01ad3-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="01ad3-182">Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="01ad3-183">Kausta **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** luuakse iga käivitatud testjuhtumi kohta eraldi kaust.</span><span class="sxs-lookup"><span data-stu-id="01ad3-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Testjuhtumi hetktõmmise kaust](./media/use_rsa_tool_12.png)

<span data-ttu-id="01ad3-185">Igast kaustast leiate testjuhtumite käivitamisel läbitud etappide hetktõmmised.</span><span class="sxs-lookup"><span data-stu-id="01ad3-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Hetktõmmiste failid](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="01ad3-187">Määramine</span><span class="sxs-lookup"><span data-stu-id="01ad3-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="01ad3-188">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="01ad3-188">Scenario</span></span>

1. <span data-ttu-id="01ad3-189">Toote koostaja loob uue väljastatud toote.</span><span class="sxs-lookup"><span data-stu-id="01ad3-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="01ad3-190">Tootmisjuht käivitab tootmistellimuse, et jagada toote varud kaheks.</span><span class="sxs-lookup"><span data-stu-id="01ad3-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="01ad3-191">Tootmine alustab ja lõpetab tootmistellimuse ning kontrollib, kas vaba kaubavaru kogus on kaks tükki.</span><span class="sxs-lookup"><span data-stu-id="01ad3-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="01ad3-192">Müügimeeskond saab tellimuse neljale tükile uuele tootele.</span><span class="sxs-lookup"><span data-stu-id="01ad3-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="01ad3-193">Seega uuendab müügimeeskond netonõudeid dünaamilise plaani kaudu.</span><span class="sxs-lookup"><span data-stu-id="01ad3-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="01ad3-194">Kuna täiendav maht pole saadaval, määratakse tellimuse vaikepoliitika väärtusele „tegemise asemel osta”.</span><span class="sxs-lookup"><span data-stu-id="01ad3-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="01ad3-195">Seega luuakse plaanitud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="01ad3-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="01ad3-196">Ostja lisab hankija, kinnitab plaanitud ostutellimuse ja seejärel kinnitab ostutellimuse.</span><span class="sxs-lookup"><span data-stu-id="01ad3-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="01ad3-197">Kui ostetud kaubad saabuvad kauplusesse, otsib kaupluse töötaja välja seotud ostutellimuse ja võtab kaubad vastu.</span><span class="sxs-lookup"><span data-stu-id="01ad3-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="01ad3-198">Kuna tellimus on nüüd lõpule viidud, võib kaubad müügitellimuse suhtes komplekteerida ja pakkida.</span><span class="sxs-lookup"><span data-stu-id="01ad3-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="01ad3-199">Finantsosakond sisestab ostuarve ja müügiarve.</span><span class="sxs-lookup"><span data-stu-id="01ad3-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="01ad3-200">Järgmisel joonisel on näha selle stsenaariumi voog.</span><span class="sxs-lookup"><span data-stu-id="01ad3-200">The following illustration shows the flow for this scenario.</span></span>

![Demostsenaariumi voog](./media/use_rsa_tool_14.png)

<span data-ttu-id="01ad3-202">Järgmisel joonisel on näha selle stsenaariumi äriprotsessid RSAT-s.</span><span class="sxs-lookup"><span data-stu-id="01ad3-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Demostsenaariumi äriprotsessid](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="01ad3-204">Strateegia – peamised õppepunktid</span><span class="sxs-lookup"><span data-stu-id="01ad3-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="01ad3-205">Andmed</span><span class="sxs-lookup"><span data-stu-id="01ad3-205">Data</span></span>

- <span data-ttu-id="01ad3-206">Veenduge, et teil oleks olemas esindavad andmemahud (koopia tootmis- / kuldse konfiguratsiooni andmed ja migreeritud andmed).</span><span class="sxs-lookup"><span data-stu-id="01ad3-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="01ad3-207">Kui loote uued andmed tegevuse salvestaja kaudu, looge katsenimed, mis ei ole vastuolus olemasolevate nimedega (nt kasutage eesliidet nagu **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="01ad3-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="01ad3-208">Kasutage Azure’i ajapunktipõhist taastet, et käivitada uuesti testid muudes kui järgu 1 keskkondades.</span><span class="sxs-lookup"><span data-stu-id="01ad3-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="01ad3-209">Kuigi võite kasutada kordumatu kombinatsiooni loomiseks Exceli funktsioone **RANDOM** ja **NOW**, on panus arvestatavalt kõrge.</span><span class="sxs-lookup"><span data-stu-id="01ad3-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="01ad3-210">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="01ad3-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="01ad3-211">Ülesande salvestaja</span><span class="sxs-lookup"><span data-stu-id="01ad3-211">Task recorder</span></span>

- <span data-ttu-id="01ad3-212">Enne salvestamise alustamist määratlege stsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="01ad3-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="01ad3-213">Hästi hallatud projektil on eelmääratletud teststsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="01ad3-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="01ad3-214">Testjuhtumi loomiseks võtke arvesse, kui ennustatav on nende teststsenaariumite tulemus.</span><span class="sxs-lookup"><span data-stu-id="01ad3-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="01ad3-215">Tükeldage salvestisi, kui need tehakse eri rollides või kui enne järgmist etappi on ooteaeg või väline sündmus.</span><span class="sxs-lookup"><span data-stu-id="01ad3-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="01ad3-216">Vältige väärtuste valimist loendites.</span><span class="sxs-lookup"><span data-stu-id="01ad3-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="01ad3-217">Selle asemel kasutage tekstivorminguid, nt **FIFO**, **AudioRM** ja **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="01ad3-218">Kui valite loendis, salvestatakse väärtuse asukoht loendis, mitte väärtus ise.</span><span class="sxs-lookup"><span data-stu-id="01ad3-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="01ad3-219">Kui sellele loendile üksuseid lisatakse, võib väärtuse asukoht muutuda.</span><span class="sxs-lookup"><span data-stu-id="01ad3-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="01ad3-220">Seega kasutab salvestus muud parameetrit ja see võib mõjutada ülejäänud stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="01ad3-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="01ad3-221">Mõelge mitme kasutaja käitumisele.</span><span class="sxs-lookup"><span data-stu-id="01ad3-221">Think about multi-user behavior.</span></span> <span data-ttu-id="01ad3-222">Näiteks ärge eeldage, et alati valitakse automaatselt teie äsja loodud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="01ad3-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="01ad3-223">Selle asemel kasutage filtrit õige tellimuse leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="01ad3-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="01ad3-224">Kasutage tegevuse salvestajas funktsiooni Kopeeri äsja loodud toote nime salvestamiseks, et seda saaks kasutada ühendatud testjuhtumites.</span><span class="sxs-lookup"><span data-stu-id="01ad3-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="01ad3-225">Kasutage tegevuse salvestajad funktsiooni Kinnita kontrollpunktide määramiseks, mis kontrollivad, kas etapid on käivitatud õigesti.</span><span class="sxs-lookup"><span data-stu-id="01ad3-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="01ad3-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="01ad3-226">RSAT</span></span>

- <span data-ttu-id="01ad3-227">Testi käivitamiseks teises ettevõttes saate muuta ettevõtte nime Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="01ad3-228">Veenduge, et sätted ja andmed oleksid äsja valitud ettevõttes saadaval.</span><span class="sxs-lookup"><span data-stu-id="01ad3-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="01ad3-229">Saate muuta testkasutajat Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="01ad3-230">Määrake testjuhtumit käivitava kasutaja meili ID.</span><span class="sxs-lookup"><span data-stu-id="01ad3-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="01ad3-231">Sellisel juhul saab testjuhtumit käivitada, kasutades määratud kasutaja turbeõigus.</span><span class="sxs-lookup"><span data-stu-id="01ad3-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="01ad3-232">Ootamiseks enne testi käivitamist saate määrata pausi Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="01ad3-233">Seda pausi saab kasutada pakett-töös (nt kui töövoog tuleb käivitada enne, kui järgmist etappi saab läbida).</span><span class="sxs-lookup"><span data-stu-id="01ad3-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="01ad3-234">Täpsem skriptimine</span><span class="sxs-lookup"><span data-stu-id="01ad3-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="01ad3-235">Käsurida</span><span class="sxs-lookup"><span data-stu-id="01ad3-235">Command line</span></span>

<span data-ttu-id="01ad3-236">RSAT-d saab käivitada aknast **Käsuviip**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="01ad3-237">Veenduge, et keskkonnamuutuja **TestRoot** oleks seatud RSAT installiteele.</span><span class="sxs-lookup"><span data-stu-id="01ad3-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="01ad3-238">(Avage Microsoft Windowsis suvand **Juhtpaneel**, valige **Süsteem ja turvalisus \> Süsteem \> Täpsemad süsteemisätted** ja seejärel valige suvand **Keskkonnamuutujad**.)</span><span class="sxs-lookup"><span data-stu-id="01ad3-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="01ad3-239">Avage administraatorina aken **Käsuviip**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="01ad3-240">Käivitage tööriist installikaustast.</span><span class="sxs-lookup"><span data-stu-id="01ad3-240">Run the tool from the installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="01ad3-241">Esitage kõik käsud.</span><span class="sxs-lookup"><span data-stu-id="01ad3-241">List all commands.</span></span>

    ```Console
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

### <a name="windows-powershell-examples"></a><span data-ttu-id="01ad3-242">Windows PowerShelli näited</span><span class="sxs-lookup"><span data-stu-id="01ad3-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="01ad3-243">Testjuhtumi käivitamine tsüklis</span><span class="sxs-lookup"><span data-stu-id="01ad3-243">Run a test case in a loop</span></span>

<span data-ttu-id="01ad3-244">Teil on testskript, mis loob uue kliendi.</span><span class="sxs-lookup"><span data-stu-id="01ad3-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="01ad3-245">Skriptimise kaudu saab seda testjuhtumis käivitada tsüklis, muutes enne iga iteratsiooni käivitamist järgmised andmed juhuslikuks.</span><span class="sxs-lookup"><span data-stu-id="01ad3-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="01ad3-246">Kliendi ID</span><span class="sxs-lookup"><span data-stu-id="01ad3-246">Customer ID</span></span>
- <span data-ttu-id="01ad3-247">Kliendi nimi</span><span class="sxs-lookup"><span data-stu-id="01ad3-247">Customer name</span></span>
- <span data-ttu-id="01ad3-248">Kliendi aadress</span><span class="sxs-lookup"><span data-stu-id="01ad3-248">Customer address</span></span>

<span data-ttu-id="01ad3-249">Kliendi ID on vormingus *ATCUS\<number\>*, kus \<number\> on väärtus vahemikus **000000001** kuni **999999999**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="01ad3-250">Järgmises näites kasutatakse üht parameetrit, **alusta**, esimese kasutatud numbri määramiseks.</span><span class="sxs-lookup"><span data-stu-id="01ad3-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="01ad3-251">See kasutab teist parameetrit, **nr**, loodavate klientide arvu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="01ad3-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="01ad3-252">Iga iteratsiooni kohta muudetakse Exceli parameetrifailis parameetreid, kasutades funktsiooni UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="01ad3-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="01ad3-253">Seejärel käivitatakse RSAT käsurida funktsioonis RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="01ad3-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="01ad3-254">Avage Microsoft Windows PowerShell Integrated Scripting Environment (ISE) haldusrežiimis ja kleepige järgmine kood aknasse nimega **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="01ad3-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="01ad3-255">Microsoft Dynamics 365 andmetest sõltuva skripti käivitamine</span><span class="sxs-lookup"><span data-stu-id="01ad3-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="01ad3-256">Järgmises näites kasutatakse kutset Open Data Protocol (OData) ostutellimuse tellimuse oleku leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="01ad3-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="01ad3-257">Kui olek ei ole **arveldatud**, võite näiteks käivitada RSAT testjuhtumi, mis arve sisestab.</span><span class="sxs-lookup"><span data-stu-id="01ad3-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
