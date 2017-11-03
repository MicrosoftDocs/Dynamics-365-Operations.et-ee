---
title: Projektikulu juurdekasv ostu sissetulekute korral
description: "Selles teemas kirjeldatakse, kuidas ostu sissetulekutest kogunevaid projektikulusid saab Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis jälgida."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0b54d48d5734cdbfba4a5de4356bff37c0a8d2d3
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="c4913-103">Projektikulu juurdekasv ostu sissetulekute korral</span><span class="sxs-lookup"><span data-stu-id="c4913-103">Project cost accrual on purchase receipts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c4913-104">Selles teemas kirjeldatakse, kuidas ostu sissetulekutest kogunevaid projektikulusid saab Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis jälgida.</span><span class="sxs-lookup"><span data-stu-id="c4913-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="c4913-105">Projekti arved saabuvad sageli kaupade ja teenuste üleandmisest hiljem, millel võib olla märkimisväärne mõju projekti juhtimismõõdikutele (KPI-dele).</span><span class="sxs-lookup"><span data-stu-id="c4913-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="c4913-106">Nende kannete jälgimise võimalus nii finants- kui ka projektiaruannetes on oluline.</span><span class="sxs-lookup"><span data-stu-id="c4913-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="c4913-107">Seda illustreerib järgmine näidisstsenaarium.</span><span class="sxs-lookup"><span data-stu-id="c4913-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="c4913-108">Contoso Consulting on käivitanud uue pilvejuurutusprojekti.</span><span class="sxs-lookup"><span data-stu-id="c4913-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="c4913-109">Luuakse ostutellimus projekti jaoks arvuti ostmiseks.</span><span class="sxs-lookup"><span data-stu-id="c4913-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="c4913-110">Arvuti hind on 1500 $ ja paigaldusteenuste hind 150 $.</span><span class="sxs-lookup"><span data-stu-id="c4913-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="c4913-111">Hankija on arvuti kohale toonud ja paigaldanud, kuid arve pole veel ettevõttesse Contoso Consulting jõudnud.</span><span class="sxs-lookup"><span data-stu-id="c4913-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="c4913-112">Projektijuht soovib näha projekti maksumuse koondsummat 1650 $ enne arve kohaletoimetamist.</span><span class="sxs-lookup"><span data-stu-id="c4913-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="c4913-113">See kulu peaks kajastuma ka ettevõtte kuu lõpu finantsaruannetes.</span><span class="sxs-lookup"><span data-stu-id="c4913-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="c4913-114">Koondkulu tuleb kajastada nii finantstaseme kui ka projekti taseme aruandluses.</span><span class="sxs-lookup"><span data-stu-id="c4913-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="c4913-115">Finance and Operationsis saab toote sissetuleku finantsuuendus jälgida kauba ja hanke kategooriates.</span><span class="sxs-lookup"><span data-stu-id="c4913-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="c4913-116">Tehke kaupadele lehel **Ostureskontro parameetrid** valik **Sisesta toote sissetulek pearaamatusse**.</span><span class="sxs-lookup"><span data-stu-id="c4913-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="c4913-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="c4913-118">Hankekategooriate puhul tehke lehel **Kategooria poliitikareegel** valik **Ostmise** poliitikad ja valige siis iga hankekategooria kohta **Kogunev ostukulu vastuvõtmisel**.</span><span class="sxs-lookup"><span data-stu-id="c4913-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="c4913-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="c4913-120">Toote sissetulekuga seotud kannete sisestamisel kasutatakse kontosid **Arvele kandmata ostukulud** ja **Ostu viitvõlg** jaotises **Sisestamise seadistus**.</span><span class="sxs-lookup"><span data-stu-id="c4913-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="c4913-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="c4913-122">Kasutades sama stsenaariumi, vaatame, kuidas toote sissetuleku sisestamine mõjutab pearaamatu ja projekti andmeid.</span><span class="sxs-lookup"><span data-stu-id="c4913-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="c4913-123">**1. etapp:** looge ja kinnitage uus projekti ostutellimus, mis kajastab arvuti ostu 1500 $ eest ja paigaldusteenuste ostu 150 $ eest.</span><span class="sxs-lookup"><span data-stu-id="c4913-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="c4913-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="c4913-125">Kui ostutellimus on kinnitatud, luuakse projektile kooskõlastatud kulu kanded.</span><span class="sxs-lookup"><span data-stu-id="c4913-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="c4913-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="c4913-127">Kooskõlastatud kulu kannete väljal **Kande päritolu** on määratud väärtus **Ostutellimus**.</span><span class="sxs-lookup"><span data-stu-id="c4913-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="c4913-128">Ostutellimuse koostamine ja kinnitamine ei loo projektile kandeid.</span><span class="sxs-lookup"><span data-stu-id="c4913-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="c4913-129">**2. etapp:** kaubad ja teenused jõuavad kohale ja registreeritakse toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="c4913-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="c4913-130">Toote sissetuleku sisestamisel luuakse kanne ja see sisestatakse pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="c4913-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="c4913-131">Kanne debiteerib ostukulu, arveldamata kulu ja krediteerib ostu juurdekasvukontot.</span><span class="sxs-lookup"><span data-stu-id="c4913-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="c4913-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c4913-133">Toote sissetuleku sisestamisel kasutatakse hankekategooriate ja toodete sisestamise seadistust ning mitte projektikategooriate sisestamise seadistust.</span><span class="sxs-lookup"><span data-stu-id="c4913-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="c4913-134">Ostu viitvõlgade õigeks kajastamiseks tuleb seda seadistust kohandada.</span><span class="sxs-lookup"><span data-stu-id="c4913-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="c4913-135">Hankekategooriat saab lehel **Hankekategooria** projektikategooriatega vastendada.</span><span class="sxs-lookup"><span data-stu-id="c4913-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="c4913-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="c4913-137">**3. etapp:** hankija arve mustandi koostamine.</span><span class="sxs-lookup"><span data-stu-id="c4913-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="c4913-138">Finance and Operationsis ei mõjuta toote sissetuleku sisestamine projekti andmeid.</span><span class="sxs-lookup"><span data-stu-id="c4913-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="c4913-139">Lahendusena võite koostada hankija arve mustandi otse pärast ostukviitungi sisestamist.</span><span class="sxs-lookup"><span data-stu-id="c4913-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="c4913-140">Minge lehele **Ostutellimus** &gt; **Vahekaart Arve** &gt; **Loo** &gt; **Arve**.</span><span class="sxs-lookup"><span data-stu-id="c4913-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="c4913-141">Nii koostatakse ootel arvedokument, mis muudab projekti andmeid.</span><span class="sxs-lookup"><span data-stu-id="c4913-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="c4913-142">Hankija arve mustandi loomisel luuakse ootel projektikanded.</span><span class="sxs-lookup"><span data-stu-id="c4913-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="c4913-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="c4913-144">Lehel **Kooskõlastatud kulu** suletakse 1. etapis loodud kirjed ja luuakse uued kirjed, mis kajastavad ootel hankija arvest pärinevat kulu kooskõlastust.</span><span class="sxs-lookup"><span data-stu-id="c4913-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="c4913-145">Kooskõlastatud kulu väljale **Kande päritolu** määratakse väärtus **Hankija arve**.</span><span class="sxs-lookup"><span data-stu-id="c4913-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="c4913-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="c4913-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="c4913-147">Hankija arve jääb ootel olekusse, kuni saabub tegelik hankija arve.</span><span class="sxs-lookup"><span data-stu-id="c4913-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>




