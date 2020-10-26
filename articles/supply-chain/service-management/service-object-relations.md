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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b1b76dffc2751d51c2a25d831fab512b747c15
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979350"
---
# <a name="service-object-relations"></a><span data-ttu-id="4fc2a-103">Hooldusobjekti seosed</span><span class="sxs-lookup"><span data-stu-id="4fc2a-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fc2a-104">Saate luua hooldusobjektide vahelisi seoseid, kas hooldusobjekti ja hooldusleppe või hooldustellimuse vahel.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="4fc2a-105">Seose loomisel lisate hooldusobjekti hooldusleppele või hooldustellimusele.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="4fc2a-106">Kui seos on loodud, saate lisada hooldusobjekti mistahes hooldusleppe või hooldustellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="4fc2a-107">Mallkooslused</span><span class="sxs-lookup"><span data-stu-id="4fc2a-107">Template BOMs</span></span>

<span data-ttu-id="4fc2a-108">Saate täpsustada ka objektisuhte mallkooslust.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="4fc2a-109">Mallkooslus on teenust osutatavale objektile.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="4fc2a-110">Hooldusvisiidi ajal hooldusobjekti komponendi asendamise saate registreerida hoolduse mallkooslusele, kasutades selleks vormi Hooldusobjektid.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="4fc2a-111">Näide</span><span class="sxs-lookup"><span data-stu-id="4fc2a-111">Example</span></span>

<span data-ttu-id="4fc2a-112">Te loote hooldusleppe kahe lifti hooldamiseks.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="4fc2a-113">Hooldusleppe identifikaator on SAL-001.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="4fc2a-114">Liftid on objektidena määratud vormis Hooldusobjektid kui EL-S/1000 ja EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="4fc2a-115">Teie lisate hooldusobjektid EL-S/1000 ja EL-L/1000 teenusleppele.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="4fc2a-116">Registreerige hooldusobjektile koosluse muudatused, kuna te asendasite objekti komponendid, seega lisate hooldusobjekti seosele hoolduskoosluse, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="4fc2a-117">Hooldusobjekt</span><span class="sxs-lookup"><span data-stu-id="4fc2a-117">Service object</span></span> | <span data-ttu-id="4fc2a-118">Seos – hoolduslepe</span><span class="sxs-lookup"><span data-stu-id="4fc2a-118">Relation – Service agreement</span></span> | <span data-ttu-id="4fc2a-119">Hoolduskooslus</span><span class="sxs-lookup"><span data-stu-id="4fc2a-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="4fc2a-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-120">EL-S/1000</span></span>      | <span data-ttu-id="4fc2a-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="4fc2a-121">ID SAL-001</span></span>                   | <span data-ttu-id="4fc2a-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="4fc2a-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-123">EL-L/1000</span></span>      | <span data-ttu-id="4fc2a-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="4fc2a-124">ID SAL-001</span></span>                   | <span data-ttu-id="4fc2a-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="4fc2a-126">Tänu sellele, et leppele rakenduvad hooldusobjekti seosed, saate nende objektidega luua hooldusleppe ridasid, nagu näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="4fc2a-127">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="4fc2a-127">Transaction type</span></span> | <span data-ttu-id="4fc2a-128">Kategooria</span><span class="sxs-lookup"><span data-stu-id="4fc2a-128">Category</span></span>           | <span data-ttu-id="4fc2a-129">Hooldusobjekt</span><span class="sxs-lookup"><span data-stu-id="4fc2a-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="4fc2a-130">Tund</span><span class="sxs-lookup"><span data-stu-id="4fc2a-130">Hour</span></span>             | <span data-ttu-id="4fc2a-131">Kontroll</span><span class="sxs-lookup"><span data-stu-id="4fc2a-131">Inspection</span></span>         | <span data-ttu-id="4fc2a-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-132">EL-S/1000</span></span>      |
| <span data-ttu-id="4fc2a-133">Tund</span><span class="sxs-lookup"><span data-stu-id="4fc2a-133">Hour</span></span>             | <span data-ttu-id="4fc2a-134">Käigukasti puhastamine</span><span class="sxs-lookup"><span data-stu-id="4fc2a-134">Gear box cleaning</span></span>  | <span data-ttu-id="4fc2a-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-135">EL-S/1000</span></span>      |
| <span data-ttu-id="4fc2a-136">Kaup</span><span class="sxs-lookup"><span data-stu-id="4fc2a-136">Item</span></span>             | <span data-ttu-id="4fc2a-137">Puhastusvahendid</span><span class="sxs-lookup"><span data-stu-id="4fc2a-137">Cleaning materials</span></span> | <span data-ttu-id="4fc2a-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-138">EL-S/1000</span></span>      |
| <span data-ttu-id="4fc2a-139">Tund</span><span class="sxs-lookup"><span data-stu-id="4fc2a-139">Hour</span></span>             | <span data-ttu-id="4fc2a-140">Kontroll</span><span class="sxs-lookup"><span data-stu-id="4fc2a-140">Inspection</span></span>         | <span data-ttu-id="4fc2a-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-141">EL-L/1000</span></span>      |
| <span data-ttu-id="4fc2a-142">Tund</span><span class="sxs-lookup"><span data-stu-id="4fc2a-142">Hour</span></span>             | <span data-ttu-id="4fc2a-143">Käigukasti puhastamine</span><span class="sxs-lookup"><span data-stu-id="4fc2a-143">Gearbox cleaning</span></span>   | <span data-ttu-id="4fc2a-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-144">EL-L/1000</span></span>      |
| <span data-ttu-id="4fc2a-145">Kaup</span><span class="sxs-lookup"><span data-stu-id="4fc2a-145">Item</span></span>             | <span data-ttu-id="4fc2a-146">Puhastusvahendid</span><span class="sxs-lookup"><span data-stu-id="4fc2a-146">Cleaning materials</span></span> | <span data-ttu-id="4fc2a-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="4fc2a-147">EL-L/1000</span></span>      |

<span data-ttu-id="4fc2a-148">Teenusvisiidi käigus peate asendama lifti EL-S/1000 käigukasti.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="4fc2a-149">Objekti komponendi välja vahetamisel pääsete hetke hooldusleppele seadistatud hooldusobjekti seost kasutades ligi koosluse koostajale.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="4fc2a-150">Ligipääs koosluse koostajale hooldusobjekti seost kasutades</span><span class="sxs-lookup"><span data-stu-id="4fc2a-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="4fc2a-151">Hoolduslepped</span><span class="sxs-lookup"><span data-stu-id="4fc2a-151">Service agreements</span></span>
2. <span data-ttu-id="4fc2a-152">Topeltklõpsake hoolduslepet või klõpsake valikut Hoolduslepe, et luua uus hoolduslepe.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="4fc2a-153">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="4fc2a-154">Teenusleppele mallkoosluse lisamiseks klõpsake valikut Hooldusobjektid.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="4fc2a-155">Vormis Hooldusobjektid klõpsake valikut Kujundamine vormi Kujundamine avamiseks, et muuta mallkooslust.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="4fc2a-156">Automaatselt loodud hooldustellimused</span><span class="sxs-lookup"><span data-stu-id="4fc2a-156">Automatically created service orders</span></span>

<span data-ttu-id="4fc2a-157">Hooldusleppele automaatselt hooldustellimuste loomisel liiguvad ka lepete hooldusobjekti seosed loodud hooldustellimustesse.</span><span class="sxs-lookup"><span data-stu-id="4fc2a-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

