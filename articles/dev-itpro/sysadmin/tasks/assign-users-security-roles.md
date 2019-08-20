---
title: Kasutajate määramine turberollidesse
description: Microsoft Dynamics 365 for Finance and Operations, Enterprise editionile juurdepääsuks peavad kasutajatele olema määratud turberollid.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851355"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="1ae40-103">Kasutajate määramine turberollidesse</span><span class="sxs-lookup"><span data-stu-id="1ae40-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ae40-104">Microsoft Dynamics 365 for Finance and Operations, Enterprise editionile juurdepääsuks peavad kasutajatele olema määratud turberollid.</span><span class="sxs-lookup"><span data-stu-id="1ae40-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="1ae40-105">See protseduur selgitab, kuidas süsteemiadministraatorid saavad määrata kasutajatele automaatselt rolle äriandmete alusel.</span><span class="sxs-lookup"><span data-stu-id="1ae40-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="1ae40-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="1ae40-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="1ae40-107">Kasutajate automaatsel rollidesse määramine</span><span class="sxs-lookup"><span data-stu-id="1ae40-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="1ae40-108">Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.</span><span class="sxs-lookup"><span data-stu-id="1ae40-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="1ae40-109">Tehke puustruktuuris valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="1ae40-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="1ae40-110">Valige roll, millele soovite reegli konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="1ae40-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="1ae40-111">Selles näites tehle valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="1ae40-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="1ae40-112">Klõpsake suvandit **Lisa reegel** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1ae40-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="1ae40-113">Otsige **Vali päring** loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1ae40-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="1ae40-114">Valige päring, mida selle reegli puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="1ae40-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="1ae40-115">Klõpsake loendis **Liikmesuse reegli nimi** valitud rea linki.</span><span class="sxs-lookup"><span data-stu-id="1ae40-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1ae40-116">Klõpsake **Redigeeri päringut**.</span><span class="sxs-lookup"><span data-stu-id="1ae40-116">Click **Edit query**.</span></span> <span data-ttu-id="1ae40-117">Redigeerige vajaduse korral päringut.</span><span class="sxs-lookup"><span data-stu-id="1ae40-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="1ae40-118">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ae40-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="1ae40-119">Kasutajate välistamine automaatsest rollimäärangust</span><span class="sxs-lookup"><span data-stu-id="1ae40-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="1ae40-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ae40-120">Close the page.</span></span>
2. <span data-ttu-id="1ae40-121">Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.</span><span class="sxs-lookup"><span data-stu-id="1ae40-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="1ae40-122">Tehke puustruktuuris valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="1ae40-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="1ae40-123">Valige roll.</span><span class="sxs-lookup"><span data-stu-id="1ae40-123">Select a role.</span></span> <span data-ttu-id="1ae40-124">Selles näites tehke valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="1ae40-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="1ae40-125">Valige menüüs **Rollile määratud kasutajad** suvand **Määra käsitsi / välista kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="1ae40-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="1ae40-126">Märkige loendis **Määra kasutajad rollidesse või välista rollidest** valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1ae40-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="1ae40-127">Valige kasutaja.</span><span class="sxs-lookup"><span data-stu-id="1ae40-127">Select a user.</span></span>  
6. <span data-ttu-id="1ae40-128">Valige paanil **Toimingupaan** suvand **Välista rollist**.</span><span class="sxs-lookup"><span data-stu-id="1ae40-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="1ae40-129">Klõpsake suvandit **Välista rollist** valitud kasutajate rollist välistamiseks.</span><span class="sxs-lookup"><span data-stu-id="1ae40-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="1ae40-130">Erandite eemaldamiseks valige kasutajad, kelle puhul soovite erandid eemaldada, ja klõpsake seejärel käsku **Lähtesta olek**.</span><span class="sxs-lookup"><span data-stu-id="1ae40-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="1ae40-131">Kui eemaldate välistamise, lähtestades kasutaja olek, määratakse kasutaja roll uuesti automaatselt.</span><span class="sxs-lookup"><span data-stu-id="1ae40-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="1ae40-132">Kuid kasutajale ei määrata kohe rolli ega välistate rolli, kui oleku lähtestate.</span><span class="sxs-lookup"><span data-stu-id="1ae40-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="1ae40-133">Selle asemel määratakse kasutajale roll või temalt eemaldatakse roll järgmisel korral, kui käitatakse automaatse rollimäärangu reeglit.</span><span class="sxs-lookup"><span data-stu-id="1ae40-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
