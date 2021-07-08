---
title: Uue ER-i lahenduse kujundamine kohandatud aruande printimiseks
description: Selles teemas selgitatakse, kuidas kujundada elektroonilise aruandluse (ER) lahendust kohandatud aruande printimiseks.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90e5381c2d30753e3ad82a38d7361b411f1d7a87
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304389"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="0aa4f-103">Uue ER-i lahenduse kujundamine kohandatud aruande printimiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0aa4f-104">Järgmistes etappides on seletatud, kuidas süsteemiadministraatori, elektroonilise aruandluse arendaja või elektroonilise aruandluse funktsionaalse konsultandi rolli omav kasutaja saab konfigureerida ER-i raamistiku parameetreid, kujundada uue ER-i lahenduse jaoks vajalikke ER-i konfiguratsioone, et pääseda juurde konkreetse äridomeeni andmetele ja luua kohandatud aruannet Microsoft Office'i vormingus.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="0aa4f-105">Neid toiminguid saab teha ettevõttes **USMF**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="0aa4f-106">ER-raamistiku konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="0aa4f-107">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="0aa4f-108">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="0aa4f-109">ER-konfiguratsiooni pakkujate loendi ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="0aa4f-110">Uue ER-vormingu konfiguratsioonipakkuja lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="0aa4f-111">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="0aa4f-112">Domeenipõhise andmemudeli kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="0aa4f-113">Uue andmemudeli konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="0aa4f-114">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="0aa4f-115">Andmemudelile nime panemine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="0aa4f-116">Andmemudeli väljade lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="0aa4f-117">Andmemudeli kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="0aa4f-118">Mudelivastenduse kujundamine konfigureeritud andmemudelile</span><span class="sxs-lookup"><span data-stu-id="0aa4f-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="0aa4f-119">Uue mudelivastenduse konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="0aa4f-120">Uue mudelivastenduse konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="0aa4f-121">Uue mudelivastenduse komponendi kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="0aa4f-122">Andmeallikate lisamine rakenduse tabelitele juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="0aa4f-123">Andmeallikate lisamine rakenduse loeteludele juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="0aa4f-124">ER-i siltide lisamine aruande loomiseks määratud keeles</span><span class="sxs-lookup"><span data-stu-id="0aa4f-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="0aa4f-125">Andmeallika lisamine loetelu väärtuste võrdlemise tulemuste muutmiseks tekstiväärtuseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="0aa4f-126">Andmeallikate sidumine andmemudeli väljadega</span><span class="sxs-lookup"><span data-stu-id="0aa4f-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="0aa4f-127">Mudelivastenduse kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="0aa4f-128">Kohandatud aruande malli kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="0aa4f-129">Vormingu kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="0aa4f-130">Kujundatud vormingu konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="0aa4f-131">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="0aa4f-132">Aruandemalli importimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="0aa4f-133">Vormingu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="0aa4f-134">Andmesidumise määratlemine aruande pealkirja jaoks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="0aa4f-135">Mudeli andmeallika ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="0aa4f-136">Vorminguelementide sidumine andmeallika väljadega</span><span class="sxs-lookup"><span data-stu-id="0aa4f-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="0aa4f-137">Kujundatud vormingu käivitamine ER-is</span><span class="sxs-lookup"><span data-stu-id="0aa4f-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="0aa4f-138">Kujundatud vormingu häälestamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="0aa4f-139">Vormingu muutmine loodud dokumendi nime muutmiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="0aa4f-140">Vormingu muutmine küsimuste järjekorra muutmiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="0aa4f-141">Muudetud vormingu käivitamine ER-is</span><span class="sxs-lookup"><span data-stu-id="0aa4f-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="0aa4f-142">Vormingu kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="0aa4f-143">Rakenduse artefaktide arendamine kujundatud aruande kutsumiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="0aa4f-144">Lähtekoodi muutmine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="0aa4f-145">Andmelepingu klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="0aa4f-146">UI-koostaja klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="0aa4f-147">Andmepakkuja klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="0aa4f-148">Siltide faili lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="0aa4f-149">Aruandeteenuse klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="0aa4f-150">Aruandekontrolleri klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="0aa4f-151">Menüüelemendi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="0aa4f-152">Menüüelemendi lisamine menüüle</span><span class="sxs-lookup"><span data-stu-id="0aa4f-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="0aa4f-153">Visual Studio projekti koostamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="0aa4f-154">Vormingu käivitamine rakenduses</span><span class="sxs-lookup"><span data-stu-id="0aa4f-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="0aa4f-155">Kujundatud ER-i lahenduse häälestamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="0aa4f-156">Mudelivastenduse muutmine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="0aa4f-157">Andmeallikate lisamine andmelepingu objektile juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="0aa4f-158">Andmeallika lisamine ER-i vorminguvastenduse kirjetele juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="0aa4f-159">Andmeallika lisamine töötava ER-i vorminguvastenduse kirjele juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="0aa4f-160">Töötava ER-i vormingu nime sisestamine andmemudelisse</span><span class="sxs-lookup"><span data-stu-id="0aa4f-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="0aa4f-161">Mudelivastenduse kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="0aa4f-162">Vormingu muutmine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="0aa4f-163">Uue vorminguelemendi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="0aa4f-164">Lisatud vorminguelemendi sidumine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="0aa4f-165">Vormingu kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="0aa4f-166">Vormingu käivitamine rakenduses</span><span class="sxs-lookup"><span data-stu-id="0aa4f-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="0aa4f-167">Vormingu käivitamine ER-is</span><span class="sxs-lookup"><span data-stu-id="0aa4f-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="0aa4f-168">Vormingu sihtkoha konfigureerimine ekraanil eelvaatamiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="0aa4f-169">Vormingu käivitamine rakenduses selle eelvaatamiseks PDF-dokumendina</span><span class="sxs-lookup"><span data-stu-id="0aa4f-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="0aa4f-170">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0aa4f-170">Additional resources</span></span>](#References)

<span data-ttu-id="0aa4f-171">Selles näites loote uue ER-i lahenduse mooduli [Küsimustik](../../../human-resources/hr-learning-questionnaires.md) jaoks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-171">In this example, you will create a new ER solution for the [Questionnaire](../../../human-resources/hr-learning-questionnaires.md) module.</span></span> <span data-ttu-id="0aa4f-172">See uus ER-i lahendus võimaldab teil kujundada aruande, kasutades Microsoft Exceli töölehte mallina.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="0aa4f-173">Seejärel saate lisaks olemasoleva SQL Serveri aruandlusteenuste (SSRS) aruande loomisele luua aruande **Küsimustik** Excelis või PDF-vormingus.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="0aa4f-174">Vajaduse korral saate uut aruannet ka hiljem muuta.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="0aa4f-175">Koodi pole vaja kirjutada.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-175">No coding is required.</span></span>

