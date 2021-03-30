---
title: Koondplaneerimise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada koondplaneerimisega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: db336946873fa1b5cc3f669823541af8cab4115b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216101"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="ac204-103">Koondplaneerimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="ac204-103">Troubleshoot master planning</span></span>

<span data-ttu-id="ac204-104">Selles teemas kirjeldatakse, kuidas lahendada koondplaneerimisega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="ac204-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="ac204-105">Koosluse tükeldamine käitub erinevalt kinnitatud tootmistellimustest ja plaanitud tootmistellimustest käsitsi loodud töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="ac204-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ac204-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ac204-106">Issue description</span></span>

<span data-ttu-id="ac204-107">Kui tootmistellimus on kinnitatud, ei tükeldata kaupu koosluse tükeldamisel.</span><span class="sxs-lookup"><span data-stu-id="ac204-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="ac204-108">Kuid kui loote käsitsi töötellimuse ja seejärel hindate tootmistellimuse, siis kaubad tükeldatakse.</span><span class="sxs-lookup"><span data-stu-id="ac204-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ac204-109">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ac204-109">Issue resolution</span></span>

<span data-ttu-id="ac204-110">Süsteem töötab ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="ac204-110">The system is working as expected.</span></span> <span data-ttu-id="ac204-111">Tükeldamine, mis ilmneb tootmistellimuse kinnitamisel, osutab plaanitud tellimusele, kuid ei ilmne, et plaanitud tellimus on praegu selles juhtumis kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="ac204-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="ac204-112">Kui tootmistellimus on hinnatud, käivitatakse tükeldamine vabastatud tootmistellimuselt, kus pole plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="ac204-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="ac204-113">Viivituse väärtust ei uuendata, kui plaanin plaanitud tellimust uuesti planeerida.</span><span class="sxs-lookup"><span data-stu-id="ac204-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="ac204-114">Plaanitud tellimuste viivituse uuendamiseks avage planeeritud tellimuse **Ümberplaneerimine** dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="ac204-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="ac204-115">Veenduge, et FastTabil **Tükeldamine** oleks suvandi **Teosta tükeldamine pärast ümberplaneerimist** väärtuseks seatud *Jah*.</span><span class="sxs-lookup"><span data-stu-id="ac204-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="ac204-116">Tootmise planeerimisel ei arvestata ohutusvaru, mis on seatud kauba laovarule fikseeritud tarne puhul.</span><span class="sxs-lookup"><span data-stu-id="ac204-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ac204-117">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ac204-117">Issue description</span></span>

<span data-ttu-id="ac204-118">Koondplaneerimine vaatleb ohutusvaru.</span><span class="sxs-lookup"><span data-stu-id="ac204-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="ac204-119">Siiski eiratakse ohutusvaru plaanitud tootmistellimuste planeerimisel.</span><span class="sxs-lookup"><span data-stu-id="ac204-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ac204-120">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ac204-120">Issue resolution</span></span>

<span data-ttu-id="ac204-121">Marginaale arvestatakse ainult koondplaneerimise käigus, mitte käsitsi planeerimisel.</span><span class="sxs-lookup"><span data-stu-id="ac204-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="ac204-122">Veerised on kavandatud toimima puhvrina planeerimise faasis, et anda osa "marginaali" tegeliku protsessi jaoks.</span><span class="sxs-lookup"><span data-stu-id="ac204-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="ac204-123">Soovitud tulemuse saamiseks saate marginaali eemaldada.</span><span class="sxs-lookup"><span data-stu-id="ac204-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="ac204-124">Seejärel tuleb protsessi uuendada nii, et see sisaldaks soovitud kellaaega (nt ooteaeg).</span><span class="sxs-lookup"><span data-stu-id="ac204-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="ac204-125">Nii koondplaneerimine kui ka käsitsi planeerimine peaksid seejärel esitama sama tulemuse.</span><span class="sxs-lookup"><span data-stu-id="ac204-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="ac204-126">Plaanitud tellimused luuakse ka siis, kui meil on laos ja tootmistellimustes kaubad juba olemas.</span><span class="sxs-lookup"><span data-stu-id="ac204-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="ac204-127">Võimalik, et saate selle probleemi lahendada, suurendades vastavate gruppide **Positiivsete päevade** väärtust **Laovarude grupi** lehel.</span><span class="sxs-lookup"><span data-stu-id="ac204-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="ac204-128">See muudatus paneb süsteemi määratlema, kas vaba kaubavaru saab nõudluse jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="ac204-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="ac204-129">Seejärel ei looda laos olevate kaupade jaoks uut plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="ac204-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="ac204-130">Koondplaneerimise käigus ei arvestata võimsuse piiranguid ja planeeritakse rohkem kui saadaolev võimsus.</span><span class="sxs-lookup"><span data-stu-id="ac204-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ac204-131">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ac204-131">Issue description</span></span>

