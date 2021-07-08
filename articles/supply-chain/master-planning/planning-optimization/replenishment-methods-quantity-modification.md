---
title: Varude täiendamise meetodid ja koguse muutmine
description: Selles teemas antakse teavet varude täiendamise meetodite kohta planeerimise optimeerimises. Lisaks selgitatakse, kuidas toote mitme tellimuse kogus mõjutab tulemust.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261692"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="61c57-104">Varude täiendamise meetodid ja koguse muutmine</span><span class="sxs-lookup"><span data-stu-id="61c57-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61c57-105">Selles teemas antakse teavet varude täiendamise meetodite kohta planeerimise optimeerimises.</span><span class="sxs-lookup"><span data-stu-id="61c57-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="61c57-106">Lisaks selgitatakse, kuidas toote mitme tellimuse kogus mõjutab tulemust.</span><span class="sxs-lookup"><span data-stu-id="61c57-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="61c57-107">Varude täiendamise meetodeid nimetatakse ka laovarude meetoditeks ja partii suuruse muutmise meetoditeks.</span><span class="sxs-lookup"><span data-stu-id="61c57-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="61c57-108">Planeerimise koodid</span><span class="sxs-lookup"><span data-stu-id="61c57-108">Coverage codes</span></span>

<span data-ttu-id="61c57-109">Planeerimise optimeerimise konfigureerimise abil saab kasutada erinevaid täiendamise meetodeid.</span><span class="sxs-lookup"><span data-stu-id="61c57-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="61c57-110">Varude täiendusmeetodid on meetodid, mida süsteem kasutab tootele esitatavate nõuete arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="61c57-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="61c57-111">Varude täiendamise meetodeid määratletakse laovarude tähistega, mida saate seadistada kas laovarude grupis või tootes.</span><span class="sxs-lookup"><span data-stu-id="61c57-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="61c57-112">Planeerimise optimeerimisel saab kasutada järgmisi laovarude tähiseid:</span><span class="sxs-lookup"><span data-stu-id="61c57-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="61c57-113">**Periood** – varude täiendamise meetod, mis koondab toote nõudluse teatud perioodi jooksul ühte tellimusse.</span><span class="sxs-lookup"><span data-stu-id="61c57-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="61c57-114">Tellimus planeeritakse perioodi esimesele päevale ja selle kogus vastab netosummale määratud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="61c57-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="61c57-115">Periood algab toote esimese nõudega ja katab määratud pikkusega aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="61c57-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="61c57-116">Järgmine periood algab toote järgmiste nõuetega.</span><span class="sxs-lookup"><span data-stu-id="61c57-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="61c57-117">*Perioodi* laovarude koodi kasutatakse sageli mitteaimatavate varude joonistamiseks, hooajast mõjutatud toodete või kallite toodete jaoks.</span><span class="sxs-lookup"><span data-stu-id="61c57-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="61c57-118">Järgmisel joonisel on toodud näide.</span><span class="sxs-lookup"><span data-stu-id="61c57-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="61c57-119">![Perioodi laovarude koodi kasutamise näide](./media/coverage-code-period.png "Perioodi laovarude koodi kasutamise näide")</span><span class="sxs-lookup"><span data-stu-id="61c57-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="61c57-120">**Nõue** – varude täiendamise meetod, mille puhul süsteem loob tootele vajaduse korral plaanitud ostu-, edastamis- või tootmistellimuse.</span><span class="sxs-lookup"><span data-stu-id="61c57-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="61c57-121">Seda meetodit kasutatakse kallite toodete puhul, millel on vahelduv nõudlus.</span><span class="sxs-lookup"><span data-stu-id="61c57-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="61c57-122">*Nõude* laovarude koodi kasutatakse sageli konfigureeritavate toodete või tellimuse järgi valmistatavate stsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="61c57-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="61c57-123">Järgmisel joonisel on toodud näide.</span><span class="sxs-lookup"><span data-stu-id="61c57-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="61c57-124">![Nõude laovarude koodi kasutamise näide](./media/coverage-code-requirement.png "Nõude laovarude koodi kasutamise näide")</span><span class="sxs-lookup"><span data-stu-id="61c57-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="61c57-125">**Min./Max.**</span><span class="sxs-lookup"><span data-stu-id="61c57-125">**Min./Max.**</span></span> <span data-ttu-id="61c57-126">– Varude täiendamise meetod põhineb laovarude tasemel.</span><span class="sxs-lookup"><span data-stu-id="61c57-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="61c57-127">See määratleb varude täiendamise kindla tasemeni, kui prognoositav vaba kaubavaru tase on allpool konkreetset künnist.</span><span class="sxs-lookup"><span data-stu-id="61c57-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="61c57-128">Varude täiendamise kogus on maksimaalse taseme ja prognoositava vaba taseme vaheline erinevus.</span><span class="sxs-lookup"><span data-stu-id="61c57-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="61c57-129">Väljad *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="61c57-129">The *Min./Max.*</span></span> <span data-ttu-id="61c57-130">varude koodi kasutatakse sageli prognoositavate varude joonistamiseks, kõrgete jooksukaupade või odavamate toodete jaoks.</span><span class="sxs-lookup"><span data-stu-id="61c57-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="61c57-131">Järgmisel joonisel on toodud näide.</span><span class="sxs-lookup"><span data-stu-id="61c57-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="61c57-132">![Min./Max. laovarude koodi kasutamise näide](./media/coverage-code-min-max.png "Min./Max. laovarude koodi kasutamise näide")</span><span class="sxs-lookup"><span data-stu-id="61c57-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="61c57-133">**Käsitsi** – varude täienduse meetodi puhul ei soovita süsteem toote ostmist, üleandmist ega tootmistellimusi.</span><span class="sxs-lookup"><span data-stu-id="61c57-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="61c57-134">Selle asemel vastutab toote planeerija toote täiendamiseks vajalike tellimuste loomise eest.</span><span class="sxs-lookup"><span data-stu-id="61c57-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="61c57-135">*Käsitsi* laovarude koodi kasutatakse sageli toodete puhul, mille jaoks süsteemi loodud plaanitud tellimusi ei taheta.</span><span class="sxs-lookup"><span data-stu-id="61c57-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="61c57-136">Tellimuse koguse mõju tellimuse vaikesätetest</span><span class="sxs-lookup"><span data-stu-id="61c57-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="61c57-137">Väljaantud toote lehel **Tellimuse vaikesätted** saate kiirkaartidel **Ostutellimus**, **Laovarud** ja **Müügitellimus** määrata kõik järgmised koguse sätted.</span><span class="sxs-lookup"><span data-stu-id="61c57-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="61c57-138">(Kiirkaarti **Laovarud** kasutatakse nii üleviimis- kui ka tootmistellimuste puhul.)</span><span class="sxs-lookup"><span data-stu-id="61c57-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="61c57-139">**Mitu** – plaanitud tellimused on selle koguse kordse väärtusega.</span><span class="sxs-lookup"><span data-stu-id="61c57-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="61c57-140">Näiteks kui välja **Mitu** väärtuseks on seatud *5*, võib tellimus olla koguses 5, 10, 15, 20 jne.</span><span class="sxs-lookup"><span data-stu-id="61c57-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="61c57-141">**Minimaalne tellimuse kogus** – plaanitud tellimused ei ole määratud väärtusest väiksemad.</span><span class="sxs-lookup"><span data-stu-id="61c57-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="61c57-142">Näiteks kui välja **Min. tellimuse kogus** väärtuseks on seatud *10*, luuakse plaanitud tellimus kogusele 10, isegi kui nõudluse täitmiseks on vaja ainult nelja tellimust.</span><span class="sxs-lookup"><span data-stu-id="61c57-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="61c57-143">**Maksimaalne tellimuse kogus** – plaanitud tellimused ei üle määratud väärtust.</span><span class="sxs-lookup"><span data-stu-id="61c57-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="61c57-144">Kui nõudlus on suurem kui **Maksimaalne tellimuse kogus**, luuakse selle katmiseks mitu plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="61c57-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="61c57-145">Näiteks kui välja **Maksimaalne tellimuse kogus** väärtuseks on seatud *100* ja nõudlus on 450, luuakse neli plaanitud tellimust kogusega 100 ja üks plaanitud tellimus kogusega 50.</span><span class="sxs-lookup"><span data-stu-id="61c57-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="61c57-146">Näited varude täiendamisest, mis kasutavad välja Min./Max.</span><span class="sxs-lookup"><span data-stu-id="61c57-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="61c57-147">laovarude kood</span><span class="sxs-lookup"><span data-stu-id="61c57-147">coverage code</span></span>

