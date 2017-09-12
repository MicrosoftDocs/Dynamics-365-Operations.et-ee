---
title: Materjalitarbe registreerimine mobiilse seadmega
description: "Selles teemas kirjeldatakse töövoogu, mis võimaldab registreerida tootmises toormaterjali pihuseadme abil."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 83703d962d6099ba8ac107548a569c8d1f34882f
ms.contentlocale: et-ee
ms.lasthandoff: 08/30/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="1ff2e-103">Materjalitarbe registreerimine mobiilse seadmega</span><span class="sxs-lookup"><span data-stu-id="1ff2e-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="1ff2e-104">Selles teemas kirjeldatakse töövoogu, mis võimaldab registreerida tootmises toormaterjali pihuseadme abil.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="1ff2e-105">Sissejuhatus</span><span class="sxs-lookup"><span data-stu-id="1ff2e-105">Introduction</span></span>
------------

<span data-ttu-id="1ff2e-106">See töövoog on vajalik juhul, kui materjali jälgitavus on rangelt nõutav.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="1ff2e-107">Sellistel juhtudel tuleb materjalide jälgitavuse tagamiseks registreerida tarbimisel täpne kellaaeg ja kogus.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="1ff2e-108">Seda protsessi võib vaadelda vastandina eelnevalt või järgnevale mahaarvamise toimingule, kus registreerimise aja ja tegeliku tarbimise aja vahel on nihe.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="1ff2e-109">See selgitab, miks mõne jälgitavuse nõudega materjali puhul ei saa kasutada automaatse tarbimise strateegiat.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="1ff2e-110">Vaatame lihtsat stsenaariumi, mis selgitab, kuidas seadistada töövoogu tooraine registreerimise võimaldamiseks tootmises pihuseadme abil.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a><span data-ttu-id="1ff2e-111">Stsenaariumi üksikasjad</span><span class="sxs-lookup"><span data-stu-id="1ff2e-111">Scenario details</span></span>

<span data-ttu-id="1ff2e-112">Pidev tootmisprotsess (5) tarbib partii kaudu juhitud toormaterjali RM-100.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-112">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="1ff2e-113">Materjali vaba varu on asukohas Bulk-001 (1) litsentsiplaadil PL-1 kahe partiina B1 ja B2, mõlema kogus 100 naela.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-113">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="1ff2e-114">RM-100 puhul väljastatakse ja töödeldakse laotöö (2) ja materjal komplekteeritakse asukohast Bulk-001 ning viiakse sisendasukohta PIL-01 (3), mis on määratletud mitte litsentsiplaadiga juhitavana.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-114">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="1ff2e-115">Masina operaator kaalub tootmise sisendasukohast (3) pärineva materjali ja registreerib kaalu ning partiinumbri tarbituks (4).</span><span class="sxs-lookup"><span data-stu-id="1ff2e-115">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="1ff2e-116">Tootmise sisendasukohast lisatakse materjali osa kindlate ajavahemike järel käsitsi tootmisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-116">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="1ff2e-117">Kui masina operaator materjali lisab, siis see kaalutakse ja partiinumber registreeritakse.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-117">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="1ff2e-118">Töövoo seadistamine tarbimise registreerimiseks pihuseadme abil</span><span class="sxs-lookup"><span data-stu-id="1ff2e-118">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="1ff2e-119">Looge valmiskauba toode FG-100, mille materjalikoosluses on partii kaudu juhitav toormaterjal RM-100.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-119">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="1ff2e-120">Lisage kaks partiid RM-100 (B1 ja B2) koguses 100 asukohta Bulk-001 litsentsiplaadil PL-1.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-120">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="1ff2e-121">RM-100 koosluse rea automaatse tarbimise põhimõtteks määratakse **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-121">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="1ff2e-122">Määrake toodangu sisendasukohaks PIL-01.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-122">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="1ff2e-123">Seda saab teha, valides selle asukoha laos 51 toodangu vaike-sisendasukohaks.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-123">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="1ff2e-124">Uue mobiilse seadme menüüelemendi loomine.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-124">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="1ff2e-125">**Menüüelemendi nimi** – materjali tarbimise registreerimine.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-125">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="1ff2e-126">**Pealkiri** – materjali tarbimise registreerimine.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-126">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="1ff2e-127">**Režiim** – kaudne.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-127">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="1ff2e-128">**Tegevuse kood** – materjali tarbimise registreerimine.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-128">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="1ff2e-129">Lisage menüüelement seadme menüüsse **Mobiilne tootmine**.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-129">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="1ff2e-130">Looge valmis tootele tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-130">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="1ff2e-131">**Kaubakood** – FG-100</span><span class="sxs-lookup"><span data-stu-id="1ff2e-131">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="1ff2e-132">**Laoala** – 5</span><span class="sxs-lookup"><span data-stu-id="1ff2e-132">**Site** - 5</span></span> 
-    <span data-ttu-id="1ff2e-133">**Ladu** – 51</span><span class="sxs-lookup"><span data-stu-id="1ff2e-133">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="1ff2e-134">**Kogus** – 150</span><span class="sxs-lookup"><span data-stu-id="1ff2e-134">**Quantity** - 150</span></span>

