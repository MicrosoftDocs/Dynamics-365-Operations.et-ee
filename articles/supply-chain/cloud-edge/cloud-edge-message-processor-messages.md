---
title: Sõnumi töötleja sõnumid
description: See teema annab teavet sõnumite protsessori teadete funktsiooni kohta kaalu ühiku töökoormuste puhul.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 03d8cad743ac2b2b1e7b2832b8272ca3dbf5a163
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021051"
---
# <a name="message-processor-messages"></a><span data-ttu-id="8e0da-103">Sõnumi töötleja sõnumid</span><span class="sxs-lookup"><span data-stu-id="8e0da-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8e0da-104">Sõnumitöötluse sõnumeid kasutatakse pilve ja servaskaala üksuste käitamisel [tootmise töökoormuste](cloud-edge-workload-manufacturing.md) ja [laohalduse töökoormuste](cloud-edge-workload-warehousing.md) jaoks.</span><span class="sxs-lookup"><span data-stu-id="8e0da-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="8e0da-105">Keskuse ja kaalu ühiku juurutuskeskkonnad vahetavad nende sünkroonimisel suurt hulka andmeid, kuid *teateprotsessor* töötleb ainult mõnda neist andmevahetustest.</span><span class="sxs-lookup"><span data-stu-id="8e0da-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="8e0da-106">Te saate vaadata teateprotsessori töödeldud teateid, kui teateid **Süsteemihaldus > Sõnumiprotsessor > Teateprotsessori teated**.</span><span class="sxs-lookup"><span data-stu-id="8e0da-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="8e0da-107">Teatepaneeli veerud ja filtrid</span><span class="sxs-lookup"><span data-stu-id="8e0da-107">Message grid columns and filters</span></span>

<span data-ttu-id="8e0da-108">Võite kasutada väljasid **sõnumiprotsessori teadete** lehe ülaosas, et aidata leida mis tahes konkreetsed sõnumid, mida otsite.</span><span class="sxs-lookup"><span data-stu-id="8e0da-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="8e0da-109">Enamik neist filtritest sobivad veeru pealkirjadega teatepaneelis.</span><span class="sxs-lookup"><span data-stu-id="8e0da-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="8e0da-110">Saadaval on järgmised filtrid ja veeru pealkirjad:</span><span class="sxs-lookup"><span data-stu-id="8e0da-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="8e0da-111">**Teate tüüp** – määrab teate tüübi.</span><span class="sxs-lookup"><span data-stu-id="8e0da-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="8e0da-112">**Teatejärjekord** – määrab järjekorra nime, milles teadet töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="8e0da-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="8e0da-113">Saadaval on järgmised järjekorrad:</span><span class="sxs-lookup"><span data-stu-id="8e0da-113">The following queues are provided:</span></span>
  - <span data-ttu-id="8e0da-114">*Skaalaüksus keskusesse*</span><span class="sxs-lookup"><span data-stu-id="8e0da-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="8e0da-115">*Lao käivitamise skaalaüksuse keskus*</span><span class="sxs-lookup"><span data-stu-id="8e0da-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="8e0da-116">*Tootmise käivitamise skaalaüksuse keskus*</span><span class="sxs-lookup"><span data-stu-id="8e0da-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="8e0da-117">**Teate olek** – määrab teate oleku.</span><span class="sxs-lookup"><span data-stu-id="8e0da-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="8e0da-118">Leidub järgmisi olekuid:</span><span class="sxs-lookup"><span data-stu-id="8e0da-118">The following states exists:</span></span>
  - <span data-ttu-id="8e0da-119">*Järjekorras* – sõnum on teateprotsessori töötlemiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="8e0da-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="8e0da-120">*Töödeldud* – sõnum on teateprotsessori poolt edukalt töödeldud.</span><span class="sxs-lookup"><span data-stu-id="8e0da-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="8e0da-121">*Tühistatud* – teade on töödeldud, kuid töötlemine nurjus.</span><span class="sxs-lookup"><span data-stu-id="8e0da-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="8e0da-122">**Sõnumi sisu** – selle filtriga tehakse sõnumisisu täistekstotsing.</span><span class="sxs-lookup"><span data-stu-id="8e0da-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="8e0da-123">(Sõnumit ei kuvata ruudustikus.) Filter käsitleb enamikke erisümboleid (nt „-”) tühikuna ja käsitleb kõiki tühikuid kahendmuutuja VÕI tehtemärkidena.</span><span class="sxs-lookup"><span data-stu-id="8e0da-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="8e0da-124">T=Nt kui otsite konkreetset väärtust `journalid`, mis oleks "USMF-123456", otsib süsteem kõik teated, mis sisaldavad "USMF" või "123456", mis on tõenäoliselt pikk loend.</span><span class="sxs-lookup"><span data-stu-id="8e0da-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="8e0da-125">Seetõttu oleks parem sisestada ainult "123456", sest see annab paremad tulemused.</span><span class="sxs-lookup"><span data-stu-id="8e0da-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="8e0da-126">Teate näidistüüp: varude korrigeerimise finantsvärskenduse taotlemine</span><span class="sxs-lookup"><span data-stu-id="8e0da-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="8e0da-127">Näiteks **sõnumi tüüpi** *Varude korrigeerimise finantsvärskendus* kasutatakse inventuuritöölehe loomiseks ja sisestamiseks keskusesse, kui töötaja kasutab lao rakendust [varude korrigeerimise registreerimiseks](cloud-edge-warehouse-inventory-adjustment.md) kaaluühiku laohalduse töökoormuses.</span><span class="sxs-lookup"><span data-stu-id="8e0da-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="8e0da-128">Kuna see konkreetne protsess pärineb kaaluühikust, kuvatakse **teatejärjekorra** väljal väärtuse *ühik keskusesse*.</span><span class="sxs-lookup"><span data-stu-id="8e0da-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="8e0da-129">Selle teatetüübi puhul salvestab kaaluühik sõnumi laorakenduse varude korrigeerimistoimingu osana.</span><span class="sxs-lookup"><span data-stu-id="8e0da-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="8e0da-130">Sõnumiandmed kantakse seejärel keskusesse üle osana samast protsessist, mida kasutatakse [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="8e0da-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="8e0da-131">Teade uuendatakse, et kuvada **teate olek** olekuna *järjekorras*.</span><span class="sxs-lookup"><span data-stu-id="8e0da-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="8e0da-132">Teateprotsessor püüab siis sõnumit töödelda ja uuendab **sõnumi olekut** edukalt *töödeldud* olekule või nurjumisel *tühistatuks*.</span><span class="sxs-lookup"><span data-stu-id="8e0da-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="8e0da-133">Saate kuvada teatelogi, sõnumi sisu ja üksikasju</span><span class="sxs-lookup"><span data-stu-id="8e0da-133">View the message log, message content, and details</span></span>

