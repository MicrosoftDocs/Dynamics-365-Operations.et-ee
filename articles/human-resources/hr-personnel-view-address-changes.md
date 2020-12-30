---
title: Aadressimuudatuste vaatamine ja haldamine
description: Selles teemas selgitatakse, kuidas vaadata ja hallata aadressimuudatusi rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a69d723b45e834b022491c8eaf2a7fb580e54f1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418098"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="1a39e-103">Aadressimuudatuste vaatamine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="1a39e-103">View and manage address changes</span></span>

<span data-ttu-id="1a39e-104">Selles teemas selgitatakse, kuidas saate vaadata ja hallata aadressimuudatusi töövõtja iseteeninduse lehel **Isikuandmete redigeerimine** või **Töötaja** üksikasjade lehel rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1a39e-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="1a39e-105">Paljud organisatsioonid tahavad, et töövõtjad haldaksid oma isikuandmeid iseteeninduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="1a39e-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="1a39e-106">Saate lubada kasutajatel tööruumis **Töövõtja iseteenindus** oma aadressi värskendada.</span><span class="sxs-lookup"><span data-stu-id="1a39e-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="1a39e-107">Seejärel saate muudatusi jälgida tööruumis **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="1a39e-108">Selle funktsiooni kasutamiseks peate määrama päevade arvu, mille jooksul soovite vaadata muudatusi lehel **Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="1a39e-109">Aadressimuudatuse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1a39e-109">Configure address change parameters</span></span>

<span data-ttu-id="1a39e-110">Et konfigureerida päevade arv, mille jooksul soovite tööruumis **Personalihaldus** aadressimuudatusi kuvada, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1a39e-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="1a39e-111">Valige navigeerimispaanil **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="1a39e-112">Valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-112">Select **Links**.</span></span>

3. <span data-ttu-id="1a39e-113">Valige **Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="1a39e-114">Sisestage jaotises **Aadressimuutus** väljale **Päevade arv** päevade arv, mille jooksul soovite kuvada aadressimuudatusi tööruumis **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="1a39e-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1a39e-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="1a39e-116">Töövõtja aadressi loomine või muutmine</span><span class="sxs-lookup"><span data-stu-id="1a39e-116">Create or change an employee address</span></span>

<span data-ttu-id="1a39e-117">Töövõtjad saavad oma aadressi värskendada tööruumis **Töövõtja iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="1a39e-118">Aadressi loomiseks või muutmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1a39e-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="1a39e-119">Valige oma avalehel paan **Töövõtja iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="1a39e-120">Valige **Redigeeri isikuandmeid**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="1a39e-121">Aadressi lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-121">To add an address, select **Add**.</span></span> <span data-ttu-id="1a39e-122">Olemasoleva aadressi värskendamiseks valige loendist aadress ja seejärel valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="1a39e-123">Sisestage **Nimi või kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="1a39e-124">Valige rippkast **Eesmärk** ja seejärel aadressi tüüp.</span><span class="sxs-lookup"><span data-stu-id="1a39e-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="1a39e-125">Sisestage **Riik/regioon**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="1a39e-126">Sisestage **Sihtnumber**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="1a39e-127">Sisestage **Tänav**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="1a39e-128">Sisestage **Linn**, **Osariik** ja **Maakond**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="1a39e-129">Tavaliselt täidetakse need väljad automaatselt välja **Sihtnumber** alusel.</span><span class="sxs-lookup"><span data-stu-id="1a39e-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="1a39e-130">Võite valida ka välja **Esmane**, et määrata esmane aadress.</span><span class="sxs-lookup"><span data-stu-id="1a39e-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="1a39e-131">Esmaseks saab märkida ainult ühe aadressi.</span><span class="sxs-lookup"><span data-stu-id="1a39e-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="1a39e-132">Kui muu aadress on juba märgitud esmaseks aadressiks, peate kinnitama, et soovite seda aadressi esmasena kasutada.</span><span class="sxs-lookup"><span data-stu-id="1a39e-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="1a39e-133">Võite valida ka välja **Privaatne**, et näidata, et aadress on privaatne.</span><span class="sxs-lookup"><span data-stu-id="1a39e-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="1a39e-134">Seda aadressi saavad vaadata ainult kasutajad, kellel on privaatse aadressi teabe vaatamiseks sõnaselge õigus.</span><span class="sxs-lookup"><span data-stu-id="1a39e-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="1a39e-135">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="1a39e-136">Töötaja aadressi loomine või muutmine</span><span class="sxs-lookup"><span data-stu-id="1a39e-136">Create or change a worker address</span></span>

