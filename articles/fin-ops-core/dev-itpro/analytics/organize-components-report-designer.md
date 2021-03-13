---
title: Aruande komponentide korraldamine aruandekoosturis
description: Selles teemas selgitatakse olemasolevate aruannete, koosteüksuste ja objektide korraldamist aruandekoosturis.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b55dcee00f571228ec1e933306d77d9edc12866
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092419"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="3d99d-103">Aruande komponentide korraldamine aruandekoosturis</span><span class="sxs-lookup"><span data-stu-id="3d99d-103">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d99d-104">Kui olete koosteüksused kujundanud ja aruanded koostanud, on abiks nende objektide korraldamine, et kasutajatel oleks neid hõlpsam leida.</span><span class="sxs-lookup"><span data-stu-id="3d99d-104">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="3d99d-105">Selles artiklis kirjeldatakse olemasolevate aruannete,koosteüksuste ja objektide korraldamist aruandekoosturis.</span><span class="sxs-lookup"><span data-stu-id="3d99d-105">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="3d99d-106">Failide korraldamiseks saate aruandekoosturis kaustu, aruandeid, koosteüksusi ja muid objekte ümber nimetada.</span><span class="sxs-lookup"><span data-stu-id="3d99d-106">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="3d99d-107">Ümbernimetatava objekti tüübist olenevalt võib teil olla vaja selle objekti seoseid värskendada.</span><span class="sxs-lookup"><span data-stu-id="3d99d-107">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="3d99d-108">Aruande kujundaja kausta või koosteüksuse ümbernimetamine</span><span class="sxs-lookup"><span data-stu-id="3d99d-108">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="3d99d-109">Saate aruandekoosturis kaustade, aruande-, rea-, veeru- ja aruandluspuu definitsioonide nime muuta.</span><span class="sxs-lookup"><span data-stu-id="3d99d-109">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="3d99d-110">Kausta või koosteüksuse ümbernimetamine aruandekoosturis</span><span class="sxs-lookup"><span data-stu-id="3d99d-110">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="3d99d-111">Kasutage aruandekoosturis ümbernimetatava kausta või objekti leidmiseks navigeerimispaani.</span><span class="sxs-lookup"><span data-stu-id="3d99d-111">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="3d99d-112">Paremklõpsake kausta või objekti ja seejärel klõpsake suvandit **Nimeta ümber**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-112">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="3d99d-113">Navigeerimispaani väli **Nimi** muutub aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="3d99d-113">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="3d99d-114">Sisestage uus nimi ja seejärel vajutage suvandit Sisesta.</span><span class="sxs-lookup"><span data-stu-id="3d99d-114">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="3d99d-115">Kui koosteüksus on readefinitsioon, veeru definitsioon või aruandluspuu definitsioon, peate värskendama teisi sellega seotud koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="3d99d-115">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="3d99d-116">Paremklõpsake 3. etapis ümbernimetatud koosteüksust, valige **Seosed** ja seejärel valige element loendist selle värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="3d99d-116">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="3d99d-117">Korrake 4. etappi, kuni kõik seotud elemendid on värskendatud.</span><span class="sxs-lookup"><span data-stu-id="3d99d-117">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="3d99d-118">Aruandegruppide loomine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="3d99d-118">Create and manage report groups</span></span>
<span data-ttu-id="3d99d-119">Saate grupeerida aruande definitsioone korraga mitme aruande loomiseks.</span><span class="sxs-lookup"><span data-stu-id="3d99d-119">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="3d99d-120">Aruandegruppide loomiseks, muutmiseks ja kustutamiseks peab teil olema kujundaja või administraatori roll.</span><span class="sxs-lookup"><span data-stu-id="3d99d-120">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="3d99d-121">Looja rolliga kasutajad saavad aruandegruppe luua ja ka aruandegruppide kasutaja aruande definitsiooni seadistust muuta.</span><span class="sxs-lookup"><span data-stu-id="3d99d-121">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="3d99d-122">Aruandegrupi loomine</span><span class="sxs-lookup"><span data-stu-id="3d99d-122">Create a report group</span></span>

