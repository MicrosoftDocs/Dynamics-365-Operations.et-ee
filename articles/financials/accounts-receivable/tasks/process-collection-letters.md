--- 
title: "Märgukirjade töötlemine"
description: "See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 075d0f5dc0c9dc4e46dc92a2da75da9f7a207472
ms.openlocfilehash: 33d9fd62a780ab109474eefa9e322a9c529f9e72
ms.contentlocale: et-ee
ms.lasthandoff: 12/06/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="c5463-103">Märgukirjade töötlemine</span><span class="sxs-lookup"><span data-stu-id="c5463-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="c5463-104">See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist.</span><span class="sxs-lookup"><span data-stu-id="c5463-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="c5463-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="c5463-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="c5463-106">Märgukirjaseeria häälestamine sisestusreeglis</span><span class="sxs-lookup"><span data-stu-id="c5463-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="c5463-107">Avage **Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid**.</span><span class="sxs-lookup"><span data-stu-id="c5463-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="c5463-108">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="c5463-108">Click **Edit**.</span></span>
3. <span data-ttu-id="c5463-109">Valige ripploendist märgukirjaseeria.</span><span class="sxs-lookup"><span data-stu-id="c5463-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="c5463-110">Kui te ei soovi luua kannete jaoks märgukirju selle sisestusreegliga, jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="c5463-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="c5463-111">Tabeli piirangu vahekaardil saate laiendada seda, kuidas sissenõudekirju töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="c5463-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="c5463-112">Kui väli on seatud olekusse **Jah**, luuakse märgukirjad selle sisestusreegli jaoks.</span><span class="sxs-lookup"><span data-stu-id="c5463-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="c5463-113">Sissenõude märgukirjade loomine</span><span class="sxs-lookup"><span data-stu-id="c5463-113">Create collection letters</span></span>
1. <span data-ttu-id="c5463-114">Avage jaotis **Krediit ja sissenõuded > Märgukiri > Märgukirjade loomine**.</span><span class="sxs-lookup"><span data-stu-id="c5463-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="c5463-115">Valige kandetüübid, mille jaoks märgukirjad luuakse.</span><span class="sxs-lookup"><span data-stu-id="c5463-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="c5463-116">Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.</span><span class="sxs-lookup"><span data-stu-id="c5463-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="c5463-117">Valige üks suvand väljalt **Märgukiri**.</span><span class="sxs-lookup"><span data-stu-id="c5463-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="c5463-118">Sisestage märgukirja kuupäev.</span><span class="sxs-lookup"><span data-stu-id="c5463-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="c5463-119">Valige sisestusreegel, kui määrasite suvandi **Kasuta sisestusreegleid** olekusse **Vali**.</span><span class="sxs-lookup"><span data-stu-id="c5463-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="c5463-120">Sisestusreegli jaoks kaks võimalust:</span><span class="sxs-lookup"><span data-stu-id="c5463-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="c5463-121">**Konto** – kasutab iga viivisearve kohta kliendi kontole määratud sisestusreeglit.</span><span class="sxs-lookup"><span data-stu-id="c5463-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="c5463-122">**Vali** – kasutage sisestusreeglit, mille valite väljal **Sisestusreegel**.</span><span class="sxs-lookup"><span data-stu-id="c5463-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="c5463-123">Jaotise kaasamiseks laiendage valikut **Kirjed**.</span><span class="sxs-lookup"><span data-stu-id="c5463-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="c5463-124">Klõpsake käsku **Filtreeri**.</span><span class="sxs-lookup"><span data-stu-id="c5463-124">Click **Filter**.</span></span>
7. <span data-ttu-id="c5463-125">Sisestage kliendi ID väljale **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="c5463-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="c5463-126">Sisestage näiteks US-001.</span><span class="sxs-lookup"><span data-stu-id="c5463-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="c5463-127">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5463-127">Click **OK**.</span></span>
9. <span data-ttu-id="c5463-128">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5463-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="c5463-129">Märgukirjade printimine</span><span class="sxs-lookup"><span data-stu-id="c5463-129">Print collection letters</span></span>
1. <span data-ttu-id="c5463-130">Avage jaotis **Krediit ja sissenõuded > Märgukiri > Märgukirjade ülevaatamine ja töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="c5463-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="c5463-131">Valige väljal **Olek** suvand **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="c5463-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="c5463-132">Valige väljal **Prinditud** suvand **Printimata**.</span><span class="sxs-lookup"><span data-stu-id="c5463-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="c5463-133">Klõpsake **Prindi**.</span><span class="sxs-lookup"><span data-stu-id="c5463-133">Click **Print**.</span></span>
5. <span data-ttu-id="c5463-134">Klõpsake suvandit **Märgukirja märkus**.</span><span class="sxs-lookup"><span data-stu-id="c5463-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="c5463-135">Jaotise kaasamiseks laiendage valikut **Kirjed**.</span><span class="sxs-lookup"><span data-stu-id="c5463-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="c5463-136">Sisestage sisestamiste äralõikekuupäev.</span><span class="sxs-lookup"><span data-stu-id="c5463-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="c5463-137">Märgukirja printimiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5463-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="c5463-138">Märgukirja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="c5463-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="c5463-139">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="c5463-139">Click **Post**.</span></span>
   2. <span data-ttu-id="c5463-140">Sisestage märgukirja sisestuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="c5463-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="c5463-141">Jaotise kaasamiseks laiendage valikut **Kirjed**.</span><span class="sxs-lookup"><span data-stu-id="c5463-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="c5463-142">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5463-142">Click **OK**.</span></span>
   5. <span data-ttu-id="c5463-143">Valige väljal **Olek** suvand **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="c5463-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="c5463-144">Valige suvand väljal **Prinditud**.</span><span class="sxs-lookup"><span data-stu-id="c5463-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="c5463-145">Märgukirjade kontrollimine kliendi tasemel</span><span class="sxs-lookup"><span data-stu-id="c5463-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="c5463-146">Saate ka seadistada märgukirjad kliendi tasemel nii, et iga kande märgukirjakoodi jälgitakse, kuid märgukirja töötlemine põhineb ühe märgukirja tasemel, mis on kliendi jaoks talletatud.</span><span class="sxs-lookup"><span data-stu-id="c5463-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="c5463-147">Üks märgukiri sisaldab kõiki kandeid, mis on kliendi tähtaja ületanud.</span><span class="sxs-lookup"><span data-stu-id="c5463-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="c5463-148">Ajapikenduse päeva jälgitakse nüüd kliendi tasemel, järgmist märgukirja ei saadeta enne ajapikenduse päevade arvu möödumist enne järgmise märgukirja saatmise tähtaega, kuigi pärast viimase märgukirja saatmist on kannete tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="c5463-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="c5463-149">See suvand vähendab kliendi kohta saadetavate märgukirjade arvu.</span><span class="sxs-lookup"><span data-stu-id="c5463-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="c5463-150">Märgukirjade kontrollimise seadistamine kliendi tasemel</span><span class="sxs-lookup"><span data-stu-id="c5463-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="c5463-151">Avage **Krediit ja kollektsioonid > Seadistus > Müügireskontro parameetrid** ja klõpsake vahekaardil **Sissenõuded**.</span><span class="sxs-lookup"><span data-stu-id="c5463-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="c5463-152">Muutke suvandi **Loomine märgukirja kohta** väärtuseks **Klient**.</span><span class="sxs-lookup"><span data-stu-id="c5463-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="c5463-153">Avage jaotis **Krediit ja sissenõuded > Märgukiri > Märgukirjade ülevaatamine ja töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="c5463-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="c5463-154">Kõikide tähtaja ületanud kannete kohta luuakse kliendile ainult üks märgukiri.</span><span class="sxs-lookup"><span data-stu-id="c5463-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="c5463-155">Eira märgukirja koodi arvutamisel makseid ja kreeditarveid</span><span class="sxs-lookup"><span data-stu-id="c5463-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="c5463-156">Kui kaasate maksed ja kreeditarved märgukirjas kaasatavatesse kannetesse, võivad maksed või kreeditarved käivitada märgukirja.</span><span class="sxs-lookup"><span data-stu-id="c5463-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="c5463-157">Saate määrata, kuidas maksed ja kreeditarved kontrollivad märgukirja koodi, muutes väärtust **Ignoreerida maksete ja kreeditarvete märgukirjakoodi arvutamisel** parameetrit.</span><span class="sxs-lookup"><span data-stu-id="c5463-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="c5463-158">Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c5463-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="c5463-159">Avage **Krediit ja kollektsioonid > Seadistus > Müügireskontro parameetrid** ja klõpsake vahekaardil **Sissenõuded**.</span><span class="sxs-lookup"><span data-stu-id="c5463-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="c5463-160">Muutke suvandi **Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="c5463-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

