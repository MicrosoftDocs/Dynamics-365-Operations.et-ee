---
title: Testimise automatiseerimine elektroonilise aruandluse abil
description: Selles teemas selgitatakse, kuidas saate kasutada elektroonilise aruandluse (ER) raamistiku põhifunktsiooni mõnede funktsioonide testimise automatiseerimiseks.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: be641e1b2f90f4d19f7ed15e47413c0aa43d5073
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771440"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="b5c35-103">Testimise automatiseerimine elektroonilise aruandluse abil</span><span class="sxs-lookup"><span data-stu-id="b5c35-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b5c35-104">Selles teemas selgitatakse, kuidas saate kasutada elektroonilise aruandluse (ER) raamistikku mõnede funktsioonide testimise automatiseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="b5c35-105">Selles teemas toodud näide näitab, kuidas automatiseerida hankija maksetöötluse testimist.</span><span class="sxs-lookup"><span data-stu-id="b5c35-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="b5c35-106">Rakendus kasutab hankija maksetöötluse ajal makseväljade ja vastavate dokumentide loomiseks ER-raamistikku.</span><span class="sxs-lookup"><span data-stu-id="b5c35-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="b5c35-107">ER-raamistik koosneb andmemudelist, mudeli vastendustest ja vorminduse komponentidest, mis toetavad makse töötlemist erinevate makseviiside jaoks ja erinevates vormingutes dokumentide loomist.</span><span class="sxs-lookup"><span data-stu-id="b5c35-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="b5c35-108">Neid komponente saab alla laadida lahendusest Microsoft Dynamics Lifecycle Services (LCS) ja importida eksemplari.</span><span class="sxs-lookup"><span data-stu-id="b5c35-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="b5c35-109">Samuti saate kohandada igat Microsofti komponenti ja kasutada seda oma kohandatud komponendi põhjana.</span><span class="sxs-lookup"><span data-stu-id="b5c35-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="b5c35-110">Kohandatud versiooni loomisega saate teha muudatusi, mis toetavad kindlaid nõudmisi.</span><span class="sxs-lookup"><span data-stu-id="b5c35-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="b5c35-111">Näiteks saate korrigeerida ER-andmemudelit ja ER-mudeli vastendamist, et saada juurdepääs kliendipõhistele rakenduse andmetele, või muuta ER-vormingut loodud dokumendi paigutuse muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="b5c35-112">Saate kasutada oma eksemplaris kohandatud ER-vorminguid, et töödelda maksete faile, mis loovad hankija makseid ja töödelda ka protsessi juhtimise aruandeid.</span><span class="sxs-lookup"><span data-stu-id="b5c35-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="b5c35-113">ER-komponentide puhul toetatakse versioonimist.</span><span class="sxs-lookup"><span data-stu-id="b5c35-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="b5c35-114">Seetõttu võib Microsoft pakkuda hankija makse töötlemiseks ER-lahenduste värskendatud versioone ja teie saate värskendatud versiooni automaatselt oma kohandatud komponendiga uuele põhjale tuginedes ühendada.</span><span class="sxs-lookup"><span data-stu-id="b5c35-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="b5c35-115">Siiski peate uue põhjaga versiooni testima, et veenduda selle ootuspärases toimimises.</span><span class="sxs-lookup"><span data-stu-id="b5c35-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="b5c35-116">ER-andmemudelid ja ER-mudelite vastendused on omased paljudele ER-vormingutele, mida kasutatakse erinevat tüüpi maksete töötlemiseks ja riigi-/piirkonnapõhiste maksedokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="b5c35-117">Seetõttu on ülimalt soovitatav automatiseerida kasutaja vastuvõtu ja integratsiooni testimine nii, et seda tehakse automaatselt mitmes ettevõttes, võttes arvesse iga sihtettevõtte riigi-/piirkonna konteksti, kasutades erinevaid andmekomplekte jne.</span><span class="sxs-lookup"><span data-stu-id="b5c35-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="b5c35-118">Lisateavet konfiguratsiooni pakkujalt saadud vormingul põhineva kohandatud vormingu versiooni loomise kohta leiate jaotisest [Elektrooniline aruandlus. Vormingu täiendamine uue alusversiooni kasutuselevõtuga](./tasks/er-upgrade-format.md).</span><span class="sxs-lookup"><span data-stu-id="b5c35-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="b5c35-119">Põhimõisted</span><span class="sxs-lookup"><span data-stu-id="b5c35-119">Key concepts</span></span>

