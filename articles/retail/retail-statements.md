---
title: "Jaemüügi väljavõtted"
description: "See teema kirjeldab, kuidas väljavõtteid luuakse ja sisestatakse."
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: ddceadb797af98f85670df72a335b2714fe2f01e
ms.contentlocale: et-ee
ms.lasthandoff: 03/07/2018

---

# <a name="retail-statements"></a><span data-ttu-id="2047b-103">Jaemüügi väljavõtted</span><span class="sxs-lookup"><span data-stu-id="2047b-103">Retail statements</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="2047b-104">Rakenduses Microsoft Dynamics for Retail 365 kasutatakse väljavõtte sisestamise protsessi pilvekassas ja uudses kassas toimuvate kannete arvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="2047b-104">In Microsoft Dynamics 365 for Retail, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="2047b-105">Väljavõtte sisestamise protsess kasutab jaotusgraafikut, et tõmmata kassa kannete komplekt peakontori klienti.</span><span class="sxs-lookup"><span data-stu-id="2047b-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="2047b-106">Lehtedel **Jaemüügi parameetrid** ja **Kauplused** määratletud parameetreid kasutatakse üksikutesse väljavõtetesse tõmmatavate kannete valimiseks.</span><span class="sxs-lookup"><span data-stu-id="2047b-106">The parameters that are defined on the **Retail parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>  

<span data-ttu-id="2047b-107">Järgmine joonis illustreerib väljavõtte sisestamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="2047b-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="2047b-108">Selles protsessis edastatakse kassas salvestatud kanded kliendile Kaupluse andmeedastaja abil.</span><span class="sxs-lookup"><span data-stu-id="2047b-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Retail scheduler.</span></span> <span data-ttu-id="2047b-109">Pärast seda, kui klient on kanded kätte saanud, saate luua, arvutada ja sisestada kaupluse kannete väljavõtte.</span><span class="sxs-lookup"><span data-stu-id="2047b-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span> 

