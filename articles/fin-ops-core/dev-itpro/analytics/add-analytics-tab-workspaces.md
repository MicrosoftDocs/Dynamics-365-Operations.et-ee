---
title: Analüüsi lisamine tööruumidele teenuse Power BI Embedded abil
description: See teema kirjeldab, kuidas kaasata Power BI aruanne tööruumi vahekaardile Analüüs.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 53c9d6343422f64aed74ce436bafd2c8b2ce1c3e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680932"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="4f77c-103">Analüüsi lisamine tööruumidele teenuse Power BI Embedded abil</span><span class="sxs-lookup"><span data-stu-id="4f77c-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4f77c-104">Seda funktsiooni toetatakse rakenduses Finance and Operations (versioon 7.2 ja uuem).</span><span class="sxs-lookup"><span data-stu-id="4f77c-104">This feature is supported in Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="4f77c-105">Sissejuhatus</span><span class="sxs-lookup"><span data-stu-id="4f77c-105">Introduction</span></span>
<span data-ttu-id="4f77c-106">See teema kirjeldab, kuidas kaasata Microsoft Power BI aruanne tööruumi vahekaardile **Analüüs**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="4f77c-107">Siin toodud näite puhul laiendame sõidukipargi halduse rakenduse tööruumi **Reserveerimise haldus**, et kaasata analüütiline tööruum vahekaardile **Analüütika**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4f77c-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="4f77c-108">Prerequisites</span></span>
+ <span data-ttu-id="4f77c-109">Juurdepääs arendaja keskkonnale, mis käitab platvormivärskendust 8 või uuemat.</span><span class="sxs-lookup"><span data-stu-id="4f77c-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="4f77c-110">Microsoft Power BI Desktopi abil loodud analüütiline aruanne (pbix-fail), millel on üksuse kaupluse andmebaasist hangitud andmemudel.</span><span class="sxs-lookup"><span data-stu-id="4f77c-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="4f77c-111">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="4f77c-111">Overview</span></span>
<span data-ttu-id="4f77c-112">Olenemata sellest, kas laiendate olemasolevat rakenduse tööruumi või võtate kasutusele omaenda uue tööruumi, saate kaasatud analüütiliste vaadete abil kuvada oma äriandmetest selgeid ja interaktiivseid vaateid.</span><span class="sxs-lookup"><span data-stu-id="4f77c-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="4f77c-113">Analüütilise tööruumi vahekaardi lisamise protsess koosneb neljast etapist.</span><span class="sxs-lookup"><span data-stu-id="4f77c-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="4f77c-114">Dynamicsi 365 ressursina pbix-faili lisamine.</span><span class="sxs-lookup"><span data-stu-id="4f77c-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="4f77c-115">Analüütilise tööruumi vahekaardi määratlemine.</span><span class="sxs-lookup"><span data-stu-id="4f77c-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="4f77c-116">Pbix-ressursi kaasamine tööruumi vahekaardile.</span><span class="sxs-lookup"><span data-stu-id="4f77c-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="4f77c-117">Valikuline: laienduste lisamine vaate kohandamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f77c-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="4f77c-118">Lisateavet analüütiliste aruannete loomise kohta vt teemast [Power BI Desktopiga alustamine](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="4f77c-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="4f77c-119">See leht on suurepärane allikas ülevaadete jaoks, mis aitavad teil luua mõjusaid analüütilise aruandluse lahendusi.</span><span class="sxs-lookup"><span data-stu-id="4f77c-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="4f77c-120">Ressursina pbix-faili lisamine</span><span class="sxs-lookup"><span data-stu-id="4f77c-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="4f77c-121">Enne alustamist peate looma või hankima Power BI aruande, mille soovite tööruumi kaasata.</span><span class="sxs-lookup"><span data-stu-id="4f77c-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="4f77c-122">Lisateavet analüütiliste aruannete loomise kohta vt teemast [Power BI Desktopiga alustamine](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="4f77c-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="4f77c-123">Pbix-faili lisamiseks Visual Studio projekti artefaktina toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f77c-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="4f77c-124">Looge asjakohases mudelis uus projekt.</span><span class="sxs-lookup"><span data-stu-id="4f77c-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="4f77c-125">Valige Solution Exploreris projekt, paremklõpsake seda ja seejärel valige suvandid **Lisa** \> **Uus üksus**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="4f77c-126">Valige dialoogiboksi **Uue üksuse lisamine** jaotises **Toimingute artefaktid** mall **Ressurss**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="4f77c-127">Sisestage nimi, mida kasutatakse aruande viitamiseks X++ metaandmetes, ja klõpsake nuppu **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Dialoogiboks Uue üksuse lisamine](media/analytical-workspace-add.png)

