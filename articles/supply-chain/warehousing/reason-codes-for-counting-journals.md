---
title: Varude inventuuri põhjusekoodid
description: Selles teemas kirjeldatakse põhjusekoodide seadistamist ja rakendamist inventuuriülesannete jaoks.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: d72b171bfe149b25f5055d5bebef85b49e952295
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228485"
---
# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="658ec-103">Varude inventuuri põhjusekoodid</span><span class="sxs-lookup"><span data-stu-id="658ec-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="658ec-104">Põhjusekoodide abil saate analüüsida inventuuriprotsessi tulemusi ja protsessi käigus tekkivaid võimalikke lahknevusi.</span><span class="sxs-lookup"><span data-stu-id="658ec-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="658ec-105">Saate määrata inventuuri tegemise põhjuse, nagu katkine kaubaalus või varude korrigeerimine, mis põhineb varude näidistel.</span><span class="sxs-lookup"><span data-stu-id="658ec-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="658ec-106">Soovitamine</span><span class="sxs-lookup"><span data-stu-id="658ec-106">Recommendation</span></span>

<span data-ttu-id="658ec-107">Enne süsteemi häälestamist on soovitatav määratleda põhjusekoodidega töötamise strateegia.</span><span class="sxs-lookup"><span data-stu-id="658ec-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="658ec-108">Proovige näiteks vastata järgmistele küsimustele.</span><span class="sxs-lookup"><span data-stu-id="658ec-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="658ec-109">Kas põhjusekoodid peaksid ladudes olema kohustuslikud?</span><span class="sxs-lookup"><span data-stu-id="658ec-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="658ec-110">Kas põhjusekoodid peaksid mõningate kaupade jaoks olema kohustuslikud või valikulised?</span><span class="sxs-lookup"><span data-stu-id="658ec-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="658ec-111">Mitu põhjusekoodi te vajate?</span><span class="sxs-lookup"><span data-stu-id="658ec-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="658ec-112">Kuidas peaksid vöötkoodilugejate kasutajad põhjusekoode kasutama?</span><span class="sxs-lookup"><span data-stu-id="658ec-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="658ec-113">Kas põhjusekoodid peaksid olema eelvalitud, kohustuslikud või mitteredigeeritavad?</span><span class="sxs-lookup"><span data-stu-id="658ec-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="658ec-114">Kas laotöötajad vajavad mobiilse seadme skannerites erinevat põhjusekoodi käitumist?</span><span class="sxs-lookup"><span data-stu-id="658ec-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="658ec-115">Kui vastus on jah, saate luua rohkem menüükäske ja määrata need erinevatele inimestele.</span><span class="sxs-lookup"><span data-stu-id="658ec-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="658ec-116">Kus põhjusekoode rakendatakse</span><span class="sxs-lookup"><span data-stu-id="658ec-116">Where reason codes apply</span></span>

<span data-ttu-id="658ec-117">Saate luua mitu põhjusekoodi poliitikat ja igal põhjusekoodi poliitikal saab olla kaks inventuuri põhjusekoodi poliitikat.</span><span class="sxs-lookup"><span data-stu-id="658ec-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="658ec-118">Inventuuri põhjusekoodi poliitikaid saab kasutada lao või kauba tasemel.</span><span class="sxs-lookup"><span data-stu-id="658ec-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="658ec-119">Põhjusekoodi poliitikate seadistamine</span><span class="sxs-lookup"><span data-stu-id="658ec-119">Set up reason code policies</span></span>

