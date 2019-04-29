---
title: Töövoos olevate tööüksuste delegeerimine
description: Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/12/2019
ms.locfileid: "976777"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="9ea37-103">Tööüksuste delegeerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="9ea37-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="9ea37-104">Tööüksuse käsitsi delegeerimine</span><span class="sxs-lookup"><span data-stu-id="9ea37-104">Manually delegate a work item</span></span>

<span data-ttu-id="9ea37-105">Üksiku tööüksuse delegeerimiseks valige menüüst **Töövoog** suvand **Delegeeri** ja seejärel sisestage delegeeritav kasutaja ning kommentaar.</span><span class="sxs-lookup"><span data-stu-id="9ea37-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="9ea37-106">See määrab tööüksuse ümber nimetatud kasutajale, nii et ta saaks selle lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="9ea37-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="9ea37-107">Tööüksuste automaatne delegeerimine</span><span class="sxs-lookup"><span data-stu-id="9ea37-107">Automatically delegate work items</span></span>

<span data-ttu-id="9ea37-108">Kui plaanite minna kontorist välja või olla muul moel kättesaamatu teatud ajaperioodil tööüksustega töötamiseks, saate uued tööüksused automaatselt teistele kasutajatele delegeerida, kasutades lehte **Kasutaja suvandid**.</span><span class="sxs-lookup"><span data-stu-id="9ea37-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="9ea37-109">Automaatse delegeerimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="9ea37-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="9ea37-110">Avage Üldine > Häälestamine > Kasutaja suvandid.</span><span class="sxs-lookup"><span data-stu-id="9ea37-110">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="9ea37-111">Klõpsake vahekaarti Töövoog.</span><span class="sxs-lookup"><span data-stu-id="9ea37-111">Click the Workflow tab.</span></span>
    * <span data-ttu-id="9ea37-112">Veenduge, et jaotis Delegatsioon on laiendatud.</span><span class="sxs-lookup"><span data-stu-id="9ea37-112">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="9ea37-113">Konfigureerimaks süsteemi automaatselt tööüksuseid teistele kasutajatele delegeerima, peate looma delegeerimisreeglid, mis määravad, millal teatud tüüpi tööüksuseid delegeeritakse.</span><span class="sxs-lookup"><span data-stu-id="9ea37-113">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="9ea37-114">Järgige delegeerimisreegli loomiseks neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="9ea37-114">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="9ea37-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9ea37-115">Click Add.</span></span>
4. <span data-ttu-id="9ea37-116">Väljal Ulatus valige suvand.</span><span class="sxs-lookup"><span data-stu-id="9ea37-116">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="9ea37-117">Kõik – saate delegeerida kõik teile määratud tööüksused.</span><span class="sxs-lookup"><span data-stu-id="9ea37-117">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="9ea37-118">Moodul – saate delegeerida ainult tööüksused, mis on seotud konkreetse töövoo tüübiga.</span><span class="sxs-lookup"><span data-stu-id="9ea37-118">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="9ea37-119">Kui valite selle suvandi, peate valima väljal Nimi töövoo tüübi.</span><span class="sxs-lookup"><span data-stu-id="9ea37-119">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="9ea37-120">Töövoo – saate delegeerida ainult konkreetse töövooga seotud tööüksused.</span><span class="sxs-lookup"><span data-stu-id="9ea37-120">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="9ea37-121">Kui valite selle suvandi, peate valima töövoo väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="9ea37-121">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="9ea37-122">Väljal Delegeeri valige kasutaja, kellele tööüksuseid delegeerida.</span><span class="sxs-lookup"><span data-stu-id="9ea37-122">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="9ea37-123">Kasutage välju Alguskuupäev ja -kellaaeg ja Lõppkuupäev ja -kellaaeg, et määrata, millal soovite tööüksuste automaatselt delegeerimist.</span><span class="sxs-lookup"><span data-stu-id="9ea37-123">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="9ea37-124">Väljale Alguskuupäev ja -kellaaeg sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="9ea37-124">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="9ea37-125">Väljale Lõppkuupäev ja -kellaaeg sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="9ea37-125">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="9ea37-126">Märkige delegeerimisreegli aktiveerimiseks ruut Lubatud.</span><span class="sxs-lookup"><span data-stu-id="9ea37-126">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="9ea37-127">Kui valisite suvandi Ulatus sätteks Moodul, siis peate väljal Nimi valima mooduli.</span><span class="sxs-lookup"><span data-stu-id="9ea37-127">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="9ea37-128">Kui valisite suvandi Ulatus sätteks Töövoog, siis peate väljal Nimi valima konkreetse delegeeritava töövoo.</span><span class="sxs-lookup"><span data-stu-id="9ea37-128">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="9ea37-129">Väljale Kommentaar sisestage kommentaar, mis selgitab tööüksuste delegeerimise põhjust.</span><span class="sxs-lookup"><span data-stu-id="9ea37-129">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

