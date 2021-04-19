---
title: Lao seadistamine
description: Selles teemas kirjeldatakse lao seadistamist, mida kasutatakse uue kanaliga Microsoft Dynamics 365 Commerce'is.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800491"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="1c1ab-103">Lao seadistamine</span><span class="sxs-lookup"><span data-stu-id="1c1ab-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c1ab-104">Selles teemas kirjeldatakse lao seadistamist, mida kasutatakse uue kanaliga Microsoft Dynamics 365 Commerce'is.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1c1ab-105">Iga ärikanal nõuab, et sellega oleks seotud konfigureeritud ladu.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="1c1ab-106">Järgmised protseduurid annavad minimaalse konfiguratsiooni, mis on vajalik ärikanalile lao seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="1c1ab-107">Lisainfot lao seadistamise kohta vaadake jaotisest [Laohalduse ülevaade](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="1c1ab-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="1c1ab-108">Laoala konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1c1ab-108">Configure a warehouse site</span></span>

<span data-ttu-id="1c1ab-109">Enne lao seadistamist peate konfigureerima laoala.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="1c1ab-110">Laoala konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="1c1ab-111">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Saidid**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="1c1ab-112">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1c1ab-113">Sisestage väärtus väljale **Sait**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="1c1ab-114">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="1c1ab-115">Määrake jaotises **Üldine** sobiv **Ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="1c1ab-116">Sisestage aadress väljale **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="1c1ab-117">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1c1ab-118">Järgmine pilt näitab laoala näidet.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-118">The following image shows an example warehouse site.</span></span>

![Laoala näide](media/warehouse-site.png)

## <a name="set-up-a-warehouse&quot;></a><span data-ttu-id=&quot;1c1ab-120&quot;>Lao seadistamine</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-120&quot;>Set up a warehouse</span></span>

<span data-ttu-id=&quot;1c1ab-121&quot;>Lao seadistamiseks toimige järgmiselt.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-121&quot;>To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id=&quot;1c1ab-122&quot;>Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-122&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id=&quot;1c1ab-123&quot;>Valige toimingupaanil nupp **Uus**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-123&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;1c1ab-124&quot;>Sisestage väärtus väljale **Ladu**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-124&quot;>In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id=&quot;1c1ab-125&quot;>Kui see on 1:1 vastendamine poega, kaaluge poe nime või piirkondliku jaotuskeskuse nime kasutamist.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-125&quot;>If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id=&quot;1c1ab-126&quot;>Sisestage väärtus väljale **Nimi**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-126&quot;>In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id=&quot;1c1ab-127&quot;>Valige ripploendist **Sait** eelnevalt loodud laoala.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-127&quot;>In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id=&quot;1c1ab-128&quot;>Valige väljal **Tüüp** väärtus **Vaikimisi**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-128&quot;>In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id=&quot;1c1ab-129&quot;>Kui soovite seadistada **Vahelao**, peate esmalt järgima neid samme, et luua täiendav ladu, kus **Tüüp** on seadistatud väärtusele **Vaheladu**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-129&quot;>If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id=&quot;1c1ab-130&quot;>Kui soovite seadistada **Transiitlao**, peate esmalt järgima neid samme, et luua täiendav ladu, kus **Tüüp** on seadistatud väärtusele **Transiit**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-130&quot;>If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id=&quot;1c1ab-131&quot;>Valige toimingupaanil nupp **Salvesta**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-131&quot;>On the action pane, select **Save**.</span></span>

## <a name=&quot;set-up-inventory-aisles&quot;></a><span data-ttu-id=&quot;1c1ab-132&quot;>Saate häälestada lao riiuliridu.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-132&quot;>Set up inventory aisles</span></span>

