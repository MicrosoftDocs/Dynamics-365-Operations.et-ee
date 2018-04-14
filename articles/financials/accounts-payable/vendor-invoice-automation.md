---
title: Hankija arve automatiseerimine
description: "Selles teemas selgitatakse funktsioone, mis on saadaval hankija arvete täielikuks automatiseerimiseks, isegi manuseid sisaldavate arvete puhul."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7794448e928fbad76a9b4b67d296705e18908ed6
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="2b724-103">Hankija arve automatiseerimine</span><span class="sxs-lookup"><span data-stu-id="2b724-103">Vendor invoice automation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="2b724-104">Selles teemas selgitatakse funktsioone, mis on saadaval hankija arvete täielikuks automatiseerimiseks, isegi manuseid sisaldavate arvete puhul.</span><span class="sxs-lookup"><span data-stu-id="2b724-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="2b724-105">Organisatsioonid, kus soovitakse ostureskontro protsesse sujuvamaks muuta, käsitlevad arvete töötlemist sageli ühe peamise protsessivaldkonnana, mis peaks olema tõhusam.</span><span class="sxs-lookup"><span data-stu-id="2b724-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="2b724-106">Paljudel juhtudel annavad need organisatsioonid paberarvete töötlemise üle optilise märgituvastusega (OCR) tegelevatele teenusepakkujatele.</span><span class="sxs-lookup"><span data-stu-id="2b724-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="2b724-107">Siis saavad nad masinloetavad arve metaandmed koos iga arve skannitud kujutisega.</span><span class="sxs-lookup"><span data-stu-id="2b724-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="2b724-108">Automatiseerimisel abistamiseks koostatakse siis viimase etapi jaoks lahendus, mis võimaldab neid üksusi siis arveldussüsteemis kasutada.</span><span class="sxs-lookup"><span data-stu-id="2b724-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="2b724-109">Microsoft Dynamics 365 for Finance and Operations võimaldab nüüd selle viimase etapi automatiseerimist valmislahenduse abil, kasutades arve automatiseerimislahendust.</span><span class="sxs-lookup"><span data-stu-id="2b724-109">Microsoft Dynamics 365 for Finance and Operations now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="2b724-110">Lahenduse kontekst</span><span class="sxs-lookup"><span data-stu-id="2b724-110">Solution context</span></span>

<span data-ttu-id="2b724-111">Arve automatiseerimislahendus võimaldab kasutada standardliidest, mis suudab võtta arve päisest ja arve ridadelt ning ka arvega seotud manustest vastu arve metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="2b724-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="2b724-112">Väline süsteem, mis suudab genereerida selle liidesega ühilduvaid üksusi, suudab saata voo Finance and Operationsisse arvete ja manuste automaatseks töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b724-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="2b724-113">Järgmisel illustratsioonil on integratsiooni näidisstsenaarium, kus Contoso on sõlminud hankija arvete töötlemiseks partnerluse OCR-teenuse pakkujaga.</span><span class="sxs-lookup"><span data-stu-id="2b724-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="2b724-114">Contoso hankijad saadavad teenusepakkujale meili teel arveid.</span><span class="sxs-lookup"><span data-stu-id="2b724-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="2b724-115">OCR-i töötluse kaudu genereerib teenusepakkuja arve metaandmed (päise ja/või read) ja arve skannitud kujutise.</span><span class="sxs-lookup"><span data-stu-id="2b724-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="2b724-116">Seejärel teisendab integratsioonikiht need üksused, et Finance and Operations saaks neid tarbida.</span><span class="sxs-lookup"><span data-stu-id="2b724-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![Integreerimise näidisstsenaarium](media/vendor_invoice_automation_01.png)

<span data-ttu-id="2b724-118">Kui on vajalik arve integreerimine, on võimalikus mitu eelmise stsenaariumi variatsiooni.</span><span class="sxs-lookup"><span data-stu-id="2b724-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="2b724-119">Andmete migreerimine on teine kasutusviis, kus seda liidest saab kasutada Finance and Operationsis arvete ja manuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="2b724-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="2b724-120">Lahenduse komponendid</span><span class="sxs-lookup"><span data-stu-id="2b724-120">Solution components</span></span>

