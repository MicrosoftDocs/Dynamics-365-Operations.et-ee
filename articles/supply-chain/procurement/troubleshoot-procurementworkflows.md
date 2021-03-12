---
title: Hangete töövoogude tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada hangete töövoogudega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e8274890c581fffc7330538430c9b2ba060041bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999099"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="0bba3-103">Hangete töövoogude tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="0bba3-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="0bba3-104">Selles teemas kirjeldatakse, kuidas lahendada hangete töövoogudega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="0bba3-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="0bba3-105">Pärast ostutellimuse taasedastamist töövoosse pärast muudatust ilmneb tõrge: „Ostutellimust X saab muuta ainult olekus „Mustand”, kui muudatuste haldus on aktiveeritud”</span><span class="sxs-lookup"><span data-stu-id="0bba3-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="0bba3-106">See probleem ilmneb ainult siis, kui ostutellimuse olek oli enne muudatuste taotlemist *Kinnitatud*.</span><span class="sxs-lookup"><span data-stu-id="0bba3-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="0bba3-107">Kui taotlete muudatusi, kui ostutellimuse olek on *Heaks kiidetud*, saab töövoogu edukalt töödelda.</span><span class="sxs-lookup"><span data-stu-id="0bba3-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="0bba3-108">Tõrke kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0bba3-108">Error description</span></span>

<span data-ttu-id="0bba3-109">Järgmine tõrge ilmneb töövoos, kui ostutellimus taasedastatakse pärast muutmist.</span><span class="sxs-lookup"><span data-stu-id="0bba3-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="0bba3-110">Peatatud (tõrge): X++ erand: ostutellimust PO0000569 saab muuta ainult olekus „Mustand”, kui muudatuste haldus on aktiveeritud siin:</span><span class="sxs-lookup"><span data-stu-id="0bba3-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="0bba3-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="0bba3-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="0bba3-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="0bba3-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="0bba3-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="0bba3-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="0bba3-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="0bba3-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0bba3-115">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="0bba3-115">Issue resolution</span></span>

<span data-ttu-id="0bba3-116">See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.</span><span class="sxs-lookup"><span data-stu-id="0bba3-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="0bba3-117">Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="0bba3-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="0bba3-118">Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="0bba3-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="0bba3-119">Probleemi saab lahendada [selle Microsofti teabebaasi (KB) artikli kaudu](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="0bba3-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="0bba3-120">Üks või mitu arvestuse jaotust on kas üle- või alajaotatud.</span><span class="sxs-lookup"><span data-stu-id="0bba3-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="0bba3-121">See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.</span><span class="sxs-lookup"><span data-stu-id="0bba3-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="0bba3-122">Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="0bba3-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="0bba3-123">Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="0bba3-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="0bba3-124">Kui tarnejääk tühistatakse ostutellimusel, mille puhul on muudatuste haldus sisse lülitatud, määratakse ostutellimuse olekuks „Kinnitatud”.</span><span class="sxs-lookup"><span data-stu-id="0bba3-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0bba3-125">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0bba3-125">Issue description</span></span>

<span data-ttu-id="0bba3-126">Muudatuste haldust kasutava ostutellimuse puhul määratakse selle olekuks otse *Kinnitatud* ja töölehte ei looda, kui ainus taotletud muudatus on tarnejäägi tühistamine ühel või mitmel real.</span><span class="sxs-lookup"><span data-stu-id="0bba3-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0bba3-127">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="0bba3-127">Issue resolution</span></span>

<span data-ttu-id="0bba3-128">Tarnejäägi tühistamine ei mõjuta kinnitustöölehe sisu.</span><span class="sxs-lookup"><span data-stu-id="0bba3-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="0bba3-129">Seda funktsiooni tuleks kasutada siis, kui rida on osaliselt vastu võetud ja järelejäänud kogus tuleks tühistada protsessi etapis, mis toimub pärast seda, kui hankija on ostutellimuse kinnitanud.</span><span class="sxs-lookup"><span data-stu-id="0bba3-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="0bba3-130">Kui see peaks kajastuma ostutellimuse kinnitusel, tuleb kogust ostutellimuse real korrigeerida, nii et kinnitus oleks vajalik.</span><span class="sxs-lookup"><span data-stu-id="0bba3-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="0bba3-131">Kui rea puhul pole midagi vastu võetud, on võimalik teise võimalusena kogus eemaldada.</span><span class="sxs-lookup"><span data-stu-id="0bba3-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="0bba3-132">Sellisel juhul on vajalik taaskinnitus.</span><span class="sxs-lookup"><span data-stu-id="0bba3-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="0bba3-133">Tühistatud ostutellimused kuvatakse ostutellimuse ettevalmistamise tööruumis mustandiloendis.</span><span class="sxs-lookup"><span data-stu-id="0bba3-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0bba3-134">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0bba3-134">Issue description</span></span>

<span data-ttu-id="0bba3-135">Pärast olekus *Kinnitatud* ostutellimuste tühistamist kuvatakse tühistatud ostutellimused ikka tööruumis **Ostutellimuse ettevalmistamine** asuvas ostutellimuste mustandite loendis.</span><span class="sxs-lookup"><span data-stu-id="0bba3-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0bba3-136">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="0bba3-136">Issue resolution</span></span>

<span data-ttu-id="0bba3-137">See probleem ilmneb ainult ostutellimuste puhul, mille korral kasutatakse muudatuste haldust.</span><span class="sxs-lookup"><span data-stu-id="0bba3-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="0bba3-138">See ilmneb seetõttu, et tühistamist peetakse muudatuseks, mis tuleb kinnitada.</span><span class="sxs-lookup"><span data-stu-id="0bba3-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="0bba3-139">Süsteem saab selle kinnitada automaatselt.</span><span class="sxs-lookup"><span data-stu-id="0bba3-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="0bba3-140">Seetõttu tuleb tühistatud ostutellimus edastada kinnitamise töövoogu, et selle olekuks saaks määrata *Heaks kiidetud*.</span><span class="sxs-lookup"><span data-stu-id="0bba3-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="0bba3-141">Seejärel ei kuvata ostutellimust enam tööruumis **Ostutellimuse ettevalmistamine** asuvas ostutellimuste mustandite loendis.</span><span class="sxs-lookup"><span data-stu-id="0bba3-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

