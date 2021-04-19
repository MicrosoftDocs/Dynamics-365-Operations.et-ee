---
title: Seostatud tööga varude teisaldamine laohalduses
description: Varude liikumise abil saate otsustada, millistel laotöötajatel on reserveeritud varude teisaldamine lubatud.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6477a91b3c65e8be5ab527eaff12c92ae7918b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808746"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="5e40d-103">Seostatud tööga varude teisaldamine laohalduses</span><span class="sxs-lookup"><span data-stu-id="5e40d-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e40d-104">Varude liikumise abil saate otsustada, millistel laotöötajatel on reserveeritud varude teisaldamine lubatud.</span><span class="sxs-lookup"><span data-stu-id="5e40d-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="5e40d-105">See võimaldab paindlikkust reguleeritud ladudes, kus võite mitte lubada töötajal valida juba loodud komplekteerimistööle uut komplekteerimiskohta.</span><span class="sxs-lookup"><span data-stu-id="5e40d-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="5e40d-106">Samuti võimaldab see laojuhil kontrollida, millised võimalused väiksemate kogemustega töötajatel olema peaksid.</span><span class="sxs-lookup"><span data-stu-id="5e40d-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="5e40d-107">Laotöötajate igapäevatoimingute juhtimise paindlikkus võib olla abiks näiteks järgmistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="5e40d-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="5e40d-108">1. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="5e40d-108">Scenario 1</span></span>

<span data-ttu-id="5e40d-109">Ettevõttel on suhteliselt väike vastuvõtuala ja see on paigutamist ootavate aluste ja kastidega ummistatud.</span><span class="sxs-lookup"><span data-stu-id="5e40d-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="5e40d-110">Sellel päeval oodatakse suurt saadetist, seega otsustab vastuvõtuametnik vastuvõtuala tühjendada, viies mõned alused teisele sissetuleva kauba kogumisalale.</span><span class="sxs-lookup"><span data-stu-id="5e40d-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="5e40d-111">2. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="5e40d-111">Scenario 2</span></span>

<span data-ttu-id="5e40d-112">Kogenud laotöötaja märkab laos võimalust konsolideerida kaubad ühte kohta, selle asemel et hoida neid väikeste kogustena kolmes lähestikku asuvas kohas.</span><span class="sxs-lookup"><span data-stu-id="5e40d-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across three nearby locations with little quantity on each.</span></span> <span data-ttu-id="5e40d-113">Töötaja soovib konsolideerida koguse, viies kõigist neist kohtadest kaubad ühte kohta ja samale litsentsiplaadile.</span><span class="sxs-lookup"><span data-stu-id="5e40d-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="5e40d-114">3. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="5e40d-114">Scenario 3</span></span>

<span data-ttu-id="5e40d-115">Alus ootab laadimisukse BAYDOOR01 läheduses olevas kogumiskohas (nt STAGE01) teelepanekut.</span><span class="sxs-lookup"><span data-stu-id="5e40d-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="5e40d-116">Kuid plaanide muutumise tõttu on veok saabumas laadimisukse BAYDOOR04 juurde.</span><span class="sxs-lookup"><span data-stu-id="5e40d-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="5e40d-117">Lähetusametnik on sellest teadlik ja peab korraldama asjad nii, et veok ei peaks ootama laadimist laadimisuksest STAGE01.</span><span class="sxs-lookup"><span data-stu-id="5e40d-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="5e40d-118">Lähetusametnik otsustab viia selle saadetise kaubad kogumiskohast STAGE01 kogumiskohta STAGE04, mis on uuele sihtkohale lähemal.</span><span class="sxs-lookup"><span data-stu-id="5e40d-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="5e40d-119">Praegused piirangud</span><span class="sxs-lookup"><span data-stu-id="5e40d-119">Current limitations</span></span>

<span data-ttu-id="5e40d-120">Töö reserveerimised, mida saab üle viia, on ainult Müügitellimus, Üleviimistellimuse väljaminek, Üleviimistellimuse sissetulek, Ostutellimus ja Täiendustöö.</span><span class="sxs-lookup"><span data-stu-id="5e40d-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="5e40d-121">Kaupade teisaldamine on piiratud tööridade jagamise vältimiseks.</span><span class="sxs-lookup"><span data-stu-id="5e40d-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="5e40d-122">See tähendab, et kui teil on töörida kauba A 100 ühiku kohta asukohast Loc1, siis ei saa teisaldada sealt teise kohta ainult 30 ühikut kaubast A.</span><span class="sxs-lookup"><span data-stu-id="5e40d-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="5e40d-123">See tooks kaasa olemasoleva töörea jagamise kogusteks 30 ja 70, kuna asukohad on nüüd erinevad.</span><span class="sxs-lookup"><span data-stu-id="5e40d-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="5e40d-124">Kogumisstsenaariumide puhul, kus litsentsiplaat, millelt kauba teisaldate, või litsentsiplaat, millele kauba teisaldate, on määratud töötellimuse litsentsiplaadiks, on lubatud ainult kogu litsentsiplaadi teisaldamine, et sihtlitsentsiplaati mitte jagada.</span><span class="sxs-lookup"><span data-stu-id="5e40d-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>

<span data-ttu-id="5e40d-125">Praegu toetatakse ainult liikumist konkreetseks otstarbeks.</span><span class="sxs-lookup"><span data-stu-id="5e40d-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="5e40d-126">See tähendab, et reserveeritud varusid ei saa malli mobiilse seadme menüüelementide liikumise kaudu liigutada.</span><span class="sxs-lookup"><span data-stu-id="5e40d-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="5e40d-127">Reserveeritud varude teisaldamise õiguse seadistamine eraldi töötajatele</span><span class="sxs-lookup"><span data-stu-id="5e40d-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="5e40d-128">Märkige töötaja puhul, kellel on lubatud reserveeritud varusid teisaldada, ruut **Luba seostatud tööta varude teisaldamine** jaotises **Laohaldus \> Seadistus \> Töötaja**.</span><span class="sxs-lookup"><span data-stu-id="5e40d-128">For the worker who is allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management \> Setup \> Worker**.</span></span>  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
