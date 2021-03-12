---
title: Töövoos olevate tööüksuste delegeerimine
description: Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48d8fd06217d318fa8208e11ffa5624f6be25be1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796702"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="4a4fa-103">Tööüksuste delegeerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="4a4fa-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="4a4fa-104">Tööüksuse käsitsi delegeerimine</span><span class="sxs-lookup"><span data-stu-id="4a4fa-104">Manually delegate a work item</span></span>

<span data-ttu-id="4a4fa-105">Üksiku tööüksuse delegeerimiseks valige menüüst **Töövoog** suvand **Delegeeri** ja seejärel sisestage delegeeritav kasutaja ning kommentaar.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="4a4fa-106">See määrab tööüksuse ümber nimetatud kasutajale, nii et ta saaks selle lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="4a4fa-107">Mitme tööüksuse käsitsi delegeerimine</span><span class="sxs-lookup"><span data-stu-id="4a4fa-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="4a4fa-108">Mitut tööüksust saab korraga delegeerida lehelt **Minule määratud tööüksused**.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="4a4fa-109">Järgmised töövoo tüübid sobivad hulgidelegeerimiseks: ostulepingu kinnitamise töövoog, ostutellimuse töövoog, ostutaotluse ülevaatus ja hankija arve töövoog.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="4a4fa-110">Funktsioon **Mitme tööüksuse delegeerimine** on vaikimisi keelatud ja seda saab lubada jaotises **Tööruumid > Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="4a4fa-111">Selle funktsiooni lubamiseks abi saamiseks võtke ühendust oma süsteemiadministraatoriga.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="4a4fa-112">Avage jaotis **Üldine > Üldine > Tööüksused > Mulle määratud tööüksused**.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="4a4fa-113">Valige delegeeritavad tööüksused.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="4a4fa-114">Klõpsake menüül **Tööüksuste delegeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="4a4fa-115">Väljal **Kasutaja** valige kasutaja, keda soovite määrata tööüksuseid delegeerima.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="4a4fa-116">Väljale **Kommentaar** sisestage kommentaar, mis selgitab, miks te tööüksusi delegeerite.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="4a4fa-117">Tööüksuse delegeerimise lõpule viimiseks klõpsake nuppu **Tööüksuste delegeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="4a4fa-118">Tööüksuste automaatne delegeerimine</span><span class="sxs-lookup"><span data-stu-id="4a4fa-118">Automatically delegate work items</span></span>

<span data-ttu-id="4a4fa-119">Kui plaanite minna kontorist välja või olla muul moel kättesaamatu teatud ajaperioodil tööüksustega töötamiseks, saate uued tööüksused automaatselt teistele kasutajatele delegeerida, kasutades lehte **Kasutaja suvandid**.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="4a4fa-120">Automaatse delegeerimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="4a4fa-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="4a4fa-121">Avage **Üldine > Seadistus > Kasutaja suvandid**.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="4a4fa-122">Klõpsake vahekaarti **Töövoog**. Veenduge, et jaotis Delegeerimine on laiendatud.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="4a4fa-123">Konfigureerimaks süsteemi automaatselt tööüksuseid teistele kasutajatele delegeerima, peate looma delegeerimisreeglid, mis määravad, millal teatud tüüpi tööüksuseid delegeeritakse.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="4a4fa-124">Järgige delegeerimisreegli loomiseks neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="4a4fa-125">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-125">Click **Add**.</span></span>
4. <span data-ttu-id="4a4fa-126">Valige väljal **Ulatus** sobiv variant.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="4a4fa-127">Kõik – saate delegeerida kõik teile määratud tööüksused.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="4a4fa-128">Moodul – saate delegeerida ainult tööüksused, mis on seotud konkreetse töövoo tüübiga.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="4a4fa-129">Kui valite selle suvandi, peate valima väljal **Nimi** töövoo tüübi.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="4a4fa-130">Töövoo – saate delegeerida ainult konkreetse töövooga seotud tööüksused.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="4a4fa-131">Kui valite selle suvandi, peate valima väljal **Nimi** töövoo.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="4a4fa-132">Väljal **Nimi** tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-132">In the **Name** field:</span></span>
    - <span data-ttu-id="4a4fa-133">Valige ulatuse **Moodul** jaoks sihtmoodul.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="4a4fa-134">Valige ulatuse **Töövoog** jaoks sihttöövoog.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="4a4fa-135">Väljal **Delegaat** valige kasutaja, keda soovite määrata tööüksuseid delegeerima.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="4a4fa-136">Kasutage välju **Alguskuupäev ja -kellaaeg** ja **Lõppkuupäev ja -kellaaeg**, et määrata, millal soovite tööüksuste automaatset delegeerimist.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="4a4fa-137">Väljale **Alguskuupäev/kellaaeg** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="4a4fa-138">Väljale **Lõppkuupäev/kellaaeg** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="4a4fa-139">Valige märkeruut **Lubatud**, et aktiveerida delegeerimise reegel.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="4a4fa-140">Väljale **Kommentaar** sisestage kommentaar, mis selgitab, miks te tööüksusi delegeerite.</span><span class="sxs-lookup"><span data-stu-id="4a4fa-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
