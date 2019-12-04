---
title: Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)
description: See teema selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide genereerimiseks OPENXML-vormingus.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcceb0e4d5f3bec54598515da0a5cbd8d11def3d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769851"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="3f470-103">Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)</span><span class="sxs-lookup"><span data-stu-id="3f470-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f470-104">See teema selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide genereerimiseks OPENXML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="3f470-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="3f470-105">Seda konfiguratsiooni kasutatakse hankija maksete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="3f470-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="3f470-106">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha ka GBSI ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="3f470-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="3f470-107">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="3f470-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="3f470-108">Samuti peab teil olema Exceli fail, mis imporditakse malli loomisel.</span><span class="sxs-lookup"><span data-stu-id="3f470-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="3f470-109">Sellele failile pääseb juurde [Maksearuande mallist](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="3f470-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="3f470-110">Makse andmemudeli konfiguratsiooni üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="3f470-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="3f470-111">Navigeerimispaanil avage **Moodulid > Organisatsiooni haldus > Tööruumid > Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="3f470-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="3f470-112">Märkige loendis näidisettevõtte seadistuse pakkujaks Litware, Inc. Kui seda seadistuse pakkujat pole näha, peate esmalt lõpetama etapid teemas [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="3f470-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="3f470-113">Valige **Määra aktiivseks**.</span><span class="sxs-lookup"><span data-stu-id="3f470-113">Select **Set active**.</span></span>
4. <span data-ttu-id="3f470-114">Valige **Osad**.</span><span class="sxs-lookup"><span data-stu-id="3f470-114">Select **Repositories**.</span></span> <span data-ttu-id="3f470-115">Valige võimaluse korral tüübi Operationsi ressursid jaoks hoidla.</span><span class="sxs-lookup"><span data-stu-id="3f470-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="3f470-116">Kui see on saadaval, jätke uue hoidla loomise järgmised etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="3f470-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="3f470-117">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="3f470-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="3f470-118">Väljas **Seadistuse osa tüüp** sisestage `Operations resourcesdd`.</span><span class="sxs-lookup"><span data-stu-id="3f470-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="3f470-119">Valige käsk **Loo hoidla**.</span><span class="sxs-lookup"><span data-stu-id="3f470-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="3f470-120">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f470-120">Select **OK**.</span></span>
9. <span data-ttu-id="3f470-121">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="3f470-121">Select **Open**.</span></span>
10. <span data-ttu-id="3f470-122">Valige puult suvand **Maksemudel**.</span><span class="sxs-lookup"><span data-stu-id="3f470-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="3f470-123">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="3f470-123">Select **Import**.</span></span> <span data-ttu-id="3f470-124">Importige see andmemudel.</span><span class="sxs-lookup"><span data-stu-id="3f470-124">Import this data model.</span></span> <span data-ttu-id="3f470-125">Seda kasutatakse andmeallikana uues vormingu konfiguratsioonis.</span><span class="sxs-lookup"><span data-stu-id="3f470-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="3f470-126">Jätke see etapp vahele, kui see konfiguratsioon on juba imporditud.</span><span class="sxs-lookup"><span data-stu-id="3f470-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="3f470-127">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3f470-127">Select **Yes**.</span></span>
13. <span data-ttu-id="3f470-128">Sulgege lehed kuni naasete lehele „Elektrooniline aruandlus“.</span><span class="sxs-lookup"><span data-stu-id="3f470-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="3f470-129">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="3f470-129">Create a new format configuration</span></span>
1. <span data-ttu-id="3f470-130">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="3f470-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="3f470-131">Valige puult suvand **Maksemudel**.</span><span class="sxs-lookup"><span data-stu-id="3f470-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="3f470-132">Rippdialoogi avamiseks valige käsk **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="3f470-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="3f470-133">Väljas **Uus** sisestage `Format based on data model PaymentModel`.</span><span class="sxs-lookup"><span data-stu-id="3f470-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="3f470-134">Looge vorming, mis põhineb andmemudelil PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="3f470-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="3f470-135">Kirjutage välja **Nimi** järgmist: `Sample worksheet report`.</span><span class="sxs-lookup"><span data-stu-id="3f470-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="3f470-136">Töölehe aruande näide</span><span class="sxs-lookup"><span data-stu-id="3f470-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="3f470-137">Kirjutage välja **Kirjeldus** järgmist: `Sample worksheet report for vendors’ payments`.</span><span class="sxs-lookup"><span data-stu-id="3f470-137">In the **Description** field, type `Sample worksheet report for vendors’ payments`.</span></span> <span data-ttu-id="3f470-138">Töölehe aruande näide hankijate maksete jaoks.</span><span class="sxs-lookup"><span data-stu-id="3f470-138">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="3f470-139">Sisestage või valige väärtus väljal **Andmemudeli definitsioon**.</span><span class="sxs-lookup"><span data-stu-id="3f470-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="3f470-140">Valige määratlus **CustomerCreditTransferInitiation**.</span><span class="sxs-lookup"><span data-stu-id="3f470-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="3f470-141">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="3f470-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="3f470-142">Uue dokumendi koostamine töölehe vormingus OPENXML</span><span class="sxs-lookup"><span data-stu-id="3f470-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="3f470-143">Valige puult suvand **Maksemudel\Töölehe näidisaruanne**.</span><span class="sxs-lookup"><span data-stu-id="3f470-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="3f470-144">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="3f470-144">Select **Designer**.</span></span>
3. <span data-ttu-id="3f470-145">Toimingupaanil valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="3f470-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="3f470-146">Valige **Excelist importimine**.</span><span class="sxs-lookup"><span data-stu-id="3f470-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="3f470-147">Valige suvand **Manused**.</span><span class="sxs-lookup"><span data-stu-id="3f470-147">Select **Attachments**.</span></span> <span data-ttu-id="3f470-148">Manustage olemasolev Exceli dokument mallina.</span><span class="sxs-lookup"><span data-stu-id="3f470-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="3f470-149">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3f470-149">Select **New**.</span></span>
7. <span data-ttu-id="3f470-150">Valige **Fail**.</span><span class="sxs-lookup"><span data-stu-id="3f470-150">Select **File**.</span></span> <span data-ttu-id="3f470-151">Osutage olemasolevale Exceli failile.</span><span class="sxs-lookup"><span data-stu-id="3f470-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="3f470-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3f470-152">Close the page.</span></span>
9. <span data-ttu-id="3f470-153">Väljas **Mall** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="3f470-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="3f470-154">Valige manustatud Exceli fail, mida kasutada mallina.</span><span class="sxs-lookup"><span data-stu-id="3f470-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="3f470-155">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f470-155">Select **OK**.</span></span> <span data-ttu-id="3f470-156">Pange tähele, et ER-i vormingu komponendid on loodud kujundamisvormingus viitava MS Exceli dokumendi struktuuri alusel (nimega vahemikud).</span><span class="sxs-lookup"><span data-stu-id="3f470-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="3f470-157">Uue andmeallika loomine kogusummade arvutamises valuutakoodide järgi</span><span class="sxs-lookup"><span data-stu-id="3f470-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="3f470-158">Valige **Vastendamine** vahekaart.</span><span class="sxs-lookup"><span data-stu-id="3f470-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="3f470-159">Rippdialoogi avamiseks valige käsk **Lisage põhinõue**.</span><span class="sxs-lookup"><span data-stu-id="3f470-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="3f470-160">Valige puult suvand **Funktsioonid\Rühmitusalus**.</span><span class="sxs-lookup"><span data-stu-id="3f470-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="3f470-161">Kirjutage välja **Nimi** järgmist: `PaymentByCurrency`.</span><span class="sxs-lookup"><span data-stu-id="3f470-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="3f470-162">Valige **Rühma muutmisalus**.</span><span class="sxs-lookup"><span data-stu-id="3f470-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="3f470-163">Valige puult **mudel**, seejärel suvand **mudel\Maksed**.</span><span class="sxs-lookup"><span data-stu-id="3f470-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="3f470-164">Valige **Lisa väli kohta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="3f470-165">Valige **Mida rühmitada**.</span><span class="sxs-lookup"><span data-stu-id="3f470-165">Select **What to group**.</span></span>
9. <span data-ttu-id="3f470-166">Valige puult **mudel\Maksed**, seejärel suvand **mudel\Maksed\Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="3f470-167">Valige **Lisa väli kohta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="3f470-168">Valige **Rühmitatud väljad**.</span><span class="sxs-lookup"><span data-stu-id="3f470-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="3f470-169">Valige puult suvand **mudel\Maksed\Etteantud summa(InstructedAmount)**.</span><span class="sxs-lookup"><span data-stu-id="3f470-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="3f470-170">Valige **Lisage väli kohta**, seejärel valige **Koondamisväljad**.</span><span class="sxs-lookup"><span data-stu-id="3f470-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="3f470-171">Tehke väljas **Meetod** valik.</span><span class="sxs-lookup"><span data-stu-id="3f470-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="3f470-172">Valige funktsioon **SUMMA koondamine**.</span><span class="sxs-lookup"><span data-stu-id="3f470-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="3f470-173">Kirjutage välja **Nimi** järgmist: `TotalInstructuredAmount`.</span><span class="sxs-lookup"><span data-stu-id="3f470-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="3f470-174">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-174">Select **Save**.</span></span>
17. <span data-ttu-id="3f470-175">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3f470-175">Close the page.</span></span>
18. <span data-ttu-id="3f470-176">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f470-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="3f470-177">Vormingu komponentide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="3f470-177">Map format components to data sources</span></span>
1. <span data-ttu-id="3f470-178">Valige puul **mudel\Maksed\Algatav osapool(InitiatingParty)\Nimi** ja **Excel\Aruandepäis\Ettevõttenimi**.</span><span class="sxs-lookup"><span data-stu-id="3f470-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="3f470-179">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-179">Select **Bind**.</span></span>
3. <span data-ttu-id="3f470-180">Valige puul **mudel\Maksed\Võlausaldaja\Tuvastamine\Allika ID (SourceID)** ja **Excel\Makseread\Pakkujakontonimi**.</span><span class="sxs-lookup"><span data-stu-id="3f470-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="3f470-181">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-181">Select **Bind**.</span></span>
5. <span data-ttu-id="3f470-182">Valige puul **mudel\Maksed\Võlausaldaja\Nimi** ja **Excel\Makseread\Pakkujanimi**.</span><span class="sxs-lookup"><span data-stu-id="3f470-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="3f470-183">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-183">Select **Bind**.</span></span>
7. <span data-ttu-id="3f470-184">Valige puul **mudel\Maksed\Võlausaldaja agentuur(CreditorAgent)\Nimi** ja **Excel\Makseread\Pank**.</span><span class="sxs-lookup"><span data-stu-id="3f470-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="3f470-185">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-185">Select **Bind**.</span></span>
9. <span data-ttu-id="3f470-186">Valige puul **mudel\Maksed\Võlausaldaja agentuur(CreditorAgent)\Suunamisnumber(RoutingNumber)** ja **Excel\Makseread\Suunamisnumber**.</span><span class="sxs-lookup"><span data-stu-id="3f470-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="3f470-187">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-187">Select **Bind**.</span></span>
11. <span data-ttu-id="3f470-188">Valige puul **mudel\Maksed\Võlausaldaja konto(CreditorAccount)\Tuvastamine\Number** ja **Excel\Makseread\Kontonumber**.</span><span class="sxs-lookup"><span data-stu-id="3f470-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="3f470-189">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-189">Select **Bind**.</span></span>
13. <span data-ttu-id="3f470-190">Valige puul **mudel\Maksed\Etteantud summa(InstructedAmount)** ja **Excel\Makseread\Võlad**.</span><span class="sxs-lookup"><span data-stu-id="3f470-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="3f470-191">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-191">Select **Bind**.</span></span>
15. <span data-ttu-id="3f470-192">Valige puul **mudel\Maksed\Valuuta** ja **Excel\Makseread\Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="3f470-193">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-193">Select **Bind**.</span></span>
17. <span data-ttu-id="3f470-194">Valige puul **Maksevaluutajärgi\rühmitatud\Valuuta** ja **Excel\Kokkuvõtteread\Kokkuvõttevaluuta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="3f470-195">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-195">Select **Bind**.</span></span>
19. <span data-ttu-id="3f470-196">Valige puul **Maksevaluutajärgi\rühmitatud\Etteantudkogusumma** ja **Excel\Kokkuvõtteread\Kokkuvõttesumma**.</span><span class="sxs-lookup"><span data-stu-id="3f470-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="3f470-197">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-197">Select **Bind**.</span></span>
21. <span data-ttu-id="3f470-198">Valige puul **Maksevaluutajärgi** ja **Excel\Kokkuvõtteread**.</span><span class="sxs-lookup"><span data-stu-id="3f470-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="3f470-199">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-199">Select **Bind**.</span></span>
23. <span data-ttu-id="3f470-200">Valige puul **mudel\Maksed** ja **Excel\Makseread**.</span><span class="sxs-lookup"><span data-stu-id="3f470-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="3f470-201">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="3f470-201">Select **Bind**.</span></span>
25. <span data-ttu-id="3f470-202">Valige **Salvesta**, seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3f470-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="3f470-203">Loodud konfiguratsiooni kasutamine maksete töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="3f470-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="3f470-204">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="3f470-204">Select **Change status**.</span></span>
2. <span data-ttu-id="3f470-205">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-205">Select **Complete**.</span></span>
3. <span data-ttu-id="3f470-206">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f470-206">Select **OK**.</span></span>
4. <span data-ttu-id="3f470-207">Navigeerimispaanil avage **Moodulid > Makstaolevad arved > Maksete seadistamine > Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="3f470-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="3f470-208">Väljal **Makseviis** väärtusega **Elektrooniline** filtreerimiseks kasutage kiirfiltrit.</span><span class="sxs-lookup"><span data-stu-id="3f470-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="3f470-209">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3f470-209">Select **Edit**.</span></span>
7. <span data-ttu-id="3f470-210">Laiendage jaotis **Failivormingud**.</span><span class="sxs-lookup"><span data-stu-id="3f470-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="3f470-211">Valige väljas **Elektrooniline üldaruanne** valik **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3f470-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="3f470-212">Väljas **Ekspordi vormingu seadistus** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="3f470-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="3f470-213">Valige seadistus **Töölehe näidisaruanne**.</span><span class="sxs-lookup"><span data-stu-id="3f470-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="3f470-214">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-214">Select **Save**.</span></span>
11. <span data-ttu-id="3f470-215">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3f470-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="3f470-216">Loodud konfiguratsiooni kasutamine makse töölehtede töötlemise testimiseks</span><span class="sxs-lookup"><span data-stu-id="3f470-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="3f470-217">Navigeerimispaanil avage **Moodulid > Makstaolevad arved > Maksed > Maksepäevik**.</span><span class="sxs-lookup"><span data-stu-id="3f470-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="3f470-218">Uue maksepäeviku loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3f470-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="3f470-219">Kirjutage välja **Nimi** järgmist: **Pakkujamakse**.</span><span class="sxs-lookup"><span data-stu-id="3f470-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="3f470-220">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="3f470-220">Select **Lines**.</span></span>
5. <span data-ttu-id="3f470-221">Väljal **Konto** kirjutage väärtused `GB_SI_000001`.</span><span class="sxs-lookup"><span data-stu-id="3f470-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="3f470-222">Määra **Võlg** väärtuseks `1000`.</span><span class="sxs-lookup"><span data-stu-id="3f470-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="3f470-223">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3f470-223">Select **New**.</span></span>
8. <span data-ttu-id="3f470-224">Väljal **Konto** kirjutage väärtused `GB_SI_000005`.</span><span class="sxs-lookup"><span data-stu-id="3f470-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="3f470-225">Määra **Võlg** väärtuseks `2000`.</span><span class="sxs-lookup"><span data-stu-id="3f470-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="3f470-226">Kirjutage välja **Valuuta** järgmist: `EUR`.</span><span class="sxs-lookup"><span data-stu-id="3f470-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="3f470-227">Väljal **Nihke konto** kirjutage väärtused `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="3f470-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="3f470-228">Kirjutage välja **Makseviis** järgmist: `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="3f470-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="3f470-229">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3f470-229">Select **Save**.</span></span>
14. <span data-ttu-id="3f470-230">Valige **Loo maksed**.</span><span class="sxs-lookup"><span data-stu-id="3f470-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="3f470-231">Kirjutage välja **Makseviis** järgmist: `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="3f470-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="3f470-232">Kirjutage välja **Faili nimi** järgmist: `Payments`.</span><span class="sxs-lookup"><span data-stu-id="3f470-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="3f470-233">Kirjutage välja **Pangakonto** järgmist: `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="3f470-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="3f470-234">Valige **OK** ja seejärel taas **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f470-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="3f470-235">Vaadake loodud tööleht üle, sh makseridade üksikasjad kui ka selles makseteates kasutatud iga valuutakoodi summad.</span><span class="sxs-lookup"><span data-stu-id="3f470-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

