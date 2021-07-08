---
title: Laovarude korrigeerimine
description: Sellest teemast saate teavet laovarude korrigeerimist töölehe kohta ja töötlemise kohta, kui kasutate skaalaühikuid.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1bf147ce430d84980516d8d4824081ee2a9321a2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271228"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="07be7-103">Laovarude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="07be7-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07be7-104">Lao varude korrigeerimise funktsiooni kasutatakse pilve ja servaskaala üksuste käitamisel [tootmise töökoormuste](cloud-edge-workload-manufacturing.md) ja [laohalduse töökoormuste](cloud-edge-workload-warehousing.md) jaoks.</span><span class="sxs-lookup"><span data-stu-id="07be7-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="07be7-105">Kui töötaja teeb laovarude korrigeerimist lao rakenduse abil laoala üksuse laohalduse töökoormuse suhtes, peab laohalduse **lao varude korrigeerimise töölehe** pakett-töö töötlema füüsilist vaba laovaru uuendamist, mida käitate ja planeerite, kui soovite minna **Laohaldus > Perioodiliste ülesannete > Lao varude korrigeerimise töölehele**.</span><span class="sxs-lookup"><span data-stu-id="07be7-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="07be7-106">Järgmistes lao rakenduste tööprotsessides kasutatakse praegu **laovarude korrigeerimise töölehte** kaaluühiku töökoormustel:</span><span class="sxs-lookup"><span data-stu-id="07be7-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="07be7-107">Korrigeerimine sisse/välja</span><span class="sxs-lookup"><span data-stu-id="07be7-107">Adjustment in/out</span></span>
- <span data-ttu-id="07be7-108">Tsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="07be7-108">Cycle counting</span></span>
- <span data-ttu-id="07be7-109">Litsentsiplaadi laadimine</span><span class="sxs-lookup"><span data-stu-id="07be7-109">License plate loading</span></span>

<span data-ttu-id="07be7-110">Iga varude kohandamise protsessi osana luuakse mitu varude tehingut, kuna jaoturi ja skaalaüksuse juurutused jagavad varude kirjet.</span><span class="sxs-lookup"><span data-stu-id="07be7-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="07be7-111">Varude korrigeerimise näide</span><span class="sxs-lookup"><span data-stu-id="07be7-111">Inventory adjustment example</span></span>

<span data-ttu-id="07be7-112">Selles näites on laotöötaja kasutanud lao rakendust, et registreerida vaba kaubavaru lisamine.</span><span class="sxs-lookup"><span data-stu-id="07be7-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="07be7-113">Kõigepealt loob kaaluühiku töökoormus lao varude korrigeerimiskande positiivse füüsilise korrigeerimise jaoks, mis seejärel sünkroonitakse keskusega ja suurendab keskuse vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="07be7-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="07be7-114">Tüüp</span><span class="sxs-lookup"><span data-stu-id="07be7-114">Type</span></span>                                    | <span data-ttu-id="07be7-115">Skaalaüksus</span><span class="sxs-lookup"><span data-stu-id="07be7-115">Scale unit</span></span> | <span data-ttu-id="07be7-116">Direction</span><span class="sxs-lookup"><span data-stu-id="07be7-116">Direction</span></span> | <span data-ttu-id="07be7-117">Keskus</span><span class="sxs-lookup"><span data-stu-id="07be7-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="07be7-118">Laovarude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="07be7-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="07be7-119">+1</span><span class="sxs-lookup"><span data-stu-id="07be7-119">+1</span></span>         | ->        | <span data-ttu-id="07be7-120">+1</span><span class="sxs-lookup"><span data-stu-id="07be7-120">+1</span></span>  |

