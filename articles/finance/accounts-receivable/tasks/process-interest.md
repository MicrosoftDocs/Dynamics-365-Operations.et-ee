---
title: Intressi töötlemine
description: See protseduur kirjeldab viivisearvete loomist, printimist ja sisestamist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140141"
---
# <a name="process-interest"></a><span data-ttu-id="92620-103">Intressi töötlemine</span><span class="sxs-lookup"><span data-stu-id="92620-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92620-104">See protseduur kirjeldab viivisearvete loomist, printimist ja sisestamist.</span><span class="sxs-lookup"><span data-stu-id="92620-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="92620-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="92620-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="92620-106">Viivise seadistamine sisestusreeglis</span><span class="sxs-lookup"><span data-stu-id="92620-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="92620-107">**Navigeerimispaanis** minge **Moodulid > Krediit ja sissenõuded > Seadistus > Kliendi postitusprofiil**.</span><span class="sxs-lookup"><span data-stu-id="92620-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="92620-108">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="92620-108">Click **Edit**.</span></span>
3. <span data-ttu-id="92620-109">Valige **Seadistus fastTab** moodulis **intressi koodi** väljal ripploendist intressi kood.</span><span class="sxs-lookup"><span data-stu-id="92620-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="92620-110">Kui te ei soovi, et viivist arvutataks kannete puhul selle sisestusreegliga, jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="92620-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="92620-111">**Tabeli piirangu** fastTab abil saate muuta viisi, kuidas intressi töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="92620-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="92620-112">Kui väli on seatud olekusse Jah, arvutatakse viivist selle sisestusreegli puhul.</span><span class="sxs-lookup"><span data-stu-id="92620-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="92620-113">Arvuta intress</span><span class="sxs-lookup"><span data-stu-id="92620-113">Calculate interest</span></span>
1. <span data-ttu-id="92620-114">**Navigeerimispaanis** minge **Moodulid > Krediit ja sissenõuded > Intress > Viivisearve loomine**.</span><span class="sxs-lookup"><span data-stu-id="92620-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="92620-115">Valige kandetüübid, mille puhul viivist arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="92620-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="92620-116">Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.</span><span class="sxs-lookup"><span data-stu-id="92620-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="92620-117">Kui te seadistate **Intress** kui "Jah" arvutate viivisearve viivise.</span><span class="sxs-lookup"><span data-stu-id="92620-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="92620-118">Võite soovida enne nende kannete kaasamist kontrollida viivisearve viivise arvutamise seadusi.</span><span class="sxs-lookup"><span data-stu-id="92620-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="92620-119">Sisestage väljale **Alates** kuupäev, millest alates intressi arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="92620-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="92620-120">Kui te ei täpsusta kuupäeva **Alates**, tühistatakse kõik sisestamata viivisearved ja viivis arvutatakse kande alguskuupäevast alates ümber.</span><span class="sxs-lookup"><span data-stu-id="92620-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="92620-121">Sisestage väljale **Kuupäevani** kuupäev, milleni intressi arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="92620-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="92620-122">Tehke väljal **Kasuta postitusprofiili** valik.</span><span class="sxs-lookup"><span data-stu-id="92620-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="92620-123">Sisestusreegli jaoks kolm võimalust:</span><span class="sxs-lookup"><span data-stu-id="92620-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="92620-124">Konto – kasutab iga viivisearve kohta kliendi kontole määratud sisestusreeglit.</span><span class="sxs-lookup"><span data-stu-id="92620-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="92620-125">Vali – kasutage sisestusreeglit, mille valite väljal Sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="92620-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="92620-126">Kanne – kasutage eraldi sisestusprofiile kannetest, milles arvutatakse viivis iga viivisearve jaoks.</span><span class="sxs-lookup"><span data-stu-id="92620-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="92620-127">Kanded, millele ei ole sisestusprofiili määratud, kasutavad sisestusprofiili, mis on määratletud vormi Müügireskontro parameetrid alal Pearaamat ja käibemaks.</span><span class="sxs-lookup"><span data-stu-id="92620-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="92620-128">Jaotise kaasamiseks laiendage fastTab valikut **Kirjed kaasamiseks**.</span><span class="sxs-lookup"><span data-stu-id="92620-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="92620-129">Klõpsake käsku **Filtreeri**.</span><span class="sxs-lookup"><span data-stu-id="92620-129">Click **Filter**.</span></span>
9. <span data-ttu-id="92620-130">Sisestage kliendi ID väljale **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="92620-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="92620-131">Sisestage näiteks US-001.</span><span class="sxs-lookup"><span data-stu-id="92620-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="92620-132">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="92620-132">Click **OK**.</span></span>
7. <span data-ttu-id="92620-133">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="92620-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="92620-134">Viivisearvete printimine</span><span class="sxs-lookup"><span data-stu-id="92620-134">Print interest notes</span></span>
1. <span data-ttu-id="92620-135">**Navigeerimispaanis** minge **Moodulid > Krediit ja sissenõuded > Intress > Viivisearve ülevaade ja töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="92620-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="92620-136">Valige väljal **Olek** suvand "Loodud".</span><span class="sxs-lookup"><span data-stu-id="92620-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="92620-137">Valige väljal **Prinditud** suvand "Printimata".</span><span class="sxs-lookup"><span data-stu-id="92620-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="92620-138">Klõpsake **Prindi**.</span><span class="sxs-lookup"><span data-stu-id="92620-138">Click **Print**.</span></span>
5. <span data-ttu-id="92620-139">Jaotise kaasamiseks laiendage fastTab valikut **Kirjed kaasamiseks**.</span><span class="sxs-lookup"><span data-stu-id="92620-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="92620-140">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="92620-140">Click **OK**.</span></span>
7. <span data-ttu-id="92620-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="92620-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="92620-142">Viivisearve sisestamine</span><span class="sxs-lookup"><span data-stu-id="92620-142">Post the interest note</span></span>
1. <span data-ttu-id="92620-143">Valige viivisearve, mis on sisestamiseks valmis (olek on loodud).</span><span class="sxs-lookup"><span data-stu-id="92620-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="92620-144">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="92620-144">Click **Post**.</span></span>
3. <span data-ttu-id="92620-145">Sisestage viivisearve sisestamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="92620-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="92620-146">Iga viivisearve kohta pearaamatukande loomiseks valige suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="92620-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="92620-147">Valiku Jah mittemärkimisel summeeritakse kliendi kõigi viivisearvete viivised ja sisestatakse pearaamatusse ühe kandega.</span><span class="sxs-lookup"><span data-stu-id="92620-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="92620-148">Jaotise kaasamiseks laiendage fastTab valikut **Kirjed kaasamiseks**.</span><span class="sxs-lookup"><span data-stu-id="92620-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="92620-149">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="92620-149">Click **OK**.</span></span>
6. <span data-ttu-id="92620-150">Valige väljal **Olek** suvand "Sisestatud".</span><span class="sxs-lookup"><span data-stu-id="92620-150">In the **Status** field, select 'Posted'.</span></span>

