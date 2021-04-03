---
title: Ostutaotlused
description: See teema kirjeldab, kuidas on ostutaotlused rakenduses Planning Optimization toetatud.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 20b4012e054a25d7d21c6f017d8ebcf18f6ee28d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501074"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="13530-103">Ostutaotlused</span><span class="sxs-lookup"><span data-stu-id="13530-103">Purchase requisitions</span></span>

<span data-ttu-id="13530-104">Koondplaneerimine saab kinnitatud ostutaotlusi täiendada.</span><span class="sxs-lookup"><span data-stu-id="13530-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="13530-105">Seega ei pea kasutajad kasutama ostutaotluste katteks ostutellimuste loomise töövoogu.</span><span class="sxs-lookup"><span data-stu-id="13530-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="13530-106">Selle asemel saab ostutaotlusi katta koondplaneerimisega.</span><span class="sxs-lookup"><span data-stu-id="13530-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="13530-107">Selle funktsiooni tõttu saab ostutaotlus luua ostutellimuse, üleviimistellimuse või tootmistellimuse, sõltuvalt seotud tootele määratud väärtusest **Plaanitud tellimuse tüüp**.</span><span class="sxs-lookup"><span data-stu-id="13530-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="13530-108">Koondplaanide seadistamine taotluste lubamine</span><span class="sxs-lookup"><span data-stu-id="13530-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="13530-109">Koondplaani laovarude arvutamiseks taotluse kaasamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="13530-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="13530-110">Avage **Koondplaneerimine** \> **Seadistus** \> **Plaanid** \> **Koondplaanid**.</span><span class="sxs-lookup"><span data-stu-id="13530-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="13530-111">Looge või valige koondplaan.</span><span class="sxs-lookup"><span data-stu-id="13530-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="13530-112">Määrake FastTab-il **Üldine** suvandil **Kaasa taotlused** valikut *Jah*.</span><span class="sxs-lookup"><span data-stu-id="13530-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="13530-113">Korrake samme 2 ja 3 iga täiendava koondplaani puhul, kuhu soovite tellimused lisada.</span><span class="sxs-lookup"><span data-stu-id="13530-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="13530-114">Kinnitatud taotluste ajapiir</span><span class="sxs-lookup"><span data-stu-id="13530-114">Approved requisitions time fence</span></span>

<span data-ttu-id="13530-115">*Kinnitatud ostutellimuste ajapiir* määrab, kui palju (päevi) tagasi koondplaan kinnitatud täiendamistaotluste nõuet kaasab.</span><span class="sxs-lookup"><span data-stu-id="13530-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="13530-116">Saate määrata kinnitatud taotluse ajapiiri nii laovarude grupi tasemel kui ka koondplaani tasemel.</span><span class="sxs-lookup"><span data-stu-id="13530-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="13530-117">Laovarude grupi kinnitatud taotluse ajapiiri määramine</span><span class="sxs-lookup"><span data-stu-id="13530-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="13530-118">Avage **Koondplaneerimine** \> **Seadistus** \> **Laovarud** \> **Laovarude grupid**.</span><span class="sxs-lookup"><span data-stu-id="13530-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="13530-119">Looge või valige laogrupp.</span><span class="sxs-lookup"><span data-stu-id="13530-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="13530-120">Määrake kiirkaardil **Muu** väli **Kinnitatud ostutaotluste ajapiir (päevades)** päevade arvule, mis ajapiiri kaasata.</span><span class="sxs-lookup"><span data-stu-id="13530-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="13530-121">Korrake samme 2 ja 3 iga täiendava laovarude grupi jaoks, millele soovite kinnitatud ostutellimuste ajapiiri seadistada.</span><span class="sxs-lookup"><span data-stu-id="13530-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="13530-122">Individuaalsetele koondplaanidele kinnitatud taotluse ajapiiri määramine</span><span class="sxs-lookup"><span data-stu-id="13530-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="13530-123">Individuaalsele koondplaanile kinnitatud taotluse ajapiiri määramisel alistab säte kõigi rakendatavate laovarude grupi ajapiiri sätte.</span><span class="sxs-lookup"><span data-stu-id="13530-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="13530-124">Avage **Koondplaneerimine** \> **Seadistus** \> **Plaanid** \> **Koondplaanid**.</span><span class="sxs-lookup"><span data-stu-id="13530-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="13530-125">Looge või valige koondplaan.</span><span class="sxs-lookup"><span data-stu-id="13530-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="13530-126">Määrake kiirkaardil **Ajapiirid päevades** väli **Kinnitatud ostutaotluste ajapiir (päevades)** päevade arvule, mis ajapiiri kaasata.</span><span class="sxs-lookup"><span data-stu-id="13530-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="13530-127">Korrake samme 2 ja 3 iga täiendava koondplaani jaoks, millele soovite kinnitatud ostutellimuste ajapiiri seadistada.</span><span class="sxs-lookup"><span data-stu-id="13530-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13530-128">**Tulemas:** kinnitatud taotluste ajapiire teenuse Planning Optimization jaoks veel ei toetata.</span><span class="sxs-lookup"><span data-stu-id="13530-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="13530-129">Kuni neid toetatakse, ignoreeritakse kõiki väärtusi, mille sisestate väljale **Kinnitatud ostutaotluste ajapiir (päevades)**.</span><span class="sxs-lookup"><span data-stu-id="13530-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="13530-130">Sõltumatu tarne, sõltumata laovarude koodist</span><span class="sxs-lookup"><span data-stu-id="13530-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="13530-131">Ostutaotlused on alati kaetud sõltumatute plaanitud tellimustega, olenemata laovarude koodist.</span><span class="sxs-lookup"><span data-stu-id="13530-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="13530-132">Selline käitumine tagab ostutaotluste ja täiendustellimuste vahelise selge jälgimise ja töövoo.</span><span class="sxs-lookup"><span data-stu-id="13530-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="13530-133">Näide 1</span><span class="sxs-lookup"><span data-stu-id="13530-133">Example 1</span></span>

