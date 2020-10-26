---
title: Laorakenduse sündmused
description: Selles teemas kirjeldatakse laorakenduse sündmusetöötlust, mida kasutatakse pakett-töö osana laorakenduse sündmuseteadete töötlemiseks.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988372"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="95e7d-103">Laorakenduse sündmusetöötlus</span><span class="sxs-lookup"><span data-stu-id="95e7d-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95e7d-104">Rakenduses Supply Chain Management töötavad pakett-tööd saavad kasutada laorakenduse sündmuste töötlemise järjekorrast pärit andmeid, et reageerida äramärgitud sündmustele nii, nagu vaja.</span><span class="sxs-lookup"><span data-stu-id="95e7d-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="95e7d-105">See funktsioon lisab järjekorda asjakohased sündmused, reageerimaks kindlat tüüpi tegevustele, mida rakendust kasutavad töötajad teevad.</span><span class="sxs-lookup"><span data-stu-id="95e7d-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="95e7d-106">Näide on see, kui funktsiooni **Üleviimistellimuste loomine ja töötlemine laorakenduses** kasutamisel luuakse ja värskendatakse üleviimistellimuse päist ja ridu peidetult ajal, mil süsteem käitab pakett-tööd **Laorakenduse sündmuste töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="95e7d-107">Laorakenduse sündmuste töötlemise funktsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="95e7d-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="95e7d-108">Enne selle funktsiooni kasutamist tuleb see teie süsteemis lubada.</span><span class="sxs-lookup"><span data-stu-id="95e7d-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="95e7d-109">Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et kontrollida funktsiooni olekut ja vajaduse korral see lubada.</span><span class="sxs-lookup"><span data-stu-id="95e7d-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="95e7d-110">Laorakenduse sündmuste töötlemise funktsioon on loetletud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="95e7d-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="95e7d-111">**Moodul** – laohaldus</span><span class="sxs-lookup"><span data-stu-id="95e7d-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="95e7d-112">**Funktsiooni nimi** – laorakenduse sündmuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="95e7d-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="95e7d-113">Pakett-töö seadistamine laorakenduse sündmuste töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="95e7d-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="95e7d-114">Laorakenduse sündmuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="95e7d-114">Process warehouse app events</span></span>

<span data-ttu-id="95e7d-115">Seadistage ajastatud pakett-töö laorakenduse sündmuste töötlemiseks üleviimistellimuse loomise ja reavärskenduste jaoks.</span><span class="sxs-lookup"><span data-stu-id="95e7d-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="95e7d-116">Avage **Laohaldus \> Perioodilised ülesanded \> Laorakenduse sündmuste töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="95e7d-117">Avaneb laorakenduse sündmuste töötlemise dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="95e7d-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="95e7d-118">Laiendage kiirkaart **Käivita taustal** ja seadke suvandi **Pakktöötlus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="95e7d-119">Valige kiirkaardil **Käivita taustal** suvand **Kordumine**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="95e7d-120">Avaneb dialoogiboks **Kordumise määratlemine**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="95e7d-121">Seadistage käivitusgraafik oma ettevõtte vajaduste järgi.</span><span class="sxs-lookup"><span data-stu-id="95e7d-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="95e7d-122">Valige **OK**, et naasta dialoogiboksi **Laorakenduse sündmuste töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="95e7d-123">Valige **OK** dialoogiboksis **Laorakenduse sündmuste töötlemine**, et lisada pakett-töö pakktöötluse järjekorda.</span><span class="sxs-lookup"><span data-stu-id="95e7d-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="95e7d-124">Laorakenduse sündmuste pärimine</span><span class="sxs-lookup"><span data-stu-id="95e7d-124">Query warehouse app events</span></span>

<span data-ttu-id="95e7d-125">Saate vaadata sündmuste järjekorda ja laorakenduse loodud sündmuseteateid, avades **Laohaldus \> Päringud ja aruanded \> Mobiilse seadme logid \> Laorakenduse sündmused**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="95e7d-126">Standardne sündmuste järjekorra protsess</span><span class="sxs-lookup"><span data-stu-id="95e7d-126">The standard event queue process</span></span>

<span data-ttu-id="95e7d-127">Laorakenduse sündmuste järjekorda kasutatakse tavaliselt järgmises kirjeldatud voos.</span><span class="sxs-lookup"><span data-stu-id="95e7d-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="95e7d-128">Sündmus lisatakse järjekorda koos sündmuseteatega.</span><span class="sxs-lookup"><span data-stu-id="95e7d-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="95e7d-129">Uue teate olek on esialgu **Ootel**, mis tähendab, et pakett-töö **Laorakenduse sündmuste töötlemine** ei võta teadet vastu ega töötle seda.</span><span class="sxs-lookup"><span data-stu-id="95e7d-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="95e7d-130">Niipea, kui teate olekuks määratakse **Järjekorras**, võtab pakett-töö **Laorakenduse töötlemine** sündmuse ette ja töötleb seda.</span><span class="sxs-lookup"><span data-stu-id="95e7d-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="95e7d-131">Pakett-töö määrab sündmuse olekuks kas **Lõpetatud** või **Nurjus** sõltuvalt sellest, kas soovitud protsess oli võimalik.</span><span class="sxs-lookup"><span data-stu-id="95e7d-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="95e7d-132">Kui kõik seotud sündmuseteated on **lõpetatud**, kustutatakse sündmus järjekorrast.</span><span class="sxs-lookup"><span data-stu-id="95e7d-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="95e7d-133">Üksikasjaliku näite leiate teemast [Protsess „Üleviimistellimuse loomine laorakenduses”](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="95e7d-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="95e7d-134">Sündmusetõrgete käsitlemine</span><span class="sxs-lookup"><span data-stu-id="95e7d-134">Handle event errors</span></span>

<span data-ttu-id="95e7d-135">Laosündmuse töötlemise osana ei saa taotletud teate tegevus pakett-tööst protsesse vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="95e7d-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="95e7d-136">Sellisel juhul määratakse sündmusteate olekuks **Nurjus**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="95e7d-137">Saate kasutada **pakett-töö logi** teavet, et saada teada põhjused ja parandada võimalikud probleemid.</span><span class="sxs-lookup"><span data-stu-id="95e7d-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="95e7d-138">Üksikasjaliku näite leiate teemast [Üleviimistellimuse loomine laorakenduses](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="95e7d-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="95e7d-139">Laorakenduse nurjunud sündmuseteate lähtestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="95e7d-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="95e7d-140">Avage **Laohaldus \> Päringud ja aruanded \> Mobiilse seadme logid \> Laorakenduse sündmused**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="95e7d-141">Otsige üles ja valige kiirkaardil **Laorakenduse sündmusteated** asjakohane sündmus, mille olek veerus **Sündmuse olek** on **Nurjus**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="95e7d-142">Valige lehe **Laorakenduse sündmuseteated** tööriistaribalt suvand **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="95e7d-143">Jätkake tööd seni, kuni kõik asjakohased teated on lähtestatud.</span><span class="sxs-lookup"><span data-stu-id="95e7d-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="95e7d-144">Saate samuti eemaldada **nurjunud** sündmuseteate, kasutades lehe **Laorakenduse sündmusteated** tööriistaribal suvandit **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="95e7d-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
