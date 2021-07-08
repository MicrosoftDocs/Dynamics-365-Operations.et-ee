---
title: Konteineri pakkimise strateegiad
description: Selles teemas kirjeldatakse konteinerite pakkimise strateegiate vahelisi erinevusi ja tuuakse näiteid.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292757"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="6dc7b-103">Konteineri pakkimise strateegiad</span><span class="sxs-lookup"><span data-stu-id="6dc7b-103">Container packing strategies</span></span>

<span data-ttu-id="6dc7b-104">*Konteineri pakkimisstrateegia* on strateegia, mida saate kasutada kauba konteinerite eraldamise määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="6dc7b-105">See teema selgitab erinevusi strateegiate *Pakenda kõikidesse avatud konteineritesse* ja *Pakenda ainult praegusesse konteinerisse*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="6dc7b-106">**Pakenda kõikidesse avatud konteineritesse** – süsteem peab kontrollima kõiki avatud konteinereid, mis on konteinerite tsükli jooksul juba loodud, veendumaks, et kaup mahub ühte neist.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="6dc7b-107">Pakkimise ajal kontrollib süsteem iga kaupa, kas see mahub mõnda varem loodud konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="6dc7b-108">Kui kaup ei mahu olemasolevasse konteinerisse, loob süsteem uue konteineri ja jätkab tööd seni, kuni see on kogu tellimuse pakkimise lõpetanud.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="6dc7b-109">Näiteks *n* tellitud üksust vajavad konteinerite loomist.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="6dc7b-110">Juhtumi puhul kontrollib süsteem iga kord kauba, mis ei mahu olemasolevasse konteinerisse, töötlemisel kokku (\[(*n* – 1) × (*n* + 1)\] ÷ 2) kontrolli, et hinnata, kas kaup mahub olemasolevatesse konteineritesse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="6dc7b-111">**Pakenda ainult praegusesse konteinerisse** – süsteem peab kontrollima ainult viimati loodud konteinerit, et veenduda, et üksus sellesse mahuks.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="6dc7b-112">Pakkimise ajal kontrollib süsteem iga kaupa, kas see mahub viimati loodud konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="6dc7b-113">Kui kaup ei mahu konteinerisse, loob süsteem uue konteineri ja jätkab tööd seni, kuni see on kogu tellimuse pakkimise lõpetanud.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="6dc7b-114">Näiteks *n* tellitud üksust vajavad konteinerite loomist.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="6dc7b-115">Juhtumi puhul teeb süsteem kokku (*n* – 1) kontrolli, et hinnata, kas kaup mahub konteineritesse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="6dc7b-116">Konteinerite pakkimise strateegiate voo näide</span><span class="sxs-lookup"><span data-stu-id="6dc7b-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="6dc7b-117">Saate konteineri jaoks seadistada järgmised üksused.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="6dc7b-118">Kaup</span><span class="sxs-lookup"><span data-stu-id="6dc7b-118">Item</span></span> | <span data-ttu-id="6dc7b-119">Füüsilised dimensioonid (laius × sügavus × kõrgus)</span><span class="sxs-lookup"><span data-stu-id="6dc7b-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="6dc7b-120">Kaal</span><span class="sxs-lookup"><span data-stu-id="6dc7b-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="6dc7b-121">HDMI kaabel 6'</span><span class="sxs-lookup"><span data-stu-id="6dc7b-121">HDMI Cable 6'</span></span> | <span data-ttu-id="6dc7b-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="6dc7b-122">1 × 1 × 1</span></span> | <span data-ttu-id="6dc7b-123">1</span><span class="sxs-lookup"><span data-stu-id="6dc7b-123">1</span></span> |
| <span data-ttu-id="6dc7b-124">HDMI kaabel 12'</span><span class="sxs-lookup"><span data-stu-id="6dc7b-124">HDMI Cable 12'</span></span> | <span data-ttu-id="6dc7b-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="6dc7b-125">2 × 1 × 1</span></span> | <span data-ttu-id="6dc7b-126">1</span><span class="sxs-lookup"><span data-stu-id="6dc7b-126">1</span></span> |
| <span data-ttu-id="6dc7b-127">HDMI kaabel 18'</span><span class="sxs-lookup"><span data-stu-id="6dc7b-127">HDMI Cable 18'</span></span> | <span data-ttu-id="6dc7b-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="6dc7b-128">3 × 1 × 1</span></span> | <span data-ttu-id="6dc7b-129">2</span><span class="sxs-lookup"><span data-stu-id="6dc7b-129">2</span></span> |

