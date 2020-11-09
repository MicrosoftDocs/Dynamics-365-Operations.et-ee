---
title: Komplekteerimisridade grupeerimine
description: See teema annab ülevaate komplekteerimisridade grupeerimisest.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017732"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="86d90-103">Komplekteerimisridade grupeerimine</span><span class="sxs-lookup"><span data-stu-id="86d90-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86d90-104">Komplekteerimisridade grupeerimisel saab mitut töörida, millel on sama üksus ja asukoht, kombineerida üheks komplekteerimiseks, mis edastatakse mobiilse seadme kasutajale.</span><span class="sxs-lookup"><span data-stu-id="86d90-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="86d90-105">Seega saavad laotöötajad võtta vastu kõige tõhusamad võimalikud juhiseid, kuid samal ajal säilitatakse nõutav süsteemi tööridade eraldamine (nt erinevate konteinerite ja tellimuste jaoks).</span><span class="sxs-lookup"><span data-stu-id="86d90-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="86d90-106">Komplekteerimisridade grupeerimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="86d90-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="86d90-107">Mobiilse seadme menüü-üksuse loomine</span><span class="sxs-lookup"><span data-stu-id="86d90-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="86d90-108">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused** ja looge uus menüü-üksus, mille nimi on **Müügigrupi rea komplekteerimine – kasutaja suunatud**.</span><span class="sxs-lookup"><span data-stu-id="86d90-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items** , and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="86d90-109">Määrake jaotises **Mobiilse seadme menüü-üksused** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="86d90-109">Under **Mobile device menu items** , set the following values:</span></span>

    - <span data-ttu-id="86d90-110">Väljale **Menüü-üksuse nimi** sisestage **Müügi komplekteerimine – grupi rida**.</span><span class="sxs-lookup"><span data-stu-id="86d90-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="86d90-111">Väljale **Pealkiri** sisestage **Müügi komplekteerimine – grupi rida**.</span><span class="sxs-lookup"><span data-stu-id="86d90-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="86d90-112">Valige väljal **Režiim** suvand **Töö**.</span><span class="sxs-lookup"><span data-stu-id="86d90-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="86d90-113">Valige suvandi **Kasuta olemasolevat tööd** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="86d90-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="86d90-114">Kiirkaardil **Üldine** saate määrata järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="86d90-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="86d90-115">Väljale **Juhtija** valige **Kasutaja suunatud**.</span><span class="sxs-lookup"><span data-stu-id="86d90-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="86d90-116">Määrake suvand **Loo litsentsiplaat** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="86d90-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="86d90-117">Määrake suvand **Grupi komplekteerimine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="86d90-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="86d90-118">Kiirkaardil **Töö klassid** järgige neid etappe, et konfigureerida mobiilse seadme menüü-üksuse kehtivad töö klassid.</span><span class="sxs-lookup"><span data-stu-id="86d90-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="86d90-119">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="86d90-119">Select **New**.</span></span>
    2. <span data-ttu-id="86d90-120">Väljal **Töö klassi ID** valige **Müük** või **SO komplekteerimine** , olenevalt kasutatavast laost.</span><span class="sxs-lookup"><span data-stu-id="86d90-120">In the **Work class ID** field, select **Sales** or **SO Pick** , depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="86d90-121">Valige väljal **Töökäsu tüüp** suvand **Müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="86d90-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="86d90-122">Mobiilse seadme menüü seadistamine</span><span class="sxs-lookup"><span data-stu-id="86d90-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="86d90-123">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="86d90-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="86d90-124">Lisage menüü-üksus, mille just lõite, soovitud menüüsse.</span><span class="sxs-lookup"><span data-stu-id="86d90-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="86d90-125">Töömalli häälestamine</span><span class="sxs-lookup"><span data-stu-id="86d90-125">Set up a work template</span></span>

