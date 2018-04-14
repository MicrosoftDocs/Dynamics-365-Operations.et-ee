---
title: Eelarve plaanimise mallid Excelile
description: See teema kirjeldab, kuidas luua Microsoft Exceli malle, mida saab kasutada eelarveplaanidega.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8b597f417fc144b90aa6469ebe1b9961dc968c15
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="b2d59-103">Eelarve plaanimise mallid Excelile</span><span class="sxs-lookup"><span data-stu-id="b2d59-103">Budget planning templates for Excel</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b2d59-104">See teema kirjeldab, kuidas luua Microsoft Exceli malle, mida saab kasutada eelarveplaanidega.</span><span class="sxs-lookup"><span data-stu-id="b2d59-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="b2d59-105">Teema näitab, kuidas luua Exceli malle, mida kasutatakse eelarveplaanidega, kasutades standardset demoandmekogumit ja administraatori identimisteavet.</span><span class="sxs-lookup"><span data-stu-id="b2d59-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="b2d59-106">Lisateavet eelarve plaanimise kohta vt teemast [Eelarve plaanimise ülevaade.](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="b2d59-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="b2d59-107">Saate vaadata ka õppetükki [Eelarve plaanimine 101](budget-plan.md), et tutvuda baasmooduli konfigureerimise ja kasutuspõhimõtetega.</span><span class="sxs-lookup"><span data-stu-id="b2d59-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="b2d59-108">Töölehe loomine eelarveplaani dokumendi paigutusega</span><span class="sxs-lookup"><span data-stu-id="b2d59-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="b2d59-109">Eelarveplaani dokumente saab vaadata ja redigeerida üht või mitut paigutust kasutades.</span><span class="sxs-lookup"><span data-stu-id="b2d59-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="b2d59-110">Igal paigutusel võib olla seostatud eelarveplaani dokumendimall, et saaksite eelarveplaani andmeid vaadata ja redigeerida Exceli töölehel.</span><span class="sxs-lookup"><span data-stu-id="b2d59-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="b2d59-111">Selles teemas luuakse eelarveplaani dokumendimall olemasolevat paigutuse konfiguratsiooni kasutades.</span><span class="sxs-lookup"><span data-stu-id="b2d59-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="b2d59-112">Avage **Eelarveplaanide loend** (**Eelarvestus** &gt; **Eelarveplaanid**).</span><span class="sxs-lookup"><span data-stu-id="b2d59-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="b2d59-113">Klõpsake uue eelarveplaani dokumendi loomiseks valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-113">Click **New** to create a new budget plan document.</span></span> 

   <span data-ttu-id="b2d59-114">[![Eelarveplaanide loend](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="b2d59-115">Ridade lisamiseks kasutage valikut **Lisa** rida.</span><span class="sxs-lookup"><span data-stu-id="b2d59-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="b2d59-116">Eelarveplaani dokumendi paigutuse konfiguratsiooni kuvamiseks klõpsake valikut **Paigutused**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

   <span data-ttu-id="b2d59-117">[![Lisa eelarveplaanid](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="b2d59-118">Saate paigutuse konfiguratsiooni üle vaadata ja seda vajaduse korral korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="b2d59-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="b2d59-119">Selle paigutuse jaoks Exceli faili loomiseks minge jaotisse **Mall** &gt; **Loo**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="b2d59-120">Kui mall on loodud, minge jaotisse **Mall** &gt; **Kuva**, et eelarveplaani dokumendimall avada ja üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="b2d59-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="b2d59-121">Saate Exceli faili salvestada kohalikule kettale.</span><span class="sxs-lookup"><span data-stu-id="b2d59-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="b2d59-122">[![Salvesta nimega](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="b2d59-123">Eelarveplaani dokumendi paigutust ei saa enam redigeerida, kui Exceli mall on sellega seostatud.</span><span class="sxs-lookup"><span data-stu-id="b2d59-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="b2d59-124">Paigutuse muutmiseks kustutage seostatud Exceli malli fail ja looge see uuesti.</span><span class="sxs-lookup"><span data-stu-id="b2d59-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="b2d59-125">See on vajalik selleks, et hoida paigutuse ja töölehe väljad sünkroonis.</span><span class="sxs-lookup"><span data-stu-id="b2d59-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="b2d59-126">Exceli mall sisaldab kõiki eelarveplaani dokumendi paigutuse elemente, kui veeru **Saadaval töölehel** sätteks on valitud Tõene.</span><span class="sxs-lookup"><span data-stu-id="b2d59-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="b2d59-127">Exceli mallis pole elementide kattumine lubatud.</span><span class="sxs-lookup"><span data-stu-id="b2d59-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="b2d59-128">Näiteks kui paigutus sisaldab veerge Taotlus Q1, Taotlus Q2, Taotlus Q3 ja Taotlus Q4 ning taotluste koondveergu, mis kujutab kõigi neljandikveergude summat, saab Exceli mallis kasutada ainult neljandikveerge või koondveergu.</span><span class="sxs-lookup"><span data-stu-id="b2d59-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="b2d59-129">Exceli fail ei saa kattuvaid veerge värskendamise ajal värskendada, kuna tabelis olevad andmed muutuvad ajakohatuks ja ebatäpseks.</span><span class="sxs-lookup"><span data-stu-id="b2d59-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="b2d59-130">[![Näide](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="b2d59-131">Exceliga eelarveplaani andmete vaatamisel ja redigeerimisel võimalike probleemide vältimiseks peab sama kasutaja olema sisse loginud nii Microsoft Dynamics 365 for Finance and Operationsisse kui ka Microsoft Dynamics Office’i lisandmooduli andmekonnektorisse.</span><span class="sxs-lookup"><span data-stu-id="b2d59-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="b2d59-132">Eelarveplaani dokumendimallile päise lisamine</span><span class="sxs-lookup"><span data-stu-id="b2d59-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="b2d59-133">Päiseteabe lisamiseks valige Exceli failis ülemine rida ja sisestage tühjad read.</span><span class="sxs-lookup"><span data-stu-id="b2d59-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="b2d59-134">Exceli failile päiseväljade lisamiseks klõpsake rakenduses **Andmekonnektor** valikut **Kujundus**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="b2d59-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="b2d59-136">Klõpsake vahekaardil **Kujundus** välju **Lisa** ja valige üksuse andmeallikaks **BudgetPlanHeader**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="b2d59-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="b2d59-138">Viige kursor Exceli failis soovitud kohta.</span><span class="sxs-lookup"><span data-stu-id="b2d59-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="b2d59-139">Valitud asukohta väljasildi lisamiseks klõpsake valikut **Lisa silt**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="b2d59-140">Valitud kohta väärtusevälja lisamiseks klõpsake valikut **Lisa väärtus**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="b2d59-141">Kujundaja sulgemiseks klõpsake valikut **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="b2d59-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="b2d59-143">Eelarveplaani dokumendimalli tabelisse arvutatud veeru lisamine</span><span class="sxs-lookup"><span data-stu-id="b2d59-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="b2d59-144">Seejärel lisatakse arvutatud veerud loodud eelarveplaani dokumendimallile.</span><span class="sxs-lookup"><span data-stu-id="b2d59-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="b2d59-145">Veerg **Koondtaotlus**, mis koondab veerud Taotlus Q1 : Taotlus Q4, ja veerg **Korrigeerimine**, mis arvutab veeru **Koondtaotlus** eelmääratletud teguri alusel ümber.</span><span class="sxs-lookup"><span data-stu-id="b2d59-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="b2d59-146">Tabelile veergude lisamiseks klõpsake rakenduses **Andmekonnektor** valikut **Kujundus**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="b2d59-147">Veergude lisamise alustamiseks klõpsake andmeallika **BudgetPlanWorksheet** kõrval olevat valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="b2d59-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="b2d59-149">Valitud väljagrupis kuvatakse mallis saadaolevad veerud.</span><span class="sxs-lookup"><span data-stu-id="b2d59-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="b2d59-150">Uue veeru lisamiseks klõpsake valikut **Valem**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="b2d59-151">Andke uuele veerule nimi ja kleepige valem väljale **Valem**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="b2d59-152">Veeru sisestamiseks klõpsake valikut **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="b2d59-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="b2d59-154">Valemi määratlemiseks looge valem arvutustabelis ja kopeerige see aknasse **Kujundus**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="b2d59-155">Finance and Operationsiga seotud tabelile antakse tavaliselt nimi AXTable1.</span><span class="sxs-lookup"><span data-stu-id="b2d59-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="b2d59-156">Näiteks veergude Taotlus Q1 : Taotlus Q4 columns summeerimiseks arvutustabelis saate kasutada valemit AxTable1\[Taotlus Q1\]+AxTable1\[Taotlus Q2\]+AxTable1\[Taotlus Q3\]+AxTable1\[Taotlus Q4\].</span><span class="sxs-lookup"><span data-stu-id="b2d59-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="b2d59-157">Korrake neid etappe veeru **Korrigeerimine** lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="b2d59-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="b2d59-158">Kasutage selle veeru puhul valemit AxTable1\[Koondtaotlus\]\*$I$1.</span><span class="sxs-lookup"><span data-stu-id="b2d59-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="b2d59-159">See võtab väärtuse lahtrist I1 ja korrutab väärtustega veerus **Koondtaotlus**, et arvutada korrigeerimise summad.</span><span class="sxs-lookup"><span data-stu-id="b2d59-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="b2d59-160">Salvestage ja sulgege Exceli fail.</span><span class="sxs-lookup"><span data-stu-id="b2d59-160">Save and close the Excel file.</span></span> <span data-ttu-id="b2d59-161">Naaske Finance and Operationsisse ja klõpsake aknas **Paigutused** valikuid **Mall &gt; Üleslaadimine**, et laadida eelarveplaani jaoks kasutatav salvestatud Exceli mall üles.</span><span class="sxs-lookup"><span data-stu-id="b2d59-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="b2d59-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="b2d59-163">Sulgege liugaken **Paigutused**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="b2d59-164">Dokumendi kuvamiseks ja redigeerimiseks Excelis klõpsake **Eelarveplaani** dokumendis valikut **Tööleht**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="b2d59-165">Pange tähele, et selle eelarveplaani töölehe loomiseks kasutati korrigeeritud Exceli malli ja arvutatud veerge värskendatakse valemitega, mille määratlesite eelmistes etappides.</span><span class="sxs-lookup"><span data-stu-id="b2d59-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="b2d59-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="b2d59-167">Näpunäited ja vihjed eelarveplaani mallide loomiseks</span><span class="sxs-lookup"><span data-stu-id="b2d59-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="b2d59-168">Kas eelarveplaani mallile saab lisada ka täiendavaid andmeallikaid ja neid kasutada?</span><span class="sxs-lookup"><span data-stu-id="b2d59-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="b2d59-169">Jah, saate samale või teistele Exceli malli lehtedele lisada lisaüksusi, kasutades menüüd **Kujundus**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="b2d59-170">Näiteks saate lisada andmeallika **BudgetPlanProposedProject**, et luua ja hallata pakutavate projektide loendit, töötades samal ajal Excelis eelarveplaani andmetega.</span><span class="sxs-lookup"><span data-stu-id="b2d59-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="b2d59-171">Pange tähele, et suuremahuliste andmeallikate lisamine võib mõjutada Exceli töövihiku jõudlust.</span><span class="sxs-lookup"><span data-stu-id="b2d59-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="b2d59-172">Täiendavatele andmeallikatele saate lisada soovitud filtreid, kasutades rakenduse **Andmekonnektor** valikut **Filter**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="b2d59-173">Kas Andmekonnektori valikut Kujundus saab teiste kasutajate eest peita?</span><span class="sxs-lookup"><span data-stu-id="b2d59-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="b2d59-174">Jah, valiku **Kujundus** peitmiseks avage **Andmekonnektori** suvandid.</span><span class="sxs-lookup"><span data-stu-id="b2d59-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="b2d59-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="b2d59-176">Laiendage jaotist **Andmekonnektori suvandid** ja tühjendage ruut **Luba kujundus**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="b2d59-177">See peidab valiku **Kujundus** rakendusest **Andmekonnektor**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="b2d59-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="b2d59-179">Kas Andmekonnektori kogemata sulgemist andmetega töötamise ajal saab takistada?</span><span class="sxs-lookup"><span data-stu-id="b2d59-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="b2d59-180">Soovitame malli lukustada, et kasutajad ei saaks seda sulgeda.</span><span class="sxs-lookup"><span data-stu-id="b2d59-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="b2d59-181">Lukustamiseks klõpsake valikut **Andmekonnektor**. Paremas ülanurgas kuvatakse ikoon.</span><span class="sxs-lookup"><span data-stu-id="b2d59-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="b2d59-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="b2d59-183">Klõpsake lisamenüü avamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="b2d59-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="b2d59-184">Valige **Lukusta**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="b2d59-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="b2d59-186">Kas eelarveplaani mallidega saab kasutada ka muid Exceli funktsioone, nagu lahtrite vormindamine, värvid, tingimusvorming ja diagrammid?</span><span class="sxs-lookup"><span data-stu-id="b2d59-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="b2d59-187">Jah, eelarveplaani mallidega töötab enamik Exceli standardvõimalusi.</span><span class="sxs-lookup"><span data-stu-id="b2d59-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="b2d59-188">Soovitame kasutada värvitähistusi, et kasutajad saaksid eristada kirjutuskaitstud ja redigeeritavaid veerge.</span><span class="sxs-lookup"><span data-stu-id="b2d59-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="b2d59-189">Tingimusvormingut kasutades saab esile tõsta eelarve probleemsed osad.</span><span class="sxs-lookup"><span data-stu-id="b2d59-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="b2d59-190">Veergude kogusummasid saab hõlpsasti esitada Exceli standardsete valemitega, mille leiate tabeli kohalt.</span><span class="sxs-lookup"><span data-stu-id="b2d59-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="b2d59-191">Samuti saate eelarveandmete täiendavaks grupeerimiseks ja visualiseerimiseks luua ning kasutada ka liigendtabeleid ja diagramme.</span><span class="sxs-lookup"><span data-stu-id="b2d59-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="b2d59-192">Klõpsake vahekaardil **Andmed** grupis **Ühendused** valikut **Värskenda kõik** ja seejärel valikut **Ühenduse atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="b2d59-193">Klõpsake vahekaarti **Kasutus**. Märkige jaotises **Värskendamine** ruut **Värskenda andmeid faili avamisel**.</span><span class="sxs-lookup"><span data-stu-id="b2d59-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="b2d59-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="b2d59-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




