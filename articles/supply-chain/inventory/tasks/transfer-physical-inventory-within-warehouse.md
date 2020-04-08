---
title: Füüsiliste laovarude ülekandmine laos
description: See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 899701413814ce38a4367618ed72d1039eca0bf8
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148166"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="e60a3-103">Füüsiliste laovarude ülekandmine laos</span><span class="sxs-lookup"><span data-stu-id="e60a3-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e60a3-104">See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise.</span><span class="sxs-lookup"><span data-stu-id="e60a3-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="e60a3-105">Enne selle käivitamist peate seadistama varude üleviimiste jaoks varude töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="e60a3-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="e60a3-106">Saate läbida selle protseduuri demoettevõtte USMF andmete põhjal, kasutades kuvatavaid näidisväärtusi, või võite kasutada oma andmeid, kui teil on tooted ja asukohad seadistatud.</span><span class="sxs-lookup"><span data-stu-id="e60a3-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="e60a3-107">Neid ülesandeid täidab üldjuhul laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="e60a3-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="e60a3-108">Lao üleviimistöölehe loomine</span><span class="sxs-lookup"><span data-stu-id="e60a3-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="e60a3-109">Avage **Navigeerimispaneelil** **Varuhaldus > Töölehe kanded > Kaubad > Edastus**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="e60a3-110">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-110">Click **New**.</span></span>
3. <span data-ttu-id="e60a3-111">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="e60a3-112">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-112">Click **OK**.</span></span> <span data-ttu-id="e60a3-113">Määrata saab iga töölehe dimensioonid Alates ja Kuni.</span><span class="sxs-lookup"><span data-stu-id="e60a3-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="e60a3-114">Need on selle töölehe tüübi puhul olulised.</span><span class="sxs-lookup"><span data-stu-id="e60a3-114">These are essential for this journal type.</span></span> <span data-ttu-id="e60a3-115">Saate viia kaupu asukohtadesse üle, kasutades mitmesuguseid reegleid.</span><span class="sxs-lookup"><span data-stu-id="e60a3-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="e60a3-116">Selles näites viime kauba üle samas laos, litsentsiplaadiga kontrollitavast asukohast asukohta, mida litsentsiplaadiga ei kontrollita.</span><span class="sxs-lookup"><span data-stu-id="e60a3-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="e60a3-117">Loo töölehe read</span><span class="sxs-lookup"><span data-stu-id="e60a3-117">Create journal lines</span></span>
1. <span data-ttu-id="e60a3-118">Klõpsake kaardil **Töölehe read fastTab** **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="e60a3-119">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="e60a3-120">Kui kasutate USMF-i, võite valida väärtuse A0001.</span><span class="sxs-lookup"><span data-stu-id="e60a3-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="e60a3-121">Sisestage välja **Saidist** väärtus või valige see.</span><span class="sxs-lookup"><span data-stu-id="e60a3-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="e60a3-122">Kui kasutate USMF-i, võite valida väärtuse 2.</span><span class="sxs-lookup"><span data-stu-id="e60a3-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="e60a3-123">Sisestage välja **Saidile** väärtus või valige see.</span><span class="sxs-lookup"><span data-stu-id="e60a3-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="e60a3-124">Kui kasutate USMF-i, võite valida väärtuse 2.</span><span class="sxs-lookup"><span data-stu-id="e60a3-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="e60a3-125">Sisestage välja **Laost** väärtus või valige see.</span><span class="sxs-lookup"><span data-stu-id="e60a3-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="e60a3-126">Kui kasutate USMF-i, võite valida väärtuse 24.</span><span class="sxs-lookup"><span data-stu-id="e60a3-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="e60a3-127">Sisestage välja **Lattu** väärtus või valige see.</span><span class="sxs-lookup"><span data-stu-id="e60a3-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="e60a3-128">Kui kasutate USMF-i, võite valida väärtuse 24.</span><span class="sxs-lookup"><span data-stu-id="e60a3-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="e60a3-129">Sisestage välja **Asukohast** väärtus või valige see.</span><span class="sxs-lookup"><span data-stu-id="e60a3-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="e60a3-130">Kui kasutate USMF-i, võite valida väärtuse FL-001.</span><span class="sxs-lookup"><span data-stu-id="e60a3-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="e60a3-131">Sisestage välja **Asukohta** väärtus või valige see.</span><span class="sxs-lookup"><span data-stu-id="e60a3-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="e60a3-132">Kui kasutate USMF-i, võite valida väärtuse BULK-001.</span><span class="sxs-lookup"><span data-stu-id="e60a3-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="e60a3-133">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="e60a3-134">Klõpsake kiirkaardil **Rea üksikasjad** vahekaarti **Varude dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="e60a3-135">Sisestage **Varude dimensioonides** välja **Identifitseerimisnumber** väärtus või valige see.</span><span class="sxs-lookup"><span data-stu-id="e60a3-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="e60a3-136">Kui kasutate USMF-i, võite valida väärtuse 24.</span><span class="sxs-lookup"><span data-stu-id="e60a3-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="e60a3-137">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="e60a3-138">Lao üleviimistöölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="e60a3-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="e60a3-139">Paanil **Toimingupaan** klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-139">On the **Action pane**, click **Post**.</span></span>
2. <span data-ttu-id="e60a3-140">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="e60a3-141">Varude kannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="e60a3-141">View inventory transactions</span></span>
1. <span data-ttu-id="e60a3-142">Klõpsake **Varu**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="e60a3-143">Klõpsake **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="e60a3-143">Click **Transactions**.</span></span> <span data-ttu-id="e60a3-144">Siin näete kandeid, mis loodi, kui oma töölehe sisestasite.</span><span class="sxs-lookup"><span data-stu-id="e60a3-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

