---
title: Käsitsi loodud töökäsud
description: Selles teemas tutvustatakse, kuidas luua varahalduses käsitsi töökäske.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2652458a5fea9e46b8b68d3b197d2ccb1385731d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811736"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="0d0f9-103">Käsitsi loodud töökäsud</span><span class="sxs-lookup"><span data-stu-id="0d0f9-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="0d0f9-104">Töökäskude käsitsi loomiseks on kaks võimalust:</span><span class="sxs-lookup"><span data-stu-id="0d0f9-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="0d0f9-105">Lehel **Kõik töökäsud** või **Aktiivsed töökäsud**</span><span class="sxs-lookup"><span data-stu-id="0d0f9-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="0d0f9-106">Lehel **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded** või **Minu töö asukoha hooldusnõuded**</span><span class="sxs-lookup"><span data-stu-id="0d0f9-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="0d0f9-107">Töökäsu loomine</span><span class="sxs-lookup"><span data-stu-id="0d0f9-107">Create work order</span></span>

1. <span data-ttu-id="0d0f9-108">Valige **Varahaldus** > **Ühine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0d0f9-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-109">Select **New**.</span></span>

3. <span data-ttu-id="0d0f9-110">Valige töökäsu tüüp dialoogi **Töökäsu loomine** väljal **Töökäsu tüüp**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="0d0f9-111">Vajadusel valige **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="0d0f9-112">Valige vara väljal **Vara**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="0d0f9-113">Kui valite vara, võivad rippmenüüs **Vara** saadaval olla kolm vahekaarti.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="0d0f9-114">**Aktiivsed varad** – see vahekaart sisaldab kõigi varade loendit, mille vara töötsükli olek on „Aktiivne”.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="0d0f9-115">**Varade vaade** – sellel vahekaardil kuvatakse töö asukohtade puuvaade ja neisse paigaldatud varad.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="0d0f9-116">**Minu varad** – see vahekaart sisaldab varasid, mis on seotud töö asukohtadega, mida teile (töötajale, kes on süsteemi sisse loginud) võidakse eraldada.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="0d0f9-117">(Lisateavet seadistuse kohta vt teemast [Hooldustöötajad ja töötajate grupid](../setup-for-objects/workers-and-worker-groups.md).) Kui töötajale pole töö asukohti seadistatud valikus [Hooldustöötajad ja töötajate grupid](../setup-for-objects/workers-and-worker-groups.md), pole vahekart **Minu varad** saadaval.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="0d0f9-118">Valige väljal **Hooldustöö tüüp** töökäsu jaoks hooldustöö töö tüüp.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="0d0f9-119">Vajadusel valige **Hooldustöö  tüübi variant** ja **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="0d0f9-120">Vajadusel saate väljal **Teenindustase** töökäsu teenindustaset muuta.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="0d0f9-121">Valige seotud väljadel **Eeldatud alguskuupäev** ja **Eeldatav lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="0d0f9-122">Töökäsu loomiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="0d0f9-123">Loendilehel **Kõik töökäsud** saate vajadusel töökäsku redigeerida.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="0d0f9-124">Pidage meeles järgmiseid punkte.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-124">Note the following points:</span></span>

