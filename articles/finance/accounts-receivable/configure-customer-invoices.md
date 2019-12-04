---
title: Kliendiarve loomine
description: '**Müügitellimuse kliendiarve** on arve, mis on seotud müügiga, ja mille organisatsioon kliendile annab.'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f5b9866fc7afba205b84b372c6a204ec4c8f64d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772716"
---
# <a name="create-a-customer-invoice"></a><span data-ttu-id="90d97-103">Kliendiarve loomine</span><span class="sxs-lookup"><span data-stu-id="90d97-103">Create a customer invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90d97-104">**Müügitellimuse kliendiarve** on arve, mis on seotud müügiga, ja mille organisatsioon kliendile annab.</span><span class="sxs-lookup"><span data-stu-id="90d97-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="90d97-105">Sellist tüüpi müügiarve luuakse müügitellimuse põhjal, mis sisaldab tellimuse ridu ja kaubakoode.</span><span class="sxs-lookup"><span data-stu-id="90d97-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="90d97-106">Kauba koodid täpsustatakse ja sisestatakse pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="90d97-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="90d97-107">Alammooduli töölehe kirjed pole müügitellimuse kliendiarve puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="90d97-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="90d97-108">Lisateabe saamiseks vt [Müügitellimuse arvete loomine](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="90d97-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="90d97-109">**Vabas vormis arve** pole müügitellimusega seotud.</span><span class="sxs-lookup"><span data-stu-id="90d97-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="90d97-110">See sisaldab tellimuse ridu, mille hulka kuuluvad pearaamatukontod, vaba tekstina sisestatud kirjeldused ja müügihind, mille sisestate.</span><span class="sxs-lookup"><span data-stu-id="90d97-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="90d97-111">Seda tüüpi arvele ei saa kaubakoodi sisestada.</span><span class="sxs-lookup"><span data-stu-id="90d97-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="90d97-112">Peate sisestama vastava käibemaksuteabe.</span><span class="sxs-lookup"><span data-stu-id="90d97-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="90d97-113">Müügi põhikonto on näidatud igal arve real, mille saate jaotada mitmele pearaamatukontole, klõpsates valikut **Summade jaotamine** lehel **Vabas vormis arve**.</span><span class="sxs-lookup"><span data-stu-id="90d97-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="90d97-114">Lisaks sisestatakse kliendi saldo vabas vormis arve puhul kasutatavatest sisestusreeglitest koondkontole.</span><span class="sxs-lookup"><span data-stu-id="90d97-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="90d97-115">Lisateavet vt </span><span class="sxs-lookup"><span data-stu-id="90d97-115">For more information see:</span></span>

[<span data-ttu-id="90d97-116">Vabateksti arvete loomine</span><span class="sxs-lookup"><span data-stu-id="90d97-116">Create free text invoices</span></span>](../accounts-receivable/create-free-text-invoice-new.md)

[<span data-ttu-id="90d97-117">Vabas vormis arve malli loomine</span><span class="sxs-lookup"><span data-stu-id="90d97-117">Create a free text invoice template</span></span>](../accounts-receivable/create-free-text-invoice-template-new.md)

