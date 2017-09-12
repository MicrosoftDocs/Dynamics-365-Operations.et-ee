--- 
title: "Intressi töötlemine"
description: See protseduur kirjeldab viivisearvete loomist, printimist ja sisestamist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="process-interest"></a><span data-ttu-id="58b53-103">Intressi töötlemine</span><span class="sxs-lookup"><span data-stu-id="58b53-103">Process interest</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58b53-104">See protseduur kirjeldab viivisearvete loomist, printimist ja sisestamist.</span><span class="sxs-lookup"><span data-stu-id="58b53-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="58b53-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="58b53-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="58b53-106">Viivise seadistamine sisestusreeglis</span><span class="sxs-lookup"><span data-stu-id="58b53-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="58b53-107">Avage Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="58b53-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="58b53-108">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="58b53-108">Click Edit.</span></span>
    * <span data-ttu-id="58b53-109">Valige ripploendist viivise kood.</span><span class="sxs-lookup"><span data-stu-id="58b53-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="58b53-110">Kui te ei soovi, et viivist arvutataks kannete puhul selle sisestusreegliga, jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="58b53-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="58b53-111">Piirangu vahekaardil Tabel saate muuta seda, kuidas viivist töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="58b53-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="58b53-112">Kui väli on seatud olekusse Jah, arvutatakse viivist selle sisestusreegli puhul.</span><span class="sxs-lookup"><span data-stu-id="58b53-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="58b53-113">Arvuta intress</span><span class="sxs-lookup"><span data-stu-id="58b53-113">Calculate interest</span></span>
1. <span data-ttu-id="58b53-114">Avage Krediit ja sissenõuded > Intress > Viivisearvete loomine.</span><span class="sxs-lookup"><span data-stu-id="58b53-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="58b53-115">Valige kandetüübid, mille puhul viivist arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="58b53-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="58b53-116">Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.</span><span class="sxs-lookup"><span data-stu-id="58b53-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="58b53-117">Viivise valimisel arvutate viivisearve viivise.</span><span class="sxs-lookup"><span data-stu-id="58b53-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="58b53-118">Võite soovida enne nende kannete kaasamist kontrollida viivisearve viivise arvutamise seadusi.</span><span class="sxs-lookup"><span data-stu-id="58b53-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="58b53-119">Viivist arvutatakse alates sellest kuupäevast kuni sihtkuupäevani.</span><span class="sxs-lookup"><span data-stu-id="58b53-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="58b53-120">Kui te alguskuupäeva ei täpsusta, tühistatakse kõik sisestamata viivisearved ja viivis arvutatakse kande alguskuupäevast alates ümber.</span><span class="sxs-lookup"><span data-stu-id="58b53-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="58b53-121">Sisestage viivisearve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="58b53-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="58b53-122">Saadaval on kolm sisestusreeglit: Konto – kasutage iga viivisearve puhul kliendi kontole määratud sisestusreeglit.</span><span class="sxs-lookup"><span data-stu-id="58b53-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="58b53-123">Vali – kasutage sisestusreeglit, mille valite väljal Sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="58b53-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="58b53-124">Kanne – kasutage eraldi sisestusprofiile kannetest, milles arvutatakse viivis iga viivisearve jaoks.</span><span class="sxs-lookup"><span data-stu-id="58b53-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="58b53-125">Kanded, millele ei ole sisestusprofiili määratud, kasutavad sisestusprofiili, mis on määratletud vormi Müügireskontro parameetrid alal Pearaamat ja käibemaks.</span><span class="sxs-lookup"><span data-stu-id="58b53-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="58b53-126">Valige sisestusreegel siin, kui määrasite suvandi Kasuta sisestusreegleid olekusse Vali.</span><span class="sxs-lookup"><span data-stu-id="58b53-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="58b53-127">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="58b53-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="58b53-128">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="58b53-128">Click Filter.</span></span>
5. <span data-ttu-id="58b53-129">Sisestage kliendi ID väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="58b53-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="58b53-130">Näiteks sisestage US-001.</span><span class="sxs-lookup"><span data-stu-id="58b53-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="58b53-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="58b53-131">Click OK.</span></span>
7. <span data-ttu-id="58b53-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="58b53-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="58b53-133">Viivisearvete printimine</span><span class="sxs-lookup"><span data-stu-id="58b53-133">Print interest notes</span></span>
1. <span data-ttu-id="58b53-134">Avage Krediit ja sissenõuded > Intress > Viivisearvete ülevaade ja töötlus.</span><span class="sxs-lookup"><span data-stu-id="58b53-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="58b53-135">Valige väljal Olek suvand Loodud.</span><span class="sxs-lookup"><span data-stu-id="58b53-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="58b53-136">Valige väljal Prinditud suvand Printimata.</span><span class="sxs-lookup"><span data-stu-id="58b53-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="58b53-137">Klõpsake Prindi.</span><span class="sxs-lookup"><span data-stu-id="58b53-137">Click Print.</span></span>
5. <span data-ttu-id="58b53-138">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="58b53-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="58b53-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="58b53-139">Click OK.</span></span>
7. <span data-ttu-id="58b53-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="58b53-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="58b53-141">Viivisearve sisestamine</span><span class="sxs-lookup"><span data-stu-id="58b53-141">Post the interest note</span></span>
1. <span data-ttu-id="58b53-142">Valige viivisearve, mis on sisestamiseks valmis (olek on loodud).</span><span class="sxs-lookup"><span data-stu-id="58b53-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="58b53-143">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="58b53-143">Click Post.</span></span>
3. <span data-ttu-id="58b53-144">Sisestage viivisearve sisestamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="58b53-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="58b53-145">Iga viivisearve kohta pearaamatukande loomiseks valige suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="58b53-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="58b53-146">Valiku Jah mittemärkimisel summeeritakse kliendi kõigi viivisearvete viivised ja sisestatakse pearaamatusse ühe kandega.</span><span class="sxs-lookup"><span data-stu-id="58b53-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="58b53-147">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="58b53-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="58b53-148">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="58b53-148">Click OK.</span></span>
6. <span data-ttu-id="58b53-149">Valige väljal Olek suvand Sisestatud.</span><span class="sxs-lookup"><span data-stu-id="58b53-149">In the Status field, select 'Posted'.</span></span>