1. <span data-ttu-id="658ec-120">Valige **Varude haldus** \> **Seadistus** \> **Varud** \> **Inventuuri põhjusekoodi poliitikad** ja looge uus põhjusekoodi poliitika.</span><span class="sxs-lookup"><span data-stu-id="658ec-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="658ec-121">Väljal **Inventuuri põhjusekoodi tüüp** valige kas **Kohustuslik** või **Valikuline**, et määrata, kas põhjusekoodi valimine peaks ühel järgmistest inventuuritöölehtedest olema valikuline või kohustuslik tegevus.</span><span class="sxs-lookup"><span data-stu-id="658ec-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="658ec-122">Tsükliline inventuur (mobiilne seade)</span><span class="sxs-lookup"><span data-stu-id="658ec-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="658ec-123">Punktinventuur (mobiilne seade)</span><span class="sxs-lookup"><span data-stu-id="658ec-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="658ec-124">Läveinventuur (mobiilne seade)</span><span class="sxs-lookup"><span data-stu-id="658ec-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="658ec-125">Saabumise korrigeerimine (mobiilne seade)</span><span class="sxs-lookup"><span data-stu-id="658ec-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="658ec-126">Väljastuse korrigeerimine (mobiilne seade)</span><span class="sxs-lookup"><span data-stu-id="658ec-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="658ec-127">Inventuuritööleht (rikas klient)</span><span class="sxs-lookup"><span data-stu-id="658ec-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="658ec-128">Põhjusekoode saate ka seadistada üksikute ladude ja toodete jaoks.</span><span class="sxs-lookup"><span data-stu-id="658ec-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="658ec-129">Toodete põhjusekoodi seadistus saab eirata ladude seadistust.</span><span class="sxs-lookup"><span data-stu-id="658ec-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="658ec-130">Kohustuslikud põhjusekoodid</span><span class="sxs-lookup"><span data-stu-id="658ec-130">Mandatory reason codes</span></span>

<span data-ttu-id="658ec-131">Kui ladude või kaupade põhjusekoodide konfiguratsioonis on määratud parameeter **Kohustuslik**, ei saa inventuuritöölehte enne põhjusekoodi sisestamist lõpule viia ega sulgeda.</span><span class="sxs-lookup"><span data-stu-id="658ec-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="658ec-132">Ladude põhjusekoodide häälestamine</span><span class="sxs-lookup"><span data-stu-id="658ec-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="658ec-133">Valige **Varude haldus** \> **Seadistus** \> **Laovarude jaotamine** \> **Laod**.</span><span class="sxs-lookup"><span data-stu-id="658ec-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="658ec-134">Vahekaardil **Ladu** väljal **Inventuuri põhjusekoodi poliitika** valige üks järgmistest suvanditest.</span><span class="sxs-lookup"><span data-stu-id="658ec-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="658ec-135">**Tühi** – kauba jaoks seadistatud parameetrit kasutatakse määratlemiseks, kas inventuuritöölehed on toote jaoks kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="658ec-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="658ec-136">**Kohustuslik** – põhjusekood on lao inventuuritöölehtedel alati nõutav.</span><span class="sxs-lookup"><span data-stu-id="658ec-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="658ec-137">**Valikuline** – põhjusekood pole lao inventuuritöölehtedel nõutav.</span><span class="sxs-lookup"><span data-stu-id="658ec-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="658ec-138">Toodete põhjusekoodide häälestamine</span><span class="sxs-lookup"><span data-stu-id="658ec-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="658ec-139">Valige **Tooteteabe haldus** \> **Tooted** \> **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="658ec-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="658ec-140">Vahekaardil **Toode** valige **Inventuuri põhjusekoodi poliitika** ja seejärel valige üks järgmistest suvanditest.</span><span class="sxs-lookup"><span data-stu-id="658ec-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="658ec-141">**Tühi** – lao jaoks seadistatud parameetrit kasutatakse määratlemiseks, kas inventuuritöölehed on toote jaoks kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="658ec-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="658ec-142">**Kohustuslik** – põhjusekood on toote inventuuritöölehtedel alati nõutav.</span><span class="sxs-lookup"><span data-stu-id="658ec-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="658ec-143">See säte alistab laotaseme põhjusekoodi sätted.</span><span class="sxs-lookup"><span data-stu-id="658ec-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="658ec-144">**Valikuline** – põhjusekood pole toote inventuuritöölehtedel nõutav.</span><span class="sxs-lookup"><span data-stu-id="658ec-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="658ec-145">See säte alistab laotaseme põhjusekoodi sätted.</span><span class="sxs-lookup"><span data-stu-id="658ec-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="658ec-146">Põhjusekoodide kasutamine inventuuritöölehtedel</span><span class="sxs-lookup"><span data-stu-id="658ec-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="658ec-147">Inventuuritöölehel saate lisada põhjusekoode järgmist tüüpi inventuuride jaoks:</span><span class="sxs-lookup"><span data-stu-id="658ec-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="658ec-148">Tsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="658ec-148">Cycle Count</span></span>
- <span data-ttu-id="658ec-149">Punktinventuur</span><span class="sxs-lookup"><span data-stu-id="658ec-149">Spot Count</span></span>
- <span data-ttu-id="658ec-150">Läveinventuur</span><span class="sxs-lookup"><span data-stu-id="658ec-150">Threshold Count</span></span>
- <span data-ttu-id="658ec-151">Saabumise korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="658ec-151">Adjustment In</span></span>
- <span data-ttu-id="658ec-152">Väljastuse korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="658ec-152">Adjustment Out</span></span>

