---
title: Kasutajate määramine turberollidesse
description: Finance and Operationsi rakendustele juurde pääsemiseks tuleb määrata kasutajatele turberoll.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2807992"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="155fc-103">Kasutajate määramine turberollidesse</span><span class="sxs-lookup"><span data-stu-id="155fc-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="155fc-104">Tavalistest võimalustest enama kasutamiseks tuleb määrata kasutajatele turberoll.</span><span class="sxs-lookup"><span data-stu-id="155fc-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="155fc-105">See protseduur selgitab, kuidas süsteemiadministraatorid saavad automaatselt määrata kasutajatele rolle äriandmete alusel.</span><span class="sxs-lookup"><span data-stu-id="155fc-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="155fc-106">Kasutajate automaatsel rollidesse määramine</span><span class="sxs-lookup"><span data-stu-id="155fc-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="155fc-107">Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.</span><span class="sxs-lookup"><span data-stu-id="155fc-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="155fc-108">Tehke puustruktuuris valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="155fc-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="155fc-109">Valige roll, millele soovite reegli konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="155fc-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="155fc-110">Selles näites tehle valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="155fc-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="155fc-111">Klõpsake suvandit **Lisa reegel** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="155fc-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="155fc-112">Otsige **Vali päring** loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="155fc-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="155fc-113">Valige päring, mida selle reegli puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="155fc-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="155fc-114">Klõpsake loendis **Liikmesuse reegli nimi** valitud rea linki.</span><span class="sxs-lookup"><span data-stu-id="155fc-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="155fc-115">Klõpsake **Redigeeri päringut**.</span><span class="sxs-lookup"><span data-stu-id="155fc-115">Click **Edit query**.</span></span> <span data-ttu-id="155fc-116">Redigeerige vajaduse korral päringut.</span><span class="sxs-lookup"><span data-stu-id="155fc-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="155fc-117">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="155fc-117">Click **OK**.</span></span>
8. <span data-ttu-id="155fc-118">Klõpsake valikut **Käivita automaatne rollide määramine**.</span><span class="sxs-lookup"><span data-stu-id="155fc-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="155fc-119">Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Kasutajad > Kasutajad** (ideaalis eraldi brauseri vahekaardil).</span><span class="sxs-lookup"><span data-stu-id="155fc-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="155fc-120">Vaadake üle erinevatele kasutajatele määratud rollid ja veenduge, et rollide määramise päring oleks õige.</span><span class="sxs-lookup"><span data-stu-id="155fc-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="155fc-121">Kohandage ja käivitage vajaduse korral uuesti.</span><span class="sxs-lookup"><span data-stu-id="155fc-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="155fc-122">Kasutajate välistamine automaatsest rollimäärangust</span><span class="sxs-lookup"><span data-stu-id="155fc-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="155fc-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="155fc-123">Close the page.</span></span>
2. <span data-ttu-id="155fc-124">Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.</span><span class="sxs-lookup"><span data-stu-id="155fc-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="155fc-125">Tehke puustruktuuris valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="155fc-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="155fc-126">Valige roll.</span><span class="sxs-lookup"><span data-stu-id="155fc-126">Select a role.</span></span> <span data-ttu-id="155fc-127">Selles näites tehke valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="155fc-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="155fc-128">Valige menüüs **Rollile määratud kasutajad** suvand **Määra käsitsi / välista kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="155fc-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="155fc-129">Märkige loendis **Määra kasutajad rollidesse või välista rollidest** valitud rida.</span><span class="sxs-lookup"><span data-stu-id="155fc-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="155fc-130">Valige kasutaja.</span><span class="sxs-lookup"><span data-stu-id="155fc-130">Select a user.</span></span>  
6. <span data-ttu-id="155fc-131">Valige paanil **Toimingupaan** suvand **Välista rollist**.</span><span class="sxs-lookup"><span data-stu-id="155fc-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="155fc-132">Klõpsake suvandit **Välista rollist** valitud kasutajate rollist välistamiseks.</span><span class="sxs-lookup"><span data-stu-id="155fc-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="155fc-133">Erandite eemaldamiseks valige kasutajad, kelle puhul soovite erandid eemaldada, ja klõpsake seejärel käsku **Lähtesta olek**.</span><span class="sxs-lookup"><span data-stu-id="155fc-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="155fc-134">Kui eemaldate välistamise, lähtestades kasutaja olek, määratakse kasutaja roll uuesti automaatselt.</span><span class="sxs-lookup"><span data-stu-id="155fc-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="155fc-135">Kuid kasutajale ei määrata kohe rolli ega välistate rolli, kui oleku lähtestate.</span><span class="sxs-lookup"><span data-stu-id="155fc-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="155fc-136">Selle asemel määratakse kasutajale roll või temalt eemaldatakse roll järgmisel korral, kui käitatakse automaatse rollimäärangu reeglit.</span><span class="sxs-lookup"><span data-stu-id="155fc-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
