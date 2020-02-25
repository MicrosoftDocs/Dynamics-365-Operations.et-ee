---
title: Kliendi tellimused Modern POS-is (MPOS-is)
description: See teema annab teavet klienditellimuste kohta kaasaegses kassas (MPOS). Klienditellimused on teise nimega eritellimused. Teema hõlmab arutelu seotud parameetrite ja kandevoogude kohta.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b8ea8339c2ad25ceed2415eb5ccf5e2048c612fa
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022219"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="6c5af-105">Kliendi tellimused Modern POS-is (MPOS-is)</span><span class="sxs-lookup"><span data-stu-id="6c5af-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c5af-106">See teema annab teavet klienditellimuste kohta kaasaegses kassas (MPOS).</span><span class="sxs-lookup"><span data-stu-id="6c5af-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="6c5af-107">Klienditellimused on teise nimega eritellimused.</span><span class="sxs-lookup"><span data-stu-id="6c5af-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="6c5af-108">Teema hõlmab arutelu seotud parameetrite ja kandevoogude kohta.</span><span class="sxs-lookup"><span data-stu-id="6c5af-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="6c5af-109">Mitmekanalilises kaubandusmaailmas pakuvad paljud jaemüüjad mitmesuguste toote- ja täitmisnõuete täitmiseks klienditellimuste ehk eritellimuste võimalust.</span><span class="sxs-lookup"><span data-stu-id="6c5af-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="6c5af-110">Tüüpilised stsenaariumid on näiteks järgmised.</span><span class="sxs-lookup"><span data-stu-id="6c5af-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="6c5af-111">Klient soovib tooted kohale toimetada kindlal kuupäeval kindlale aadressile.</span><span class="sxs-lookup"><span data-stu-id="6c5af-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="6c5af-112">Klient soovib tooted kätte saada teisest poest või asukohast kui see, kust ta tooted ostis.</span><span class="sxs-lookup"><span data-stu-id="6c5af-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="6c5af-113">Klient soovib, et tema ostetud tooted saab kätte keegi teine.</span><span class="sxs-lookup"><span data-stu-id="6c5af-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="6c5af-114">Jaemüüjad kasutavad klienditellimusi ka kaotatud müügi minimeerimiseks, mida laoseisak võib põhjustada, kuna kauba saab tarnida või kätte saada teisel ajal või teises kohas.</span><span class="sxs-lookup"><span data-stu-id="6c5af-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="6c5af-115">Klienditellimuste seadistamine</span><span class="sxs-lookup"><span data-stu-id="6c5af-115">Set up customer orders</span></span>

