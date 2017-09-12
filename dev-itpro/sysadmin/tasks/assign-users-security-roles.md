--- 
title: "Kasutajate määramine turberollidesse"
description: "Rakendusele Microsoft Dynamics 365 for Finance and Operations, Enterprise edition tuleb määrata kasutajatele turberoll."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="c31a2-103">Kasutajate määramine turberollidesse</span><span class="sxs-lookup"><span data-stu-id="c31a2-103">Assign users to security roles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c31a2-104">Rakendusele Microsoft Dynamics 365 for Finance and Operations, Enterprise edition tuleb määrata kasutajatele turberoll.</span><span class="sxs-lookup"><span data-stu-id="c31a2-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="c31a2-105">See protseduur selgitab, kuidas süsteemiadministraatorid saavad määrata kasutajatele automaatselt rolle äriandmete alusel.</span><span class="sxs-lookup"><span data-stu-id="c31a2-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="c31a2-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="c31a2-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="c31a2-107">Kasutajate automaatsel rollidesse määramine</span><span class="sxs-lookup"><span data-stu-id="c31a2-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="c31a2-108">Minge jaotisesse Süsteemihaldus > Turve > Kasutajate rollidesse määramine.</span><span class="sxs-lookup"><span data-stu-id="c31a2-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="c31a2-109">Tehke puustruktuuris valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="c31a2-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="c31a2-110">Valige roll, millele soovite reegli konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="c31a2-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="c31a2-111">Selles näites tehle valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="c31a2-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="c31a2-112">Klõpsake suvandit Lisa reegel rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c31a2-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="c31a2-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c31a2-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c31a2-114">Valige päring, mida selle reegli puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="c31a2-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="c31a2-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c31a2-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c31a2-116">Klõpsake suvandit Redigeeri päringut.</span><span class="sxs-lookup"><span data-stu-id="c31a2-116">Click Edit query.</span></span>
    * <span data-ttu-id="c31a2-117">Redigeerige vajaduse korral päringut.</span><span class="sxs-lookup"><span data-stu-id="c31a2-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="c31a2-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c31a2-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="c31a2-119">Kasutajate välistamine automaatsest rollimäärangust</span><span class="sxs-lookup"><span data-stu-id="c31a2-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="c31a2-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c31a2-120">Close the page.</span></span>
2. <span data-ttu-id="c31a2-121">Minge jaotisesse Süsteemihaldus > Turve > Kasutajate rollidesse määramine.</span><span class="sxs-lookup"><span data-stu-id="c31a2-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="c31a2-122">Tehke puustruktuuris valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="c31a2-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="c31a2-123">Valige roll.</span><span class="sxs-lookup"><span data-stu-id="c31a2-123">Select a role.</span></span> <span data-ttu-id="c31a2-124">Selles näites tehke valik Raamatupidaja.</span><span class="sxs-lookup"><span data-stu-id="c31a2-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="c31a2-125">Klõpsake suvandit Kasutajate käsitsi määramine/välistamine.</span><span class="sxs-lookup"><span data-stu-id="c31a2-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="c31a2-126">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="c31a2-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c31a2-127">Valige kasutaja.</span><span class="sxs-lookup"><span data-stu-id="c31a2-127">Select a user.</span></span>  
6. <span data-ttu-id="c31a2-128">Klõpsake suvandit Välista rollist.</span><span class="sxs-lookup"><span data-stu-id="c31a2-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="c31a2-129">Klõpsake suvandit Välista rollist valitud kasutajate rollist välistamiseks.</span><span class="sxs-lookup"><span data-stu-id="c31a2-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="c31a2-130">Erandite eemaldamiseks valige kasutajad, kelle puhul soovite erandid eemaldada, ja klõpsake seejärel käsku Lähtesta olek.</span><span class="sxs-lookup"><span data-stu-id="c31a2-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="c31a2-131">Kui eemaldate välistamise, lähtestades kasutaja olek, määratakse kasutaja roll uuesti automaatselt.</span><span class="sxs-lookup"><span data-stu-id="c31a2-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="c31a2-132">Kuid kasutajale ei määrata kohe rolli ega välistate rolli, kui oleku lähtestate.</span><span class="sxs-lookup"><span data-stu-id="c31a2-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="c31a2-133">Selle asemel määratakse kasutajale roll või temalt eemaldatakse roll järgmisel korral, kui käitatakse automaatse rollimäärangu reeglit.</span><span class="sxs-lookup"><span data-stu-id="c31a2-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