<span data-ttu-id="2b724-121">Lahenduse jalajälg sisaldab järgmisi komponente.</span><span class="sxs-lookup"><span data-stu-id="2b724-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="2b724-122">Arve päise, arve ridade ja arve manuste andmeüksused</span><span class="sxs-lookup"><span data-stu-id="2b724-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="2b724-123">Erandite töötlemine arvete puhul</span><span class="sxs-lookup"><span data-stu-id="2b724-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="2b724-124">Kõrvuti manusevaatur arvetel</span><span class="sxs-lookup"><span data-stu-id="2b724-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="2b724-125">Ülejäänud teema kirjeldab üksikasjalikult neid lahenduse komponente.</span><span class="sxs-lookup"><span data-stu-id="2b724-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="2b724-126">Andmeüksused</span><span class="sxs-lookup"><span data-stu-id="2b724-126">Data entities</span></span>

<span data-ttu-id="2b724-127">Andmepakett on tööühik, mis tuleb saata Finance and Operationsisse arvete päiste, ridade ja manuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="2b724-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="2b724-128">Andmepaketi koosteüksuste jaoks kasutatakse järgmisi andmeüksusi.</span><span class="sxs-lookup"><span data-stu-id="2b724-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="2b724-129">Hankija arve päis</span><span class="sxs-lookup"><span data-stu-id="2b724-129">Vendor invoice header</span></span>
+ <span data-ttu-id="2b724-130">Hankija arve rida</span><span class="sxs-lookup"><span data-stu-id="2b724-130">Vendor invoice line</span></span>
+ <span data-ttu-id="2b724-131">Hankijaarve dokumendimanus</span><span class="sxs-lookup"><span data-stu-id="2b724-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="2b724-132">Hankija arve dokumendi manus on uus andmeüksus, mis selle funktsiooni osana kasutusele võetakse.</span><span class="sxs-lookup"><span data-stu-id="2b724-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="2b724-133">Hankija arve päiseüksust on muudetud nii, et see toetab manuseid.</span><span class="sxs-lookup"><span data-stu-id="2b724-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="2b724-134">Selle funktsiooni jaoks pole hankija arve reaüksust muudetud.</span><span class="sxs-lookup"><span data-stu-id="2b724-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="2b724-135">See teema ei anna andmepaketi üksikasjalikku definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="2b724-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="2b724-136">Samuti ei selgita see, kuidas andmepakette luua.</span><span class="sxs-lookup"><span data-stu-id="2b724-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="2b724-137">Selle teabe leiate jaotisest [Andmeüksuste ja pakettide raamistik](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="2b724-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="2b724-138">Arveid ja manuseid sisaldavate testandmete kiireks genereerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2b724-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="2b724-139">Logige oma Finance and Operationsi eksemplari sisse.</span><span class="sxs-lookup"><span data-stu-id="2b724-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="2b724-140">Avage **Ostureskontro** > **Arved** > **Ootel hankija arved**.</span><span class="sxs-lookup"><span data-stu-id="2b724-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="2b724-141">Looge arved, millel on read ja manused.</span><span class="sxs-lookup"><span data-stu-id="2b724-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b724-142">Manused peavad olema päise manused.</span><span class="sxs-lookup"><span data-stu-id="2b724-142">The attachments must be header attachments.</span></span> <span data-ttu-id="2b724-143">Praegu ei toeta hankija arvedokumendi manuse üksus reamanuseid.</span><span class="sxs-lookup"><span data-stu-id="2b724-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="2b724-144">Avage tööruum **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="2b724-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="2b724-145">Looge eksporditöö, mis sisaldab hankija arve päist, hankija arve rida ja hankija arvedokumendi manuse üksusi.</span><span class="sxs-lookup"><span data-stu-id="2b724-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="2b724-146">Eksportige andmed.</span><span class="sxs-lookup"><span data-stu-id="2b724-146">Export the data.</span></span>
1. <span data-ttu-id="2b724-147">Laadige eksporditud andmed paketina alla.</span><span class="sxs-lookup"><span data-stu-id="2b724-147">Download the exported data as a package.</span></span> <span data-ttu-id="2b724-148">Nüüd saate kasutada paketti andmete importimiseks sihteksemplaridesse testimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="2b724-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="2b724-149">Arve juriidilise isiku määramine</span><span class="sxs-lookup"><span data-stu-id="2b724-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="2b724-150">Andmepakettide kaudu imporditud arved saab seostada juriidilise isikuga, mille juurde need kuuluvad, kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="2b724-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="2b724-151">Arvet töötlev imporditöö impordib selle samasse ettevõttesse, milles töö tööruumis **Andmehaldus** plaaniti.</span><span class="sxs-lookup"><span data-stu-id="2b724-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="2b724-152">Teisisõnu: töö ettevõte määrab ettevõtte, millele arve kuulub.</span><span class="sxs-lookup"><span data-stu-id="2b724-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="2b724-153">Kui arveid sisaldav andmepakett saadetakse Finance and Operationsisse, saab kutsuja (st integreerimislahendus, mis töötab väljaspool Finance and Operationsit) nimetada selgelt HTTP taotluses ettevõtte ID.</span><span class="sxs-lookup"><span data-stu-id="2b724-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="2b724-154">Sel juhul alistatakse ettevõtte kontekst, milles töötlemistöö Finance and Operationsis töötab, ja arved imporditakse HTTP taotluse kaudu edastatud ettevõttesse.</span><span class="sxs-lookup"><span data-stu-id="2b724-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="2b724-155">See käitumine on standardne andmehalduse käitumine.</span><span class="sxs-lookup"><span data-stu-id="2b724-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="2b724-156">Seda on selgitatud siin, arvete kontekstis, üksnes terviklikkuse huvides.</span><span class="sxs-lookup"><span data-stu-id="2b724-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="2b724-157">Erandi töötlemine</span><span class="sxs-lookup"><span data-stu-id="2b724-157">Exception processing</span></span>

<span data-ttu-id="2b724-158">Stsenaariumide korral, kus hankija arved tulevad Finance and Operationsisse integreerimise kaudu, peab olema Ostureskontro töörühma liikmel lihtne võimalus erandite või nurjunud arvete töötlemiseks ja ootel arvete loomiseks nurjunud arvetest.</span><span class="sxs-lookup"><span data-stu-id="2b724-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="2b724-159">See hankija arvete erandite töötlemine on nüüd Finance and Operationsi osa.</span><span class="sxs-lookup"><span data-stu-id="2b724-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="2b724-160">Erandite loendileht</span><span class="sxs-lookup"><span data-stu-id="2b724-160">Exceptions list page</span></span>

<span data-ttu-id="2b724-161">Uus arve erandite loendileht on saadaval jaotises **Ostureskontro** > **Arved** > **Impordi nurjumised** > **Hankija arved, mille importimine nurjus**.</span><span class="sxs-lookup"><span data-stu-id="2b724-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="2b724-162">Sellel lehel kuvatakse kõik hankija arve päisekirjed hankija arve päise andmeüksuse vahetabelist.</span><span class="sxs-lookup"><span data-stu-id="2b724-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="2b724-163">Pange tähele, et saate vaadata samu kirjeid tööruumis **Andmehaldus**, kus saate teha ka samad toimingud, mis on antud erandi käsitlemise funktsioonis.</span><span class="sxs-lookup"><span data-stu-id="2b724-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="2b724-164">Kuid kasutajaliides, mida erandi käsitlemise funktsioon pakub, on optimeeritud funktsionaalse kasutaja jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b724-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Erandite loendileht](media/vendor_invoice_automation_02.png)

<span data-ttu-id="2b724-166">See loendileht sisaldab järgmisi välju, mis tulevad sisse voo kaudu.</span><span class="sxs-lookup"><span data-stu-id="2b724-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="2b724-167">**Ettevõte** – ettevõte, millele arve kuulub</span><span class="sxs-lookup"><span data-stu-id="2b724-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="2b724-168">**Tõrketeade** – haldusraamistiku väljastatav tõrketeade, mis selgitab, miks arvet ei saanud luua</span><span class="sxs-lookup"><span data-stu-id="2b724-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="2b724-169">**Number** – arve number</span><span class="sxs-lookup"><span data-stu-id="2b724-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="2b724-170">**Arve konto**</span><span class="sxs-lookup"><span data-stu-id="2b724-170">**Invoice account**</span></span>
+ <span data-ttu-id="2b724-171">**Nimi** – hankija nimi</span><span class="sxs-lookup"><span data-stu-id="2b724-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="2b724-172">**Hankija konto**</span><span class="sxs-lookup"><span data-stu-id="2b724-172">**Vendor account**</span></span>
+ <span data-ttu-id="2b724-173">**Ostutellimus** – arve ostutellimuse number</span><span class="sxs-lookup"><span data-stu-id="2b724-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="2b724-174">**Sisestuskuupäev**</span><span class="sxs-lookup"><span data-stu-id="2b724-174">**Posting date**</span></span>
+ <span data-ttu-id="2b724-175">**Arve kuupäev**</span><span class="sxs-lookup"><span data-stu-id="2b724-175">**Invoice date**</span></span>
+ <span data-ttu-id="2b724-176">**Arve kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="2b724-176">**Invoice description**</span></span>
+ <span data-ttu-id="2b724-177">**Valuuta**</span><span class="sxs-lookup"><span data-stu-id="2b724-177">**Currency**</span></span>
+ <span data-ttu-id="2b724-178">**Logi**</span><span class="sxs-lookup"><span data-stu-id="2b724-178">**Log**</span></span>
+ <span data-ttu-id="2b724-179">**Rea viide** – välisest süsteemist pärinev identifikaator</span><span class="sxs-lookup"><span data-stu-id="2b724-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b724-180">Rea viide ei ole arve ID.</span><span class="sxs-lookup"><span data-stu-id="2b724-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="2b724-181">Loendilehel on ka eelvaatepaan, mida saab kasutada järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2b724-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="2b724-182">Kogu tõrketeate kuvamiseks, et tabelis poleks vaja veergu **Tõrketeade** laiendada.</span><span class="sxs-lookup"><span data-stu-id="2b724-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="2b724-183">Kogu arve manuste loendi kuvamiseks, kui arvega tuli kaasa manuseid.</span><span class="sxs-lookup"><span data-stu-id="2b724-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="2b724-184">Loendileht toetab järgmisi tegevusi.</span><span class="sxs-lookup"><span data-stu-id="2b724-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="2b724-185">**Redigeerimine** – avage erandi kirje redigeerimisrežiimis, et saaksite probleemid kõrvaldada.</span><span class="sxs-lookup"><span data-stu-id="2b724-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="2b724-186">**Valikud** – juurdepääs loendilehtedel olevatele standardvalikutele.</span><span class="sxs-lookup"><span data-stu-id="2b724-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="2b724-187">Saate kasutada valikut **Lisa tööruumi** erandite loendilehe kinnitamiseks tööruumi loendi või paanina.</span><span class="sxs-lookup"><span data-stu-id="2b724-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="2b724-188">Erandi üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="2b724-188">Exception details page</span></span>

<span data-ttu-id="2b724-189">Kui käivitate redigeerimisrežiimi, kuvatakse probleemidega arve erandi üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="2b724-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="2b724-190">Kui on manuseid, kuvatakse arve ja vaikemanus erandi üksikasjade lehel kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="2b724-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Erandi üksikasjade leht](media/vendor_invoice_automation_03.png)