<span data-ttu-id="61c57-148">Kui te ei määra lehel **Tellimuse vaikesäte** toote väärtust väljal **Mitu** ja kasutate välja *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="61c57-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="61c57-149">täiendusmeetod, Planning Optimization täiendab varusid kuni kindla tasemeni, kui prognoositav vaba kogus on alla kindla künnise.</span><span class="sxs-lookup"><span data-stu-id="61c57-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="61c57-150">Kui määratlete tootele mitmekordse koguse, kuvatakse väljad *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="61c57-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="61c57-151">täiendusmeetod muudab oma käitumist ja arvestab **Mitu** väärtust.</span><span class="sxs-lookup"><span data-stu-id="61c57-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="61c57-152">Teisisõnu täiendab plaanimise optimeerimine varusid määratletud maksimumtasemeni, kui eeldatav vaba kaubavaru tase on määratletud miinimumtasemest väiksem.</span><span class="sxs-lookup"><span data-stu-id="61c57-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="61c57-153">Täienduskogus peab siiski olema **Mitu** väärtuse kordne.</span><span class="sxs-lookup"><span data-stu-id="61c57-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="61c57-154">Kui varude täiendamise kogus (erinevus maksimumtaseme ja prognoositud vaba kaubavaru taseme vahel) pole määratletud mitmekordse koguse kordne, kasutab plaanimise optimeerimine esimest võimalikku väärtust, mis koos prognoositud vaba kaubavaru tasemega jääb alla piirnormi.</span><span class="sxs-lookup"><span data-stu-id="61c57-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="61c57-155">Kui summa on miinimumtasemest väiksem, kasutab plaanimise optimeerimine esimest väärtust, mis koos prognoositava vaba kaubavaruga ületab piirnormi.</span><span class="sxs-lookup"><span data-stu-id="61c57-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="61c57-156">Järgmistes alajaotistes on toodud mõned näited, mis näitavad, kuidas toote mitmekordne tellimuse kogus mõjutab välja *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="61c57-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="61c57-157">varude täiendamise meetod.</span><span class="sxs-lookup"><span data-stu-id="61c57-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="61c57-158">Näide 1</span><span class="sxs-lookup"><span data-stu-id="61c57-158">Example 1</span></span>

