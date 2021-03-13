---
title: Veose vastavusseviimine transpordihalduses
description: Selles artiklis selgitatakse veose vastavusseviimise protsessi.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014504"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="91f65-103">Veose vastavusseviimine transpordihalduses</span><span class="sxs-lookup"><span data-stu-id="91f65-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91f65-104">Selles artiklis selgitatakse veose vastavusseviimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="91f65-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="91f65-105">Veose vastavusseviimine võib toimuda käsitsi või olla seadistatud toimuma automaatselt.</span><span class="sxs-lookup"><span data-stu-id="91f65-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="91f65-106">Veose automaatse vastavusseviimise kasutamiseks tuleb seadistada auditi koondandmed, milles saate määratleda kriteeriumid, mis määravad, millised veoarved automaatselt vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="91f65-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="91f65-107">Veose vastavusseviimise protsess</span><span class="sxs-lookup"><span data-stu-id="91f65-107">The freight reconciliation process</span></span>

<span data-ttu-id="91f65-108">Veohinnad arvutab hinnamootor, mis on seotud vastava vedajaga.</span><span class="sxs-lookup"><span data-stu-id="91f65-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="91f65-109">Koorma kinnitamisel koostatakse veoarve ja veohinnad kantakse sellele üle.</span><span class="sxs-lookup"><span data-stu-id="91f65-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="91f65-110">Veohinnad jaotatakse vastavale lähtedokumendile (ostutellimus, müügitellimus ja/või üleviimistellimus) muude kuludena, olenevalt tavapärase arveldusprotsessi puhul kasutatavast seadistusest.</span><span class="sxs-lookup"><span data-stu-id="91f65-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="91f65-111">Kauba vastavusseviimise protsess (mida nimetatakse ka vastendusprotsessiks) alustatakse kohe, kui veoarve vedajalt saabub.</span><span class="sxs-lookup"><span data-stu-id="91f65-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="91f65-112">Arve võib võtta vastu elektrooniliselt või paberkandjal.</span><span class="sxs-lookup"><span data-stu-id="91f65-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="91f65-113">Kui arve saadakse paberkandjal, võite koostada elektroonilise arve, kasutades mallina veoarvet.</span><span class="sxs-lookup"><span data-stu-id="91f65-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="91f65-114">[![Veose vastavusseviimise protsess](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="91f65-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="91f65-115">Käsitsi vastavusseviimine</span><span class="sxs-lookup"><span data-stu-id="91f65-115">Manual reconciliation</span></span>

<span data-ttu-id="91f65-116">Kui viite veose vastavusse käsitsi, tuleb vastendada iga arve rida veoarve reaga või arveldatava koorma ridadega.</span><span class="sxs-lookup"><span data-stu-id="91f65-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="91f65-117">Selline vastendamine toimub lehel **Veoarve ja arvete võrdlemine**.</span><span class="sxs-lookup"><span data-stu-id="91f65-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="91f65-118">Kui arve real olev summa ei vasta veoarve summale, tuleb valida vahe jaoks vastavusseviimise põhjus.</span><span class="sxs-lookup"><span data-stu-id="91f65-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="91f65-119">Kui vastavusseviimisel on mitu põhjust, võite vastendamata summa nende vahel ära jagada.</span><span class="sxs-lookup"><span data-stu-id="91f65-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="91f65-120">Vastavusseviimise põhjus määrab, kuidas vahesummad pearaamatusse sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="91f65-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="91f65-121">Kui arvestatakse kogu arve summat, esitatakse see kinnitamiseks ja seejärel tööleht sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="91f65-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="91f65-122">Järgmine illustratsioon näitab, kuidas koostada veose arvet ja veost vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="91f65-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="91f65-123">[![Veose vastavusseviimise ülesanded](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="91f65-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="91f65-124">Automaatne vastavusseviimine</span><span class="sxs-lookup"><span data-stu-id="91f65-124">Automatic reconciliation</span></span>

<span data-ttu-id="91f65-125">Automaatse vastavusseviimise kasutamiseks tuleb määrata vastavusseviimise graafik ning kasutatavad arved ja vedajad.</span><span class="sxs-lookup"><span data-stu-id="91f65-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="91f65-126">Vastendamine arve ridadel ja veoarvetel toimub auditi koondandmete ja veose arve tüübi seadistusele.</span><span class="sxs-lookup"><span data-stu-id="91f65-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="91f65-127">Pärast automaatse vastavusseviimise käitamist tuleb tegeleda arvetega, millele süsteem vastet ei leia.</span><span class="sxs-lookup"><span data-stu-id="91f65-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="91f65-128">Neid arveid peab siis käsitsi töötlema, enne kui saate kõik arved maksmiseks sisestada.</span><span class="sxs-lookup"><span data-stu-id="91f65-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="91f65-129">Veoarvete vastendamine veose arvetega, kasutades automaatset ja käsitsi vastavusseviimist</span><span class="sxs-lookup"><span data-stu-id="91f65-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="91f65-130">*Vastendamine* on igale veoarvele vastavate veose arvete otsimise protsess.</span><span class="sxs-lookup"><span data-stu-id="91f65-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="91f65-131">Seda saab teha, vastendades arveread ükshaaval (käsitsi vastendamine) või vastendades kõik saadaolevad arved korraga (automaatne vastendamine).</span><span class="sxs-lookup"><span data-stu-id="91f65-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="91f65-132">Automaatne vastendamine</span><span class="sxs-lookup"><span data-stu-id="91f65-132">Auto matching</span></span>

<span data-ttu-id="91f65-133">Kui vastendate mitu veoarvet sama veose arvega, toimib automaatse vastendamise protsess järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="91f65-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="91f65-134">Kõik veoarved, mida ei vastendata, sorditakse summa alusel suurima summaga esimesena.</span><span class="sxs-lookup"><span data-stu-id="91f65-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="91f65-135">Veoarveid vastendatakse ükshaaval, kuni veoarvel puudub positiivne summa.</span><span class="sxs-lookup"><span data-stu-id="91f65-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="91f65-136">Sõltuvalt auditi koondandmete seadistusest ja veose arvete jääksummast määratakse järelejäänud summa.</span><span class="sxs-lookup"><span data-stu-id="91f65-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="91f65-137">Käsitsi vastavusse viimine</span><span class="sxs-lookup"><span data-stu-id="91f65-137">Manual matching</span></span>

<span data-ttu-id="91f65-138">Vastendamiseks on saadaval kõik positiivsete summadega veoarved.</span><span class="sxs-lookup"><span data-stu-id="91f65-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="91f65-139">Sarnaselt automaatsele vastendamisele, saab kasutaja vastendada veoarved ainult negatiivsete summadega veoste arvetega, mis pole täielikult vastendatud.</span><span class="sxs-lookup"><span data-stu-id="91f65-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="91f65-140">Näide</span><span class="sxs-lookup"><span data-stu-id="91f65-140">Example</span></span>

<span data-ttu-id="91f65-141">Oletame, et teil on veoarve (FB) summaks 1500 ja olete loonud kolm veose arvet ühe arv reaga iga arve jaoks järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="91f65-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="91f65-142">Algne veoarve (FB): summa 1500</span><span class="sxs-lookup"><span data-stu-id="91f65-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="91f65-143">Arve 1 (Inv1): summa 1000</span><span class="sxs-lookup"><span data-stu-id="91f65-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="91f65-144">Arve 2 (Inv2): summa 600</span><span class="sxs-lookup"><span data-stu-id="91f65-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="91f65-145">Arve 3 (Inv3): summa –100</span><span class="sxs-lookup"><span data-stu-id="91f65-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="91f65-146">Automaatse vastendamise tulemus</span><span class="sxs-lookup"><span data-stu-id="91f65-146">Automatic matching result</span></span>

<span data-ttu-id="91f65-147">Automaatne vastendamine käivitab järgmise järjestuse.</span><span class="sxs-lookup"><span data-stu-id="91f65-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="91f65-148">Sordi kõik veoarved summa alusel kahanevalt: Inv1 -> Inv2 -> Inv3.</span><span class="sxs-lookup"><span data-stu-id="91f65-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="91f65-149">Vastenda Inv1 FB-ga.</span><span class="sxs-lookup"><span data-stu-id="91f65-149">Match Inv1 with FB.</span></span> <span data-ttu-id="91f65-150">Inv1-le on vastendatud 1000 ja FB-le on järele jäänud summa 500, seega on olekuks *Osaliselt vastendatud*.</span><span class="sxs-lookup"><span data-stu-id="91f65-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="91f65-151">Vastenda Inv2 FB-ga.</span><span class="sxs-lookup"><span data-stu-id="91f65-151">Match Inv2 with FB.</span></span> <span data-ttu-id="91f65-152">Inv2-le on vastendatud 500 ja FB-le on järele jäänud summa 0, seega on olekuks *Täielikult vastendatud*.</span><span class="sxs-lookup"><span data-stu-id="91f65-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="91f65-153">Kuna FB on nüüd täielikult vastendatud, siis arvet Inv3 ei töödelda.</span><span class="sxs-lookup"><span data-stu-id="91f65-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="91f65-154">Käsitsi vastendamise tulemus</span><span class="sxs-lookup"><span data-stu-id="91f65-154">Manual matching result</span></span>

<span data-ttu-id="91f65-155">Käsitsi vastendamiseks varieeruvad tulemused olenevalt vastendamise järjestusest, nagu näidatud järgmistel näidisjuhtumitel.</span><span class="sxs-lookup"><span data-stu-id="91f65-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="91f65-156">Käsitsi vastendamise juhtum 1</span><span class="sxs-lookup"><span data-stu-id="91f65-156">Manual matching case 1</span></span>

<span data-ttu-id="91f65-157">Üks moodus käsitsi vastendamiseks on jätkata järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="91f65-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="91f65-158">Vastenda FB Inv1-ga.</span><span class="sxs-lookup"><span data-stu-id="91f65-158">Match FB with Inv1.</span></span> <span data-ttu-id="91f65-159">FB-le on järele jäänud summa 500, seega on olekuks *Osaliselt vastendatud*.</span><span class="sxs-lookup"><span data-stu-id="91f65-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="91f65-160">Vastenda Inv2 FB-ga.</span><span class="sxs-lookup"><span data-stu-id="91f65-160">Match Inv2 with FB.</span></span> <span data-ttu-id="91f65-161">Inv2-le on vastendatud 500 ja FB-le on järele jäänud summa 0, seega on olekuks *Täielikult vastendatud*.</span><span class="sxs-lookup"><span data-stu-id="91f65-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="91f65-162">Inv3 käsitsi vastendamisel ei leia te vastendamata veose arveid.</span><span class="sxs-lookup"><span data-stu-id="91f65-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="91f65-163">See juhtum on põhimõtteliselt sama, mis automaatne vastendamine</span><span class="sxs-lookup"><span data-stu-id="91f65-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="91f65-164">Käsitsi vastendamise juhtum 2</span><span class="sxs-lookup"><span data-stu-id="91f65-164">Manual matching case 2</span></span>

<span data-ttu-id="91f65-165">Teine moodus käsitsi vastendamiseks on jätkata järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="91f65-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="91f65-166">Vastenda Inv3 FB-ga.</span><span class="sxs-lookup"><span data-stu-id="91f65-166">Match Inv3 with FB.</span></span> <span data-ttu-id="91f65-167">Nüüd on FB jääksumma 1600, mis on sama, mis negatiivse 100 lahutamisel 1500-st.</span><span class="sxs-lookup"><span data-stu-id="91f65-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="91f65-168">Nii FB kui ka Inv3 vastendatud kogus on –100.</span><span class="sxs-lookup"><span data-stu-id="91f65-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="91f65-169">Vastendage Inv1 ja Inv2 FB-ga üksteise järel.</span><span class="sxs-lookup"><span data-stu-id="91f65-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="91f65-170">FB on täielikult vastendatud.</span><span class="sxs-lookup"><span data-stu-id="91f65-170">FB is fully matched.</span></span>

<span data-ttu-id="91f65-171">Nagu see näide näitab, tuleks veose arveid vastendada negatiivsete summadega ainult käsitsi.</span><span class="sxs-lookup"><span data-stu-id="91f65-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="91f65-172">See tagab, et veose arveid ja negatiivseid summasid oleks võimalik vastendada veose arvega, mis ei ole täielikult vastendatud, kuna see võimaldab teil kontrollida sobiva järjestuse järjekorda.</span><span class="sxs-lookup"><span data-stu-id="91f65-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>