<span data-ttu-id="2b724-192">Eelneval illustratsioonil ei olnud sisse tulnud hankija arve päises ridu.</span><span class="sxs-lookup"><span data-stu-id="2b724-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="2b724-193">Seetõttu on ridade osa tühi.</span><span class="sxs-lookup"><span data-stu-id="2b724-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="2b724-194">Erandi üksikasjade leht toetab järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="2b724-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="2b724-195">**Ootel arve loomine** – kui olete erandi töötlemise käigus arvel olevad probleemid kõrvaldanud, võite klõpsata seda nuppu ootel arve loomiseks.</span><span class="sxs-lookup"><span data-stu-id="2b724-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="2b724-196">Ootel arvete loomine toimub taustal (asünkroonse toiminguna).</span><span class="sxs-lookup"><span data-stu-id="2b724-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="2b724-197">Jagatud teenus võrreldes organisatsioonipõhise erandi töötlemisega</span><span class="sxs-lookup"><span data-stu-id="2b724-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="2b724-198">Erandite loendileht toetab standardseid turbekonstruktsioone, mida **andmehalduse** tööruum vahetabeli kirjete töötlemiseks toetab.</span><span class="sxs-lookup"><span data-stu-id="2b724-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="2b724-199">Arve imporditööd saab kaitsta järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2b724-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="2b724-200">Kasutaja rolliga</span><span class="sxs-lookup"><span data-stu-id="2b724-200">By user role</span></span>
+ <span data-ttu-id="2b724-201">Kasutaja järgi</span><span class="sxs-lookup"><span data-stu-id="2b724-201">By user</span></span>
+ <span data-ttu-id="2b724-202">Juriidilise isiku järgi</span><span class="sxs-lookup"><span data-stu-id="2b724-202">By legal entity</span></span>

