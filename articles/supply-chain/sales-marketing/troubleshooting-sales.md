---
title: Müügitellimuste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada müügitellimustega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b5389b0d5a8ff68a3c16dedd2d8bb62f6e99af4f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824722"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="e5283-103">Müügitellimuste tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="e5283-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="e5283-104">Selles teemas kirjeldatakse, kuidas lahendada müügitellimustega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="e5283-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="e5283-105">Maksuteavet ei värskendata, kui muudan müügitellimuse päises asukohta.</span><span class="sxs-lookup"><span data-stu-id="e5283-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5283-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e5283-106">Issue description</span></span>

<span data-ttu-id="e5283-107">Kui kohta, ladu või tarneaadressi muudetakse kas müügitellimuse päises või reatasemel, ei värskendata juhtumi maksuteavet ridade puhul automaatselt.</span><span class="sxs-lookup"><span data-stu-id="e5283-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5283-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="e5283-108">Issue resolution</span></span>

<span data-ttu-id="e5283-109">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="e5283-109">This behavior is by design.</span></span> <span data-ttu-id="e5283-110">See probleem ilmneb seetõttu, et tarneaadressi, kohta ja ladu ei muudeta samuti automaatselt reatasemel.</span><span class="sxs-lookup"><span data-stu-id="e5283-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="e5283-111">Peate need käsitsi värskendama.</span><span class="sxs-lookup"><span data-stu-id="e5283-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="e5283-112">Kui samas perioodis või kattuvates perioodides on kaks kaubanduslepet, valitakse alati sama lepperida.</span><span class="sxs-lookup"><span data-stu-id="e5283-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5283-113">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e5283-113">Issue description</span></span>

<span data-ttu-id="e5283-114">Kui samas perioodis või kattuvates perioodides on määratletud kaks kaubanduslepet, valitakse sama kaubanduslepe iga kord, kui loote müügitellimuse ridu, mis sisaldavad neid kaupu.</span><span class="sxs-lookup"><span data-stu-id="e5283-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5283-115">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="e5283-115">Issue resolution</span></span>

