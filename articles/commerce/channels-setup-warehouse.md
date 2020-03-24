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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113755"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="7d4b1-103">Lao seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d4b1-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7d4b1-104">Selles teemas kirjeldatakse lao seadistamist, mida kasutatakse uue kanaliga Microsoft Dynamics 365 Commerce'is.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d4b1-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="7d4b1-105">Overview</span></span>

<span data-ttu-id="7d4b1-106">Iga ärikanal nõuab, et sellega oleks seotud konfigureeritud ladu.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="7d4b1-107">Järgmised protseduurid annavad minimaalse konfiguratsiooni, mis on vajalik ärikanalile lao seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="7d4b1-108">Lisainfot lao seadistamise kohta vaadake jaotisest [Laohalduse ülevaade](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7d4b1-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="7d4b1-109">Laoala konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7d4b1-109">Configure a warehouse site</span></span>

<span data-ttu-id="7d4b1-110">Enne lao seadistamist peate konfigureerima laoala.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="7d4b1-111">Laoala konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="7d4b1-112">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Saidid**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="7d4b1-113">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d4b1-114">Sisestage väärtus väljale **Sait**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="7d4b1-115">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7d4b1-116">Määrake jaotises **Üldine** sobiv **Ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="7d4b1-117">Sisestage aadress väljale **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="7d4b1-118">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d4b1-119">Järgmine pilt näitab laoala näidet.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-119">The following image shows an example warehouse site.</span></span>

![Laoala näide](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="7d4b1-121">Lao seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d4b1-121">Set up a warehouse</span></span>

<span data-ttu-id="7d4b1-122">Lao seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="7d4b1-123">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="7d4b1-124">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d4b1-125">Sisestage väärtus väljale **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="7d4b1-126">Kui see on 1:1 vastendamine poega, kaaluge poe nime või piirkondliku jaotuskeskuse nime kasutamist.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="7d4b1-127">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7d4b1-128">Valige ripploendist **Sait** eelnevalt loodud laoala.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="7d4b1-129">Valige väljal **Tüüp** väärtus **Vaikimisi**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="7d4b1-130">Kui soovite seadistada **Vahelao**, peate esmalt järgima neid samme, et luua täiendav ladu, kus **Tüüp** on seadistatud väärtusele **Vaheladu**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="7d4b1-131">Kui soovite seadistada **Transiitlao**, peate esmalt järgima neid samme, et luua täiendav ladu, kus **Tüüp** on seadistatud väärtusele **Transiit**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="7d4b1-132">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="7d4b1-133">Saate häälestada lao riiuliridu.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-133">Set up inventory aisles</span></span>

<span data-ttu-id="7d4b1-134">Riiuliridade seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="7d4b1-135">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Asukoha seadistus \> Riiuliread**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="7d4b1-136">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d4b1-137">Valige ripploendist **Ladu** eelnevalt loodud ladu.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="7d4b1-138">Sisestage väljale **Riiulirida** nimi (nt "Vaik").</span><span class="sxs-lookup"><span data-stu-id="7d4b1-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="7d4b1-139">Sisestage väljale **Nimi** nimi (nt "Vaikimisi riiulirida").</span><span class="sxs-lookup"><span data-stu-id="7d4b1-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="7d4b1-140">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="7d4b1-141">Lao varude asukohtade häälestamine</span><span class="sxs-lookup"><span data-stu-id="7d4b1-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="7d4b1-142">Standardsete, kahjustatud ja tagastatud lao varude asukohtade seadistamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="7d4b1-143">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="7d4b1-144">Valige varem loodud ladu.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="7d4b1-145">Valige tegevuspaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="7d4b1-146">Valige tegevuspaanilt **Ladu**ja seejärel valige **Varude asukoht**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="7d4b1-147">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-147">On the action pane, select **New**.</span></span> <span data-ttu-id="7d4b1-148">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="7d4b1-149">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="7d4b1-150">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="7d4b1-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="7d4b1-151">Sisestage lao nimi kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="7d4b1-152">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="7d4b1-153">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="7d4b1-154">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="7d4b1-155">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="7d4b1-156">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="7d4b1-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="7d4b1-157">Sisestage "Kahjustatud" kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="7d4b1-158">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="7d4b1-159">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="7d4b1-160">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="7d4b1-161">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="7d4b1-162">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="7d4b1-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="7d4b1-163">Sisestage "Tagastused" kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="7d4b1-164">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="7d4b1-165">Järgmine pilt näitab San Francisco lao varude asukoha seadistust.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Varude asukoha seadistuse näide](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="7d4b1-167">Lao seadistamise lõpetamine</span><span class="sxs-lookup"><span data-stu-id="7d4b1-167">Complete warehouse setup</span></span>

<span data-ttu-id="7d4b1-168">Lao seadistamise lõpetamiseks järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="7d4b1-169">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="7d4b1-170">Valige varem loodud ladu.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="7d4b1-171">Valige tegevuspaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="7d4b1-172">Jaotises **Varude ja laohaldus**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="7d4b1-173">Seadistage **Vaikimisi vastuvõtu asukoht** eespool loodud asukohale.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="7d4b1-174">Valige **Vaikimisi väljastamise asukoht** eespool loodud asukohale.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="7d4b1-175">Sisestage lao aadress jaotisesse **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="7d4b1-176">Jaotises **Jaemüük**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="7d4b1-177">Sisestage kasti **Vaikimisi tagastuste asukoht** eelnevalt loodud tagastuste asukoht.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="7d4b1-178">Sea **Kauplus** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="7d4b1-179">Seadistage **Kaal** väärtusele **1.00**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="7d4b1-180">Sisestage kasti **Laoala dimensioonid** eelnevalt loodud vaikimisi asukoht.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="7d4b1-181">Seadistage jaotises **Ladu** **Füüsilise negatiivse laovaru** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="7d4b1-182">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d4b1-183">Järgmine pilt näitab konfigureeritud lao üksikasju.</span><span class="sxs-lookup"><span data-stu-id="7d4b1-183">The following image shows details for a configured warehouse.</span></span>

![Konfigureeritud lao näide](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="7d4b1-185">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7d4b1-185">Additional resources</span></span>

[<span data-ttu-id="7d4b1-186">Laohalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="7d4b1-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7d4b1-187">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="7d4b1-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7d4b1-188">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="7d4b1-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7d4b1-189">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d4b1-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="7d4b1-190">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="7d4b1-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7d4b1-191">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d4b1-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





