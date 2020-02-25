---
title: Kaupluse varude haldamine
description: Selles teemas kirjeldatakse dokumenditüüpe, mida saate kasutada varude haldamiseks.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3f7f228bbf312a2ccdc96d3e95287898bee01de4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022229"
---
# <a name="store-inventory-management"></a><span data-ttu-id="dc221-103">Kaupluse varude haldamine</span><span class="sxs-lookup"><span data-stu-id="dc221-103">Store inventory management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dc221-104">Töötades varudega rakenduses Dynamics 365 Commerce ja kasutades kassarakendust, on oluline märkida, et kassa pakub piiratud tuge varude dimensioonidele ja teatud laokaubatüüpidele.</span><span class="sxs-lookup"><span data-stu-id="dc221-104">When working with inventory in Dynamics 365 Commerce and using the POS application, it is important to note that POS provides limited support for inventory dimensions and certain inventory item types.</span></span>

<span data-ttu-id="dc221-105">Kassalahendus ei toeta järgmiste kaupade konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="dc221-105">The POS solution does not support the following item configurations:</span></span>

- <span data-ttu-id="dc221-106">Kooslusekaubad (v.a komplekttooted, mis kasutavad koosluse raamistiku mõningaid komponente)</span><span class="sxs-lookup"><span data-stu-id="dc221-106">BOM items (except kit products, which utilize some components of the BOM framework)</span></span>
- <span data-ttu-id="dc221-107">Tegeliku kaaluga kaubad</span><span class="sxs-lookup"><span data-stu-id="dc221-107">Catch weight items</span></span>
- <span data-ttu-id="dc221-108">Partiiga juhitavad kaubad</span><span class="sxs-lookup"><span data-stu-id="dc221-108">Batch-controlled items</span></span>

<span data-ttu-id="dc221-109">Kassarakendus ei toeta praegu kassas järgmisi jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="dc221-109">The POS application currently does not support the following tracking dimensions in the POS:</span></span>

- <span data-ttu-id="dc221-110">Partii jälgimisdimensioon</span><span class="sxs-lookup"><span data-stu-id="dc221-110">Batch tracking dimension</span></span>
- <span data-ttu-id="dc221-111">Omanikudimensioon</span><span class="sxs-lookup"><span data-stu-id="dc221-111">Owner dimension</span></span>

<span data-ttu-id="dc221-112">Kassalahendus pakub piiratud tuge järgmistele dimensioonidele.</span><span class="sxs-lookup"><span data-stu-id="dc221-112">The POS solution provides limited support for the following dimensions.</span></span> <span data-ttu-id="dc221-113">Piiratud tugi tähendab, et kassa võib lao/kaupluse seadistuse konfiguratsiooni põhjal mõne neist dimensioonidest varude kannetesse automaatselt vaikimisi määrata.</span><span class="sxs-lookup"><span data-stu-id="dc221-113">Limited support indicates that the POS may default some of these dimensions into inventory transactions automatically based on warehouse/store setup configuration.</span></span> <span data-ttu-id="dc221-114">Kassa ei toeta dimensioone täielikult samal viisil, nagu neid toetatakse müügikande käsitsi sisestamisel ERP-sse.</span><span class="sxs-lookup"><span data-stu-id="dc221-114">POS will not fully support the dimensions in the way they are supported if a sales transaction is manually entered into the ERP.</span></span> 

