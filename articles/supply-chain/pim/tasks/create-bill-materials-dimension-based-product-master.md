---
title: Dimensioonipõhise tooteetaloni jaoks koosluse loomine
description: Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 799479c4b4cdf5b61b1f55a61454823558b9013b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237420"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="54d26-103">Dimensioonipõhise tooteetaloni jaoks koosluse loomine</span><span class="sxs-lookup"><span data-stu-id="54d26-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54d26-104">Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras.</span><span class="sxs-lookup"><span data-stu-id="54d26-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="54d26-105">Esimesed 4 salvestust seadistavad andmed, mida on selle protseduuri lõpuleviimiseks vaja.</span><span class="sxs-lookup"><span data-stu-id="54d26-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="54d26-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="54d26-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="54d26-107">Seda ülesannet täidab tavaliselt toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="54d26-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="54d26-108">Toote valimine</span><span class="sxs-lookup"><span data-stu-id="54d26-108">Select the product</span></span>
1. <span data-ttu-id="54d26-109">Klõpsake valikut Väljastatud toodete hooldus.</span><span class="sxs-lookup"><span data-stu-id="54d26-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="54d26-110">Klõpsake valikut Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="54d26-110">Click Released products.</span></span>
3. <span data-ttu-id="54d26-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="54d26-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="54d26-112">Otsige üles väljastatud tooteetalon koos dimensioonipõhise konfiguratsiooni tehnoloogiaga, mille lõite esimese ülesande juhendis selles järjekorras.</span><span class="sxs-lookup"><span data-stu-id="54d26-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="54d26-113">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="54d26-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="54d26-114">Klõpsake koosluse versioone.</span><span class="sxs-lookup"><span data-stu-id="54d26-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="54d26-115">Uue koosluse ja koosluse versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="54d26-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="54d26-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="54d26-116">Click New.</span></span>
2. <span data-ttu-id="54d26-117">Klõpsake kooslust ja koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="54d26-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="54d26-118">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="54d26-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="54d26-119">Tegevuskoha seadistamine</span><span class="sxs-lookup"><span data-stu-id="54d26-119">Setting a site</span></span>  
    * <span data-ttu-id="54d26-120">Selles protseduuris ei määrata kooslusele konkreetset tegevuskohta.</span><span class="sxs-lookup"><span data-stu-id="54d26-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="54d26-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="54d26-121">Click OK.</span></span>
5. <span data-ttu-id="54d26-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="54d26-122">Click New.</span></span>
    * <span data-ttu-id="54d26-123">Selles protseduuris lisame kooslusele neli rida.</span><span class="sxs-lookup"><span data-stu-id="54d26-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="54d26-124">Kaks rida tähistavad kaabli suvandeid ja kaks rida tähistavad kartoteegi suvandeid.</span><span class="sxs-lookup"><span data-stu-id="54d26-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="54d26-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="54d26-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="54d26-126">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="54d26-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="54d26-127">Valige kauba number A0001, HDMI 6' kaablid.</span><span class="sxs-lookup"><span data-stu-id="54d26-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="54d26-128">Sisestage või valige väärtus väljal Konfiguratsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="54d26-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="54d26-129">Valige kaabli konfiguratsioonigrupp, mis loodi juhendis 4 selles järjekorras.</span><span class="sxs-lookup"><span data-stu-id="54d26-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="54d26-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="54d26-130">Click New.</span></span>
    * <span data-ttu-id="54d26-131">Valige kauba number A0002, HDMI 12' kaablid.</span><span class="sxs-lookup"><span data-stu-id="54d26-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="54d26-132">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="54d26-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="54d26-133">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="54d26-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="54d26-134">Sisestage või valige väärtus väljal Konfiguratsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="54d26-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="54d26-135">Valige uuesti kaabli konfiguratsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="54d26-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="54d26-136">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="54d26-136">Click New.</span></span>
14. <span data-ttu-id="54d26-137">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="54d26-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="54d26-138">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="54d26-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="54d26-139">Valige kauba number D0002 kartoteek.</span><span class="sxs-lookup"><span data-stu-id="54d26-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="54d26-140">Sisestage või valige väärtus väljal Konfiguratsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="54d26-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="54d26-141">Valige kartoteegi konfiguratsioonigrupp sellele koosluse reale.</span><span class="sxs-lookup"><span data-stu-id="54d26-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="54d26-142">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="54d26-142">Click New.</span></span>
18. <span data-ttu-id="54d26-143">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="54d26-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="54d26-144">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="54d26-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="54d26-145">Valige kauba number M0007 StandardCabinet viimase koosluse reana.</span><span class="sxs-lookup"><span data-stu-id="54d26-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="54d26-146">Sisestage või valige väärtus väljal Konfiguratsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="54d26-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="54d26-147">Valige kartoteegi konfiguratsioonigrupp viimasele koosluse reale.</span><span class="sxs-lookup"><span data-stu-id="54d26-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="54d26-148">Kinnita ja aktiveeri</span><span class="sxs-lookup"><span data-stu-id="54d26-148">Approve and activate</span></span>
1. <span data-ttu-id="54d26-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="54d26-149">Close the page.</span></span>
2. <span data-ttu-id="54d26-150">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="54d26-150">Click Approve.</span></span>
3. <span data-ttu-id="54d26-151">Valige või sisestage väärtus väljal Kinnitaja.</span><span class="sxs-lookup"><span data-stu-id="54d26-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="54d26-152">Valige Jah väljal Kas soovite ka koosluse kinnitada?</span><span class="sxs-lookup"><span data-stu-id="54d26-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="54d26-153">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="54d26-153">Click OK.</span></span>
6. <span data-ttu-id="54d26-154">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="54d26-154">Click Activate.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]