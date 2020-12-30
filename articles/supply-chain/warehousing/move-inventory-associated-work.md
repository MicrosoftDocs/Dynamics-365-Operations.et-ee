---
title: Seostatud tööga varude teisaldamine laohalduses
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada osa komplekteerimise kinnitust mobiilselt seadmelt.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aee3af8da6610c16fc2d98091bfa3f01f1bd0f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426222"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="20dcf-103">Seostatud tööga varude teisaldamine laohalduses</span><span class="sxs-lookup"><span data-stu-id="20dcf-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20dcf-104">Varude liikumise abil saate otsustada, millistel laotöötajatel on reserveeritud varude teisaldamine lubatud.</span><span class="sxs-lookup"><span data-stu-id="20dcf-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="20dcf-105">See võimaldab paindlikkust reguleeritud ladudes, kus võite mitte lubada töötajal valida juba loodud komplekteerimistööle uut komplekteerimiskohta.</span><span class="sxs-lookup"><span data-stu-id="20dcf-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="20dcf-106">Samuti võimaldab see laojuhil kontrollida, millised võimalused väiksemate kogemustega töötajatel olema peaksid.</span><span class="sxs-lookup"><span data-stu-id="20dcf-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="20dcf-107">Laotöötajate igapäevatoimingute juhtimise paindlikkus võib olla abiks näiteks järgmistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="20dcf-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="20dcf-108">1. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="20dcf-108">Scenario 1</span></span>
<span data-ttu-id="20dcf-109">Ettevõttel on suhteliselt väike vastuvõtuala ja see on paigutamist ootavate aluste ja kastidega ummistatud.</span><span class="sxs-lookup"><span data-stu-id="20dcf-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="20dcf-110">Sellel päeval oodatakse suurt saadetist, seega otsustab vastuvõtuametnik vastuvõtuala tühjendada, viies mõned alused teisele sissetuleva kauba kogumisalale.</span><span class="sxs-lookup"><span data-stu-id="20dcf-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="20dcf-111">2. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="20dcf-111">Scenario 2</span></span>
<span data-ttu-id="20dcf-112">Kogenud laotöötaja märkab laos võimalust konsolideerida kaubad ühte kohta, selle asemel et hoida neid väikeste kogustena 3 lähestikku asuvas kohas.</span><span class="sxs-lookup"><span data-stu-id="20dcf-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="20dcf-113">Töötaja soovib konsolideerida koguse, viies kõigist neist kohtadest kaubad ühte kohta ja samale litsentsiplaadile.</span><span class="sxs-lookup"><span data-stu-id="20dcf-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="20dcf-114">3. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="20dcf-114">Scenario 3</span></span>
<span data-ttu-id="20dcf-115">Alus ootab laadimisukse BAYDOOR01 läheduses olevas kogumiskohas (nt STAGE01) teelepanekut.</span><span class="sxs-lookup"><span data-stu-id="20dcf-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="20dcf-116">Kuid plaanide muutumise tõttu on veok saabumas laadimisukse BAYDOOR04 juurde.</span><span class="sxs-lookup"><span data-stu-id="20dcf-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="20dcf-117">Lähetusametnik on sellest teadlik ja peab korraldama asjad nii, et veok ei peaks ootama laadimist laadimisuksest STAGE01.</span><span class="sxs-lookup"><span data-stu-id="20dcf-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="20dcf-118">Lähetusametnik otsustab viia selle saadetise kaubad kogumiskohast STAGE01 kogumiskohta STAGE04, mis on uuele sihtkohale lähemal.</span><span class="sxs-lookup"><span data-stu-id="20dcf-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="20dcf-119">Praegused piirangud</span><span class="sxs-lookup"><span data-stu-id="20dcf-119">Current limitations</span></span>

<span data-ttu-id="20dcf-120">Töö reserveerimised, mida saab üle viia, on ainult Müügitellimus, Üleviimistellimuse väljaminek, Üleviimistellimuse sissetulek, Ostutellimus ja Täiendustöö.</span><span class="sxs-lookup"><span data-stu-id="20dcf-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="20dcf-121">Kaupade teisaldamine on piiratud tööridade jagamise vältimiseks.</span><span class="sxs-lookup"><span data-stu-id="20dcf-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="20dcf-122">See tähendab, et kui teil on töörida kauba A 100 ühiku kohta asukohast Loc1, siis ei saa teisaldada sealt teise kohta ainult 30 ühikut kaubast A.</span><span class="sxs-lookup"><span data-stu-id="20dcf-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="20dcf-123">See tooks kaasa olemasoleva töörea jagamise kogusteks 30 ja 70, kuna asukohad on nüüd erinevad.</span><span class="sxs-lookup"><span data-stu-id="20dcf-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="20dcf-124">Kogumisstsenaariumide puhul, kus litsentsiplaat, millelt kauba teisaldate, või litsentsiplaat, millele kauba teisaldate, on määratud töötellimuse litsentsiplaadiks, on lubatud ainult kogu litsentsiplaadi teisaldamine, et sihtlitsentsiplaati mitte jagada.</span><span class="sxs-lookup"><span data-stu-id="20dcf-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="20dcf-125">Praegu toetatakse ainult liikumist konkreetseks otstarbeks.</span><span class="sxs-lookup"><span data-stu-id="20dcf-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="20dcf-126">See tähendab, et reserveeritud varusid ei saa malli mobiilse seadme menüüelementide liikumise kaudu liigutada.</span><span class="sxs-lookup"><span data-stu-id="20dcf-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="20dcf-127">Reserveeritud varude teisaldamise õiguse seadistamine eraldi töötajatele</span><span class="sxs-lookup"><span data-stu-id="20dcf-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="20dcf-128">Märkige töötaja puhul, kellel peaks olema lubatud reserveeritud varusid teisaldada, ruut **Luba seostatud tööta varude teisaldamine** jaotises **Laohaldus** > **Seadistus** > **Töötaja**.</span><span class="sxs-lookup"><span data-stu-id="20dcf-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="20dcf-129">Üle toodud</span><span class="sxs-lookup"><span data-stu-id="20dcf-129">Backported</span></span>

<span data-ttu-id="20dcf-130">See funktsioon on toodud üle ka rakendusse Microsoft Dynamics AX 2012 R3 ja tehakse CU12 osana kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="20dcf-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="20dcf-131">Selle saab KB numbri 3192548 kaudu ka eraldi alla laadida.</span><span class="sxs-lookup"><span data-stu-id="20dcf-131">It can also be downloaded individually through KB number 3192548.</span></span> 