<span data-ttu-id="6c5af-116">Lehel **Kaubanduse parameetrid** saate määrata muu hulgas järgmisi parameetreid klienditellimuste täitmisviisi määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="6c5af-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="6c5af-117">**Deposiidi vaikeprotsent** – saate määrata summa, mille klient peab enne tellimuse kinnitamist deposiidina tasuma.</span><span class="sxs-lookup"><span data-stu-id="6c5af-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="6c5af-118">Deposiidi vaikesumma arvutatakse protsendina tellimuse väärtusest.</span><span class="sxs-lookup"><span data-stu-id="6c5af-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="6c5af-119">Olenevalt õigustest võib poemüüja summa alistada, kasutades valikut **Deposiidi alistamine**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="6c5af-120">**Tühistamistasu protsent** – saate määrata klienditellimuse tühistamisel rakendatava tasu summa.</span><span class="sxs-lookup"><span data-stu-id="6c5af-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="6c5af-121">**Tühistamistasu kood** – kui klienditellimuse tühistamisel rakendatakse tasu, kajastub see müügitellimusel tasukoodi all.</span><span class="sxs-lookup"><span data-stu-id="6c5af-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="6c5af-122">Kasutage seda parameetrit tühistamistasu koodi määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="6c5af-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="6c5af-123">**Saatekulude kood** – jaemüüjad saavad määrata lisatasu kauba saatmiseks kliendile.</span><span class="sxs-lookup"><span data-stu-id="6c5af-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="6c5af-124">Saatekulude summa kajastub müügitellimusel tasukoodi all.</span><span class="sxs-lookup"><span data-stu-id="6c5af-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="6c5af-125">Kasutage seda parameetrit saatekulude koodi vastendamiseks klienditellimuse saatekuludega.</span><span class="sxs-lookup"><span data-stu-id="6c5af-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="6c5af-126">**Saatekulude tagasimakse** – saate määrata, kas klienditellimusega seostatud saatekulud on tagasi makstavad.</span><span class="sxs-lookup"><span data-stu-id="6c5af-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="6c5af-127">**Maksimaalne kinnitamata summa** – saate määrata saatekulude tagasimakse maksimaalse summa tagastustellimustele, kui saatekulud on tagasi makstavad.</span><span class="sxs-lookup"><span data-stu-id="6c5af-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="6c5af-128">Selle summa ületamisel peab tagasimakse jätkamiseks tegema haldur alistamistoimingu.</span><span class="sxs-lookup"><span data-stu-id="6c5af-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="6c5af-129">Järgmiste stsenaariumide võimaldamiseks võib saatekulude tagasimakse ületada algselt makstud summat.</span><span class="sxs-lookup"><span data-stu-id="6c5af-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="6c5af-130">Tasud rakendatakse müügitellimuse päise tasemel ja tooterea osalise koguse tagastamisel ei saa toodete ja koguse puhul lubatud saatekulude maksimaalset tagasimakset määrata viisil, mis toimiks kõigi klientide puhul.</span><span class="sxs-lookup"><span data-stu-id="6c5af-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="6c5af-131">Saatekulud lisatakse igale saatmisele.</span><span class="sxs-lookup"><span data-stu-id="6c5af-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="6c5af-132">Kui klient tagastab tooteid mitu korda ja jaemüüja poliitika määrab, et jaemüüja kannab saatekulude tagastamiskulu, on tagastatavad saatekulud suuremad kui tegelikud saatekulud.</span><span class="sxs-lookup"><span data-stu-id="6c5af-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="6c5af-133">Klienditellimuste kannetevoog</span><span class="sxs-lookup"><span data-stu-id="6c5af-133">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="6c5af-134">Klienditellimuse loomine kaasaegses kassas</span><span class="sxs-lookup"><span data-stu-id="6c5af-134">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="6c5af-135">Lisage kandesse klient.</span><span class="sxs-lookup"><span data-stu-id="6c5af-135">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="6c5af-136">Lisage tooted ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="6c5af-136">Add products to the cart.</span></span>
3. <span data-ttu-id="6c5af-137">Klõpsake valikut **Loo klienditellimus** ja seejärel valige tellimuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="6c5af-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="6c5af-138">Tellimuse tüüp võib olla kas **Klienditellimus** või **Pakkumine**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-138">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="6c5af-139">Klõpsake valikut **Saada valitud** või **Saada kõik**, et saata tooted kliendi kontol olevale aadressile ning määrake nõutud saatmiskuupäev ja saatekulud.</span><span class="sxs-lookup"><span data-stu-id="6c5af-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="6c5af-140">Klõpsake valikut **Komplekteeri valitud** või **Komplekteeri kõik**, et valida tooted, mis komplekteeritakse praegusest poest või teisest poest kindlal kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="6c5af-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="6c5af-141">Koguge deposiidisumma, kui deposiit on nõutav.</span><span class="sxs-lookup"><span data-stu-id="6c5af-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="6c5af-142">Olemasoleva klienditellimuse redigeerimine</span><span class="sxs-lookup"><span data-stu-id="6c5af-142">Edit an existing customer order</span></span>