<span data-ttu-id="07be7-121">Seejärel töötleb keskus inventuuritöölehe sisestust, mille saab [sõnumiprotsessori teadete](cloud-edge-message-processor-messages.md) kaudu.</span><span class="sxs-lookup"><span data-stu-id="07be7-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="07be7-122">See uuendab edasist vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="07be7-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="07be7-123">Topeltlao vältimiseks loob keskus protsessi osana vastaskande ja eemaldab varem kirjendatud vaba kaubavaru, mis on seotud lao varude korrigeerimisega.</span><span class="sxs-lookup"><span data-stu-id="07be7-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="07be7-124">Tüüp</span><span class="sxs-lookup"><span data-stu-id="07be7-124">Type</span></span>                                    | <span data-ttu-id="07be7-125">Skaalaüksus</span><span class="sxs-lookup"><span data-stu-id="07be7-125">Scale unit</span></span> | <span data-ttu-id="07be7-126">Direction</span><span class="sxs-lookup"><span data-stu-id="07be7-126">Direction</span></span> | <span data-ttu-id="07be7-127">Keskus</span><span class="sxs-lookup"><span data-stu-id="07be7-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="07be7-128">Inventuur</span><span class="sxs-lookup"><span data-stu-id="07be7-128">Counting</span></span>                                | <span data-ttu-id="07be7-129">+1</span><span class="sxs-lookup"><span data-stu-id="07be7-129">+1</span></span>         | <-        | <span data-ttu-id="07be7-130">+1</span><span class="sxs-lookup"><span data-stu-id="07be7-130">+1</span></span>  |
| <span data-ttu-id="07be7-131">Lao varude korrigeerimine (vastaskonto)</span><span class="sxs-lookup"><span data-stu-id="07be7-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="07be7-132">–1</span><span class="sxs-lookup"><span data-stu-id="07be7-132">-1</span></span>         | <-        | <span data-ttu-id="07be7-133">–1</span><span class="sxs-lookup"><span data-stu-id="07be7-133">-1</span></span>  |

<span data-ttu-id="07be7-134">Pärast seda, kui kaaluühik on keskusele loonud **Lao varude korrigeerimise töölehe**, saate üle vaadata nii **inventuuritöölehte** kui ka **vastastöölehte** mille keskus on loonud korrigeerimisprotsessi osana.</span><span class="sxs-lookup"><span data-stu-id="07be7-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="07be7-135">Saate läbi vaadata kõik need töölehe sisestused ja kanded Supply Chain Managementis järgmiste sammude abil:</span><span class="sxs-lookup"><span data-stu-id="07be7-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="07be7-136">Logige sisse kaaluühikusse.</span><span class="sxs-lookup"><span data-stu-id="07be7-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="07be7-137">Avage **Laohaldus \> Perioodilised ülesanded \> Laovarude kohandamise tööleht**.</span><span class="sxs-lookup"><span data-stu-id="07be7-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="07be7-138">**Lao varude korrigeerimise töölehe** lehel otsige ja avage tööleht, mis kirjendas vaba kaubavaru muudatust.</span><span class="sxs-lookup"><span data-stu-id="07be7-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="07be7-139">**Töölehe ridade** jaotises kuvatakse kõik selle töölehe salvestatud korrektsioonid.</span><span class="sxs-lookup"><span data-stu-id="07be7-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="07be7-140">Keskusesse sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="07be7-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="07be7-141">Avage **Laohaldus \> Perioodilised ülesanded \> Laovarude kohandamise tööleht**.</span><span class="sxs-lookup"><span data-stu-id="07be7-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="07be7-142">**Lao varude korrigeerimise töölehe** lehel peaksite nägema sama töölehte, mis on loetletud, kui keskus ja kaaluühik on sünkroonitud.</span><span class="sxs-lookup"><span data-stu-id="07be7-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="07be7-143">Avage tööleht.</span><span class="sxs-lookup"><span data-stu-id="07be7-143">Open the journal.</span></span> <span data-ttu-id="07be7-144">Kui [teateprotsessori teateid](cloud-edge-message-processor-messages.md) on töödeldud, näete linke **inventuuritöölehele** ja päises **vastastöölehele**.</span><span class="sxs-lookup"><span data-stu-id="07be7-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="07be7-145">**Inventuuritööleht** peab kuvama töölehe ridadega samad dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="07be7-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="07be7-146">**Vastaskonto tööleht** peab näitama vastaskontot, mis eemaldab topeltvarude korrigeerimise.</span><span class="sxs-lookup"><span data-stu-id="07be7-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="07be7-147">Kui kogu sünkroonimine ja töötlemine on lõpetatud, sünkroonitakse **inventuuri tööleht** ja **vastastööleht** tagasi kaaluühikusse.</span><span class="sxs-lookup"><span data-stu-id="07be7-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="07be7-148">Neid saab vaadata ka vastaval **laovarude korrigeerimise töölehe** leheküljel.</span><span class="sxs-lookup"><span data-stu-id="07be7-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