<span data-ttu-id="6dc7b-130">Seadistate ka järgmise pakendi jaoks kasutatava kasti.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="6dc7b-131">Konteiner</span><span class="sxs-lookup"><span data-stu-id="6dc7b-131">Container</span></span> | <span data-ttu-id="6dc7b-132">Füüsilised dimensioonid (pikkus × laius × kõrgus)</span><span class="sxs-lookup"><span data-stu-id="6dc7b-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="6dc7b-133">Kaal</span><span class="sxs-lookup"><span data-stu-id="6dc7b-133">Weight</span></span> | <span data-ttu-id="6dc7b-134">Maht</span><span class="sxs-lookup"><span data-stu-id="6dc7b-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="6dc7b-135">Keskmine kast</span><span class="sxs-lookup"><span data-stu-id="6dc7b-135">Medium Box</span></span> | <span data-ttu-id="6dc7b-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="6dc7b-136">6 × 3 × 2</span></span> | <span data-ttu-id="6dc7b-137">10</span><span class="sxs-lookup"><span data-stu-id="6dc7b-137">10</span></span> | <span data-ttu-id="6dc7b-138">100</span><span class="sxs-lookup"><span data-stu-id="6dc7b-138">100</span></span> |

<span data-ttu-id="6dc7b-139">Lõpuks seadistate tellimuse, mis sisaldab järgmisi tooteid ja koguseid.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="6dc7b-140">Müügitellimuse rida</span><span class="sxs-lookup"><span data-stu-id="6dc7b-140">Sales order line</span></span> | <span data-ttu-id="6dc7b-141">Kogus</span><span class="sxs-lookup"><span data-stu-id="6dc7b-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="6dc7b-142">HDMI kaabel 12'</span><span class="sxs-lookup"><span data-stu-id="6dc7b-142">HDMI Cable 12'</span></span> | <span data-ttu-id="6dc7b-143">9</span><span class="sxs-lookup"><span data-stu-id="6dc7b-143">9</span></span> |
| <span data-ttu-id="6dc7b-144">HDMI kaabel 18'</span><span class="sxs-lookup"><span data-stu-id="6dc7b-144">HDMI Cable 18'</span></span> | <span data-ttu-id="6dc7b-145">8</span><span class="sxs-lookup"><span data-stu-id="6dc7b-145">8</span></span> |
| <span data-ttu-id="6dc7b-146">HDMI kaabel 6'</span><span class="sxs-lookup"><span data-stu-id="6dc7b-146">HDMI Cable 6'</span></span> | <span data-ttu-id="6dc7b-147">13</span><span class="sxs-lookup"><span data-stu-id="6dc7b-147">13</span></span> |

