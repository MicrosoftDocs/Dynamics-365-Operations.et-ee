---
title: Projektikulu juurdekasv ostu sissetulekute korral
description: Selles teemas kirjeldatakse, kuidas jälgida ostu sissetulekutest kogunevaid projektikulusid Microsoft Dynamics 365 Financeis.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 615e22234323e2235fba002c50f9ab9c230c021e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827886"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="15e04-103">Projektikulu juurdekasv ostu sissetulekute korral</span><span class="sxs-lookup"><span data-stu-id="15e04-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15e04-104">Selles teemas kirjeldatakse, kuidas jälgida ostu sissetulekutest kogunevaid projektikulusid Microsoft Dynamics 365 Financeis.</span><span class="sxs-lookup"><span data-stu-id="15e04-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="15e04-105">Projekti arved saabuvad sageli kaupade ja teenuste üleandmisest hiljem, millel võib olla märkimisväärne mõju projekti juhtimismõõdikutele (KPI-dele).</span><span class="sxs-lookup"><span data-stu-id="15e04-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="15e04-106">Nende kannete jälgimise võimalus nii finants- kui ka projektiaruannetes on oluline.</span><span class="sxs-lookup"><span data-stu-id="15e04-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="15e04-107">Seda illustreerib järgmine näidisstsenaarium.</span><span class="sxs-lookup"><span data-stu-id="15e04-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="15e04-108">Contoso Consulting on käivitanud uue pilvejuurutusprojekti.</span><span class="sxs-lookup"><span data-stu-id="15e04-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="15e04-109">Luuakse ostutellimus projekti jaoks arvuti ostmiseks.</span><span class="sxs-lookup"><span data-stu-id="15e04-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="15e04-110">Arvuti hind on 1500 $ ja paigaldusteenuste hind 150 $.</span><span class="sxs-lookup"><span data-stu-id="15e04-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="15e04-111">Hankija on arvuti kohale toonud ja paigaldanud, kuid arve pole veel ettevõttesse Contoso Consulting jõudnud.</span><span class="sxs-lookup"><span data-stu-id="15e04-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="15e04-112">Projektijuht soovib näha projekti maksumuse koondsummat 1650 $ enne arve kohaletoimetamist.</span><span class="sxs-lookup"><span data-stu-id="15e04-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="15e04-113">See kulu peaks kajastuma ka ettevõtte kuu lõpu finantsaruannetes.</span><span class="sxs-lookup"><span data-stu-id="15e04-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="15e04-114">Koondkulu tuleb kajastada nii finantstaseme kui ka projekti taseme aruandluses.</span><span class="sxs-lookup"><span data-stu-id="15e04-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="15e04-115">Toote sissetuleku finantsuuendust saab jälgida kauba ja hanke kategooriates.</span><span class="sxs-lookup"><span data-stu-id="15e04-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="15e04-116">Tehke kaupadele lehel **Ostureskontro parameetrid** valik **Sisesta toote sissetulek pearaamatusse**.</span><span class="sxs-lookup"><span data-stu-id="15e04-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="15e04-117">[![Ostureskontro parameetrite leht](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="15e04-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="15e04-118">Hankekategooriate puhul tehke lehel **Kategooria poliitikareegel** valik **Ostmise** poliitikad ja valige siis iga hankekategooria kohta **Kogunev ostukulu vastuvõtmisel**.</span><span class="sxs-lookup"><span data-stu-id="15e04-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="15e04-119">[![Kategooria poliitikareegli leht](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="15e04-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="15e04-120">Toote sissetulekuga seotud kannete sisestamisel kasutatakse kontosid **Arvele kandmata ostukulud** ja **Ostu viitvõlg** jaotises **Sisestamise seadistus**.</span><span class="sxs-lookup"><span data-stu-id="15e04-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="15e04-121">Kasutades sama stsenaariumi, vaatame, kuidas toote sissetuleku sisestamine mõjutab pearaamatu ja projekti andmeid.</span><span class="sxs-lookup"><span data-stu-id="15e04-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="15e04-122">**1. etapp:** looge ja kinnitage uus projekti ostutellimus, mis kajastab arvuti ostu 1500 $ eest ja paigaldusteenuste ostu 150 $ eest.</span><span class="sxs-lookup"><span data-stu-id="15e04-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="15e04-123">[![Uue ostutellimuse loomine](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="15e04-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="15e04-124">Kui ostutellimus on kinnitatud, luuakse projektile kooskõlastatud kulu kanded.</span><span class="sxs-lookup"><span data-stu-id="15e04-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="15e04-125">[![Loodud kanded](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="15e04-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="15e04-126">Kooskõlastatud kulu kannete väljal **Kande päritolu** on määratud väärtus **Ostutellimus**.</span><span class="sxs-lookup"><span data-stu-id="15e04-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="15e04-127">Ostutellimuse koostamine ja kinnitamine ei loo projektile kandeid.</span><span class="sxs-lookup"><span data-stu-id="15e04-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="15e04-128">**2. etapp:** kaubad ja teenused jõuavad kohale ja registreeritakse toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="15e04-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="15e04-129">Toote sissetuleku sisestamisel luuakse kanne ja see sisestatakse pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="15e04-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="15e04-130">Kanne debiteerib ostukulu, arveldamata kulu ja krediteerib ostu juurdekasvukontot.</span><span class="sxs-lookup"><span data-stu-id="15e04-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="15e04-131">[![Kande kanded](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="15e04-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="15e04-132">Toote sissetuleku sisestamisel kasutatakse hankekategooriate ja toodete sisestamise seadistust ning mitte projektikategooriate sisestamise seadistust.</span><span class="sxs-lookup"><span data-stu-id="15e04-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="15e04-133">Ostu viitvõlgade õigeks kajastamiseks tuleb seda seadistust kohandada.</span><span class="sxs-lookup"><span data-stu-id="15e04-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="15e04-134">Hankekategooriat saab lehel **Hankekategooria** projektikategooriatega vastendada.</span><span class="sxs-lookup"><span data-stu-id="15e04-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="15e04-135">[![Hankekategooria leht](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="15e04-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="15e04-136">**3. etapp:** hankija arve mustandi koostamine.</span><span class="sxs-lookup"><span data-stu-id="15e04-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="15e04-137">Toote sissetuleku sisestamine ei mõjuta projekti andmeid.</span><span class="sxs-lookup"><span data-stu-id="15e04-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="15e04-138">Lahendusena võite koostada hankija arve mustandi otse pärast ostukviitungi sisestamist.</span><span class="sxs-lookup"><span data-stu-id="15e04-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="15e04-139">Minge lehele **Ostutellimus** &gt; **Vahekaart Arve** &gt; **Loo** &gt; **Arve**.</span><span class="sxs-lookup"><span data-stu-id="15e04-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="15e04-140">Nii koostatakse ootel arvedokument, mis muudab projekti andmeid.</span><span class="sxs-lookup"><span data-stu-id="15e04-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="15e04-141">Hankija arve mustandi loomisel luuakse ootel projektikanded.</span><span class="sxs-lookup"><span data-stu-id="15e04-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="15e04-142">[![Ootel projektikanded](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="15e04-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="15e04-143">Lehel **Kooskõlastatud kulu** suletakse 1. etapis loodud kirjed ja luuakse uued kirjed, mis kajastavad ootel hankija arvest pärinevat kulu kooskõlastust.</span><span class="sxs-lookup"><span data-stu-id="15e04-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="15e04-144">Kooskõlastatud kulu väljale **Kande päritolu** määratakse väärtus **Hankija arve**.</span><span class="sxs-lookup"><span data-stu-id="15e04-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="15e04-145">[![Kooskõlastatud kulude leht](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="15e04-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="15e04-146">Hankija arve jääb ootel olekusse, kuni saabub tegelik hankija arve.</span><span class="sxs-lookup"><span data-stu-id="15e04-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]