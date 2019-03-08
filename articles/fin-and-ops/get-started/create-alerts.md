---
title: Teatisereeglite loomine
description: Selles teemas antakse teavet teatiste kohta ja selgitatakse, kuidas luua teatisereeglit selliselt, et saaksite teavitusi selliste sündmuste kohta nagu saabuv kuupäev või konkreetne muudatus.
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: cbf4917424e72a70a6d513b5daf45f6bf9cd57c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "329409"
---
# <a name="create-alert-rules"></a><span data-ttu-id="e3070-103">Teatisereeglite loomine</span><span class="sxs-lookup"><span data-stu-id="e3070-103">Create alert rules</span></span>

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a><span data-ttu-id="e3070-104">Alustamine</span><span class="sxs-lookup"><span data-stu-id="e3070-104">Getting started</span></span>

<span data-ttu-id="e3070-105">Enne teatisreegli loomist otsustage, millal või milliste olukordades te teatisi saada soovite.</span><span class="sxs-lookup"><span data-stu-id="e3070-105">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="e3070-106">Teades, millise sündmuse kohta te teatist soovite, saate otsida rakenduses Microsoft Dynamics 365 for Finance and Operations lehe, millel kuvatakse teatist käivitava sündmuse andmed.</span><span class="sxs-lookup"><span data-stu-id="e3070-106">When you know which event you want to be notified about, in Microsoft Dynamics 365 for Finance and Operations find the page where the data that causes that event appears.</span></span> <span data-ttu-id="e3070-107">Sündmuseks võib olla saabuv kuupäev või teatud toimuv muudatus.</span><span class="sxs-lookup"><span data-stu-id="e3070-107">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="e3070-108">Seega peate leidma lehe, kus kuvatakse kas määratud kuupäev, muudetud väli või uus loodud kirje.</span><span class="sxs-lookup"><span data-stu-id="e3070-108">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="e3070-109">Alles seda teades saate luua teatisereegli.</span><span class="sxs-lookup"><span data-stu-id="e3070-109">After you have this information, you can create the alert rule.</span></span>

<span data-ttu-id="e3070-110">Teatisereegli loomisel saate määrata kriteeriumid, mis peavad olema täidetud enne teatise käivitamist.</span><span class="sxs-lookup"><span data-stu-id="e3070-110">When you create an alert rule, you define the criteria that must be met before an alert is triggered.</span></span> <span data-ttu-id="e3070-111">Mõelge kriteeriumist kui vastavusest sündmuse toimumise ja teatud tingimuste täitmise vahel.</span><span class="sxs-lookup"><span data-stu-id="e3070-111">You can think of criteria as a match between the occurrence of an event and the fulfillment of specific conditions.</span></span> <span data-ttu-id="e3070-112">Sündmuse toimumisel hakkab süsteem rakenduses Finance and Operations seatud tingimuste põhjal kontrolli läbi viima.</span><span class="sxs-lookup"><span data-stu-id="e3070-112">When an event occurs, the system starts to perform a check according to the conditions that are set up in Finance and Operations.</span></span>

## <a name="events"></a><span data-ttu-id="e3070-113">Sündmused</span><span class="sxs-lookup"><span data-stu-id="e3070-113">Events</span></span>

<span data-ttu-id="e3070-114">Teatisereeglit käivitav sündmus saab olla kas saabuv kuupäev või teatud toimuv muudatus.</span><span class="sxs-lookup"><span data-stu-id="e3070-114">The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="e3070-115">Sündmuste käivitajad on määratud dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind, kui**.</span><span class="sxs-lookup"><span data-stu-id="e3070-115">Triggers for events are defined on the **Alert me when** FastTab of the **Create alert rule** dialog box.</span></span> <span data-ttu-id="e3070-116">Konkreetsel väljal saadaolevad sündmused sõltuvad valitud käivitajast.</span><span class="sxs-lookup"><span data-stu-id="e3070-116">The events that are available for a particular field depend on the trigger that is selected.</span></span>