1. <span data-ttu-id="0aa4f-176">Olemasoleva aruande käivitamiseks avage **Küsimustik** \> **Kujundus** \> **Küsimustike aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Küsimustike aruande menüüelemendi valimine küsimustiku moodulis, et käivitada olemasolev SSRS-aruanne](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="0aa4f-178">Määrake dialoogiboksis **Küsimustike aruanne** valikukriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="0aa4f-179">Lisage filter, et aruanne sisaldaks ainult küsimustikku **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Valikukriteeriumide täpsustamine küsimustike aruande dialoogiboksis](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="0aa4f-181">Järgmisel illustratsioonil on kujutatud SSRS-i aruande loodud versioon küsimustiku **SBCCrsExam** jaoks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Loodud SSRS-aruanne](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="0aa4f-183">ER-raamistiku konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-183">Configure the ER framework</span></span>

<span data-ttu-id="0aa4f-184">Elektroonilise aruandluse arendaja rollis kasutajana peate konfigureerima minimaalse ER-i parameetrite kogumi, enne kui saate hakata kasutama ER-i raamistikku oma uue ER-i lahenduse kujundamiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="0aa4f-185">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-185">Configure ER parameters</span></span>

1. <span data-ttu-id="0aa4f-186">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0aa4f-187">Tööruumis **Elektrooniline aruandlus** valige **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="0aa4f-188">Valige lehel **Elektroonilise aruandluse parameetrid** vahekaardil **Üldine** suvandi **Luba kujundusrežiim** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="0aa4f-189">Vahekaardil **Manused** määrake järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="0aa4f-190">Seadke välja **Konfiguratsioonid** väärtuseks **Fail** ettevõtte **USMF** jaoks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="0aa4f-191">Seadke väljade **Tööarhiiv**, **Ajutine**, **Alus** ja **Muud** väärtuseks **Fail**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="0aa4f-192">Lisateavet ER-parameetrite kohta vt jaotisest [ER-raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="0aa4f-193">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="0aa4f-194">Kõigi ER-i konfiguratsioonide omanikuks on märgitud ER-i konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="0aa4f-195">Seega peate enne ER-i konfiguratsioonide lisamist või redigeerimist aktiveerima tööruumis **Elektrooniline aruandlus** ER-i konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="0aa4f-196">ER-konfiguratsiooni saab redigeerida ainult selle omanik.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="0aa4f-197">Seega enne ER-konfiguratsiooni redigeerimist pea olema tööruumis **Elektrooniline aruandlus** aktiveeriud vastav ER-konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="0aa4f-198">ER-konfiguratsiooni pakkujate loendi ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="0aa4f-199">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0aa4f-200">Valige tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** suvand **Konfiguratsioonipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="0aa4f-201">Lehel **Konfiguratsioonipakkujad** on igal konfiguratsioonipakkuja kirjel kordumatu nimi ja URL.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="0aa4f-202">Vaadake üle selle lehe sisu.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-202">Review the contents of this page.</span></span> <span data-ttu-id="0aa4f-203">Kui üksuse **Litware, Inc.** (`https://www.litware.com`) kirje on juba olemas, jätke järgmine protseduur vahele [Uue ER-konfiguratsiooni pakkuja lisamine](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="0aa4f-204">Uue ER-konfiguratsiooni pakkuja lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="0aa4f-205">Lehel **Konfiguratsioonipakkujad** valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="0aa4f-206">Väljale **Nimi** sisestage väärtus **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="0aa4f-207">Sisestage väljale **Interneti-aadress** `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="0aa4f-208">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="0aa4f-209">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="0aa4f-210">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0aa4f-211">Valige tööruumis **Elektrooniline aruandlus** konfiguratsioonipakkuja **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="0aa4f-212">Valige **Määra aktiivseks**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-212">Select **Set active**.</span></span>

<span data-ttu-id="0aa4f-213">Lisateabe saamiseks ER-konfiguratsiooni pakkujate kohta vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="0aa4f-214">Domeenipõhise andmemudeli kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-214">Design a domain-specific data model</span></span>

<span data-ttu-id="0aa4f-215">Peate looma uue ER-i konfiguratsiooni, mis sisaldab [andmemudeli](general-electronic-reporting.md#data-model-and-model-mapping-components) komponenti **Küsimustiku** äridomeeni jaoks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="0aa4f-216">Seda andmemudelit kasutatakse hiljem andmeallikana, kui kujundate ER-i vormingut aruande **Küsimustik** loomiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="0aa4f-217">Kui täidate jaotises [Uue andmemudeli konfiguratsiooni importimine](#ImportDataModel) toodud juhised, saate vajaliku andmemudeli importida esitatud XML-failist.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="0aa4f-218">Teise võimalusena saate täita jaotise [Uue andmemudeli konfiguratsiooni loomine](#DesignDataModel) juhised, et kujundada see andmemudel täiesti algusest.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="0aa4f-219">Uue andmemudeli konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="0aa4f-220">Laadige alla fail [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) ja salvestage see oma kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-220">Download the [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="0aa4f-221">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0aa4f-222">Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="0aa4f-223">Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="0aa4f-224">Valige **Sirvi** ning seejärel otsige üles ja valige fail **Questionnaires model.version.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="0aa4f-225">Konfiguratsiooni importimiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="0aa4f-226">Jätkamiseks jätke järgmine protseduur [Uue andmemudeli konfiguratsiooni loomine](#DesignDataModel) vahele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="0aa4f-227">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="0aa4f-228">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="0aa4f-229">Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="0aa4f-230">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="0aa4f-231">Sisestage rippdialoogiboksi väljale **Nimi** tekst **Küsimustiku mudel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="0aa4f-232">Konfiguratsiooni loomiseks valige **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="0aa4f-233">Andmemudelile nime panemine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-233">Name the data model</span></span>

1. <span data-ttu-id="0aa4f-234">Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku mudel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="0aa4f-235">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-235">Select **Designer**.</span></span>
3. <span data-ttu-id="0aa4f-236">Sisestage lehe **Andmemudeli kujundaja** kiirkaardi **Üldine** väljale **Nimi** tekst <a name="DataModeName"></a>**Questionnaires**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="0aa4f-237">Uute andmemudeli väljade lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-237">Add new data model fields</span></span>

1. <span data-ttu-id="0aa4f-238">Valige lehel **Andmemudeli kujundaja** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="0aa4f-239">Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-240">Valige uue sõlme tüübiks **Mudeli juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="0aa4f-241">Sisestage väljale **Nimi** tekst <a name="RootDefinitionName"></a>**Root**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="0aa4f-242">Uue sõlme lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="0aa4f-243">Seda juuredeskriptorit kasutatakse aruande **Küsimustik** jaoks andmete esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="0aa4f-244">Ühel andmemudelil võib olla mitu deskriptorit.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="0aa4f-245">Igat deskriptorit saab määrata ühe ER-i vormingu jaoks, et tuvastada aruande loomiseks vajalikud andmed.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="0aa4f-246">Valige uuesti **Uus** ja seejärel järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-247">Valige uue sõlme tüübiks **Aktiivse sõlme tütar**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="0aa4f-248">Sisestage väljale **Nimi** tekst **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="0aa4f-249">Valige väljalt **Üksuse tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="0aa4f-250">Uue välja lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="0aa4f-251">Seda välja on vaja, et edastada praeguse ettevõtte nimi ER-i aruandesse, mis kasutab seda andmemudelit andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="0aa4f-252">Valige uuesti **Uus** ja seejärel järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-253">Valige uue sõlme tüübiks **Aktiivse sõlme tütar**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="0aa4f-254">Sisestage väljale **Nimi** tekst **Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="0aa4f-255">Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="0aa4f-256">Uue välja lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="0aa4f-257">Seda välja kasutatakse selleks, et edastada küsimustike loend ER-i aruandesse, mis kasutab seda andmemudelit andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="0aa4f-258">Valige sõlm **Küsimustik**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="0aa4f-259">Jätkake samal viisil vajalike väljade lisamist redigeeritavasse andmemudelisse, kuni olete lõpetanud järgmise andmemudeli struktuuri.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="0aa4f-260">Välja tee</span><span class="sxs-lookup"><span data-stu-id="0aa4f-260">Field path</span></span>                                                    | <span data-ttu-id="0aa4f-261">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="0aa4f-261">Data type</span></span>   | <span data-ttu-id="0aa4f-262">Välja kirjeldus / tagastatav väärtus</span><span class="sxs-lookup"><span data-stu-id="0aa4f-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="0aa4f-263">Juur</span><span class="sxs-lookup"><span data-stu-id="0aa4f-263">Root</span></span>                                                          |             | <span data-ttu-id="0aa4f-264">Viitepunkt küsimustiku andmete taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="0aa4f-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="0aa4f-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="0aa4f-266">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-266">String</span></span>      | <span data-ttu-id="0aa4f-267">Praeguse ettevõtte nimi.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-267">The name of the current company.</span></span> |
    | <span data-ttu-id="0aa4f-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="0aa4f-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="0aa4f-269">Salvestamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-269">Record</span></span>      | <span data-ttu-id="0aa4f-270">Vormingu käivitamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-270">Format execution details.</span></span> |
    | <span data-ttu-id="0aa4f-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="0aa4f-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="0aa4f-272">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-272">String</span></span>      | <span data-ttu-id="0aa4f-273">Käivitatud ER-i vormingu nimi.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="0aa4f-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="0aa4f-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="0aa4f-275">Kirjete loend</span><span class="sxs-lookup"><span data-stu-id="0aa4f-275">Record list</span></span> | <span data-ttu-id="0aa4f-276">Küsimustike loend</span><span class="sxs-lookup"><span data-stu-id="0aa4f-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="0aa4f-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="0aa4f-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="0aa4f-278">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-278">String</span></span>      | <span data-ttu-id="0aa4f-279">Praeguse küsimustiku olek.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="0aa4f-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="0aa4f-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="0aa4f-281">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-281">String</span></span>      | <span data-ttu-id="0aa4f-282">Praeguse küsimustiku kood.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="0aa4f-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="0aa4f-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="0aa4f-284">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-284">String</span></span>      | <span data-ttu-id="0aa4f-285">Praeguse küsimustiku kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="0aa4f-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="0aa4f-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="0aa4f-287">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-287">String</span></span>      | <span data-ttu-id="0aa4f-288">Praeguse küsimustiku tüüp.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="0aa4f-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="0aa4f-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="0aa4f-290">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-290">String</span></span>      | <span data-ttu-id="0aa4f-291">Praeguse küsimustiku numbriline järjekord.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="0aa4f-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="0aa4f-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="0aa4f-293">Salvestamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-293">Record</span></span>      | <span data-ttu-id="0aa4f-294">Praeguse küsimustiku tulemuste parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="0aa4f-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="0aa4f-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="0aa4f-296">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-296">String</span></span>      | <span data-ttu-id="0aa4f-297">Praeguse tulemusegrupi identifitseerimiskood.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="0aa4f-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="0aa4f-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="0aa4f-299">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-299">String</span></span>      | <span data-ttu-id="0aa4f-300">Praeguse tulemusegrupi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="0aa4f-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="0aa4f-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="0aa4f-302">Tegelik</span><span class="sxs-lookup"><span data-stu-id="0aa4f-302">Real</span></span>        | <span data-ttu-id="0aa4f-303">Maksimaalne punktide arv, mida on võimalik saada.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="0aa4f-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="0aa4f-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="0aa4f-305">Kirjete loend</span><span class="sxs-lookup"><span data-stu-id="0aa4f-305">Record list</span></span> | <span data-ttu-id="0aa4f-306">Praeguse küsimustiku küsimuste loend.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="0aa4f-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="0aa4f-308">Täisarv</span><span class="sxs-lookup"><span data-stu-id="0aa4f-308">Integer</span></span>     | <span data-ttu-id="0aa4f-309">Praeguse vastuste kogumi järjekorranumber.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="0aa4f-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="0aa4f-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="0aa4f-311">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-311">String</span></span>      | <span data-ttu-id="0aa4f-312">Praeguse küsimuse identifitseerimiskood.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="0aa4f-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="0aa4f-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="0aa4f-314">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-314">String</span></span>      | <span data-ttu-id="0aa4f-315">Lipp, mis näitab, kas praegusele küsimusele tuleb vastata.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="0aa4f-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="0aa4f-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="0aa4f-317">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-317">String</span></span>      | <span data-ttu-id="0aa4f-318">Lipp, mis näitab, kas praegune küsimus on esmane.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="0aa4f-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="0aa4f-320">Täisarv</span><span class="sxs-lookup"><span data-stu-id="0aa4f-320">Integer</span></span>     | <span data-ttu-id="0aa4f-321">Praeguse küsimuse järjekorranumber.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="0aa4f-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="0aa4f-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="0aa4f-323">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-323">String</span></span>      | <span data-ttu-id="0aa4f-324">Praeguse küsimuse tekst.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-324">The text of the current question.</span></span> |
    | <span data-ttu-id="0aa4f-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="0aa4f-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="0aa4f-326">Kirjete loend</span><span class="sxs-lookup"><span data-stu-id="0aa4f-326">Record list</span></span> | <span data-ttu-id="0aa4f-327">Praeguse küsimuse vastuste loend.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="0aa4f-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="0aa4f-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="0aa4f-329">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-329">String</span></span>      | <span data-ttu-id="0aa4f-330">Lipp, mis näitab, kas praegune vastus on õige.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="0aa4f-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="0aa4f-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="0aa4f-332">Tegelik</span><span class="sxs-lookup"><span data-stu-id="0aa4f-332">Real</span></span>        | <span data-ttu-id="0aa4f-333">Punktid, mis saadakse praeguse vastuse valimisel.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="0aa4f-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="0aa4f-335">Täisarv</span><span class="sxs-lookup"><span data-stu-id="0aa4f-335">Integer</span></span>     | <span data-ttu-id="0aa4f-336">Praeguse vastuse järjekorranumber.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="0aa4f-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="0aa4f-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="0aa4f-338">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-338">String</span></span>      | <span data-ttu-id="0aa4f-339">Praeguse vastuse tekst.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-339">The text of the current answer.</span></span> |

    <span data-ttu-id="0aa4f-340">Järgmisel illustratsioonil on kujutatud lõpule viidud redigeeritav andmemudel lehel **Andmemudeli kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Konfigureeritud andmemudel ER-i andmemudeli kujundajas](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="0aa4f-342">Salvestage muudatused.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-342">Save your changes.</span></span>
8. <span data-ttu-id="0aa4f-343">Sulgege leht **Andmemudeli kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="0aa4f-344">Andmemudeli kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="0aa4f-345">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-346">Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku mudel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="0aa4f-347">Valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="0aa4f-348">Valige **Muuda olekut** \> **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0aa4f-349">Selle konfiguratsiooni versiooni 1 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0aa4f-350">Versiooni 1 ei saa enam muuta.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="0aa4f-351">See versioon sisaldab konfigureeritud andmemudelit ja seda saab kasutada teiste ER-i konfiguratsioonide alusena.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="0aa4f-352">Luuakse selle konfiguratsiooni versioon 2, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0aa4f-353">Saate seda versiooni redigeerida, et kohandada andmemudelit **Küsimustik**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Redigeeritava ER-i konfiguratsiooni versioonid konfiguratsioonide lehel](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="0aa4f-355">Lisateavet ER-i konfiguratsioonide versioonide kohta leiate teemast [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="0aa4f-356">Konfigureeritud andmemudel esindab abstraktselt äridomeeni **Küsimustik** ega ole seotud artefaktidega, mis kuuluvad rakendusse Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="0aa4f-357">Mudelivastenduse kujundamine konfigureeritud andmemudelile</span><span class="sxs-lookup"><span data-stu-id="0aa4f-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="0aa4f-358">Elektroonilise aruandluse arendaja rollis kasutajana peate looma uue ER-i konfiguratsiooni, mis sisaldab [mudelivastenduse](general-electronic-reporting.md#data-model-and-model-mapping-components) komponenti andmemudeli **Küsimustik** jaoks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="0aa4f-359">Kuna see komponent kasutab Finance'i jaoks mõeldud konfigureeritud andmemudelit, on see rakenduse Finance põhine.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="0aa4f-360">Peate konfigureerima mudelivastenduse komponendi, et määrata rakenduse objektid, mida tuleb käitusajal kasutada rakenduse andmete lisamiseks konfigureeritud andmemudelisse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="0aa4f-361">Selle ülesande lõpetamiseks peate teadma Finance'is oleva äridomeeni **Küsimustik** andmestruktuuri juurutamise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="0aa4f-362">Kui täidate järgnevas jaotises [Uue mudelivastenduse konfiguratsiooni importimine](#ImportModelMapping) toodud juhised, saate vajaliku mudelivastenduse konfiguratsiooni importida esitatud XML-failist.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="0aa4f-363">Teise võimalusena saate täita jaotise [Uue mudelivastenduse konfiguratsiooni loomine](#CreateModelMapping) juhised, et kujundada see mudelivastendus täiesti algusest.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="0aa4f-364">Uue mudelivastenduse konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="0aa4f-365">Laadige alla fail [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) ja salvestage see oma kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-365">Download the [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="0aa4f-366">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0aa4f-367">Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="0aa4f-368">Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="0aa4f-369">Valige **Sirvi** ning seejärel otsige üles ja valige fail **Questionnaires mapping.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="0aa4f-370">Konfiguratsiooni importimiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="0aa4f-371">Jätkamiseks jätke järgmine protseduur [Uue mudelivastenduse konfiguratsiooni loomine](#CreateModelMapping) vahele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="0aa4f-372">Uue mudelivastenduse konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="0aa4f-373">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-374">Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku mudel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="0aa4f-375">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="0aa4f-376">Dialoogiakna ripploendis järgige allolevaid etappe.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-377">Valige väljal **Uus** suvand **Küsimustike andmemudelil põhinev mudelivastendus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="0aa4f-378">Sisestage väljale **Nimi** tekst **Küsimustiku vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="0aa4f-379">Valige väljal **Andmemudeli definitsioon** definitsioon **Juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="0aa4f-380">Konfiguratsiooni loomiseks valige **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="0aa4f-381">Uue mudelivastenduse komponendi kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="0aa4f-382">Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="0aa4f-383">Valige **Kujundaja**, et avada vastenduste loend.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="0aa4f-384">Valige vastendus **Küsimustike vastendamine**, mis lisati automaatselt definitsiooni **Juur** jaoks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="0aa4f-385">Valige **Kujundaja**, et alustada valitud vastenduse konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="0aa4f-386">Definitsiooni **Juur** jaoks lisatakse automaatselt uus vastendus.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="0aa4f-387">Sellel vastendusel suund **Mudelisse**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="0aa4f-388">Seetõttu saab seda vastendust kasutada selleks, et lisada vajalikud andmed andmemudelisse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="0aa4f-389">Andmeallikate lisamine rakenduse tabelitele juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-389">Add data sources to access application tables</span></span>

<span data-ttu-id="0aa4f-390">Peate konfigureerima andmeallikad, et pääseda juurde küsimustiku üksikasju sisaldavatele rakenduse tabelitele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="0aa4f-391">Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="0aa4f-392">Lisage uus andmeallikas, mida kasutatakse tabelile KMCollection juurdepääsemiseks, kus iga kirje tähistab ühte küsimustikku.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="0aa4f-393">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0aa4f-394">Sisestage dialoogiboksis väljale **Nimi** väärtus **Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="0aa4f-395">Sisestage väljale **Tabel** väärtus **KMCollection**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="0aa4f-396">Määrake suvandi **Küsi päringut** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="0aa4f-397">Seejärel saate selle tabeli jaoks määrata [filtreerimissuvandid](../../fin-ops/get-started/advanced-filtering-query-options.md), mida rakendatakse käitusajal süsteemipäringu dialoogiboksis.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="0aa4f-398">Uue andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="0aa4f-399">Valige paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="0aa4f-400">Lisage uus andmeallikas, mida kasutatakse tabelile KMQuestion juurdepääsemiseks, kus iga kirje tähistab ühte küsimust küsimustikus.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="0aa4f-401">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0aa4f-402">Sisestage dialoogiboksis väljale **Nimi** väärtus **Question**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="0aa4f-403">Sisestage väljale **Tabel** väärtus **KMQuestion**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="0aa4f-404">Uue andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="0aa4f-405">Valige paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="0aa4f-406">Lisage uus andmeallikas, mida kasutatakse tabelile KMAnswer juurdepääsemiseks, kus iga kirje tähistab ühte vastust küsimustikus olevale küsimusele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="0aa4f-407">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0aa4f-408">Väljale **Nimi** sisestage **Answer**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="0aa4f-409">Sisestage väljale **Tabel** väärtus **KMAnswer**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="0aa4f-410">Uue andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="0aa4f-411">Valige paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="0aa4f-412">Lisage uus arvutatud väli, mida kasutatakse selleks, et pääseda ematabeli KMCollection kõikide kirjete kaudu juurde tabeli KMQuestionResultGroup kirjetele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="0aa4f-413">Valige paanil **Andmeallikad** suvand **Küsimustik**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="0aa4f-414">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-414">Select **Add**.</span></span>
    3. <span data-ttu-id="0aa4f-415">Sisestage dialoogiboksis väljale **Nimi** väärtus **\$ResultGroup**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="0aa4f-416">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="0aa4f-417">Sisestage [ER-i valemiredaktoris](general-electronic-reporting-formula-designer.md) väljale **Valem** väärtus **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)**, et kasutada tabelite KMCollection ja KMQuestionResultGroup vahelise üks-mitmele seose [teed](er-formula-language.md#Paths).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#Paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="0aa4f-418">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="0aa4f-419">Uue arvutatud välja lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="0aa4f-420">Valige paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="0aa4f-421">Lisage uus arvutatud väli, mida kasutatakse selleks, et pääseda ematabeli KMCollectionQuestion kõikide kirjete kaudu juurde tabeli KMQuestion küsimusekirjetele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="0aa4f-422">Valige paanil **Andmeallikad** suvand **Küsimustik**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="0aa4f-423">Laiendage sõlme **\<Seosed**, mis sisaldab tabeli KMCollection üks-mitmele seoseid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="0aa4f-424">Valige seotud tabel **KMCollectionQuestion** ja seejärel **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="0aa4f-425">Sisestage dialoogiboksis väljale **Nimi** väärtus **\$Question**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="0aa4f-426">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="0aa4f-427">Sisestage valemiredaktoris väljale **Valem** väärtus **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))**, et tagastada asjakohased küsimusekirjed tabelist KMQuestion.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="0aa4f-428">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="0aa4f-429">Uue arvutatud välja lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="0aa4f-430">Valige paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="0aa4f-431">Lisage uus arvutatud väli, mida kasutatakse selleks, et pääseda ematabeli KMQuestion kõikide kirjete kaudu juurde tabeli KMAnswer vastusekirjetele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="0aa4f-432">Valige paanil **Andmeallikad** suvand **Questionnaire.\<Relations.KMCollectionQuestion.\$Question** ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="0aa4f-433">Sisestage dialoogiboksis väljale **Nimi** väärtus **\$Answer**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="0aa4f-434">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="0aa4f-435">Sisestage valemiredaktoris väljale **Valem** väärtus **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)**, et tagastada asjakohased vastusekirjed tabelist KMAnswer.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="0aa4f-436">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="0aa4f-437">Uue arvutatud välja lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="0aa4f-438">Valige paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="0aa4f-439">Lisage uus andmeallikas, mida kasutatakse tabeli CompanyInfo meetoditele juurdepääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="0aa4f-440">Pange tähele, et selle tabeli meetod **find()** tagastab kirje, mis tähistab Finance'i praeguse eksemplari ettevõtet, mille jaoks seda vastendust kutsutakse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="0aa4f-441">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0aa4f-442">Sisestage dialoogiboksis väljale **Nimi** väärtus **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="0aa4f-443">Sisestage väljale **Tabel** väärtus **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="0aa4f-444">Uue andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="0aa4f-445">Andmeallikate lisamine rakenduse loeteludele juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="0aa4f-446">Peate konfigureerima andmeallikad, et pääseda rakenduse loeteludele juurde ja võrrelda nende väärtusi rakenduse tabelites olevate väljade väärtustega, mille tüüp on **Loetelu**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="0aa4f-447">Peate kasutama võrdluse tulemust andmemudeli asjakohaste väljade täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="0aa4f-448">Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Loetelu**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="0aa4f-449">Lisage uus andmeallikas, mida kasutatakse loetelu **EnumAppNoYes** väärtustele juurdepääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="0aa4f-450">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0aa4f-451">Sisestage dialoogiboksis väljale **Nimi** väärtus **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="0aa4f-452">Sisestage väljale **Loetelu** väärtus **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="0aa4f-453">Uue andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="0aa4f-454">Valige paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Loetelu**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="0aa4f-455">Lisage uus andmeallikas, mida kasutatakse loetelu **KMCollectionQuestionMode** väärtustele juurdepääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="0aa4f-456">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0aa4f-457">Sisestage dialoogiboksis väljale **Nimi** väärtus **EnumAppQuestionOrder**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="0aa4f-458">Sisestage väljale **Loetelu** väärtus **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="0aa4f-459">Uue andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="0aa4f-460">ER-i siltide lisamine aruande loomiseks määratud keeles</span><span class="sxs-lookup"><span data-stu-id="0aa4f-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="0aa4f-461">Saate lisada ER-i silte, et konfigureerida mõned oma andmeallikad tagastama väärtusi, mis sõltuvad mudelivastenduse kutse kontekstis määratletud keelest.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="0aa4f-462">Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallikad** suvand **Vastus** ja seejärel **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="0aa4f-463">Aktiveerige väli **Silt**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="0aa4f-464">Valige käsk **Tõlgi**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-464">Select **Translate**.</span></span>
4. <span data-ttu-id="0aa4f-465">Järgige dialoogiboksis **Teksti tõlkimine** allolevaid etappe.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-466">Sisestage väljale **Sildi ID** väärtus **PositiveAnswer**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="0aa4f-467">Sisestage väljale **Tekst vaikekeeles** väärtus **Yes**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="0aa4f-468">Valige käsk **Tõlgi**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="0aa4f-469">Sisestage väljale **Sildi ID** väärtus **NegativeAnswer**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="0aa4f-470">Sisestage väljale **Tekst vaikekeeles** väärtus **No**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="0aa4f-471">Valige käsk **Tõlgi**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-471">Select **Translate**.</span></span>

5. <span data-ttu-id="0aa4f-472">Sulgege dialoogiboks **Teksti tõlkimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="0aa4f-473">Valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-473">Select **Cancel**.</span></span>

![ER-i siltide lisamine redigeeritavale mudelivastendusele](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="0aa4f-475">Sisestasite ER-i sildid ainult vaikekeele jaoks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="0aa4f-476">Lisateavet selle kohta, kuidas ER-i silte saab teistesse keeltesse tõlkida, leiate teemast [Mitmekeelsete aruannete kujundamine](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="0aa4f-477">Andmeallika lisamine loetelu väärtuste võrdlemise tulemuste muutmiseks tekstiväärtuseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="0aa4f-478">Kuna peate võrdlemise tulemused eri allikate jaoks mitu korda loetelu väärtuste ja teksti väärtuste vahel teisendama, on hea mõte konfigureerida see loogika ühe andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="0aa4f-479">Selle andmeallika korduvkasutatavaks muutmiseks peate selle konfigureerima parameetritega andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="0aa4f-480">Lisateavet leiate teemast [Arvutatud välja tüüpi ER-i andmeallikate parameetritega kutsete toetamine](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="0aa4f-481">Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Üldine\\Tühi konteiner**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="0aa4f-482">Lisage uus konteineri tüüpi andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="0aa4f-483">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="0aa4f-484">Sisestage dialoogiboksis väljale **Nimi** väärtus **Helper**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="0aa4f-485">Uue konteineri tüüpi andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="0aa4f-486">Valige paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="0aa4f-487">Lisage uus andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-487">Add a new data source:</span></span>

    1. <span data-ttu-id="0aa4f-488">Valige paanil **Andmeallikad** suvand **Abiline**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="0aa4f-489">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-489">Select **Add**.</span></span>
    3. <span data-ttu-id="0aa4f-490">Sisestage rippdialoogiboksis väljale **Nimi** väärtus **NoYesEnumToString**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="0aa4f-491">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="0aa4f-492">Valige valemiredaktoris **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="0aa4f-493">Konfigureeritud avaldisele parameetrite määramiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="0aa4f-494">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-494">Select **New**.</span></span>
        2. <span data-ttu-id="0aa4f-495">Sisestage dialoogiboksis väljale **Nimi** väärtus **Argument**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="0aa4f-496">Valige väljal **Tüüp** andmetüüp **Kahendmuutuja**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="0aa4f-497">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-497">Select **OK**.</span></span>

    7. <span data-ttu-id="0aa4f-498">Sisestage väljale **Valem** väärtus **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")**, et tagastada asjakohase ER-i sildi tekst, võttes arvesse käivitamise konteksti keelt ja määratletud parameetri väärtust.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="0aa4f-499">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="0aa4f-500">Uue andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-500">Select **OK** to add the new data source.</span></span>

![Konfigureeritud mudelivastendus ER-i mudelivastenduse kujundajas](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="0aa4f-502">Andmeallikate sidumine andmemudeli väljadega</span><span class="sxs-lookup"><span data-stu-id="0aa4f-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="0aa4f-503">Peate siduma konfigureeritud andmeallikad andmemudeli väljadega, et määrata, kuidas andmemudelisse käitusajal rakenduse andmeid lisatakse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="0aa4f-504">Valige lehel **Mudelivastenduse kujundaja** paanil **Andmemudel** suvand **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="0aa4f-505">Laiendage paanil **Andmeallikad** suvand **CompanyInfo** ja järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-506">Laiendage sõlm **CompanyInfo.find()**, mis tähistab tabeli CompanyInfo meetodit **find()**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="0aa4f-507">Valige **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="0aa4f-508">Valige **Seo**, et täita selle ettevõtte nimi, mille jaoks kutsutakse käitusajal konfigureeritud mudelivastendust.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="0aa4f-509">Valige paanil **Andmemudel** suvand **Küsimustik**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="0aa4f-510">Valige paanil **Andmeallikad** suvand **Küsimustik** ja seejärel **Seo**, et täita küsimustiku kirjed.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="0aa4f-511">Laiendage paanil **Andmemudel** suvand **Küsimustik** ja järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-512">Valige paanil **Andmemudel** suvand **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="0aa4f-513">Valige paanil **Andmemudel** suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="0aa4f-514">Sisestage väljale **Valem** väärtus **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)**, et täita loetelu väärtuste võrdluse tulemus, mis sõltub tekstist ja keelest.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="0aa4f-515">Jätkake samal viisil andmeallikate sidumist andmemudeli väljadega, kuni saavutate järgmise tulemuse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="0aa4f-516">Välja tee</span><span class="sxs-lookup"><span data-stu-id="0aa4f-516">Field path</span></span>                                              | <span data-ttu-id="0aa4f-517">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="0aa4f-517">Data type</span></span>   | <span data-ttu-id="0aa4f-518">Tegevus</span><span class="sxs-lookup"><span data-stu-id="0aa4f-518">Action</span></span> | <span data-ttu-id="0aa4f-519">Siduv avaldis</span><span class="sxs-lookup"><span data-stu-id="0aa4f-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="0aa4f-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="0aa4f-520">CompanyName</span></span>                                             | <span data-ttu-id="0aa4f-521">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-521">String</span></span>      | <span data-ttu-id="0aa4f-522">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-522">Bind</span></span>   | <span data-ttu-id="0aa4f-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="0aa4f-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="0aa4f-524">Küsimustik</span><span class="sxs-lookup"><span data-stu-id="0aa4f-524">Questionnaire</span></span>                                           | <span data-ttu-id="0aa4f-525">Kirjete loend</span><span class="sxs-lookup"><span data-stu-id="0aa4f-525">Record list</span></span> | <span data-ttu-id="0aa4f-526">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-526">Bind</span></span>   | <span data-ttu-id="0aa4f-527">Küsimustik</span><span class="sxs-lookup"><span data-stu-id="0aa4f-527">Questionnaire</span></span> |
    | <span data-ttu-id="0aa4f-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="0aa4f-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="0aa4f-529">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-529">String</span></span>      | <span data-ttu-id="0aa4f-530">Redigeeri</span><span class="sxs-lookup"><span data-stu-id="0aa4f-530">Edit</span></span>   | <span data-ttu-id="0aa4f-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="0aa4f-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="0aa4f-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="0aa4f-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="0aa4f-533">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-533">String</span></span>      | <span data-ttu-id="0aa4f-534">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-534">Bind</span></span>   | <span data-ttu-id="0aa4f-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="0aa4f-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="0aa4f-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="0aa4f-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="0aa4f-537">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-537">String</span></span>      | <span data-ttu-id="0aa4f-538">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-538">Bind</span></span>   | <span data-ttu-id="0aa4f-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="0aa4f-539">\@.Description</span></span> |
    | <span data-ttu-id="0aa4f-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="0aa4f-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="0aa4f-541">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-541">String</span></span>      | <span data-ttu-id="0aa4f-542">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-542">Bind</span></span>   | <span data-ttu-id="0aa4f-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="0aa4f-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="0aa4f-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="0aa4f-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="0aa4f-545">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-545">String</span></span>      | <span data-ttu-id="0aa4f-546">Redigeeri</span><span class="sxs-lookup"><span data-stu-id="0aa4f-546">Edit</span></span>   | <span data-ttu-id="0aa4f-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="0aa4f-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="0aa4f-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="0aa4f-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="0aa4f-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span><span class="sxs-lookup"><span data-stu-id="0aa4f-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="0aa4f-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span><span class="sxs-lookup"><span data-stu-id="0aa4f-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="0aa4f-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="0aa4f-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="0aa4f-552">"")</span><span class="sxs-lookup"><span data-stu-id="0aa4f-552">"")</span></span> |
    | <span data-ttu-id="0aa4f-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="0aa4f-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="0aa4f-554">Salvestamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-554">Record</span></span>      |        | |
    | <span data-ttu-id="0aa4f-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="0aa4f-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="0aa4f-556">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-556">String</span></span>      | <span data-ttu-id="0aa4f-557">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-557">Bind</span></span>   | <span data-ttu-id="0aa4f-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="0aa4f-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="0aa4f-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="0aa4f-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="0aa4f-560">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-560">String</span></span>      | <span data-ttu-id="0aa4f-561">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-561">Bind</span></span>   | <span data-ttu-id="0aa4f-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="0aa4f-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="0aa4f-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="0aa4f-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="0aa4f-564">Tegelik</span><span class="sxs-lookup"><span data-stu-id="0aa4f-564">Real</span></span>        | <span data-ttu-id="0aa4f-565">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-565">Bind</span></span>   | <span data-ttu-id="0aa4f-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="0aa4f-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="0aa4f-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="0aa4f-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="0aa4f-568">Kirjete loend</span><span class="sxs-lookup"><span data-stu-id="0aa4f-568">Record list</span></span> | <span data-ttu-id="0aa4f-569">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-569">Bind</span></span>   | <span data-ttu-id="0aa4f-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="0aa4f-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="0aa4f-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="0aa4f-572">Täisarv</span><span class="sxs-lookup"><span data-stu-id="0aa4f-572">Integer</span></span>     | <span data-ttu-id="0aa4f-573">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-573">Bind</span></span>   | <span data-ttu-id="0aa4f-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="0aa4f-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="0aa4f-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="0aa4f-576">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-576">String</span></span>      | <span data-ttu-id="0aa4f-577">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-577">Bind</span></span>   | <span data-ttu-id="0aa4f-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="0aa4f-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="0aa4f-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="0aa4f-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="0aa4f-580">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-580">String</span></span>      | <span data-ttu-id="0aa4f-581">Redigeeri</span><span class="sxs-lookup"><span data-stu-id="0aa4f-581">Edit</span></span>   | <span data-ttu-id="0aa4f-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="0aa4f-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="0aa4f-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="0aa4f-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="0aa4f-584">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-584">String</span></span>      | <span data-ttu-id="0aa4f-585">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-585">Bind</span></span>   | <span data-ttu-id="0aa4f-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="0aa4f-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="0aa4f-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="0aa4f-588">Täisarv</span><span class="sxs-lookup"><span data-stu-id="0aa4f-588">Integer</span></span>     | <span data-ttu-id="0aa4f-589">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-589">Bind</span></span>   | <span data-ttu-id="0aa4f-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="0aa4f-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="0aa4f-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="0aa4f-592">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-592">String</span></span>      | <span data-ttu-id="0aa4f-593">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-593">Bind</span></span>   | <span data-ttu-id="0aa4f-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="0aa4f-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="0aa4f-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="0aa4f-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="0aa4f-596">Kirjete loend</span><span class="sxs-lookup"><span data-stu-id="0aa4f-596">Record list</span></span> | <span data-ttu-id="0aa4f-597">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-597">Bind</span></span>   | <span data-ttu-id="0aa4f-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="0aa4f-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="0aa4f-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="0aa4f-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="0aa4f-600">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-600">String</span></span>      | <span data-ttu-id="0aa4f-601">Redigeeri</span><span class="sxs-lookup"><span data-stu-id="0aa4f-601">Edit</span></span>   | <span data-ttu-id="0aa4f-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="0aa4f-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="0aa4f-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="0aa4f-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="0aa4f-604">Tegelik</span><span class="sxs-lookup"><span data-stu-id="0aa4f-604">Real</span></span>        | <span data-ttu-id="0aa4f-605">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-605">Bind</span></span>   | <span data-ttu-id="0aa4f-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="0aa4f-606">\@.point</span></span> |
    | <span data-ttu-id="0aa4f-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="0aa4f-608">Täisarv</span><span class="sxs-lookup"><span data-stu-id="0aa4f-608">Integer</span></span>     | <span data-ttu-id="0aa4f-609">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-609">Bind</span></span>   | <span data-ttu-id="0aa4f-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="0aa4f-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="0aa4f-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="0aa4f-612">String</span><span class="sxs-lookup"><span data-stu-id="0aa4f-612">String</span></span>      | <span data-ttu-id="0aa4f-613">Seo</span><span class="sxs-lookup"><span data-stu-id="0aa4f-613">Bind</span></span>   | <span data-ttu-id="0aa4f-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="0aa4f-614">\@.text</span></span> |

    <span data-ttu-id="0aa4f-615">Järgmisel illustratsioonil on kujutatud konfigureeritud mudelivastenduse lõplik olek lehel **Mudelivastenduse kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Täiesti konfigureeritud mudelivastendus ER-i mudelivastenduse kujundajas](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="0aa4f-617">Salvestage muudatused.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-617">Save your changes.</span></span>
8. <span data-ttu-id="0aa4f-618">Sulgege leht **Mudelivastenduse kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="0aa4f-619">Mudelivastenduse kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="0aa4f-620">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-621">Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="0aa4f-622">Valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="0aa4f-623">Valige **Muuda olekut** \> **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0aa4f-624">Selle konfiguratsiooni versiooni 1.1 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0aa4f-625">Versiooni 1.1 ei saa enam muuta.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="0aa4f-626">See versioon sisaldab konfigureeritud mudelivastendust ja seda saab kasutada teiste ER-i konfiguratsioonide alusena.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="0aa4f-627">Luuakse selle konfiguratsiooni versioon 1.2, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0aa4f-628">Saate seda versiooni redigeerida, et kohandada konfiguratsiooni **Küsimustiku vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Redigeeritava ER-i konfiguratsiooni versioonid lehel „Konfiguratsioonid”](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="0aa4f-630">Konfigureeritud mudelivastendus esindab äridomeeni **Küsimustik** esindava abstraktse andmemudeli rakenduse Finance põhist juurutamist.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="0aa4f-631">Kohandatud aruande malli kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-631">Design a template for a custom report</span></span>

<span data-ttu-id="0aa4f-632">ER-i raamistik kasutab eelmääratletud malle, et luua aruandeid Microsoft Office'i vormingutes (Exceli töövihikud või Wordi dokumendid).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="0aa4f-633">Vajaliku aruande loomisel täidetakse mall konfigureeritud andmevoo järgi vajalike andmetega.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="0aa4f-634">Seetõttu peate esmalt kujundama oma kohandatud aruande jaoks malli.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="0aa4f-635">See mall peab olema kujundatud Exceli töövihikuna, mille struktuur esindab kohandatud aruande paigutust.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="0aa4f-636">Peate panema nime kõikidele Exceli üksustele, mida kavatsete täita vajalike andmetega.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="0aa4f-637">Laadige alla fail [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) ja salvestage see oma kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-637">Download the [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="0aa4f-638">Avage fail Excelis ja vaadake üle töövihiku struktuur.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="0aa4f-639">Nagu järgmisel illustratsioonil näha, on allalaaditud mall loodud printima määratud küsimustikke, mis esitavad küsimustiku küsimused koos asjakohaste vastustega.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Exceli mall määratud küsimustike printimiseks](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="0aa4f-641">Küsimustiku üksikasjade täitmiseks on sellele mallile lisatud Exceli nimed.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="0aa4f-642">Exceli nimede ülevaatamiseks saate kasutada nimehaldurit.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-642">You can use Name Manager to review the Excel names.</span></span>

![Nimehalduri kasutamine Exceli nimede ülevaatamiseks esitatud Exceli mallis](./media/er-quick-start1-template-names.png)

<span data-ttu-id="0aa4f-644">Aruande sildid on lisatud inglise keeles fikseeritud tekstina.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="0aa4f-645">Saate asendada aruande sildid uute Exceli nimedega, mis täidavad keelest sõltuva tekstiga sildid, kasutades ER-i vormingu [silte](#AddMmLabels), nagu tegite konfigureeritud mudelivastenduse puhul keelest sõltuvate avaldiste korral.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="0aa4f-646">Sel juhul tuleb ER-i sildid lisada redigeeritavas ER-i vormingus.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="0aa4f-647">Nagu järgmisel illustratsioonil näha, on kohandatud aruande päist muudetud, et lisada leheküljenumbrid Excelis.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Kohandatud aruande päis esitatud Exceli mallis](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="0aa4f-649">Vormingu kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-649">Design a format</span></span>

<span data-ttu-id="0aa4f-650">Elektroonilise aruandluse funktsionaalse konsultandi rollis kasutajana peate looma uue ER-i konfiguratsiooni, mis sisaldab [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponenti.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="0aa4f-651">Peate konfigureerima vormingu komponendi, et määrata, kuidas sisestatakse vajalikud andmed käitusajal aruandemalli.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="0aa4f-652">Kui täidate jaotises [Kujundatud vormingu konfiguratsiooni importimine](#FormatImport) toodud juhised, saate vajaliku vormingu importida esitatud XML-failist.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="0aa4f-653">Teise võimalusena saate täita jaotise [Uue vormingu konfiguratsiooni loomine](#FormatCreate) juhised, et kujundada see vorming täiesti algusest.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="0aa4f-654">Kujundatud vormingu konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="0aa4f-655">Laadige alla fail [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) ja salvestage see oma kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-655">Download the [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="0aa4f-656">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0aa4f-657">Valige tööruumis **Elektrooniline aruandlus** suvand **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="0aa4f-658">Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="0aa4f-659">Valige **Sirvi** ning seejärel otsige üles ja valige fail **Questionnaires format.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="0aa4f-660">Konfiguratsiooni importimiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="0aa4f-661">Jätkamiseks jätke järgmine protseduur [Uue vormingu konfiguratsiooni loomine](#FormatCreate) vahele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="0aa4f-662">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="0aa4f-663">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-664">Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku mudel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="0aa4f-665">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="0aa4f-666">Dialoogiakna ripploendis järgige allolevaid etappe.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-667">Valige väljal **Uus** suvand **Küsimustike andmemudelil põhinev vorming**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="0aa4f-668">Sisestage väljale **Nimi** tekst **Küsimustiku aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="0aa4f-669">Valige väljal **Andmemudeli versioon** väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="0aa4f-670">Kui valite kindla põhiandmemudeli versiooni, ühtib andmemudeli asjakohase versiooni struktuur loodavas vormingus andmeallika **Mudel** struktuuriga.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="0aa4f-671">Võite selle välja tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-671">You can leave this field blank.</span></span> <span data-ttu-id="0aa4f-672">Sellisel juhul ühtib andmemudeli versiooni **Mustand** struktuur loodavas vormingus andmeallika **Mudel** struktuuriga.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="0aa4f-673">Seejärel saate kohandada oma mudelit ja näha neid korrigeerimisi oma vormingus.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="0aa4f-674">See meetod võib parandada ER-i lahenduse kujunduse tõhusust, kui konfigureerite oma andmemudeli, mudelivastenduse ja vormingu samal ajal.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="0aa4f-675">Kui valite põhiandmemudeli kindla versiooni, saate hiljem vormingut redigeerides aktiveerida versiooni **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="0aa4f-676">Valige väljal **Andmemudeli definitsioon** definitsioon **Juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="0aa4f-677">Konfiguratsiooni loomiseks valige **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="0aa4f-678">Aruandemalli importimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-678">Import a report template</span></span>

1. <span data-ttu-id="0aa4f-679">Valige lehel **Konfiguratsioonid** konfiguratsioonipuul **Küsimustiku aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="0aa4f-680">Valige **Kujundaja**, et alustada kohandatud vormingu konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="0aa4f-681">Valige lehe **Vormingu kujundaja** toimingupaanil suvand **Impordi** \> **Impordi Excelist**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="0aa4f-682">Järgige dialoogiboksis järgmiseid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-683">Valige **Lisa mall**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="0aa4f-684">Otsige üles ja valige kohalikult salvestatud fail **Questionnaires report template.xslx** ning seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="0aa4f-685">Malli importimiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-685">Select **OK** to import the template.</span></span>

    ![Aruandemalli importimine](./media/er-quick-start1-template-import.png)

<span data-ttu-id="0aa4f-687">Vorminguelement **Excel\\File** lisatakse automaatselt juurelemendina redigeeritavasse vormingusse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="0aa4f-688">Lisaks lisatakse automaatselt kõikide imporditud mallis tuvastatud Exceli nimede jaoks kas vorminguelement **Excel\\Range** või **Excel\\Cell**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="0aa4f-689">Vorming **Excel\\Header**, millel on pesastatud element **String**, lisatakse automaatselt, et kajastada imporditud malli päisesätteid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Automaatselt lisatud elemente sisaldava vormingu struktuur ER-i toimingute kujundajas](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="0aa4f-691">Vormingu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-691">Configure a format</span></span>

1. <span data-ttu-id="0aa4f-692">Valige lehel **Vormingu kujundaja** vormingupuus juurelement **Excel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="0aa4f-693">Sisestage lehe paremal pool vahekaardi **Vorming** väljale **Nimi** väärtus <a name="AddFormatRootElement"></a>**Report**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="0aa4f-694">Valige väljal **Keele-eelistus** suvand **Kasutaja eelistus**, et käitada aruanne kasutaja eelistatud keeles.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="0aa4f-695">Valige väljal **Kultuurieelistus** suvand **Kasutaja eelistus**, et käitada aruanne kasutaja eelistatud kultuuris.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="0aa4f-696">Lisateavet ER-i protsessi jaoks keele- ja kultuurikontekstide määramise kohta leiate teemast [Mitmekeelsete aruannete kujundamine](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Kujundatud aruande jaoks keele- ja kultuurisätete konfigureerimine ER-i toimingute kujundajas](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="0aa4f-698">Laiendage vormingupuul juursõlm ja valige **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="0aa4f-699">Valige vahekaardil **Vorming** väljal **Edastamise suund** suvand **Edastust pole**, kuna te ei eelda, et ühe küsimustiku jaoks on mitu tulemusegruppi.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Edastamise suuna määramine vahemiku vorminguelementide jaoks ER-i toimingute kujundajas](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="0aa4f-701">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="0aa4f-702">Andmesidumise määratlemine aruande pealkirja jaoks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-702">Define the data binding for a report title</span></span>

<span data-ttu-id="0aa4f-703">Peate määrama vorminguelemendi jaoks andmesidumise, mida kasutatakse loodud aruande pealkirja täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="0aa4f-704">Valige lehel **Vormingu kujundaja** parempoolsel vahekaardil **Vastendus** element **Report\\ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="0aa4f-705">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="0aa4f-706">Valige valemiredaktoris **Tõlgi**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="0aa4f-707">Järgige dialoogiboksis **Teksti tõlkimine** allolevaid etappe.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0aa4f-708">Sisestage väljale **Sildi ID** väärtus **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="0aa4f-709">Sisestage väljale **Tekst vaikekeeles** väärtus **Küsimustike aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="0aa4f-710">Valige **Tõlgi** ja seejärel suvand **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="0aa4f-711">Valige **Tõlgi**, et sulgeda dialoogiboks **Teksti tõlkimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="0aa4f-712">Sulgege valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-712">Close the formula editor.</span></span>

    ![Seose konfigureerimine loodud aruande pealkirja täitmiseks](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="0aa4f-714">Saate kasutada seda meetodit, et muuta kõik muud praeguse malli sildid keelest sõltuvaks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="0aa4f-715">Lisateavet selle kohta, kuidas ühe ER-i konfiguratsiooni lisatud silte saab tõlkida kõikidesse toetatud keeltesse, leiate teemast [Mitmekeelsete aruannete kujundamine](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="0aa4f-716">Mudeli andmeallika ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-716">Review model data source</span></span>

1. <span data-ttu-id="0aa4f-717">Valige lehel **Vormingu kujundaja** vahekaardil **Vastendus** andmeallikas <a name="ModelDSName"></a>**mudel**, mis esindab selle ER-i vormingu põhiandmemudelit.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="0aa4f-718">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-718">Select **Edit**.</span></span>
3. <span data-ttu-id="0aa4f-719">Vaadake üle dialoogiboksis **Andmeallika atribuudid** olev teave.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="0aa4f-720">See andmeallikas tähistab andmeallika komponendi **Küsimustikud** versiooni 1, mis asub ER-i konfiguratsioonis **Küsimustike mudel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Mudeli andmeallika atribuudid ER-i toimingute kujundajas](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="0aa4f-722">Vorminguelementide sidumine andmeallika väljadega</span><span class="sxs-lookup"><span data-stu-id="0aa4f-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="0aa4f-723">Et määrata, kuidas mall käitusajal täidetakse, peate siduma iga vorminguelemendi, mis on seotud asjakohase Exceli nimega, selle vormingu andmeallika ühe väljaga.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="0aa4f-724">Valige lehel **Vormingu kujundaja** vormingupuus vorminguelement **Report\\CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="0aa4f-725">Valige vahekaardil **Vastendus** andmeallika väli **model.CompanyName**, mille tüüp on **String**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="0aa4f-726">Valige **Seo**, et sisestada malli ettevõtte nimi.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="0aa4f-727">Valige vormingupuus element **Report\\Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="0aa4f-728">Valige vahekaardil **Vastendus** andmeallika väli **model.Questionnaire**, mille tüüp on **Kirjete loend**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="0aa4f-729">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-729">Select **Bind**.</span></span>
7. <span data-ttu-id="0aa4f-730">Valige **Kuva üksikasjad**, et näha vorminguelementide üksikasju.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="0aa4f-731">Vahemiku vorminguelement **Küsimustik** konfigureeritakse vertikaalselt edastavana.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="0aa4f-732">Kui see seotakse andmeallikaga, mille tüüp on **Kirjete loend**, korratakse Exceli malli asjakohast vahemikku **Küsimustik** seotud andmeallika iga kirje puhul.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Vahemiku vorminguelemendi „Küsimustik” sidumine asjakohaste kirjete loendi tüüpi andmeallikatega ER-i toimingute kujundajas](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="0aa4f-734">Kuna Exceli malli vahemik **Küsimustik** on määratletud ridades 5 kuni 14, korratakse neid ridu iga esitatud küsimustiku puhul.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Exceli malli read, mida korratakse loodud aruandes kirjete loendi tüüpi andmeallikate kõikide kirjete puhul](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="0aa4f-736">Konfigureerige samasugused seosed ülejäänud vorminguelementide jaoks, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0aa4f-737">Selles tabelis eeldatakse veerus „Andmeallika tee” oleva teabe puhul, et ER-i funktsioon [suhteline tee](relative-path-data-bindings-er-models-format.md) on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="0aa4f-738">Vorminguelemendi tee</span><span class="sxs-lookup"><span data-stu-id="0aa4f-738">Format element path</span></span>                                      | <span data-ttu-id="0aa4f-739">Andmeallika tee</span><span class="sxs-lookup"><span data-stu-id="0aa4f-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="0aa4f-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="0aa4f-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="0aa4f-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="0aa4f-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="0aa4f-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="0aa4f-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="0aa4f-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="0aa4f-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="0aa4f-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="0aa4f-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="0aa4f-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="0aa4f-747">**\@.Active**, kus **\@** on **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="0aa4f-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="0aa4f-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="0aa4f-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-749">**\@.Code**</span></span> |
    | <span data-ttu-id="0aa4f-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="0aa4f-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="0aa4f-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-751">**\@.Description**</span></span> |
    | <span data-ttu-id="0aa4f-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="0aa4f-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="0aa4f-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="0aa4f-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="0aa4f-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="0aa4f-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="0aa4f-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="0aa4f-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="0aa4f-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="0aa4f-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="0aa4f-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="0aa4f-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="0aa4f-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="0aa4f-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="0aa4f-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="0aa4f-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="0aa4f-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="0aa4f-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-763">**\@.Question**</span></span> |
    | <span data-ttu-id="0aa4f-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="0aa4f-765">**\@.CollectionSequenceNumber**, kus **\@** on **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="0aa4f-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="0aa4f-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="0aa4f-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-767">**\@.Id**</span></span> |
    | <span data-ttu-id="0aa4f-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="0aa4f-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="0aa4f-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="0aa4f-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="0aa4f-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="0aa4f-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="0aa4f-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="0aa4f-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="0aa4f-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="0aa4f-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="0aa4f-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="0aa4f-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-775">**\@.Text**</span></span> |
    | <span data-ttu-id="0aa4f-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="0aa4f-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="0aa4f-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="0aa4f-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="0aa4f-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="0aa4f-779">**\@.CorrectAnswer**, kus **\@** on **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="0aa4f-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="0aa4f-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="0aa4f-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-781">**\@.Points**</span></span> |
    | <span data-ttu-id="0aa4f-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="0aa4f-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="0aa4f-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-783">**\@.Text**</span></span> |

9. <span data-ttu-id="0aa4f-784">Kui olete lõpetanud, valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="0aa4f-785">Järgmisel illustratsioonil on kujutatud konfigureeritud andmesidumiste lõplik olek lehel **Vormingu kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Konfigureeritud andmesidumised ER-i toimingute kujundajas](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="0aa4f-787">Terve määratud andmeallikate ja sidumiste kogum tähistab konfigureeritud vormingu vorminguvastenduse komponenti.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="0aa4f-788">Seda vorminguvastendust kutsutakse, kui käivitate aruande loomiseks konfigureeritud vormingu.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="0aa4f-789">Kujundatud vormingu käivitamine ER-is</span><span class="sxs-lookup"><span data-stu-id="0aa4f-789">Run a designed format from ER</span></span>

<span data-ttu-id="0aa4f-790">Saate nüüd kujundatud vormingu lehel **Konfiguratsioonid** testimiseks käivitada.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="0aa4f-791">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-792">Laiendage lehel **Konfiguratsioon** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="0aa4f-793">Valige **Kujundaja** vormingu versiooni jaoks, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="0aa4f-794">Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="0aa4f-795">Konfigureerige dialoogiboksis **ER-i parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="0aa4f-796">Valige filtreerimissuvandi kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="0aa4f-797">Aruande käivitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="0aa4f-798">Vaadake loodud aruanne üle.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-798">Review the generated report.</span></span>

<span data-ttu-id="0aa4f-799">[Vaikimisi](electronic-reporting-destinations.md#default-behavior) on loodud aruanne Exceli failis, mille saate alla laadida.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="0aa4f-800">Järgmistel illustratsioonidel on kujutatud Exceli vormingus loodud aruande kaks lehekülge.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Exceli vormingus loodud aruande näide, lehekülg 1](./media/er-quick-start1-report1a.png)

![Exceli vormingus loodud aruande näide, lehekülg 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="0aa4f-803">Kujundatud vormingu häälestamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="0aa4f-804">Vormingu muutmine loodud dokumendi nime muutmiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="0aa4f-805">Loodud dokumendile pannakse vaikimisi nimi praeguse kasutaja pseudonüümi põhjal.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="0aa4f-806">Vormingut muutes saate seda funktsiooni muuta nii, et loodud dokumendile pannakse nimi teie kohandatud loogika põhjal.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="0aa4f-807">Näiteks võib loodud dokumendi nimi põhineda praeguse seansi kuupäeval ja kellaajal ning aruande pealkirjal.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="0aa4f-808">Valige lehel **Vormingu kujundaja** juurüksus **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="0aa4f-809">Valige vahekaardil **Vastendus** suvand **Redigeeri faili nime**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="0aa4f-810">Sisestage väljale **Valem** väärtus **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="0aa4f-811">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="0aa4f-812">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="0aa4f-813">Vormingu muutmine küsimuste järjekorra muutmiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="0aa4f-814">Küsimused ei ole loodud aruandes õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="0aa4f-815">Järjekorra muutmiseks saate muuta vormingut.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="0aa4f-816">Valige lehel **Vormingu kujundaja** juurüksus **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="0aa4f-817">Laiendage vahekaardil **Vastendus** vormingupuus suvand **Report\\Questionnaire\\Question**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Vahemiku tüüpi küsimuse vorminguelement ER-i toimingute kujundajas](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="0aa4f-819">Valige vahekaardil **Vastendus** suvand **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="0aa4f-820">Valige **Lisa** \> **Funktsioonid\\Arvutatud väli** ja seejärel sisestage väljale **Nimi** väärtus **OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="0aa4f-821">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="0aa4f-822">Sisestage valemiredaktoris väljale **Valem** väärtus **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)**, et järjestada praeguse küsimustiku küsimuste loend järjekorranumbri alusel.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="0aa4f-823">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="0aa4f-824">Valige **OK**, et lõpetada uue arvutatud välja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="0aa4f-825">Valige vahekaardil **Vastendus** suvand **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="0aa4f-826">Valige vormingupuul **Excel\\Questionnaire\\Question**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="0aa4f-827">Valige **Seo** ja seejärel kinnitage, et praegune tee **model.Questionnaire.Questions** vahetatakse pesastatud elementide kõikides seostes uue tee **model.Questionnaire.OrderedQuestions** vastu.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="0aa4f-828">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-828">Select **Save**.</span></span>

![Küsimuse vorminguelemendi sidumine konfigureeritud andmeallikaga OrderedQuestions ER-i toimingute kujundajas](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="0aa4f-830">Muudetud vormingu käivitamine ER-is</span><span class="sxs-lookup"><span data-stu-id="0aa4f-830">Run a modified format from ER</span></span>

<span data-ttu-id="0aa4f-831">Nüüd saate muudetud vormingu testimiseks ER-i raamistikus käivitada.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="0aa4f-832">Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="0aa4f-833">Konfigureerige dialoogiboksis **ER-i parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="0aa4f-834">Valige filtreerimissuvandi kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="0aa4f-835">Aruande käivitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="0aa4f-836">Vaadake loodud aruanne üle.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-836">Review the generated report.</span></span>

<span data-ttu-id="0aa4f-837">Järgmisel illustratsioonil on näha Exceli vormingus loodud aruanne, kus küsimused on õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Exceli vormingus loodud aruanne, mille küsimused on õiges järjekorras](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="0aa4f-839">Vormingu kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-839">Complete the format design</span></span>

1. <span data-ttu-id="0aa4f-840">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-841">Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="0aa4f-842">Valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="0aa4f-843">Valige **Muuda olekut** \> **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0aa4f-844">Selle konfiguratsiooni versiooni 1.1 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0aa4f-845">Versiooni 1.1 ei saa enam muuta.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="0aa4f-846">See versioon sisaldab konfigureeritud vormingut ja seda saab kasutada kohandatud aruande printimiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="0aa4f-847">Luuakse selle konfiguratsiooni versioon 1.2, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0aa4f-848">Saate seda versiooni redigeerida, et kohandada aruande **Küsimustik** vormingut.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Redigeeritava ER-i konfiguratsiooni versioonid lehel „Konfiguratsioonid”](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="0aa4f-850">Konfigureeritud vorming moodustab aruande **Küsimustik** kujunduse ja see pole seotud Finance'i-põhiste artefaktidega.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="0aa4f-851">Rakenduse artefaktide arendamine kujundatud aruande kutsumiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="0aa4f-852">Süsteemiadministraatori rollis kasutajana peate arendama välja uue loogika, et konfigureeritud ER-i vormingut saaks kutsuda rakenduse kasutajaliidesest (UI) kohandatud aruande loomiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="0aa4f-853">Praegu ei paku ER seda tüüpi loogika konfigureerimiseks ühtegi võimalust.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="0aa4f-854">Seetõttu on vaja teha natuke tehnilist tööd.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="0aa4f-855">Uue loogika arendamiseks peate juurutama topoloogia, mis toetab pidevat järku.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="0aa4f-856">Lisainfo saamiseks vt [Pideva järgu ja testimise automaatikat toetavate topoloogiate juurutamine](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="0aa4f-857">Samuti peab teil selle topoloogia puhul olema juurdepääs arenduskeskkonnale.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="0aa4f-858">Lisateavet saadaval ER-i API kohta leiate teemast [ER-i raamistiku API](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="0aa4f-859">Lähtekoodi muutmine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="0aa4f-860">Andmelepingu klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-860">Add a data contract class</span></span>

<span data-ttu-id="0aa4f-861">Lisage oma Microsoft Visual Studio projekti uus klass **QuestionnairesErReportContract** ja kirjutage kood, mis määrab, millist andmelepingut tuleks konfigureeritud ER-i vormingu käivitamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="0aa4f-862">UI-koostaja klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-862">Add a UI builder class</span></span>

<span data-ttu-id="0aa4f-863">Lisage uus klass **QuestionnairesErReportUIBuilder** oma Visual Studio projekti ja kirjutage kood, et luua käitusaja dialoogiboks, mida kasutatakse käivitatava ER-i vormingu vorminguvastenduse ID ülesleidmiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="0aa4f-864">Esitatud kood otsib ainult ER-i vorminguid, mis sisaldavad andmeallikat, mille tüüp on **Andmemudel**, ning mis viitab andmemudelile **[Küsimustikud](#DataModeName)**, kasutades definitsiooni **[Juur](#RootDefinitionName)**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="0aa4f-865">Teise võimalusena saate ER-i vormingute filtreerimiseks kasutada ER-i integratsioonipunkte.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="0aa4f-866">Lisateavet leiate teemast [API vorminguvastenduse otsingu kuvamiseks](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="0aa4f-867">Andmepakkuja klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-867">Add a data provider class</span></span>

<span data-ttu-id="0aa4f-868">Lisage oma Microsoft Visual Studio projekti uus klass **QuestionnairesErReportDP** ja kirjutage kood, mis määrab andmepakkuja, keda tuleks konfigureeritud ER-i vormingu käivitamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="0aa4f-869">Esitatud kood hõlmab selle andmepakkuja puhul ainult andmelepingut.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="0aa4f-870">Siltide faili lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-870">Add a labels file</span></span>

<span data-ttu-id="0aa4f-871">Lisage uus siltide fail **QuestionnairesErReportLabels\_en-US** oma Visual Studio projekti ja määrake uute kasutajaliidese ressursside jaoks järgmised sildid.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="0aa4f-872">Silt **\@QuestionnairesReport** uue menüüelemendi jaoks, mis sisaldab USA inglise keeles (en-US) järgmist teksti: **Küsimustike aruanne (ER-i põhine)**</span><span class="sxs-lookup"><span data-stu-id="0aa4f-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="0aa4f-873">Silt **\@QuestionnairesReportBatchJobDescription** pakett-töö pealkirja jaoks, kui valitud ER-i vorming on pakett-tööna käivitamiseks ajastatud</span><span class="sxs-lookup"><span data-stu-id="0aa4f-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="0aa4f-874">Aruandeteenuse klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-874">Add a report service class</span></span>

<span data-ttu-id="0aa4f-875">Lisage uus klass **QuestionnairesErReportService** oma Visual Studio projekti ja kirjutage kood, mis kutsub ER-i vormingut, tuvastab selle vorminguvastenduse ID abil ja esitab parameetrina andmelepingu.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="0aa4f-876">Kui peate kasutama ER-i vormingut, mis käitab rakenduse andmeid, peate vorminguvastenduses konfigureerima andmeallika, mille tüüp on **Andmemudel**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="0aa4f-877">See andmeallikas viitab määratud andmemudeli kindlale osale, kasutades ühte juurdefinitsiooni.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="0aa4f-878">ER-i vormingu käivitamisel kutsub see andmeallikat, et saada juurdepääs asjakohasele ER-i mudelivastendusele, mis on konfigureeritud asjaomase mudeli ja juurdefinitsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="0aa4f-879">Kogu teavet, mida te lähtekoodis ette valmistate ja andmelepingu osana talletate, saab edastada töötavale ER-i vormingule, kasutades seda tüüpi ER-i mudelivastendust.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="0aa4f-880">ER-i mudelivastenduses peate konfigureerima andmeallika, mille tüüp on **Objekt** ja mis viitab klassile **[QuestionnairesErReportContract](#DataContractClass)**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="0aa4f-881">Mudelivastenduse tuvastamiseks peate määrama andmeallika, mis kutsub seda mudelivastendust.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="0aa4f-882">Esitatud koodis on see andmeallikas täpsustatud konstanti **ERModelDataSourceName** abil, mille väärtus on **[mudel](#ModelDSName)**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="0aa4f-883">Et tuvastada, millist andmeallikat kasutatakse mudelivastenduses andmelepingu paljastamiseks, peate määrama andmeallika nime.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="0aa4f-884">Esitatud koodis on see nimi täpsustatud konstanti **ParametersDataSourceName** abil, mille väärtus on <a name="DataContractDSName"></a>**RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="0aa4f-885">Uues keskkonnas peate võib-olla värskendama ER-i metaandmeid, et seda tüüpi klass oleks ER-i mudelivastenduse kujundajas saadaval.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="0aa4f-886">Lisateavet leiate teemast [ER-i raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="0aa4f-887">Aruandekontrolleri klassi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-887">Add a report controller class</span></span>

<span data-ttu-id="0aa4f-888">Lisage uus klass **QuestionnairesErReportController** oma Visual Studio projekti ja kirjutage kood, mis käitab ER-i vormingu teie eelistuste põhjal kas sünkroonses või pakktöötlusrežiimis dialoogiboksis, mis on kujundatud klassis **QuestionnairesErReportUIBuilder** leiduva loogika põhjal.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="0aa4f-889">Menüüelemendi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-889">Add a menu item</span></span>

<span data-ttu-id="0aa4f-890">Lisage uus menüüelement **QuestionnairesErReport** oma Visual Studio projekti.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="0aa4f-891">Atribuudis **Objekt** viitab see menüüelement klassile **QuestionnairesErReportController** ning seda kasutatakse kasutajaõiguse määramiseks ER-i vormingu valimiseks ja käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="0aa4f-892">Atribuudis **Silt** viitab see menüüelement varem loodud sildile **\@QuestionnairesReport**, nii et rakenduse kasutajaliideses kuvatakse õige tekst.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="0aa4f-893">Menüüelemendi lisamine menüüle</span><span class="sxs-lookup"><span data-stu-id="0aa4f-893">Add a menu item to a menu</span></span>

<span data-ttu-id="0aa4f-894">Lisage olemasolev menüü **KM** oma Visual Studio projekti.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="0aa4f-895">Peate sellesse menüüsse lisama uue üksuse **QuestionnairesErReport**, mille tüüp on **Väljund**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="0aa4f-896">See üksus peab viitama menüüelemendile **QuestionnairesErReport**, mida kirjeldatakse eelmises jaotises.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="0aa4f-897">Visual Studio projekti koostamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-897">Build a Visual Studio project</span></span>

<span data-ttu-id="0aa4f-898">Koostage oma projekt, et muuta uus menüüelement kasutajatele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="0aa4f-899">Vormingu käivitamine rakenduses</span><span class="sxs-lookup"><span data-stu-id="0aa4f-899">Run a format from the application</span></span>

1. <span data-ttu-id="0aa4f-900">Avage **Küsimustik** \> **Kujundus** \> **Küsimustike aruanne (ER-i põhine)**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Menüüelemendi „Küsimustike aruanne (ER-i põhine)” valimine küsimustiku moodulis, et käivitada konfigureeritud ER-i vorming](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="0aa4f-902">Valige dialoogiboksis **Vorminguvastendus** suvand **Küsimustike aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="0aa4f-903">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-903">Select **OK**.</span></span>
4. <span data-ttu-id="0aa4f-904">Konfigureerige dialoogiboksis **Elektroonilise aruande parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="0aa4f-905">Valige filtreerimissuvandi kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="0aa4f-906">Aruande käivitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-906">Select **OK** to run the report.</span></span>

    ![Valikukriteeriumide täpsustamine elektroonilise aruande dialoogiboksis](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="0aa4f-908">Vaadake loodud aruanne üle.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="0aa4f-909">Kujundatud ER-i lahenduse häälestamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-909">Tune a designed ER solution</span></span>

<span data-ttu-id="0aa4f-910">Saate muuta konfigureeritud ER-i lahendust nii, et see kasutaks andmepakkuja klassi, mille arendasite töötava ER-i vormingu üksikasjadele juurdepääsemiseks, ja nii, et see sisestaks selle ER-i vormingu nime loodud aruandesse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="0aa4f-911">Mudelivastenduse muutmine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="0aa4f-912">Andmeallikate lisamine andmelepingu objektile juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="0aa4f-913">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-914">Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="0aa4f-915">Valige **Kujundaja**, et avada leht **Mudelist andmeallikasse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="0aa4f-916">Valige **Kujundaja**, et avada valitud vastendus mudelivastenduse kujundajas.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="0aa4f-917">Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Objekt**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="0aa4f-918">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="0aa4f-919">Sisestage dialoogiboksis väljale **Nimi** väärtus **[RunTimeParameters](#DataContractDSName)**, nagu on määratletud klassi **QuestionnairesErReportService** lähtekoodis.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="0aa4f-920">Sisestage väljale **Klass** väärtus **[QuestionnairesErReportContract](#DataContractClass)**, mille kood kirjutati varem.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="0aa4f-921">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-921">Select **OK**.</span></span>
10. <span data-ttu-id="0aa4f-922">Laiendage suvand **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="0aa4f-923">Lisatud andmeallikas annab teavet töötava ER-i vorminguvastenduse kirje ID kohta.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Lisatud andmeallikas ER-i mudelivastenduse kujundajas](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="0aa4f-925">Andmeallika lisamine ER-i vorminguvastenduse kirjetele juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="0aa4f-926">Jätkake valitud mudelivastenduse redigeerimist andmeallika lisamise kaudu, et pääseda juurde ER-i vorminguvastenduse kirjetele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="0aa4f-927">Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="0aa4f-928">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="0aa4f-929">Sisestage dialoogiboksis väljale **Nimi** väärtus **ER1**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="0aa4f-930">Sisestage väljale **Tabel** väärtus **ERFormatMappingTable**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="0aa4f-931">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="0aa4f-932">Andmeallika lisamine töötava ER-i vorminguvastenduse kirjele juurdepääsemiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="0aa4f-933">Jätkake valitud mudelivastenduse redigeerimist andmeallika lisamise kaudu, et pääseda juurde töötava ER-i vormingu vorminguvastenduse kirjele.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="0aa4f-934">Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="0aa4f-935">Valige paanil **Andmeallikad** suvand **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="0aa4f-936">Sisestage dialoogiboksis väljale **Nimi** väärtus **ER2**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="0aa4f-937">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="0aa4f-938">Sisestage valemiredaktoris väljale **Valem** väärtus **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="0aa4f-939">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="0aa4f-940">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="0aa4f-941">Töötava ER-i vormingu nime sisestamine andmemudelisse</span><span class="sxs-lookup"><span data-stu-id="0aa4f-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="0aa4f-942">Jätkake valitud mudelivastenduse redigeerimist, et töötava ER-i vormingu nimi sisestataks andmemudelisse.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="0aa4f-943">Laiendage lehel **Mudelivastenduse kujundaja** paanil **Andmemudel** suvand **ExecutionContext** ja seejärel valige **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="0aa4f-944">Valige paanil **Andmemudel** suvand **Redigeeri**, et konfigureerida valitud andmemudeli välja jaoks andmesidumine.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="0aa4f-945">Sisestage valemiredaktoris väljale **Valem** väärtus **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="0aa4f-946">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="0aa4f-947">Kuna kasutasite välja **FormatName**, siis paljastab konfigureeritud mudelivastendus nüüd ER-i vormingu nime, mis kutsub käivitamise ajal seda mudelivastendust.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Andmemudeli välja sidumine lisatud andmeallika meetodiga ER-i mudelivastenduse kujundajas](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="0aa4f-949">Mudelivastenduse kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="0aa4f-950">Valige lehel **Mudelivastenduse kujundaja** suvand **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="0aa4f-951">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-951">Close the page.</span></span>
3. <span data-ttu-id="0aa4f-952">Sulgege mudelivastenduste leht.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="0aa4f-953">Veenduge lehe **Konfiguratsioonid** konfiguratsioonipuus, et konfiguratsioon **Küsimustiku vastendamine** oleks endiselt valitud.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="0aa4f-954">Siis valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="0aa4f-955">Valige **Muuda olekut** \> **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0aa4f-956">Selle konfiguratsiooni versiooni 1.2 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0aa4f-957">Versiooni 1.2 ei saa enam muuta.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="0aa4f-958">See versioon sisaldab konfigureeritud mudelivastendust ja seda saab kasutada teiste ER-i konfiguratsioonide alusena.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="0aa4f-959">Luuakse selle konfiguratsiooni versioon 1.3, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0aa4f-960">Saate seda versiooni redigeerida, et kohandada mudelivastendust **Küsimustik**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="0aa4f-961">Vormingu muutmine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-961">Modify a format</span></span>

<span data-ttu-id="0aa4f-962">Saate muuta konfigureeritud ER-i vormingut nii, et selle nimi kuvataks ER-i vormingu käivitamisel loodava aruande jaluses.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="0aa4f-963">Uue vorminguelemendi lisamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-963">Add a new format element</span></span>

1. <span data-ttu-id="0aa4f-964">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-965">Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="0aa4f-966">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-966">Select **Designer**.</span></span>
4. <span data-ttu-id="0aa4f-967">Valige lehel **Vormingu kujundaja** juurüksus **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="0aa4f-968">Valige **Lisa**, et lisada uus pesastatud vorminguelement valitud juurüksusele **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="0aa4f-969">Valige **Excel\\Footer**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="0aa4f-970">Sisestage väljale **Nimi** väärtus **Footer**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="0aa4f-971">Valige **Report\Footer** ja seejärel **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="0aa4f-972">Valige **Text\\String**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="0aa4f-973">Lisatud vorminguelemendi sidumine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-973">Bind the added format element</span></span>

1. <span data-ttu-id="0aa4f-974">Valige lehel **Vormingu kujundaja** vahekaardil **Vastendus** vormingupuus aktiivse elemendi **Jalus\\String** puhul suvand **Redigeeri valemit**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="0aa4f-975">Sisestage valemiredaktoris väljale **Valem** väärtus **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="0aa4f-976">Valige **Salvesta** ja sulgege seejärel valemiredaktor.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="0aa4f-977">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-977">Select **Save**.</span></span>

<span data-ttu-id="0aa4f-978">Konfigureeritud vormingut on nüüd muudetud nii, et selle nimi sisestatakse loodud aruande jalusesse, kasutades elementi **Footer\\String**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Jaluse vorminguelemendi lisamine konfigureeritud vormingusse ER-i toimingute kujundajas](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="0aa4f-980">Vormingu kujunduse lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-980">Complete the format design</span></span>

1. <span data-ttu-id="0aa4f-981">Sulgege **Vormingu kujundaja** leht.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="0aa4f-982">Veenduge lehe **Konfiguratsioonid** konfiguratsioonipuus, et konfiguratsioon **Küsimustiku aruanne** oleks endiselt valitud.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="0aa4f-983">Siis valige kiirkaardil **Versioonid** konfiguratsiooni versioon, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="0aa4f-984">Valige **Muuda olekut** \> **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="0aa4f-985">Selle konfiguratsiooni versiooni 1.2 olek muudetakse olekust **Mustand** olekusse **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="0aa4f-986">Versiooni 1.2 ei saa enam muuta.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="0aa4f-987">See versioon sisaldab konfigureeritud vormingut ja seda saab kasutada teiste ER-i konfiguratsioonide alusena.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="0aa4f-988">Luuakse selle konfiguratsiooni versioon 1.3, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="0aa4f-989">Saate seda versiooni redigeerida, et kohandada aruannet **Küsimustik**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="0aa4f-990">Vormingu käivitamine rakenduses</span><span class="sxs-lookup"><span data-stu-id="0aa4f-990">Run a format from the application</span></span>

1. <span data-ttu-id="0aa4f-991">Avage **Küsimustik** \> **Kujundus** \> **Küsimustike aruanne (ER-i põhine)**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="0aa4f-992">Valige dialoogiboksis **Vorminguvastendus** suvand **Küsimustike aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="0aa4f-993">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-993">Select **OK**.</span></span>
4. <span data-ttu-id="0aa4f-994">Konfigureerige dialoogiboksis **ER-i parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="0aa4f-995">Valige filtreerimissuvandi kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="0aa4f-996">Aruande käivitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="0aa4f-997">Vaadake loodud fail Exceli vormingus üle.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="0aa4f-998">Pange tähele, et loodud aruande jalus sisaldab aruande loomiseks kasutatud ER-i vormingu nime.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Loodud aruanne Exceli vormingus](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="0aa4f-1000">Vormingu käivitamine ER-is</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1000">Run a format from ER</span></span>

1. <span data-ttu-id="0aa4f-1001">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0aa4f-1002">Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Küsimustiku mudel** ja seejärel valige **Küsimustiku aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="0aa4f-1003">Valige toimingupaanil käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="0aa4f-1004">Konfigureerige dialoogiboksis **Elektroonilise aruande parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="0aa4f-1005">Valige filtreerimissuvandi kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="0aa4f-1006">Aruande käivitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="0aa4f-1007">Vaadake loodud fail Exceli vormingus üle.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="0aa4f-1008">Pange tähele, et loodud aruande jalus ei sisalda aruande loomiseks kasutatud ER-i vormingu nime, kuna andmelepingu objekti ei edastatud töötavasse mudelivastendusse, kui seda kutsus ER-is käivitatud ER-i vorming.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="0aa4f-1009">Vormingu sihtkoha konfigureerimine ekraanil eelvaatamiseks</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="0aa4f-1010">Avage **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse sihtkoht**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="0aa4f-1011">Lisage lehel **Elektroonilise aruandluse sihtkoht** konfigureeritud ER-i vormingu **Küsimustiku aruanne** jaoks sihtkoha kirje.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="0aa4f-1012">Seadistage kiirkaardil **Faili sihtkoht** [sihtkoht](er-destination-type-screen.md) **Ekraan** vormingu komponendi **Aruanne** jaoks, mis on [lisatud](#AddFormatRootElement) konfigureeritud ER-i vormingu **Küsimustiku aruanne** juurelemendina.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="0aa4f-1013">Konfigureerige kiirkaardil **PDF-i teisenduse sätted** sihtkoht, et teisendada aruanne [PDF-vormingusse](electronic-reporting-destinations.md#OutputConversionToPDF), mis kasutab lehe paigutust **Horisontaalne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Elektroonilise aruandluse sihtkoha lehel ER-i vormingu jaoks kohandatud sihtkoha „Ekraan” konfigureerimine](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="0aa4f-1015">Vormingu käivitamine rakenduses selle eelvaatamiseks PDF-dokumendina</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="0aa4f-1016">Avage **Küsimustik** \> **Kujundus** \> **Küsimustike aruanne (ER-i põhine)**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="0aa4f-1017">Valige dialoogiboksis **Vorminguvastendus** suvand **Küsimustike aruanne**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="0aa4f-1018">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1018">Select **OK**.</span></span>
4. <span data-ttu-id="0aa4f-1019">Konfigureerige dialoogiboksis **Elektroonilise aruande parameetrid** kiirkaardil **Kaasatavad kirjed** filtreerimissuvand nii, et kaasataks ainult küsimustik **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="0aa4f-1020">Valige filtreerimissuvandi kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="0aa4f-1021">Pange tähele, et kiirkaardil **Sihtkohad** on välja **Väljund** väärtuseks seatud **Ekraan**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="0aa4f-1022">Kui soovite konfigureeritud sihtkohta muuta, valige **Muuda**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![ER-i aruande käitusaja dialoogiboks, kus saate muuta konfigureeritud sihtkohta](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="0aa4f-1024">Aruande käivitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="0aa4f-1025">Vaadake loodud aruanne PDF-vormingus üle.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1025">Review the generated report in PDF format.</span></span>

    ![PDF-vormingus loodud aruande eelvaade ekraanil](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="0aa4f-1027">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1027">Additional resources</span></span>

- [<span data-ttu-id="0aa4f-1028">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0aa4f-1029">Elektroonilise aruandluse valemi keel</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="0aa4f-1030">Mitmekeelsete aruannete kujundamine</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="0aa4f-1031">ER-raamistiku API</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="0aa4f-1032">Funktsioon CASE</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="0aa4f-1033">Funktsioon CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="0aa4f-1034">Funktsioon DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="0aa4f-1035">Funktsioon FILTER</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="0aa4f-1036">Funktsioon FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="0aa4f-1037">Funktsioon FORMAT</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="0aa4f-1038">Funktsioon IF</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="0aa4f-1039">Funktsioon ORDERBY</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="0aa4f-1040">Funktsioon SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="0aa4f-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
