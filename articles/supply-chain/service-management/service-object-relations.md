---
title: Hooldusobjekti seosed
description: Saate luua hooldusobjektide vahelisi seoseid, kas hooldusobjekti ja hooldusleppe või hooldustellimuse vahel.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c196a070d1e18b2cc14c54eda0fe0aad5346d93
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215121"
---
# <a name="service-object-relations"></a><span data-ttu-id="d9ee5-103">Hooldusobjekti seosed</span><span class="sxs-lookup"><span data-stu-id="d9ee5-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9ee5-104">Saate luua hooldusobjektide vahelisi seoseid, kas hooldusobjekti ja hooldusleppe või hooldustellimuse vahel.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="d9ee5-105">Seose loomisel lisate hooldusobjekti hooldusleppele või hooldustellimusele.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="d9ee5-106">Kui seos on loodud, saate lisada hooldusobjekti mistahes hooldusleppe või hooldustellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="d9ee5-107">Mallkooslused</span><span class="sxs-lookup"><span data-stu-id="d9ee5-107">Template BOMs</span></span>

<span data-ttu-id="d9ee5-108">Saate täpsustada ka objektisuhte mallkooslust.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="d9ee5-109">Mallkooslus on teenust osutatavale objektile.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="d9ee5-110">Hooldusvisiidi ajal hooldusobjekti komponendi asendamise saate registreerida hoolduse mallkooslusele, kasutades selleks vormi Hooldusobjektid.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="d9ee5-111">Näide</span><span class="sxs-lookup"><span data-stu-id="d9ee5-111">Example</span></span>

<span data-ttu-id="d9ee5-112">Te loote hooldusleppe kahe lifti hooldamiseks.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="d9ee5-113">Hooldusleppe identifikaator on SAL-001.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="d9ee5-114">Liftid on objektidena määratud vormis Hooldusobjektid kui EL-S/1000 ja EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="d9ee5-115">Teie lisate hooldusobjektid EL-S/1000 ja EL-L/1000 teenusleppele.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="d9ee5-116">Registreerige hooldusobjektile koosluse muudatused, kuna te asendasite objekti komponendid, seega lisate hooldusobjekti seosele hoolduskoosluse, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="d9ee5-117">Hooldusobjekt</span><span class="sxs-lookup"><span data-stu-id="d9ee5-117">Service object</span></span> | <span data-ttu-id="d9ee5-118">Seos – hoolduslepe</span><span class="sxs-lookup"><span data-stu-id="d9ee5-118">Relation – Service agreement</span></span> | <span data-ttu-id="d9ee5-119">Hoolduskooslus</span><span class="sxs-lookup"><span data-stu-id="d9ee5-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="d9ee5-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-120">EL-S/1000</span></span>      | <span data-ttu-id="d9ee5-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="d9ee5-121">ID SAL-001</span></span>                   | <span data-ttu-id="d9ee5-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="d9ee5-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-123">EL-L/1000</span></span>      | <span data-ttu-id="d9ee5-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="d9ee5-124">ID SAL-001</span></span>                   | <span data-ttu-id="d9ee5-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="d9ee5-126">Tänu sellele, et leppele rakenduvad hooldusobjekti seosed, saate nende objektidega luua hooldusleppe ridasid, nagu näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="d9ee5-127">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="d9ee5-127">Transaction type</span></span> | <span data-ttu-id="d9ee5-128">Kategooria</span><span class="sxs-lookup"><span data-stu-id="d9ee5-128">Category</span></span>           | <span data-ttu-id="d9ee5-129">Hooldusobjekt</span><span class="sxs-lookup"><span data-stu-id="d9ee5-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="d9ee5-130">Tund</span><span class="sxs-lookup"><span data-stu-id="d9ee5-130">Hour</span></span>             | <span data-ttu-id="d9ee5-131">Kontroll</span><span class="sxs-lookup"><span data-stu-id="d9ee5-131">Inspection</span></span>         | <span data-ttu-id="d9ee5-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-132">EL-S/1000</span></span>      |
| <span data-ttu-id="d9ee5-133">Tund</span><span class="sxs-lookup"><span data-stu-id="d9ee5-133">Hour</span></span>             | <span data-ttu-id="d9ee5-134">Käigukasti puhastamine</span><span class="sxs-lookup"><span data-stu-id="d9ee5-134">Gear box cleaning</span></span>  | <span data-ttu-id="d9ee5-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-135">EL-S/1000</span></span>      |
| <span data-ttu-id="d9ee5-136">Kaup</span><span class="sxs-lookup"><span data-stu-id="d9ee5-136">Item</span></span>             | <span data-ttu-id="d9ee5-137">Puhastusvahendid</span><span class="sxs-lookup"><span data-stu-id="d9ee5-137">Cleaning materials</span></span> | <span data-ttu-id="d9ee5-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-138">EL-S/1000</span></span>      |
| <span data-ttu-id="d9ee5-139">Tund</span><span class="sxs-lookup"><span data-stu-id="d9ee5-139">Hour</span></span>             | <span data-ttu-id="d9ee5-140">Kontroll</span><span class="sxs-lookup"><span data-stu-id="d9ee5-140">Inspection</span></span>         | <span data-ttu-id="d9ee5-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-141">EL-L/1000</span></span>      |
| <span data-ttu-id="d9ee5-142">Tund</span><span class="sxs-lookup"><span data-stu-id="d9ee5-142">Hour</span></span>             | <span data-ttu-id="d9ee5-143">Käigukasti puhastamine</span><span class="sxs-lookup"><span data-stu-id="d9ee5-143">Gearbox cleaning</span></span>   | <span data-ttu-id="d9ee5-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-144">EL-L/1000</span></span>      |
| <span data-ttu-id="d9ee5-145">Kaup</span><span class="sxs-lookup"><span data-stu-id="d9ee5-145">Item</span></span>             | <span data-ttu-id="d9ee5-146">Puhastusvahendid</span><span class="sxs-lookup"><span data-stu-id="d9ee5-146">Cleaning materials</span></span> | <span data-ttu-id="d9ee5-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d9ee5-147">EL-L/1000</span></span>      |

<span data-ttu-id="d9ee5-148">Teenusvisiidi käigus peate asendama lifti EL-S/1000 käigukasti.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="d9ee5-149">Objekti komponendi välja vahetamisel pääsete hetke hooldusleppele seadistatud hooldusobjekti seost kasutades ligi koosluse koostajale.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="d9ee5-150">Ligipääs koosluse koostajale hooldusobjekti seost kasutades</span><span class="sxs-lookup"><span data-stu-id="d9ee5-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="d9ee5-151">Hoolduslepped</span><span class="sxs-lookup"><span data-stu-id="d9ee5-151">Service agreements</span></span>
2. <span data-ttu-id="d9ee5-152">Topeltklõpsake hoolduslepet või klõpsake valikut Hoolduslepe, et luua uus hoolduslepe.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="d9ee5-153">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="d9ee5-154">Teenusleppele mallkoosluse lisamiseks klõpsake valikut Hooldusobjektid.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="d9ee5-155">Vormis Hooldusobjektid klõpsake valikut Kujundamine vormi Kujundamine avamiseks, et muuta mallkooslust.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="d9ee5-156">Automaatselt loodud hooldustellimused</span><span class="sxs-lookup"><span data-stu-id="d9ee5-156">Automatically created service orders</span></span>

<span data-ttu-id="d9ee5-157">Hooldusleppele automaatselt hooldustellimuste loomisel liiguvad ka lepete hooldusobjekti seosed loodud hooldustellimustesse.</span><span class="sxs-lookup"><span data-stu-id="d9ee5-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