<span data-ttu-id="e3070-117">Näiteks, kui seadistate teatisereegli väljale **Alguskuupäev**, on tähtajalised sündmused asjakohased.</span><span class="sxs-lookup"><span data-stu-id="e3070-117">For example, if you're setting up an alert rule for the **Start date** field, due date events are appropriate.</span></span> <span data-ttu-id="e3070-118">Seetõttu on selle välja puhul saadaval sündmuse tüüp **tähtaeg on**.</span><span class="sxs-lookup"><span data-stu-id="e3070-118">Therefore, the **is due in** event type is available for that field.</span></span> <span data-ttu-id="e3070-119">Samas näiteks välja **Kulukeskus** puhul pole tähtajaline sündmus asjakohane.</span><span class="sxs-lookup"><span data-stu-id="e3070-119">However, for a field such as **Cost center**, a due date event isn't appropriate.</span></span> <span data-ttu-id="e3070-120">Seetõttu pole saadaval sündmuse tüüpi **tähtaeg on**.</span><span class="sxs-lookup"><span data-stu-id="e3070-120">Therefore, the **is due in** event type isn't available.</span></span> <span data-ttu-id="e3070-121">Selle asemel on saadaval sündmuse tüüp **on muutunud**.</span><span class="sxs-lookup"><span data-stu-id="e3070-121">Instead, the **has changed** event type is available.</span></span>

## <a name="event-types"></a><span data-ttu-id="e3070-122">Sündmuste tüübid</span><span class="sxs-lookup"><span data-stu-id="e3070-122">Event types</span></span>

<span data-ttu-id="e3070-123">Toimuda võivad kolme tüüpi sündmused.</span><span class="sxs-lookup"><span data-stu-id="e3070-123">Three types of events can occur:</span></span>

- <span data-ttu-id="e3070-124">**Loomis- ja kustutamistüüpi sündmused** – need sündmused käivitavad teatise juhul, kui kirje luuakse või kustutatakse.</span><span class="sxs-lookup"><span data-stu-id="e3070-124">**Create-type and delete-type events** – These events trigger an alert when a record is created or deleted.</span></span>
- <span data-ttu-id="e3070-125">**Värskendamistüüpi sündmused** – need sündmused käivitavad teatise, kui andmed kindlal väljal muutuvad.</span><span class="sxs-lookup"><span data-stu-id="e3070-125">**Update-type events** – These events trigger an alert when the data in a specific field changes.</span></span>
- <span data-ttu-id="e3070-126">**Tähtaja-tüüpi sündmused** – need sündmused käivitavad teatise, kui kuupäev saabub.</span><span class="sxs-lookup"><span data-stu-id="e3070-126">**Due date-type events** – These events trigger an alert when a date arrives.</span></span>
    
<span data-ttu-id="e3070-127">Toimuvad muudatused saab käivitada kasutaja.</span><span class="sxs-lookup"><span data-stu-id="e3070-127">Changes that occur can be initiated by a user.</span></span> <span data-ttu-id="e3070-128">Näiteks kasutaja muudab ostutellimuse tarnekuupäeva.</span><span class="sxs-lookup"><span data-stu-id="e3070-128">For example, a user changes the delivery date of a purchase order.</span></span> <span data-ttu-id="e3070-129">Teise võimalusena võivad muudatused ilmneda protsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="e3070-129">Alternatively, changes can occur as part of a process.</span></span> <span data-ttu-id="e3070-130">Näiteks muutub lehe väli **Olek**, et peegeldada süsteemi mitmesuguste protsesside töötsüklit.</span><span class="sxs-lookup"><span data-stu-id="e3070-130">For example, the **Status** field on a page changes to reflect the life cycle of various processes in the system.</span></span>

## <a name="conditions"></a><span data-ttu-id="e3070-131">Tingimused</span><span class="sxs-lookup"><span data-stu-id="e3070-131">Conditions</span></span>