<span data-ttu-id="658ec-153">Põhjusekoodid lisatakse töölehe ridadele inventuuritöölehtedel tüübiga **Inventuuritööleht**.</span><span class="sxs-lookup"><span data-stu-id="658ec-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="658ec-154">Valige **Varude haldus** \> **Töölehe sisestused** \> **Kauba inventuur** \> **Inventuur**.</span><span class="sxs-lookup"><span data-stu-id="658ec-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="658ec-155">Inventuuritöölehe rea üksikasjades väljal **Inventuuri põhjusekood** valige suvand.</span><span class="sxs-lookup"><span data-stu-id="658ec-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="658ec-156">Inventuurižurnaali kuvamine selle salvestamisel põhjusekoodide järgi</span><span class="sxs-lookup"><span data-stu-id="658ec-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="658ec-157">Valige **Varude haldus** \> **Päringud ja aruanded** \> **Inventuurižurnaal** ja seejärel väljal **Inventuuri põhjusekood** vaadake inventuurižurnaali, mis on salvestatud põhjusekoodi kaudu.</span><span class="sxs-lookup"><span data-stu-id="658ec-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="658ec-158">Põhjusekoodi kasutamine koguse korrigeerimiseks</span><span class="sxs-lookup"><span data-stu-id="658ec-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="658ec-159">Lehel **Vaba kaubavaru** valige **Koguse korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="658ec-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="658ec-160">Saate lehe **Vaba kaubavaru** avada mitmel viisil.</span><span class="sxs-lookup"><span data-stu-id="658ec-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="658ec-161">Näiteks valige **Varude haldus** \> **Päringud ja aruanded** \> **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="658ec-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="658ec-162">Valige **Koguse korrigeerimine** ja seejärel väljal **Inventuuri põhjusekood** valige põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="658ec-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="658ec-163">Põhjusekoodide konfigureerimine mobiilse seadme menüükäskude jaoks</span><span class="sxs-lookup"><span data-stu-id="658ec-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="658ec-164">Saate konfigureerida põhjusekoode iga inventuuritüübi jaoks mobiilse seadme menüükäsus.</span><span class="sxs-lookup"><span data-stu-id="658ec-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="658ec-165">Mobiilse seadme menüükäsu konfiguratsioon sisaldab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="658ec-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="658ec-166">Kas põhjusekood kuvatakse inventuuri ajal mobiilse seadme töötajale.</span><span class="sxs-lookup"><span data-stu-id="658ec-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="658ec-167">Vaikepõhjusekood, mis kuvatakse mobiilse seadme menüükäsus</span><span class="sxs-lookup"><span data-stu-id="658ec-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="658ec-168">Kas kasutaja saab põhjusekoodi redigeerida.</span><span class="sxs-lookup"><span data-stu-id="658ec-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="658ec-169">Põhjusekoodide seadistamine mobiilses seadmes</span><span class="sxs-lookup"><span data-stu-id="658ec-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="658ec-170">Valige **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="658ec-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="658ec-171">Vahekaardil **Tsükliline inventuur** valige **Tsükliline inventuur**.</span><span class="sxs-lookup"><span data-stu-id="658ec-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="658ec-172">Väljal **Inventuuri vaikepõhjusekood** määrake vaikepõhjusekood, mis tuleks salvestada, kui inventuuri tehakse mobiilse seadme menüükäsu abil.</span><span class="sxs-lookup"><span data-stu-id="658ec-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="658ec-173">Väljal **Kuva inventuuri põhjusekood** valige **Rida**, et kuvada põhjusekood pärast iga hälbe salvestamist.</span><span class="sxs-lookup"><span data-stu-id="658ec-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="658ec-174">Teise võimalusena valige **Peida**, kui põhjusekoodi ei tohiks kuvada.</span><span class="sxs-lookup"><span data-stu-id="658ec-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="658ec-175">Määrake suvandi **Redigeeri inventuuri põhjusekoodi** väärtuseks kas **Jah** või **Ei**.</span><span class="sxs-lookup"><span data-stu-id="658ec-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="658ec-176">Kui määrate selle suvandi väärtuseks **Jah**, saab töötaja redigeerida põhjusekoodi, kui see kuvatakse inventuuri ajal mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="658ec-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="658ec-177">Nupu **Tsükliline inventuur** saab lubada igas mobiilse seadme menüükäsus, kus saab teha inventuuri.</span><span class="sxs-lookup"><span data-stu-id="658ec-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="658ec-178">Näidete hulka kuuluvad menüükäsud punktinventuuride jaoks, kasutaja suunatud töö ja süsteemi suunatud töö.</span><span class="sxs-lookup"><span data-stu-id="658ec-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="658ec-179">Tsüklilise inventuuri kinnitused</span><span class="sxs-lookup"><span data-stu-id="658ec-179">Cycle count approvals</span></span>

