---
title: Tagastuse hind ja tagastuspartii ID
description: Võib-olla soovite, et tagastatud toodete kulu oleks võrdne toodete kuluga ajal, kui tooted kliendile müüsite. Seda saate määrata valikuga **Tagastatud partii ID**.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3d038b90595511b25863865045c5ce8ad45b1e0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216321"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="70c07-104">Tagastuse hind ja tagastuspartii ID</span><span class="sxs-lookup"><span data-stu-id="70c07-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="70c07-105">Varudesse tagastatavate toodete kulu arvutatakse, kasutades toodete praegust kulu.</span><span class="sxs-lookup"><span data-stu-id="70c07-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="70c07-106">Kuid võib-olla soovite, et tagastatud toodete kulu oleks võrdne toodete kuluga ajal, kui tooted kliendile müüsite.</span><span class="sxs-lookup"><span data-stu-id="70c07-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="70c07-107">Selleks võite kasutada välja **Tagastatud partii ID** kiirkaardil **Rea üksikasjad** vormis **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="70c07-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="70c07-108">Vaadake näiteks järgmist stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="70c07-108">For example, consider the following scenario.</span></span> <span data-ttu-id="70c07-109">Saadate kliendile arve.</span><span class="sxs-lookup"><span data-stu-id="70c07-109">You invoice a customer.</span></span> <span data-ttu-id="70c07-110">Seejärel tagastab klient teile tarnitud tooted.</span><span class="sxs-lookup"><span data-stu-id="70c07-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="70c07-111">Teie tagastate tooted lattu.</span><span class="sxs-lookup"><span data-stu-id="70c07-111">You return the products to stock.</span></span> <span data-ttu-id="70c07-112">Kliendile tagastatud toodete eest tagastatava makse korral arvutatakse toodete kulu, kasutades toodete praegust kulu.</span><span class="sxs-lookup"><span data-stu-id="70c07-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="70c07-113">Kui kui kasutate välja **Tagastuse partii ID**, arvutatakse tagastatud toodete kulu, kasutades algsel müügil kliendile esitatud arvel olevat kulu.</span><span class="sxs-lookup"><span data-stu-id="70c07-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="70c07-114">Muu kui praeguse kulu kasutamiseks tagasimaksete tegemiseks kliendile toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="70c07-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="70c07-115">Meetod 1: sisestage käsitsi tagastuse omahind</span><span class="sxs-lookup"><span data-stu-id="70c07-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="70c07-116">Kui lisate tagastustellimusse kauba, tagastatakse kaubad lattu vaikimisi praeguse omahinnaga.</span><span class="sxs-lookup"><span data-stu-id="70c07-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="70c07-117">Muu tagastuse omahinna määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="70c07-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="70c07-118">Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Tagastustellimused** \> **Kõik tagastustellimused**.</span><span class="sxs-lookup"><span data-stu-id="70c07-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="70c07-119">Klõpsake **Toimingupaanil** grupis **Uus** valikut **Tagastustellimus**.</span><span class="sxs-lookup"><span data-stu-id="70c07-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="70c07-120">Valige vormis **Tagastustellimuse loomine** kliendikonto ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="70c07-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="70c07-121">Valige vormil **Tagastustellimus – RMA number: %1, %2** kaup ja sisestage väljale **Kogus** negatiivne kogus.</span><span class="sxs-lookup"><span data-stu-id="70c07-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="70c07-122">Klõpsake kiirkaarti **Rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="70c07-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="70c07-123">Vahekaardil **Üldine** sisestage väärtus välja **Tagastuse omahind**.</span><span class="sxs-lookup"><span data-stu-id="70c07-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="70c07-124">Seda väärtust kasutatakse kaupade tagastamisel lattu.</span><span class="sxs-lookup"><span data-stu-id="70c07-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="70c07-125">Kui te väärtust ei sisesta, kasutatakse kaupade tagastamisel lattu praegust omahinda.</span><span class="sxs-lookup"><span data-stu-id="70c07-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="70c07-126">Meetod 2: looge automaatselt omahind kliendiarve rea põhjal</span><span class="sxs-lookup"><span data-stu-id="70c07-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="70c07-127">See on tagastusridade loomisel eelistatud meetod.</span><span class="sxs-lookup"><span data-stu-id="70c07-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="70c07-128">Selleks et kasutada toodete kulu, mis kehtis toodete müümisel kliendile, looge tagastustellimus ja määrake tagastusele müügirida.</span><span class="sxs-lookup"><span data-stu-id="70c07-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="70c07-129">Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Tagastustellimused** \> **Kõik tagastustellimused**.</span><span class="sxs-lookup"><span data-stu-id="70c07-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="70c07-130">Klõpsake **Toimingupaanil** grupis **Uus** valikut **Tagastustellimus**.</span><span class="sxs-lookup"><span data-stu-id="70c07-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="70c07-131">Valige vormis **Tagastustellimuse loomine** kliendikonto ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="70c07-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="70c07-132">Klõpsake vormil **Tagastustellimus – RMA number: %1, %2** **Toimingupaanil** suvandit **Otsi müügitellimust**.</span><span class="sxs-lookup"><span data-stu-id="70c07-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="70c07-133">Valige vormis **Otsi müügitellimust** tagastatav arverida ja klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="70c07-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="70c07-134">Kiirkaardil **Rea üksikasjad** vahekaardil **Üldine** väljas **Tagastuse partii ID** kuvatakse väärtus algselt müügirealt.</span><span class="sxs-lookup"><span data-stu-id="70c07-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="70c07-135">Peale selle kuvab väli **Tagastuse omahind** omahinna algselt müügirealt.</span><span class="sxs-lookup"><span data-stu-id="70c07-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="70c07-136">Kulu kalkulatsiooni näide</span><span class="sxs-lookup"><span data-stu-id="70c07-136">Cost calculation example</span></span>