<span data-ttu-id="ac204-132">Kui kasutate operatsiooni planeerimist, kus on piiratud võimsus ja kui protsess määrab nii ressursirühma kui ka üksikute ressursside jaoks nõuete kombinatsiooni, on väike võimalus üle broneerida, kuna algoritm kontrollib võimsuse konflikte.</span><span class="sxs-lookup"><span data-stu-id="ac204-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="ac204-133">See ülebroneerimine võib ilmneda, kui kasutate koondplaneerimise käivitamiseks abilisi.</span><span class="sxs-lookup"><span data-stu-id="ac204-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="ac204-134">See on kõige tõenäolisem juhul, kui on palju töid, millel on suhteliselt lühike käitusaeg.</span><span class="sxs-lookup"><span data-stu-id="ac204-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ac204-135">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ac204-135">Issue resolution</span></span>

<span data-ttu-id="ac204-136">Kui on oluline, et operatsiooni planeerimisel ei esineks ülebroneerimist, saate koondplaneerimise planeerimisosa muuta ühekordseks, lülitades sisse **Täpne piiratud võimsus operatsiooni planeerimiseks** valiku **Koondplaneerimise parameetrite** lehel.</span><span class="sxs-lookup"><span data-stu-id="ac204-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="ac204-137">See valik pole vaikimisi saadaval.</span><span class="sxs-lookup"><span data-stu-id="ac204-137">This option isn't available by default.</span></span> <span data-ttu-id="ac204-138">Peate selle lehele käsitsi lisama, kasutades isikupärastamise funktsioone.</span><span class="sxs-lookup"><span data-stu-id="ac204-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="ac204-139">Selle suvandi kasutamisel toimub planeerimine aeglasemalt, kuna puudub paralleelne töötlemine.</span><span class="sxs-lookup"><span data-stu-id="ac204-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="ac204-140">Plaanitud tellimused võtaksid uuendamiseks kaua aega.</span><span class="sxs-lookup"><span data-stu-id="ac204-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ac204-141">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ac204-141">Issue description</span></span>

<span data-ttu-id="ac204-142">Plaanitud tellimuse vajaduse koguse ja/või tarnekuupäeva uuendamisel võtab see tavaliselt aega vähemalt 30 sekundit, et värskendust salvestada.</span><span class="sxs-lookup"><span data-stu-id="ac204-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ac204-143">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ac204-143">Issue resolution</span></span>

<span data-ttu-id="ac204-144">See on teadaolev probleem sisseehitatud koondplaneerimise mootoriga.</span><span class="sxs-lookup"><span data-stu-id="ac204-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="ac204-145">Selle põhjuseks on aluseks olev automaatne tükeldamine koosluse struktuuri kaudu redigeerimisel.</span><span class="sxs-lookup"><span data-stu-id="ac204-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="ac204-146">Seda probleemi käsitletakse planeerimise optimeerimisel, kus planeerija saab vastavaid tellimusi värskendada ja kinnitada ning soovi korral käivitab planeerimise käivitamise, et värskendada aluseks oleva koosluse struktuuri jaoks plaanitud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="ac204-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="ac204-147">Üks viis jõudluse parandamiseks sisseehitatud koondplaneerimise mootoriga on teha järgmist:</span><span class="sxs-lookup"><span data-stu-id="ac204-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="ac204-148">Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.</span><span class="sxs-lookup"><span data-stu-id="ac204-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="ac204-149">Valige plaan.</span><span class="sxs-lookup"><span data-stu-id="ac204-149">Select a plan.</span></span>
1. <span data-ttu-id="ac204-150">Laiendage **Ajapiir päevades** FastTab.</span><span class="sxs-lookup"><span data-stu-id="ac204-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="ac204-151">Seadke **Tükeldamine** väärtusele *Jah* ja seadke selle sätte all oleva välja väärtuseks 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ac204-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="ac204-152">See piirab selle koondplaani jaoks teostatavate tükeldamiste perioodi ühele päevale.</span><span class="sxs-lookup"><span data-stu-id="ac204-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]