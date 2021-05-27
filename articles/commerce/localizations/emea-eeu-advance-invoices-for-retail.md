---
title: Commerce'i ettemaksuarved Ida-Euroopa puhul
description: Selles teemas selgitatakse, kuidas seadistada Ida-Euroopa ettemaksu teavitusi.
author: epopov
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7771dfb9d9aa6dc87ef9eaee078c45ea66a5e143
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020290"
---
# <a name="advance-invoices-for-commerce-for-eastern-europe"></a><span data-ttu-id="816ed-103">Commerce'i ettemaksuarved Ida-Euroopa puhul</span><span class="sxs-lookup"><span data-stu-id="816ed-103">Advance invoices for Commerce for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="816ed-104">Selles teemas sisalduv teave kehtib Ida-Euroopa asukohale ja puudutab konkreetselt kaubandust.</span><span class="sxs-lookup"><span data-stu-id="816ed-104">The information in this topic applies to the Eastern European localization and is specific to the commerce industry.</span></span>

<span data-ttu-id="816ed-105">Poola, Ungari ja Tšehhi Vabariigi korral tuleb peale kliendilt müügipunktis saadud ettemakset see ettemakse maksude eesmärgil registreerida ning vajalik on luua ja trükkida ettemaksuarve, mis sisaldab ettemaksu summat.</span><span class="sxs-lookup"><span data-stu-id="816ed-105">For Poland, Hungary, and Czech Republic, when a prepayment is received from a customer via Point of Sale (POS), the prepayment must be registered for tax purposes, and it's required to generate and print an advance invoice document that includes the prepayment amount.</span></span> <span data-ttu-id="816ed-106">Lisaks tuleb Poola korral ettemaksearvete tehingud kanda pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="816ed-106">Additionally, for Poland, advance invoice transactions must be posted in the general ledger.</span></span>

<span data-ttu-id="816ed-107">Kui müügitellimuse arve lõpuks sisestatakse, peaks lõppdokument sisaldama ettemaksuarvet ning näidatud peaksid olema mistahes ettemaksed.</span><span class="sxs-lookup"><span data-stu-id="816ed-107">When the invoice for the sales order is finally posted, the final document should include the advance invoice, and any prepayments should be indicated.</span></span>