![Imporditöö, mida kaitstakse kasutaja rolli ja juriidilise isiku järgi](media/vendor_invoice_automation_04.png)

<span data-ttu-id="2b724-204">Kui arve imporditöö jaoks on konfigureeritud turvalisus, arvestab erandite loendileht neid sätteid.</span><span class="sxs-lookup"><span data-stu-id="2b724-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="2b724-205">Kasutajad näevad ainult neid arve erandi kirjeid, mida see seadistus neil näha lubab.</span><span class="sxs-lookup"><span data-stu-id="2b724-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="2b724-206">Näiteks Contoso on otsustanud töödelda arve erandeid juriidilise isiku järgi.</span><span class="sxs-lookup"><span data-stu-id="2b724-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="2b724-207">Seetõttu konfigureeritakse turvalisus arve imporditöö puhul sellisel viisil, et kasutaja juriidilises isikus A näeb ainult arve erandeid juriidilises isikus A, samas kui kasutaja juriidilises isikus B näeb ainult arve erandeid juriidilises isikus B. Selline seadistus võimaldab arve erandite haldamise kohustusi jagada.</span><span class="sxs-lookup"><span data-stu-id="2b724-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="2b724-208">Contoso võib otsustada ka turvalisust mitte kehtestada, et samad kasutajad saaksid töödelda arve erandeid kõigi juriidiliste isikute puhul.</span><span class="sxs-lookup"><span data-stu-id="2b724-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="2b724-209">See seadistus lubab jagatud teenuste stsenaariumi arve erandite haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="2b724-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="2b724-210">Kõrvuti manusevaatur</span><span class="sxs-lookup"><span data-stu-id="2b724-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="2b724-211">Hankija arvete manuste hõlpsaks kuvamiseks on järgmistel arveldusprotsessis kasutatavatel lehtedel nüüd manusevaatur.</span><span class="sxs-lookup"><span data-stu-id="2b724-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="2b724-212">**Erandite käsitlemine**</span><span class="sxs-lookup"><span data-stu-id="2b724-212">**Exception handling**</span></span>
+ <span data-ttu-id="2b724-213">Leht **Ootel hankija arved** (saadaval ka arve ülevaatusprotsessis)</span><span class="sxs-lookup"><span data-stu-id="2b724-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="2b724-214">Päringuleht **Arve tööleht** (sisestatud arvete jaoks)</span><span class="sxs-lookup"><span data-stu-id="2b724-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="2b724-215">Siin on põhifunktsioonid, mida manusevaatur pakub.</span><span class="sxs-lookup"><span data-stu-id="2b724-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="2b724-216">Kõigi dokumendihalduri toetatavate manusetüüpide kuvamine (failid, kujutised, URL-id ja märkused).</span><span class="sxs-lookup"><span data-stu-id="2b724-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="2b724-217">Mitmeleheliste TIFF-failide kuvamine.</span><span class="sxs-lookup"><span data-stu-id="2b724-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="2b724-218">Järgmiste toimingute tegemine pildifailidega.</span><span class="sxs-lookup"><span data-stu-id="2b724-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="2b724-219">Pildi osade esiletõstmine.</span><span class="sxs-lookup"><span data-stu-id="2b724-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="2b724-220">Pildi osade blokeerimine.</span><span class="sxs-lookup"><span data-stu-id="2b724-220">Block parts of the image.</span></span>
  + <span data-ttu-id="2b724-221">Märkuste lisamine pildile.</span><span class="sxs-lookup"><span data-stu-id="2b724-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="2b724-222">Pildi suurendamine ja vähendamine.</span><span class="sxs-lookup"><span data-stu-id="2b724-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="2b724-223">Pildi panoraamimine.</span><span class="sxs-lookup"><span data-stu-id="2b724-223">Pan the image.</span></span>
  + <span data-ttu-id="2b724-224">Tegevuste tagasivõtmine ja uuesti tegemine.</span><span class="sxs-lookup"><span data-stu-id="2b724-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="2b724-225">Pildi sobitamine suurusega.</span><span class="sxs-lookup"><span data-stu-id="2b724-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="2b724-226">Need tegevused on saadaval ainult pildifailide puhul (JPEG, TIFF, PNG jne).</span><span class="sxs-lookup"><span data-stu-id="2b724-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="2b724-227">Kõik muudatused, mida nende tegevustega pildil teete, salvestatakse pildifaili.</span><span class="sxs-lookup"><span data-stu-id="2b724-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="2b724-228">Praegu ei sisalda manusevaatur versioonide kasutamist ega auditeerimisvõimalusi.</span><span class="sxs-lookup"><span data-stu-id="2b724-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="2b724-229">Vaikemanus</span><span class="sxs-lookup"><span data-stu-id="2b724-229">Default attachment</span></span>