<span data-ttu-id="8e0da-134">Teate kohta üksikasjaliku teabe leiate, kui valite selle ruudustikust ja avate seejärel **logi** või **teate sisu** vahekaardid teateruudustikus, kus kuvatakse iga töötlussündmus.</span><span class="sxs-lookup"><span data-stu-id="8e0da-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="8e0da-135">**Sõnumi sisu** sõltub **sõnumitüübist** ja selle teksti pikkus on seega erinev.</span><span class="sxs-lookup"><span data-stu-id="8e0da-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="8e0da-136">Tavaline sõnumisisu tekst algab väärtusega **{** ja lõpeb väärtusega **}** ja nende vahel on sellised väljanimed, nagu näiteks `journalId`, millele järgneb **:** ja selline väärtus, nagu *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="8e0da-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="8e0da-137">Vahekaardi **Logi** tööriistaribal on järgmised nupud:</span><span class="sxs-lookup"><span data-stu-id="8e0da-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="8e0da-138">**Logi** – kuvatakse töötlemistulemused.</span><span class="sxs-lookup"><span data-stu-id="8e0da-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="8e0da-139">Sellest on abi eelkõige töötlemise nurjumise põhjuste mõistmisel nende teadete puhul, mille **töötlemise tulemus** on *Nurjunud*.</span><span class="sxs-lookup"><span data-stu-id="8e0da-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="8e0da-140">**Kogum** – mitu teatetöötlustoimingut saab käitada ühe ja sama pakktöötluse osana.</span><span class="sxs-lookup"><span data-stu-id="8e0da-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="8e0da-141">Selle nupu abil saate vaadata üksikasjalikke andmeid.</span><span class="sxs-lookup"><span data-stu-id="8e0da-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="8e0da-142">Näiteks saate vaadata, kas on olemas sõltuvusi, mis nõuavad süsteemilt kindlas järjekorras teatud teadete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="8e0da-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="8e0da-143">Teateprotsessori pakett-töö</span><span class="sxs-lookup"><span data-stu-id="8e0da-143">Message processor batch job</span></span>

<span data-ttu-id="8e0da-144">Pilve ja serva juurutuse käitamisel käivitatakse sõnumiprotsessori pakett-töö automaatselt uue teate loomisel töötlemiseks, seega ei pea te seda tööd käsitsi *plaanima*.</span><span class="sxs-lookup"><span data-stu-id="8e0da-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="8e0da-145">Vajadusel pääsete pakett-tööle, kui valides **Süsteemihaldus > Sõnumiprotsessor > Teateprotsessor**.</span><span class="sxs-lookup"><span data-stu-id="8e0da-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="8e0da-146">Sõnumi käsitsi saatmine või tühistamine</span><span class="sxs-lookup"><span data-stu-id="8e0da-146">Manually process or cancel a message</span></span>