1. <span data-ttu-id="6c5af-143">Klõpsake avalehel valikut **Leia tellimus**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-143">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="6c5af-144">Otsige üles ja valige redigeeritav tellimus.</span><span class="sxs-lookup"><span data-stu-id="6c5af-144">Find and select the order to edit.</span></span> <span data-ttu-id="6c5af-145">Klõpsake lehe alaservas valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="6c5af-146">Tellimuse komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="6c5af-146">Pick up an order</span></span>

1. <span data-ttu-id="6c5af-147">Klõpsake avalehel valikut **Leia tellimus**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-147">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="6c5af-148">Valige komplekteeritav tellimus.</span><span class="sxs-lookup"><span data-stu-id="6c5af-148">Select the order to pick up.</span></span> <span data-ttu-id="6c5af-149">Klõpsake lehe alaservas valikut **Komplekteerimine ja pakkimine**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-149">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="6c5af-150">Klõpsake valikut **Komplekteeri**</span><span class="sxs-lookup"><span data-stu-id="6c5af-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="6c5af-151">Tellimuse tühistamine</span><span class="sxs-lookup"><span data-stu-id="6c5af-151">Cancel an order</span></span>

1. <span data-ttu-id="6c5af-152">Klõpsake avalehel valikut **Leia tellimus**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-152">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="6c5af-153">Valige tühistatav tellimus.</span><span class="sxs-lookup"><span data-stu-id="6c5af-153">Select the order to cancel.</span></span> <span data-ttu-id="6c5af-154">Klõpsake lehe alaservas valikut **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-154">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="6c5af-155">Tagastustellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="6c5af-155">Create a return order</span></span>

1. <span data-ttu-id="6c5af-156">Klõpsake avalehel valikut **Leia tellimus**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-156">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="6c5af-157">Valige tagastatav tellimus, valige tellimuse arve ja seejärel valige tagastatava kauba tooterida.</span><span class="sxs-lookup"><span data-stu-id="6c5af-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="6c5af-158">Klõpsake lehe alaservas valikut **Tagasta tellimus**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="6c5af-159">Klienditellimuste asünkroonne kannetevoog</span><span class="sxs-lookup"><span data-stu-id="6c5af-159">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="6c5af-160">Klienditellimus saab luua kassa klientrakendusest kas sünkroonses režiimis või asünkroonses režiimis.</span><span class="sxs-lookup"><span data-stu-id="6c5af-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="6c5af-161">Klienditellimuste asünkroonses režiimis loomise lubamine</span><span class="sxs-lookup"><span data-stu-id="6c5af-161">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="6c5af-162">Klõpsake **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassaprofiil** &gt; **Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-162">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="6c5af-163">Määrake kiirkaardil **Üldine** valiku **Klienditellimuse loomine asünkroonses režiimis** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6c5af-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="6c5af-164">Kui suvandi **Klienditellimuse loomine asünkroonses režiimis** sätteks on valitud **Jah**, luuakse klienditellimused alati asünkroonses režiimis, isegi kui Retail Transaction Service (RTS) on saadaval.</span><span class="sxs-lookup"><span data-stu-id="6c5af-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="6c5af-165">Kui määrate valiku sätteks **Ei**, luuakse klienditellimused alati sünkroonses režiimis, kasutades RTS-i.</span><span class="sxs-lookup"><span data-stu-id="6c5af-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="6c5af-166">Kui klienditellimused luuakse asünkroonses režiimis, tõmmatakse ja sisestatakse need Commerce'i tõmbamise (P) töödena.</span><span class="sxs-lookup"><span data-stu-id="6c5af-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="6c5af-167">Vastavad müügitellimused luuakse, kui käsk **Sünkrooni tellimused** käivitatakse käsitsi või pakktöötluse kaudu.</span><span class="sxs-lookup"><span data-stu-id="6c5af-167">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c5af-168">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6c5af-168">Additional resources</span></span>

[<span data-ttu-id="6c5af-169">Hübriidkliendi tellimused</span><span class="sxs-lookup"><span data-stu-id="6c5af-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)