---
title: Ettevõttesisese kaupade liikumise ülekandedokumentide seadistamine
description: See protseduur näitab, kuidas koostada üleviimisdokumente kaupade liikumisel ettevõtte sees.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe4dd04595c961e1c66178e6ac6955e945869ded
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185677"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="17acc-103">Ettevõttesisese kaupade liikumise ülekandedokumentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="17acc-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17acc-104">See protseduur näitab, kuidas koostada üleviimisdokumente kaupade liikumisel ettevõtte sees.</span><span class="sxs-lookup"><span data-stu-id="17acc-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="17acc-105">See protseduur on saadaval ainult juriidilistele isikutele, kelle esmane aadress on Leedus.</span><span class="sxs-lookup"><span data-stu-id="17acc-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="17acc-106">Selle protseduuri loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Leedu, andmeid.</span><span class="sxs-lookup"><span data-stu-id="17acc-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="17acc-107">Enne seda protseduuri tuleb teha protseduur Kaupade liikumise ülekandedokumendi seadistamine ettevõtte sees.</span><span class="sxs-lookup"><span data-stu-id="17acc-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="17acc-108">See protseduur on mõeldud laoraamatupidajatele.</span><span class="sxs-lookup"><span data-stu-id="17acc-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="17acc-109">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="17acc-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="17acc-110">Üleviimistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="17acc-110">Create a transfer order</span></span>
1. <span data-ttu-id="17acc-111">Avage Varude haldamine > Sissetulevad tellimused > Üleviimistellimus.</span><span class="sxs-lookup"><span data-stu-id="17acc-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="17acc-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="17acc-112">Click New.</span></span>
3. <span data-ttu-id="17acc-113">Sisestage või valige väärtus väljal Laost.</span><span class="sxs-lookup"><span data-stu-id="17acc-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="17acc-114">Sisestage või valige väärtus väljal Lattu.</span><span class="sxs-lookup"><span data-stu-id="17acc-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="17acc-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="17acc-115">Click Add.</span></span>
6. <span data-ttu-id="17acc-116">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="17acc-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="17acc-117">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="17acc-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="17acc-118">Üleviimistellimuse transpordi üksikasjade sisestamine</span><span class="sxs-lookup"><span data-stu-id="17acc-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="17acc-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="17acc-119">Click Save.</span></span>
2. <span data-ttu-id="17acc-120">Klõpsake tegumiribal valikut Läheta.</span><span class="sxs-lookup"><span data-stu-id="17acc-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="17acc-121">Klõpsake valikut Transpordi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="17acc-121">Click Transportation details.</span></span>
4. <span data-ttu-id="17acc-122">Tehke väljal Prindi transpordi üksikasjad valik Jah.</span><span class="sxs-lookup"><span data-stu-id="17acc-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="17acc-123">Valige või sisestage väärtus väljal Kauba väljastaja.</span><span class="sxs-lookup"><span data-stu-id="17acc-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="17acc-124">Tippige väärtus väljale Pakk.</span><span class="sxs-lookup"><span data-stu-id="17acc-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="17acc-125">Tippige väärtus väljale Koorma riskitase.</span><span class="sxs-lookup"><span data-stu-id="17acc-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="17acc-126">Valige või sisestage väärtus väljal Vedaja.</span><span class="sxs-lookup"><span data-stu-id="17acc-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="17acc-127">Valige või sisestage väärtus väljal Mudel.</span><span class="sxs-lookup"><span data-stu-id="17acc-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="17acc-128">Tippige väärtus väljale Registreerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="17acc-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="17acc-129">Tippige väärtus väljale Treileri registreerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="17acc-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="17acc-130">Valige või sisestage väärtus väljal Juht.</span><span class="sxs-lookup"><span data-stu-id="17acc-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="17acc-131">Tippige väärtus väljale Juhi nimi.</span><span class="sxs-lookup"><span data-stu-id="17acc-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="17acc-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="17acc-132">Click Save.</span></span>
15. <span data-ttu-id="17acc-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="17acc-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="17acc-134">Sisestamata üleviimistellimuse saatelehe kuvamine</span><span class="sxs-lookup"><span data-stu-id="17acc-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="17acc-135">Klõpsake suvandit Saateleht.</span><span class="sxs-lookup"><span data-stu-id="17acc-135">Click Packing slip.</span></span>
2. <span data-ttu-id="17acc-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="17acc-136">Click OK.</span></span>
3. <span data-ttu-id="17acc-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="17acc-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="17acc-138">Sisestatud üleviimistellimuse saatelehe kuvamine</span><span class="sxs-lookup"><span data-stu-id="17acc-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="17acc-139">Klõpsake tegumiribal valikut Üleviimistellimus.</span><span class="sxs-lookup"><span data-stu-id="17acc-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="17acc-140">Klõpsake tegumiribal valikut Läheta.</span><span class="sxs-lookup"><span data-stu-id="17acc-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="17acc-141">Klõpsake valikut Lähetuse üleviimistellimus.</span><span class="sxs-lookup"><span data-stu-id="17acc-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="17acc-142">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="17acc-142">Click the General tab.</span></span>
5. <span data-ttu-id="17acc-143">Tehke valik väljal Uuenda.</span><span class="sxs-lookup"><span data-stu-id="17acc-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="17acc-144">Klõpsake vahekaarti Ülevaade.</span><span class="sxs-lookup"><span data-stu-id="17acc-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="17acc-145">Sisestage väärtus väljale Saateleht.</span><span class="sxs-lookup"><span data-stu-id="17acc-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="17acc-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="17acc-146">Click OK.</span></span>
9. <span data-ttu-id="17acc-147">Klõpsake tegumiribal valikut Läheta.</span><span class="sxs-lookup"><span data-stu-id="17acc-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="17acc-148">Klõpsake suvandit Saateleht.</span><span class="sxs-lookup"><span data-stu-id="17acc-148">Click Packing slip.</span></span>
11. <span data-ttu-id="17acc-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="17acc-149">Click OK.</span></span>
