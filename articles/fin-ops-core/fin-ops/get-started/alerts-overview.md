---
title: Teatiste ülevaade
description: See teema annab üldteavet teatiste kohta. Teatisi saate kasutada, et olla kursis sündmustega, mida soovite tööpäeva jooksul jälgida.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a42e836c0b72798de3375c169e45b121debd55ec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191266"
---
# <a name="alerts-overview"></a><span data-ttu-id="cb7c8-104">Teatiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="cb7c8-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="cb7c8-105">Teatiste kohta</span><span class="sxs-lookup"><span data-stu-id="cb7c8-105">About alerts</span></span>
<span data-ttu-id="cb7c8-106">Teatised moodustavad süsteemis kriitiliste sündmuste teadete süsteemi.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="cb7c8-107">Teatisi saate kasutada, et olla kursis sündmustega, mida soovite tööpäeva jooksul jälgida.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="cb7c8-108">Saate hõlpsalt luua omi teatisereegleid tähtaja ületanud tarnete, kustutatud tellimuste, muutuvate hindade või muude reageerimist nõudvate sündmuste kohta.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="cb7c8-109">Ettevõtte ressursiplaanimises (ERP) on toodud mitmesuguseid tavapäraseid stsenaariumeid, mille puhul teatiste funktsiooni kasutada saab.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="cb7c8-110">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="cb7c8-111">Stsenaarium 1: teatisereegli loomine uute müügitellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="cb7c8-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="cb7c8-112">Avage leht **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="cb7c8-113">Valige toimingupaani vahekaardil **Suvandid** rühmas **Anna ühiskasutusse** valik **Loo kohandatud teatis**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="cb7c8-114">Valige dialoogiboksi **Loo teatisereegel** kiirkaardi **Teavita mind, kui** väljalt **Sündmus** suvand **On loodud uus kirje**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="cb7c8-115">Stsenaarium 2: teatise loomine tarnekuupäeva edasilükkumise kohta</span><span class="sxs-lookup"><span data-stu-id="cb7c8-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="cb7c8-116">Avage leht **Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="cb7c8-117">Ostutellimus üksikasjade vaatamiseks valige ostutellimuse ID.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="cb7c8-118">Laiendage kiirkaarti **Ostutellimuse päis**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="cb7c8-119">Valige toimingupaani vahekaardil **Suvandid** rühmas **Anna ühiskasutusse** valik **Loo kohandatud teatis**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="cb7c8-120">Valige dialoogiboksi **Loo teatisereegel** kiirkaardi **Teavita mind, kui** väljalt **Väli** suvand **Tarnekuupäev**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="cb7c8-121">Valige väljal **Sündmus** suvand **on edasi lükatud**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="cb7c8-122">Pärast dialoogiboksi **Loo teatisereegel** sulgemist kuvatakse teie reegel lehel **Halda teatisereegleid**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="cb7c8-123">Lehte **Halda teatisereegleid** saab kasutada olemasolevate teatisereeglite värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="cb7c8-124">Näiteks saab muuta sündmuse käivitajaid, värskendada sündmuse teatiseid ja aegumiskuupäevi.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="cb7c8-125">Lehe **Halda teatisereegleid** avamiseks kasutage toimingupaani vahekaardi **Suvandid** nuppu **Teavita mind**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="cb7c8-126">Mis toimub teatisereegli loomisel?</span><span class="sxs-lookup"><span data-stu-id="cb7c8-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="cb7c8-127">Teatisereeglite loomisel saate eelmääratletud sündmuse konkreetse väljaga seostada.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="cb7c8-128">Näiteks, kui väljal määratud kuupäev saabub või välja sisu muutub.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="cb7c8-129">Teise võimalusena saate sündmuse seostada kindlal leheküljel olevate kirjetega.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="cb7c8-130">Näiteks kirje loomisel või kustutamisel.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="cb7c8-131">Kui valitud sündmus toimub välja puhul või lehel oleva kirje puhul, saadetakse teile teatis.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="cb7c8-132">Näiteks loote reegli, mille konkreetse ostutellimuse rea välja **Tarnekuupäev** seostate sündmusega **tähtajast on möödas**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="cb7c8-133">Määrate ajavahemikuks viis päeva.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-133">You set the time frame to five days.</span></span> <span data-ttu-id="cb7c8-134">Sel juhul saadetakse teatis viis päeva pärast ostutellimuse rea tarnekuupäeva.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="cb7c8-135">Lisaks saate teatisereegleid tingimuste seadistamisega täpsustada.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="cb7c8-136">Näiteks võite saada teatiseid konkreetse hankija kontode jaoks loodud uute ostutellimuste kohta.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="cb7c8-137">Teatise ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="cb7c8-137">Preparing for an alert</span></span>