5. <span data-ttu-id="4f77c-129">Leidke pbix-fail, mis sisaldab analüütilise aruande määratlust, seejärel klõpsake käsku **Ava**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Dialoogiboks Ressursifaili valimine](media/analytical-workspace-select-resource.png)

<span data-ttu-id="4f77c-131">Nüüd kui olete lisanud pbix-faili Dynamics 365 ressursina, saate kaasata aruanded tööruumidesse ja lisada ka otselingid, kasutades menüü-üksusi.</span><span class="sxs-lookup"><span data-stu-id="4f77c-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="4f77c-132">Vahekaardi juhtelemendi lisamine rakenduse tööruumi</span><span class="sxs-lookup"><span data-stu-id="4f77c-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="4f77c-133">Selles näites laiendame mudeli Sõidukipargi haldus tööruumi **Reserveerimise haldus**, lisades vahekaardi **Analüütika** vormi **FMClerkWorkspace** määratlusele.</span><span class="sxs-lookup"><span data-stu-id="4f77c-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="4f77c-134">Järgmisel joonisel on näha, milline näeb vorm **FMClerkWorkspace** välja Microsoft Visual Studio kujundajas.</span><span class="sxs-lookup"><span data-stu-id="4f77c-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![Vorm FMClerkWorkspace enne muudatusi](media/analytical-workspace-definition-before.png)

<span data-ttu-id="4f77c-136">Vormi määratluse laiendamiseks tööruumi **Reserveerimise haldus** puhul toimige järgmisel.</span><span class="sxs-lookup"><span data-stu-id="4f77c-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="4f77c-137">Avage kujunduse määratluse laiendamiseks vormikujundaja.</span><span class="sxs-lookup"><span data-stu-id="4f77c-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="4f77c-138">Valige kujunduse määratluses ülemine element sildiga **Kujundus | Muster: tegevuses tööruum**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="4f77c-139">Paremklõpsake ja valige suvandid **Uus** \> **Vahekaart**, et lisada uus juhtelement nimega **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="4f77c-140">Valige vormikujundajas suvand **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="4f77c-141">Paremklõpsake ja valige uue vahekaardilehe lisamiseks suvand **Uus vahekaardileht**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="4f77c-142">Andke vahekaardilehele tähenduslik nimi, näiteks **Tööruum**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="4f77c-143">Valige vormikujundajas suvand **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="4f77c-144">Paremklõpsake ja valige suvand **Uus vahekaardileht**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="4f77c-145">Andke vahekaardilehele tähenduslik nimi, näiteks **Analüütika**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="4f77c-146">Valige vormikujundajas suvand **Analüütika (vahekaardileht)**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="4f77c-147">Seadke atribuudi **Pealdis** väärtuseks **Analüüs** ja seadke atribuudi **Automaatne deklaratsioon** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-147">Set the **Caption** property to **Analytics**, and set the **Auto Declaration** property to **Yes**.</span></span>
12. <span data-ttu-id="4f77c-148">Paremklõpsake juhtelementi ja valige suvandid **Uus** \> **Rühm**, et lisada uus vormirühma juhtelement.</span><span class="sxs-lookup"><span data-stu-id="4f77c-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="4f77c-149">Andke vormirühmale tähenduslik nimi, näiteks **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="4f77c-150">Valige vormikujundajas suvand **PanoramaBody (vahekaart)** ja seejärel lohistage juhtelement vahekaardile **Tööruum**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="4f77c-151">Valige kujunduse määratluses ülemine element sildiga **Kujundus | Muster: tegevuses tööruum**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="4f77c-152">Paremklõpsake ja valige suvand **Eemalda muster**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="4f77c-153">Paremklõpsake uuesti ja valige suvandid **Lisa muster** \> **Vahekaartidega tööruum**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="4f77c-154">Koostage järk muudatuste kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f77c-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="4f77c-155">Järgmisel joonisel on näha, milline näeb kujundus välja pärast nende muudatuste rakendamist.</span><span class="sxs-lookup"><span data-stu-id="4f77c-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace pärast muudatusi](media/analytical-workspace-definition-after.png)

