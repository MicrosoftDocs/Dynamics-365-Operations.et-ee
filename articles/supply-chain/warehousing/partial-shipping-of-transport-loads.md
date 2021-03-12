---
title: Transpordikoorma osaline saadetis
description: Selles teemas selgitatakse, kuidas saate koorma lähetada osaliselt ja koorma võimsuse planeerimise edasi lükata.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 68a3d175e89e89d0909b140863b1aa61a184fce6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963281"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="dcdee-103">Transpordikoorma osaline saadetis</span><span class="sxs-lookup"><span data-stu-id="dcdee-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dcdee-104">Koormate osalise saadetise loomisel saate käsitleda koormaid, kus võimsust ei saa määrata enne, kui kõik müügiread on koormale lisatud.</span><span class="sxs-lookup"><span data-stu-id="dcdee-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="dcdee-105">Protsessi saab lõpule viia, kui täpne kaubaaluste arv on teada.</span><span class="sxs-lookup"><span data-stu-id="dcdee-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="dcdee-106">Seega peate otsustama, millise kaubaaluseid määratakse millisele transpordile, alles siis, kui transporti laaditakse füüsiliselt etapiviisilistest varudest välja.</span><span class="sxs-lookup"><span data-stu-id="dcdee-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="dcdee-107">See funktsioon pakub alternatiivi jäigema struktuuri rakendamisele, kus peate juba enne komplekteerimis- või laadimistöö loomist otsustama, milliseid kaubaaluseid määratakse millisele transpordile.</span><span class="sxs-lookup"><span data-stu-id="dcdee-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="dcdee-108">Selle asemel saavad kasutajad konfigureerida individuaalseid koormaid osalise saadetise kinnituse jaoks.</span><span class="sxs-lookup"><span data-stu-id="dcdee-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="dcdee-109">Seejärel saavad toimuda nende koormate transpordi laadimise protsessid.</span><span class="sxs-lookup"><span data-stu-id="dcdee-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="dcdee-110">Seetõttu saab transpordi planeerimise osakond planeerida koormaid ilma individuaalsete transportide võimsusi arvestamata.</span><span class="sxs-lookup"><span data-stu-id="dcdee-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="dcdee-111">Laadimise ajal saavad töötajad määratleda uue transpordikoorma, millele saab laadida kaubaaluse.</span><span class="sxs-lookup"><span data-stu-id="dcdee-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="dcdee-112">Teise võimalusena saavad tuvastada olemasoleva transpordikoorma.</span><span class="sxs-lookup"><span data-stu-id="dcdee-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="dcdee-113">Neid andmeid saab salvestada mobiilse seadme kaudu.</span><span class="sxs-lookup"><span data-stu-id="dcdee-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="dcdee-114">Seetõttu saavad erinevad laotöötajad laadida varusid samast või erinevatest koormatest samale veokile.</span><span class="sxs-lookup"><span data-stu-id="dcdee-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="dcdee-115">Koormaid saab seejärel lähetada täielikult või osaliselt.</span><span class="sxs-lookup"><span data-stu-id="dcdee-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="dcdee-116">Varude laadimiseks koormast kindlasse transpordikoormasse ja koorma osaliseks lähetamiseks tuleb luua töö, kasutades töömallis laadimisklassi.</span><span class="sxs-lookup"><span data-stu-id="dcdee-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="dcdee-117">Tavalist komplekteerimistööd tüübiga **Komplekteerimine** ei saa transpordikoormale (nt veok) laadida.</span><span class="sxs-lookup"><span data-stu-id="dcdee-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="dcdee-118">Transpordikoorma seadistamine osalise saadetise jaoks</span><span class="sxs-lookup"><span data-stu-id="dcdee-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="dcdee-119">Koormate seadistamine osalise saadetise jaoks koosneb kahest järgmisest protseduurist.</span><span class="sxs-lookup"><span data-stu-id="dcdee-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="dcdee-120">Laadimisstrateegia määramine</span><span class="sxs-lookup"><span data-stu-id="dcdee-120">Set the loading strategy</span></span>

<span data-ttu-id="dcdee-121">Peate lubama osalise laadimise, määrates laadimisstrateegia.</span><span class="sxs-lookup"><span data-stu-id="dcdee-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="dcdee-122">Laadimisstrateegia saate määrata pärast koorma loomist.</span><span class="sxs-lookup"><span data-stu-id="dcdee-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="dcdee-123">Valige **Laohaldus** \> **Koormad** \> **Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="dcdee-124">Valige koorem ja klõpsake suvandil **Päis**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="dcdee-125">Väljal **Laadimisstrateegia** valige **Osalise koorma lähetamine on lubatud**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="dcdee-126">Menüükäsu loomine transpordikoormate laadimiseks</span><span class="sxs-lookup"><span data-stu-id="dcdee-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="dcdee-127">Peate looma uue menüükäsu, mis lubab laadida transpordikoormaid.</span><span class="sxs-lookup"><span data-stu-id="dcdee-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="dcdee-128">Transpordikoorem võimaldab grupeerida tööridu ühest või mitmest koormast.</span><span class="sxs-lookup"><span data-stu-id="dcdee-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="dcdee-129">Kõik, mis on lisatud transpordikoormale, saab seejärel lähetada mobiilse seadme skanneri abil.</span><span class="sxs-lookup"><span data-stu-id="dcdee-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="dcdee-130">Valige **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="dcdee-131">Valige **Uus** ja tehke siis väljal **Olek** valik **Töö**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="dcdee-132">Valige suvandi **Kasuta olemasolevat tööd** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="dcdee-133">Vahekaardil **Üldine** valige väljal **Juhtija:** suvand **Transpordi laadimine**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="dcdee-134">Saadetise kinnituse lubamiseks mobiilse seadme skanneris valige väljal **Lubatud lähetuskinnituse tüüp** suvand **Transpordikoorem**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="dcdee-135">Kliendilt tulnud transpordikoorma saadetise kinnitamine</span><span class="sxs-lookup"><span data-stu-id="dcdee-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="dcdee-136">Selle seadistuse abil saate kinnitada transpordikoorma, mis sisaldab saadetavat täielikku või osaliselt laaditud koormat.</span><span class="sxs-lookup"><span data-stu-id="dcdee-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="dcdee-137">Valige **Laohaldus** \> **Koormad** \> **Transpordikoormad**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="dcdee-138">Paani Tegumiriba vahekaardil **Läheta ja võta vastu** grupis **Kinnita** valige suvand **Transport**.</span><span class="sxs-lookup"><span data-stu-id="dcdee-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>
