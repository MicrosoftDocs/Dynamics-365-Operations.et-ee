---
title: Materjalitarbe registreerimine mobiilse seadmega
description: Selles teemas kirjeldatakse töövoogu, mis võimaldab registreerida tootmises toormaterjali pihuseadme abil.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5b9c73cf9b23eb8ad9ed872b76b92b395609e9a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "336125"
---
# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="64e00-103">Materjalitarbe registreerimine mobiilse seadmega</span><span class="sxs-lookup"><span data-stu-id="64e00-103">Register material consumption using a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64e00-104">Selles teemas kirjeldatakse töövoogu, mis võimaldab registreerida tootmises toormaterjali pihuseadme abil.</span><span class="sxs-lookup"><span data-stu-id="64e00-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="64e00-105">Sissejuhatus</span><span class="sxs-lookup"><span data-stu-id="64e00-105">Introduction</span></span>
------------

<span data-ttu-id="64e00-106">See töövoog on vajalik juhul, kui materjali jälgitavus on rangelt nõutav.</span><span class="sxs-lookup"><span data-stu-id="64e00-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="64e00-107">Sellistel juhtudel tuleb materjalide jälgitavuse tagamiseks registreerida tarbimisel täpne kellaaeg ja kogus.</span><span class="sxs-lookup"><span data-stu-id="64e00-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="64e00-108">Seda protsessi võib vaadelda vastandina eelnevalt või järgnevale mahaarvamise toimingule, kus registreerimise aja ja tegeliku tarbimise aja vahel on nihe.</span><span class="sxs-lookup"><span data-stu-id="64e00-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="64e00-109">See selgitab, miks mõne jälgitavuse nõudega materjali puhul ei saa kasutada automaatse tarbimise strateegiat.</span><span class="sxs-lookup"><span data-stu-id="64e00-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="64e00-110">Vaatame lihtsat stsenaariumi, mis selgitab, kuidas seadistada töövoogu tooraine registreerimise võimaldamiseks tootmises pihuseadme abil.</span><span class="sxs-lookup"><span data-stu-id="64e00-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="64e00-111">[![töövoo seadistamine tooraine registreerimise võimaldamiseks tootmises pihuseadme abil](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="64e00-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="64e00-112">Stsenaariumi üksikasjad</span><span class="sxs-lookup"><span data-stu-id="64e00-112">Scenario details</span></span>

<span data-ttu-id="64e00-113">Pidev tootmisprotsess (5) tarbib partii kaudu juhitud toormaterjali RM-100.</span><span class="sxs-lookup"><span data-stu-id="64e00-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="64e00-114">Materjali vaba varu on asukohas Bulk-001 (1) litsentsiplaadil PL-1 kahe partiina B1 ja B2, mõlema kogus 100 naela.</span><span class="sxs-lookup"><span data-stu-id="64e00-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="64e00-115">RM-100 puhul väljastatakse ja töödeldakse laotöö (2) ja materjal komplekteeritakse asukohast Bulk-001 ning viiakse sisendasukohta PIL-01 (3), mis on määratletud mitte litsentsiplaadiga juhitavana.</span><span class="sxs-lookup"><span data-stu-id="64e00-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="64e00-116">Masina operaator kaalub tootmise sisendasukohast (3) pärineva materjali ja registreerib kaalu ning partiinumbri tarbituks (4).</span><span class="sxs-lookup"><span data-stu-id="64e00-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="64e00-117">Tootmise sisendasukohast lisatakse materjali osa kindlate ajavahemike järel käsitsi tootmisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="64e00-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="64e00-118">Kui masina operaator materjali lisab, siis see kaalutakse ja partiinumber registreeritakse.</span><span class="sxs-lookup"><span data-stu-id="64e00-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-theworkflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="64e00-119">Töövoo seadistamine tarbimise registreerimiseks pihuseadme abil</span><span class="sxs-lookup"><span data-stu-id="64e00-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="64e00-120">Looge valmiskauba toode FG-100, mille materjalikoosluses on partii kaudu juhitav toormaterjal RM-100.</span><span class="sxs-lookup"><span data-stu-id="64e00-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="64e00-121">Lisage kaks partiid RM-100 (B1 ja B2) koguses 100 asukohta Bulk-001 litsentsiplaadil PL-1.</span><span class="sxs-lookup"><span data-stu-id="64e00-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="64e00-122">RM-100 koosluse rea automaatse tarbimise põhimõtteks määratakse **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="64e00-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="64e00-123">Määrake toodangu sisendasukohaks PIL-01.</span><span class="sxs-lookup"><span data-stu-id="64e00-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="64e00-124">Seda saab teha, valides selle asukoha laos 51 toodangu vaike-sisendasukohaks.</span><span class="sxs-lookup"><span data-stu-id="64e00-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="64e00-125">Uue mobiilse seadme menüüelemendi loomine.</span><span class="sxs-lookup"><span data-stu-id="64e00-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="64e00-126">**Menüüelemendi nimi** – materjali tarbimise registreerimine.</span><span class="sxs-lookup"><span data-stu-id="64e00-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="64e00-127">**Pealkiri** – materjali tarbimise registreerimine.</span><span class="sxs-lookup"><span data-stu-id="64e00-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="64e00-128">**Režiim** – kaudne.</span><span class="sxs-lookup"><span data-stu-id="64e00-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="64e00-129">**Tegevuse kood** – materjali tarbimise registreerimine.</span><span class="sxs-lookup"><span data-stu-id="64e00-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="64e00-130">Lisage menüüelement seadme menüüsse **Mobiilne tootmine**.</span><span class="sxs-lookup"><span data-stu-id="64e00-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="64e00-131">Looge valmis tootele tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="64e00-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="64e00-132">**Kaubakood** – FG-100</span><span class="sxs-lookup"><span data-stu-id="64e00-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="64e00-133">**Laoala** – 5</span><span class="sxs-lookup"><span data-stu-id="64e00-133">**Site** - 5</span></span> 
-    <span data-ttu-id="64e00-134">**Ladu** – 51</span><span class="sxs-lookup"><span data-stu-id="64e00-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="64e00-135">**Kogus** – 150</span><span class="sxs-lookup"><span data-stu-id="64e00-135">**Quantity** - 150</span></span>

