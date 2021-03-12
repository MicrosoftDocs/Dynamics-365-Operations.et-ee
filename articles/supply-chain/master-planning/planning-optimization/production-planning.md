---
title: Tootmise planeerimine
description: Selles teemas kirjeldatakse tootmise planeerimist ja selgitatakse, kuidas muuta plaanitud tootmistellimusi Planning Optimizationi abil.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992391"
---
# <a name="production-planning"></a><span data-ttu-id="8f782-103">Tootmise planeerimine</span><span class="sxs-lookup"><span data-stu-id="8f782-103">Production planning</span></span>

<span data-ttu-id="8f782-104">Planning Optimization toetab mitut tootmisstsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="8f782-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="8f782-105">Kui migreerite olemasolevalt sisse-ehitatud koondplaneerimise mootorilt, on oluline, et teaksite mõnda muutunud käitumist.</span><span class="sxs-lookup"><span data-stu-id="8f782-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="8f782-106">Plaanitud tootmistellimused</span><span class="sxs-lookup"><span data-stu-id="8f782-106">Planned production orders</span></span>

<span data-ttu-id="8f782-107">Kui koondplaneerimine loob plaanitud tellimuste täitmiseks nõuded, määratletakse tellimuse tüüp välja **Plaanitud tellimuse tüüp** väärtusega.</span><span class="sxs-lookup"><span data-stu-id="8f782-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="8f782-108">Kui välja **Plaanitud tellimuse tüüp** tüäärtuseks on seatud *Tootmine*, luuakse plaanitud tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="8f782-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="8f782-109">Need plaanitud tootmistellimused sisaldavad teavet aktiivse koosluse kohta (BOM) ja protsessi ID-d seostuvast tootmise seadistusest.</span><span class="sxs-lookup"><span data-stu-id="8f782-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="8f782-110">Koosluste nõuded</span><span class="sxs-lookup"><span data-stu-id="8f782-110">Requirements from BOMs</span></span>

<span data-ttu-id="8f782-111">Koondplaneerimise ajal arvestatakse koosluse teabega.</span><span class="sxs-lookup"><span data-stu-id="8f782-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="8f782-112">Plaani väljund hõlmab materjalitarnet, mis kataks seotud materjali nõudluse tootmisele.</span><span class="sxs-lookup"><span data-stu-id="8f782-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="8f782-113">Koondplaneerimise ajal kasutatakse praegust aktiivset kooslust tootmiseks vajalike materjalide määramiseks.</span><span class="sxs-lookup"><span data-stu-id="8f782-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="8f782-114">See samm tehakse läbi kõigi nõutava tootmistellimusega seotud koosluse struktuuri tasemetel.</span><span class="sxs-lookup"><span data-stu-id="8f782-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="8f782-115">Materjalivajadus täidetakse, kasutades saadaolevaid vabasid kaubavarusid, olemasolevaid tellimuse tarneid ja kinnitatud plaanitud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="8f782-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="8f782-116">Kui lisamaterjale vajatakse kus tahes, luuakse nõudluse katmiseks plaanitud tellimus.</span><span class="sxs-lookup"><span data-stu-id="8f782-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="8f782-117">Plaanimine kinnitamis ajal</span><span class="sxs-lookup"><span data-stu-id="8f782-117">Scheduling during firming</span></span>

<span data-ttu-id="8f782-118">Plaanitud tootmistellimused sisaldavad protsessi ID-d, mis on vajalik tootmise planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8f782-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="8f782-119">Samas planeerimise tugi plaanitud tellimustele käitamise ajal on ootel.</span><span class="sxs-lookup"><span data-stu-id="8f782-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="8f782-120">Protsessi ID-d kasutatakse plaanitud tootmistellimuste plaanimiseks tootmise ajal.</span><span class="sxs-lookup"><span data-stu-id="8f782-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="8f782-121">Seetõttu võib plaanitud tootmistellimuste täitmisaeg erineda plaanitud ja neist loodud kindlast tootmistellimuste täitmisajast, nagu on järgnevalt kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="8f782-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="8f782-122">**Plaanitud tootmistellimus** – täitmisaeg põhineb väljastatud toote staatilisel täitmisajal.</span><span class="sxs-lookup"><span data-stu-id="8f782-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="8f782-123">**Kinnistatud tootmistellimus** – täitmisaeg põhineb planeerimisel, mis kasutab protsessiteavet ja seotud ressursipiiranguid.</span><span class="sxs-lookup"><span data-stu-id="8f782-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="8f782-124">Lisateavet funktsiooni eeldatava saadavuse kohta vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8f782-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="8f782-125">Kui te sõltute tootmise funktsioonidest, mis ei ole veel Planning Optimizationi jaoks saadaval, saate jätkata integreeritud koondplaneerimise mootori kasutamist.</span><span class="sxs-lookup"><span data-stu-id="8f782-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="8f782-126">Erandit pole vaja.</span><span class="sxs-lookup"><span data-stu-id="8f782-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="8f782-127">Hilinemised</span><span class="sxs-lookup"><span data-stu-id="8f782-127">Delays</span></span>

