---
title: Käsitsi loodud töökäsud
description: Selles teemas tutvustatakse, kuidas luua varahalduses käsitsi töökäske.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875608"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="952f5-103">Käsitsi loodud töökäsud</span><span class="sxs-lookup"><span data-stu-id="952f5-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="952f5-104">Töökäskude käsitsi loomiseks on kaks võimalust:</span><span class="sxs-lookup"><span data-stu-id="952f5-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="952f5-105">jaotistes **Kõik töökäsud** või **Aktiivsed töökäsud**</span><span class="sxs-lookup"><span data-stu-id="952f5-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="952f5-106">jaotises **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded** või **Minu töö asukoha hooldusnõuded**</span><span class="sxs-lookup"><span data-stu-id="952f5-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="952f5-107">Töökäsu loomine</span><span class="sxs-lookup"><span data-stu-id="952f5-107">Create work order</span></span>

1. <span data-ttu-id="952f5-108">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="952f5-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="952f5-109">Klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="952f5-109">Click the **New** button.</span></span>

3. <span data-ttu-id="952f5-110">Valige ripploendist **Töökäsu loomine** töökäsu tüüp.</span><span class="sxs-lookup"><span data-stu-id="952f5-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="952f5-111">Vajadusel valige kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="952f5-111">If required, select a description.</span></span>

5. <span data-ttu-id="952f5-112">Valige töökäsule vara ja ka hooldustöö tüüp.</span><span class="sxs-lookup"><span data-stu-id="952f5-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="952f5-113">Kuil valite vara, võib saadaval olla kolm vahekaarti. Vahekaart **Minu varad** sisaldab töö asukohtaga seotud varasid, millele teie (süsteemi sisseloginud töötaja) võite olla määratud (seadistatud jaotises [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="952f5-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="952f5-114">Kui töötajale ei ole jaotises [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md) töö asukohti seadistatud, siis vahekaarti **Minu varad** ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="952f5-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="952f5-115">Vahekaart **Aktiivsed varad** sisaldab kõigi varade loendit, mille vara töötsükli olek on „Aktiivne”.</span><span class="sxs-lookup"><span data-stu-id="952f5-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="952f5-116">Vahekaardil **Varade vaade** kuvatakse töö asukohtade puuvaade ja nendesse asukohtadesse paigaldatud varad.</span><span class="sxs-lookup"><span data-stu-id="952f5-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="952f5-117">Vajadusel valige **Hooldustöö  tüübi variant** ja **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="952f5-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="952f5-118">Vajadusel saate väljal **Teenindustase** töökäsu teenindustaset muuta.</span><span class="sxs-lookup"><span data-stu-id="952f5-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="952f5-119">Valige vastavatele väljadele oodatavad algus- ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="952f5-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="952f5-120">Uue töökäsu loomiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="952f5-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="952f5-121">Vajadusel redigeerige töökäsku jaotises **Kõik töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="952f5-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="952f5-122">Jaotises **Kõik töökäsud** saate töökäsule üksikasjade vaates lisada mitmeid varasid, lisades ridu kiirkaardile **Töökäsu hooldustööd**.</span><span class="sxs-lookup"><span data-stu-id="952f5-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="952f5-123">Vara juures saate valida ainult neid hooldustööde tüüpe, mis on määratletud varale valitud vara tüübi juures.</span><span class="sxs-lookup"><span data-stu-id="952f5-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="952f5-124">Kui olete muutnud vara teenindustaset või vara pärast nende töökäsu juures kasutamist kriitiliselt (vt [Vara teenindustasemed](../setup-for-objects/object-priorities.md) ja [Vara kriitilisused](../setup-for-objects/object-criticalities.md)), ei värskendata vastavalt teenindustaset ega töökäsu kriitilisust.</span><span class="sxs-lookup"><span data-stu-id="952f5-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="952f5-125">Töökäsu kriitilisust arvutatakse uuesti iga kord, kui töökäsule lisatakse või sealt kustutatakse töökäsu rida.</span><span class="sxs-lookup"><span data-stu-id="952f5-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="952f5-126">Jaotise **Kõik töökäsud** üksikasjade vaates > vaates **Päis** > kiirkaardil **Ajakava** saate valida vastutava hooldustöötajate rühma või vastutava hooldustöötaja väljadel **Vastutav rühm** või **Vastutav**.</span><span class="sxs-lookup"><span data-stu-id="952f5-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="952f5-127">Neid sätteid saab muuta seni, kuni töökäsk on aktiivne, näiteks siis kui töökäsu töötsükli olek muutub.</span><span class="sxs-lookup"><span data-stu-id="952f5-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="952f5-128">Töökäsu loomisel tehtud automaatne valik põhineb jaotise **Vastutavad hooldustöötajad** seadistusel.</span><span class="sxs-lookup"><span data-stu-id="952f5-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="952f5-129">Kui lisate või eemaldate töökäsu töid pärast töökäsu loomist ja väljad **Vastutav rühm** ja **Vastutav** on töökäsu värskendamise ajal tühjad, otsib varahaldus seadistuse vormil võimalikku vastet vastutavale hooldustöötajate rühmale või vastutavale hooldustöötajale.</span><span class="sxs-lookup"><span data-stu-id="952f5-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="952f5-130">Kui väli **Vastutav rühm** või väli **Vastutav** on töökäsu värskendamisel juba täidetud, siis muudatusi ei tehta.</span><span class="sxs-lookup"><span data-stu-id="952f5-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="952f5-131">Jaotises **Hoolduse olek** saate teha arvutusi, et saada ülevaade sissetulevate ja lõpetatud töökäskude töökoormusest.</span><span class="sxs-lookup"><span data-stu-id="952f5-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="952f5-132">Kasutage kiirkaardil **Rea üksikasjad** välju **Laiuskraad** ja **Pikkuskraad**, et lisada töökäsu tööl valitud varale geograafilised koordinaadid.</span><span class="sxs-lookup"><span data-stu-id="952f5-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="952f5-133">Loo seotud töökäsk</span><span class="sxs-lookup"><span data-stu-id="952f5-133">Create related work order</span></span>

