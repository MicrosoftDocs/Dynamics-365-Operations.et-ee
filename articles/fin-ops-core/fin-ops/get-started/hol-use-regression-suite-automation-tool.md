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
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="036ca-104">Tööriista Regression suite automation tool kasutamise õppetükk</span><span class="sxs-lookup"><span data-stu-id="036ca-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="036ca-105">Kasutage Interneti-brauseri tööriistu selle lehe allalaadimiseks ja salvestamiseks PDF-vormingus.</span><span class="sxs-lookup"><span data-stu-id="036ca-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="036ca-106">Selles õppetükis tutvustatakse tööriista Regression suite automation tool (RSAT) täpsemaid funktsioone, see hõlmab demomääramist ning kirjeldab strateegiat ja peamisi õppekohti.</span><span class="sxs-lookup"><span data-stu-id="036ca-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="036ca-107">RSAT-i ja tegevuse salvestaja olulised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="036ca-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="036ca-108">Välja väärtuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="036ca-108">Validate a field value</span></span>

<span data-ttu-id="036ca-109">RSAT võimaldab teil lisada oma testjuhtumisse kinnitamistoiminguid, et kinnitada eeldatavaid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="036ca-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="036ca-110">Selle funktsiooni kohta lisateabe saamiseks vaadake artiklit [Eeldatavate väärtuste valideerimine](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="036ca-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="036ca-111">Järgmises näites näete, kuidas kasutada seda funktsiooni kinnitamaks, kas vaba kaubavaru väärtus on suurem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="036ca-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="036ca-112">Looge ettevõtte **USMF** demoandmetes tegevuse salvestis, mis sisaldab järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="036ca-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="036ca-113">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="036ca-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="036ca-114">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="036ca-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="036ca-115">Näiteks filtreerige välja **Kaubakood** väärtuse **1000** järgi.</span><span class="sxs-lookup"><span data-stu-id="036ca-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="036ca-116">Valige **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="036ca-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="036ca-117">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="036ca-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="036ca-118">Näiteks filtreerige välja **Tegevuskoht** väärtuse **1** järgi.</span><span class="sxs-lookup"><span data-stu-id="036ca-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="036ca-119">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="036ca-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="036ca-120">Kinnitage, et välja **Kokku saadaval** väärtus on **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="036ca-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="036ca-121">Salvestage tegevuse salvestis ja lisage see oma testi juhtumile Azure DevOpsis.</span><span class="sxs-lookup"><span data-stu-id="036ca-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="036ca-122">Lisage testjuhtum katseplaani ja laadige testjuhtum RSAT-sse.</span><span class="sxs-lookup"><span data-stu-id="036ca-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="036ca-123">Avage Exceli parameetrifail.</span><span class="sxs-lookup"><span data-stu-id="036ca-123">Open the Excel parameter file.</span></span> <span data-ttu-id="036ca-124">Vahekaardil **InventOnhandItem** näete jaotist **Kinnita InventOnhandItem**, mis sisaldab välja **Tehtemärk**.</span><span class="sxs-lookup"><span data-stu-id="036ca-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Väli Tehtemärk](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="036ca-126">Kinnitamaks, kas vaba kaubavaru on alati rohkem kui 0, muutke välja **Väärtus** väärtuselt **411** väärtusele **0** ja väljal **Tehtemärk** võrdusmärk (**=**) märgiks „suurem kui” (**\>**).</span><span class="sxs-lookup"><span data-stu-id="036ca-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Väljade Väärtus ja Tehtemärk muudetud väärtused](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="036ca-128">Salvestage ja sulgege Exceli parameetrifail.</span><span class="sxs-lookup"><span data-stu-id="036ca-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="036ca-129">Valige suvand **Laadi üles**, et salvestada Exceli parameetrifailis tehtud muudatused rakendusse Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="036ca-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="036ca-130">Kui määratud üksuse välja **Kokku saadaval** väärtus varudes on suurem kui 0 (null), siis test läbitakse, olenemata tegelikust vabast kaubavarust.</span><span class="sxs-lookup"><span data-stu-id="036ca-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="036ca-131">Salvestatud muutujad ja testjuhtumite aheltöötlus</span><span class="sxs-lookup"><span data-stu-id="036ca-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="036ca-132">Üks RSAT põhifunktsioone on testjuhtumite aheltöötlus (test suudab edastada muutujaid teistele testidele).</span><span class="sxs-lookup"><span data-stu-id="036ca-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="036ca-133">Lisateabe saamiseks vt artiklit [Muutujate kopeerimine keti testjuhtumitele](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="036ca-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="036ca-134">Tuletatud testjuhtum</span><span class="sxs-lookup"><span data-stu-id="036ca-134">Derived test case</span></span>

<span data-ttu-id="036ca-135">RSAT võimaldab kasutada sama tegevuse salvestist mitme testjuhtumi korral, võimaldades ülesandel töötada erinevate andmete konfiguratsioonidega.</span><span class="sxs-lookup"><span data-stu-id="036ca-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="036ca-136">Lisateabe saamiseks vt artiklit [Tuletatud testjuhtumid](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="036ca-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="036ca-137">Teatiste ja sõnumite kinnitamine</span><span class="sxs-lookup"><span data-stu-id="036ca-137">Validate notifications and messages</span></span>

<span data-ttu-id="036ca-138">Seda funktsiooni saab kasutada ka kontrollimaks, kas tegevus toimus.</span><span class="sxs-lookup"><span data-stu-id="036ca-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="036ca-139">Näiteks kui luuakse tootmistellimus, seda hinnatakse ja see seejärel käivitatakse, kuvab rakendus teate „Tootmine – alusta”, mis annab teada, et tootmistellimust on alustatud.</span><span class="sxs-lookup"><span data-stu-id="036ca-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Teatis Tootmine – alusta](./media/use_rsa_tool_05.png)