<span data-ttu-id="61c57-159">Toote konfiguratsioon on järgmine:</span><span class="sxs-lookup"><span data-stu-id="61c57-159">A product has the following configuration:</span></span>

- <span data-ttu-id="61c57-160">**Laovarude kood**: *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="61c57-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="61c57-161">**Miinimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="61c57-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="61c57-162">**Maksimum:** *22*</span><span class="sxs-lookup"><span data-stu-id="61c57-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="61c57-163">**Mitu:** *0*</span><span class="sxs-lookup"><span data-stu-id="61c57-163">**Multiple:** *0*</span></span>

<span data-ttu-id="61c57-164">Tootel on 10 vaba kaubavaru tükki ja muud nõudlust ega pakkumist ei ole.</span><span class="sxs-lookup"><span data-stu-id="61c57-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="61c57-165">Koondplaneerimise käivitamisel luuakse varude täiendamiseks maksimumkoguseni planeeritud tellimus 12 tüki kohta.</span><span class="sxs-lookup"><span data-stu-id="61c57-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="61c57-166">Näide 2</span><span class="sxs-lookup"><span data-stu-id="61c57-166">Example 2</span></span>

<span data-ttu-id="61c57-167">Toote konfiguratsioon on järgmine:</span><span class="sxs-lookup"><span data-stu-id="61c57-167">A product has the following configuration:</span></span>

- <span data-ttu-id="61c57-168">**Laovarude kood**: *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="61c57-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="61c57-169">**Miinimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="61c57-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="61c57-170">**Maksimum:** *22*</span><span class="sxs-lookup"><span data-stu-id="61c57-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="61c57-171">**Mitu:** *5*</span><span class="sxs-lookup"><span data-stu-id="61c57-171">**Multiple:** *5*</span></span>

<span data-ttu-id="61c57-172">Tootel on 10 vaba kaubavaru tükki ja muud nõudlust ega pakkumist ei ole.</span><span class="sxs-lookup"><span data-stu-id="61c57-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="61c57-173">Koondplaneerimise käivitamisel luuakse 10 tüki plaanitud tellimust (kuna 15 täiendusühikut pluss 10 vaba kaubavaru tükki ületavad maksimumkoguse).</span><span class="sxs-lookup"><span data-stu-id="61c57-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="61c57-174">Näide 3</span><span class="sxs-lookup"><span data-stu-id="61c57-174">Example 3</span></span>

<span data-ttu-id="61c57-175">Toote konfiguratsioon on järgmine:</span><span class="sxs-lookup"><span data-stu-id="61c57-175">A product has the following configuration:</span></span>

- <span data-ttu-id="61c57-176">**Laovarude kood**: *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="61c57-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="61c57-177">**Miinimum:** *21*</span><span class="sxs-lookup"><span data-stu-id="61c57-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="61c57-178">**Maksimum:** *24*</span><span class="sxs-lookup"><span data-stu-id="61c57-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="61c57-179">**Mitu:** *5*</span><span class="sxs-lookup"><span data-stu-id="61c57-179">**Multiple:** *5*</span></span>

<span data-ttu-id="61c57-180">Tootel on 10 vaba kaubavaru tükki ja muud nõudlust ega pakkumist ei ole.</span><span class="sxs-lookup"><span data-stu-id="61c57-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="61c57-181">Koondplaneerimise käivitamisel luuakse 15 tüki plaanitud tellimust (kuna 10 täiendusühikut pluss 10 vaba kaubavaru tükki on vähem, kui miinimumkogus).</span><span class="sxs-lookup"><span data-stu-id="61c57-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