<span data-ttu-id="2b724-230">Kui hankija arvel on mitu manust, saate määrata ühe dokumendi lehel **Manused** vaikemanuseks.</span><span class="sxs-lookup"><span data-stu-id="2b724-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="2b724-231">Valik **On vaikemanus** on uus valik, mis lisati selle funktsiooni osana.</span><span class="sxs-lookup"><span data-stu-id="2b724-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="2b724-232">See valik on näha ka hankija arvedokumendi manuse andmeüksuses.</span><span class="sxs-lookup"><span data-stu-id="2b724-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="2b724-233">Seetõttu saab vaikemanuse määrata integreerimiste kaudu.</span><span class="sxs-lookup"><span data-stu-id="2b724-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="2b724-234">Vaikemanuseks saab määrata ainult ühe dokumendi.</span><span class="sxs-lookup"><span data-stu-id="2b724-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="2b724-235">Pärast dokumendi määramist vaikemanuseks kuvatakse see arve avamisel automaatselt manusevaaturis.</span><span class="sxs-lookup"><span data-stu-id="2b724-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="2b724-236">Kui te ühtegi dokumenti vaikemanuseks ei määra, ei näita vaatur arve avamisel automaatselt ühtegi manust.</span><span class="sxs-lookup"><span data-stu-id="2b724-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="2b724-237">Kuva/peida arve manused</span><span class="sxs-lookup"><span data-stu-id="2b724-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="2b724-238">Uus nupp, mis on saadaval päringulehtedel **Erandi töötlemine**, **Ootel arve** ja **Arve tööleht**, võimaldab manusevaaturit kuvada või peita.</span><span class="sxs-lookup"><span data-stu-id="2b724-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="2b724-239">Turvalisus</span><span class="sxs-lookup"><span data-stu-id="2b724-239">Security</span></span>