<span data-ttu-id="2047b-110">[![Väljavõtte sisestamise protsess](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="2047b-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="2047b-111">Väljavõtete loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="2047b-111">Creating and posting statements</span></span>
<span data-ttu-id="2047b-112">Saate luua väljavõtte käsitsi või päeva jooksul perioodiliselt käivituma seadistatud pakktöötlust kasutades.</span><span class="sxs-lookup"><span data-stu-id="2047b-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="2047b-113">Mõlemal juhul kasutatakse väljavõtete loomiseks ja sisestamiseks järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="2047b-113">In both cases, the following steps are used to create and post statements.</span></span>

###  <a name="create-the-statement"></a><span data-ttu-id="2047b-114">Väljavõtte loomine</span><span class="sxs-lookup"><span data-stu-id="2047b-114">Create the statement</span></span>
<span data-ttu-id="2047b-115">Selles etapis identifitseeritakse kauplus, millele väljavõte käsitsi luuakse.</span><span class="sxs-lookup"><span data-stu-id="2047b-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="2047b-116">Pakktöötluse konfigureerimisel saate luua automaatselt väljavõtteid kõigi kaupluste kohta enda määratud ajakava alusel.</span><span class="sxs-lookup"><span data-stu-id="2047b-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span> 

### <a name="calculate-the-statement"></a><span data-ttu-id="2047b-117">Väljavõtte arvutamine</span><span class="sxs-lookup"><span data-stu-id="2047b-117">Calculate the statement</span></span>
<span data-ttu-id="2047b-118">Selles etapis valitakse kanderead lehtedel **Jaemüügi parameetrid** ja **Kauplused** igale kauplusele määratletud kriteeriumide alusel.</span><span class="sxs-lookup"><span data-stu-id="2047b-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Retail parameters** and **Stores** pages.</span></span> <span data-ttu-id="2047b-119">Neil lehtedel saate määratleda kriteeriumid ja määrata, kuidas kandeid arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="2047b-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="2047b-120">Väljavõttesse kaasatud kannete loendi vaatamiseks enne väljavõtte arvutamist kasutage lehte **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="2047b-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span> 

<span data-ttu-id="2047b-121">Väljavõtte arvutamisel kasutatakse loendatud summana registrite päevakassasid.</span><span class="sxs-lookup"><span data-stu-id="2047b-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="2047b-122">Loetud summa saab sisestada ka käsitsi.</span><span class="sxs-lookup"><span data-stu-id="2047b-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="2047b-123">Väljavõttel kuvatakse kõikide maksemeetodite kannete müügisumma ja tegeliku loendatud summa vahe.</span><span class="sxs-lookup"><span data-stu-id="2047b-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="2047b-124">Väljavõte sisestatakse ainult juhul, kui erinevus on väiksem kui kaupluse puhul määratletud maksimaalne sisestuse erinevus.</span><span class="sxs-lookup"><span data-stu-id="2047b-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span> 

> [!NOTE]
> <span data-ttu-id="2047b-125">Väljavõtte arvutamise protsess kasutab globaalset numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="2047b-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="2047b-126">Väljavõtte arvutamisel hõlmab arvutus järgmisi ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="2047b-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="2047b-127">Märkige valitud kuupäevavahemiku kohta kanded, mida eelmise väljavõtte arvutusse ei kaasatud.</span><span class="sxs-lookup"><span data-stu-id="2047b-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span> 
- <span data-ttu-id="2047b-128">Arvutage valitud kannete puhul makstud kogusummad.</span><span class="sxs-lookup"><span data-stu-id="2047b-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="2047b-129">Tulemused kuvatakse väljavõtte ridadel, olenevalt väljavõtte meetodist.</span><span class="sxs-lookup"><span data-stu-id="2047b-129">The results are shown on the statement lines, depending on the statement method:</span></span>

  - <span data-ttu-id="2047b-130">Kui väljavõtte meetod on **Kokku**, luuakse valitud kannetes iga makseviisi jaoks üks rida.</span><span class="sxs-lookup"><span data-stu-id="2047b-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span> 
  - <span data-ttu-id="2047b-131">Kui väljavõtte meetod on **Personal**, luuakse iga makseviisi jaoks üks rida kannetes, mille sooritas valitud personali liige.</span><span class="sxs-lookup"><span data-stu-id="2047b-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span> 
  - <span data-ttu-id="2047b-132">Kui väljavõtte meetod on **Kassaterminal**, luuakse iga makseviisi jaoks üks rida kannetes, mis sooritati valitud registris.</span><span class="sxs-lookup"><span data-stu-id="2047b-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span> 
  - <span data-ttu-id="2047b-133">Kui väljavõtte meetod on **Vahetus**, luuakse iga makseviisi jaoks üks rida kannetes, mis sooritati vahetuse jooksul.</span><span class="sxs-lookup"><span data-stu-id="2047b-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="2047b-134">Kui lehel **Kauplused** on märgitud ruut **Tükelda väljavõtte meetodi alusel**, luuakse eraldi väljavõte, võttes aluseks väljal **Väljavõtte meetod** valitud väärtuse.</span><span class="sxs-lookup"><span data-stu-id="2047b-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="2047b-135">Kui teie kaupluse töötunnid ületavad kesköö, saate konfigureerida väljavõtte sisestamist nii, et see põhineb kalendripäeva lõpu asemel tööpäeva lõpu seisul.</span><span class="sxs-lookup"><span data-stu-id="2047b-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span> 

<span data-ttu-id="2047b-136">Sisestage lehe **Kauplused** kiirkaardi **Väljavõte/sulgemine** väljal **Tööpäeva lõpp** aeg, millal viimane kanne tuleb salvestada, et see kaasataks tööpäeva väljavõttesse.</span><span class="sxs-lookup"><span data-stu-id="2047b-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day’s statement.</span></span> <span data-ttu-id="2047b-137">Märkige ruut **Sisesta tööpäevana** kannete sisestamiseks sama tööpäeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="2047b-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="2047b-138">Väljavõtte sisestamisel saab sama tööpäeva jooksul salvestatud kanded kaasata samasse müügitellimusse, isegi kui mõni kanne toimub enne keskööd ja mõni pärast keskööd.</span><span class="sxs-lookup"><span data-stu-id="2047b-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span> 

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="2047b-139">Näide: väljavõtte sisestamine tööpäeva kohta, mis hõlmab kahte kalendripäeva</span><span class="sxs-lookup"><span data-stu-id="2047b-139">Example: Post a statement for a business day that extends over two calendar days</span></span> 

<span data-ttu-id="2047b-140">Kauplus on avatud 8.00 kuni 03.00 ja kaupluse konfiguratsioonis on ruut **Sisesta tööpäevana** märgitud.</span><span class="sxs-lookup"><span data-stu-id="2047b-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="2047b-141">31. mail salvestab kauplus kandeid ajavahemikus 8.00 kuni kesköö.</span><span class="sxs-lookup"><span data-stu-id="2047b-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="2047b-142">Kauplus salvestab ka kandeid 1. juunil ajavahemikus 00.01 kuni 03.00.</span><span class="sxs-lookup"><span data-stu-id="2047b-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span> 

<span data-ttu-id="2047b-143">Kui kauplus sisestab väljavõtte tööpäeva sulgemise seisuga, hõlmab loodav müügitellimus kõiki kandeid, mis salvestati töötundidel 08.00 kuni 03.00, kuigi kanded toimusid kahel päeval, 31. mail ja 1. juunil.</span><span class="sxs-lookup"><span data-stu-id="2047b-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span> 

<span data-ttu-id="2047b-144">Kui sama kaupluse puhul on märkeruut **Sisesta tööpäevana** tühi, luuakse eraldi müügitellimused, kui kauplus sisestab oma tööpäeva lõpu väljavõtte.</span><span class="sxs-lookup"><span data-stu-id="2047b-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="2047b-145">Üks müügitellimus sisaldab kandeid, mis registreeriti 31. mail töötundidel 8.00 kuni kesköö ja teine müügitellimus sisaldab kandeid, mis registreeriti 1. juunil ajavahemikus 00.01. kuni 03.00.</span><span class="sxs-lookup"><span data-stu-id="2047b-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>
 
> [!NOTE]
> <span data-ttu-id="2047b-146">Enne väljavõtete loomist tuleb sulgeda väljavõtte perioodi vahetused.</span><span class="sxs-lookup"><span data-stu-id="2047b-146">Before you can create statements, you should close the shifts in the statement period.</span></span> 

### <a name="post-the-statement"></a><span data-ttu-id="2047b-147">Väljavõtte sisestamine</span><span class="sxs-lookup"><span data-stu-id="2047b-147">Post the statement</span></span>
<span data-ttu-id="2047b-148">Väljavõtte sisestamisel luuakse väljavõtte jaemüügi müügitellimused ja arved.</span><span class="sxs-lookup"><span data-stu-id="2047b-148">When you post a statement, sales orders and invoices are created for the retail sales in the statement.</span></span>

- <span data-ttu-id="2047b-149">Sularahamüük koondatakse ühele müügitellimusele ja selle eest esitatakse arve kauplusele määratud vaikekliendile.</span><span class="sxs-lookup"><span data-stu-id="2047b-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span> 
- <span data-ttu-id="2047b-150">Jaemüük, mille puhul klient lisati kandele rakenduses Microsoft Dynamics 365 for Retail POS, luuakse eraldi müügitellimused ja arved, üks iga kordumatu kliendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="2047b-150">Retail sales for which a customer was added to the transaction in Microsoft Dynamics 365 for Retail POS generate separate sales orders and invoices, one for each unique customer.</span></span> 

<span data-ttu-id="2047b-151">Makse töölehed luuakse väljavõtte maksetele automaatselt ja kassa kaupluse varud uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="2047b-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>