[<span data-ttu-id="90d97-118">Vabas vormis arve malli määramine kliendile</span><span class="sxs-lookup"><span data-stu-id="90d97-118">Assign free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="90d97-119">Korduvate vabas vormis arvete genereerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="90d97-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="90d97-120">**Esialgne arve** on arve, mis on vormistatud hinnanguliste arvesummadega enne arve sisestamist.</span><span class="sxs-lookup"><span data-stu-id="90d97-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="90d97-121">Saate printida esialgse arve nii müügitellimuse kliendiarve kui ka vabas vormis arve kohta.</span><span class="sxs-lookup"><span data-stu-id="90d97-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="90d97-122">Eraldi müügitellimustel põhinevate kliendiarvete sisestamine ja printimine</span><span class="sxs-lookup"><span data-stu-id="90d97-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="90d97-123">Selle protsessi abil saate koostada müügitellimusel põhineva arve.</span><span class="sxs-lookup"><span data-stu-id="90d97-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="90d97-124">Seda võib teha, kui otsustate arve kliendile esitada enne kaupade või teenuste tarnimist.</span><span class="sxs-lookup"><span data-stu-id="90d97-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="90d97-125">Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** arveldatud kogustega valitud müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="90d97-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="90d97-126">Kui kõigi müügitellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse müügitellimuse olekuks **Arveldatud**.</span><span class="sxs-lookup"><span data-stu-id="90d97-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="90d97-127">Kui kogus **Arve jääk** ei ole 0 (null), siis müügitellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid.</span><span class="sxs-lookup"><span data-stu-id="90d97-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="90d97-128">Müügitellimuste olekut saab vaadata loendilehel **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="90d97-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="90d97-129">Lehel **Avatud kliendiarved** saate vaadata sisestatud arveid.</span><span class="sxs-lookup"><span data-stu-id="90d97-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="90d97-130">Saatelehtedel ja kuupäevadel põhinevate üksikute kliendiarvete sisestamine ja printimine</span><span class="sxs-lookup"><span data-stu-id="90d97-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="90d97-131">Kasutage seda protsessi, kui müügitellimuse kohta on sisestatud vähemalt üks saateleht.</span><span class="sxs-lookup"><span data-stu-id="90d97-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="90d97-132">Kliendiarve aluseks on need saatelehed ja arve näitab saatelehtedelt pärit koguseid.</span><span class="sxs-lookup"><span data-stu-id="90d97-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="90d97-133">Finantsteave arve jaoks põhineb teabel, mis sisestatakse, kui sisestate arve.</span><span class="sxs-lookup"><span data-stu-id="90d97-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="90d97-134">Saate luua kliendiarve, mis põhineb saatelehe tähtajaliselt välja saadetud reakaupadel, isegi kui kõik konkreetse müügitellimuse kaubad ei ole veel välja saadetud.</span><span class="sxs-lookup"><span data-stu-id="90d97-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="90d97-135">Seda saate teha nt siis, kui teie juriidiline isik väljastab igale kliendile ühe arve kuus, mis katab kõik selle kuu tarned.</span><span class="sxs-lookup"><span data-stu-id="90d97-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="90d97-136">Iga saateleht esindab müügitellimusel olevate kaupade osalist või täielikku väljasaatmist.</span><span class="sxs-lookup"><span data-stu-id="90d97-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="90d97-137">Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** tarnitud kogustega valitud saatelehtedelt.</span><span class="sxs-lookup"><span data-stu-id="90d97-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="90d97-138">Kui kõigi müügitellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse müügitellimuse olekuks **Arveldatud**.</span><span class="sxs-lookup"><span data-stu-id="90d97-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="90d97-139">Kui kogus **Arve jääk** ei ole 0 (null), siis müügitellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid.</span><span class="sxs-lookup"><span data-stu-id="90d97-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="90d97-140">Laokandeid uuendatakse koos arvenumbritega ja olek müügitellimuse väljal **Rea olek** muutub olekuks **Arveldatud**.</span><span class="sxs-lookup"><span data-stu-id="90d97-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="90d97-141">Müügitellimuste olekut saab vaadata loendilehel **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="90d97-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="90d97-142">Müügitellimuste või saatelehtede konsolideerimine sisestamiseks</span><span class="sxs-lookup"><span data-stu-id="90d97-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="90d97-143">Kasutage seda protsessi, kui vähemalt üks müügitellimus on arveldamiseks valmis ja soovite need ühele arvele konsolideerida.</span><span class="sxs-lookup"><span data-stu-id="90d97-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="90d97-144">Saate valida mitu arvet loendilehelt **Müügitellimus** ja kasutage siis nende konsolideerimiseks valikut **Loo arved**.</span><span class="sxs-lookup"><span data-stu-id="90d97-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="90d97-145">Lehel **Arve sisestamine** saate muuta valiku **Koondtellimus** sätet, et summeerida tellimuse numbri alusel (kui ühe müügitellimuse kohta on mitu saatelehte) või arvekonto alusel (kui ühe arvekonto kohta on mitu müügitellimust).</span><span class="sxs-lookup"><span data-stu-id="90d97-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="90d97-146">Kasutage nuppu **Korrasta** müügitellimuste konsolideerimiseks ühele arvele valiku **Koondtellimus** sätete põhjal.</span><span class="sxs-lookup"><span data-stu-id="90d97-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="90d97-147">Sisestamiskäitumist muutvad lisasätted</span><span class="sxs-lookup"><span data-stu-id="90d97-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="90d97-148">Järgmised väljad muudavad sisestamisprotsessi käitumist.</span><span class="sxs-lookup"><span data-stu-id="90d97-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90d97-149">Väli</span><span class="sxs-lookup"><span data-stu-id="90d97-149">Field</span></span></th>
<th><span data-ttu-id="90d97-150">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="90d97-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90d97-151">Kogus</span><span class="sxs-lookup"><span data-stu-id="90d97-151">Quantity</span></span></td>
<td><span data-ttu-id="90d97-152">Valige kogused, millel dokumendi sisestus põhineb.</span><span class="sxs-lookup"><span data-stu-id="90d97-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="90d97-153">Saadaolevad valikud erinevad olenevalt sisestatava dokumendi tüübist (nt saateleht või arve).</span><span class="sxs-lookup"><span data-stu-id="90d97-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="90d97-154"><strong>Tarni kohe</strong> – valige kõik kogused, mis on sisestatud väljale <strong>Tarni kohe</strong>.</span><span class="sxs-lookup"><span data-stu-id="90d97-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="90d97-155">Selle suvandi abil saate kinnitada või esitada osalise tellimuse.</span><span class="sxs-lookup"><span data-stu-id="90d97-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="90d97-156"><strong>Komplekteeritud</strong> – valitakse kõik komplekteeritud kogused.</span><span class="sxs-lookup"><span data-stu-id="90d97-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="90d97-157"><strong>Kõik</strong> – valitakse kõik müügitellimuse kogused, mida pole veel praeguse dokumenditüübiga värskendatud.</span><span class="sxs-lookup"><span data-stu-id="90d97-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="90d97-158"><strong>Saateleht</strong> – valitakse kõik saatelehe värskendatud kogused.</span><span class="sxs-lookup"><span data-stu-id="90d97-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="90d97-159"><strong>Komplekteeritud kogus ja ladustamata tooted</strong> – valitakse kõik komplekteeritud kogused ja kõik ladustamata tooted.</span><span class="sxs-lookup"><span data-stu-id="90d97-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90d97-160">Sisestamine</span><span class="sxs-lookup"><span data-stu-id="90d97-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="90d97-161">Selle suvandi valimisel paigutatakse müügitellimus töölehele.</span><span class="sxs-lookup"><span data-stu-id="90d97-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="90d97-162">Selle suvandi tühjendamisel prinditakse esialgne müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="90d97-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="90d97-163"><strong>Märkus</strong>. Kui tegite maksegraafiku leppe, siis esialgsel müügitellimusel maksegraafikut ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="90d97-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="90d97-164">Maksegraafikud kuvatakse vaid tegelikel müügitellimustel.</span><span class="sxs-lookup"><span data-stu-id="90d97-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90d97-165">Hiline valik</span><span class="sxs-lookup"><span data-stu-id="90d97-165">Late selection</span></span></td>
<td><span data-ttu-id="90d97-166">Valige see suvand, kui soovite valitud päringu hiljem rakendada.</span><span class="sxs-lookup"><span data-stu-id="90d97-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="90d97-167">Seda suvandit kasutatakse pakett-tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="90d97-167">This option is used for batch jobs.</span></span> <span data-ttu-id="90d97-168">Päring käivitatakse pakett-töö käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="90d97-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90d97-169">Vähenda kogust</span><span class="sxs-lookup"><span data-stu-id="90d97-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="90d97-170">Selle suvandi valimisel vähendatakse dokumendi sisestamisel automaatselt tarnitud kogust, et tarnitud kogus oleks võrdne saadaoleva varuga.</span><span class="sxs-lookup"><span data-stu-id="90d97-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90d97-171">Prindi</span><span class="sxs-lookup"><span data-stu-id="90d97-171">Print</span></span></td>
<td><span data-ttu-id="90d97-172">Saate valida, millal dokumendid prinditakse.</span><span class="sxs-lookup"><span data-stu-id="90d97-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="90d97-173"><strong>Praegune</strong> – saate printida dokumente pärast iga arve uuendamist.</span><span class="sxs-lookup"><span data-stu-id="90d97-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="90d97-174"><strong>Pärast</strong> – dokumendid prinditakse pärast kõikide arvete uuendamist.</span><span class="sxs-lookup"><span data-stu-id="90d97-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="90d97-175">
<strong>Märkus.</strong> Väli <strong>Prindi</strong> on saadaval vaid juhul, kui teete valiku <strong>Prindi arve</strong>, <strong>Prindi kinnitus</strong>, <strong>Prindi komplekteerimisleht</strong> või <strong>Prindi saateleht</strong>.</span><span class="sxs-lookup"><span data-stu-id="90d97-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="90d97-176">Nt peate lehel <strong>Vormi sortimine</strong> seadistama süsteemi teavet arvekonto alusel sortima.</span><span class="sxs-lookup"><span data-stu-id="90d97-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="90d97-177">Seejärel saate valida suvandi <strong>Pärast</strong>, et printida dokumendid arvekonto alusel sorditud partiina.</span><span class="sxs-lookup"><span data-stu-id="90d97-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="90d97-178">Vastasel juhul prinditakse dokumendid enne töötlemise lõpule viimist ja dokumente ei sordita lehel <strong>Vormi sortimine</strong> määratud järjestusse.</span><span class="sxs-lookup"><span data-stu-id="90d97-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90d97-179">Prindi arve</span><span class="sxs-lookup"><span data-stu-id="90d97-179">Print invoice</span></span></td>
<td><span data-ttu-id="90d97-180">Tehke see valik arve printimiseks.</span><span class="sxs-lookup"><span data-stu-id="90d97-180">Select this option to print the invoice.</span></span> <span data-ttu-id="90d97-181">Kui see valik on välja lülitatud, saate sisestada arve ilma seda printimata.</span><span class="sxs-lookup"><span data-stu-id="90d97-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90d97-182">Saada meilisõnum</span><span class="sxs-lookup"><span data-stu-id="90d97-182">Send e-mail</span></span></td>
<td><span data-ttu-id="90d97-183">Tehke see valik müügitellimuse arve saatmiseks kliendile meilimanusena pärast arve sisestamist.</span><span class="sxs-lookup"><span data-stu-id="90d97-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="90d97-184">Manused saadetakse PDF- ja XML-failidena.</span><span class="sxs-lookup"><span data-stu-id="90d97-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="90d97-185">See valik on saadaval ainult juhul, kui teete valiku <strong>Luba CFD (elektroonilised arved)</strong> lehel <strong>Elektroonilise arve parameetrid</strong>.</span><span class="sxs-lookup"><span data-stu-id="90d97-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="90d97-186"><strong>Märkus.</strong> (MEX) See juhtelement on saadaval ainult juriidilistele isikutele, kelle peamine aadress on Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="90d97-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90d97-187">Kasuta prindihalduse sihtkohta</span><span class="sxs-lookup"><span data-stu-id="90d97-187">Use print management destination</span></span></td>
<td><span data-ttu-id="90d97-188">Tehke see valik, et kasutada printimissätteid, mis on määratud kandele, dokumendile või moodulile lehel <strong>Prindihalduse seadistus</strong>.</span><span class="sxs-lookup"><span data-stu-id="90d97-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90d97-189">Kontrolli krediidilimiiti</span><span class="sxs-lookup"><span data-stu-id="90d97-189">Check credit limit</span></span></td>
<td><span data-ttu-id="90d97-190">Saate valida teabe, mida krediidilimiidi kontrollimisel tuleb analüüsida.</span><span class="sxs-lookup"><span data-stu-id="90d97-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="90d97-191"><strong>Pole</strong> – krediidilimiidi kontrollimiseks pole mingit vajadust.</span><span class="sxs-lookup"><span data-stu-id="90d97-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="90d97-192"><strong>Saldo</strong> – krediidilimiiti kontrollitakse kliendi saldo suhtes.</span><span class="sxs-lookup"><span data-stu-id="90d97-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="90d97-193"><strong>Saldo + saateleht või toote sissetulek</strong> – krediidilimiiti kontrollitakse kliendi saldo ja tarnete suhtes.</span><span class="sxs-lookup"><span data-stu-id="90d97-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="90d97-194"><strong>Saldo + kõik</strong> – krediidilimiiti kontrollitakse kliendi saldo, tarnete ja avatud tellimuste suhtes.</span><span class="sxs-lookup"><span data-stu-id="90d97-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90d97-195">Kreediti parandus</span><span class="sxs-lookup"><span data-stu-id="90d97-195">Credit correction</span></span></td>
<td><span data-ttu-id="90d97-196">Selle suvandi valimisel kuvatakse kreeditarve kanded tehingukannetes deebetina.</span><span class="sxs-lookup"><span data-stu-id="90d97-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90d97-197">Krediteeri järelejääv kogus</span><span class="sxs-lookup"><span data-stu-id="90d97-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="90d97-198">Kui sisestate kreeditarve, valige see suvand järelejäänud koguse tellimusel säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="90d97-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="90d97-199">Kui see suvand pole märgitud, määratakse järelejäänud koguseks 0 (null).</span><span class="sxs-lookup"><span data-stu-id="90d97-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90d97-200">Koondsisestamine</span><span class="sxs-lookup"><span data-stu-id="90d97-200">Summary update for</span></span></td>
<td><span data-ttu-id="90d97-201">Saate valida mitme müügitellimuse summeerimise viisi.</span><span class="sxs-lookup"><span data-stu-id="90d97-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="90d97-202"><strong>Puudub</strong> – müügitellimusi ei summeerita.</span><span class="sxs-lookup"><span data-stu-id="90d97-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="90d97-203">Näiteks luuakse iga müügitellimuse kohta eraldi arve.</span><span class="sxs-lookup"><span data-stu-id="90d97-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="90d97-204"><strong>Arvekonto</strong> – kõik valitud tellimused summeeritakse lehel <strong>Koondsisestamise parameetrid</strong> seadistatud kriteeriumide alusel.</span><span class="sxs-lookup"><span data-stu-id="90d97-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="90d97-205"><strong>Tellimus</strong> – valitud tellimuste vahemik summeeritakse ühte määratud tellimusse.</span><span class="sxs-lookup"><span data-stu-id="90d97-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="90d97-206">Tellimuses summeeritakse lehel <strong>Koondsisestamise parameetrid</strong> seadistatud kriteeriumide alusel.</span><span class="sxs-lookup"><span data-stu-id="90d97-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="90d97-207">Selle valiku korral tuleb valida väärtus väljal <strong>Müügitellimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="90d97-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="90d97-208"><strong>Automaatkokkuvõte</strong> – kui lehel <strong>Koondsisestamine</strong> on määratud koondsisestamised, summeeritakse kõik valitud tellimused lehel <strong>Koondsisestamise parameetrid</strong> määratud kriteeriumide alusel.</span><span class="sxs-lookup"><span data-stu-id="90d97-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="90d97-209">Kui koondsisestamisi pole määratud, sisestatakse tellimus eraldi.</span><span class="sxs-lookup"><span data-stu-id="90d97-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="90d97-210"><strong>Saateleht</strong> – valitud tellimuste vahemik summeeritakse iga saatelehe puhul ühele arvele.</span><span class="sxs-lookup"><span data-stu-id="90d97-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="90d97-211">Seda valikut saab kasutada ainult juhul, kui on tehtud valik <strong>Saateleht</strong> väljal <strong>Kogus</strong>.</span><span class="sxs-lookup"><span data-stu-id="90d97-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>