<span data-ttu-id="6dc7b-148">Järgmine tabel võtab kokku, kuidas konteinerite loomine toimib, kui kasutate strateegiat *Pakenda kõikidesse avatud konteineritesse* ja kui kasutate strateegiat *Pakenda ainult praegusesse konteinerisse*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="6dc7b-149">Pakitakse kõigisse avatud konteineritesse</span><span class="sxs-lookup"><span data-stu-id="6dc7b-149">Pack into all open containers</span></span> | <span data-ttu-id="6dc7b-150">Pakenda praegusesse konteinerisse</span><span class="sxs-lookup"><span data-stu-id="6dc7b-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="6dc7b-151">HDMI kaabel 12':</span><span class="sxs-lookup"><span data-stu-id="6dc7b-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="6dc7b-152">Uue konteineri tüübi loomine, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="6dc7b-153">Asetage 9 ea konteinerisse CONT0001.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="6dc7b-154">HDMI kaabel 12':</span><span class="sxs-lookup"><span data-stu-id="6dc7b-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="6dc7b-155">Uue konteineri tüübi loomine, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="6dc7b-156">Asetage 9 ea konteinerisse CONT0001.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="6dc7b-157">HDMI kaabel 18':</span><span class="sxs-lookup"><span data-stu-id="6dc7b-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="6dc7b-158">Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0001.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="6dc7b-159">Uue konteineri tüübi loomine, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="6dc7b-160">Asetage 5 ea konteinerisse CONT0002.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="6dc7b-161">Uue konteineri tüübi loomine, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="6dc7b-162">Asetage 3 ea konteinerisse CONT0003.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="6dc7b-163">HDMI kaabel 18':</span><span class="sxs-lookup"><span data-stu-id="6dc7b-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="6dc7b-164">Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0001.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="6dc7b-165">Uue konteineri tüübi loomine, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="6dc7b-166">Asetage 5 ea konteinerisse CONT0002.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="6dc7b-167">Uue konteineri tüübi loomine, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="6dc7b-168">Asetage 3 ea konteinerisse CONT0003.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="6dc7b-169">HDMI kaabel 6':</span><span class="sxs-lookup"><span data-stu-id="6dc7b-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="6dc7b-170">Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0001.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="6dc7b-171">Asetage 1 ea konteinerisse CONT0001.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="6dc7b-172">Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0002.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="6dc7b-173">Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0003.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="6dc7b-174">Asetage 4 ea konteinerisse CONT0003.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="6dc7b-175">Uue konteineri tüübi loomine, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="6dc7b-176">Asetage 8 ea konteinerisse CONT0004.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="6dc7b-177">HDMI kaabel 6':</span><span class="sxs-lookup"><span data-stu-id="6dc7b-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="6dc7b-178">Kontrollige, kas kaup võiks mahtuda konteinerisse CONT0003.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="6dc7b-179">Asetage 4 ea konteinerisse CONT0003.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="6dc7b-180">Uue konteineri tüübi loomine, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="6dc7b-181">Asetage 9 ea konteinerisse CONT0004.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="6dc7b-182">Näidisstsenaarium - ühe tellimuse pakendamine ühte konteinerisse</span><span class="sxs-lookup"><span data-stu-id="6dc7b-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="6dc7b-183">Selles jaotises on toodud stsenaarium, kus süsteem on seadistatud konsolideerima mitut tellimust ühte saadetisse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="6dc7b-184">Seega tehakse konteinerite kogum müügitellimusest, et tagada, et iga tellimus, mis sisaldab mitut toodet, pakitakse eraldi konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="6dc7b-185">See funktsioon võimaldab teil käsitleda stsenaariume, kus peate igasse konteinerisse pakkima ainult ühe müügitellimuse, nii et jaotuskeskus saab jaekaupluste vahel ristlaadida täiskonteinereid.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="6dc7b-186">Lisaks jaemüügi stsenaariumidele (kaupluste tellimus ja saatmine jaotuskeskusesse ristlaadimiseks) kasutatakse seda tehnikat tavaliselt ka kulusäästlikes tarneahelates (müügitellimus ajamahuka tootmisrea kohta).</span><span class="sxs-lookup"><span data-stu-id="6dc7b-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="6dc7b-187">See stsenaarium näitab, kuidas saate vähendada konteinerite arvu, mida hinnatakse pakkimisel kasutates konteinerite loomisel strateegiat *Pakenda ainult praegusesse konteinerisse*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6dc7b-188">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="6dc7b-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="6dc7b-189">Lülitage süsteemis sisse funktsioon Konsolideeri saadetised</span><span class="sxs-lookup"><span data-stu-id="6dc7b-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="6dc7b-190">See stsenaarium kasutab funktsiooni *Konsolideeri saadetised*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="6dc7b-191">Kui see funktsioon ei ole juba teie süsteemis saadaval, peate selle [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="6dc7b-192">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="6dc7b-192">Make demo data available</span></span>

<span data-ttu-id="6dc7b-193">See stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6dc7b-194">Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="6dc7b-195">Konteineritüüpide kontrollimine või loomine</span><span class="sxs-lookup"><span data-stu-id="6dc7b-195">Inspect or create container types</span></span>

<span data-ttu-id="6dc7b-196">Oma konteineritüüpide kontrollimiseks või uute konteineritüüpide loomiseks (kui need on nõutud) järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-197">Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteinerite tüübid**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="6dc7b-198">Kontrollige, et kõik järgnevad konteineritüübid on demoandmetes saadaval.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="6dc7b-199">Redigeerige või looge konteineritüüpe vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="6dc7b-200">Konteineri tüüp 1:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-200">Container type 1:</span></span>

        - <span data-ttu-id="6dc7b-201">**Konteineri tüübi kood:** *Box-Large*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="6dc7b-202">**Kirjeldus:** *suur kast*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="6dc7b-203">**Maksimaalne netokaal:** *100*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="6dc7b-204">**Maht:** *400*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="6dc7b-205">**Pikkus:** *4*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-205">**Length:** *4*</span></span>
        - <span data-ttu-id="6dc7b-206">**Laius:** *10*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-206">**Width:** *10*</span></span>
        - <span data-ttu-id="6dc7b-207">**Kõrgus:** *10*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-207">**Height:** *10*</span></span>

    - <span data-ttu-id="6dc7b-208">Konteineri tüüp 2:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-208">Container type 2:</span></span>

        - <span data-ttu-id="6dc7b-209">**Konteineri tüübi kood:** *Box-Medium*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="6dc7b-210">**Kirjeldus:** *keskmine kast*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="6dc7b-211">**Maksimaalne netokaal:** *50*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="6dc7b-212">**Maht:** *200*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="6dc7b-213">**Pikkus:** *2*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-213">**Length:** *2*</span></span>
        - <span data-ttu-id="6dc7b-214">**Laius:** *10*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-214">**Width:** *10*</span></span>
        - <span data-ttu-id="6dc7b-215">**Kõrgus:** *10*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-215">**Height:** *10*</span></span>

    - <span data-ttu-id="6dc7b-216">Konteineri tüüp 3:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-216">Container type 3:</span></span>

        - <span data-ttu-id="6dc7b-217">**Konteineri tüübi kood:** *Box-Small*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="6dc7b-218">**Kirjeldus:** *väike kast*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="6dc7b-219">**Maksimaalne netokaal:** *20*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="6dc7b-220">**Maht:** *100*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="6dc7b-221">**Pikkus:** *1*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-221">**Length:** *1*</span></span>
        - <span data-ttu-id="6dc7b-222">**Laius:** *10*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-222">**Width:** *10*</span></span>
        - <span data-ttu-id="6dc7b-223">**Kõrgus:** *10*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="6dc7b-224">Konteinerigruppide kontrollimine või loomine</span><span class="sxs-lookup"><span data-stu-id="6dc7b-224">Inspect or create container groups</span></span>

<span data-ttu-id="6dc7b-225">Oma konteinerigruppide kontrollimiseks või uute konteinerigruppide loomiseks (kui need on nõutud) järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-226">Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteinerigrupid**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="6dc7b-227">Kontrollige, et kõik järgnevad konteinerigrupid on demoandmetes saadaval.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="6dc7b-228">Kui see pole saadaval, valige loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="6dc7b-229">**Konteinerigrupi ID:** *Boxes*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="6dc7b-230">**Kirjeldus:** *karbi suurused*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="6dc7b-231">Konteinerigrupi **Kastid** kiirkaardil *Üksikasjad* veenduge, et järgmised read on olemas.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="6dc7b-232">Kui ei, valige lisamiseks suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="6dc7b-233">Rida 1:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-233">Line 1:</span></span>

        - <span data-ttu-id="6dc7b-234">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="6dc7b-235">**Konteineri tüüp:** *Box-Large*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="6dc7b-236">**Konteineri kasutamise protsent:** *100*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="6dc7b-237">Rida 2:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-237">Line 2:</span></span>

        - <span data-ttu-id="6dc7b-238">**Järjekorranumber:** *2*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="6dc7b-239">**Konteineri tüüp:** *Box-Medium*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="6dc7b-240">**Konteineri kasutamise protsent:** *100*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="6dc7b-241">Rida 3:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-241">Line 3:</span></span>

        - <span data-ttu-id="6dc7b-242">**Järjekorranumber:** *3*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="6dc7b-243">**Konteineri tüüp:** *Box-Small*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="6dc7b-244">**Konteineri kasutamise protsent:** *100*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="6dc7b-245">Looge uus konteineri koostemall</span><span class="sxs-lookup"><span data-stu-id="6dc7b-245">Create a new container build template</span></span>

<span data-ttu-id="6dc7b-246">Uue konteineri koostemalli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-247">Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteineri koostemall**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="6dc7b-248">Valige **Uus**, et luua konteineri koostemall, kus on järgmised sätted:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="6dc7b-249">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6dc7b-250">**Konteineri malli ID:** *Box*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="6dc7b-251">**Konteinerigrupi ID:** *Boxes*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="6dc7b-252">**Aluspäringu tüübid:** *müügi eraldusrida*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="6dc7b-253">**Vooetapi kood:** *234*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="6dc7b-254">**Tükeldatud valiku lubamine:** *jah*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="6dc7b-255">**Konteineri pakkimisstrateegia:** *pakenda ainult praegusesse konteinerisse*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="6dc7b-256">**Pakendamine direktiivi ühikute kaupa:** *ei*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="6dc7b-257">Kuigi uue malli rida on endiselt valitud, valige tegevuspaanil **Muuda päringut**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="6dc7b-258">Kuvatakse standardne päringu redaktori dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="6dc7b-259">Järgmiste sätetega rea ​​lisamiseks valige vahekaardil **Sortimine** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="6dc7b-260">**Tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="6dc7b-261">**Tuletatud tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="6dc7b-262">**Väli:** *Tellimuse number*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="6dc7b-263">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6dc7b-264">Kõigi teiste avatud konteinerite rattasõidu vältimiseks ja protsessi kiirendamiseks, kontrollides korraga ühte konteinerit, kasutage lisaks tellimisnumbri järgi sorteerimisele ka strateegiat *Pakenda ainult praegusesse konteinerisse*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="6dc7b-265">See kombinatsioon töötab töömallis nagu tööpaus.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="6dc7b-266">Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="6dc7b-267">Kuigi uue malli rida on endiselt valitud, valige tegevuspaanil **Konteinerite segamise piirangud**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="6dc7b-268">Nüüd lisate piirangu, mis asetab kaubad ühest tellimusest ühte konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="6dc7b-269">Mis tahes muu tellimuse kaubad pannakse eraldi konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="6dc7b-270">Valige **Uus**, et luua segamsie piirangud, kus on järgmised sätted:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="6dc7b-271">**Tabel:** *Müügitellimused*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="6dc7b-272">**Valige väli:** *SalesId* (väli kuvatakse ruudustikus *müügitellimusena*.)</span><span class="sxs-lookup"><span data-stu-id="6dc7b-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="6dc7b-273">Piirangu lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="6dc7b-274">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="6dc7b-275">Voomalli häälestamine konteinerite koostamise jaoks</span><span class="sxs-lookup"><span data-stu-id="6dc7b-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="6dc7b-276">Voomalli seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-277">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="6dc7b-278">Määrake loendi paani välja **Voomalli tüüp** suvandiks *Lähetamine*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="6dc7b-279">Valige loendist **63 konteinerite loomise** mall.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="6dc7b-280">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6dc7b-281">Otsige kiirkaardi **Meetodid** veerust **Valitud meetodid**, järgmine rida:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="6dc7b-282">**Meetodi nimi:** *konteinerisse määramine*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="6dc7b-283">**Nimi:** *konteinerisse määramine*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="6dc7b-284">Seadke rea välja **Vooetapi kood** väärtuseks *234*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="6dc7b-285">Töömalli häälestamine</span><span class="sxs-lookup"><span data-stu-id="6dc7b-285">Set up a work template</span></span>

<span data-ttu-id="6dc7b-286">Töömalli seadistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-287">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6dc7b-288">Seadke välja **Töökäsu tüüp** valikuks *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="6dc7b-289">Ruudustikus **Ülevaade** leidke ja valige töömall, mida tuleks kasutada üksiktellimuse pakkimiseks ühte konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="6dc7b-290">Valige selle stsenaariumi jaoks mall **63 Ettevalmistamiseks konteinerisse**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="6dc7b-291">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="6dc7b-292">Kuvatakse standardne päringu redaktori dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="6dc7b-293">Vahekaardil **Sortimine** lisage järgmised read:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="6dc7b-294">Rida 1:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-294">Line 1:</span></span>

        - <span data-ttu-id="6dc7b-295">**Tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="6dc7b-296">**Tuletatud tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="6dc7b-297">**Väli:** *Saadetise ID*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="6dc7b-298">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="6dc7b-299">Rida 2:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-299">Line 2:</span></span>

        - <span data-ttu-id="6dc7b-300">**Tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="6dc7b-301">**Tuletatud tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="6dc7b-302">**Väli:** *Tellimuse number*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="6dc7b-303">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="6dc7b-304">Rida 3:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-304">Line 3:</span></span>

        - <span data-ttu-id="6dc7b-305">**Tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="6dc7b-306">**Tuletatud tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="6dc7b-307">**Väli:** *konteineri ID*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="6dc7b-308">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="6dc7b-309">Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="6dc7b-310">Teile kuvatakse järgmine teade: „Grupeerimine lähtestatakse, kas soovite jätkata?”</span><span class="sxs-lookup"><span data-stu-id="6dc7b-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="6dc7b-311">Jätkamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="6dc7b-312">Kui **63 Ettevalmistamiseks konteinerisse** on veel valitud, valige tegevuspaanil **Tööpäiste piirid**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="6dc7b-313">Nüüd rakendate töö katkestamiseks sätteid, nii et tellimuse iga konteiner on lingitud ühe töötellimusega.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="6dc7b-314">Märkige ruut **Rühmita selle välja järgi** iga rea puhul lehel **Tööpäise piirid** (**Saadetise ID**, **Tellimuse number** ja **Konteineri ID**).</span><span class="sxs-lookup"><span data-stu-id="6dc7b-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="6dc7b-315">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="6dc7b-316">Seadistage saadetise konsolideerimise põhimõtted</span><span class="sxs-lookup"><span data-stu-id="6dc7b-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="6dc7b-317">Saadetise konsolideerimise poliitika seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-318">Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="6dc7b-319">Seadke loendi paanil välja **Poliitika tüüp** väärtuseks *Müügitellimus*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="6dc7b-320">Valige loendist **vaike** poliitika.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="6dc7b-321">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6dc7b-322">Valige kiirkaardi **Konsolideerimise väljad** loendist **Valitud väljad** rida, mille välja **Välja nimi** väärtuseks on seatud *Tellimuse number*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="6dc7b-323">Valige nupp **Eemalda** ![Vasak nool](media/backward-button.png), et teisaldada väli loendisse **Allesjäänud väljad**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="6dc7b-324">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="6dc7b-325">Seadistage toote füüsilised mõõtmed</span><span class="sxs-lookup"><span data-stu-id="6dc7b-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="6dc7b-326">Selles stsenaariumis kasutatavate toodete füüsiliste mõõtmete häälestamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-327">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6dc7b-328">Valige toode, kus **kaubakoodi** väli on seadistatud valikule *A0001*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="6dc7b-329">Valige toimingupaani vahekaardi **Varude haldamine** grupis **Ladu** suvand **Füüsilised dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="6dc7b-330">Lehel **Füüsilised mõõtmed** peaksite ruudustikus nägema järgmist rida:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="6dc7b-331">**Ühik:** *tk*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="6dc7b-332">**Brutokaal:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="6dc7b-333">**Laius:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="6dc7b-334">**Sügavus:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="6dc7b-335">**Kõrgus:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="6dc7b-336">**Maht:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="6dc7b-337">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-337">Close the page.</span></span>
1. <span data-ttu-id="6dc7b-338">Valige toode, kus **kaubakoodi** väli on seadistatud valikule *A0002*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="6dc7b-339">Valige toimingupaani vahekaardi **Varude haldamine** grupis **Ladu** suvand **Füüsilised dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="6dc7b-340">Lehel **Füüsilised mõõtmed** peaksite ruudustikus nägema järgmist rida:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="6dc7b-341">**Ühik:** *tk*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="6dc7b-342">**Brutokaal:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="6dc7b-343">**Laius:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="6dc7b-344">**Sügavus:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="6dc7b-345">**Kõrgus:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="6dc7b-346">**Maht:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="6dc7b-347">Müügitellimuse 1 loomine</span><span class="sxs-lookup"><span data-stu-id="6dc7b-347">Create sales order 1</span></span>

<span data-ttu-id="6dc7b-348">Müügitellimuse loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-349">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6dc7b-350">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6dc7b-351">Kuvatakse dialoogiboks uue müügitellimuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="6dc7b-352">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-352">Set the following values:</span></span>

    - <span data-ttu-id="6dc7b-353">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="6dc7b-354">**Ladu:** *63*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="6dc7b-355">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="6dc7b-356">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-356">The new sales order is opened.</span></span> <span data-ttu-id="6dc7b-357">Lisage kiirkaardil **Müügitellimuse read** järgmised müügiread:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="6dc7b-358">Rida 1:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-358">Line 1:</span></span>

        - <span data-ttu-id="6dc7b-359">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="6dc7b-360">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="6dc7b-361">Rida 2:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-361">Line 2:</span></span>

        - <span data-ttu-id="6dc7b-362">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="6dc7b-363">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="6dc7b-364">Valige esimene rida ja seejärel valige **Laovarud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="6dc7b-365">Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="6dc7b-366">Seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-366">Then close the page.</span></span>
1. <span data-ttu-id="6dc7b-367">Korrake teise rea kahte eelmist sammu.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="6dc7b-368">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="6dc7b-369">Müügitellimuse 2 loomine</span><span class="sxs-lookup"><span data-stu-id="6dc7b-369">Create sales order 2</span></span>

<span data-ttu-id="6dc7b-370">Teise müügitellimuse loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-371">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6dc7b-372">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6dc7b-373">Kuvatakse dialoogiboks uue müügitellimuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="6dc7b-374">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-374">Set the following values:</span></span>

    - <span data-ttu-id="6dc7b-375">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="6dc7b-376">**Ladu:** *63*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="6dc7b-377">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="6dc7b-378">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-378">The new sales order is opened.</span></span> <span data-ttu-id="6dc7b-379">Lisage kiirkaardil **Müügitellimuse read** järgmised müügiread:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="6dc7b-380">Rida 1:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-380">Line 1:</span></span>

        - <span data-ttu-id="6dc7b-381">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="6dc7b-382">**Kogus:** *4*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="6dc7b-383">Rida 2:</span><span class="sxs-lookup"><span data-stu-id="6dc7b-383">Line 2:</span></span>

        - <span data-ttu-id="6dc7b-384">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="6dc7b-385">**Kogus:** *4*</span><span class="sxs-lookup"><span data-stu-id="6dc7b-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="6dc7b-386">Valige esimene rida ja seejärel valige **Laovarud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="6dc7b-387">Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="6dc7b-388">Seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-388">Then close the page.</span></span>
1. <span data-ttu-id="6dc7b-389">Korrake teise rea kahte eelmist sammu.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="6dc7b-390">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="6dc7b-391">Koormuse loomine</span><span class="sxs-lookup"><span data-stu-id="6dc7b-391">Create the load</span></span>

<span data-ttu-id="6dc7b-392">Selle stsenaariumi jaoks loodud tellimuste jaoks koormuse loomiseks ja seejärel lattu väljaandmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="6dc7b-393">Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="6dc7b-394">Otsige üles ja valige vahekaardil **Müügiread** kõik müügitellimuse read selle stsenaariumi jaoks loodud müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="6dc7b-395">Valige toimingupaani vahekaardi **Pakkumine ja nõudlus** grupis **Lisa** suvand **Uuele koormusele**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="6dc7b-396">Valitud tellimuseread lisatakse uude koormusse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="6dc7b-397">Valige dialoogiboksi **Koormuse malli määramine** väljal **Koormuse malli ID** koormuse mall, näiteks *40' koormus*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="6dc7b-398">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="6dc7b-399">Otsige üles ja valige äsja loodud koormus jaotises **Koormused**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="6dc7b-400">Valige **Väljastamine \> Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="6dc7b-401">Dialoogiaknas **Lattu väljastamine** valige valitud koormuse lattu väljastamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="6dc7b-402">Kontrolli saadetisi ja konteinereid</span><span class="sxs-lookup"><span data-stu-id="6dc7b-402">Verify the shipments and containers</span></span>

<span data-ttu-id="6dc7b-403">Järgmine protseduur võimaldab teil kontrollida loodud saadetisi.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="6dc7b-404">Selle abil saate selle stsenaariumi jaoks loodud tellimuse üle vaadata ja veenduda, et olete oodatud tulemused saavutanud.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="6dc7b-405">Avage **Laohaldus \> Saadetised \> Kõik saadetised**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="6dc7b-406">Otsige ja valige saadetis, mis loodi äsja väljaantud koorma jaoks.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="6dc7b-407">Avage toimingupaanilt vahekaart **Transport** ja valige **Kuva konteinerid**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="6dc7b-408">Veenduge, et müügitellimuste kaubad määratakse kahte erinevasse konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dc7b-409">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6dc7b-409">Additional resources</span></span>

- [<span data-ttu-id="6dc7b-410">Konteinerisse määramine</span><span class="sxs-lookup"><span data-stu-id="6dc7b-410">Containerization</span></span>](wave-containerization.md)