1. <span data-ttu-id="3d99d-123">Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-123">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="3d99d-124">Klõpsake menüüs **Fail** valikuid **Uus** &gt; **Aruandegrupi definitsioon** uue aruandegrupi avamiseks vaaturi aknas.</span><span class="sxs-lookup"><span data-stu-id="3d99d-124">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="3d99d-125">Teine võimalus on klõpsata tööriistaribal nuppu **Aruandegrupp** ![Aruandegrupp](media/report-group.gif "Aruanderühm")</span><span class="sxs-lookup"><span data-stu-id="3d99d-125">Alternatively, click the **Report Group** button ![Report Group](media/report-group.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="3d99d-126">Klõpsake vahekaarti **Aruandegrupp**. Eraldi aruande definitsioonide teabe tühistamiseks selle aruande loomise puhul märkige ruut **Ettevõtte, üksikasjade ja kuupäeva sätete tühistamine** eraldi aruande definitsioonidest.</span><span class="sxs-lookup"><span data-stu-id="3d99d-126">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="3d99d-127">Ettevõtte nime, üksikasjataseme, tinglikkuse seadistuse ja kuupäeva teave sisestatakse automaatselt, kuid saate endiselt värskendusi teha.</span><span class="sxs-lookup"><span data-stu-id="3d99d-127">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="3d99d-128">Mitme arvestusvaluutasid näitava aruande koostamiseks märkige ruut **Kaasa kõik aruandlusvaluutad**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-128">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="3d99d-129">Seejärel pääsete mitmesse vaatesse, klõpsates aruande vaatamisel veebivaaturis nuppu **Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-129">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="3d99d-130">Aruandegruppi kaasatavate aruannete valimiseks klõpsake väljal **Grupi aruanded** valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-130">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="3d99d-131">Mitme aruande valimiseks dialoogiboksis **Lisa** hoidke aruannete valimisel all klahvi Ctrl.</span><span class="sxs-lookup"><span data-stu-id="3d99d-131">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="3d99d-132">Kui olete aruannete valimise lõpetanud, klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-132">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="3d99d-133">Uue aruandegrupi salvestamiseks klõpsake **Fail** &gt; **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-133">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="3d99d-134">Aruandegrupi muutmine</span><span class="sxs-lookup"><span data-stu-id="3d99d-134">Modify a report group</span></span>

1. <span data-ttu-id="3d99d-135">Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-135">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="3d99d-136">Aruandegrupi muutmiseks topeltklõpsake.</span><span class="sxs-lookup"><span data-stu-id="3d99d-136">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="3d99d-137">Tehke vahekaardil **Aruandegrupp** soovitud muudatused.</span><span class="sxs-lookup"><span data-stu-id="3d99d-137">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="3d99d-138">Klõpsake menüüs **Fail** käsku **Salvesta** muudetud aruandegrupi salvestamiseks. Teine võimalus on klõpsata tööriistaribal nuppu **Salvesta** ![Salvesta](media/save.gif "Salvesta")</span><span class="sxs-lookup"><span data-stu-id="3d99d-138">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](media/save.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="3d99d-139">Kui olete plaaninud aruanded määratud vahemikel koostamiseks, saate need sätted tühistada ja aruande kohe luua.</span><span class="sxs-lookup"><span data-stu-id="3d99d-139">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="3d99d-140">Aruandegrupi aruande loomine</span><span class="sxs-lookup"><span data-stu-id="3d99d-140">Generate a report group report</span></span>