<span data-ttu-id="8e0da-147">Sõltuvalt selle praegusest olekust, saate sõnumit käsitsi töödelda või tühistada.</span><span class="sxs-lookup"><span data-stu-id="8e0da-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="8e0da-148">Selleks valige ruudustikus teade ja valige siis tegevuspaanil suvand **Protsess** või **Tühista**</span><span class="sxs-lookup"><span data-stu-id="8e0da-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="8e0da-149">Saate häälestada ärisündmusi teatiste esitamiseks nurjunud töötlemise tulemuste kohta</span><span class="sxs-lookup"><span data-stu-id="8e0da-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="8e0da-150">Lisaks **sõnumi oleku** filtreerimiseks *Tühistatud* teadete järgi, et leida ebaõnnestunud teateid, saate seadistada keskuse [ärisündmused](../../fin-ops-core/dev-itpro/business-events/home-page.md), mis teavitavad teid töötluse nurjunud tulemustest.</span><span class="sxs-lookup"><span data-stu-id="8e0da-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="8e0da-151">Selleks aktiveerige ärisündmus nimega *Teateprotsessori teade*, mis on töödeldud **ärisündmuste kataloogi** lehel (**Süsteemihaldus > Häälestus > Ärisündmused > Ärisündmuste kataloog**).</span><span class="sxs-lookup"><span data-stu-id="8e0da-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="8e0da-152">Osana aktiveerimisprotsessist juhendatakse teid määramaks, kas sündmus on omane ühele või kõigile juriidilistele isikutele ja andma **lõpp-punkti nime**, mis tuleb esimesena määratleda.</span><span class="sxs-lookup"><span data-stu-id="8e0da-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="8e0da-153">Kui seade **Kui ärisündmus toimub** on näiteks seatud väärtusele *Microsoft Power Automate* (mitte *HTTPS*), luuakse **lõpp-punkti** nimi seadistuse *Microsoft Power Automate* põhjal automaatselt Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="8e0da-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="8e0da-154">Microsoft Power Automate näide</span><span class="sxs-lookup"><span data-stu-id="8e0da-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="8e0da-155">Selles näites kasutage seadet **Kui ärisündmus toimub**, kui *Microsoft Power Automate* edastab meile, mis sisaldavad InfoLogi sõnumeid ja hüperlinke, et avada lehe **Sõnumi töötleja sõnumid** spetsiifilise nurjunud sõnumi kohta keskmuse rakendamise puhul.</span><span class="sxs-lookup"><span data-stu-id="8e0da-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="8e0da-156">Vajadusel saate lisada lisaloogika, et saata teatised paralleelselt, kasutades erinevaid kanaleid ja juhtida adressaate sündmuse andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="8e0da-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="8e0da-157">Looge [Power Automate](https://preview.flow.microsoft.com)-s voo käivitamiseks uus automatiseeritud pilvevoog **Ärisündmuse toimumisel – Fin & Ops App (Dynamics 365** ), millele järgnevad **Parse JSON** ja **saatke meilisõnumid**, nagu näidatud järgmises illustratsioonis.</span><span class="sxs-lookup"><span data-stu-id="8e0da-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate automaatne pilvevoog":::

1. <span data-ttu-id="8e0da-159">Sammus **Kui ärisündmus toimus** saate kas üles otsida või sisestada keskuse **instants** pärast **Kategooriat** ja seejärel **Ärisündmus** *Sõnumiprotsessori sõnum on töödeldud*, nagu näidatud järgmises illustratsioonis.</span><span class="sxs-lookup"><span data-stu-id="8e0da-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Kui ärisündmuse toimumise etapp":::

1. <span data-ttu-id="8e0da-161">Sammu **Parse JSON** puhul sisestage **skeem**, mis määratleb laiendatud väljad.</span><span class="sxs-lookup"><span data-stu-id="8e0da-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="8e0da-162">Saate kasutada suvandit *Laadi skeem* alla ärisündmuste kataloogi lehel **Supply Chain Management** is või alustada, kleepides näidisskeemi teksti.</span><span class="sxs-lookup"><span data-stu-id="8e0da-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="8e0da-163">See näitetekst antakse pärast järgmist illustratsiooni.</span><span class="sxs-lookup"><span data-stu-id="8e0da-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Sõelu etapp JSON":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="8e0da-165">**E-kirja saatmise sammus** saate valida üksikud väljad või alustada, kasutades meili kehanäidet **kehaväljale**.</span><span class="sxs-lookup"><span data-stu-id="8e0da-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="8e0da-166">See näide antakse pärast järgmist illustratsiooni.</span><span class="sxs-lookup"><span data-stu-id="8e0da-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate Meilisõnumi saatmise samm":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="8e0da-168">Ärisündmuse salvestamisel aktiveeritakse see automaatselt ja on valmis kasutama Supply Chain Managementi osana.</span><span class="sxs-lookup"><span data-stu-id="8e0da-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