- <span data-ttu-id="dc221-115">**Lao asukoht** – kasutajatel ei ole võimalik hallata vastuvõtva lao asukohta kaupade vastuvõtmisel kaupluse lattu, kui kauplus ei ole konfigureeritud kasutama laohalduse protsessi.</span><span class="sxs-lookup"><span data-stu-id="dc221-115">**Warehouse Location** – Users will not have the ability to manage the receiving warehouse location for items received into a store warehouse when the store has not been configured to use the warehouse management process.</span></span> <span data-ttu-id="dc221-116">Nende kaupade puhul kasutatakse kaupluse ladu vaikimisi määratletud vastuvõtva asukohana.</span><span class="sxs-lookup"><span data-stu-id="dc221-116">A default receiving location defined on the store warehouse will be used for these items.</span></span> <span data-ttu-id="dc221-117">Kui laohalduse protsess on kaupluses lubatud, siis käivitatakse piiratud tugi, mis palub kasutajal valida vastuvõttev asukoht kogu sissetuleku kohta.</span><span class="sxs-lookup"><span data-stu-id="dc221-117">If the warehouse management process has been enabled for the store, limited support that prompts the user to choose a receiving location for the entire receipt will be triggered.</span></span> <span data-ttu-id="dc221-118">Poest müüdavaid kaupu müüakse alati kaupluse laoseadistuses vaikimisi määratletud asukohast.</span><span class="sxs-lookup"><span data-stu-id="dc221-118">Items sold from the store will always be sold out of the default location as defined on the store warehouse setup.</span></span> <span data-ttu-id="dc221-119">Tagastatava kauba lao asukoha haldamist saab kontrollida poe lao vaikimisi tagastatava asukoha definitsiooni alusel või tagastamise põhjusekoodide alusel, nagu on määratletud tagastamise asukoha poliitikas.</span><span class="sxs-lookup"><span data-stu-id="dc221-119">The location for managing return inventory can be controlled through default return location definition on the store warehouse or based on return reason codes as defined in the return location policy.</span></span>
- <span data-ttu-id="dc221-120">**Litsentsiplaat** – litsentsiplaadid kohalduvad ainult siis, kui kauba ja kaupluselao puhul on lubatud suvand **Kasuta laohaldusprotsesse**.</span><span class="sxs-lookup"><span data-stu-id="dc221-120">**License plate** – License plates are only applicable when **Use warehouse management process** has been enabled on the item and the store warehouse.</span></span> <span data-ttu-id="dc221-121">Kui Varud võetakse kaupluse lattu, kus laohalduse protsess on lubatud, ja kauba vastuvõtmiseks valitud asukoht on seotud asukoha profiiliga, mis nõuab litsentsiplaadi juhtimist, siis rakendus Kassa rakendab vastuvõtvale reale litsentsiplaati süstemaatiliselt.</span><span class="sxs-lookup"><span data-stu-id="dc221-121">In POS, if inventory is received into a store warehouse where the warehouse management process has been enabled, and the location chosen to receive the item into is tied to a location profile that requires license plate control, the POS application will systematically apply a license plate to the receiving line.</span></span> <span data-ttu-id="dc221-122">Kassa kasutajatel ei ole võimalust neid litsentsiplaadi andmeid muuta ega hallata.</span><span class="sxs-lookup"><span data-stu-id="dc221-122">Users in POS will not have the ability to change or manage this license plate data.</span></span> <span data-ttu-id="dc221-123">Kui on nõutav litsentsiplaadi täielik haldamine, soovitatakse kauplusel kasutada rakendusi WMS Mobile või ERP-i kontoriklienti nende kaupade vastuvõtmise haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="dc221-123">If full management of license plates is required, it is suggested the store use the WMS mobile application or the back office ERP client to manage the receipt of these items.</span></span>
- <span data-ttu-id="dc221-124">**Seerianumber** – rakendusel Kassa on piiratud tugi ühe seerianumbri jaoks, mis registreeritakse kande müügireal kassas loodud tellimuste alusel järjestatud kaupadele.</span><span class="sxs-lookup"><span data-stu-id="dc221-124">**Serial number** – The POS application has limited support for single serial number to be registered on a transaction sales line for orders created in POS with serialized items.</span></span> <span data-ttu-id="dc221-125">Seda seerianumbrit ei kinnitata laos registreeritud seerianumbrite suhtes.</span><span class="sxs-lookup"><span data-stu-id="dc221-125">This serial number is not validated against registered serial numbers already in inventory.</span></span> <span data-ttu-id="dc221-126">Kui müügitellimus on loodud kõnekeskuse kanalis või on täidetud ERP-i kaudu ja mitu seerianumbrit on registreeritud ühel müügireal ERP-is täitmise protsessi käigus, siis neid seerianumbreid ei saa rakendada ega kinnitata, kui nende tellimuste puhul teostatakse kassas tagastust.</span><span class="sxs-lookup"><span data-stu-id="dc221-126">If a sales order is created in the call center channel or fulfilled through the ERP and multiple serial numbers are registered to a single sales line during the fulfillment process in the ERP, these serial numbers will not be able to be applied or validated if a return is processed in POS for these orders.</span></span>
- <span data-ttu-id="dc221-127">**Lao olek** – kaupade puhul, mis kasutavad laohalduse protsessi ja nõuavad lao olekut, ei saa oleku välja määrata ega muuta rakenduse Kassa kaudu.</span><span class="sxs-lookup"><span data-stu-id="dc221-127">**Inventory status** – For items that use the warehouse management process and require an inventory status, this status field is not able to be set or modified through the POS application.</span></span> <span data-ttu-id="dc221-128">Kaupluse lao konfiguratsioonis määratletud lao vaikimisi olekut kasutatakse kaupade lattu vastuvõtmisel.</span><span class="sxs-lookup"><span data-stu-id="dc221-128">The default inventory status as defined on the store warehouse configuration will be used when items are received into inventory.</span></span>