1. <span data-ttu-id="3d99d-141">Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-141">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="3d99d-142">Avage loodav aruandegrupp.</span><span class="sxs-lookup"><span data-stu-id="3d99d-142">Open the report group to generate.</span></span>
3. <span data-ttu-id="3d99d-143">Klõpsake aruannete loomiseks nuppu **Loo aruanne** ![Loo aruanne](media/generate-report.gif "Aruande loomine")</span><span class="sxs-lookup"><span data-stu-id="3d99d-143">Click the **Generate Report** button ![Generate Report](media/generate-report.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="3d99d-144">Aruandegrupi kustutamine</span><span class="sxs-lookup"><span data-stu-id="3d99d-144">Delete a report group</span></span>

1. <span data-ttu-id="3d99d-145">Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="3d99d-146">Paremklõpsake kustutamiseks aruandegruppi ja seejärel tehke valik **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-146">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="3d99d-147">Kui kuvatakse kinnitusteade, klõpsake valikut **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3d99d-147">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="3d99d-148">Vahekaardi Aruandegrupp juhtelemendid</span><span class="sxs-lookup"><span data-stu-id="3d99d-148">Report Group tab controls</span></span>
<span data-ttu-id="3d99d-149">Järgmises tabelis kirjeldatakse vahekaardi **Aruandegrupp** juhtelemente.</span><span class="sxs-lookup"><span data-stu-id="3d99d-149">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3d99d-150">Juhtelement</span><span class="sxs-lookup"><span data-stu-id="3d99d-150">Control</span></span></th>
<th><span data-ttu-id="3d99d-151">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3d99d-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3d99d-152">Ettevõtte, üksikasjade ja kuupäeva sätete tühistamine individuaalsetest aruande definitsioonidest</span><span class="sxs-lookup"><span data-stu-id="3d99d-152">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="3d99d-153">Märkige see ruut selle aruandegrupi aruannete individuaalsete aruande definitsioonide tühistamiseks ainult nende aruannete loomise puhul.</span><span class="sxs-lookup"><span data-stu-id="3d99d-153">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d99d-154">Ettevõtte nimi</span><span class="sxs-lookup"><span data-stu-id="3d99d-154">Company name</span></span></td>
<td><span data-ttu-id="3d99d-155">Aruannete puhul kasutatava ettevõtte valimine.</span><span class="sxs-lookup"><span data-stu-id="3d99d-155">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d99d-156">Üksikasjatase</span><span class="sxs-lookup"><span data-stu-id="3d99d-156">Detail level</span></span></td>
<td><span data-ttu-id="3d99d-157">Määrake aruannete üksikasjatase.</span><span class="sxs-lookup"><span data-stu-id="3d99d-157">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="3d99d-158"><strong>Finantsid</strong> – kõrgetasemeline kokkuvõttev aruanne.</span><span class="sxs-lookup"><span data-stu-id="3d99d-158"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="3d99d-159">Te ei saa kontodes ja dimensioonides süvitsi minna, välja arvatud aruandluspuu kaudu lisatud kontode ning dimensioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="3d99d-159">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="3d99d-160"><strong>Rahaline &amp; Konto</strong> − aruanne, mis sisaldab kõrgetasemelist kokkuvõtet ja konto üksikasju.</span><span class="sxs-lookup"><span data-stu-id="3d99d-160"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="3d99d-161"><strong>Rahaline, Konto &amp; Kanne</strong> − aruanne, mis sisaldab kõrgetasemelist kokkuvõtet ja kande üksikasju..</span><span class="sxs-lookup"><span data-stu-id="3d99d-161"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="3d99d-162">Tinglik</span><span class="sxs-lookup"><span data-stu-id="3d99d-162">Provisional</span></span></td>
<td><span data-ttu-id="3d99d-163">Määrake aruannete tegevuste tüübid.</span><span class="sxs-lookup"><span data-stu-id="3d99d-163">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="3d99d-164"><strong>Ainult sisestatud toiming</strong> – kaasake ainult finantsandmetes sisestatud kanded ja saldod.</span><span class="sxs-lookup"><span data-stu-id="3d99d-164"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="3d99d-165"><strong>Sisestatud ja sisestamata toiming</strong> – kaasake kõik finantsandmetesse sisestatud ja saadetud kanded ja saldod.</span><span class="sxs-lookup"><span data-stu-id="3d99d-165"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="3d99d-166"><strong>Ainult sisestamata toiming</strong> – kaasake ainult finantsandmetesse sisestatud, kuid veel saatmata kanded.</span><span class="sxs-lookup"><span data-stu-id="3d99d-166"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="3d99d-167">Kõigi aruandlusvaluutade kaasamine</span><span class="sxs-lookup"><span data-stu-id="3d99d-167">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="3d99d-168">Kui teie Microsoft Dynamicsi ERP-süsteemis on konfigureeritud täiendavaid aruandlusvaluutasid, loetletakse need siin.</span><span class="sxs-lookup"><span data-stu-id="3d99d-168">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="3d99d-169">Märkige see ruut lisaaruannete koostamiseks näidatud valuutades.</span><span class="sxs-lookup"><span data-stu-id="3d99d-169">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="3d99d-170">Aruannete vaatamiseks veebivaaturis klõpsake nuppu <strong>Valuuta</strong> ja valige valuuta.</span><span class="sxs-lookup"><span data-stu-id="3d99d-170">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d99d-171">Aruande definitsiooni ei salvestatud kuupäevateavet</span><span class="sxs-lookup"><span data-stu-id="3d99d-171">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="3d99d-172">Baasperiood</span><span class="sxs-lookup"><span data-stu-id="3d99d-172">Base period</span></span></li>
<li><span data-ttu-id="3d99d-173">Baasaasta</span><span class="sxs-lookup"><span data-stu-id="3d99d-173">Base year</span></span></li>
<li><span data-ttu-id="3d99d-174">Ajavahemik</span><span class="sxs-lookup"><span data-stu-id="3d99d-174">Period covered</span></span></li>
</ul>
<span data-ttu-id="3d99d-175">Aruande definitsiooni salvestatakse ainult baasperioodi vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="3d99d-175">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d99d-176">Aruande definitsiooni salvestati kuupäevateave</span><span class="sxs-lookup"><span data-stu-id="3d99d-176">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="3d99d-177">Aruande kuupäev</span><span class="sxs-lookup"><span data-stu-id="3d99d-177">Report date</span></span></li>
<li><span data-ttu-id="3d99d-178">Vaikimisi baasperiood</span><span class="sxs-lookup"><span data-stu-id="3d99d-178">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="3d99d-179">Rühma aruanded</span><span class="sxs-lookup"><span data-stu-id="3d99d-179">Reports in group</span></span></td>
<td><span data-ttu-id="3d99d-180">Aruandegrupi aruannete lisamine, eemaldamine ja ümberkorraldamine.</span><span class="sxs-lookup"><span data-stu-id="3d99d-180">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="3d99d-181">Aruandedefinitsioonide lisamiseks aruanderühma topeltklõpsake aruanderühma, et see avada, ning klõpsake seejärel suvandit <strong>Lisa</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d99d-181">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="3d99d-182">Valige aruanderühma kaasatavad aruanded ning klõpsake seejärel <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d99d-182">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="3d99d-183">Aruande eemaldamiseks aruanderühmast valige see ja klõpsake seejärel käsku <strong>Eemalda</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d99d-183">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="3d99d-184">Aruannete loomise järjestuse muutmiseks valige loendist aruanne ja seejärel klõpsake valikut <strong>Liigu üles</strong> või <strong>Liigu alla</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d99d-184">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="3d99d-185">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3d99d-185">Additional resources</span></span>

[<span data-ttu-id="3d99d-186">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="3d99d-186">Financial reporting</span></span>](financial-reporting-intro.md)