<span data-ttu-id="e3070-132">Dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisel juhul** saate kasutada tingimusi, kontrollimaks, millal teid sündmustest teavitatakse.</span><span class="sxs-lookup"><span data-stu-id="e3070-132">On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can use conditions to control when you're alerted about events.</span></span>

<span data-ttu-id="e3070-133">Näiteks saate määrata, et süsteem peaks teid teavitama, kui ostutellimuste olekut muudetakse, kuid ainult juhul, kui olek on kooskõlas määratud tingimustega.</span><span class="sxs-lookup"><span data-stu-id="e3070-133">For example, you can specify that the system should alert you when the status of purchase orders changes, but only if the status matches a specific set of conditions.</span></span> <span data-ttu-id="e3070-134">Täpsemalt, soovite saada teatist, kui ostutellimuse olekuks määratakse **Saadud**.</span><span class="sxs-lookup"><span data-stu-id="e3070-134">Specifically, you want to be alerted when the status of a purchase order is set to **Received**.</span></span> <span data-ttu-id="e3070-135">See olekumuudatus on sündmus, mis käivitab teatise.</span><span class="sxs-lookup"><span data-stu-id="e3070-135">This change in status is the event that triggers the alert.</span></span>

<span data-ttu-id="e3070-136">Seejärel peate otsustama, milliste ostutellimuste kohta te teatisi soovite.</span><span class="sxs-lookup"><span data-stu-id="e3070-136">Next, you must decide which purchase orders you want to be alerted about.</span></span> <span data-ttu-id="e3070-137">Näiteks saate valida ühe järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="e3070-137">For example, you can select one of the following options.</span></span> <span data-ttu-id="e3070-138">Need suvandid määravad teatisereegli tingimused.</span><span class="sxs-lookup"><span data-stu-id="e3070-138">These options define the conditions for the alert rule.</span></span>

- <span data-ttu-id="e3070-139">**Praegu valitud kirje** – saate teatise, kui kindla ostutellimuse olek muutub olekuks **Saadud**.</span><span class="sxs-lookup"><span data-stu-id="e3070-139">**Current selected record** – You receive an alert when the status of a specific purchase order changes to **Received**.</span></span>
- <span data-ttu-id="e3070-140">**Kõik kirjed** – saate teatise, kui muudetakse aktiivses lehe vaates oleva kauba ostutellimuse olekut.</span><span class="sxs-lookup"><span data-stu-id="e3070-140">**All records** – You receive an alert when the status of a purchase order is changed for an item in the active page view.</span></span> <span data-ttu-id="e3070-141">Teatud kirjete kogumile reeglite loomiseks saate kasutada lehel saadaolevat täpsemat filtrifunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="e3070-141">You can use the advanced filtering that is available on the page to create rules for a specific set of records.</span></span> <span data-ttu-id="e3070-142">Näiteks saate luua teatise, mis käivitatakse kõigi konkreetse kliendigrupi klientide ostutellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="e3070-142">For example, you can create an alert that is triggered for all purchase orders for the customers in a specific customer group.</span></span>
    
## <a name="expiry-of-rule"></a><span data-ttu-id="e3070-143">Reegli aegumine</span><span class="sxs-lookup"><span data-stu-id="e3070-143">Expiry of rule</span></span>

<span data-ttu-id="e3070-144">Dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind kuni** saate määrata, kui kaua teatisereegel aktiivne peaks olema.</span><span class="sxs-lookup"><span data-stu-id="e3070-144">On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>

## <a name="alert-contents"></a><span data-ttu-id="e3070-145">Teatise sisu</span><span class="sxs-lookup"><span data-stu-id="e3070-145">Alert contents</span></span>

<span data-ttu-id="e3070-146">Dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisega** saate määrata teema ja sõnumi teksti, mida teatiste puhul peaks kasutatama.</span><span class="sxs-lookup"><span data-stu-id="e3070-146">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>

