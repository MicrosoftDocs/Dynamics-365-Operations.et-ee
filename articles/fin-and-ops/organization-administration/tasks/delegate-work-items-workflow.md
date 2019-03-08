---
title: Töövoos olevate tööüksuste delegeerimine
description: Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "346245"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="7fade-103">Töövoos olevate tööüksuste delegeerimine</span><span class="sxs-lookup"><span data-stu-id="7fade-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fade-104">Kui plaanite olla kontorist väljas või muul viisil tööüksustega tegelemiseks kättesaamatu, saate tööüksused teistele kasutajatele delegeerida või ümber määrata.</span><span class="sxs-lookup"><span data-stu-id="7fade-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="7fade-105">See protseduur aitab teil konfigureerida süsteemi automaatselt delegeerima teie tööüksused teisele kasutajale.</span><span class="sxs-lookup"><span data-stu-id="7fade-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="7fade-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="7fade-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="7fade-107">Automaatse delegeerimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="7fade-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="7fade-108">Avage Üldine > Häälestamine > Kasutaja suvandid.</span><span class="sxs-lookup"><span data-stu-id="7fade-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="7fade-109">Klõpsake vahekaarti Töövoog.</span><span class="sxs-lookup"><span data-stu-id="7fade-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="7fade-110">Veenduge, et jaotis Delegatsioon on laiendatud.</span><span class="sxs-lookup"><span data-stu-id="7fade-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="7fade-111">Konfigureerimaks süsteemi automaatselt tööüksuseid teistele kasutajatele delegeerima, peate looma delegeerimisreeglid, mis määravad, millal teatud tüüpi tööüksuseid delegeeritakse.</span><span class="sxs-lookup"><span data-stu-id="7fade-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="7fade-112">Järgige delegeerimisreegli loomiseks neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="7fade-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="7fade-113">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="7fade-113">Click Add.</span></span>
4. <span data-ttu-id="7fade-114">Väljal Ulatus valige suvand.</span><span class="sxs-lookup"><span data-stu-id="7fade-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="7fade-115">Kõik – saate delegeerida kõik teile määratud tööüksused.</span><span class="sxs-lookup"><span data-stu-id="7fade-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="7fade-116">Moodul – saate delegeerida ainult tööüksused, mis on seotud konkreetse töövoo tüübiga.</span><span class="sxs-lookup"><span data-stu-id="7fade-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="7fade-117">Kui valite selle suvandi, peate valima väljal Nimi töövoo tüübi.</span><span class="sxs-lookup"><span data-stu-id="7fade-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="7fade-118">Töövoo – saate delegeerida ainult konkreetse töövooga seotud tööüksused.</span><span class="sxs-lookup"><span data-stu-id="7fade-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="7fade-119">Kui valite selle suvandi, peate valima töövoo väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="7fade-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="7fade-120">Väljal Delegeeri valige kasutaja, kellele tööüksuseid delegeerida.</span><span class="sxs-lookup"><span data-stu-id="7fade-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="7fade-121">Kasutage välju Alguskuupäev ja -kellaaeg ja Lõppkuupäev ja -kellaaeg, et määrata, millal soovite tööüksuste automaatselt delegeerimist.</span><span class="sxs-lookup"><span data-stu-id="7fade-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="7fade-122">Väljale Alguskuupäev ja -kellaaeg sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="7fade-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="7fade-123">Väljale Lõppkuupäev ja -kellaaeg sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="7fade-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="7fade-124">Märkige delegeerimisreegli aktiveerimiseks ruut Lubatud.</span><span class="sxs-lookup"><span data-stu-id="7fade-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="7fade-125">Kui valisite suvandi Ulatus sätteks Moodul, siis peate väljal Nimi valima mooduli.</span><span class="sxs-lookup"><span data-stu-id="7fade-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="7fade-126">Kui valisite suvandi Ulatus sätteks Töövoog, siis peate väljal Nimi valima konkreetse delegeeritava töövoo.</span><span class="sxs-lookup"><span data-stu-id="7fade-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="7fade-127">Väljale Kommentaar sisestage kommentaar, mis selgitab tööüksuste delegeerimise põhjust.</span><span class="sxs-lookup"><span data-stu-id="7fade-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