<span data-ttu-id="cb7c8-138">Enne teatisreegli loomist otsustage, millal või milliste olukordades te teatisi saada soovite.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="cb7c8-139">Teades, millise sündmuse kohta te teatist soovite, saate otsida lehe, millel kuvatakse teatist käivitava sündmuse andmed.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="cb7c8-140">Sündmuseks võib olla saabuv kuupäev või teatud toimuv muudatus.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="cb7c8-141">Seega peate leidma lehe, kus kuvatakse kas määratud kuupäev, muudetud väli või uus loodud kirje.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="cb7c8-142">Alles seda teades saate luua teatisereegli.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="cb7c8-143">Teatisereegli osad</span><span class="sxs-lookup"><span data-stu-id="cb7c8-143">Components of an alert rule</span></span>

<span data-ttu-id="cb7c8-144">Teatisereegel koosneb viiest osast.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-144">An alert rule has five components:</span></span>

- <span data-ttu-id="cb7c8-145">**Sündmus** – teatisereeglit käivitav sündmus saab olla kas saabuv kuupäev või teatud toimuv muudatus.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="cb7c8-146">Sündmused saate määrata dialoogiboksi **Loo teatise reegel** kiirkaardil **Töö oleku muudatuste kohta meiliteatiste saatmine**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="cb7c8-147">**Tingimus** – dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisel juhul** saate valida tingimuse ulatuse, kontrollimaks, millal teid sündmustest teavitatakse.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="cb7c8-148">Saate reeglit rakendada kas ainult praegusele kirjele või kõigile lehel nähtavatele kirjetele.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="cb7c8-149">Kui reegel on juriidiliste isikute ülene, määrake suvandi **Organisatsiooniülene** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="cb7c8-150">**Reegli aegumine** – dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind kuni** saate määrata, kui kaua teatisereegel aktiivne peaks olema.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="cb7c8-151">**Sisu** – dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisega** saate määrata teema ja sõnumi teksti, mida teatiste puhul peaks kasutatama.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="cb7c8-152">**Kasutaja** – dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavitatav** saate määrata, milline kasutaja peaks teatiseid saama.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="cb7c8-153">Vaikimisi on valitud teie kasutaja ID.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb7c8-154">See valik on piiratud organisatsiooni administraatoritele.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-154">This option is restricted to organization administrators.</span></span>

## <a name="email-notifications-from-alerts"></a><span data-ttu-id="cb7c8-155">Teadete meiliteatised</span><span class="sxs-lookup"><span data-stu-id="cb7c8-155">Email notifications from alerts</span></span>

<span data-ttu-id="cb7c8-156">Teadete meiliteatised pole veel lubatud.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-156">Email notifications from alerts are not yet enabled.</span></span> <span data-ttu-id="cb7c8-157">See lubatakse tulevases värskenduses.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-157">This will be enabled in a future update.</span></span>

## <a name="videos"></a><span data-ttu-id="cb7c8-158">Videod</span><span class="sxs-lookup"><span data-stu-id="cb7c8-158">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="cb7c8-159">Kuidas kasutada teatisi filtreeritud andmete jälgimiseks</span><span class="sxs-lookup"><span data-stu-id="cb7c8-159">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="cb7c8-160">Video [Kuidas kasutada teatisi filtreeritud andmete jälgimiseks](https://youtu.be/ZYKMcv6kl9s) (eespool näidatud) on lisatud [Finance and Operationsi esitusloendisse](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), mis on saadavalYouTube'is.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-160">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="cb7c8-161">Teatise reegli valikud</span><span class="sxs-lookup"><span data-stu-id="cb7c8-161">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3E4PV]

<span data-ttu-id="cb7c8-162">Video [Teatise reegli valikud](https://youtu.be/cpzimwOjicM) (eespool näidatud) on lisatud [Finance and Operationsi esitusloendisse](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), mis on saadaval YouTube'is.</span><span class="sxs-lookup"><span data-stu-id="cb7c8-162">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