<span data-ttu-id="8f782-128">Kui nõutava materjali täitmisaeg on pikem kui periood tänase kuupäeva ja materjalivajaduse kuupäeva vahel, siis nõutava materjali plaanitud tellimus ja seotud tootmistellimus hilinevad.</span><span class="sxs-lookup"><span data-stu-id="8f782-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="8f782-129">Plaanitud tellimuste puhul arvutatakse viivitus (päevades) väljastatud toote täitmisaja alusel.</span><span class="sxs-lookup"><span data-stu-id="8f782-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="8f782-130">Viivituse teavet levitatakse seejärel kõigi koosluse struktuuri tasemete kaudu.</span><span class="sxs-lookup"><span data-stu-id="8f782-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="8f782-131">Seega saate hilinenud toormaterjali mõju jälgida kogu tee kliendi müügitellimuseni.</span><span class="sxs-lookup"><span data-stu-id="8f782-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="8f782-132">Plaanitud tellimuste muutmine</span><span class="sxs-lookup"><span data-stu-id="8f782-132">Modifying planned orders</span></span>

<span data-ttu-id="8f782-133">Kui muudate plaanitud tellimuse teavet, saate järgmise teate: „Pange tähele, et plaanitud tellimustes käsitsi tehtud muudatuste mõju ei kajastu ülejäänud plaanis enne järgmise koondplaani käivitamist.”</span><span class="sxs-lookup"><span data-stu-id="8f782-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="8f782-134">Kui soovite muuta plaanitud tellimuse teavet ja vaadata mõju seotud materjalinõuetele, järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="8f782-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="8f782-135">Värskendage plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="8f782-135">Update the planned order.</span></span>
2. <span data-ttu-id="8f782-136">Kinnitage plaanitud tellimus.</span><span class="sxs-lookup"><span data-stu-id="8f782-136">Approve the planned order.</span></span>
3. <span data-ttu-id="8f782-137">Käivitage koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="8f782-137">Run master planning.</span></span>

<span data-ttu-id="8f782-138">Koondplaneerimise käivitamisel ei tohiks kasutada filtreid, kui kaasatud on plaanitud tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="8f782-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="8f782-139">Lisateabe saamiseks vaadake selle teema järgnevaid jaotisi [Filtrid](#filters).</span><span class="sxs-lookup"><span data-stu-id="8f782-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="8f782-140">Kui plaanitud tellimuse tarnekuupäev muudetakse hilisemaks kuupäevaks, võib nõudlus olla seotud uue plaanitud tellimusega.</span><span class="sxs-lookup"><span data-stu-id="8f782-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="8f782-141">Selline käitumine ilmneb siis, kui uus tarnekuupäev põhjustab seotud nõudluse viivitusi, kuid vastavalt täitmisaja sätetele võib viivitusi vältida.</span><span class="sxs-lookup"><span data-stu-id="8f782-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="8f782-142">Koosluse leht</span><span class="sxs-lookup"><span data-stu-id="8f782-142">Explosion page</span></span>

<span data-ttu-id="8f782-143">Saate kasutada lehte **Kooslus**, et analüüsida nõudlust, mis on vajalik konkreetse tootmistellimuse või plaanitud tootmistellimuse, seotud laovarude ja sidumisteabe jaoks.</span><span class="sxs-lookup"><span data-stu-id="8f782-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="8f782-144">Teavet lehel **Kooslus** uuendatakse koondplaneerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="8f782-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="8f782-145">Teavet ei saa uuendada otse lehel **Kooslus**.</span><span class="sxs-lookup"><span data-stu-id="8f782-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="8f782-146">Filtrid</span><span class="sxs-lookup"><span data-stu-id="8f782-146">Filters</span></span>

<span data-ttu-id="8f782-147">Tootmisega seotud stsenaariumite plaanimiseks on soovitatav vältida filtreeritud koondplaneerimise käitamist.</span><span class="sxs-lookup"><span data-stu-id="8f782-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="8f782-148">Kindlustamaks, et teenusel Planning Optimization oleks õige tulemuse arvutamiseks vajalik teave, peate kaasama kõik tooted, millel on mis tahes seos toodetega plaanitud tellimuse koosluse struktuuris.</span><span class="sxs-lookup"><span data-stu-id="8f782-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="8f782-149">Kuigi sõltuvad alamüksused tuvastatakse ja kaasatakse koondplaneerimisel automaatselt, siis integreeritud koondplaneerimise mootori kasutamisel plaanimise optimeerimine seda tegevust ei tee.</span><span class="sxs-lookup"><span data-stu-id="8f782-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="8f782-150">Näiteks kui toote A koosluse struktuurist kasutatakse ka üksikut polti ka toote B tootmiseks, peavad filtrisse olema kaasatud kõik tooted, mis on toodete A ja B koosluse struktuuris.</span><span class="sxs-lookup"><span data-stu-id="8f782-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="8f782-151">Kuna kõigi toodete filtri osa kindlustamine võib olla väga keerukas, on soovitatav vältida filtreeritud koondplaneerimise käivitamist tootmistellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="8f782-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>