<span data-ttu-id="4f77c-157">Nüüd, kui olete tööruumi aruande kaasamiseks kasutatavad vormi juhtelemendid lisanud, peate määratlema ülemjuhtelemendi suuruse, nii et see mahuks paigutusse.</span><span class="sxs-lookup"><span data-stu-id="4f77c-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="4f77c-158">Vaikimisi jäävad aruandes nähtavaks nii leht **Filtripaan** kui ka leht **Vahekaart**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="4f77c-159">Saate nende juhtelementide nähtavust siiski aruande sihttarbija vajaduste järgi muuta.</span><span class="sxs-lookup"><span data-stu-id="4f77c-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="4f77c-160">Kaasatud tööruumide puhul soovitame kasutada ühtluse nimel laiendusi nii lehe **Filtripaan** kui ka **Vahekaart** peitmiseks.</span><span class="sxs-lookup"><span data-stu-id="4f77c-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="4f77c-161">Nüüd olete rakenduse vormimääratluse laiendamise ülesande täitnud.</span><span class="sxs-lookup"><span data-stu-id="4f77c-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="4f77c-162">Lisateavet laienduste kasutamise ja kohanduste tegemise kohta vaadake jaotisest [Kohandamine laienduste ja ülekatte kaudu](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="4f77c-162">For more information about how to use extensions to do customizations, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="4f77c-163">X++ äriloogika lisamine vaaturi juhtelemendi kaasamiseks</span><span class="sxs-lookup"><span data-stu-id="4f77c-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="4f77c-164">Tööruumi **Reserveerimise haldus** kaasatud aruandevaaturi juhtelementi lähtestava äriloogika lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4f77c-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="4f77c-165">Avage kujunduse määratluse laiendamiseks vormikujundaja **FMClerkWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="4f77c-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="4f77c-166">Vajutage klahvi F7, et pääseda juurde koodimääratluse taga olevale koodile.</span><span class="sxs-lookup"><span data-stu-id="4f77c-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="4f77c-167">Lisage järgmine X++ kood.</span><span class="sxs-lookup"><span data-stu-id="4f77c-167">Add the following X++ code.</span></span>

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="4f77c-168">Koostage järk muudatuste kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f77c-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="4f77c-169">Nüüd olete kaasatud aruandevaaturi juhtelementi lähtestava äriloogika lisamise ülesande täitnudl.</span><span class="sxs-lookup"><span data-stu-id="4f77c-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="4f77c-170">Järgmisel joonisel on näha, milline näeb tööruum välja pärast nende muudatuste rakendamist.</span><span class="sxs-lookup"><span data-stu-id="4f77c-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Tööruumi kaasatud aruanne](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="4f77c-172">Pääsete juurde olemasolevale toiminguvaatele, kasutades lehe pealkirja all olevaid tööruumi vahekaarte.</span><span class="sxs-lookup"><span data-stu-id="4f77c-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="4f77c-173">Viide</span><span class="sxs-lookup"><span data-stu-id="4f77c-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="4f77c-174">Meetod PBIReportHelper.initializeReportControl</span><span class="sxs-lookup"><span data-stu-id="4f77c-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="4f77c-175">See jaotis annab teavet abilise klassi kohta, mida kasutatakse Power BI aruande kaasamiseks (pbix-ressurss) vormirühma juhtelementi.</span><span class="sxs-lookup"><span data-stu-id="4f77c-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="4f77c-176">Süntaks</span><span class="sxs-lookup"><span data-stu-id="4f77c-176">Syntax</span></span>
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="4f77c-177">Parameetrid</span><span class="sxs-lookup"><span data-stu-id="4f77c-177">Parameters</span></span>

| <span data-ttu-id="4f77c-178">Nimi</span><span class="sxs-lookup"><span data-stu-id="4f77c-178">Name</span></span>             | <span data-ttu-id="4f77c-179">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4f77c-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f77c-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="4f77c-180">resourceName</span></span>     | <span data-ttu-id="4f77c-181">Pbix-ressursi nimi</span><span class="sxs-lookup"><span data-stu-id="4f77c-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="4f77c-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="4f77c-182">formGroupControl</span></span> | <span data-ttu-id="4f77c-183">Vormirühma juhtelement, millele Power BI aruande juhtelement rakendada.</span><span class="sxs-lookup"><span data-stu-id="4f77c-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="4f77c-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="4f77c-184">defaultPageName</span></span>  | <span data-ttu-id="4f77c-185">Vaikelehe nimi.</span><span class="sxs-lookup"><span data-stu-id="4f77c-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="4f77c-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="4f77c-186">showFilterPane</span></span>   | <span data-ttu-id="4f77c-187">Kahendmuutuja väärtus, mis näitab, kas filtripaan tuleb kuvada (**tõene**) või peita (**väär**).</span><span class="sxs-lookup"><span data-stu-id="4f77c-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="4f77c-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="4f77c-188">showNavPane</span></span>      | <span data-ttu-id="4f77c-189">Kahendmuutuja väärtus, mis näitab, kas navigeerimispaan tuleb kuvada (**tõene**) või peita (**väär**).</span><span class="sxs-lookup"><span data-stu-id="4f77c-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="4f77c-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="4f77c-190">defaultFilters</span></span>   | <span data-ttu-id="4f77c-191">Power BI aruande vaikefiltrid.</span><span class="sxs-lookup"><span data-stu-id="4f77c-191">The default filters for the Power BI report.</span></span>                                                                 |