> [!NOTE]
> <span data-ttu-id="dc221-129">Kõik organisatsioonid peavad kaubakonfiguratsioone kassa kaudu arendus- või katsekeskkonnas katsetama, enne kui need tootmisse juurutab.</span><span class="sxs-lookup"><span data-stu-id="dc221-129">All organizations must test item configurations through POS in development or test environments before deploying them to production.</span></span> <span data-ttu-id="dc221-130">Katsetage oma kaupu, tehes nendega kassa kaudu regulaarseid sularahaga müügikandeid ja luues klienditellimusi (kohaldatavusel).</span><span class="sxs-lookup"><span data-stu-id="dc221-130">Test your items by performing regular cash and carry sales transacting and creating customer orders (if applicable) through the POS with your items.</span></span> <span data-ttu-id="dc221-131">Katsetamine peab hõlmama katsekeskkonnas täielikke väljavõtte sisestamise protsesse ja probleemide puudumise kontrollimist.</span><span class="sxs-lookup"><span data-stu-id="dc221-131">Testing must include running a full statement posting processes in your test environment and verifying that there are no issues.</span></span>
>
> <span data-ttu-id="dc221-132">Kaupade konfigureerimine viisil, mida kassarakendus ei toeta, ilma nõuetekohase katsetamiseta, võib põhjustada teie väljavõtete sisestamise protsessi nurjumist tootmises ilma probleemide hõlpsa lahendamise võimaluseta.</span><span class="sxs-lookup"><span data-stu-id="dc221-132">Configuring items in a way that is not supported by the POS application, without proper testing, can result in your statement posting process failing in production without an easy way to correct the issues.</span></span> <span data-ttu-id="dc221-133">Nende sisestusprotsesside õnnestumise võimaldamiseks võib kaaluda rakendusele partneri või kliendi kohanduste lubamist.</span><span class="sxs-lookup"><span data-stu-id="dc221-133">Partner or customer customizations to the application may optionally be considered to allow these posting processes to successfully complete.</span></span> <span data-ttu-id="dc221-134">Kui kohandused pole vajalikud, peab organisatsioon veenduma, et toodete tootekonfiguratsioon on tehtud viisil, mida toetab standardne kassarakenduse / tellimuse loomise / väljavõtte sisestamise protsess.</span><span class="sxs-lookup"><span data-stu-id="dc221-134">If customizations are not needed, the organization must ensure that the product configuration of your products has been done in a way that is supported by the standard POS application/order creation/statement posting process.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="dc221-135">Ostutellimused</span><span class="sxs-lookup"><span data-stu-id="dc221-135">Purchase orders</span></span>