<span data-ttu-id="952f5-134">Võite luua seotud töökäsu olemasolevale töökäsule, kui näiteks soovite töötada peamise ja sekundaarsete töökäskudega.</span><span class="sxs-lookup"><span data-stu-id="952f5-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="952f5-135">Uus töökäsk põhineb olemasolevast töökäsust pärit töökäsu tööl.</span><span class="sxs-lookup"><span data-stu-id="952f5-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="952f5-136">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="952f5-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="952f5-137">Valige töökäsk, millele soovite teha seotud töökäsku.</span><span class="sxs-lookup"><span data-stu-id="952f5-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="952f5-138">Klõpsake suvandil **Seotud töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="952f5-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="952f5-139">Valige rippdialoogis **Loo seotud töökäsk** see töökäsu töö väljal **Töökäsu töö**, millele soovite seotud töökäsku luua.</span><span class="sxs-lookup"><span data-stu-id="952f5-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="952f5-140">Valige hooldustöö tüüp väljal **Hooldustöö tüüp** ja vajadusel seotud hooldustöö  tüübi variant ning vahetage väljadel **Hooldustöö  tüübi variant** ja **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="952f5-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="952f5-141">Kui see on esimene seotud töökäsk, mille teete, klõpsake raadionuppu **Uus töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="952f5-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="952f5-142">Valige vastavatel väljadel **Töökäsu tüüp** ja **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="952f5-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="952f5-143">Vajadusel muutke väljal **Teenindustase** töökäsu teenindustaset.</span><span class="sxs-lookup"><span data-stu-id="952f5-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="952f5-144">Sisestage vastavatele väljadele oodatavad algus- ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="952f5-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="952f5-145">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="952f5-145">Click **OK**.</span></span> <span data-ttu-id="952f5-146">Uut seotud töökäsku kuvatakse loendis **Kõik töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="952f5-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="952f5-147">Kui loote seotud töökäsu töökäsule, millel juba on seotud töökäske, võite lisada töökäsu töö juba soetud töökäsule.</span><span class="sxs-lookup"><span data-stu-id="952f5-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="952f5-148">Selleks klõpsake etapis 6 raadionuppu **Lisa seotud töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="952f5-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="952f5-149">Seejärel valite seotud töökäsu, millele soovite lisada uut töökäsu tööd.</span><span class="sxs-lookup"><span data-stu-id="952f5-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="952f5-150">Redigeerige vajadusel välju **Teenindustase**, **Oodatav algus** ja **Oodatav lõpp** ning klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="952f5-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="952f5-151">Töökäsu töö lisatakse olemasolevale seotud töökäsule.</span><span class="sxs-lookup"><span data-stu-id="952f5-151">The work order job is added to the existing related work order.</span></span>


![Joonis 1](media/03-work-orders.png)

<span data-ttu-id="952f5-153">**Märkus:** kui olete seadistanud seotud töökäsu maski jaotise **Varahalduse parameetrid** > **Töökäsud** lingi > väljal **Seotud töökäsu mask**, luuakse töökäsu ID-d vastavalt maski seadistusele.</span><span class="sxs-lookup"><span data-stu-id="952f5-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="952f5-154">Kui seotud töökäsu maski ei ole seadistatud, kasutatakse seotud töökäskudele järgmist saadaolevat töökäsu ID-d.</span><span class="sxs-lookup"><span data-stu-id="952f5-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="952f5-155">Töökäsu kopeerimine</span><span class="sxs-lookup"><span data-stu-id="952f5-155">Copy work order</span></span>

