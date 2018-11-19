---
title: Retaili ettemaksuarved Ida-Euroopa puhul
description: Selles teemas selgitatakse, kuidas seadistada Ida-Euroopa ettemaksu teavitusi.
author: epopov
manager: annbe
ms.date: 10/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: ba2cfb176242e2e611375c9943a9e4da2b2bb02a
ms.contentlocale: et-ee
ms.lasthandoff: 11/01/2018

---

# <a name="advance-invoices-for-retail-for-eastern-europe"></a><span data-ttu-id="f8356-103">Retaili ettemaksuarved Ida-Euroopa puhul</span><span class="sxs-lookup"><span data-stu-id="f8356-103">Advance invoices for Retail for Eastern Europe</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8356-104">Selles teemas sisalduv teave kehtib Ida-Euroopa asukohale ja puudutab konkreetselt jaemüüki.</span><span class="sxs-lookup"><span data-stu-id="f8356-104">The information in this topic applies to the Eastern European localization and is specific to the retail industry.</span></span>

<span data-ttu-id="f8356-105">Poola, Ungari ja Tšehhi Vabariigi korral tuleb peale kliendilt müügipunktis saadud ettemakset see ettemakse maksude eesmärgil registreerida ning vajalik on luua ja trükkida ettemaksuarve, mis sisaldab ettemaksu summat.</span><span class="sxs-lookup"><span data-stu-id="f8356-105">For Poland, Hungary, and Czech Republic, when a prepayment is received from a customer via Point of Sale (POS), the prepayment must be registered for tax purposes, and it's required to generate and print an advance invoice document that includes the prepayment amount.</span></span> <span data-ttu-id="f8356-106">Lisaks tuleb Poola korral ettemaksearvete tehingud kanda pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="f8356-106">Additionally, for Poland, advance invoice transactions must be posted in the general ledger.</span></span>

<span data-ttu-id="f8356-107">Kui müügitellimuse arve lõpuks sisestatakse, peaks lõppdokument sisaldama ettemaksuarvet ning näidatud peaksid olema mistahes ettemaksed.</span><span class="sxs-lookup"><span data-stu-id="f8356-107">When the invoice for the sales order is finally posted, the final document should include the advance invoice, and any prepayments should be indicated.</span></span>