1. <span data-ttu-id="86d90-126">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="86d90-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="86d90-127">Leidke selle funktsiooniga kasutatav töömall.</span><span class="sxs-lookup"><span data-stu-id="86d90-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="86d90-128">Selle näite puhul valige standardne **51 Ettevalmistamiseks komplekteerimine** Contoso töömall.</span><span class="sxs-lookup"><span data-stu-id="86d90-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="86d90-129">Valige menüüs käsk **Redigeeri päringut**.</span><span class="sxs-lookup"><span data-stu-id="86d90-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="86d90-130">Vahekaardil **Sortimine** valige suvand **Lisa** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="86d90-130">On the **Sorting** tab, select **Add** , and then set the following values:</span></span>

    - <span data-ttu-id="86d90-131">Valige väljal **Tabel** suvand **Ajutised töökanded**.</span><span class="sxs-lookup"><span data-stu-id="86d90-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="86d90-132">Valige väljal **Tuletatud tabel** suvand **Ajutised töökanded**.</span><span class="sxs-lookup"><span data-stu-id="86d90-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="86d90-133">Valige väljal **Väli** suvand **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="86d90-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="86d90-134">Valige väljal **Otsingu suund** suvand **Kasvav**.</span><span class="sxs-lookup"><span data-stu-id="86d90-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="86d90-135">Komplekteerimisrea grupeerimise funktsiooni töötamiseks peavad töö read olema sorditud kauba ID järgi.</span><span class="sxs-lookup"><span data-stu-id="86d90-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="86d90-136">Kui samu üksuseid sisaldavad read ei ole üksteise järel järjestatud, siis neid ei grupeerita.</span><span class="sxs-lookup"><span data-stu-id="86d90-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="86d90-137">Näide</span><span class="sxs-lookup"><span data-stu-id="86d90-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="86d90-138">Komplekteerimistöö loomine</span><span class="sxs-lookup"><span data-stu-id="86d90-138">Create picking work</span></span>