<span data-ttu-id="658ec-180">Enne inventuuri kinnitamist saab kasutaja muuta selle inventuuriga seotud põhjusekoodi.</span><span class="sxs-lookup"><span data-stu-id="658ec-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="658ec-181">Inventuuri kinnitamisel sisestatakse põhjusekood inventuuritöölehe ridadele.</span><span class="sxs-lookup"><span data-stu-id="658ec-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="658ec-182">Tsüklilise inventuuri kinnituste muutmine</span><span class="sxs-lookup"><span data-stu-id="658ec-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="658ec-183">Valige **Laohaldus** \> **Tsükliline inventuur** \> **Ülevaatuse ootel tsüklilise inventuuri töö**.</span><span class="sxs-lookup"><span data-stu-id="658ec-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="658ec-184">Valige **Ülevaatuse ootel tsüklilise inventuuri töö** ja seejärel väljal **Põhjusekood** valige uus põhjusekood.</span><span class="sxs-lookup"><span data-stu-id="658ec-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="658ec-185">Mobiilse seadme menüükäsu muutmine saabumise korrigeerimise ja väljastuse korrigeerimise jaoks</span><span class="sxs-lookup"><span data-stu-id="658ec-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="658ec-186">Valige **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüükäsud** ja seejärel valige **Saabumise ja väljastuse korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="658ec-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="658ec-187">Valige suvandi **Kasuta olemasolevat tööd** sätteks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="658ec-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="658ec-188">Väljal **Töö loomise protsess** valige **Saabumise korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="658ec-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="658ec-189">Järgmised väljad lisatakse mobiilse seadme menüükäsule, kui töö loomise protsessi käigus on valitud **Saabumise korrigeerimine** või **Väljastuse korrigeerimine**:</span><span class="sxs-lookup"><span data-stu-id="658ec-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="658ec-190">Inventuuri vaikepõhjusekood</span><span class="sxs-lookup"><span data-stu-id="658ec-190">Default counting reason code</span></span>
- <span data-ttu-id="658ec-191">Kuva inventuuri põhjusekood</span><span class="sxs-lookup"><span data-stu-id="658ec-191">Display counting reason code</span></span>
- <span data-ttu-id="658ec-192">Redigeeri inventuuri põhjusekoodi</span><span class="sxs-lookup"><span data-stu-id="658ec-192">Edit counting reason code</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]