<span data-ttu-id="952f5-156">Võimalik on luua olemasolevast töökäsust kiiresti uus töökäsk.</span><span class="sxs-lookup"><span data-stu-id="952f5-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="952f5-157">Selline töökäskudega töötamine erineb hoolduskavade põhjal töökäskude loomisest.</span><span class="sxs-lookup"><span data-stu-id="952f5-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="952f5-158">See on kasulik näiteks siis, kui teil on töökäsk, mis sisaldab palju töökäsu töid mitmete erinevate varade töödega, mis tuleksid teostada regulaarsete intervallidega.</span><span class="sxs-lookup"><span data-stu-id="952f5-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="952f5-159">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="952f5-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="952f5-160">Valige töökäsk, mille sisu soovite kopeerida.</span><span class="sxs-lookup"><span data-stu-id="952f5-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="952f5-161">Klõpsake suvandil **Kopeeri töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="952f5-161">Click **Copy work order**.</span></span> <span data-ttu-id="952f5-162">Kuvatakse valitud töökäsu seadistust valitud töökäsust.</span><span class="sxs-lookup"><span data-stu-id="952f5-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="952f5-163">Vajadusel saate mõnda nendest väljadest redigeerida.</span><span class="sxs-lookup"><span data-stu-id="952f5-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="952f5-164">Uue töökäsu loomiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="952f5-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="952f5-165">Vajadusel redigeerige töökäsku jaotises **Kõik töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="952f5-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="952f5-166">Kui töökäsk on loodud, kopeeritakse osad andmed otse olemasolevast töökäsust.</span><span class="sxs-lookup"><span data-stu-id="952f5-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="952f5-167">Prognooside, tööriistade, hoolduse kontrollnimekirjade, töö asukohtade, aadresside ja ajastamise infot ei kopeerita, vaid lähtestatakse kehtivast varahalduse seadistusest.</span><span class="sxs-lookup"><span data-stu-id="952f5-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="952f5-168">See tähendab, et kui ajavahemikult esimese töökäsu loomisest kuni töökäsu koopia tegemiseni tehti aeg-ajalt nendes andmetes muudatusi, sisalduvad need muudatused uues loodud töökäsus.</span><span class="sxs-lookup"><span data-stu-id="952f5-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="952f5-169">Näited prognoosi muudatustest või värskendatud hoolduse kontrollnimekirjast.</span><span class="sxs-lookup"><span data-stu-id="952f5-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Joonis 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="952f5-171">Töökäsu loomine hooldusnõude põhjal</span><span class="sxs-lookup"><span data-stu-id="952f5-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="952f5-172">Klõpsake **Varahaldus** > **Üldine** > **Hooldusnõuded** > **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded**.</span><span class="sxs-lookup"><span data-stu-id="952f5-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="952f5-173">Valige hooldusnõuded, millele soovite luua töökäsu, ning klõpsake **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="952f5-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="952f5-174">Klõpsake jaotises **Kõik nõuded** valikut **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="952f5-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="952f5-175">Täitke ripploend **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="952f5-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="952f5-176">Kui hooldusnõudes on valitud hooldustöö tüüp, saate valida vajadusel teise hooldustöö tüübi, kui loote töökäsu.</span><span class="sxs-lookup"><span data-stu-id="952f5-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="952f5-177">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="952f5-177">Click **OK**.</span></span> <span data-ttu-id="952f5-178">Näete teadet, mis teavitab teid, et töökäsk on loodud.</span><span class="sxs-lookup"><span data-stu-id="952f5-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="952f5-179">Kui soovite näha millised töökäsud on hooldusnõudega ühendatud, valige hooldusnõue loendist **Kõik hooldustaotlused** või **Aktiivsed hooldustaotlused** ning klõpsake nupul **Töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="952f5-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Joonis 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="952f5-181">Töökäske saab ka automaatselt luua ajastades hoolduskava töid või seadistades varale "Automaatselt loodavaid" hoolduskavasid või hoolduskordi.</span><span class="sxs-lookup"><span data-stu-id="952f5-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="952f5-182">Hooldusnõuetest loodud töökäsud jaotises **Hooldusgraafik** luuakse nii, et hooldusnõuetest on valitud hooldustöö tüübid.</span><span class="sxs-lookup"><span data-stu-id="952f5-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

