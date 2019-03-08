---
title: Kasutajate määramine turberollidesse
description: Microsoft Dynamics 365 for Finance and Operations, Enterprise editionile juurdepääsuks peavad kasutajatele olema määratud turberollid.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "349948"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="2bf8d-103">Kasutajate määramine turberollidesse</span><span class="sxs-lookup"><span data-stu-id="2bf8d-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2bf8d-104">Microsoft Dynamics 365 for Finance and Operations, Enterprise editionile juurdepääsuks peavad kasutajatele olema määratud turberollid.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="2bf8d-105">See protseduur selgitab, kuidas süsteemiadministraatorid saavad määrata kasutajatele automaatselt rolle äriandmete alusel.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="2bf8d-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="2bf8d-107">Kasutajate automaatsel rollidesse määramine</span><span class="sxs-lookup"><span data-stu-id="2bf8d-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="2bf8d-108">Minge jaotisesse Süsteemihaldus > Turve > Kasutajate rollidesse määramine.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="2bf8d-109">Tehke puustruktuuris valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="2bf8d-110">Valige roll, millele soovite reegli konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="2bf8d-111">Selles näites tehle valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="2bf8d-112">Klõpsake suvandit Lisa reegel rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="2bf8d-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2bf8d-114">Valige päring, mida selle reegli puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="2bf8d-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2bf8d-116">Klõpsake suvandit Redigeeri päringut.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-116">Click Edit query.</span></span>
    * <span data-ttu-id="2bf8d-117">Redigeerige vajaduse korral päringut.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="2bf8d-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="2bf8d-119">Kasutajate välistamine automaatsest rollimäärangust</span><span class="sxs-lookup"><span data-stu-id="2bf8d-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="2bf8d-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-120">Close the page.</span></span>
2. <span data-ttu-id="2bf8d-121">Minge jaotisesse Süsteemihaldus > Turve > Kasutajate rollidesse määramine.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="2bf8d-122">Tehke puustruktuuris valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="2bf8d-123">Valige roll.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-123">Select a role.</span></span> <span data-ttu-id="2bf8d-124">Selles näites tehke valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="2bf8d-125">Klõpsake suvandit Kasutajate käsitsi määramine/välistamine.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="2bf8d-126">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2bf8d-127">Valige kasutaja.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-127">Select a user.</span></span>  
6. <span data-ttu-id="2bf8d-128">Klõpsake suvandit Välista rollist.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="2bf8d-129">Klõpsake suvandit Välista rollist valitud kasutajate rollist välistamiseks.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="2bf8d-130">Erandite eemaldamiseks valige kasutajad, kelle puhul soovite erandid eemaldada, ja klõpsake seejärel käsku Lähtesta olek.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="2bf8d-131">Kui eemaldate välistamise, lähtestades kasutaja olek, määratakse kasutaja roll uuesti automaatselt.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="2bf8d-132">Kuid kasutajale ei määrata kohe rolli ega välistate rolli, kui oleku lähtestate.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="2bf8d-133">Selle asemel määratakse kasutajale roll või temalt eemaldatakse roll järgmisel korral, kui käitatakse automaatse rollimäärangu reeglit.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