<span data-ttu-id="2b724-240">Rollipõhise turvalisuse kaudu juhitakse järgmisi tegevusi manusevaaturis.</span><span class="sxs-lookup"><span data-stu-id="2b724-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="2b724-241">Esiletõstmine</span><span class="sxs-lookup"><span data-stu-id="2b724-241">Highlighting</span></span>
+ <span data-ttu-id="2b724-242">Blokeeri</span><span class="sxs-lookup"><span data-stu-id="2b724-242">Block</span></span>
+ <span data-ttu-id="2b724-243">Kommenteerimine</span><span class="sxs-lookup"><span data-stu-id="2b724-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="2b724-244">Hankija ootelolevate arvete leht</span><span class="sxs-lookup"><span data-stu-id="2b724-244">Pending vendor invoices page</span></span>

<span data-ttu-id="2b724-245">Järgmised õigused annavad manusevaaturile kirjutuskaitstud juurdepääsu või lugemise/kirjutamise juurdepääsu esiletõstmise, blokeerimise ja kommenteerimise toimingute jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b724-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="2b724-246">**Hankija arve pildi haldamine** – see privileeg annab lugemis-/kirjutamisõiguse.</span><span class="sxs-lookup"><span data-stu-id="2b724-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="2b724-247">**Hankija arve pildi kuvamine** – see privileeg annab kirjutuskaitstud juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="2b724-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="2b724-248">Järgmised kohustused annavad manusevaaturile kirjutuskaitstud juurdepääsu või lugemise/kirjutamise juurdepääsu järgmiste tegevuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b724-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="2b724-249">**Hankija arvete haldamine** – sellele kohustusele on määratud hankija arvete pildi haldamise privileeg.</span><span class="sxs-lookup"><span data-stu-id="2b724-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="2b724-250">**Hankija arve oleku kohta päringu esitamine** – sellele kohustusele on määratud hankija arve pildi vaatamise privileeg.</span><span class="sxs-lookup"><span data-stu-id="2b724-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="2b724-251">Järgmised rollid annavad manusevaaturile kirjutuskaitstud juurdepääsu või lugemise/kirjutamise juurdepääsu järgmiste tegevuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b724-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="2b724-252">**Ostureskontro ametnik** ja **Ostureskontro juht** – nendele rollidele määratakse kohustus Hankija arvete haldamine.</span><span class="sxs-lookup"><span data-stu-id="2b724-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="2b724-253">**Ostureskontro ametnik**, **Ostureskontro juht**, **Ostureskontro tsentraliseeritud maksuametnik** ja **Ostureskontro maksuametnik** – nendele rollidele määratakse kohustus Hankija arve oleku kohta päringu esitamine.</span><span class="sxs-lookup"><span data-stu-id="2b724-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="2b724-254">Arve erandi üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="2b724-254">Invoice exception details page</span></span>