## <a name="user-id"></a><span data-ttu-id="e3070-147">Kasutaja kood</span><span class="sxs-lookup"><span data-stu-id="e3070-147">User ID</span></span>

<span data-ttu-id="e3070-148">Dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisega** saate määrata, milline kasutaja peaks teatiseid saama.</span><span class="sxs-lookup"><span data-stu-id="e3070-148">On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="e3070-149">Vaikimisi on valitud teie kasutaja ID.</span><span class="sxs-lookup"><span data-stu-id="e3070-149">By default, your user ID is selected.</span></span> <span data-ttu-id="e3070-150">See valik on piiratud organisatsiooni administraatoritele.</span><span class="sxs-lookup"><span data-stu-id="e3070-150">This option is restricted to organization administrators.</span></span>

## <a name="create-an-alert-rule"></a><span data-ttu-id="e3070-151">Teatisereegli loomine</span><span class="sxs-lookup"><span data-stu-id="e3070-151">Create an alert rule</span></span>

1. <span data-ttu-id="e3070-152">Avage leht, mis sisaldab jälgitavaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="e3070-152">Open the page that contains the data to monitor.</span></span>
2. <span data-ttu-id="e3070-153">Valige toimingupaani vahekaardil **Suvandid** rühmas **Anna ühiskasutusse** suvand **Teavita mind järgmisega**.</span><span class="sxs-lookup"><span data-stu-id="e3070-153">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create alert rule**.</span></span>
3. <span data-ttu-id="e3070-154">Valige jälgitav väli dialoogiboksi **Loo teatise reegel** väljal **Väli**.</span><span class="sxs-lookup"><span data-stu-id="e3070-154">In the **Create alert rule** dialog box, in the **Field** field, select the field to monitor.</span></span>
4. <span data-ttu-id="e3070-155">Valige sündmuse tüüp väljal **Sündmus**.</span><span class="sxs-lookup"><span data-stu-id="e3070-155">In the **Event** field, select the type of event.</span></span>
5. <span data-ttu-id="e3070-156">Valige suvand kiirkaardil **Teavita mind järgmisel juhul**.</span><span class="sxs-lookup"><span data-stu-id="e3070-156">On the **Alert me for** FastTab, select an option.</span></span>
6. <span data-ttu-id="e3070-157">Kui teatisereegel peaks passiivseks muutuma kindlal kuupäeval, määrake lõppkuupäev kiirkaardil **Teavita mind kuni**.</span><span class="sxs-lookup"><span data-stu-id="e3070-157">If the alert rule should become inactive on a specific date, on the **Alert me until** FastTab, select an end date.</span></span>
7. <span data-ttu-id="e3070-158">Kinnitage meilisõnumi teema vaikepealkiri või sisestage uus teema kiirkaardi **Teavita mind järgmisega** väljal **Teema**.</span><span class="sxs-lookup"><span data-stu-id="e3070-158">On the **Alert me with** FastTab, in the **Subject** field, accept the default subject heading for the email message, or enter a new subject.</span></span> <span data-ttu-id="e3070-159">Teksti kasutatakse meilisõnumi teema pealkirjana, mille saate teatise käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="e3070-159">The text is used as the subject heading for the email message that you receive when an alert is triggered.</span></span>
8. <span data-ttu-id="e3070-160">Sisestage valikuline teade väljale **Teade**.</span><span class="sxs-lookup"><span data-stu-id="e3070-160">In the **Message** field, enter an optional message.</span></span> <span data-ttu-id="e3070-161">Teksti kasutatakse sõnumina, mille saate teatise käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="e3070-161">The text is used as the message that you receive when an alert is triggered.</span></span>
9. <span data-ttu-id="e3070-162">Valige **OK**, et salvestada sätted ja luua teatisereegel.</span><span class="sxs-lookup"><span data-stu-id="e3070-162">Select **OK** to save the settings and create the alert rule.</span></span>