<span data-ttu-id="e5283-116">Kui kindla kuupäevaga on rohkem kui üks kaubanduslepe, valitakse alati kõige madalama hinnaga kaubanduslepe.</span><span class="sxs-lookup"><span data-stu-id="e5283-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="e5283-117">Lisateabe saamiseks laadige alla järgmine tehniline ülevaade: [kaubanduslepped rakenduses Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="e5283-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="e5283-118">Kas saan nõudluse täitmiseks siduda ostutellimuse müügitellimusega?</span><span class="sxs-lookup"><span data-stu-id="e5283-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="e5283-119">Te saate luua ostutellimuse müügitellimuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="e5283-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="e5283-120">Lisateavet leiate teemast [Ostutellimuse loomine müügitellimuse põhjal](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="e5283-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="e5283-121">Ma ei saa tagastustellimust või müügitellimust tühistada ega kustutada.</span><span class="sxs-lookup"><span data-stu-id="e5283-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="e5283-122">Saate tühistada ainult müügitellimusi ja tagastustellimusi, mille olek on *Loodud*.</span><span class="sxs-lookup"><span data-stu-id="e5283-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="e5283-123">Lisateavet vt teemast [Tagastustellimuse tühistamine](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="e5283-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="e5283-124">Kui proovin müügitellimust tühistada, kuvatakse tõrge „Reserveeringuid ei saa eemaldada, kuna loodud on töö, mis sõltub nendest reserveeringutest”.</span><span class="sxs-lookup"><span data-stu-id="e5283-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="e5283-125">Tõrkekood: WAX4661</span><span class="sxs-lookup"><span data-stu-id="e5283-125">Error code: WAX4661</span></span>

<span data-ttu-id="e5283-126">Kui töö on seotud müügitellimusega, ei saa müügitellimust tühistada enne töö tühistamist.</span><span class="sxs-lookup"><span data-stu-id="e5283-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="e5283-127">See nõue kehtib ka juhul, kui müügitellimusega seotud töö on suletud.</span><span class="sxs-lookup"><span data-stu-id="e5283-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="e5283-128">Selle probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e5283-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="e5283-129">Tühistage töö ja pange varud tagasi soovitud asukohta.</span><span class="sxs-lookup"><span data-stu-id="e5283-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="e5283-130">Valige müügitellimuse asjakohane koorem ja valige koorma real kas **Vähenda komplekteeritud kogust** või toimingupaanil **Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="e5283-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="e5283-131">Töö olek on nüüd *Tühistatud* ning varude tagasipanemiseks asukohta, mida kirjeldati tühistamise ajal, luuakse automaatselt uus varude liikumise töö, mida ka kohe töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="e5283-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="e5283-132">Kustutage koorem.</span><span class="sxs-lookup"><span data-stu-id="e5283-132">Delete the load.</span></span> <span data-ttu-id="e5283-133">Saadetis kustutatakse samuti.</span><span class="sxs-lookup"><span data-stu-id="e5283-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="e5283-134">Nüüd peaks olema teil võimalik müügitellimust tühistada.</span><span class="sxs-lookup"><span data-stu-id="e5283-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="e5283-135">Ma ei saa tühistada kontsernisisest ostutellimust, mis on seotud müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="e5283-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5283-136">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e5283-136">Issue description</span></span>

<span data-ttu-id="e5283-137">Kui proovite tühistada müügitellimusega seotud kontsernisisest ostutellimust, võidakse kuvada järgmine tõrketeade: „Kogust ei saa vähendada, kuna järelejäänud värskendatud kogus muudab märki”.</span><span class="sxs-lookup"><span data-stu-id="e5283-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5283-138">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="e5283-138">Issue resolution</span></span>

<span data-ttu-id="e5283-139">See probleem parandati rakenduse Microsoft Dynamics 365 Supply Chain Management versioonis 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="e5283-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="e5283-140">Selles ja uuemates versioonides saate nüüd tühistada müügitellimusega seotud kontsernisiseseid ostutellimusi.</span><span class="sxs-lookup"><span data-stu-id="e5283-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="e5283-141">Kas saan taastada kustutatud arveldatud müügitellimuse?</span><span class="sxs-lookup"><span data-stu-id="e5283-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5283-142">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e5283-142">Issue description</span></span>

<span data-ttu-id="e5283-143">Arveldatud müügitellimus kustutati kogemata ja te soovite selle taastada või vaadata selle üksikasju.</span><span class="sxs-lookup"><span data-stu-id="e5283-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5283-144">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="e5283-144">Issue resolution</span></span>

<span data-ttu-id="e5283-145">Kui kustutatud müügitellimus on juba arveldatud, valige **Kliendi konto \> Kanded \> Algdokument \> Kuva üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="e5283-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="e5283-146">Leidke otsitav arve üles ja valige see, et vaadata selle üksikasju.</span><span class="sxs-lookup"><span data-stu-id="e5283-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="e5283-147">Need üksikasjad hõlmavad müügitellimuse viidet.</span><span class="sxs-lookup"><span data-stu-id="e5283-147">These details include the sales order reference.</span></span> <span data-ttu-id="e5283-148">Samuti peaks olema sellel lehel võimalik juurde pääseda müügitellimuse üksikasjadele.</span><span class="sxs-lookup"><span data-stu-id="e5283-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="e5283-149">Müügitellimuse päise tähtaega pole andmeüksuses SalesOrderHeaderV2Entity.</span><span class="sxs-lookup"><span data-stu-id="e5283-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="e5283-150">Üksuses *SalesOrderHeaderV2Entity* pole tähtaja välja.</span><span class="sxs-lookup"><span data-stu-id="e5283-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="e5283-151">Ma pean kustutama hüljatud müügitellimuskirjed.</span><span class="sxs-lookup"><span data-stu-id="e5283-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="e5283-152">Hüljatud müügitellimuskirjete puhastamiseks käivitage perioodiline töö *Müügitellimuse kustutamine* ühes järgmistes kohtadest.</span><span class="sxs-lookup"><span data-stu-id="e5283-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="e5283-153">Müük ja turundus \> Perioodilised ülesanded \> Puhastamine \> Müügitellimuste kustutamine</span><span class="sxs-lookup"><span data-stu-id="e5283-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="e5283-154">Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Puhastamine \> Müügitellimuste kustutamine</span><span class="sxs-lookup"><span data-stu-id="e5283-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="e5283-155">Kas on võimalik arvutada komisjonitasusid arvete puhul, mis on juba sisestatud?</span><span class="sxs-lookup"><span data-stu-id="e5283-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="e5283-156">Rakendus Supply Chain Management ei toeta praegu sisestatud arvete puhul komisjonitasude arvutamist.</span><span class="sxs-lookup"><span data-stu-id="e5283-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="e5283-157">Kontsernisiseses protsessis ei toetata kogumiüksust.</span><span class="sxs-lookup"><span data-stu-id="e5283-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="e5283-158">Kogumiüksus pole ostutellimuse jaoks saadaval, sest kogumiüksuse müügitellimuse ridu uurides võib märgata, et kogus on *0* (null) ja olek on *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="e5283-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="e5283-159">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="e5283-159">This behavior is by design.</span></span> <span data-ttu-id="e5283-160">Müügitellimus ostab ainult kogumiüksuse komponente.</span><span class="sxs-lookup"><span data-stu-id="e5283-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="e5283-161">See ei osta kogumiüksust ennast.</span><span class="sxs-lookup"><span data-stu-id="e5283-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="e5283-162">Kui peate kogumi ostma, kaaluge, kas peate selle märkima kogumiüksusena, kuna see funktsioon on mõeldud tulu tuvastamise stsenaariumide jaoks.</span><span class="sxs-lookup"><span data-stu-id="e5283-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="e5283-163">Lisateavet kogumiüksuste kohta leiate teemast [Kogumid](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="e5283-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]