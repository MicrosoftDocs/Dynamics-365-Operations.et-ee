---
title: Töövoos olevate tööüksuste delegeerimine
description: Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515760"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="71651-103">Tööüksuste delegeerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="71651-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="71651-104">Tööüksuse käsitsi delegeerimine</span><span class="sxs-lookup"><span data-stu-id="71651-104">Manually delegate a work item</span></span>

<span data-ttu-id="71651-105">Üksiku tööüksuse delegeerimiseks valige menüüst **Töövoog** suvand **Delegeeri** ja seejärel sisestage delegeeritav kasutaja ning kommentaar.</span><span class="sxs-lookup"><span data-stu-id="71651-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="71651-106">See määrab tööüksuse ümber nimetatud kasutajale, nii et ta saaks selle lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="71651-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="71651-107">Mitme tööüksuse käsitsi delegeerimine</span><span class="sxs-lookup"><span data-stu-id="71651-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="71651-108">Mitut tööüksust saab korraga delegeerida lehelt **Minule määratud tööüksused**.</span><span class="sxs-lookup"><span data-stu-id="71651-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="71651-109">Järgmised töövoo tüübid sobivad hulgidelegeerimiseks: ostulepingu kinnitamise töövoog, ostutellimuse töövoog, ostutaotluse ülevaatus ja hankija arve töövoog.</span><span class="sxs-lookup"><span data-stu-id="71651-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="71651-110">Funktsioon **Mitme tööüksuse delegeerimine** on vaikimisi keelatud ja seda saab lubada jaotises **Tööruumid > Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="71651-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="71651-111">Selle funktsiooni lubamiseks abi saamiseks võtke ühendust oma süsteemiadministraatoriga.</span><span class="sxs-lookup"><span data-stu-id="71651-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="71651-112">Avage jaotis **Üldine > Üldine > Tööüksused > Mulle määratud tööüksused**.</span><span class="sxs-lookup"><span data-stu-id="71651-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="71651-113">Valige delegeeritavad tööüksused.</span><span class="sxs-lookup"><span data-stu-id="71651-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="71651-114">Klõpsake menüül **Tööüksuste delegeerimine**.</span><span class="sxs-lookup"><span data-stu-id="71651-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="71651-115">Väljal **Kasutaja** valige kasutaja, keda soovite määrata tööüksuseid delegeerima.</span><span class="sxs-lookup"><span data-stu-id="71651-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="71651-116">Väljale **Kommentaar** sisestage kommentaar, mis selgitab, miks te tööüksusi delegeerite.</span><span class="sxs-lookup"><span data-stu-id="71651-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="71651-117">Tööüksuse delegeerimise lõpule viimiseks klõpsake nuppu **Tööüksuste delegeerimine**.</span><span class="sxs-lookup"><span data-stu-id="71651-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="71651-118">Tööüksuste automaatne delegeerimine</span><span class="sxs-lookup"><span data-stu-id="71651-118">Automatically delegate work items</span></span>

<span data-ttu-id="71651-119">Kui plaanite minna kontorist välja või olla muul moel kättesaamatu teatud ajaperioodil tööüksustega töötamiseks, saate uued tööüksused automaatselt teistele kasutajatele delegeerida, kasutades lehte **Kasutaja suvandid**.</span><span class="sxs-lookup"><span data-stu-id="71651-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="71651-120">Automaatse delegeerimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="71651-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="71651-121">Avage **Üldine > Seadistus > Kasutaja suvandid**.</span><span class="sxs-lookup"><span data-stu-id="71651-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="71651-122">Klõpsake vahekaarti **Töövoog**. Veenduge, et jaotis Delegeerimine on laiendatud.</span><span class="sxs-lookup"><span data-stu-id="71651-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="71651-123">Konfigureerimaks süsteemi automaatselt tööüksuseid teistele kasutajatele delegeerima, peate looma delegeerimisreeglid, mis määravad, millal teatud tüüpi tööüksuseid delegeeritakse.</span><span class="sxs-lookup"><span data-stu-id="71651-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="71651-124">Järgige delegeerimisreegli loomiseks neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="71651-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="71651-125">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="71651-125">Click **Add**.</span></span>
4. <span data-ttu-id="71651-126">Väljal **Ulatus** valige sobiv variant.</span><span class="sxs-lookup"><span data-stu-id="71651-126">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="71651-127">Kõik – saate delegeerida kõik teile määratud tööüksused.</span><span class="sxs-lookup"><span data-stu-id="71651-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="71651-128">Moodul – saate delegeerida ainult tööüksused, mis on seotud konkreetse töövoo tüübiga.</span><span class="sxs-lookup"><span data-stu-id="71651-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="71651-129">Kui valite selle suvandi, peate valima väljal Nimi töövoo tüübi.</span><span class="sxs-lookup"><span data-stu-id="71651-129">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="71651-130">Töövoo – saate delegeerida ainult konkreetse töövooga seotud tööüksused.</span><span class="sxs-lookup"><span data-stu-id="71651-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="71651-131">Kui valite selle suvandi, peate valima töövoo väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="71651-131">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="71651-132">Väljal **Delegaat** valige kasutaja, keda soovite määrata tööüksuseid delegeerima.</span><span class="sxs-lookup"><span data-stu-id="71651-132">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="71651-133">Kasutage välju Alguskuupäev ja -kellaaeg ja Lõppkuupäev ja -kellaaeg, et määrata, millal soovite tööüksuste automaatselt delegeerimist.</span><span class="sxs-lookup"><span data-stu-id="71651-133">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="71651-134">Väljale **Alguskuupäev/kellaaeg** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="71651-134">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="71651-135">Väljale **Lõppkuupäev/kellaaeg** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="71651-135">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="71651-136">Valige märkeruut **Lubatud**, et aktiveerida delegeerimise reegel.</span><span class="sxs-lookup"><span data-stu-id="71651-136">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="71651-137">Kui valisite ulatuseks **Moodul**, peate seejärel valima mooduli väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="71651-137">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="71651-138">Kui valisite ulatuseks **Töövoog**, peate seejärel valima konkreetse töövoo, mida delegeerida väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="71651-138">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="71651-139">Väljale **Kommentaar** sisestage kommentaar, mis selgitab, miks te tööüksusi delegeerite.</span><span class="sxs-lookup"><span data-stu-id="71651-139">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>