<span data-ttu-id="b5c35-120">Funktsionaalsed lauskasutajad saavad algatada kasutajate aktsepteerimise ja integreerimise testimist ilma, et peaksid lähtekoodi kirjutama.</span><span class="sxs-lookup"><span data-stu-id="b5c35-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="b5c35-121">Kasutage ER-alusfunktsiooni loodud dokumentide ja põhieksemplaride võrdlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="b5c35-122">Lisainfo saamiseks vt [oodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="b5c35-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="b5c35-123">Kasutage tegevuse salvestajat testjuhtumite kirjendamiseks ja kaasake lähteolukorra hinnang.</span><span class="sxs-lookup"><span data-stu-id="b5c35-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="b5c35-124">Lisateavet vt [Tegevuse salvestaja ressursid](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="b5c35-124">For more information, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="b5c35-125">Grupeerige testjuhtumid vajalike teststsenaariumite jaoks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="b5c35-126">Lisateavet vt [Kasutaja vastuvõtu testide loomine ja automatiseerimine](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span><span class="sxs-lookup"><span data-stu-id="b5c35-126">For more information, see [Create and automate user acceptance tests](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="b5c35-127">Kasutage LCS-s äriprotsesside modelleerijat (BPM) kasutaja vastuvõtu testimise teekide tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="b5c35-128">Kasutage BPM-i testimise teeke katseplaani ja testkomplektide loomiseks lahenduses Microsoft Azure DevOps Services (Azure DevOps).</span><span class="sxs-lookup"><span data-stu-id="b5c35-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="b5c35-129">Funktsionaalsed lauskasutajad saavad teostada kasutajate vastuvõtu ja integreerimise testimist.</span><span class="sxs-lookup"><span data-stu-id="b5c35-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="b5c35-130">Kasutage soovitud testkomplekti testjuhtumite teostamiseks tööriista Regression suite automation tool (RSAT).</span><span class="sxs-lookup"><span data-stu-id="b5c35-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="b5c35-131">Teatage testitulemused Azure DevOps-ile ja kasutage seda teenust nende tulemuste uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b5c35-132">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="b5c35-132">Prerequisites</span></span>

