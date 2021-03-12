---
title: Toote sissetulekute ja arvelduse tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada toote sissetulekute ja arveldusega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 22b1abec0c6dd5f571e604c5c07379b397b8bdaa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999049"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="d3e9c-103">Toote sissetulekute ja arvelduse tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="d3e9c-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="d3e9c-104">Selles teemas kirjeldatakse, kuidas lahendada toote sissetulekute ja arveldusega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="d3e9c-105">Ma ei saa sisestada rohkem kui üht arvet ostutellimuse reale, millel on kategooriapõhised kaubad.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="d3e9c-106">Kui soovite arveid sisestada, on kogus kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="d3e9c-107">Kui rea terve kogus on arveldatud ainult osalise summana, ei saa te ülejäänud summat teises arves arveldada.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="d3e9c-108">Ostutellimuse kinnitamise ajal kuvatakse tõrge „Objekti viide ei ole seatud” või hankija arve sisestamisel ilmneb erand „Kutsumise sihtmärgi puhul ilmnes erand”.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="d3e9c-109">See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="d3e9c-110">Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="d3e9c-111">Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="d3e9c-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="d3e9c-112">Ma ei saa mitut toote sissetulekut üheks ostutellimuseks konsolideerida.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="d3e9c-113">Te ei saa mitut toote sissetulekut üheks ostutellimuseks konsolideerida, kui toote sissetuleku ridadel on eri aruandluskuupäevad.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="d3e9c-114">Rakenduse Microsoft Dynamics 365 Supply Chain Management varasemates versioonides oli selles olukorras konsolideerimine lubatud.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="d3e9c-115">Kuid selle tava puhul tekivad tihti vead.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-115">However, the practice is prone to error.</span></span> <span data-ttu-id="d3e9c-116">Loodavate ostutellimuse ridade aruandluskuupäev ei tohi erineda selliste toote sissetuleku ridade aruandluskuupäevast, mille põhjal need ostutellimuse read loodi.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="d3e9c-117">(Ostutellimuse ridade aruandluskuupäev ühtib ostutellimuse päises oleva aruandluskuupäevaga.) Seetõttu pole mitme toote sissetuleku konsolideerimine üheks ostutellimuseks enam lubatud.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="d3e9c-118">Aruandluskuupäeva kasutatakse näiteks eelarvereservi ja pandiõiguse puhul.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="d3e9c-119">Seetõttu tuleks see säilitada toote sissetulekust ostutellimusele ülemineku ajal.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="d3e9c-120">Toote sissetulekute tühistamise korral saab kandeid sisestada peatatud pearaamatukontole.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d3e9c-121">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d3e9c-121">Issue description</span></span>

<span data-ttu-id="d3e9c-122">Kui toote sissetulek tühistatakse, lubab süsteem sisestada kandeid peatatud pearaamatukontodele, kuigi põhikontod on peatatud.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="d3e9c-123">Probleemi taastekitamine</span><span class="sxs-lookup"><span data-stu-id="d3e9c-123">Reproduce the issue</span></span>

<span data-ttu-id="d3e9c-124">Järgmine protsess näitab üht viisi probleemi taastekitamiseks.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="d3e9c-125">Veenduge, et lehe **Ostureskontro parameetrid** vahekaardil **Üldine** oleks suvandi **Sisesta toote sissetulek pearaamatusse** väärtuseks seatud *Jah*.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="d3e9c-126">Looge ostutellimus ja lisage tellimuse rida, mille toote kogus on *1000*.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="d3e9c-127">Kinnitage ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="d3e9c-128">Sisestage toote sissetulek ja kontrollige kandeid.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="d3e9c-129">Peatage asjakohased põhikontod *200140* ja *140200*.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="d3e9c-130">Tühistage sisestatud toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="d3e9c-131">Pange tähele, et peatatud pearaamatukontodele saab kandeid sisestada.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d3e9c-132">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="d3e9c-132">Issue resolution</span></span>

