---
title: Plaanitud tellimuste kuvamine, haldamine ja kinnitamine
description: Käesolevas teemas kirjeldatakse, kuidas planeerimise optimeerimise korral kuvada, hallata ja kinnitada plaanitud tellimusi.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935653"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="7185c-103">Plaanitud tellimuste kuvamine, haldamine ja kinnitamine</span><span class="sxs-lookup"><span data-stu-id="7185c-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7185c-104">Käesolevas teemas kirjeldatakse, kuidas planeerimise optimeerimise korral kuvada, hallata ja kinnitada plaanitud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="7185c-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="7185c-105">Plaanitud tellimuste kuvamine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="7185c-105">View and manage planned orders</span></span>

<span data-ttu-id="7185c-106">Plaanitud tellimusi saate vaadata ja hallata mis tahes plaanitud tellimuste loendilehel.</span><span class="sxs-lookup"><span data-stu-id="7185c-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="7185c-107">Sõltuvalt plaanitud tellimuste tüübist, mida soovite kasutada, saate minna ühte järgmistest kohtadest.</span><span class="sxs-lookup"><span data-stu-id="7185c-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="7185c-108">Koondplaneerimise \> tööruumide \> koondplaneerimine</span><span class="sxs-lookup"><span data-stu-id="7185c-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="7185c-109">Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused</span><span class="sxs-lookup"><span data-stu-id="7185c-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="7185c-110">Tootmise juhtimine \> Tootmistellimused \> Plaanitud tootmistellimused</span><span class="sxs-lookup"><span data-stu-id="7185c-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="7185c-111">Hanked \> Ostutellimused \> Plaanitud ostutellimused</span><span class="sxs-lookup"><span data-stu-id="7185c-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="7185c-112">Varude haldamine \> Sissetulevad tellimused \> Plaanitud üleviimised</span><span class="sxs-lookup"><span data-stu-id="7185c-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="7185c-113">Varude haldamine \> Väljaminevad tellimused \> Plaanitud üleviimised</span><span class="sxs-lookup"><span data-stu-id="7185c-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="7185c-114">Plaanitud tellimuste vaatamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="7185c-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="7185c-115">Edenemise jälgimiseks või plaanitud tellimuse töötlemise muutmiseks saate kasutada iga plaanitud tellimuse **olekuvälja**.</span><span class="sxs-lookup"><span data-stu-id="7185c-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="7185c-116">Saadaval on järgmised suvandi **Olek** väärtused.</span><span class="sxs-lookup"><span data-stu-id="7185c-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="7185c-117">**Töötlemata** – kui koondplaneerimine loob plaanitud tellimused, antakse neile see olek.</span><span class="sxs-lookup"><span data-stu-id="7185c-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="7185c-118">Selle olekuga plaanitud tellimused kustutatakse järgmise plaanimise käitamisel.</span><span class="sxs-lookup"><span data-stu-id="7185c-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="7185c-119">**Lõpetatud** – see olek näitab, et plaanitud tellimus on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="7185c-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="7185c-120">Kui otsustate plaanitud tellimust mitte kinnitada, saate sellele manuaalselt määrata oleku *Lõpule viidud*.</span><span class="sxs-lookup"><span data-stu-id="7185c-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="7185c-121">Pange tähele, et süsteem käsitleb olekuid *Töötlemata* ja *Lõpetatud* sama moodi.</span><span class="sxs-lookup"><span data-stu-id="7185c-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="7185c-122">**Kinnitatud** – see olek näitab, et plaanitud tellimus on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="7185c-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="7185c-123">Kui soovite kinnitada plaanitud tellimuse, saate määrata selle olekuks *Kinnitatud*.</span><span class="sxs-lookup"><span data-stu-id="7185c-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="7185c-124">Kui soovite säilitada plaanitud tellimusele tehtud muudatusi või kui plaanite plaanitud tellimust kinnitab, muutke selle olekuks *Kinnitatud*.</span><span class="sxs-lookup"><span data-stu-id="7185c-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="7185c-125">Plaanitud tellimused, mille olek on *Kinnitatud*, loetakse koondplaneerimises fikseerituks ja eeldatavaks tarneks.</span><span class="sxs-lookup"><span data-stu-id="7185c-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="7185c-126">Seetõttu ei muudeta ega kustutata neid hiljem koondplaneerimise käitamisel.</span><span class="sxs-lookup"><span data-stu-id="7185c-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="7185c-127">Selle toimimisviisi saavutamiseks kopeerib planeerimisloogika koondplaneerimise ajal *kinnitatud* olekus plaanitud tellimused vana plaani versioonist uude plaani versiooni.</span><span class="sxs-lookup"><span data-stu-id="7185c-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="7185c-128">Pange tähele, et *Kinnitatud* olekus plaanitud tellimusi loetakse tarnitavateks ainult konkreetse koondplaani korral.</span><span class="sxs-lookup"><span data-stu-id="7185c-128">Note that planned orders that have a status of *Approved*\* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="7185c-129">Üksiku plaanitud tellimuse oleku muutmiseks [avage mis tahes plaanitud tellimuste loendileht](#view-planned-orders), avage tellimus ja tehke seejärel üht järgmistest sammudest.</span><span class="sxs-lookup"><span data-stu-id="7185c-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="7185c-130">Kiirkaardil **Üldine** muutke välja **Olek** väärtust.</span><span class="sxs-lookup"><span data-stu-id="7185c-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="7185c-131">Valige toimingupaani vahekaardil **Plaanitud tellimus** grupis **Protsess** suvand **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="7185c-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="7185c-132">Tellimuse kinnitamiseks valige tegumiribal suvand **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="7185c-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="7185c-133">Mitme plaanitud tellimuse oleku ühekorraga muutmiseks [avage mis tahes plaanitud tellimuste loendileht](#view-planned-orders), märkige ruut iga tellimuse puhul, mida soovite muuta, ja seejärel järgige üht järgmistest sammudest.</span><span class="sxs-lookup"><span data-stu-id="7185c-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="7185c-134">Valige toimingupaani vahekaardil **Plaanitud tellimus** grupis **Protsess** suvand **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="7185c-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="7185c-135">Tellimuste kinnitamiseks valige tegumiribal suvand **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="7185c-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="7185c-136">Plaanitud tellimuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="7185c-136">Approve planned orders</span></span>

<span data-ttu-id="7185c-137">Plaanitud tellimuste kinnitamine on valikuline etapp plaanitud tellimuseest kinnitatud tellimuse loomise protsessis.</span><span class="sxs-lookup"><span data-stu-id="7185c-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="7185c-138">Järgmine näide näitab, kuidas saate kasutada suvandi **Olek** väärtust, mis on määratud igale plaanitud tellimusele kinnitustöövoogude juurutamiseks.</span><span class="sxs-lookup"><span data-stu-id="7185c-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="7185c-139">Kinnitusprotsessi juurutamiseks korrigeerige iga plaanitud tellimuse suvandi **Olek** väärtust käsitsi, nagu eelmises jaotises kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="7185c-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Plaanitud tellimuse voog](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="7185c-141">Soovitame teil kõik muudetud plaanitud tellimused kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7185c-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="7185c-142">Vastasel korral eiratakse muudatusi ja need kirjutatakse järgmise planeerimise käivitamisel üle.</span><span class="sxs-lookup"><span data-stu-id="7185c-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7185c-143">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7185c-143">Additional resources</span></span>

- [<span data-ttu-id="7185c-144">Kindlad plaanitud tellimused</span><span class="sxs-lookup"><span data-stu-id="7185c-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
