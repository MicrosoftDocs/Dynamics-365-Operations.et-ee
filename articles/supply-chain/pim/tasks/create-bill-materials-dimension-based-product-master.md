---
title: Dimensioonipõhise tooteetaloni jaoks koosluse loomine
description: Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920701"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="da263-103">Dimensioonipõhise tooteetaloni jaoks koosluse loomine</span><span class="sxs-lookup"><span data-stu-id="da263-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da263-104">Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras.</span><span class="sxs-lookup"><span data-stu-id="da263-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="da263-105">Esimesed 4 salvestust seadistavad andmed, mida on selle protseduuri lõpuleviimiseks vaja.</span><span class="sxs-lookup"><span data-stu-id="da263-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="da263-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="da263-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="da263-107">Seda ülesannet täidab tavaliselt toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="da263-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="da263-108">Toote valimine</span><span class="sxs-lookup"><span data-stu-id="da263-108">Select the product</span></span>

1. <span data-ttu-id="da263-109">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="da263-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="da263-110">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da263-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="da263-111">Otsige üles väljastatud tooteetalon koos dimensioonipõhise konfiguratsiooni tehnoloogiaga, mille lõite esimese ülesande juhendis selles järjekorras.</span><span class="sxs-lookup"><span data-stu-id="da263-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="da263-112">Valige tegevuste paanil käsk **Insener**.</span><span class="sxs-lookup"><span data-stu-id="da263-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="da263-113">Valige suvand **Koosluse versioonid**.</span><span class="sxs-lookup"><span data-stu-id="da263-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="da263-114">Uue koosluse ja koosluse versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="da263-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="da263-115">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da263-115">Select **New**.</span></span>
1. <span data-ttu-id="da263-116">Valige **kooslus ja koosluse versioon**.</span><span class="sxs-lookup"><span data-stu-id="da263-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="da263-117">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="da263-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="da263-118">Tegevuskoha seadistamine</span><span class="sxs-lookup"><span data-stu-id="da263-118">Setting a site</span></span>  
    * <span data-ttu-id="da263-119">Selles protseduuris ei määrata kooslusele konkreetset tegevuskohta.</span><span class="sxs-lookup"><span data-stu-id="da263-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="da263-120">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="da263-120">Select **OK**.</span></span>
1. <span data-ttu-id="da263-121">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da263-121">Select **New**.</span></span>
    * <span data-ttu-id="da263-122">Selles protseduuris lisame kooslusele neli rida.</span><span class="sxs-lookup"><span data-stu-id="da263-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="da263-123">Kaks rida tähistavad kaabli suvandeid ja kaks rida tähistavad kartoteegi suvandeid.</span><span class="sxs-lookup"><span data-stu-id="da263-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="da263-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da263-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="da263-125">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="da263-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="da263-126">Valige kauba number A0001, HDMI 6' kaablid.</span><span class="sxs-lookup"><span data-stu-id="da263-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="da263-127">Sisestage või valige väärtus väljal **Konfiguratsioonigrupp**.</span><span class="sxs-lookup"><span data-stu-id="da263-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="da263-128">Valige kaabli konfiguratsioonigrupp, mis loodi juhendis 4 selles järjekorras.</span><span class="sxs-lookup"><span data-stu-id="da263-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="da263-129">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da263-129">Select **New**.</span></span>
    * <span data-ttu-id="da263-130">Valige kauba number A0002, HDMI 12' kaablid.</span><span class="sxs-lookup"><span data-stu-id="da263-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="da263-131">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da263-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="da263-132">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="da263-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="da263-133">Sisestage või valige väärtus väljal **Konfiguratsioonigrupp**.</span><span class="sxs-lookup"><span data-stu-id="da263-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="da263-134">Valige uuesti kaabli konfiguratsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="da263-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="da263-135">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da263-135">Select **New**.</span></span>
1. <span data-ttu-id="da263-136">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da263-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="da263-137">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="da263-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="da263-138">Valige kauba number D0002 kartoteek.</span><span class="sxs-lookup"><span data-stu-id="da263-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="da263-139">Sisestage või valige väärtus väljal **Konfiguratsioonigrupp**.</span><span class="sxs-lookup"><span data-stu-id="da263-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="da263-140">Valige kartoteegi konfiguratsioonigrupp sellele koosluse reale.</span><span class="sxs-lookup"><span data-stu-id="da263-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="da263-141">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da263-141">Select **New**.</span></span>
1. <span data-ttu-id="da263-142">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da263-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="da263-143">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="da263-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="da263-144">Valige kauba number M0007 StandardCabinet viimase koosluse reana.</span><span class="sxs-lookup"><span data-stu-id="da263-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="da263-145">Sisestage või valige väärtus väljal **Konfiguratsioonigrupp**.</span><span class="sxs-lookup"><span data-stu-id="da263-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="da263-146">Valige kartoteegi konfiguratsioonigrupp viimasele koosluse reale.</span><span class="sxs-lookup"><span data-stu-id="da263-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="da263-147">Kinnita ja aktiveeri</span><span class="sxs-lookup"><span data-stu-id="da263-147">Approve and activate</span></span>

1. <span data-ttu-id="da263-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da263-148">Close the page.</span></span>
1. <span data-ttu-id="da263-149">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="da263-149">Select **Approve**.</span></span>
1. <span data-ttu-id="da263-150">Valige või sisestage väärtus väljal **Kinnitaja**.</span><span class="sxs-lookup"><span data-stu-id="da263-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="da263-151">Valige *Jah* väljal **Kas soovite ka koosluse kinnitada?**.</span><span class="sxs-lookup"><span data-stu-id="da263-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="da263-152">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="da263-152">Select **OK**.</span></span>
1. <span data-ttu-id="da263-153">Valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="da263-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]