<span data-ttu-id="816ed-108">Kui loote müügireskontost müügitellimusi, peate looma ettemaksuarved käsitsi, kasutades jaotise [Ida-Euroopa ettemaksuarved](/dynamics365/unified-operations/financials/localizations/emea-advance-invoice) protseduure.</span><span class="sxs-lookup"><span data-stu-id="816ed-108">If you generate sales orders from Accounts receivable, you must manually generate advance invoices by using the procedure in [Advance invoices for Eastern Europe](/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span></span> <span data-ttu-id="816ed-109">Kui loote müügitellimusi kassa kaudu, loob ja sisestab teile ettemaksearved süsteem.</span><span class="sxs-lookup"><span data-stu-id="816ed-109">If you generate sales orders via POS, the system generates and posts the advance invoices for you.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="816ed-110">Toetatud stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="816ed-110">Supported scenarios</span></span>

<span data-ttu-id="816ed-111">Toetatud on järgmised stsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="816ed-111">The following scenarios are supported:</span></span>

- <span data-ttu-id="816ed-112">Ettemaksuarve loomine ja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="816ed-112">Create and post an advance invoice.</span></span>
- <span data-ttu-id="816ed-113">Deposiidisumma muutmine.</span><span class="sxs-lookup"><span data-stu-id="816ed-113">Modify a deposit amount.</span></span> <span data-ttu-id="816ed-114">Kui klient otsustab sissemakse summat suurendada, väljastatakse lisandub ettemaksuarve.</span><span class="sxs-lookup"><span data-stu-id="816ed-114">If a customer decides to increase the amount of a deposit, an additional advance invoice is issued.</span></span> <span data-ttu-id="816ed-115">Kõigi teiste deposiidisumma muudatuste korral (näiteks, kui kliendi tellimust muudetakse), luuakse eelnevalt loodud ettemaksuarvele kreeditarve ning luuakse ja sisestatakse uus ettemaksuarve parandatud summaga.</span><span class="sxs-lookup"><span data-stu-id="816ed-115">For all other changes to the deposit amount (for example, if a customer order is edited), a credit note is created for the advance invoice that was previously generated, and a new advance invoice is generated and posted for the corrected amount.</span></span>
- <span data-ttu-id="816ed-116">Seotud ettemaksuarvetega müügitellimuse tühistamine.</span><span class="sxs-lookup"><span data-stu-id="816ed-116">Cancel a sales order that has linked advance invoices.</span></span> <span data-ttu-id="816ed-117">Sellisel juhul luuakse ettemaksuarvele kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="816ed-117">In this case, a credit note is created for the advance invoice.</span></span>
- <span data-ttu-id="816ed-118">Ettemaksuarvetega seotud müügitellimuse arve sisestamine.</span><span class="sxs-lookup"><span data-stu-id="816ed-118">Post a sales order invoice that has linked advance invoices.</span></span> <span data-ttu-id="816ed-119">Müügiarve tühistatakse müügitellimusega seotud ettemaksuarve summas.</span><span class="sxs-lookup"><span data-stu-id="816ed-119">The advance invoice that is linked to a sales order is reversed for the amount of the sales invoice.</span></span> <span data-ttu-id="816ed-120">Esialgse ettemaksuarve kanded tasakaalustatakse ettemaksuarve tühistamise kannetega.</span><span class="sxs-lookup"><span data-stu-id="816ed-120">The advance invoice transactions are settled with advance invoice reversal transactions.</span></span>

## <a name="set-up-advance-invoices"></a><span data-ttu-id="816ed-121">Ettemaksuarvete seadistamine</span><span class="sxs-lookup"><span data-stu-id="816ed-121">Set up advance invoices</span></span>

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a><span data-ttu-id="816ed-122">Ettemaksuarvete loomise funktsionaalsuse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="816ed-122">Turn on the functionality for creating advance invoices</span></span>

1. <span data-ttu-id="816ed-123">Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="816ed-123">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span>
2. <span data-ttu-id="816ed-124">Seadistage **Tellimus** kiirkaardi **Klienditellimused** vahekaardi suvand **Deposiidi ettemaksuarve koostamine** **Jah** peale.</span><span class="sxs-lookup"><span data-stu-id="816ed-124">On the **Customer orders** tab, on the **Order** FastTab, set the **Create advance invoice for deposit** option to **Yes**.</span></span>

### <a name="define-the-parameters-for-posting-advance-invoices"></a><span data-ttu-id="816ed-125">Ettemaksuarvete sisestamise parameetrite määramine.</span><span class="sxs-lookup"><span data-stu-id="816ed-125">Define the parameters for posting advance invoices</span></span>

1. <span data-ttu-id="816ed-126">Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="816ed-126">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="816ed-127">Seadistage **Ettemaksuarve** kiirkaardi **Uuendused** vahekaardil **Sisestusreeglid**, **Käibemaksugrupp**, ja **Kauba käibemaksugrupp** väljad.</span><span class="sxs-lookup"><span data-stu-id="816ed-127">On the **Updates** tab, on the **Advance invoice** FastTab, set the **Posting profile**, **Sales tax group**, and **Item sales tax group** fields.</span></span> <span data-ttu-id="816ed-128">Kui need väljad on õigesti seadistatud, sisestatakse ettemaksuarve.</span><span class="sxs-lookup"><span data-stu-id="816ed-128">If these fields are set correctly, the advance invoice will be posted.</span></span> <span data-ttu-id="816ed-129">Kui need väljad ei ole seadistatud, ettemaksuarveid ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="816ed-129">If these fields aren't set, advance invoices won't be posted.</span></span>

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a><span data-ttu-id="816ed-130">Lülitage välja käibemaksu sisestamine ettemaksu töölehekandele</span><span class="sxs-lookup"><span data-stu-id="816ed-130">Turn off posting of the Sales tax on prepayment journal voucher</span></span>

<span data-ttu-id="816ed-131">Ettemaksu töölehekande käibemaksu ei sisestata, kui ettemaksuarve sisestamine on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="816ed-131">The Sales tax on prepayment journal voucher must not be posted if advance invoice posting is turned on.</span></span> <span data-ttu-id="816ed-132">Selle nõude täitmise kontrollimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="816ed-132">To verify that this requirement is met, follow these steps.</span></span>

1. <span data-ttu-id="816ed-133">Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="816ed-133">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="816ed-134">Veenduge, et **Makse** kiirkaardi **Pearaamat ja käibemaks** vahekaardil on järgmised väljad kas tühjad või seadistatud **Ei** peale:</span><span class="sxs-lookup"><span data-stu-id="816ed-134">On the **Ledger and sales tax** tab, on the **Payment** FastTab, make sure that the following fields are blank or set to **No**:</span></span>

    - <span data-ttu-id="816ed-135">Ettemaksu töölehekande käibemaks</span><span class="sxs-lookup"><span data-stu-id="816ed-135">Sales tax on prepayment journal voucher</span></span>
    - <span data-ttu-id="816ed-136">Sisestusreeglid ettemaksu töölehekandega</span><span class="sxs-lookup"><span data-stu-id="816ed-136">Posting profile with prepayment journal voucher</span></span>
    - <span data-ttu-id="816ed-137">Ettemakse maksugrupp</span><span class="sxs-lookup"><span data-stu-id="816ed-137">Tax group for prepayment</span></span>
    - <span data-ttu-id="816ed-138">Kauba käibemaksugrupp</span><span class="sxs-lookup"><span data-stu-id="816ed-138">Item Sales tax group</span></span>

## <a name="print-advance-invoices"></a><span data-ttu-id="816ed-139">Ettemaksuarvete printimine</span><span class="sxs-lookup"><span data-stu-id="816ed-139">Print advance invoices</span></span>

<span data-ttu-id="816ed-140">Ettemaksuarveid saate printida kassast Microsoft Windowsi printeriga, mis on riistvarajaamaga ühendatud.</span><span class="sxs-lookup"><span data-stu-id="816ed-140">You can print advance invoices from POS on a Microsoft Windows printer that is connected to the hardware station.</span></span> <span data-ttu-id="816ed-141">Kassast ettemaksuarvete printimiseks on kaks võimalust:</span><span class="sxs-lookup"><span data-stu-id="816ed-141">There are two options for printing an advance invoice from POS:</span></span>

- <span data-ttu-id="816ed-142">**Printige ettemaksuarve pärast kassas kande lõpetamist.**</span><span class="sxs-lookup"><span data-stu-id="816ed-142">**Print an advance invoice after a transaction is concluded in POS.**</span></span> <span data-ttu-id="816ed-143">See suvand kuvatakse automaatselt, kui ettemaksuarve on loodud ja Windowsi printer on õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="816ed-143">This option occurs automatically if an advance invoice was generated and a Windows printer was correctly set up.</span></span> <span data-ttu-id="816ed-144">Sel juhul prinditakse ainult viimane klienditellimusega seotud ettemaksuarve.</span><span class="sxs-lookup"><span data-stu-id="816ed-144">In this case, only the last advance invoice that is linked to the customer order is printed.</span></span>
- <span data-ttu-id="816ed-145">**Ettemaksuarve töölehelt uuesti printimine.**</span><span class="sxs-lookup"><span data-stu-id="816ed-145">**Reprint an advance invoice from the transaction journal.**</span></span> <span data-ttu-id="816ed-146">Valige töölehtede avamiseks **Näita töölehte**, leidke klienditellimus ja seejärel valige **Prindi ettemaksuarve**.</span><span class="sxs-lookup"><span data-stu-id="816ed-146">Select **Show journal** to open the transactions journal, find the customer order, and then select **Print Advance invoice**.</span></span> <span data-ttu-id="816ed-147">Sel juhul prinditakse kõik kliendi tellimusega seotud ettemaksuarved.</span><span class="sxs-lookup"><span data-stu-id="816ed-147">In this case, all advance invoices that are linked to the customer order are printed.</span></span>

### <a name="set-up-a-windows-printer"></a><span data-ttu-id="816ed-148">Windowsi printeri seadistamine</span><span class="sxs-lookup"><span data-stu-id="816ed-148">Set up a Windows printer</span></span>

<span data-ttu-id="816ed-149">Riistvarajaamaga ühendatud Windowsi printeriga dokumentide kassast printimise võimaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="816ed-149">Follow these steps to enable documents to be printed from POS on a Windows printer that is connected to the hardware station.</span></span>

1. <span data-ttu-id="816ed-150">Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="816ed-150">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
2. <span data-ttu-id="816ed-151">Valige riistvaraprofiil, mis on seotud selle kauplusega, kus printerit kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="816ed-151">Select a hardware profile that is related to the store where the printer is used.</span></span>
3. <span data-ttu-id="816ed-152">Uuendage seaded kas jaotises **Printer** või jaotises **Printer 2**:</span><span class="sxs-lookup"><span data-stu-id="816ed-152">In either the **Printer** section or the **Printer 2** section, update the settings:</span></span>

    - <span data-ttu-id="816ed-153">Väljal **Printer** valige **Windowsi draiver**.</span><span class="sxs-lookup"><span data-stu-id="816ed-153">In the **Printer** field, select **Windows driver**.</span></span>
    - <span data-ttu-id="816ed-154">Sisestage printeri nimi väljale **Seadme nimi**.</span><span class="sxs-lookup"><span data-stu-id="816ed-154">In the **Device name** field, enter the name of the printer.</span></span>

4. <span data-ttu-id="816ed-155">Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="816ed-155">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="816ed-156">Valige töö **1090** ja seejärel **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="816ed-156">Select job **1090**, and then select **Run now**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]