---
title: Lao seadistamine
description: Selles teemas kirjeldatakse lao seadistamist, mida kasutatakse uue kanaliga Microsoft Dynamics 365 Commerce'is.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993649"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="539f7-103">Lao seadistamine</span><span class="sxs-lookup"><span data-stu-id="539f7-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="539f7-104">Selles teemas kirjeldatakse lao seadistamist, mida kasutatakse uue kanaliga Microsoft Dynamics 365 Commerce'is.</span><span class="sxs-lookup"><span data-stu-id="539f7-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="539f7-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="539f7-105">Overview</span></span>

<span data-ttu-id="539f7-106">Iga ärikanal nõuab, et sellega oleks seotud konfigureeritud ladu.</span><span class="sxs-lookup"><span data-stu-id="539f7-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="539f7-107">Järgmised protseduurid annavad minimaalse konfiguratsiooni, mis on vajalik ärikanalile lao seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="539f7-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="539f7-108">Lisainfot lao seadistamise kohta vaadake jaotisest [Laohalduse ülevaade](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="539f7-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="539f7-109">Laoala konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="539f7-109">Configure a warehouse site</span></span>

<span data-ttu-id="539f7-110">Enne lao seadistamist peate konfigureerima laoala.</span><span class="sxs-lookup"><span data-stu-id="539f7-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="539f7-111">Laoala konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="539f7-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="539f7-112">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Saidid**.</span><span class="sxs-lookup"><span data-stu-id="539f7-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="539f7-113">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="539f7-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="539f7-114">Sisestage väärtus väljale **Sait**.</span><span class="sxs-lookup"><span data-stu-id="539f7-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="539f7-115">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="539f7-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="539f7-116">Määrake jaotises **Üldine** sobiv **Ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="539f7-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="539f7-117">Sisestage aadress väljale **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="539f7-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="539f7-118">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="539f7-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="539f7-119">Järgmine pilt näitab laoala näidet.</span><span class="sxs-lookup"><span data-stu-id="539f7-119">The following image shows an example warehouse site.</span></span>

![Laoala näide](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="539f7-121">Lao seadistamine</span><span class="sxs-lookup"><span data-stu-id="539f7-121">Set up a warehouse</span></span>

<span data-ttu-id="539f7-122">Lao seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="539f7-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="539f7-123">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="539f7-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="539f7-124">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="539f7-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="539f7-125">Sisestage väärtus väljale **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="539f7-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="539f7-126">Kui see on 1:1 vastendamine poega, kaaluge poe nime või piirkondliku jaotuskeskuse nime kasutamist.</span><span class="sxs-lookup"><span data-stu-id="539f7-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="539f7-127">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="539f7-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="539f7-128">Valige ripploendist **Sait** eelnevalt loodud laoala.</span><span class="sxs-lookup"><span data-stu-id="539f7-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="539f7-129">Valige väljal **Tüüp** väärtus **Vaikimisi**.</span><span class="sxs-lookup"><span data-stu-id="539f7-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="539f7-130">Kui soovite seadistada **Vahelao**, peate esmalt järgima neid samme, et luua täiendav ladu, kus **Tüüp** on seadistatud väärtusele **Vaheladu**.</span><span class="sxs-lookup"><span data-stu-id="539f7-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="539f7-131">Kui soovite seadistada **Transiitlao**, peate esmalt järgima neid samme, et luua täiendav ladu, kus **Tüüp** on seadistatud väärtusele **Transiit**.</span><span class="sxs-lookup"><span data-stu-id="539f7-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="539f7-132">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="539f7-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="539f7-133">Saate häälestada lao riiuliridu.</span><span class="sxs-lookup"><span data-stu-id="539f7-133">Set up inventory aisles</span></span>

<span data-ttu-id="539f7-134">Riiuliridade seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="539f7-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="539f7-135">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Asukoha seadistus \> Riiuliread**.</span><span class="sxs-lookup"><span data-stu-id="539f7-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="539f7-136">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="539f7-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="539f7-137">Valige ripploendist **Ladu** eelnevalt loodud ladu.</span><span class="sxs-lookup"><span data-stu-id="539f7-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="539f7-138">Sisestage väljale **Riiulirida** nimi (nt "Vaik").</span><span class="sxs-lookup"><span data-stu-id="539f7-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="539f7-139">Sisestage väljale **Nimi** nimi (nt "Vaikimisi riiulirida").</span><span class="sxs-lookup"><span data-stu-id="539f7-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="539f7-140">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="539f7-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="539f7-141">Lao varude asukohtade häälestamine</span><span class="sxs-lookup"><span data-stu-id="539f7-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="539f7-142">Standardsete, kahjustatud ja tagastatud lao varude asukohtade seadistamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="539f7-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="539f7-143">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="539f7-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="539f7-144">Valige varem loodud ladu.</span><span class="sxs-lookup"><span data-stu-id="539f7-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="539f7-145">Valige tegevuspaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="539f7-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="539f7-146">Valige tegevuspaanilt **Ladu** ja seejärel valige **Varude asukoht**.</span><span class="sxs-lookup"><span data-stu-id="539f7-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="539f7-147">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="539f7-147">On the action pane, select **New**.</span></span> <span data-ttu-id="539f7-148">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="539f7-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="539f7-149">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="539f7-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="539f7-150">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="539f7-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="539f7-151">Sisestage lao nimi kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="539f7-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="539f7-152">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="539f7-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="539f7-153">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="539f7-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="539f7-154">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="539f7-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="539f7-155">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="539f7-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="539f7-156">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="539f7-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="539f7-157">Sisestage "Kahjustatud" kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="539f7-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="539f7-158">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="539f7-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="539f7-159">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="539f7-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="539f7-160">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="539f7-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="539f7-161">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="539f7-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="539f7-162">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="539f7-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="539f7-163">Sisestage "Tagastused" kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="539f7-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="539f7-164">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="539f7-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="539f7-165">Järgmine pilt näitab San Francisco lao varude asukoha seadistust.</span><span class="sxs-lookup"><span data-stu-id="539f7-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Varude asukoha seadistuse näide](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="539f7-167">Lao seadistamise lõpetamine</span><span class="sxs-lookup"><span data-stu-id="539f7-167">Complete warehouse setup</span></span>

<span data-ttu-id="539f7-168">Lao seadistamise lõpetamiseks järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="539f7-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="539f7-169">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="539f7-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="539f7-170">Valige varem loodud ladu.</span><span class="sxs-lookup"><span data-stu-id="539f7-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="539f7-171">Valige tegevuspaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="539f7-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="539f7-172">Jaotises **Varude ja laohaldus**.</span><span class="sxs-lookup"><span data-stu-id="539f7-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="539f7-173">Seadistage **Vaikimisi vastuvõtu asukoht** eespool loodud asukohale.</span><span class="sxs-lookup"><span data-stu-id="539f7-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="539f7-174">Valige **Vaikimisi väljastamise asukoht** eespool loodud asukohale.</span><span class="sxs-lookup"><span data-stu-id="539f7-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="539f7-175">Sisestage lao aadress jaotisesse **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="539f7-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="539f7-176">Jaotises **Jaemüük**.</span><span class="sxs-lookup"><span data-stu-id="539f7-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="539f7-177">Sisestage kasti **Vaikimisi tagastuste asukoht** eelnevalt loodud tagastuste asukoht.</span><span class="sxs-lookup"><span data-stu-id="539f7-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="539f7-178">Sea **Kauplus** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="539f7-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="539f7-179">Seadistage **Kaal** väärtusele **1.00**.</span><span class="sxs-lookup"><span data-stu-id="539f7-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="539f7-180">Sisestage kasti **Laoala dimensioonid** eelnevalt loodud vaikimisi asukoht.</span><span class="sxs-lookup"><span data-stu-id="539f7-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="539f7-181">Seadistage jaotises **Ladu** **Füüsilise negatiivse laovaru** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="539f7-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="539f7-182">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="539f7-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="539f7-183">Järgmine pilt näitab konfigureeritud lao üksikasju.</span><span class="sxs-lookup"><span data-stu-id="539f7-183">The following image shows details for a configured warehouse.</span></span>

![Konfigureeritud lao näide](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="539f7-185">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="539f7-185">Additional resources</span></span>

[<span data-ttu-id="539f7-186">Laohalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="539f7-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="539f7-187">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="539f7-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="539f7-188">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="539f7-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="539f7-189">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="539f7-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="539f7-190">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="539f7-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="539f7-191">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="539f7-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