<span data-ttu-id="86d90-139">Enne kogumi komplekteerimise seadistamist peate looma mõne sobiliku väljamineva töö.</span><span class="sxs-lookup"><span data-stu-id="86d90-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="86d90-140">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="86d90-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="86d90-141">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="86d90-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="86d90-142">Valige väljalt **Kliendi konto** mis tahes klient.</span><span class="sxs-lookup"><span data-stu-id="86d90-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="86d90-143">Kiirkaardi **Üldine** väljal **Ladu** valige **51**.</span><span class="sxs-lookup"><span data-stu-id="86d90-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="86d90-144">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="86d90-144">Then select **OK**.</span></span>
5. <span data-ttu-id="86d90-145">Lisage jaotises **Müügitellimuse read** järgmised kuus rida:</span><span class="sxs-lookup"><span data-stu-id="86d90-145">Under **Sales order lines** , add the following six lines:</span></span>

    - <span data-ttu-id="86d90-146">**1. rida:** valige väljal **Kaubakood** väärtus **M9200**.</span><span class="sxs-lookup"><span data-stu-id="86d90-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="86d90-147">Sisestage väljale **Kogus** väärtus **3**.</span><span class="sxs-lookup"><span data-stu-id="86d90-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="86d90-148">**2. rida:** valige väljal **Kaubakood** väärtus **M9201**.</span><span class="sxs-lookup"><span data-stu-id="86d90-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="86d90-149">Sisestage väljale **Kogus** väärtus **3**.</span><span class="sxs-lookup"><span data-stu-id="86d90-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="86d90-150">**3. rida:** valige väljal **Kaubakood** väärtus **M9202**.</span><span class="sxs-lookup"><span data-stu-id="86d90-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="86d90-151">Sisestage väljale **Kogus** väärtus **2**.</span><span class="sxs-lookup"><span data-stu-id="86d90-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="86d90-152">**4. rida:** valige väljal **Kaubakood** väärtus **M9200**.</span><span class="sxs-lookup"><span data-stu-id="86d90-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="86d90-153">Sisestage väljale **Kogus** väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="86d90-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="86d90-154">**5. rida:** valige väljal **Kaubakood** väärtus **M9200**.</span><span class="sxs-lookup"><span data-stu-id="86d90-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="86d90-155">Sisestage väljale **Kogus** väärtus **3**.</span><span class="sxs-lookup"><span data-stu-id="86d90-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="86d90-156">**6. rida:** valige väljal **Kaubakood** väärtus **M9202**.</span><span class="sxs-lookup"><span data-stu-id="86d90-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="86d90-157">Sisestage väljale **Kogus** väärtus **7**.</span><span class="sxs-lookup"><span data-stu-id="86d90-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="86d90-158">Siin on iga üksuse üldkoguste kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="86d90-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="86d90-159">**Üksus M9200:** igat 7</span><span class="sxs-lookup"><span data-stu-id="86d90-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="86d90-160">**Üksus M9201:** igat 3</span><span class="sxs-lookup"><span data-stu-id="86d90-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="86d90-161">**Üksus M9202:** igat 9</span><span class="sxs-lookup"><span data-stu-id="86d90-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="86d90-162">Enne tellimuste lattu vabastamist peate veenduma, et komplekteerimise asukohtadel on kõikide tellimuste kõigi üksuste jaoks piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="86d90-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="86d90-163">Vaadake üle seadistus **Asukoha korraldus** , et määratleda, milliseid komplekteerimise asukohti müügitellimuse komplekteerimiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="86d90-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="86d90-164">Reserveerige varud ja vabastage need lattu.</span><span class="sxs-lookup"><span data-stu-id="86d90-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="86d90-165">Luuakse töö ID, millel on kuus rida.</span><span class="sxs-lookup"><span data-stu-id="86d90-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="86d90-166">Read sorditakse kaubakoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="86d90-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="86d90-167">Mobiilse seadme voo käitamine</span><span class="sxs-lookup"><span data-stu-id="86d90-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="86d90-168">Valige mobiilses seadmes menüü, mis sisaldab uut mobiilse seadme menüü-üksust.</span><span class="sxs-lookup"><span data-stu-id="86d90-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="86d90-169">Valige menüü-üksus **Müügi komplekteerimine – grupi rida** ja käivitage komplekteerimine.</span><span class="sxs-lookup"><span data-stu-id="86d90-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="86d90-170">Pärast menüü valimist ja töö ID sisestamist näete komplekteerimise etappi, kus kõik üksuse M9200 komplekteerimisread on grupeeritud.</span><span class="sxs-lookup"><span data-stu-id="86d90-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="86d90-171">Saate juhise komplekteerida üksust M9200 seitse tükki.</span><span class="sxs-lookup"><span data-stu-id="86d90-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="86d90-172">Kinnitage komplekteerimise etapp.</span><span class="sxs-lookup"><span data-stu-id="86d90-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="86d90-173">Avage poolelioleva töö kliendi ekraan ja pange tähele, et kõik kolm üksuse M9200 komplekteerimisrida suleti samaaegselt.</span><span class="sxs-lookup"><span data-stu-id="86d90-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="86d90-174">Esitatakse töö rida 4.</span><span class="sxs-lookup"><span data-stu-id="86d90-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="86d90-175">Kinnitage komplekteerimise etapp.</span><span class="sxs-lookup"><span data-stu-id="86d90-175">Confirm the pick step.</span></span>

    <span data-ttu-id="86d90-176">Viimane komplekteerimise etapp mobiilsel seadmel koondab töökäsu viimased kaks komplekteerimisrida.</span><span class="sxs-lookup"><span data-stu-id="86d90-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="86d90-177">Viige lõpule kõik üheksa üksuse M9202 komplekteerimise sammu.</span><span class="sxs-lookup"><span data-stu-id="86d90-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="86d90-178">Kinnitage võtmise etapp ja mis tahes täiendavad komplekteerimise/võtmise paarid töö lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="86d90-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="86d90-179">Tööridu saab grupeerida ainult siis, kui need on järjekorras.</span><span class="sxs-lookup"><span data-stu-id="86d90-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="86d90-180">Järgmisi funktsioone ei toetata.</span><span class="sxs-lookup"><span data-stu-id="86d90-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="86d90-181">Tegeliku kaaluga kaubad.</span><span class="sxs-lookup"><span data-stu-id="86d90-181">Catch-weight items.</span></span> <span data-ttu-id="86d90-182">Kui töös sisalduvad tegeliku kaaluga kaubad, kuvatakse teile enne komplekteerimise alustamist tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="86d90-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="86d90-183">Osade komplekteerimine.</span><span class="sxs-lookup"><span data-stu-id="86d90-183">Piece picking.</span></span>
>    - <span data-ttu-id="86d90-184">Töö read, millel on lõpetamata täiendamise töö.</span><span class="sxs-lookup"><span data-stu-id="86d90-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="86d90-185">Ülekomplekteerimine.</span><span class="sxs-lookup"><span data-stu-id="86d90-185">Over-picking.</span></span>
>    - <span data-ttu-id="86d90-186">Kiirelt komplekteeritava kauba ümberjaotamine</span><span class="sxs-lookup"><span data-stu-id="86d90-186">Short picking with item reallocation</span></span>