<span data-ttu-id="dc221-136">Ostutellimused koostatakse peakontoris.</span><span class="sxs-lookup"><span data-stu-id="dc221-136">Purchase orders are created at the head office.</span></span> <span data-ttu-id="dc221-137">Kui ostutellimuse päisesse on kaasatud ladu, saab tellimust vastu võtta kaupluses, kasutades Modern POS-i (MPOS) või pilvekassat toimingu **Komplekteerimine ja vastuvõtmine** kaudu.</span><span class="sxs-lookup"><span data-stu-id="dc221-137">If a warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS through the **Picking/Receiving** operation.</span></span> <span data-ttu-id="dc221-138">Pärast seda, kui laos vastuvõetud kogused sisestatakse ostutellimuse dokumendi jaoks kassas väljale **Saa kohe**, saab neid salvestada kohalikult või kooskõlastatult.</span><span class="sxs-lookup"><span data-stu-id="dc221-138">After the quantities that are received at the store are entered in the **Receive Now** field in POS for the purchase order document, they can be saved locally or committed.</span></span> <span data-ttu-id="dc221-139">Selle teabe salvestamisel kohalikult eil ole mõju laovarule.</span><span class="sxs-lookup"><span data-stu-id="dc221-139">Saving this data locally has no effect on in-stock inventory.</span></span> <span data-ttu-id="dc221-140">Salvestamine peaks toimuma ainult juhul, kui kasutaja ei ole valmis sissetulekut sisestama HQ-sse ja vajab lihtsalt võimalust eelnevalt sisestatud andmed **Saa kohe** ajutiselt talletada.</span><span class="sxs-lookup"><span data-stu-id="dc221-140">Saving should be done only if the user is not ready to post the receipt to HQ and just needs a way to temporarily store the previously entered **Receive Now** data.</span></span> <span data-ttu-id="dc221-141">See salvestab nüüd andmed kohalikult kasutaja kanali andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="dc221-141">This saves the receive now data locally to the user's channel database.</span></span> <span data-ttu-id="dc221-142">Pärast dokumendi töötlemist, kasutades suvandit **Kinnita**,saadetakse andmed **Saa kohe** HQ-sse ja ostutellimuse sissetulek sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="dc221-142">After the document is processed using the **Commit** option, the **Receive Now** data is sent to HQ and the purchase order receipt will be posted.</span></span> 

## <a name="transfer-orders"></a><span data-ttu-id="dc221-143">Üleviimistellimused</span><span class="sxs-lookup"><span data-stu-id="dc221-143">Transfer orders</span></span>

<span data-ttu-id="dc221-144">Üleviimistellimusega saab määrata, et kindel kauplus on asukoht, kust kaupu saab lähetada või kuhu võetakse varusid vastu.</span><span class="sxs-lookup"><span data-stu-id="dc221-144">A transfer order can specify that a particular store is the location that items can be shipped from or the location the inventory will be received into.</span></span> <span data-ttu-id="dc221-145">Kui kassa kasutaja on üleviimistellimust lähetav ladu, saavad nad sisestada koguse **Läheta kohe** otse kassast.</span><span class="sxs-lookup"><span data-stu-id="dc221-145">If the POS user is the shipping warehouse for a transfer order, they will be able to enter **Ship Now** quantities from POS.</span></span> <span data-ttu-id="dc221-146">Lähetava kaupluse sisestatud andmeid saab salvestada kohalikult või kooskõlastatud.</span><span class="sxs-lookup"><span data-stu-id="dc221-146">The data entered by the shipping store can be saved locally or committed.</span></span> <span data-ttu-id="dc221-147">Kohalikult salvestamisel ei tehta üleviimistellimuse dokumendile HQ-s ühtegi värskendust.</span><span class="sxs-lookup"><span data-stu-id="dc221-147">When saved locally, no updates are made to the transfer order document in HQ.</span></span> <span data-ttu-id="dc221-148">Salvestamine peaks toimuma ainult juhul, kui kasutaja ei ole valmis saadetist sisestama HQ-sse ja vajab lihtsalt võimalust eelnevalt sisestatud andmed **Läheta kohe** ajutiselt talletada.</span><span class="sxs-lookup"><span data-stu-id="dc221-148">Saving should be done only if the user is not ready to post the shipment to HQ and needs a way to temporarily store the previously entered **Ship Now** data.</span></span> <span data-ttu-id="dc221-149">Kui kauplus on saadetise kinnitamiseks valmis, tuleb valida suvand **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="dc221-149">After the store is ready to confirm shipment, the **Commit** option should be selected.</span></span> <span data-ttu-id="dc221-150">See sisestab üleviimistellimuse saadetise HQ-sse, et vastuvõttev ladu saaks selle nüüd vastu vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="dc221-150">This posts the shipment of the transfer order in HQ so that the receiving warehouse will now be able to receive against it.</span></span> 