<span data-ttu-id="64e00-136">Tootmistellimus **hinnatakse** ja **väljastatakse** ning luuakse laotöö.</span><span class="sxs-lookup"><span data-stu-id="64e00-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="64e00-137">Tehke töö, kasutades pihuseadme toormaterjali komplekteerimise töövoogu.</span><span class="sxs-lookup"><span data-stu-id="64e00-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="64e00-138">See toob materjali hulgiasukohast tootmise sisendasukohta PIL-01.</span><span class="sxs-lookup"><span data-stu-id="64e00-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="64e00-139">Kui töö on lõpetatud, on materjali olek **Komplekteeritud toodangu sisendasukohas**.</span><span class="sxs-lookup"><span data-stu-id="64e00-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="64e00-140">Pärast töö töötlemist võib olek olla **Komplekteeritud** või **Füüsiliselt reserveeritud**.</span><span class="sxs-lookup"><span data-stu-id="64e00-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="64e00-141">See konfigureeritakse parameetriga **Väljastamisolek pärast paigutamist laovormil**.</span><span class="sxs-lookup"><span data-stu-id="64e00-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="64e00-142">Alustage tootmistellimust kliendist või pihuseadmelt, kasutades menüüelementi **Tootmise algus**.</span><span class="sxs-lookup"><span data-stu-id="64e00-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="64e00-143">Pärast tootmistellimuse alustamist võite registreerida materjali tarbimise pihuseadme töövoo abil.</span><span class="sxs-lookup"><span data-stu-id="64e00-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="64e00-144">Alustame 25 naela partii B1 tarbimise registreerimisega.</span><span class="sxs-lookup"><span data-stu-id="64e00-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="64e00-145">Valige pihuseadme menüüst menüüelement **Registreeri materjali** **tarbimine**, sisestage järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="64e00-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="64e00-146">Toote tellimisnumber.</span><span class="sxs-lookup"><span data-stu-id="64e00-146">The production order number.</span></span> 
-    <span data-ttu-id="64e00-147">Asukoht, kust materjali tarbitakse, praegusel juhul PIL-01.</span><span class="sxs-lookup"><span data-stu-id="64e00-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="64e00-148">Kaubakood RM-100.</span><span class="sxs-lookup"><span data-stu-id="64e00-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="64e00-149">Partii number B1.</span><span class="sxs-lookup"><span data-stu-id="64e00-149">Batch number B1.</span></span> 
-    <span data-ttu-id="64e00-150">Kogus 25.</span><span class="sxs-lookup"><span data-stu-id="64e00-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="64e00-151">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="64e00-151">Select **OK**.</span></span>

<span data-ttu-id="64e00-152">Pange tähele, et ekraanil kuvatakse teade „Töölehe rida on loodud”.</span><span class="sxs-lookup"><span data-stu-id="64e00-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="64e00-153">Tootmistellimusel on avatud tööleht tüübiga **Tootmise komplekteerimisloend** kaubale koodiga RM-100 ja partiinumbriga B1.</span><span class="sxs-lookup"><span data-stu-id="64e00-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="64e00-154">Nüüd saate otsustada registreerimist jätkata, nt partiinumbril B2, ja iga kord, kui valite **OK**, lisatakse avatud töölehele uus töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="64e00-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="64e00-155">Kui olete registreerimise lõpetanud, siis valige **Valmis** töölehe sisestamiseks ja töövoo lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="64e00-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="64e00-156">Lisakommentaarid</span><span class="sxs-lookup"><span data-stu-id="64e00-156">Additional comments</span></span> 

-   <span data-ttu-id="64e00-157">Kui kasutaja tühistab töövoo pärast töölehe rea loomist, siis on tööleht sisestamata olekus, ent kui kasutaja kasutab hiljem töövoogu sama tootmistellimuse jaoks, siis lisatakse read avatud töölehele, mitte uuele töölehele.</span><span class="sxs-lookup"><span data-stu-id="64e00-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="64e00-158">Uus töövoog toetab ka seerianumbrite registreerimist.</span><span class="sxs-lookup"><span data-stu-id="64e00-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="64e00-159">Registreerida on võimalik ainult kooslusel või valitud tootmistellimuses või partiitellimuses määratletud kaubakoodi.</span><span class="sxs-lookup"><span data-stu-id="64e00-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="64e00-160">Materjali saab üle tarbida.</span><span class="sxs-lookup"><span data-stu-id="64e00-160">Material can be overconsumed.</span></span> <span data-ttu-id="64e00-161">Näiteks kui eeldatav materjalitarbimise kogus on 100 naela, siis võib selle tarbida üle näiteks kogusega 105 naela.</span><span class="sxs-lookup"><span data-stu-id="64e00-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>