<span data-ttu-id=&quot;1c1ab-133&quot;>Riiuliridade seadistamiseks toimige järgmiselt.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-133&quot;>To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id=&quot;1c1ab-134&quot;>Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Asukoha seadistus \> Riiuliread**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-134&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id=&quot;1c1ab-135&quot;>Valige toimingupaanil nupp **Uus**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-135&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;1c1ab-136&quot;>Valige ripploendist **Ladu** eelnevalt loodud ladu.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;1c1ab-136&quot;>In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id=&quot;1c1ab-137&quot;>Sisestage väljale **Riiulirida** nimi (nt &quot;Vaik").</span><span class="sxs-lookup"><span data-stu-id="1c1ab-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="1c1ab-138">Sisestage väljale **Nimi** nimi (nt "Vaikimisi riiulirida").</span><span class="sxs-lookup"><span data-stu-id="1c1ab-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="1c1ab-139">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="1c1ab-140">Lao varude asukohtade häälestamine</span><span class="sxs-lookup"><span data-stu-id="1c1ab-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="1c1ab-141">Standardsete, kahjustatud ja tagastatud lao varude asukohtade seadistamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="1c1ab-142">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="1c1ab-143">Valige varem loodud ladu.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="1c1ab-144">Valige tegevuspaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="1c1ab-145">Valige tegevuspaanilt **Ladu** ja seejärel valige **Varude asukoht**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="1c1ab-146">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-146">On the action pane, select **New**.</span></span> <span data-ttu-id="1c1ab-147">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="1c1ab-148">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="1c1ab-149">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="1c1ab-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="1c1ab-150">Sisestage lao nimi kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="1c1ab-151">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="1c1ab-152">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="1c1ab-153">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="1c1ab-154">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="1c1ab-155">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="1c1ab-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="1c1ab-156">Sisestage "Kahjustatud" kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="1c1ab-157">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="1c1ab-158">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="1c1ab-159">Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="1c1ab-160">Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="1c1ab-161">Seadistage **Käsitsi värskendamine** väärtusele **Jah**</span><span class="sxs-lookup"><span data-stu-id="1c1ab-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="1c1ab-162">Sisestage "Tagastused" kasti **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="1c1ab-163">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="1c1ab-164">Järgmine pilt näitab San Francisco lao varude asukoha seadistust.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Varude asukoha seadistuse näide](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="1c1ab-166">Lao seadistamise lõpetamine</span><span class="sxs-lookup"><span data-stu-id="1c1ab-166">Complete warehouse setup</span></span>

<span data-ttu-id="1c1ab-167">Lao seadistamise lõpetamiseks järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="1c1ab-168">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="1c1ab-169">Valige varem loodud ladu.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="1c1ab-170">Valige tegevuspaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="1c1ab-171">Jaotises **Varude ja laohaldus**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="1c1ab-172">Seadistage **Vaikimisi vastuvõtu asukoht** eespool loodud asukohale.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="1c1ab-173">Valige **Vaikimisi väljastamise asukoht** eespool loodud asukohale.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="1c1ab-174">Sisestage lao aadress jaotisesse **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="1c1ab-175">Jaotises **Jaemüük**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="1c1ab-176">Sisestage kasti **Vaikimisi tagastuste asukoht** eelnevalt loodud tagastuste asukoht.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="1c1ab-177">Sea **Kauplus** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="1c1ab-178">Seadistage **Kaal** väärtusele **1.00**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="1c1ab-179">Sisestage kasti **Laoala dimensioonid** eelnevalt loodud vaikimisi asukoht.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="1c1ab-180">Seadistage jaotises **Ladu** **Füüsilise negatiivse laovaru** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="1c1ab-181">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1c1ab-182">Järgmine pilt näitab konfigureeritud lao üksikasju.</span><span class="sxs-lookup"><span data-stu-id="1c1ab-182">The following image shows details for a configured warehouse.</span></span>

![Konfigureeritud lao näide](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="1c1ab-184">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1c1ab-184">Additional resources</span></span>

[<span data-ttu-id="1c1ab-185">Laohalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="1c1ab-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1c1ab-186">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="1c1ab-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="1c1ab-187">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="1c1ab-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="1c1ab-188">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="1c1ab-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="1c1ab-189">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="1c1ab-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="1c1ab-190">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="1c1ab-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