<span data-ttu-id="70c07-137">Kui kasutate välja **Tagastuse partii ID** tagastustellimuse real tagastuse omahinna määramiseks, kasutatakse kulu tagastustellimuse real.</span><span class="sxs-lookup"><span data-stu-id="70c07-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="70c07-138">Kui kasutate lao sulgemise või ümberarvutuse funktsiooni, kohandatakse kulu algsel müügireal.</span><span class="sxs-lookup"><span data-stu-id="70c07-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="70c07-139">Kulu tagastustellimuse real kohandatakse automaatselt, et see kajastaks sama kulu tüki kohta.</span><span class="sxs-lookup"><span data-stu-id="70c07-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="70c07-140">Looge ja väljastage toode nimega Test.</span><span class="sxs-lookup"><span data-stu-id="70c07-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="70c07-141">Sisestage vormi **Väljastatud toote üksikasjad** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="70c07-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="70c07-142">Kiirkaardil **Kulude haldamine** väljas **Kaubagrupp** valige grupp **Osad**.</span><span class="sxs-lookup"><span data-stu-id="70c07-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="70c07-143">Kiirkaardi **Üldine** väljal **Kauba mudeligrupp** valige suvand **DEF**.</span><span class="sxs-lookup"><span data-stu-id="70c07-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="70c07-144">Kiirkaardil **Ost** välja **Hind** sisestage kauba omahinnaks 10.00.</span><span class="sxs-lookup"><span data-stu-id="70c07-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="70c07-145">Klõpsake **toimingupaanil** valikut **Dimensioonigrupid**.</span><span class="sxs-lookup"><span data-stu-id="70c07-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="70c07-146">Valige väljas **Laoala dimensiooni grupp** suvand **Ainult tegevuskoht ja ladu**.</span><span class="sxs-lookup"><span data-stu-id="70c07-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="70c07-147">Valige väljas **Jälgimisdimensiooni grupp** suvand **Aktiivne jälgimisdimensioon puudub**.</span><span class="sxs-lookup"><span data-stu-id="70c07-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="70c07-148">Looge 10 katsekaubale ostutellimus hinnaga 6.00 tüki kohta ja sisestage arve ostutellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="70c07-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="70c07-149">Looge 10 katsekaubale teine ostutellimus hinnaga 8.00 tüki kohta ja sisestage arve ostutellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="70c07-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="70c07-150">Sisestage arve müügitellimusele, et müüa viis katsekaupa.</span><span class="sxs-lookup"><span data-stu-id="70c07-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="70c07-151">Sel juhul määratakse müügitellimusele reale kulu väärtus 35.00 (5 tükki \* keskmine kulu 7.00 tüki kohta).</span><span class="sxs-lookup"><span data-stu-id="70c07-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="70c07-152">Looge kliendile tagastustellimus.</span><span class="sxs-lookup"><span data-stu-id="70c07-152">Create a return order for the customer.</span></span> <span data-ttu-id="70c07-153">Valige vormis **Otsi müügitellimust** arverida ja klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="70c07-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="70c07-154">Kontrollige vormis **Tagastustellimus – RMA number: %1, %2**, kas tagastustellimus on loodud katsekauba tagastamiseks.</span><span class="sxs-lookup"><span data-stu-id="70c07-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="70c07-155">Tagastustellimuse koguseks on määratud –5.00.</span><span class="sxs-lookup"><span data-stu-id="70c07-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="70c07-156">Väljas **Tagastuse partii ID** kuvatakse partii ID.</span><span class="sxs-lookup"><span data-stu-id="70c07-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="70c07-157">See partii ID võetakse kliendile müüdud kauba algsest müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="70c07-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="70c07-158">Väli **Tagastuse omahind** kuvab omahinna algselt müügirealt.</span><span class="sxs-lookup"><span data-stu-id="70c07-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="70c07-159">Registreerige tagastatud kauba sissetulek.</span><span class="sxs-lookup"><span data-stu-id="70c07-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="70c07-160">Sisestage tagastatud kaupadele saateleht.</span><span class="sxs-lookup"><span data-stu-id="70c07-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="70c07-161">Sisestage tagastustellimusele arve.</span><span class="sxs-lookup"><span data-stu-id="70c07-161">Post an invoice for the return order.</span></span> <span data-ttu-id="70c07-162">Valige loendilehelt **Kõik müügitellimused** müügitellimus, mille puhul tellimuse tüüp on **Tagastatud tellimus**.</span><span class="sxs-lookup"><span data-stu-id="70c07-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="70c07-163">Avage vorm **Laokanded**.</span><span class="sxs-lookup"><span data-stu-id="70c07-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="70c07-164">Kontrollige, kas tagastusel on arvutatud kulu 7.00 tüki kohta, kasutades väärtust väljas **Tagastuse omahind**, väljas **Omahind** on kogukulu 35.00.</span><span class="sxs-lookup"><span data-stu-id="70c07-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="70c07-165">Vormi **Laokanded** saate avada vormilt **Tagastustellimus – RMA number: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="70c07-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="70c07-166">Klõpsake ruudustikul **Read** valikuid **Varud** \> **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="70c07-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="70c07-167">Kasutage varude ja laohalduses vormi **Sulgemine ja korrigeerimine**, et käivitada protseduur **3. Sulgemine**.</span><span class="sxs-lookup"><span data-stu-id="70c07-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="70c07-168">See toiming kohandab algse müügirea kulu, mis arvutati väärtuselt –35.00 (5 tükki \* 7.00) väärtusele –30.00 (5 tükki \* 6.00).</span><span class="sxs-lookup"><span data-stu-id="70c07-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="70c07-169">See on seepärast, et laomudeligrupp kasutab elavjärjekorra mudelit (FIFO) ja 6.00 tüki kohta FIFO kulu esimesest ostutellimusest.</span><span class="sxs-lookup"><span data-stu-id="70c07-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="70c07-170">Peale selle kohandab toiming tagastusmüügi rea kulu, et see ühtiks kuluga tüki kohta algsel müügireal.</span><span class="sxs-lookup"><span data-stu-id="70c07-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="70c07-171">Seega kohandatakse tagastusrea kulu väärtuselt 35.00 väärtusele 30.00.</span><span class="sxs-lookup"><span data-stu-id="70c07-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