<span data-ttu-id="1ff2e-135">Tootmistellimus **hinnatakse** ja **väljastatakse** ning luuakse laotöö.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-135">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="1ff2e-136">Tehke töö, kasutades pihuseadme toormaterjali komplekteerimise töövoogu.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-136">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="1ff2e-137">See toob materjali hulgiasukohast tootmise sisendasukohta PIL-01.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-137">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="1ff2e-138">Kui töö on lõpetatud, on materjalil olek **Komplekteeritud toodangu sisendasukohas**.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-138">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="1ff2e-139">Pärast töö töötlemist võib olek olla **Komplekteeritud** või **Füüsiliselt reserveeritud**.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-139">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="1ff2e-140">See konfigureeritakse parameetriga **Väljastamisolek pärast paigutamist laovormil**.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-140">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="1ff2e-141">Alustage tootmistellimust kliendist või pihuseadmelt, kasutades menüüelementi **Tootmise algus**.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-141">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="1ff2e-142">Pärast tootmistellimuse alustamist võite registreerida materjali tarbimise pihuseadme töövoo abil.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-142">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="1ff2e-143">Alustame 25 naela partii B1 tarbimise registreerimisega.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-143">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="1ff2e-144">Valige pihuseadme menüüst menüüelement **Registreeri materjali** **tarbimine**, sisestage järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-144">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="1ff2e-145">Toote tellimisnumber.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-145">The production order number.</span></span> 
-    <span data-ttu-id="1ff2e-146">Asukoht, kust materjali tarbitakse, praegusel juhul PIL-01.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-146">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="1ff2e-147">Kaubakood RM-100.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-147">Item number RM-100.</span></span> 
-    <span data-ttu-id="1ff2e-148">Partii number B1.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-148">Batch number B1.</span></span> 
-    <span data-ttu-id="1ff2e-149">Kogus 25.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-149">A quantity of 25.</span></span>

7.  <span data-ttu-id="1ff2e-150">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-150">Select **OK**.</span></span>

<span data-ttu-id="1ff2e-151">Pange tähele, et ekraanil kuvatakse teade „Töölehe rida on loodud”.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-151">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="1ff2e-152">Tootmistellimusel on avatud tööleht tüübiga **Tootmise komplekteerimisloend** kaubale koodiga RM-100 ja partiinumbriga B1.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-152">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="1ff2e-153">Nüüd saate otsustada registreerimist jätkata, nt partiinumbril B2, ja iga kord, kui valite **OK**, lisatakse avatud töölehele uus töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-153">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="1ff2e-154">Kui olete registreerimise lõpetanud, siis valige **Valmis** töölehe sisestamiseks ja töövoo lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-154">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="1ff2e-155">Lisakommentaarid</span><span class="sxs-lookup"><span data-stu-id="1ff2e-155">Additional comments</span></span> 

-   <span data-ttu-id="1ff2e-156">Kui kasutaja tühistab töövoo pärast töölehe rea loomist, siis on tööleht sisestamata olekus, kuid kui kasutaja kasutab hiljem töövoogu sama tootmistellimuse jaoks, siis lisatakse read avatud töölehele, mitte uuele töölehele.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-156">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="1ff2e-157">Uus töövoog toetab ka seerianumbrite registreerimist.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-157">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="1ff2e-158">Registreerida on võimalik ainult kooslusel või valitud tootmistellimuses või partiitellimuses määratletud kaubakoodi.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-158">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="1ff2e-159">Materjali saab üle tarbida.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-159">Material can be overconsumed.</span></span> <span data-ttu-id="1ff2e-160">Näiteks kui eeldatav materjalitarbimise kogus on 100 naela, siis võib selle tarbida üle näiteks kogusega 105 naela.</span><span class="sxs-lookup"><span data-stu-id="1ff2e-160">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