<span data-ttu-id="dc221-151">Kui kassa kasutaja on üleviimistellimust vastuvõttev ladu, saavad nad sisestada koguse **Saa kohe** otse kassast.</span><span class="sxs-lookup"><span data-stu-id="dc221-151">If the POS user is the receiving warehouse for a transfer order, they will be able to enter the **Receive Now** quantities from POS.</span></span> <span data-ttu-id="dc221-152">Vastuvõtva kaupluse sisestatud andmeid saab salvestada kohalikult või kooskõlastatud.</span><span class="sxs-lookup"><span data-stu-id="dc221-152">The data entered by the receiving store can be saved locally or committed.</span></span> <span data-ttu-id="dc221-153">Salvestamine peaks toimuma ainult juhul, kui kasutaja ei ole valmis sissetulekut sisestama HQ-sse ja vajab võimalust eelnevalt sisestatud andmed **Saa kohe** ajutiselt talletada.</span><span class="sxs-lookup"><span data-stu-id="dc221-153">Saving should be done only if the user is not ready to post the receipt to HQ and needs a way to temporarily store the previously entered **Receive Now** data.</span></span> <span data-ttu-id="dc221-154">See salvestab nüüd andmed kohalikult kasutaja kanali andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="dc221-154">This saves the receive now data locally to the user's channel database.</span></span> <span data-ttu-id="dc221-155">Pärast dokumendi töötlemist, kasutades suvandit **Kinnita**, saadetakse andmed **Saa kohe** HQ-sse ja üleviimistellimuse sissetulek sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="dc221-155">After the document is processed using the **Commit** option, the **Receive Now** data is sent to HQ and the transfer order receipt will be posted.</span></span> <span data-ttu-id="dc221-156">On oluline, et vastuvõttev kauplus saab ainult kinnitada vastuvõetavaid kogused, mis on saadetud kogustega võrdsed või sellest väiksemad.</span><span class="sxs-lookup"><span data-stu-id="dc221-156">It's important to note that the receiving store will be restricted to only being able to commit receive quantities that are equal to or less than shipped quantities.</span></span> <span data-ttu-id="dc221-157">Katse võtta vastu koguseid üleviimistellimusega, mida pole eelnevalt saadetud, põhjustab tõrkeid ja sissetulekut ei kinnitata HQ-s.</span><span class="sxs-lookup"><span data-stu-id="dc221-157">An attempt to receive quantities on a transfer order that have not previously shipped will result in errors and the receipt will not be confirmed in HQ.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="dc221-158">Laoinventuurid</span><span class="sxs-lookup"><span data-stu-id="dc221-158">Stock counts</span></span>

<span data-ttu-id="dc221-159">Laoinventuurid võivad olla plaanipärased või plaanivälised.</span><span class="sxs-lookup"><span data-stu-id="dc221-159">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="dc221-160">Plaanitud laoinventuurid algatab peakontor, mis määrab ka loendatavad kaubad.</span><span class="sxs-lookup"><span data-stu-id="dc221-160">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="dc221-161">Peakontor loob inventuuridokumendi, mida saab vastu võtta kaupluses, kus vaba laovaru kogused sisestatakse MPOS-is või pilve POS-is.</span><span class="sxs-lookup"><span data-stu-id="dc221-161">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="dc221-162">Plaanimata laoinventuurid käivitatakse kaupluses ja vaba laoseisu koguseid värskendatakse MPOS-is või pilve POS-is.</span><span class="sxs-lookup"><span data-stu-id="dc221-162">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="dc221-163">Erinevalt ajastatud laoinventuuridest puudub plaanimata laovarudel eelmääratletud kaupade loend.</span><span class="sxs-lookup"><span data-stu-id="dc221-163">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="dc221-164">Mõlemat tüüpi laoinventuuri lõpetamisel see kooskõlastatakse ja saadetakse peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="dc221-164">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="dc221-165">Peakontoris inventuur kinnitatakse ja sisestatakse eraldi etapina.</span><span class="sxs-lookup"><span data-stu-id="dc221-165">At the head office, the count is validated and posted as a separate step.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="dc221-166">Otsing varudest</span><span class="sxs-lookup"><span data-stu-id="dc221-166">Inventory lookup</span></span>

<span data-ttu-id="dc221-167">Jooksvat vaba tootekogust mitme kaupluse ja lao kohta saab vaadata lehelt **Otsing varudest**.</span><span class="sxs-lookup"><span data-stu-id="dc221-167">The current product quantity on hand for multiple stores and warehouses can be viewed on the **Inventory lookup** page.</span></span> <span data-ttu-id="dc221-168">Lisaks jooksvale vabale kaubavarule saab tulevasi lubamiseks saadaval (ATP) koguseid vaadata iga eraldi kaupluse kohta.</span><span class="sxs-lookup"><span data-stu-id="dc221-168">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="dc221-169">Selleks valige kauplus, mille ATP-d soovite vaadata, ja seejärel klõpsake valikut **Kaupluse saadavuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="dc221-169">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>