<span data-ttu-id="b5c35-133">Enne selles teemas kirjeldatud ülesannete lõpetamist peate täitma järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="b5c35-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="b5c35-134">Rakendage topoloogiat, mis toetab testimise automatiseerimist.</span><span class="sxs-lookup"><span data-stu-id="b5c35-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="b5c35-135">**Süsteemi administraatori** rolli jaoks peab teil olema juurdepääs selle topoloogia eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="b5c35-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="b5c35-136">See topoloogia peab sisaldama demo andmeid, mida selles näites kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="b5c35-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="b5c35-137">Lisateavet vt [Pideva koostamise ja testimise automaatikat toetavate keskkondade juurutamine ja kasutamine](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="b5c35-137">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="b5c35-138">Kasutaja vastuvõtu ja integreerimise testide automaatseks teostamiseks peate paigaldama RSATi topoloogiasse, mida kasutate, ja selle sobivalt konfigureerima.</span><span class="sxs-lookup"><span data-stu-id="b5c35-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="b5c35-139">Lisainfot RSATi installimise ja konfigureerimise ning Finance and Operations rakenduste ja Azure DevOps'iga toimimise konfigureerimise kohta vt [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span><span class="sxs-lookup"><span data-stu-id="b5c35-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="b5c35-140">Pöörake tähelepanu tööriista kasutamise eeltingimustele.</span><span class="sxs-lookup"><span data-stu-id="b5c35-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="b5c35-141">Järgmisel joonisel on näide RSATi seadistuste kohta.</span><span class="sxs-lookup"><span data-stu-id="b5c35-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="b5c35-142">Sinine ristkülik ümbritseb parameetrid, mis määravad juurdepääsu Azure DevOps-ile.</span><span class="sxs-lookup"><span data-stu-id="b5c35-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="b5c35-143">Roheline ristkülik ümbritseb parameetrid, mis määravad juurdepääsu eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="b5c35-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="b5c35-144">![RSAT sätted](media/GER-Configure.png "RSAT-i sätete dialoogiboksi kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="b5c35-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="b5c35-145">Testjuhtumite õige käivitusjärjestuse tagamiseks komplektidesse sorteerimiseks, et saaksite koguda testkäivituste logisid edasiseks aruandluseks ja uurimiseks, peab teil olema rakendatud topoloogiast juurdepääs Azure DevOps-ile.</span><span class="sxs-lookup"><span data-stu-id="b5c35-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="b5c35-146">Selle teema näite lõpetuseks soovitame teil alla laadida [ER-i kasutamine RSAT-testideks](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="b5c35-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="b5c35-147">See zip-fail sisaldab järgmisi tegevusjuhiseid.</span><span class="sxs-lookup"><span data-stu-id="b5c35-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="b5c35-148">Sisu</span><span class="sxs-lookup"><span data-stu-id="b5c35-148">Content</span></span>                                           | <span data-ttu-id="b5c35-149">Faili nimi ja asukoht</span><span class="sxs-lookup"><span data-stu-id="b5c35-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="b5c35-150">Andmete testimiseks ettevalmistamise tegevuse salvestamise näidis</span><span class="sxs-lookup"><span data-stu-id="b5c35-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="b5c35-151">Ettevalmistamine\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="b5c35-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="b5c35-152">Hankija makse töötlemise tegevuse salvestamise näidis</span><span class="sxs-lookup"><span data-stu-id="b5c35-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="b5c35-153">Töötlus\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="b5c35-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="b5c35-154">Valmistage ostureskontro moodul hankija maksete töötlemiseks ette</span><span class="sxs-lookup"><span data-stu-id="b5c35-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="b5c35-155">Logige oma eksemplari sisse.</span><span class="sxs-lookup"><span data-stu-id="b5c35-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="b5c35-156">Laadige järgmised ER-konfiguratsioonid LCS-ist alla.</span><span class="sxs-lookup"><span data-stu-id="b5c35-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="b5c35-157">Juhiste saamiseks vt [Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="b5c35-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="b5c35-158">**Maksemudel** ER-mudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="b5c35-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="b5c35-159">**Maksemudeli vastendamine 1611** ER-mudeli vastendamise konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="b5c35-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="b5c35-160">**BACS (UK)** ER-vormingu konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="b5c35-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="b5c35-161">![Elektroonilise aruandluse konfiguratsioonid](media/GER-Configurations.png "Elektroonilise aruandluse konfiguratsioonide lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="b5c35-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="b5c35-162">Valige **GBSI** demo andmete ettevõte, millel on riigi-/piirkonna kontekst Suurbritannias.</span><span class="sxs-lookup"><span data-stu-id="b5c35-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="b5c35-163">Ostureskontro parameetrite konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="b5c35-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="b5c35-164">Avage **Ostureskonto \> Makse seadistus \> Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="b5c35-165">Valige **Elektrooniline** makseviis.</span><span class="sxs-lookup"><span data-stu-id="b5c35-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="b5c35-166">Konfigureerige valitud makseviis nii, et see kasutab **BACS (UK)** ER-vormingut, mille varem hankija makse töötlemiseks alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="b5c35-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="b5c35-167">Seadistage kiirkaardil **Failivormingud** suvand **Üldine elektrooniline ekspordivorming** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="b5c35-168">Valige väljal **Vormingu konfiguratsiooni eksportimine** **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="b5c35-169">![Makseviiside leht](media/GER-APParameters.png "Makseviiside lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="b5c35-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5c35-170">Kui teil on selle ER-vormingu tuletatud versioon, mis loodi kohanduste toetamiseks, saate valida selle konfiguratsiooni makseviisi **Elektrooniline** alt.</span><span class="sxs-lookup"><span data-stu-id="b5c35-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="b5c35-171">Looge hankija makse näidis.</span><span class="sxs-lookup"><span data-stu-id="b5c35-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="b5c35-172">Avage **Ostureskonto \> Maksed \> Maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="b5c35-173">Veenduge, et te ei ole maksete töölehte sisestanud.</span><span class="sxs-lookup"><span data-stu-id="b5c35-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="b5c35-174">![Maksete töölehe leht](media/GER-APJournal.png "Maksete töölehe lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="b5c35-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="b5c35-175">Valige **Read** ja sisestage rida, millel on järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="b5c35-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="b5c35-176">Väli</span><span class="sxs-lookup"><span data-stu-id="b5c35-176">Field</span></span>               | <span data-ttu-id="b5c35-177">Näidisväärtus</span><span class="sxs-lookup"><span data-stu-id="b5c35-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="b5c35-178">Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="b5c35-178">Vendor name</span></span>         | <span data-ttu-id="b5c35-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="b5c35-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="b5c35-180">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="b5c35-180">Debit</span></span>               | <span data-ttu-id="b5c35-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b5c35-181">1,000.00</span></span>        |
        | <span data-ttu-id="b5c35-182">Valuuta</span><span class="sxs-lookup"><span data-stu-id="b5c35-182">Currency</span></span>            | <span data-ttu-id="b5c35-183">GBP</span><span class="sxs-lookup"><span data-stu-id="b5c35-183">GBP</span></span>             |
        | <span data-ttu-id="b5c35-184">Vastaskonto tüüp</span><span class="sxs-lookup"><span data-stu-id="b5c35-184">Offset account type</span></span> | <span data-ttu-id="b5c35-185">Pank</span><span class="sxs-lookup"><span data-stu-id="b5c35-185">Bank</span></span>            |
        | <span data-ttu-id="b5c35-186">Vastaskonto</span><span class="sxs-lookup"><span data-stu-id="b5c35-186">Offset account</span></span>      | <span data-ttu-id="b5c35-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="b5c35-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="b5c35-188">Makseviis</span><span class="sxs-lookup"><span data-stu-id="b5c35-188">Method of payment</span></span>   | <span data-ttu-id="b5c35-189">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="b5c35-189">Electronic</span></span>      |

    <span data-ttu-id="b5c35-190">![Hankija maksete leht](media/GER-APJournalLines.png "Hankija maksete lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="b5c35-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="b5c35-191">Valmistage ER-raamistik hankija maksete töötlemise testimiseks ette</span><span class="sxs-lookup"><span data-stu-id="b5c35-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="b5c35-192">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b5c35-192">Configure ER parameters</span></span>

1. <span data-ttu-id="b5c35-193">Avage **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="b5c35-194">Vali vahekaardi **Manused** väljal **Alus** selleks dokumenditüübiks **Fail**, mida dokumendihalduse (DM) raamistik kasutab DM-manustena alusfunktsiooniga seotud dokumentide hoidmiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="b5c35-195">![Elektroonilise aruandluse parameetrite leht](media/GER-ERParameters.png "Elektroonilise aruandluse parameetrite lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="b5c35-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="b5c35-196">Handkija maksetega seotud dokumentide algkoopiate loomine</span><span class="sxs-lookup"><span data-stu-id="b5c35-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="b5c35-197">Avage **Ostureskonto \> Maksed \> Maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="b5c35-198">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-198">Select **Lines**.</span></span>
3. <span data-ttu-id="b5c35-199">Valige **Loo maksed**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="b5c35-200">Valige **Elektrooniline** makseviis.</span><span class="sxs-lookup"><span data-stu-id="b5c35-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="b5c35-201">Valige **GBSI OPER** pangakonto.</span><span class="sxs-lookup"><span data-stu-id="b5c35-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="b5c35-202">Seadistage valik **Kontrollaruande printimine** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="b5c35-203">Laadige loodud väljund zip-failina alla.</span><span class="sxs-lookup"><span data-stu-id="b5c35-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="b5c35-204">Avage allalaaditud fail.</span><span class="sxs-lookup"><span data-stu-id="b5c35-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="b5c35-205">Ekstraktige allalaaditud failist järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="b5c35-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="b5c35-206">**Fail** maksefail tekstivormingus</span><span class="sxs-lookup"><span data-stu-id="b5c35-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="b5c35-207">**ERVendOutPaymControlReport** kontrollaruande fail XLSX-vormingus</span><span class="sxs-lookup"><span data-stu-id="b5c35-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="b5c35-208">![Ekstraktitud failid](media/GER-APJournalProcessed.png "Kuvatõmmis ekstraktitud failide nimedest Windows Exploreris")</span><span class="sxs-lookup"><span data-stu-id="b5c35-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="b5c35-209">ER-alusfunktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="b5c35-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="b5c35-210">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="b5c35-211">Valige tegumiriba **Konfiguratsioonid** vahekaardil **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="b5c35-212">Määrake suvand **Käivita silumisrežiimis** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="b5c35-213">Lülitades parameetri **Käivita silumisrežiimis** sisse, sunnite ER-raamistiku pärast mistahes väljuvaid dokumente loova ER-vormingu käivitamist teostama järgmisi tegevusi.</span><span class="sxs-lookup"><span data-stu-id="b5c35-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="b5c35-214">Määratlege, kas täidetud ER-vormingu mistahes komponentidele on konfigureeritud algväärtus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="b5c35-215">Tehke kindlaks, kas iga konfigureeritud algväärtus on kohaldatav praegustele tingimustele (sisselogitud ettevõtte ettevõtte kood, failinimi ja genereeritud väljundi failinime laiend jne).</span><span class="sxs-lookup"><span data-stu-id="b5c35-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="b5c35-216">Iga kohaldatava algväärtuse korral tehke järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="b5c35-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="b5c35-217">Võrrelge ER-vormingu täitmisel loodud väljundit vastava algväärtusega.</span><span class="sxs-lookup"><span data-stu-id="b5c35-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="b5c35-218">Talletage võrdluse tulemused ER-konfiguratsioonide silumislogis.</span><span class="sxs-lookup"><span data-stu-id="b5c35-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="b5c35-219">Hankija maksete töötlemise ER-algväärtuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b5c35-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="b5c35-220">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="b5c35-221">Valige suvand **Alused**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="b5c35-222">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-222">Select **New**.</span></span>
4. <span data-ttu-id="b5c35-223">Valige väljal **Viide** vorming **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="b5c35-224">Valige suvand **Manused**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="b5c35-225">Lisage hankija makse failile uus algväärtus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="b5c35-226">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-226">Select **New**.</span></span>
    2. <span data-ttu-id="b5c35-227">Valige väljal **Tüüp** dokumendihalduse dokumendi tüüp **Fail**, mille konfigureerisite algväärtuse artefakti talletamise ER-parameetrites.</span><span class="sxs-lookup"><span data-stu-id="b5c35-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="b5c35-228">Sirvige kohalikult salvestatud **Fail** maksefaili tekstivormingus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="b5c35-229">Sisestage väljale **Kirjeldus** **Makse TXT fail**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="b5c35-230">Lisage hankija makse kontrollaruandele uus algväärtus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="b5c35-231">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-231">Select **New**.</span></span>
    2. <span data-ttu-id="b5c35-232">Valige väljal **Tüüp** dokumendihalduse dokumendi tüüp **Fail**, mille konfigureerisite algväärtuse artefakti talletamise ER-parameetrites.</span><span class="sxs-lookup"><span data-stu-id="b5c35-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="b5c35-233">Sirvige, et valida kohalikult salvestatud **ERVendOutPaymControlReport** kontrollaruanne XLSX vormingus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="b5c35-234">Sisestage väljale **Kirjeldus** **Makse XLSX kontrollaruanne**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="b5c35-235">![Hankija makse faili ja kontrollaruande algväärtused](media/GER-BaselineAttachments.png "Kuvatõmmis valitud makse XLSX kontrollaruandega konfiguratsioonilehest")</span><span class="sxs-lookup"><span data-stu-id="b5c35-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="b5c35-236">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b5c35-236">Close the page.</span></span>
9. <span data-ttu-id="b5c35-237">Valige kiirkaardil **Algväätused** suvand **Uus**, et konfigureerida maksefaili algväärtus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="b5c35-238">Pange reale nimeks **Maksefaili alussätted**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="b5c35-239">Valige väljal **Faili komponendi nimi** suvand **fail**, et rakendada see algväärtus sellele ER-vormingu väljundile, mis genereerib maksefaili BACS (UK) tekstivormingus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="b5c35-240">Valige väljal **Ettevõtted** suvand **GBSI**, et rakendada seda algväärtust siis, kui GBSI ettevõttes kasutatakse **BACS (UK)** ER-vormingut.</span><span class="sxs-lookup"><span data-stu-id="b5c35-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="b5c35-241">Sisestage väljale **Failinime mask** **\*.TXT**, et rakendada seda algväärtust ainule neile vormingu **fail** komponentide väljunditele, mille failinime laiendiks on **.txt**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="b5c35-242">Valige väljal **Algväärtus** suvand **Makse TXT fail**, et seda algväärtust kasutataks loodud väljundiga võrdlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="b5c35-243">Valige **Uus**, et konfigureerida kontrollaruandele algväärtus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="b5c35-244">Pange reale nimeks **Kontrollaruande alussätted**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="b5c35-245">Valige väljal **Faili komponendi nimi** suvand **ERVendOutPaymControlReport**, et rakendada see algväärtus sellele ER-vormingu väljundile, mis genereerib kontrollaruande.</span><span class="sxs-lookup"><span data-stu-id="b5c35-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="b5c35-246">Valige väljal **Ettevõtted** suvand **GBSI**, et rakendada seda algväärtust siis, kui GBSI ettevõttes kasutatakse **BACS (UK)** ER-vormingut.</span><span class="sxs-lookup"><span data-stu-id="b5c35-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="b5c35-247">Sisestage väljale **Failinime mask** **\*.XLSX**, et rakendada seda algväärtust ainule neile vormingu **ERVendOutPaymControlReport** komponentide väljunditele, mille failinime laiendiks on **.xslx**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="b5c35-248">Valige väljal **Algväärtus** suvand **Makse XLSX kontrollaruanne**, et seda algväärtust kasutataks loodud väljundiga võrdlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="b5c35-249">![Kiirkaart Algväärtused konfiguratsioonide lehel](media/GER-BaselineRules.png "Kuvatõmmis kiirkaardist Väärtused konfiguratsioonide lehel")</span><span class="sxs-lookup"><span data-stu-id="b5c35-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="b5c35-250">Kirjendab testid hankija maksete töötlemise kinnitamiseks</span><span class="sxs-lookup"><span data-stu-id="b5c35-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="b5c35-251">Funktsionaalse lauskasutajana saate kirjendada oma samme hankija maksete töötlemise testimiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="b5c35-252">Soovitame teil esitada (ja vastavalt vajadusele redigeerida) tegevuse salvestist **Ettevalmistamine\\Recording.xml**, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="b5c35-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="b5c35-253">Seda salvestust kasutatakse kõiki testimisandmete õigesse olekusse seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="b5c35-254">See samm on vajalik, sest testimist saab teha mitu korda ja iga katse peab kasutama andmeid, mis on samas olekus.</span><span class="sxs-lookup"><span data-stu-id="b5c35-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="b5c35-255">Kasutajasätete lähtestamine</span><span class="sxs-lookup"><span data-stu-id="b5c35-255">Reset user settings</span></span>

1. <span data-ttu-id="b5c35-256">Avage vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="b5c35-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="b5c35-257">Valige nupp **Sätted** (hammasratta sümbol).</span><span class="sxs-lookup"><span data-stu-id="b5c35-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="b5c35-258">Valige **Kasutaja valikud**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-258">Select **User options**.</span></span>
4. <span data-ttu-id="b5c35-259">Valige **Kasutusandmed**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="b5c35-260">Valige **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-260">Select **Reset**.</span></span>
6. <span data-ttu-id="b5c35-261">Valige **Jah**, et kinnitada, et soovite kasutusandmeid lähtestada.</span><span class="sxs-lookup"><span data-stu-id="b5c35-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="b5c35-262">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b5c35-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="b5c35-263">Kirjendage andmete testimiseks ettevalmistamise sammud</span><span class="sxs-lookup"><span data-stu-id="b5c35-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="b5c35-264">Valige nupp **Sätted** (hammasratta sümbol).</span><span class="sxs-lookup"><span data-stu-id="b5c35-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="b5c35-265">Valige **Tegevuse salvestaja**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="b5c35-266">Valige **Salvestise taasesitus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="b5c35-267">Valige **Ava sellest arvutist**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="b5c35-268">Valige **Sirvi** ja valige kohalikult salvestatud **Ettevalmistamine\\Recording.,xml** fail.</span><span class="sxs-lookup"><span data-stu-id="b5c35-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="b5c35-269">Valige nupp **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-269">Select **Start**.</span></span>
7. <span data-ttu-id="b5c35-270">Jätkake valiku **Esita järgmine ootel etapp** kuni salvestuse kõik etapid on esitatud.</span><span class="sxs-lookup"><span data-stu-id="b5c35-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="b5c35-271">Selle tegevuse salvestamine sooritab järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="b5c35-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="b5c35-272">Seadke töödeldud makse rea olek väärtusele **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="b5c35-273">![Tegevuse salvestamise etapid 3 kuni 4](media/GER-Recording1Review1.png "Kuvatõmmis tegevuse salvestamise etappidest 3 kuni 4")</span><span class="sxs-lookup"><span data-stu-id="b5c35-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="b5c35-274">Lülitage elektroonilise aruandluse kasutaja parameeter **Käivita silumisrežiimis** sisse.</span><span class="sxs-lookup"><span data-stu-id="b5c35-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="b5c35-275">![Tegevuse salvestamise etapid 9 kuni 10](media/GER-Recording1Review2.png "Kuvatõmmis tegevuse salvestamise etappidest 9 kuni 10")</span><span class="sxs-lookup"><span data-stu-id="b5c35-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="b5c35-276">Puhastage see elektroonilise aruandluse silumislogi, mis sisaldab loodud failide ja algväärtuste võrdluse tulemusi.</span><span class="sxs-lookup"><span data-stu-id="b5c35-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="b5c35-277">![Tegevuse salvestamise etapid 13 kuni 15](media/GER-Recording1Review3.png "Kuvatõmmis tegevuse salvestamise etappidest 13 kuni 15")</span><span class="sxs-lookup"><span data-stu-id="b5c35-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="b5c35-278">Kirjendage hankija maksete töötlemise testimise etapid</span><span class="sxs-lookup"><span data-stu-id="b5c35-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="b5c35-279">Soovitame teil esitada (ja vastavalt vajadusele redigeerida) tegevuse salvestist **Töötlus\\Recording.xml**, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="b5c35-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="b5c35-280">Seda salvestist kasutatakse hankija maksete töötlemiseks ja loodud dokumentide ja vastavate alusväärtuste võrdluse tulemuste kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="b5c35-281">Valige nupp **Sätted** (hammasratta sümbol).</span><span class="sxs-lookup"><span data-stu-id="b5c35-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="b5c35-282">Valige **Tegevuse salvestaja**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="b5c35-283">Valige **Salvestise taasesitus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="b5c35-284">Valige **Ava sellest arvutist**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="b5c35-285">Valige **Sirvi** ja valige kohalikult salvestatud **Töötlus\\Recording.,xml** fail.</span><span class="sxs-lookup"><span data-stu-id="b5c35-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="b5c35-286">Valige nupp **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-286">Select **Start**.</span></span>
7. <span data-ttu-id="b5c35-287">Jätkake valiku **Esita järgmine ootel etapp** kuni salvestuse kõik etapid on esitatud.</span><span class="sxs-lookup"><span data-stu-id="b5c35-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="b5c35-288">Selle tegevuse salvestamine sooritab järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="b5c35-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="b5c35-289">Hankija maksete töötlemise käivitamine.</span><span class="sxs-lookup"><span data-stu-id="b5c35-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="b5c35-290">Valige õiged käitamisaja parameetrid ja lülitage kontrollaruande loomine sisse.</span><span class="sxs-lookup"><span data-stu-id="b5c35-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="b5c35-291">![Tegevuse salvestamise etapid 3 kuni 8](media/GER-Recording2Review1.png "Kuvatõmmis tegevuse salvestamise etappidest 3 kuni 8")</span><span class="sxs-lookup"><span data-stu-id="b5c35-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="b5c35-292">Avage see elektroonilise aruandluse silumislogi, et kirjendada loodud väljundite ja vastavate algväärtuste võrdluse tulemusi.</span><span class="sxs-lookup"><span data-stu-id="b5c35-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="b5c35-293">Elektroonilise aruandluse silumislogis kuvatakse võrdlustulemusi väljal **Loodud tekst**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="b5c35-294">Väljad **Vormingu komponent** ja **Logikande põhjustanud vormingutee** viitavad faili komponendile, millele loodud väljundit on võrreldud algväärtusega.</span><span class="sxs-lookup"><span data-stu-id="b5c35-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="b5c35-295">![Elektroonilise aruandluse käitamise logide lehe kirjed](media/GER-ERDebugLog.png "Elektroonilise aruandluse käitamise logide lehe kirjete kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="b5c35-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="b5c35-296">Praeguse väljundi võrdlemine algväärtusega on kirjendatud kasutades tegevuse salvestaja suvandit **Kinnita** ja valides suvandi **Praegune väärtus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="b5c35-297">![Kinnitamise suvandi kasutamine praeguse väärtusega võrdlemiseks](media/GER-TRRecordValidation.png "Kuvatõmmis kinnitamise suvandi kasutamisest praeguse väärtusega võrdlemiseks")</span><span class="sxs-lookup"><span data-stu-id="b5c35-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="b5c35-298">Järgmisel joonisel on näha, millised salvestatud kinnitamise etapid tegevuse salvestises välja näevad.</span><span class="sxs-lookup"><span data-stu-id="b5c35-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="b5c35-299">![Tegevuse salvestamise etapid 13 ja 15](media/GER-Recording2Review2.png "Kuvatõmmis tegevuse salvestamise etappidest 13 ja 15")</span><span class="sxs-lookup"><span data-stu-id="b5c35-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="b5c35-300">Lisage salvestatud testid Azure DevOps-i</span><span class="sxs-lookup"><span data-stu-id="b5c35-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="b5c35-301">Avage Azure DevOps-i keskkond.</span><span class="sxs-lookup"><span data-stu-id="b5c35-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="b5c35-302">Valige projekt, mille määratlesite RSATi parameetrites, kui [konfigureerisite tööriista](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="b5c35-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="b5c35-303">Valige katseplaan, mille määratlesite RSATi parameetrites, kui [konfigureerisite tööriista](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="b5c35-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="b5c35-304">Looge valitud katseplaanile uus testjuhtum.</span><span class="sxs-lookup"><span data-stu-id="b5c35-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="b5c35-305">Pange testjuhtumi nimeks **Hankija elektroonilise makse testtöötluseks andmete ettevalmistamine**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="b5c35-306">Manustage fail **Recording.xml** kaustast **Ettevalmistamine**, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="b5c35-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="b5c35-307">Looge valitud katseplaanile uus testjuhtum.</span><span class="sxs-lookup"><span data-stu-id="b5c35-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="b5c35-308">Pane testjuhtumi nimeks **Hankija maksete testtöötlemine kasutades ER-vormingut BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="b5c35-309">Manustage fail **Recording.xml** kaustast **Töötlemine**, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="b5c35-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="b5c35-310">![Uued testjuhtumid valitud katseplaani jaoks](media/GER-RSAT-DevOps-Tests-Passed.png "Kuvatõmmis uutest testjuhtumitest valitud katseplaani jaoks")</span><span class="sxs-lookup"><span data-stu-id="b5c35-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="b5c35-311">Pöörake tähelepanu lisatud testide õigele käivitamisjärjekorrale.</span><span class="sxs-lookup"><span data-stu-id="b5c35-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="b5c35-312">Valmistage RSAT ette salvestatud testide käivitamiseks</span><span class="sxs-lookup"><span data-stu-id="b5c35-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="b5c35-313">Laadige testid Azure DevOps-ist RSAT-sse</span><span class="sxs-lookup"><span data-stu-id="b5c35-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="b5c35-314">Avab kohalik RSATi rakendus praeguses topoloogias.</span><span class="sxs-lookup"><span data-stu-id="b5c35-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="b5c35-315">Valige **Lae**, et laadida praegu Azure DevOps-is olevad testid RSAT-sse.</span><span class="sxs-lookup"><span data-stu-id="b5c35-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="b5c35-316">![RSAT-sse laetud testid](media/GER-RSAT-RSAT-Tests-Loaded.png "Kuvatõmmis RSAT-sse laetud testidest")</span><span class="sxs-lookup"><span data-stu-id="b5c35-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="b5c35-317">Automatiseerimise ja parameetrite failide loomine</span><span class="sxs-lookup"><span data-stu-id="b5c35-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="b5c35-318">Valige RSAT-is testid, mida soovite Azure DevOps-ist laadida.</span><span class="sxs-lookup"><span data-stu-id="b5c35-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="b5c35-319">Valige RSAT-i automatiseerimise ja parameetrite failide loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="b5c35-320">![RSAT-is loodud RSAT-i automatiseerimise ja parameetrite failid](media/GER-RSAT-RSAT-Tests-Initiated.png "Kuvatõmmis RSAT-is loodud RSAT-i automatiseerimise ja parameetrite failidest")</span><span class="sxs-lookup"><span data-stu-id="b5c35-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="b5c35-321">Parameetrite failide muutmine</span><span class="sxs-lookup"><span data-stu-id="b5c35-321">Modify the parameters files</span></span>

1. <span data-ttu-id="b5c35-322">Valige RSATis testjuhtum **Hankija elektroonilise makse testtöötluseks andmete ettevalmistamine**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="b5c35-323">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-323">Select **Edit**.</span></span>
3. <span data-ttu-id="b5c35-324">Muutke Microsoft Excel-i avatud töövihikus töölehel **Üldine** ettevõtte koodiks **GBSI**, sest seda ettevõtted kasutatakse katse teostamiseks.</span><span class="sxs-lookup"><span data-stu-id="b5c35-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="b5c35-325">Valige RSAT-is testjuhtum **Hankija maksete testtöötlemine kasutades ER-vormingut BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="b5c35-326">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-326">Select **Edit**.</span></span>
6. <span data-ttu-id="b5c35-327">Muutke avatud Exceli töövihikus töölehel **Üldine** ettevõtte koodiks **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="b5c35-328">Pange tähele töölehel **ERFormatMappingRunLogTable**, et lahtrid A:3 ja C:3 sisaldavad elektroonilise aruandluse silumislogi tabeli väljade teksti, mida kasutatakse tulemuste kinnitamiseks võrreldes algväärtuse väljundiga.</span><span class="sxs-lookup"><span data-stu-id="b5c35-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="b5c35-329">Neid tekste kasutatakse nende elektroonilise aruandluse silumislogi kirjete hindamiseks, mis katse käigus loodi.</span><span class="sxs-lookup"><span data-stu-id="b5c35-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="b5c35-330">![ERFormatMappingRunLogTable tööleht](media/GER-RSAT-RSAT-ExcelParameters.png "Kuvatõmmis ERFormatMappingRunLogTable töölehest")</span><span class="sxs-lookup"><span data-stu-id="b5c35-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="b5c35-331">Testide teostamine ja tulemuste analüüs</span><span class="sxs-lookup"><span data-stu-id="b5c35-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="b5c35-332">Teostage RSATis testid</span><span class="sxs-lookup"><span data-stu-id="b5c35-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="b5c35-333">Valige RSATis laaditud testid.</span><span class="sxs-lookup"><span data-stu-id="b5c35-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="b5c35-334">Valige käsk **Käitus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-334">Select **Run**.</span></span>

<span data-ttu-id="b5c35-335">Pange tähele, et testjutumid käivitatakse rakenduses automaatselt veebibrauseri abil.</span><span class="sxs-lookup"><span data-stu-id="b5c35-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="b5c35-336">Testitulemuste analüüsimine</span><span class="sxs-lookup"><span data-stu-id="b5c35-336">Analyze the results of test execution</span></span>

<span data-ttu-id="b5c35-337">Testitulemused salvestatakse RSATis.</span><span class="sxs-lookup"><span data-stu-id="b5c35-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="b5c35-338">Pange tähele, et mõlemad testid on läbitud.</span><span class="sxs-lookup"><span data-stu-id="b5c35-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="b5c35-339">![RSAT-i läbinud testid](media/GER-RSAT-RSAT-Tests-Passed.png "Kuvatõmmis RSAT-i läbinud testidest")</span><span class="sxs-lookup"><span data-stu-id="b5c35-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="b5c35-340">Pange tähele, et testitulemused saadetakse ka rakendusse Azure DevOps et saaksite teha edasisi analüüse.</span><span class="sxs-lookup"><span data-stu-id="b5c35-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="b5c35-341">![Testitulemused rakenduses Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Kuvatõmmis testitulemustest rakenduses Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="b5c35-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="b5c35-342">Testide ebaõnnestumise simuleerimine</span><span class="sxs-lookup"><span data-stu-id="b5c35-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="b5c35-343">See testikomplekt peab nurjuma, kui vähemalt üks loodud väljunditest ei vasta vastavale algväärtusele.</span><span class="sxs-lookup"><span data-stu-id="b5c35-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="b5c35-344">Selle olukorra saavutamiseks saate kasutada oma tuletatud versiooni **BACS (UK)** vormingust, mis loob makse faili, millel on erinev sisu kui vastaval algväärtusel.</span><span class="sxs-lookup"><span data-stu-id="b5c35-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="b5c35-345">Selle olukorra simuleerimiseks saate kasutada sama **BACS (UK)** vormingut, kuid muutke makse summat töödeldud makse real.</span><span class="sxs-lookup"><span data-stu-id="b5c35-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="b5c35-346">Avage rakendus ja minge lehele **Makstaolevad arved \> Maksed \> Maksepäevik**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="b5c35-347">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-347">Select **Lines**.</span></span>
3. <span data-ttu-id="b5c35-348">Valige makse rida ja seejärel valige **Makse olek \> Puudub**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="b5c35-349">Muutke välja **Deebet** väärtus **1 000,00** pealt **2 000,00** peale.</span><span class="sxs-lookup"><span data-stu-id="b5c35-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="b5c35-350">Oma muudatuste salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="b5c35-351">Teostage RSATis testid</span><span class="sxs-lookup"><span data-stu-id="b5c35-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="b5c35-352">Valige RSATis laaditud testid.</span><span class="sxs-lookup"><span data-stu-id="b5c35-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="b5c35-353">Valige käsk **Käitus**.</span><span class="sxs-lookup"><span data-stu-id="b5c35-353">Select **Run**.</span></span>

<span data-ttu-id="b5c35-354">Pange tähele, et testjutumid käivitatakse rakenduses automaatselt veebibrauseri abil.</span><span class="sxs-lookup"><span data-stu-id="b5c35-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="b5c35-355">Testitulemuste analüüsimine</span><span class="sxs-lookup"><span data-stu-id="b5c35-355">Analyze the results of test execution</span></span>

<span data-ttu-id="b5c35-356">Testitulemused salvestatakse RSATis.</span><span class="sxs-lookup"><span data-stu-id="b5c35-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="b5c35-357">Pange tähele, et teine katse nurjus teise käivitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="b5c35-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="b5c35-358">![Nurjunud testi tulemused RSAT-is](media/GER-RSAT-RSAT-Tests-Failed.png "Kuvatõmmis nurjunud testi tulemustest RSAT-is")</span><span class="sxs-lookup"><span data-stu-id="b5c35-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="b5c35-359">Pange tähele, et testitulemused saadetakse ka rakendusse Azure DevOps et saaksite teha edasisi analüüse.</span><span class="sxs-lookup"><span data-stu-id="b5c35-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="b5c35-360">![Nurjunud testi tulemused rakenduses Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Kuvatõmmis nurjunud testi tulemustest rakenduses Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="b5c35-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="b5c35-361">Saade juurdepääsu iga testi olekule.</span><span class="sxs-lookup"><span data-stu-id="b5c35-361">You can access the status of each test.</span></span> <span data-ttu-id="b5c35-362">Saate juurdepääsu ka käivitamise logile, et saaksite analüüsida mistahes nurjumise põhjuseid.</span><span class="sxs-lookup"><span data-stu-id="b5c35-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="b5c35-363">Järgmisel joonisel näitab käivitamis elogi, et tõrge tekkis seetõttu, et loodud makse faili ja selle algväärtuse sisu oli erinev.</span><span class="sxs-lookup"><span data-stu-id="b5c35-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="b5c35-364">![Käivitumise logi rakenduses Azure DevOps nurjumise analüüsimiseks](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Kuvatõmmis käivituse logist rakenduses Azure DevOps nurjumise analüüsimiseks")</span><span class="sxs-lookup"><span data-stu-id="b5c35-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="b5c35-365">Seetõttu, nagu olete näinud, saab mis tahes ER-vormingu toimimist hinnata automaatselt, kasutades RSAT testimise platvormina ja kasutades tegevuse salvestajal põhinevaid testjuhtumeid, mis kasutavad ER-i algväärtuse funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="b5c35-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5c35-366">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b5c35-366">Additional resources</span></span>

- [<span data-ttu-id="b5c35-367">Tegevuse salvestaja ressursid</span><span class="sxs-lookup"><span data-stu-id="b5c35-367">Task recorder resources</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="b5c35-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="b5c35-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="b5c35-369">Kasutaja vastuvõtu testide loomine ja automatiseerimine</span><span class="sxs-lookup"><span data-stu-id="b5c35-369">Create and automate user acceptance tests</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="b5c35-370">Pideva koostamise ja testimise automaatikat toetavate keskkondade juurutamine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="b5c35-370">Deploy and use an environment that supports continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="b5c35-371">Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega</span><span class="sxs-lookup"><span data-stu-id="b5c35-371">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="b5c35-372">Elektrooniline aruandlus. Vormingu täiendamine uue alusversiooni kasutuselevõtuga</span><span class="sxs-lookup"><span data-stu-id="b5c35-372">ER Upgrade your format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="b5c35-373">Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b5c35-373">ER Import a configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)