<span data-ttu-id="13530-134">Toode on häälestatud nii, et sellel oleks **katvuse koodi** väärtus *Min/max*. Sellel on järgmised varude ja ostutellimuse olekud:</span><span class="sxs-lookup"><span data-stu-id="13530-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="13530-135">Vaba kaubavaru kogus = 10.</span><span class="sxs-lookup"><span data-stu-id="13530-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="13530-136">Minimaalne laokogus = 15.</span><span class="sxs-lookup"><span data-stu-id="13530-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="13530-137">Maksimaalne laokogus = 20.</span><span class="sxs-lookup"><span data-stu-id="13530-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="13530-138">Olemas on ühe tüki ostutaotlus.</span><span class="sxs-lookup"><span data-stu-id="13530-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="13530-139">Selle taotlemise kuupäev on täna.</span><span class="sxs-lookup"><span data-stu-id="13530-139">It has a requested date of today.</span></span>

<span data-ttu-id="13530-140">Kui koondplaneerimine töötab, luuakse kaks plaanitud tellimust: üks 10 ühiku jaoks, et täiendada varud maksimaalse koguseni, ja üks tüki kohta, et ostutaotlust täiendada.</span><span class="sxs-lookup"><span data-stu-id="13530-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="13530-141">Näide 2</span><span class="sxs-lookup"><span data-stu-id="13530-141">Example 2</span></span>

<span data-ttu-id="13530-142">Toode on häälestatud nii, et sellel oleks **katvuse koodi** väärtus *Min/max*. Sellel on järgmised varude ja ostutellimuse olekud:</span><span class="sxs-lookup"><span data-stu-id="13530-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="13530-143">Vaba kaubavaru kogus = 17.</span><span class="sxs-lookup"><span data-stu-id="13530-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="13530-144">Minimaalne laokogus = 15.</span><span class="sxs-lookup"><span data-stu-id="13530-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="13530-145">Maksimaalne laokogus = 20.</span><span class="sxs-lookup"><span data-stu-id="13530-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="13530-146">Olemas on ühe tüki ostutaotlus.</span><span class="sxs-lookup"><span data-stu-id="13530-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="13530-147">Selle taotlemise kuupäev on täna.</span><span class="sxs-lookup"><span data-stu-id="13530-147">It has a requested date of today.</span></span>

<span data-ttu-id="13530-148">Kui koondplaneerimine töötab, luuakse ostutaotluse täiendamiseks üks plaanitud tellimus ühe tüki kohta.</span><span class="sxs-lookup"><span data-stu-id="13530-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="13530-149">Näide 3</span><span class="sxs-lookup"><span data-stu-id="13530-149">Example 3</span></span>

<span data-ttu-id="13530-150">Toode on seadistatud nii, et sellel on väärtus **Laovarude kood** väärtusega *Periood* ja perioodi pikkus on 7 päeva.</span><span class="sxs-lookup"><span data-stu-id="13530-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="13530-151">Sellel on järgmised varude, müügitellimuste ja ostutellimuste olekud:</span><span class="sxs-lookup"><span data-stu-id="13530-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="13530-152">Vaba kaubavaru kogus = 0.</span><span class="sxs-lookup"><span data-stu-id="13530-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="13530-153">Olemas on müügitellimus viiele eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="13530-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="13530-154">Selle on eeldatav lähetuskuupäev täna, millele on lisatud üks päev.</span><span class="sxs-lookup"><span data-stu-id="13530-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="13530-155">Olemas on kolme tüki ostutaotlus.</span><span class="sxs-lookup"><span data-stu-id="13530-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="13530-156">Selle taotlemise kuupäev on täna pluss kolm päeva.</span><span class="sxs-lookup"><span data-stu-id="13530-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="13530-157">Kui koondplaneerimine töötab, luuakse kaks plaanitud tellimust: üks kolme ühiku jaoks, et täiendada ostutaotlust ja üks viie ühiku jaoks, et müügitellimuse nõue taastada.</span><span class="sxs-lookup"><span data-stu-id="13530-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="13530-158">Pärast ostutaotlusega seotud plaanitud tellimuse kinnitamist edastab planeerimismootor sidumise ostutaotlusele.</span><span class="sxs-lookup"><span data-stu-id="13530-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="13530-159">Kui hiljem leitakse, et kinnitatud tellimusel puudub mõni ostutaotluse täitmiseks vajalik kogus, loob süsteem erinevuse jaoks uue plaanitud tellimuse.</span><span class="sxs-lookup"><span data-stu-id="13530-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="13530-160">Täpsemat teavet ostutaotluste kohta vt teemast [Ostutaotluste ülevaade](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="13530-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]