<span data-ttu-id="f8356-108">Kui loote müügireskontost müügitellimusi, peate looma ettemaksuarved käsitsi, kasutades jaotise [Ida-Euroopa ettemaksuarved](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/emea-advance-invoice) protseduure.</span><span class="sxs-lookup"><span data-stu-id="f8356-108">If you generate sales orders from Accounts receivable, you must manually generate advance invoices by using the procedure in [Advance invoices for Eastern Europe](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span></span> <span data-ttu-id="f8356-109">Kui loote müügitellimusi kassa kaudu, loob ja sisestab teile ettemaksearved süsteem.</span><span class="sxs-lookup"><span data-stu-id="f8356-109">If you generate sales orders via POS, the system generates and posts the advance invoices for you.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="f8356-110">Toetatud stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="f8356-110">Supported scenarios</span></span>

<span data-ttu-id="f8356-111">Toetatud on järgmised stsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="f8356-111">The following scenarios are supported:</span></span>

- <span data-ttu-id="f8356-112">Ettemaksuarve loomine ja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="f8356-112">Create and post an advance invoice.</span></span>
- <span data-ttu-id="f8356-113">Deposiidisumma muutmine.</span><span class="sxs-lookup"><span data-stu-id="f8356-113">Modify a deposit amount.</span></span> <span data-ttu-id="f8356-114">Kui klient otsustab sissemakse summat suurendada, väljastatakse lisandub ettemaksuarve.</span><span class="sxs-lookup"><span data-stu-id="f8356-114">If a customer decides to increase the amount of a deposit, an additional advance invoice is issued.</span></span> <span data-ttu-id="f8356-115">Kõigi teiste deposiidisumma muudatuste korral (näiteks, kui kliendi tellimust muudetakse), luuakse eelnevalt loodud ettemaksuarvele kreeditarve ning luuakse ja sisestatakse uus ettemaksuarve parandatud summaga.</span><span class="sxs-lookup"><span data-stu-id="f8356-115">For all other changes to the deposit amount (for example, if a customer order is edited), a credit note is created for the advance invoice that was previously generated, and a new advance invoice is generated and posted for the corrected amount.</span></span>
- <span data-ttu-id="f8356-116">Seotud ettemaksuarvetega müügitellimuse tühistamine.</span><span class="sxs-lookup"><span data-stu-id="f8356-116">Cancel a sales order that has linked advance invoices.</span></span> <span data-ttu-id="f8356-117">Sellisel juhul luuakse ettemaksuarvele kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="f8356-117">In this case, a credit note is created for the advance invoice.</span></span>
- <span data-ttu-id="f8356-118">Ettemaksuarvetega seotud müügitellimuse arve sisestamine.</span><span class="sxs-lookup"><span data-stu-id="f8356-118">Post a sales order invoice that has linked advance invoices.</span></span> <span data-ttu-id="f8356-119">Müügiarve tühistatakse müügitellimusega seotud ettemaksuarve summas.</span><span class="sxs-lookup"><span data-stu-id="f8356-119">The advance invoice that is linked to a sales order is reversed for the amount of the sales invoice.</span></span> <span data-ttu-id="f8356-120">Esialgse ettemaksuarve kanded tasakaalustatakse ettemaksuarve tühistamise kannetega.</span><span class="sxs-lookup"><span data-stu-id="f8356-120">The advance invoice transactions are settled with advance invoice reversal transactions.</span></span>

## <a name="set-up-advance-invoices"></a><span data-ttu-id="f8356-121">Ettemaksuarvete seadistamine</span><span class="sxs-lookup"><span data-stu-id="f8356-121">Set up advance invoices</span></span>

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a><span data-ttu-id="f8356-122">Ettemaksuarvete loomise funktsionaalsuse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="f8356-122">Turn on the functionality for creating advance invoices</span></span>

1. <span data-ttu-id="f8356-123">Valige **Jaemüük \> Peakontori seadistamine \> Parameetrid \> Jaemüügi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f8356-123">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span>
2. <span data-ttu-id="f8356-124">Seadistage **Tellimus** kiirkaardi **Klienditellimused** vahekaardi suvand **Deposiidi ettemaksuarve koostamine** **Jah** peale.</span><span class="sxs-lookup"><span data-stu-id="f8356-124">On the **Customer orders** tab, on the **Order** FastTab, set the **Create advance invoice for deposit** option to **Yes**.</span></span>

### <a name="define-the-parameters-for-posting-advance-invoices"></a><span data-ttu-id="f8356-125">Ettemaksuarvete sisestamise parameetrite määramine.</span><span class="sxs-lookup"><span data-stu-id="f8356-125">Define the parameters for posting advance invoices</span></span>

1. <span data-ttu-id="f8356-126">Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f8356-126">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="f8356-127">Seadistage **Ettemaksuarve** kiirkaardi **Uuendused** vahekaardil **Sisestusreeglid**, **Käibemaksugrupp**, ja **Kauba käibemaksugrupp** väljad.</span><span class="sxs-lookup"><span data-stu-id="f8356-127">On the **Updates** tab, on the **Advance invoice** FastTab, set the **Posting profile**, **Sales tax group**, and **Item sales tax group** fields.</span></span> <span data-ttu-id="f8356-128">Kui need väljad on õigesti seadistatud, sisestatakse ettemaksuarve.</span><span class="sxs-lookup"><span data-stu-id="f8356-128">If these fields are set correctly, the advance invoice will be posted.</span></span> <span data-ttu-id="f8356-129">Kui need väljad ei ole seadistatud, ettemaksuarveid ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="f8356-129">If these fields aren't set, advance invoices won't be posted.</span></span>

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a><span data-ttu-id="f8356-130">Lülitage välja käibemaksu sisestamine ettemaksu töölehekandele</span><span class="sxs-lookup"><span data-stu-id="f8356-130">Turn off posting of the Sales tax on prepayment journal voucher</span></span>

<span data-ttu-id="f8356-131">Ettemaksu töölehekande käibemaksu ei sisestata, kui ettemaksuarve sisestamine on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="f8356-131">The Sales tax on prepayment journal voucher must not be posted if advance invoice posting is turned on.</span></span> <span data-ttu-id="f8356-132">Selle nõude täitmise kontrollimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f8356-132">To verify that this requirement is met, follow these steps.</span></span>

1. <span data-ttu-id="f8356-133">Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f8356-133">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="f8356-134">Veenduge, et **Makse** kiirkaardi **Pearaamat ja käibemaks** vahekaardil on järgmised väljad kas tühjad või seadistatud **Ei** peale:</span><span class="sxs-lookup"><span data-stu-id="f8356-134">On the **Ledger and sales tax** tab, on the **Payment** FastTab, make sure that the following fields are blank or set to **No**:</span></span>

    - <span data-ttu-id="f8356-135">Ettemaksu töölehekande käibemaks</span><span class="sxs-lookup"><span data-stu-id="f8356-135">Sales tax on prepayment journal voucher</span></span>
    - <span data-ttu-id="f8356-136">Sisestusreeglid ettemaksu töölehekandega</span><span class="sxs-lookup"><span data-stu-id="f8356-136">Posting profile with prepayment journal voucher</span></span>
    - <span data-ttu-id="f8356-137">Ettemakse maksugrupp</span><span class="sxs-lookup"><span data-stu-id="f8356-137">Tax group for prepayment</span></span>
    - <span data-ttu-id="f8356-138">Kauba käibemaksugrupp</span><span class="sxs-lookup"><span data-stu-id="f8356-138">Item Sales tax group</span></span>

## <a name="print-advance-invoices"></a><span data-ttu-id="f8356-139">Ettemaksuarvete printimine</span><span class="sxs-lookup"><span data-stu-id="f8356-139">Print advance invoices</span></span>

<span data-ttu-id="f8356-140">Ettemaksuarveid saate printida kassast Microsoft Windowsi printeriga, mis on riistvarajaamaga ühendatud.</span><span class="sxs-lookup"><span data-stu-id="f8356-140">You can print advance invoices from POS on a Microsoft Windows printer that is connected to the hardware station.</span></span> <span data-ttu-id="f8356-141">Kassast ettemaksuarvete printimiseks on kaks võimalust:</span><span class="sxs-lookup"><span data-stu-id="f8356-141">There are two options for printing an advance invoice from POS:</span></span>

- <span data-ttu-id="f8356-142">**Printige ettemaksuarve pärast kassas kande lõpetamist.**</span><span class="sxs-lookup"><span data-stu-id="f8356-142">**Print an advance invoice after a transaction is concluded in POS.**</span></span> <span data-ttu-id="f8356-143">See suvand kuvatakse automaatselt, kui ettemaksuarve on loodud ja Windowsi printer on õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="f8356-143">This option occurs automatically if an advance invoice was generated and a Windows printer was correctly set up.</span></span> <span data-ttu-id="f8356-144">Sel juhul prinditakse ainult viimane klienditellimusega seotud ettemaksuarve.</span><span class="sxs-lookup"><span data-stu-id="f8356-144">In this case, only the last advance invoice that is linked to the customer order is printed.</span></span>
- <span data-ttu-id="f8356-145">**Ettemaksuarve töölehelt uuesti printimine.**</span><span class="sxs-lookup"><span data-stu-id="f8356-145">**Reprint an advance invoice from the transaction journal.**</span></span> <span data-ttu-id="f8356-146">Valige töölehtede avamiseks **Näita töölehte**, leidke klienditellimus ja seejärel valige **Prindi ettemaksuarve**.</span><span class="sxs-lookup"><span data-stu-id="f8356-146">Select **Show journal** to open the transactions journal, find the customer order, and then select **Print Advance invoice**.</span></span> <span data-ttu-id="f8356-147">Sel juhul prinditakse kõik kliendi tellimusega seotud ettemaksuarved.</span><span class="sxs-lookup"><span data-stu-id="f8356-147">In this case, all advance invoices that are linked to the customer order are printed.</span></span>

### <a name="set-up-a-windows-printer"></a><span data-ttu-id="f8356-148">Windowsi printeri seadistamine</span><span class="sxs-lookup"><span data-stu-id="f8356-148">Set up a Windows printer</span></span>

<span data-ttu-id="f8356-149">Riistvarajaamaga ühendatud Windowsi printeriga dokumentide kassast printimise võimaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f8356-149">Follow these steps to enable documents to be printed from POS on a Windows printer that is connected to the hardware station.</span></span>

1. <span data-ttu-id="f8356-150">Avage **Jaemüük \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Riistvara profiilid**.</span><span class="sxs-lookup"><span data-stu-id="f8356-150">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
2. <span data-ttu-id="f8356-151">Valige riistvaraprofiil, mis on seotud selle kauplusega, kus printerit kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="f8356-151">Select a hardware profile that is related to the store where the printer is used.</span></span>
3. <span data-ttu-id="f8356-152">Uuendage seaded kas jaotises **Printer** või jaotises **Printer 2**:</span><span class="sxs-lookup"><span data-stu-id="f8356-152">In either the **Printer** section or the **Printer 2** section, update the settings:</span></span>

    - <span data-ttu-id="f8356-153">Väljal **Printer** valige **Windowsi draiver**.</span><span class="sxs-lookup"><span data-stu-id="f8356-153">In the **Printer** field, select **Windows driver**.</span></span>
    - <span data-ttu-id="f8356-154">Sisestage printeri nimi väljale **Seadme nimi**.</span><span class="sxs-lookup"><span data-stu-id="f8356-154">In the **Device name** field, enter the name of the printer.</span></span>

4. <span data-ttu-id="f8356-155">Avage **Jaemüük \> Jaemüügi IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="f8356-155">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="f8356-156">Valige töö **1090** ja seejärel **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="f8356-156">Select job **1090**, and then select **Run now**.</span></span>