<span data-ttu-id="1a39e-137">Aadressi saate värskendada tööruumis **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="1a39e-138">Aadressi loomiseks või muutmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1a39e-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="1a39e-139">Valige tööruumis **Personalihaldus** suvand **Lingid** ja seejärel **Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="1a39e-140">Valige töötaja ja seejärel **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="1a39e-141">Aadressi lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-141">To add an address, select **Add**.</span></span> <span data-ttu-id="1a39e-142">Olemasoleva aadressi värskendamiseks valige loendist aadress ja seejärel valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="1a39e-143">Sisestage **Nimi või kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="1a39e-144">Valige rippkast **Eesmärk** ja seejärel aadressi tüüp.</span><span class="sxs-lookup"><span data-stu-id="1a39e-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="1a39e-145">Sisestage **Riik/regioon**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="1a39e-146">Sisestage **Sihtnumber**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="1a39e-147">Sisestage **Tänav**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="1a39e-148">Sisestage **Linn**, **Osariik** ja **Maakond**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="1a39e-149">Tavaliselt täidetakse need väljad automaatselt välja **Sihtnumber** alusel.</span><span class="sxs-lookup"><span data-stu-id="1a39e-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="1a39e-150">Võite valida ka välja **Esmane**, et määrata esmane aadress.</span><span class="sxs-lookup"><span data-stu-id="1a39e-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="1a39e-151">Esmaseks saab märkida ainult ühe aadressi.</span><span class="sxs-lookup"><span data-stu-id="1a39e-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="1a39e-152">Kui muu aadress on juba märgitud esmaseks aadressiks, peate kinnitama, et soovite seda aadressi esmasena kasutada.</span><span class="sxs-lookup"><span data-stu-id="1a39e-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="1a39e-153">Võite valida ka välja **Privaatne**, et näidata, et aadress on privaatne.</span><span class="sxs-lookup"><span data-stu-id="1a39e-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="1a39e-154">Seda aadressi saavad vaadata ainult kasutajad, kellel on privaatse aadressi teabe vaatamiseks sõnaselge õigus.</span><span class="sxs-lookup"><span data-stu-id="1a39e-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="1a39e-155">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="1a39e-156">Aadressi jaoks tulevase muudatuse loomine</span><span class="sxs-lookup"><span data-stu-id="1a39e-156">Create a future change for an address</span></span>

<span data-ttu-id="1a39e-157">Mõnel juhul võite soovida värskendada aadressi tulevikus.</span><span class="sxs-lookup"><span data-stu-id="1a39e-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="1a39e-158">Näiteks tuleks see kasuks, kui töövõtja kolib järgmise kuu 15. kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="1a39e-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="1a39e-159">Avage leht **Aadresside haldamine**, valides ükskõik millisest aadressiruudustikust **Rohkem suvandeid > Täpsemalt**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="1a39e-160">Valige uue aadressi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="1a39e-161">Sisestage aadressi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="1a39e-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="1a39e-162">Valige kiirkaart **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="1a39e-163">Valige väljal **Jõustumiskuupäev** kuupäev, mil uus aadress jõustub.</span><span class="sxs-lookup"><span data-stu-id="1a39e-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="1a39e-164">Võite väljal **Aegumiskuupäev** valida, millal aadress enam ei kehti.</span><span class="sxs-lookup"><span data-stu-id="1a39e-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="1a39e-165">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="1a39e-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="1a39e-166">Aadressimuudatuste vaatamine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="1a39e-166">View and monitor address changes</span></span>

<span data-ttu-id="1a39e-167">Personaliosakonna töötajad saavad vaadata ja jälgida muudatusi tööruumis **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="1a39e-168">Aadressimuudatuste vaatamiseks avage **Avalehel** paan **Personalihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1a39e-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="1a39e-169">Aadressimuudatused kuvatakse paanil ülemises parempoolses nurgas.</span><span class="sxs-lookup"><span data-stu-id="1a39e-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="1a39e-170">Jaotise **Aadressimuudatused** kohal olev arv näitab, mitu korda muudeti aadressi lehel **Inimressursside parameetrid** täpsustatud päevade jooksul.</span><span class="sxs-lookup"><span data-stu-id="1a39e-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="1a39e-171">Kui valite paani **Aadressimuudatused**, kuvatakse uuel leheküljel iga aadressimuudatuse üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="1a39e-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="1a39e-172">Soovi korral saate valida ülemises parempoolses nurgas suvandi **Kaasa tulevased aadressimuudatused**, et kuvada tulevase kuupäevaga aadressimuudatused.</span><span class="sxs-lookup"><span data-stu-id="1a39e-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="1a39e-173">Kui soovite aadressimuudatuste puhul saada teatist või e-kirja, saate toimingupaani vahekaardil **Suvandid** luua uue teatisereegli.</span><span class="sxs-lookup"><span data-stu-id="1a39e-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="1a39e-174">Lisateavet teatisereeglite kohta leiate teemast [Teatisereeglite loomine](/fin-ops-core/fin-ops/get-started/create-alert-rules.md).</span><span class="sxs-lookup"><span data-stu-id="1a39e-174">For more information about alert rules, see [Create alert rules](/fin-ops-core/fin-ops/get-started/create-alert-rules.md).</span></span><br><br>

> <span data-ttu-id="1a39e-175">Kui soovite aadressimuudatuste jaoks konfigureerida töövoogu, saate valida oma teatisereeglis suvandi **Saada väliselt** ning kasutada seejärel ärisündmuse käivitamiseks ja töövoo konfigureerimiseks rakendust Power Automate.</span><span class="sxs-lookup"><span data-stu-id="1a39e-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="1a39e-176">Lisateavet leiate teemast [Teatised ärisündmustena](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md).</span><span class="sxs-lookup"><span data-stu-id="1a39e-176">For more information, see [Alerts as business events](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md).</span></span>