<span data-ttu-id="2b724-255">Järgmised õigused annavad manusevaaturile kirjutuskaitstud juurdepääsu või lugemise/kirjutamise juurdepääsu esiletõstmise, blokeerimise ja kommenteerimise toimingute jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b724-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="2b724-256">Valmis kujul annavad selles jaotises nimetatud rollid arve piltidele manusevaaturis kirjutuskaitstud juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="2b724-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="2b724-257">Kui rollil peaks olema piltide puhul ka kirjutamisõigusega juurdepääs, saate anda sellele rollile kirjutamisõiguse, kasutades siin kirjeldatud privileegi ja kohustust.</span><span class="sxs-lookup"><span data-stu-id="2b724-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="2b724-258">**Hankija arve päiseüksuse pildi haldamine** – see privileeg annab manuses olevate arve piltide lugemise/kirjutamise õiguse.</span><span class="sxs-lookup"><span data-stu-id="2b724-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="2b724-259">**Hankija arve päiseüksuse pildi kuvamine** – see privileeg annab õiguse manuses oleva arve pildi kirjutuskaitsega avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2b724-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="2b724-260">Järgmised kohustused annavad manusevaaturile kirjutuskaitstud juurdepääsu järgmiste tegevuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b724-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="2b724-261">**Hankija arvete haldamine** – sellele kohustusele on määratud hankija arve päiseüksuse pildi haldamise privileeg.</span><span class="sxs-lookup"><span data-stu-id="2b724-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="2b724-262">Järgmised rollid annavad manusevaaturile kirjutuskaitstud juurdepääsu järgmiste tegevuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b724-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="2b724-263">**Ostureskontro ametnik** ja **Ostureskontro juht** – nendele rollidele määratakse kohustus Hankija arvete haldamine.</span><span class="sxs-lookup"><span data-stu-id="2b724-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="2b724-264">Vaikimisi, kui kasutaja roll annab mõnel lehel redigeerimisõigused, on kasutajal redigeerimisõigused ka manusevaaturis esiletõstmise, blokeerimise ja kommenteerimise toiminguteks.</span><span class="sxs-lookup"><span data-stu-id="2b724-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="2b724-265">Kuid kui on stsenaariume, mille puhul konkreetsel rollil peaksid olema redigeerimisõigused lehel, kuid mitte manusevaaturis, saab sel puhul kasutada sobivaid privileege eespool antud loendist.</span><span class="sxs-lookup"><span data-stu-id="2b724-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>