<span data-ttu-id="d3e9c-133">Kandeid saab toote sissetulekute tühistamise korral peatatud pearaamatukontodele sisestada, kuna selline olukord lubab teha õigeid sisestusi.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="d3e9c-134">Toote sissetuleku kandenumbrit tarbitakse isegi siis, kui toote sissetuleku käigus ei looda ühtegi finantskannet.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="d3e9c-135">Kui suvandi **Kumuleerimise kohustus toote sissetulekul** väärtuseks on kauba mudeligrupi puhul seatud *Ei*, siis pearaamatusse sisestusi ei tehta.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="d3e9c-136">Sellegi poolest kirjendatakse füüsiline sündmus raamatupidamise otstarbel alammoodulis ja selle sündmuse jaoks on vaja kandenumbrit.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="d3e9c-137">See kandenumber on laokannetes viidatud kandenumber.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="d3e9c-138">Me soovitame seada suvandi **Kumuleerimise kohustus toote sissetulekul** väärtuseks *Jah*, nagu on kirjeldatud ajaveebipostituses [Lisakulude sisestamine toote sissetuleku ajal](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="d3e9c-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="d3e9c-139">Säte „Sisesta pearaamatu kulude kontole” pole sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d3e9c-140">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d3e9c-140">Issue description</span></span>

<span data-ttu-id="d3e9c-141">Probleem ilmneb siis, kui ostutellimust arveldatakse olukorras, kus suvandi **Sisesta pearaamatu kulude kontole** väärtuseks on seatud *Jah* vahekaardil **Arve**, mis asub lehel **Ostureskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="d3e9c-142">Probleemi taastekitamine</span><span class="sxs-lookup"><span data-stu-id="d3e9c-142">Reproduce the issue</span></span>

<span data-ttu-id="d3e9c-143">Järgmine protsess näitab üht viisi probleemi taastekitamiseks.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="d3e9c-144">Avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="d3e9c-145">Seadke vahekaardil **Arve** suvandi **Sisesta pearaamatu kulude kontole** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="d3e9c-146">Avage **Varude haldus \> Seadistus \> Sisestus \> Sisestus**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="d3e9c-147">Tehke kindlaks, et te olete vahekaardil **Ostutellimus** kõik toote ostukulu read kustutanud.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="d3e9c-148">Avage jaotis **Ostureskontro \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d3e9c-149">Looge ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-149">Create a purchase order.</span></span> <span data-ttu-id="d3e9c-150">Valige väljal **Hankija konto** suvand *1001 Acme Office Supplies*.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="d3e9c-151">Lisage järgmiste sätetega ostutellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="d3e9c-152">**Kauba kood:** *D0011 Laser Projector*</span><span class="sxs-lookup"><span data-stu-id="d3e9c-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="d3e9c-153">**Koht:** *1*</span><span class="sxs-lookup"><span data-stu-id="d3e9c-153">**Site:** *1*</span></span>
    - <span data-ttu-id="d3e9c-154">**Ladu:** *11*</span><span class="sxs-lookup"><span data-stu-id="d3e9c-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="d3e9c-155">**Kogus:** *4*</span><span class="sxs-lookup"><span data-stu-id="d3e9c-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="d3e9c-156">Valige toimingupaanil vahekaardi **Ostmine** grupis **Tegevus** suvand **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="d3e9c-157">Tehke toimingupaani vahekaardil **Vastuvõtmine** grupis **Loo** valik **Toote sissetulek**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="d3e9c-158">Sisestage dialoogiboksis **Toote sissetuleku sisestamine** väljale **Toote sissetulek** suvaline number ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="d3e9c-159">Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="d3e9c-160">Sisestage väljale **Number** arve numbrina suvaline arv.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="d3e9c-161">Värskendage vastavusseviimise olekut ja sisestage.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="d3e9c-162">Pange tähele, et te saate nüüd ostutellimuse põhjal arvet luues järgmise tõrke: „Toote ostukulu kandetüübi kontonumbrit pole olemas”.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d3e9c-163">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="d3e9c-163">Issue resolution</span></span>

<span data-ttu-id="d3e9c-164">See sõltub arvete ja arvegruppide parameetrite seadistusest.</span><span class="sxs-lookup"><span data-stu-id="d3e9c-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="d3e9c-165">Lisateavet leiate ajaveebipostitusest [Raamatupidamine ostukulu ja varude muudatuste puhul](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="d3e9c-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
