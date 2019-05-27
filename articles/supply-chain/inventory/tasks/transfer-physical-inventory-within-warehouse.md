---
title: Füüsiliste laovarude ülekandmine laos
description: See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b3e91be8aeab10188b6d3925d44a9ec1106406
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554180"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="e44f8-103">Füüsiliste laovarude ülekandmine laos</span><span class="sxs-lookup"><span data-stu-id="e44f8-103">Transfer physical inventory within the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e44f8-104">See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise.</span><span class="sxs-lookup"><span data-stu-id="e44f8-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="e44f8-105">Enne selle käivitamist peate seadistama varude üleviimiste jaoks varude töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="e44f8-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="e44f8-106">Saate läbida selle protseduuri demoettevõtte USMF andmete põhjal, kasutades kuvatavaid näidisväärtusi, või võite kasutada oma andmeid, kui teil on tooted ja asukohad seadistatud.</span><span class="sxs-lookup"><span data-stu-id="e44f8-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="e44f8-107">Neid ülesandeid täidab üldjuhul laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="e44f8-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="e44f8-108">Lao üleviimistöölehe loomine</span><span class="sxs-lookup"><span data-stu-id="e44f8-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="e44f8-109">Minge jaotisse Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="e44f8-109">Go to Transfer.</span></span>
2. <span data-ttu-id="e44f8-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e44f8-110">Click New.</span></span>
3. <span data-ttu-id="e44f8-111">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="e44f8-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="e44f8-112">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e44f8-112">Click OK.</span></span>
    * <span data-ttu-id="e44f8-113">Määrata saab iga töölehe dimensioonid Alates ja Kuni.</span><span class="sxs-lookup"><span data-stu-id="e44f8-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="e44f8-114">Need on selle töölehe tüübi puhul olulised.</span><span class="sxs-lookup"><span data-stu-id="e44f8-114">These are essential for this journal type.</span></span> <span data-ttu-id="e44f8-115">Saate viia kaupu asukohtadesse üle, kasutades mitmesuguseid reegleid.</span><span class="sxs-lookup"><span data-stu-id="e44f8-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="e44f8-116">Selles näites viime kauba üle samas laos, litsentsiplaadiga kontrollitavast asukohast asukohta, mida litsentsiplaadiga ei kontrollita.</span><span class="sxs-lookup"><span data-stu-id="e44f8-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="e44f8-117">Tööleheridade loomine</span><span class="sxs-lookup"><span data-stu-id="e44f8-117">Create journal lines</span></span>
1. <span data-ttu-id="e44f8-118">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e44f8-118">Click New.</span></span>
2. <span data-ttu-id="e44f8-119">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="e44f8-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e44f8-120">Kui kasutate USMF-i, võite valida väärtuse A0001.</span><span class="sxs-lookup"><span data-stu-id="e44f8-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="e44f8-121">Sisestage või valige väärtus väljal Lähtekoht.</span><span class="sxs-lookup"><span data-stu-id="e44f8-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="e44f8-122">Kui kasutate USMF-i, võite valida väärtuse 2.</span><span class="sxs-lookup"><span data-stu-id="e44f8-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="e44f8-123">Sisestage või valige väärtus väljal Sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="e44f8-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="e44f8-124">Kui kasutate USMF-i, võite valida väärtuse 2.</span><span class="sxs-lookup"><span data-stu-id="e44f8-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="e44f8-125">Sisestage või valige väärtus väljal Laost.</span><span class="sxs-lookup"><span data-stu-id="e44f8-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="e44f8-126">Kui kasutate USMF-i, võite valida väärtuse 24.</span><span class="sxs-lookup"><span data-stu-id="e44f8-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="e44f8-127">Sisestage või valige väärtus väljal Lattu.</span><span class="sxs-lookup"><span data-stu-id="e44f8-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="e44f8-128">Kui kasutate USMF-i, võite valida väärtuse 24.</span><span class="sxs-lookup"><span data-stu-id="e44f8-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="e44f8-129">Sisestage või valige väärtus väljal Lähteasukoht.</span><span class="sxs-lookup"><span data-stu-id="e44f8-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="e44f8-130">Kui kasutate USMF-i, võite valida väärtuse FL-001.</span><span class="sxs-lookup"><span data-stu-id="e44f8-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="e44f8-131">Sisestage või valige väärtus väljal Sihtasukoht.</span><span class="sxs-lookup"><span data-stu-id="e44f8-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="e44f8-132">Kui kasutate USMF-i, võite valida väärtuse BULK-001.</span><span class="sxs-lookup"><span data-stu-id="e44f8-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="e44f8-133">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="e44f8-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="e44f8-134">Klõpsake vahekaarti Varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="e44f8-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="e44f8-135">Valige või sisestage väärtus väljal Litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="e44f8-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="e44f8-136">Kui kasutate USMF-i, võite valida väärtuse 24.</span><span class="sxs-lookup"><span data-stu-id="e44f8-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="e44f8-137">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e44f8-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="e44f8-138">Lao üleviimistöölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="e44f8-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="e44f8-139">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="e44f8-139">Click Post.</span></span>
2. <span data-ttu-id="e44f8-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e44f8-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="e44f8-141">Varude kannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="e44f8-141">View inventory transactions</span></span>
1. <span data-ttu-id="e44f8-142">Klõpsake Ladu.</span><span class="sxs-lookup"><span data-stu-id="e44f8-142">Click Inventory.</span></span>
2. <span data-ttu-id="e44f8-143">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="e44f8-143">Click Transactions.</span></span>
    * <span data-ttu-id="e44f8-144">Siin näete kandeid, mis loodi, kui oma töölehe sisestasite.</span><span class="sxs-lookup"><span data-stu-id="e44f8-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

