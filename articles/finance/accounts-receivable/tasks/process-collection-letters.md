---
title: Märgukirjade töötlemine
description: See teema kirjeldab märgukirjade loomist, printimist ja sisestamist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177388"
---
# <a name="process-collection-letters"></a><span data-ttu-id="a95c8-103">Märgukirjade töötlemine</span><span class="sxs-lookup"><span data-stu-id="a95c8-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a95c8-104">See teema kirjeldab märgukirjade loomist, printimist ja sisestamist.</span><span class="sxs-lookup"><span data-stu-id="a95c8-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="a95c8-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="a95c8-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="a95c8-106">Märgukirjaseeria häälestamine sisestusreeglis</span><span class="sxs-lookup"><span data-stu-id="a95c8-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="a95c8-107">Minge **Navigeerimispaan > Moodulid > Kreedit ja sissenõuded > Häälestus > Kliendi postitusprofiil**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="a95c8-108">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-108">Click **Edit**.</span></span>
3. <span data-ttu-id="a95c8-109">Valige ripploendist märgukirjaseeria.</span><span class="sxs-lookup"><span data-stu-id="a95c8-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="a95c8-110">Kui te ei soovi luua kannete jaoks märgukirju selle sisestusreegliga, jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="a95c8-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="a95c8-111">Laiendage **Tabeli piirangut**, et muuta viisi, kuidas sissenõudekirju töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="a95c8-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="a95c8-112">Kui väli on seatud olekusse **Jah**, luuakse märgukirjad selle sisestusreegli jaoks.</span><span class="sxs-lookup"><span data-stu-id="a95c8-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="a95c8-113">Sissenõude märgukirjade loomine</span><span class="sxs-lookup"><span data-stu-id="a95c8-113">Create collection letters</span></span>
1. <span data-ttu-id="a95c8-114">Minge **Navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Sissenõudekiri > Sissenõudekirja loomine**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="a95c8-115">Valige kandetüübid, mille jaoks märgukirjad luuakse.</span><span class="sxs-lookup"><span data-stu-id="a95c8-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="a95c8-116">Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.</span><span class="sxs-lookup"><span data-stu-id="a95c8-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="a95c8-117">Valige üks suvand väljalt **Märgukiri**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="a95c8-118">Sisestage väljale **Sissenõudekirja kuupäev** sissenõudekirja kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a95c8-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="a95c8-119">Valige sisestusreegel, kui määrasite suvandi **Kasuta sisestusreegleid** olekusse **Vali**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="a95c8-120">Sisestusreegli jaoks kaks võimalust:</span><span class="sxs-lookup"><span data-stu-id="a95c8-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="a95c8-121">**Konto** – kasutab iga viivisearve kohta kliendi kontole määratud sisestusreeglit.</span><span class="sxs-lookup"><span data-stu-id="a95c8-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="a95c8-122">**Vali** – kasutage sisestusreeglit, mille valite väljal **Sisestusreegel**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="a95c8-123">Jaotise kaasamiseks laiendage valikut **Kirjed**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="a95c8-124">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-124">Select **Filter**.</span></span>
8. <span data-ttu-id="a95c8-125">Sisestage kliendi ID väljale **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="a95c8-126">Sisestage näiteks US-001.</span><span class="sxs-lookup"><span data-stu-id="a95c8-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="a95c8-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-127">Select **OK**.</span></span>
10. <span data-ttu-id="a95c8-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="a95c8-129">Märgukirjade printimine</span><span class="sxs-lookup"><span data-stu-id="a95c8-129">Print collection letters</span></span>
1. <span data-ttu-id="a95c8-130">Minge **navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Sissenõudekiri > Sissenõudekirjade ülevaade ja töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="a95c8-131">Valige väljal **Olek** suvand **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="a95c8-132">Valige väljal **Prinditud** suvand **Printimata**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="a95c8-133">Valige **Prindi**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-133">Select **Print**.</span></span>
5. <span data-ttu-id="a95c8-134">Valige  **Sissenõudekiri**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="a95c8-135">Sisestage moodulisse **Parameetrid** sisestuste sulgemiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a95c8-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="a95c8-136">Laiendage moodulit **Kirjed kaasamiseks** ja sisestage sissenõudekirja märkme üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="a95c8-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="a95c8-137">Sissenõudekirja printimiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="a95c8-138">Märgukirja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="a95c8-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="a95c8-139">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-139">Select **Post**.</span></span>
    1. <span data-ttu-id="a95c8-140">Sisestage märgukirja sisestuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a95c8-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="a95c8-141">Jaotise kaasamiseks laiendage valikut **Kirjed**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="a95c8-142">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-142">Select **OK**.</span></span>
    1. <span data-ttu-id="a95c8-143">Valige väljal **Olek** suvand **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="a95c8-144">Valige suvand väljal **Prinditud**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="a95c8-145">Märgukirjade kontrollimine kliendi tasemel</span><span class="sxs-lookup"><span data-stu-id="a95c8-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="a95c8-146">Saate ka seadistada märgukirjad kliendi tasemel nii, et iga kande märgukirjakoodi jälgitakse, kuid märgukirja töötlemine põhineb ühe märgukirja tasemel, mis on kliendi jaoks talletatud.</span><span class="sxs-lookup"><span data-stu-id="a95c8-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="a95c8-147">Üks märgukiri sisaldab kõiki kandeid, mis on kliendi tähtaja ületanud.</span><span class="sxs-lookup"><span data-stu-id="a95c8-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="a95c8-148">Ajapikenduse päeva jälgitakse nüüd kliendi tasemel, järgmist märgukirja ei saadeta enne ajapikenduse päevade arvu möödumist enne järgmise märgukirja saatmise tähtaega, kuigi pärast viimase märgukirja saatmist on kannete tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="a95c8-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="a95c8-149">See suvand vähendab kliendi kohta saadetavate märgukirjade arvu.</span><span class="sxs-lookup"><span data-stu-id="a95c8-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="a95c8-150">Märgukirjade kontrollimise seadistamine kliendi tasemel</span><span class="sxs-lookup"><span data-stu-id="a95c8-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="a95c8-151">Minge **Navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Seadistus > Müügireskontro parameetrid** ja klõpsake vahekaardil **Sissenõuded**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-151">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="a95c8-152">Muutke suvandi **Loomine märgukirja kohta** väärtuseks **Klient**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="a95c8-153">Minge **navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Sissenõudekiri > Sissenõudekirjade ülevaade ja töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-153">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="a95c8-154">Kõikide tähtaja ületanud kannete kohta luuakse kliendile ainult üks märgukiri.</span><span class="sxs-lookup"><span data-stu-id="a95c8-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="a95c8-155">Eira märgukirja koodi arvutamisel makseid ja kreeditarveid</span><span class="sxs-lookup"><span data-stu-id="a95c8-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="a95c8-156">Kui kaasate maksed ja kreeditarved märgukirjas kaasatavatesse kannetesse, võivad maksed või kreeditarved käivitada märgukirja.</span><span class="sxs-lookup"><span data-stu-id="a95c8-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="a95c8-157">Saate määrata, kuidas maksed ja kreeditarved kontrollivad märgukirja koodi, muutes väärtust **Ignoreerida maksete ja kreeditarvete märgukirjakoodi arvutamisel** parameetrit.</span><span class="sxs-lookup"><span data-stu-id="a95c8-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="a95c8-158">Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a95c8-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="a95c8-159">Minge **Navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Seadistus > Müügireskontro parameetrid** ja klõpsake vahekaardil **Sissenõuded**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-159">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="a95c8-160">Muutke suvandi **Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a95c8-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>