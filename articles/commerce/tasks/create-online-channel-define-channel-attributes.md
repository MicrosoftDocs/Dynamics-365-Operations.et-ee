---
title: Võrgukanali loomine ja kanaliatribuutide määratlemine
description: See protseduur juhendab uue võrgukanali loomisel ja selle lisamisel organisatsiooni hierarhiasse.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f15b035c01801041d637a2d315d8a3ddcc9d6540
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140928"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="43f0f-103">Võrgukanali loomine ja kanaliatribuutide määratlemine</span><span class="sxs-lookup"><span data-stu-id="43f0f-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43f0f-104">See protseduur juhendab uue võrgukanali loomisel ja selle lisamisel organisatsiooni hierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="43f0f-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="43f0f-105">Organisatsiooni hierarhia tuleb luua enne uue võrgukanali loomist.</span><span class="sxs-lookup"><span data-stu-id="43f0f-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="43f0f-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="43f0f-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="43f0f-107">Uue võrgukanali loomine</span><span class="sxs-lookup"><span data-stu-id="43f0f-107">Create a new online channel</span></span>
1. <span data-ttu-id="43f0f-108">Avage Jaemüük ja kaubandus > Kanalid > Veebipoed.</span><span class="sxs-lookup"><span data-stu-id="43f0f-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="43f0f-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="43f0f-109">Click New.</span></span>
3. <span data-ttu-id="43f0f-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="43f0f-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="43f0f-111">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="43f0f-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="43f0f-112">Tehke valik väljal Salvesta ajavöönd.</span><span class="sxs-lookup"><span data-stu-id="43f0f-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="43f0f-113">Valige või sisestage väärtus väljal Default customer (Vaikimisi klient).</span><span class="sxs-lookup"><span data-stu-id="43f0f-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="43f0f-114">Valige või sisestage väärtus väljal Kliendi aadressiraamat.</span><span class="sxs-lookup"><span data-stu-id="43f0f-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="43f0f-115">Valige või sisestage väärtus väljal Terms of payment (Makse tingimused).</span><span class="sxs-lookup"><span data-stu-id="43f0f-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="43f0f-116">Valige või sisestage väärtus väljal Makseviis.</span><span class="sxs-lookup"><span data-stu-id="43f0f-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="43f0f-117">Sisestage või valige väärtus väljal Email notification profile (E-posti teatise profiil).</span><span class="sxs-lookup"><span data-stu-id="43f0f-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="43f0f-118">Laiendage jaotist Financial dimensions (Finantsdimensioonid).</span><span class="sxs-lookup"><span data-stu-id="43f0f-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="43f0f-119">Sisestage või valige välja Äriüksus väärtus.</span><span class="sxs-lookup"><span data-stu-id="43f0f-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="43f0f-120">Samuti saate määrata teiste vaikedimensioonide väärtused.</span><span class="sxs-lookup"><span data-stu-id="43f0f-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="43f0f-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="43f0f-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="43f0f-122">Võrgukanali lisamine organisatsiooni hierarhiasse</span><span class="sxs-lookup"><span data-stu-id="43f0f-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="43f0f-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="43f0f-123">Close the page.</span></span>
2. <span data-ttu-id="43f0f-124">Avage Organisatsiooni haldus > Organisatsioonid > Organisatsiooni hierarhiad.</span><span class="sxs-lookup"><span data-stu-id="43f0f-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="43f0f-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="43f0f-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="43f0f-126">Klõpsake käsku Kuva.</span><span class="sxs-lookup"><span data-stu-id="43f0f-126">Click View.</span></span>
5. <span data-ttu-id="43f0f-127">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="43f0f-127">Click Edit.</span></span>
    * <span data-ttu-id="43f0f-128">Saate valida ükskõik, millise hierarhiasõlme, millesse soovite uue kanali lisada.</span><span class="sxs-lookup"><span data-stu-id="43f0f-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="43f0f-129">Klõpsake nuppu Sisesta.</span><span class="sxs-lookup"><span data-stu-id="43f0f-129">Click Insert.</span></span>
7. <span data-ttu-id="43f0f-130">Klõpsake nuppu ärikanal.</span><span class="sxs-lookup"><span data-stu-id="43f0f-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="43f0f-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="43f0f-131">Click OK.</span></span>
9. <span data-ttu-id="43f0f-132">Rippdialoogi avamiseks klõpsake käsku Avalda.</span><span class="sxs-lookup"><span data-stu-id="43f0f-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="43f0f-133">Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="43f0f-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="43f0f-134">Klõpsake Avalda.</span><span class="sxs-lookup"><span data-stu-id="43f0f-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="43f0f-135">Tellimuste konfigureerimine peaaegu reaalajas teatiste jaoks</span><span class="sxs-lookup"><span data-stu-id="43f0f-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="43f0f-136">Minge jaotisse Jaemüük ja kaubandus > Peakontori seadistamine > Parameetrid > Kaubanduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="43f0f-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="43f0f-137">Määrake reaalajas kasutamise teenus e-kaubanduse tellimuste loomiseks väärtusele Jah.</span><span class="sxs-lookup"><span data-stu-id="43f0f-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="43f0f-138">Kävitage jaotusgraafik 1070 muudatuste sünkroonimiseks kanali andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="43f0f-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


