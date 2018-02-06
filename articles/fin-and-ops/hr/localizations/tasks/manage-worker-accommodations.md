--- 
title: "Töötajate majutuse haldamine"
description: "See protseduur annab ülevaate töökeskkonna erivajaduse tüüpide, nagu ergonoomilised toolid või perioodilised vaheajad, seadistamise kohta."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a05fec7b79003d5b98470d85644d70bd1dbac285
ms.openlocfilehash: 83c2495eb7602282d7bb97515e655f3dbd33cb4a
ms.contentlocale: et-ee
ms.lasthandoff: 02/06/2018

---
# <a name="manage-worker-accommodations"></a><span data-ttu-id="3d4e1-103">Töötajate majutuse haldamine</span><span class="sxs-lookup"><span data-stu-id="3d4e1-103">Manage worker accommodations</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="3d4e1-104">See protseduur annab ülevaate töökeskkonna erivajaduse tüüpide, nagu ergonoomilised toolid või perioodilised vaheajad, seadistamise kohta.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-104">This procedure walks through the steps for setting up work environment accommodation types, such as ergonomic chairs or periodic breaks.</span></span> <span data-ttu-id="3d4e1-105">Samuti näitab see, kuidas määrata neid erivajaduse tüüpe töötajale ja kas erivajaduse tüüp kinnitada või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-105">It also shows how to assign these accommodation types to a worker, and either approve or deny the accommodation type.</span></span> <span data-ttu-id="3d4e1-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="setup-accommodations"></a><span data-ttu-id="3d4e1-107">Erivajaduste seadistamine</span><span class="sxs-lookup"><span data-stu-id="3d4e1-107">Setup accommodations</span></span>
1. <span data-ttu-id="3d4e1-108">Avage Personaliarvestus > Seadistus > Erivajaduse tüübid.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-108">Go to Human resources > Setup > Accommodation types.</span></span>
2. <span data-ttu-id="3d4e1-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-109">Click New.</span></span>
3. <span data-ttu-id="3d4e1-110">Sisestage erivajaduse nimi väljale Erivajaduse tüüp.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-110">In the Accommodation type field, enter a name for the accommodation.</span></span> <span data-ttu-id="3d4e1-111">Näide: klaviatuur.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-111">Example: Keyboard.</span></span>
4. <span data-ttu-id="3d4e1-112">Sisestage erivajaduse kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-112">In the Description field, enter a description for the accommodation.</span></span> <span data-ttu-id="3d4e1-113">Näide: ergonoomiline klaviatuur.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-113">Example: Ergonomic Keyboard.</span></span>
5. <span data-ttu-id="3d4e1-114">Sisestage väljale Märkus mis tahes teave, mis aitab erivajadust selgitada.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-114">In the Note field, enter any information that helps to clarify the accommodation.</span></span>
6. <span data-ttu-id="3d4e1-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-115">Click Save.</span></span>
7. <span data-ttu-id="3d4e1-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-116">Close the page.</span></span>

## <a name="assign-accommodations"></a><span data-ttu-id="3d4e1-117">Erivajaduste määramine</span><span class="sxs-lookup"><span data-stu-id="3d4e1-117">Assign accommodations</span></span>
1. <span data-ttu-id="3d4e1-118">Avage Personaliarvestus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-118">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="3d4e1-119">Valige töötaja loendist.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-119">From the list, select an employee.</span></span>
3. <span data-ttu-id="3d4e1-120">Klõpsake töötaja nime, et näha üksikasju erivajadust taotleva töötaja kohta.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-120">Click the employee's name to view details about the employee who is requesting the accommodation.</span></span>
4. <span data-ttu-id="3d4e1-121">Laiendage kiirkaarti Isikuandmed.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-121">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="3d4e1-122">Klõpsake suvandit Erivajadused.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-122">Click Accommodations.</span></span>
6. <span data-ttu-id="3d4e1-123">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-123">Click New.</span></span>
7. <span data-ttu-id="3d4e1-124">Valige sobiv erivajadus väljalt Erivajaduse tüüp.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-124">In the Accommodation type field, select the appropriate accommodation.</span></span> <span data-ttu-id="3d4e1-125">Näide: klaviatuur.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-125">Example: Keyboard</span></span>
8. <span data-ttu-id="3d4e1-126">Sisestage väljale Tööülesanne erivajadust nõudev tööülesanne.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-126">In the Job task field, enter the work task that requires the accommodation.</span></span>
9. <span data-ttu-id="3d4e1-127">Sisestage sobiv olek väljale Olek.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-127">In the Status field, enter the appropriate status.</span></span> <span data-ttu-id="3d4e1-128">Näide: mõistlik.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-128">Example: Reasonable</span></span>
    * <span data-ttu-id="3d4e1-129">Saadaval on järgmised olekud.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-129">The following statuses are available.</span></span> <span data-ttu-id="3d4e1-130">Taotletud näitab, et erivajadus on loodud, kuid seda pole veel üle vaadatud.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-130">Requested indicates that the accommodation has been created but not yet reviewed.</span></span> <span data-ttu-id="3d4e1-131">Teostatav näitab, et erivajadus on teostatav ja täidetakse.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-131">Reasonable indicates that the accommodation is reasonable and will be granted.</span></span> <span data-ttu-id="3d4e1-132">Raskesti teostatav näitab, et erivajadus seab tööandjale põhjendamatu koormuse ja on tagasi lükatud.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-132">Undue hardship indicates that the accommodation will place an unreasonable burden on the employer, and has been denied.</span></span> <span data-ttu-id="3d4e1-133">Selles näites kinnitati taotlus kohe, kuna erivajaduse taotlus oli minimaalne.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-133">In this example, the request was approved immediately because the accommodation request was minimal.</span></span>  
10. <span data-ttu-id="3d4e1-134">Valige erivajaduse taotluse kinnitanud isik väljalt Aktsepteeritud.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-134">In the Accepted field, select the person who accepted the accommodation request.</span></span>
11. <span data-ttu-id="3d4e1-135">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-135">Click Select.</span></span>
12. <span data-ttu-id="3d4e1-136">Sisestage erivajaduse taotluse kinnitamise kuupäev ja kellaaeg väljale Aktsepteeritud.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-136">In the Accepted date field, enter the date and time when the accommodation request was accepted.</span></span>
13. <span data-ttu-id="3d4e1-137">Laiendage jaotist Märkus.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-137">Expand the Note section.</span></span>
14. <span data-ttu-id="3d4e1-138">Sisestage väljale Finants mis tahes teave või ressursi kulud, mis aitavad erivajaduse mõju selgitada.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-138">In the Financial field, enter any information or resource costs that helps to clarify the impact of the accommodation.</span></span>
    * <span data-ttu-id="3d4e1-139">Kui erivajadus on tagasi lükatud, saab välja Vastus kasutada näitamaks, miks taotlus tagasi lükati.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-139">If the accommodation has been denied, the Reply field can be used to indicate why a request was denied.</span></span>  
15. <span data-ttu-id="3d4e1-140">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-140">Click Save.</span></span>