- <span data-ttu-id="0d0f9-125">Loendilehe **Kõik töökäsud** üksikasjalikus vaates saatetöökäsule lisada mitu vara, kui lisate read kiirkaardile **Töökäsu hooldustööd**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="0d0f9-126">Vara juures saate valida ainult neid hooldustööde tüüpe, mis on määratletud varale valitud vara tüübi juures.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="0d0f9-127">Kui muudate pärast töökäsu vara kasutamist vara teenusetaset või vara kriitilisust, ei värskendata selle töökäsu teenusetaset või kriitilisust vastavalt.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="0d0f9-128">Lisateavet teenusetasemete ja kriitilisuse kohta vt teemast [Vara teenusetasemed](../setup-for-objects/object-priorities.md) ning [Varade kriitilisuse tüübid](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="0d0f9-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="0d0f9-129">Töökäsu kriitilisus arvutatakse ümber iga kord, kui töökäsu rida lisatakse või kustutatakse töökäsult.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="0d0f9-130">Üksikasjalik vaate **Kõik töökäsud** > vahekaardi **Päis** > kiirkaardi **Graafik** jaotises **Vastutav rühm** või väljal **Vastutav**, saate valida vastutava hooldustöötajate rühma või vastutava hooldustöötaja.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="0d0f9-131">Neid sätteid saab muuta, kui töökäsk on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="0d0f9-132">Näiteks saab neid muuta, kui töökäsu töötsükli olek muutub.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="0d0f9-133">Töökäsu loomisel tehtud automaatne valik põhineb lehe **Vastutavad hooldustöötajad** seadistusel.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="0d0f9-134">Kui lisate või eemaldate töökäsu töid pärast töökäsu loomist ja väljad **Vastutav rühm** ja **Vastutav** on töökäsu värskendamise ajal tühjad, proovib varahaldus otsida vastutava hooldustöötajate rühma või vastutavat töötaja võimalikku vastet seadistuse lehel.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="0d0f9-135">Kui väli **Vastutav rühm** või **Vastutav** on töökäsu värskendamisel juba seadistatud, siis muudatusi ei tehta.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="0d0f9-136">Lisateavet vastutavate hooldustöötajate ja töötajate rühma kohta vt teemast [Vastutavad hooldustöötajad](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="0d0f9-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="0d0f9-137">Lehel [Hoolduse olek](../controlling-and-reporting/maintenance-status.md) saate teha arvutusi, et saada ülevaade sissetulevate ja lõpetatud töökäskude töökoormusest.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="0d0f9-138">Lehe **Kõik töökäsud** üksikasjaliku vaate kiirkaardil **Rea üksikasjad** saate töökäsu töös valitud vara geograafiliste koordinaatide lisamiseks kasutada välju **Laiuskraad** ja **Pikkuskraad**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="0d0f9-139">Loo seotud töökäsk</span><span class="sxs-lookup"><span data-stu-id="0d0f9-139">Create related work order</span></span>

<span data-ttu-id="0d0f9-140">Saate luua töökäsu, mis on seotud olemasoleva töökäsuga.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="0d0f9-141">Funktsioon on kasulik näiteks esmaste ja teisejärguliste töökäskudega töötamise puhul.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="0d0f9-142">Uus töökäsk põhineb olemasolevast töökäsust pärit töökäsu tööl.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="0d0f9-143">Valige **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0d0f9-144">Looge töökäsk, millel luua seotud töökäsk.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="0d0f9-145">Tehke tegumiriba vahekaardi **Töökäsk** jaotises **Uus** valik **Seotud töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="0d0f9-146">Valige dialoogi **Seotud töökäsu loomine** väljal **Töökäsu töö** töökäsu töö, millele luua seotud töökäsk.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="0d0f9-147">Väljal **Hooldustöö tüüp** valige hooldustöö tüüp.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="0d0f9-148">Vajadusel valige seotud hooldustöö tüübi variant ja vahetus väljadel **Hooldustöö tüübi variant** ja **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="0d0f9-149">Kui see töökäsk on esimene seotud töökäsk, mis on valitud töökäsu jaoks loodud, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="0d0f9-150">Tehke valik **Uus töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="0d0f9-151">Valige töökäsu tüüpväljal **Töökäsu tüüp**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="0d0f9-152">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="0d0f9-153">Vajadusel muutke töökäsu teenusetaset väljal **Teenusetase**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="0d0f9-154">Valige algus-ja lõppkuupäevad väljal **Eeldatav algus** ja **Eeldatav lõpp** .</span><span class="sxs-lookup"><span data-stu-id="0d0f9-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="0d0f9-155">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-155">Select **OK**.</span></span> <span data-ttu-id="0d0f9-156">Uus seotud töökäsk kuvatakse loendilehel **Kõik töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="0d0f9-157">Kui töökäsul, millele loote seotud töökäsu, on seotud töökäsud juba olemas, järgige uue töökäsu töö lisamiseks olemasolevale seotud töökäsule järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="0d0f9-158">Valige **Lisa seotud töökäsule**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="0d0f9-159">Valige väljal **Töökäsk** seotud töökäsk, millel lisada uus töökäsk.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="0d0f9-160">Vajadusel muutke töökäsu teenusetaset väljal **Teenusetase**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="0d0f9-161">Vajadusel muutke eeldatavad algus- ja lõppkuupäevad väljadel **Eeldatav algus** ja **Eeldatav lõpp**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="0d0f9-162">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-162">Select **OK**.</span></span> <span data-ttu-id="0d0f9-163">Töökäsu töö lisatakse olemasolevale seotud töökäsule.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="0d0f9-164">Alloleval joonisel kuvatakse dialoogi **Seotud töökäsu loomine** näide.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Joonis 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="0d0f9-166">Kui olete seadistanud seotud töökäsu maski vahekaardi **Varahalduse parameetrid** > **Töökäsud** > väljal **Seotud töökäsu mask**, luuakse töökäsu ID-d vastavalt maski seadistusele.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="0d0f9-167">Kui seotud töökäsu maski ei ole seadistatud, kasutatakse seotud töökäskudele järgmist saadaolevat töökäsu ID-d.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="0d0f9-168">Töökäsu kopeerimine</span><span class="sxs-lookup"><span data-stu-id="0d0f9-168">Copy a work order</span></span>

<span data-ttu-id="0d0f9-169">Saate olemasolevast töökäsust kiiresti luua uue töökäsu.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="0d0f9-170">Sel viisil töökäskudega töötamine erineb töökäskude loomisest [hooldusgraafikute](../preventive-and-reactive-maintenance/maintenance-plans.md) põhjal.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="0d0f9-171">See on kasulik näiteks siis, kui töökäsk sisaldab mitut töökäsu tööd ja erinevate varade mitmed tööd tuleb lõpule viia regulaarsete intervallidega.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="0d0f9-172">Valige **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0d0f9-173">Valige töökäsk, mille sisu soovite kopeerida.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="0d0f9-174">Tehke tegumiribal > vahekaardi **Töökäsk** > jaotises **Uus** valik **Kopeeri töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="0d0f9-175">Kuvatakse valitud töökäsu seadistust valitud töökäsust.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="0d0f9-176">Vajadusel saate mõnda nendest väljadest redigeerida.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="0d0f9-177">Uue töökäsu loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="0d0f9-178">Loendilehel **Kõik töökäsud** saate vajadusel töökäsku redigeerida.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="0d0f9-179">Kui töökäsk on loodud, kopeeritakse osad andmed otse olemasolevast töökäsust.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="0d0f9-180">Teavet prognooside, tööriistade, hoolduse kontrollnimekirjade, töö asukoha, aadresside ja ajastamise kohta ei kopeerita.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="0d0f9-181">Selle asemel lähtestatakse see varahalduse praegusest seadistusest.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="0d0f9-182">Seega, kui seda teavet muudeti esimese töökäsu loomise ja töökäsu koopia tegemise aja vahel, kaasatakse muudatused uude töökäsku.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="0d0f9-183">Näitena võib tuua prognooside muudatused ja hoolduse kontrollnimekirjade värskendused.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="0d0f9-184">Alloleval joonisel kuvatakse dialoogi **Töökäsu kopeerimine** näide.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Joonis 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="0d0f9-186">Töökäsu loomine hooldusnõude põhjal</span><span class="sxs-lookup"><span data-stu-id="0d0f9-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="0d0f9-187">Valige **Varahaldus** > **Ühine** > **Hooldusnõuded** > **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="0d0f9-188">Valige hooldusnõuded, millele soovite luua töökäsu, ning klõpsake **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="0d0f9-189">Tehke tegumiriba > vahekaardi **Hooldusnõue** > jaotises **Uus** valik **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="0d0f9-190">Seadistage väljad dialoogis **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="0d0f9-191">Kui hooldusnõudes on valitud hooldustöö tüüp, saate valida vajadusel teise hooldustöö tüübi, kui loote töökäsu.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="0d0f9-192">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-192">Select **OK**.</span></span> <span data-ttu-id="0d0f9-193">Teates teavitatakse teid töökäsu loomisest.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="0d0f9-194">Et vaadata, millised töökäsud on hooldusnõudega ühendatud, valige hooldusnõue loendilehel **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="0d0f9-195">Seejärel tehke vahekaardi **Hooldusnõue** jaotise **Kuva** tegumiribal valik **Töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="0d0f9-196">Allolevalt joonisel kuvatakse dialoogis **Töökäsu loomine** näide.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Joonis 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="0d0f9-198">Kui soovite, et töökäsud loodaks automaatselt, saate vara hoolduskava töid ajastada või seadistada [hoolduskavade](../preventive-and-reactive-maintenance/maintenance-plans.md) või [hoolduskordade](../preventive-and-reactive-maintenance/maintenance-rounds.md) automaatse loomise.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="0d0f9-199">Hooldusnõuetest loodud töökäskudel on loendilehel **Kogu hooldusgraafik** hooldustööde tüübid, mis on hooldusnõuetes valitud.</span><span class="sxs-lookup"><span data-stu-id="0d0f9-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