<span data-ttu-id="036ca-141">Saate selle teate kinnitada läbi RSAT, sisestades teate teksti vastava salvestise Exceli parameetrifaili vahekaardile **Teate kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="036ca-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Vahekaart Teate kinnitamine](./media/use_rsa_tool_06.png)

<span data-ttu-id="036ca-143">Pärast testjuhtumi käivitamist võrreldakse teadet Exceli parameetrifailis kuvatava teatega.</span><span class="sxs-lookup"><span data-stu-id="036ca-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="036ca-144">Kui teated ei kattu, siis testjuhtum nurjub.</span><span class="sxs-lookup"><span data-stu-id="036ca-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="036ca-145">Võite sisestada Exceli parameetrifaili vahekaardile **Teate kinnitamine** rohkem kui ühe teate.</span><span class="sxs-lookup"><span data-stu-id="036ca-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="036ca-146">Teated võivad olla ka tõrke- või hoiatusteated, mitte teavitavad teated.</span><span class="sxs-lookup"><span data-stu-id="036ca-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="036ca-147">Hetktõmmis</span><span class="sxs-lookup"><span data-stu-id="036ca-147">Snapshot</span></span>

<span data-ttu-id="036ca-148">See funktsioon teeb kuvatõmmise etappidest, mis läbiti tegevuse salvestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="036ca-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="036ca-149">See on kasulik auditeerimiseks või silumiseks.</span><span class="sxs-lookup"><span data-stu-id="036ca-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="036ca-150">Selle funktsiooni kasutamiseks avage fail **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT installikaustas (nt **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muutke elemendi väärtus **väär** väärtusele **tõene**.</span><span class="sxs-lookup"><span data-stu-id="036ca-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="036ca-151">Kui käivitate testjuhtumi, teeb RSAT hetktõmmised (pildid) töökaustas oleva testjuhtumite taasesitusekausta etappidest.</span><span class="sxs-lookup"><span data-stu-id="036ca-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="036ca-152">Kui kasutate RSAT-i vanemat versiooni, salvestatakse pildid kausta **C:\\Kasutajad\\\<Kasutajanimi\>\\AppData\\Roaming\\regressionTool\\playback**, iga käitatud testjuhtumi korral luuakse eraldi kaust.</span><span class="sxs-lookup"><span data-stu-id="036ca-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="036ca-153">Määramine</span><span class="sxs-lookup"><span data-stu-id="036ca-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="036ca-154">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="036ca-154">Scenario</span></span>

1. <span data-ttu-id="036ca-155">Toote koostaja loob uue väljastatud toote.</span><span class="sxs-lookup"><span data-stu-id="036ca-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="036ca-156">Tootmisjuht käivitab tootmistellimuse, et jagada toote varud kaheks.</span><span class="sxs-lookup"><span data-stu-id="036ca-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="036ca-157">Tootmine alustab ja lõpetab tootmistellimuse ning kontrollib, kas vaba kaubavaru kogus on kaks tükki.</span><span class="sxs-lookup"><span data-stu-id="036ca-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="036ca-158">Müügimeeskond saab tellimuse neljale tükile uuele tootele.</span><span class="sxs-lookup"><span data-stu-id="036ca-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="036ca-159">Seega uuendab müügimeeskond netonõudeid dünaamilise plaani kaudu.</span><span class="sxs-lookup"><span data-stu-id="036ca-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="036ca-160">Kuna täiendav maht pole saadaval, määratakse tellimuse vaikepoliitika väärtusele „tegemise asemel osta”.</span><span class="sxs-lookup"><span data-stu-id="036ca-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="036ca-161">Seega luuakse plaanitud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="036ca-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="036ca-162">Ostja lisab hankija, kinnitab plaanitud ostutellimuse ja seejärel kinnitab ostutellimuse.</span><span class="sxs-lookup"><span data-stu-id="036ca-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="036ca-163">Kui ostetud kaubad saabuvad kauplusesse, otsib kaupluse töötaja välja seotud ostutellimuse ja võtab kaubad vastu.</span><span class="sxs-lookup"><span data-stu-id="036ca-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="036ca-164">Kuna tellimus on nüüd lõpule viidud, võib kaubad müügitellimuse suhtes komplekteerida ja pakkida.</span><span class="sxs-lookup"><span data-stu-id="036ca-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="036ca-165">Finantsosakond sisestab ostuarve ja müügiarve.</span><span class="sxs-lookup"><span data-stu-id="036ca-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="036ca-166">Järgmisel joonisel on näha selle stsenaariumi voog.</span><span class="sxs-lookup"><span data-stu-id="036ca-166">The following illustration shows the flow for this scenario.</span></span>

![Demostsenaariumi voog](./media/use_rsa_tool_14.png)

<span data-ttu-id="036ca-168">Järgmisel joonisel on kujutatud LCS-i äriprotsesside modelleerija selle stsenaariumi äriprotsesside hierarhia.</span><span class="sxs-lookup"><span data-stu-id="036ca-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Demostsenaariumi äriprotsessid](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="036ca-170">Strateegia – peamised õppepunktid</span><span class="sxs-lookup"><span data-stu-id="036ca-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="036ca-171">Andmed</span><span class="sxs-lookup"><span data-stu-id="036ca-171">Data</span></span>

- <span data-ttu-id="036ca-172">Veenduge, et teil oleks olemas esindavad andmemahud (koopia tootmis- / kuldse konfiguratsiooni andmed ja migreeritud andmed).</span><span class="sxs-lookup"><span data-stu-id="036ca-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="036ca-173">Kui loote uued andmed tegevuse salvestaja kaudu, looge katsenimed, mis ei ole vastuolus olemasolevate nimedega (nt kasutage eesliidet nagu **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="036ca-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="036ca-174">Kasutage Azure’i ajapunktipõhist taastet, et käivitada uuesti testid muudes kui järgu 1 keskkondades.</span><span class="sxs-lookup"><span data-stu-id="036ca-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="036ca-175">Kuigi võite kasutada kordumatu kombinatsiooni loomiseks Exceli funktsioone **RANDOM** ja **NOW**, on panus arvestatavalt kõrge.</span><span class="sxs-lookup"><span data-stu-id="036ca-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="036ca-176">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="036ca-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="036ca-177">Ülesande salvestaja</span><span class="sxs-lookup"><span data-stu-id="036ca-177">Task recorder</span></span>

- <span data-ttu-id="036ca-178">Enne salvestamise alustamist määratlege stsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="036ca-179">Hästi hallatud projektil on eelmääratletud teststsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="036ca-180">Testjuhtumi loomiseks võtke arvesse, kui ennustatav on nende teststsenaariumite tulemus.</span><span class="sxs-lookup"><span data-stu-id="036ca-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="036ca-181">Tükeldage salvestisi, kui need tehakse eri rollides või kui enne järgmist etappi on ooteaeg või väline sündmus.</span><span class="sxs-lookup"><span data-stu-id="036ca-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="036ca-182">Vältige väärtuste valimist loendites.</span><span class="sxs-lookup"><span data-stu-id="036ca-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="036ca-183">Selle asemel kasutage tekstivorminguid, nt **FIFO**, **AudioRM** ja **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="036ca-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="036ca-184">Kui valite loendis, salvestatakse väärtuse asukoht loendis, mitte väärtus ise.</span><span class="sxs-lookup"><span data-stu-id="036ca-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="036ca-185">Kui sellele loendile üksuseid lisatakse, võib väärtuse asukoht muutuda.</span><span class="sxs-lookup"><span data-stu-id="036ca-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="036ca-186">Seega kasutab salvestus muud parameetrit ja see võib mõjutada ülejäänud stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="036ca-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="036ca-187">Mõelge mitme kasutaja käitumisele.</span><span class="sxs-lookup"><span data-stu-id="036ca-187">Think about multi-user behavior.</span></span> <span data-ttu-id="036ca-188">Näiteks ärge eeldage, et alati valitakse automaatselt teie äsja loodud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="036ca-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="036ca-189">Selle asemel kasutage filtrit õige tellimuse leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="036ca-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="036ca-190">Kasutage tegevuse salvestajas funktsiooni Kopeeri äsja loodud toote nime salvestamiseks, et seda saaks kasutada ühendatud testjuhtumites.</span><span class="sxs-lookup"><span data-stu-id="036ca-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="036ca-191">Kasutage tegevuse salvestajad funktsiooni Kinnita kontrollpunktide määramiseks, mis kontrollivad, kas etapid on käivitatud õigesti.</span><span class="sxs-lookup"><span data-stu-id="036ca-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="036ca-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="036ca-192">RSAT</span></span>

- <span data-ttu-id="036ca-193">Testi käivitamiseks teises ettevõttes saate muuta ettevõtte nime Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="036ca-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="036ca-194">Veenduge, et sätted ja andmed oleksid äsja valitud ettevõttes saadaval.</span><span class="sxs-lookup"><span data-stu-id="036ca-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="036ca-195">Saate muuta testkasutajat Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="036ca-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="036ca-196">Määrake testjuhtumit käivitava kasutaja meili ID.</span><span class="sxs-lookup"><span data-stu-id="036ca-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="036ca-197">Sellisel juhul saab testjuhtumit käivitada, kasutades määratud kasutaja turbeõigus.</span><span class="sxs-lookup"><span data-stu-id="036ca-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="036ca-198">Ootamiseks enne testi käivitamist saate määrata pausi Exceli parameetrifaili vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="036ca-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="036ca-199">Seda pausi saab kasutada pakett-töös (nt kui töövoog tuleb käivitada enne, kui järgmist etappi saab läbida).</span><span class="sxs-lookup"><span data-stu-id="036ca-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="036ca-200">Täpsem skriptimine</span><span class="sxs-lookup"><span data-stu-id="036ca-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="036ca-201">CLI</span><span class="sxs-lookup"><span data-stu-id="036ca-201">CLI</span></span>

<span data-ttu-id="036ca-202">RSAT saab käivitada aknast **Käsuviip** või **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="036ca-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="036ca-203">Veenduge, et keskkonnamuutuja **TestRoot** oleks seatud RSAT installiteele.</span><span class="sxs-lookup"><span data-stu-id="036ca-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="036ca-204">(Avage Microsoft Windowsis suvand **Juhtpaneel**, valige **Süsteem ja turvalisus \> Süsteem \> Täpsemad süsteemisätted** ja seejärel valige suvand **Keskkonnamuutujad**.)</span><span class="sxs-lookup"><span data-stu-id="036ca-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="036ca-205">Avage administraatorina aken **Käsuviip** või **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="036ca-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="036ca-206">Navigeerige RSAT-i installikausta.</span><span class="sxs-lookup"><span data-stu-id="036ca-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="036ca-207">Esitage kõik käsud.</span><span class="sxs-lookup"><span data-stu-id="036ca-207">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="036ca-208">?</span><span class="sxs-lookup"><span data-stu-id="036ca-208">?</span></span> 
<span data-ttu-id="036ca-209">Kuvab kõigi saadaolevate käskude ja nende parameetrite spikri.</span><span class="sxs-lookup"><span data-stu-id="036ca-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="036ca-210">Valikulised parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="036ca-211">Kus ``[command]`` on üks allpool määratud käskudest.</span><span class="sxs-lookup"><span data-stu-id="036ca-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="036ca-212">about</span><span class="sxs-lookup"><span data-stu-id="036ca-212">about</span></span>
<span data-ttu-id="036ca-213">Kuvab praeguse versiooni.</span><span class="sxs-lookup"><span data-stu-id="036ca-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="036ca-214">cls</span><span class="sxs-lookup"><span data-stu-id="036ca-214">cls</span></span>
<span data-ttu-id="036ca-215">Tühjendab ekraani.</span><span class="sxs-lookup"><span data-stu-id="036ca-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="036ca-216">laadi alla</span><span class="sxs-lookup"><span data-stu-id="036ca-216">download</span></span>
<span data-ttu-id="036ca-217">Laadib alla määratud testjuhtumi manused väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="036ca-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="036ca-218">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="036ca-219">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="036ca-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-220">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-220">Required parameters</span></span>
<span data-ttu-id="036ca-221">**``test_case_id``** Tähistab testjuhtumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="036ca-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="036ca-222">**``output_dir``** Tähistab väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="036ca-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="036ca-223">Kaust peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="036ca-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-224">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="036ca-225">redigeeri</span><span class="sxs-lookup"><span data-stu-id="036ca-225">edit</span></span>
<span data-ttu-id="036ca-226">Võimaldab teil avada parameetrite faili Exceli programmis ja seda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="036ca-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-227">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-227">Required parameters</span></span>
<span data-ttu-id="036ca-228">**``excel_file``** Peab sisaldama olemasoleva Exceli faili täielikku teed.</span><span class="sxs-lookup"><span data-stu-id="036ca-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-229">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="036ca-230">generate</span><span class="sxs-lookup"><span data-stu-id="036ca-230">generate</span></span>
<span data-ttu-id="036ca-231">Loob testkäivitamise ja parameetrifailid väljundkataloogi määratud testjuhtumi jaoks.</span><span class="sxs-lookup"><span data-stu-id="036ca-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="036ca-232">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="036ca-233">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="036ca-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-234">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-234">Required parameters</span></span>
<span data-ttu-id="036ca-235">**``test_case_id``** Tähistab testjuhtumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="036ca-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="036ca-236">**``output_dir``** Tähistab väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="036ca-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="036ca-237">Kaust peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="036ca-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-238">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="036ca-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="036ca-239">generatederived</span></span>
<span data-ttu-id="036ca-240">Loob uue testjuhtumi, mis tulenevad esitatud testjuhtumist.</span><span class="sxs-lookup"><span data-stu-id="036ca-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="036ca-241">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="036ca-242">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="036ca-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-243">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-243">Required parameters</span></span>
<span data-ttu-id="036ca-244">**``parent_test_case_id``** Tähistab ülemtestjuhtumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="036ca-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="036ca-245">**``test_plan_id``** Tähistab katseplaani ID-d.</span><span class="sxs-lookup"><span data-stu-id="036ca-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="036ca-246">**``test_suite_id``** Tähistab testkomplekti ID-d.</span><span class="sxs-lookup"><span data-stu-id="036ca-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-247">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="036ca-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="036ca-248">generatetestonly</span></span>
<span data-ttu-id="036ca-249">Loob väljundkataloogi määratud testjuhtumi jaoks ainult testkäivitamise faili.</span><span class="sxs-lookup"><span data-stu-id="036ca-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="036ca-250">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="036ca-251">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="036ca-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-252">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-252">Required parameters</span></span>
<span data-ttu-id="036ca-253">**``test_case_id``** Tähistab testjuhtumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="036ca-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="036ca-254">**``output_dir``** Tähistab väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="036ca-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="036ca-255">Kaust peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="036ca-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-256">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="036ca-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="036ca-257">generatetestsuite</span></span>
<span data-ttu-id="036ca-258">Loob kõik väljundkataloogi määratud komplekti testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="036ca-259">Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid.</span><span class="sxs-lookup"><span data-stu-id="036ca-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="036ca-260">Kasutage veeru mis tahes väärtust parameetrina **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="036ca-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-261">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-261">Required parameters</span></span>
<span data-ttu-id="036ca-262">**``test_suite_name``** Tähistab testkomplekti nime.</span><span class="sxs-lookup"><span data-stu-id="036ca-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="036ca-263">**``output_dir``** Tähistab väljundkausta.</span><span class="sxs-lookup"><span data-stu-id="036ca-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="036ca-264">Kaust peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="036ca-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-265">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="036ca-266">spikker</span><span class="sxs-lookup"><span data-stu-id="036ca-266">help</span></span>
<span data-ttu-id="036ca-267">Identne [?](#section)</span><span class="sxs-lookup"><span data-stu-id="036ca-267">Identical to the [?](#section)</span></span> <span data-ttu-id="036ca-268">käsuga</span><span class="sxs-lookup"><span data-stu-id="036ca-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="036ca-269">loend</span><span class="sxs-lookup"><span data-stu-id="036ca-269">list</span></span>
<span data-ttu-id="036ca-270">Loetleb kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="036ca-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="036ca-271">listtestplans</span></span>
<span data-ttu-id="036ca-272">Loetleb kõik saadaolevad katseplaanid.</span><span class="sxs-lookup"><span data-stu-id="036ca-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="036ca-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="036ca-273">listtestsuite</span></span>
<span data-ttu-id="036ca-274">Loetleb määratud testkomplekti testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="036ca-275">Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid.</span><span class="sxs-lookup"><span data-stu-id="036ca-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="036ca-276">Kasutage esimese veeru mis tahes väärtust parameetrina **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="036ca-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-277">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-277">Required parameters</span></span>
<span data-ttu-id="036ca-278">**``suite_name``** Soovitud komplekti nimi.</span><span class="sxs-lookup"><span data-stu-id="036ca-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-279">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="036ca-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="036ca-280">listtestsuitenames</span></span>
<span data-ttu-id="036ca-281">Loetleb kõik saadaolevad testkomplektid.</span><span class="sxs-lookup"><span data-stu-id="036ca-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="036ca-282">playback</span><span class="sxs-lookup"><span data-stu-id="036ca-282">playback</span></span>
<span data-ttu-id="036ca-283">Taasesitab Exceli faili abil testjuhtumi.</span><span class="sxs-lookup"><span data-stu-id="036ca-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-284">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-284">Required parameters</span></span>
<span data-ttu-id="036ca-285">**``excel_file``** Exceli faili täielik tee.</span><span class="sxs-lookup"><span data-stu-id="036ca-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="036ca-286">Fail peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="036ca-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="036ca-287">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="036ca-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="036ca-288">playbackbyid</span></span>
<span data-ttu-id="036ca-289">Taasesitab korraga mitu testjuhtumit.</span><span class="sxs-lookup"><span data-stu-id="036ca-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="036ca-290">Saate kasutada käsku ``list``, et hankida kõik saadaolevad testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="036ca-291">Kasutage esimese veeru mis tahes väärtust parameetrina **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="036ca-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-292">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-292">Required parameters</span></span>
<span data-ttu-id="036ca-293">**``test_case_id1``** Olemasoleva testjuhtumi ID.</span><span class="sxs-lookup"><span data-stu-id="036ca-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="036ca-294">**``test_case_id2``** Olemasoleva testjuhtumi ID.</span><span class="sxs-lookup"><span data-stu-id="036ca-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="036ca-295">**``test_case_idN``** Olemasoleva testjuhtumi ID.</span><span class="sxs-lookup"><span data-stu-id="036ca-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="036ca-296">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="036ca-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="036ca-297">playbackmany</span></span>
<span data-ttu-id="036ca-298">Taasesitab korraga mitu testjuhtumit, kasutades Exceli faile.</span><span class="sxs-lookup"><span data-stu-id="036ca-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-299">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-299">Required parameters</span></span>
<span data-ttu-id="036ca-300">**``excel_file1``** Exceli faili täielik tee.</span><span class="sxs-lookup"><span data-stu-id="036ca-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="036ca-301">Fail peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="036ca-301">File must exist.</span></span>  
<span data-ttu-id="036ca-302">**``excel_file2``** Exceli faili täielik tee.</span><span class="sxs-lookup"><span data-stu-id="036ca-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="036ca-303">Fail peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="036ca-303">File must exist.</span></span>  
<span data-ttu-id="036ca-304">**``excel_fileN``** Exceli faili täielik tee.</span><span class="sxs-lookup"><span data-stu-id="036ca-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="036ca-305">Fail peab olemas olema.</span><span class="sxs-lookup"><span data-stu-id="036ca-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="036ca-306">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="036ca-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="036ca-307">playbacksuite</span></span>
<span data-ttu-id="036ca-308">Taasesitab konkreetse testkomplekti kõik testjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="036ca-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="036ca-309">Saate kasutada käsku ``listtestsuitenames``, et hankida kõik saadaolevad testkomplektid.</span><span class="sxs-lookup"><span data-stu-id="036ca-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="036ca-310">Kasutage esimese veeru mis tahes väärtust parameetrina **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="036ca-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-311">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-311">Required parameters</span></span>
<span data-ttu-id="036ca-312">**``suite_name``** Soovitud komplekti nimi.</span><span class="sxs-lookup"><span data-stu-id="036ca-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-313">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="036ca-314">quit</span><span class="sxs-lookup"><span data-stu-id="036ca-314">quit</span></span>
<span data-ttu-id="036ca-315">Sulgeb rakenduse.</span><span class="sxs-lookup"><span data-stu-id="036ca-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="036ca-316">upload</span><span class="sxs-lookup"><span data-stu-id="036ca-316">upload</span></span>
<span data-ttu-id="036ca-317">Laadib üles kõik määratud testkomplekti või testjuhtumitesse kuuluvad failid.</span><span class="sxs-lookup"><span data-stu-id="036ca-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="036ca-318">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-318">Required parameters</span></span>
<span data-ttu-id="036ca-319">**``suite_name``** Kõik määratud testkomplekti kuuluvad failid laaditakse üles.</span><span class="sxs-lookup"><span data-stu-id="036ca-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="036ca-320">**``testcase_id``** Kõik määratud testjuhtumi(te)sse kuuluvad failid laaditakse üles.</span><span class="sxs-lookup"><span data-stu-id="036ca-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-321">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="036ca-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="036ca-322">uploadrecording</span></span>
<span data-ttu-id="036ca-323">Laadib üles ainult määratud testjuhtumitesse kuuluva salvestamisfaili.</span><span class="sxs-lookup"><span data-stu-id="036ca-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="036ca-324">Nõutud parameetrid</span><span class="sxs-lookup"><span data-stu-id="036ca-324">Required parameters</span></span>
<span data-ttu-id="036ca-325">**``testcase_id``** Määratud testjuhtumitesse kuuluv salvestamisfail laaditakse üles.</span><span class="sxs-lookup"><span data-stu-id="036ca-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="036ca-326">Näited</span><span class="sxs-lookup"><span data-stu-id="036ca-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="036ca-327">usage</span><span class="sxs-lookup"><span data-stu-id="036ca-327">usage</span></span>
<span data-ttu-id="036ca-328">Näitab selle rakenduse kahte käivitamisviisi: üks kasutab vaikimisi seadistusfaili, teine esitab seadistusfaili.</span><span class="sxs-lookup"><span data-stu-id="036ca-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="036ca-329">Windows PowerShelli näited</span><span class="sxs-lookup"><span data-stu-id="036ca-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="036ca-330">Allolevad näidisskriptid on esitatud olemasoleval kujul ja need on illustratiivsed ning Microsoft ei toeta neid.</span><span class="sxs-lookup"><span data-stu-id="036ca-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="036ca-331">Testjuhtumi käivitamine tsüklis</span><span class="sxs-lookup"><span data-stu-id="036ca-331">Run a test case in a loop</span></span>

<span data-ttu-id="036ca-332">Teil on testskript, mis loob uue kliendi.</span><span class="sxs-lookup"><span data-stu-id="036ca-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="036ca-333">Skriptimise kaudu saab seda testjuhtumis käivitada tsüklis, muutes enne iga iteratsiooni käivitamist järgmised andmed juhuslikuks.</span><span class="sxs-lookup"><span data-stu-id="036ca-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="036ca-334">Kliendi ID</span><span class="sxs-lookup"><span data-stu-id="036ca-334">Customer ID</span></span>
- <span data-ttu-id="036ca-335">Kliendi nimi</span><span class="sxs-lookup"><span data-stu-id="036ca-335">Customer name</span></span>
- <span data-ttu-id="036ca-336">Kliendi aadress</span><span class="sxs-lookup"><span data-stu-id="036ca-336">Customer address</span></span>

<span data-ttu-id="036ca-337">Kliendi ID on vormingus *ATCUS\<number\>*, kus \<number\> on väärtus vahemikus **000000001** kuni **999999999**.</span><span class="sxs-lookup"><span data-stu-id="036ca-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="036ca-338">Järgmises näites kasutatakse üht parameetrit, **alusta**, esimese kasutatud numbri määramiseks.</span><span class="sxs-lookup"><span data-stu-id="036ca-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="036ca-339">See kasutab teist parameetrit, **nr**, loodavate klientide arvu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="036ca-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="036ca-340">Iga iteratsiooni kohta muudetakse Exceli parameetrifailis parameetreid, kasutades funktsiooni UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="036ca-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="036ca-341">Seejärel käivitatakse RSAT käsurida funktsioonis RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="036ca-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="036ca-342">Avage Microsoft Windows PowerShell Integrated Scripting Environment (ISE) haldusrežiimis ja kleepige järgmine kood aknasse nimega **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="036ca-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="036ca-343">Microsoft Dynamics 365 andmetest sõltuva skripti käivitamine</span><span class="sxs-lookup"><span data-stu-id="036ca-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="036ca-344">Järgmises näites kasutatakse kutset Open Data Protocol (OData) ostutellimuse tellimuse oleku leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="036ca-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="036ca-345">Kui olek ei ole **arveldatud**, võite näiteks käivitada RSAT testjuhtumi, mis arve sisestab.</span><span class="sxs-lookup"><span data-stu-id="036ca-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
