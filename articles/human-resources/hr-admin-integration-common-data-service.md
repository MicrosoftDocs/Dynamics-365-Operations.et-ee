---
title: Common Data Service'i integratsiooni konfigureerimine
description: Saate Common Data Service’i ja Dynamics 365 Human Resourcesi vahelise integratsiooni sisse või välja lülitada. Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja üksust uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 04280aa0908ed6dab86ef87b6c1843e4b4348e08
ms.sourcegitcommit: c9657b44adb9c1a77c7c2f6ab63a58cc848974ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198418"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="bd37a-104">Common Data Service'i integratsiooni konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="bd37a-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="bd37a-105">Saate Common Data Service’i ja Dynamics 365 Human Resourcesi vahelise integratsiooni sisse või välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="bd37a-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="bd37a-106">Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja üksust uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.</span><span class="sxs-lookup"><span data-stu-id="bd37a-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="bd37a-107">Kui lülitate integratsiooni välja, saavad kasutajad teha muudatusi rakenduses Human Resources või Common Data Service, kuid neid muudatusi ei sünkroonita kahe keskkonna vahel.</span><span class="sxs-lookup"><span data-stu-id="bd37a-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="bd37a-108">Rakenduste Human Resources ja Common Data Service vahelise andmete integratsioon on vaikimisi välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="bd37a-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="bd37a-109">Võib-olla soovite integratsiooni välja lülitada järgmistes olukordades.</span><span class="sxs-lookup"><span data-stu-id="bd37a-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="bd37a-110">Te täidate andmeid andmete halduse raamistiku kaudu ja peate andmeid õige oleku saavutamiseks mitu korda importima.</span><span class="sxs-lookup"><span data-stu-id="bd37a-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="bd37a-111">Andmed on seotud kas rakendusega Human Resources või Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bd37a-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="bd37a-112">Kui lülitate integratsiooni välja, saate kustutada kirje ühes keskkonnas, kustutamata seda teises.</span><span class="sxs-lookup"><span data-stu-id="bd37a-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="bd37a-113">Kui lülitate integratsiooni tagasi sisse, sünkroonitakse kirje keskkonnas, kus seda ei kustutatud, tagasi keskkonda, kus see kustutati.</span><span class="sxs-lookup"><span data-stu-id="bd37a-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="bd37a-114">Sünkroonimine algab järgmisel korral, kui käivitub rakenduse **Common Data Service integratsioon vastamata nõude sünkroonimise** pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="bd37a-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="bd37a-115">Kui lülitate andmete integreerimise välja, veenduge, et te ei redigeeriks sama kirjet mõlemas keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="bd37a-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="bd37a-116">Kui lülitate integratsiooni uuesti sisse, sünkroonitakse viimati redigeeritud kirje.</span><span class="sxs-lookup"><span data-stu-id="bd37a-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="bd37a-117">Seega, kui te ei teinud mõlemas keskkonnas kirjes samu muudatusi, võib esineda andmekadu.</span><span class="sxs-lookup"><span data-stu-id="bd37a-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="bd37a-118">Juurdepääs rakenduse Common Data Service integratsiooni lehele</span><span class="sxs-lookup"><span data-stu-id="bd37a-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="bd37a-119">Valige rakenduse Human Resources eksemplaris, kus soovite integratsiooni sätteid rakendusega Common Data Service vaadata või konfigureerida, paan **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="bd37a-120">[![Süsteemihalduse paan](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="bd37a-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="bd37a-121">Valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="bd37a-122">[![Vahekaart Lingid](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="bd37a-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="bd37a-123">Valige jaotises **Integratsioonid** rakenduse **Common Data Service konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="bd37a-124">[![Common Data Service’i konfiguratsiooni link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="bd37a-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="bd37a-125">Rakenduste Human Resources ja Common Data Service vahelise andmete integratsiooni sisse ja välja lülitamine</span><span class="sxs-lookup"><span data-stu-id="bd37a-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="bd37a-126">Integratsiooni sisselülitamiseks seadke **Luba integreerimine rakendusele Common Data Service** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd37a-127">Kui lülitate integratsiooni sisse, sünkroonitakse andmed järgmisel korral, kui **Common Data Service’i integratsiooni vastamata nõude sünkroonimise** pakett-töö käivitub.</span><span class="sxs-lookup"><span data-stu-id="bd37a-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="bd37a-128">Kõik andmed peaksid olema kättesaadavad pärast pakett-töö lõpetamist.</span><span class="sxs-lookup"><span data-stu-id="bd37a-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="bd37a-129">Integratsiooni väljalülitamiseks seadke suvandi väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="bd37a-130">[![Rakenduse Common Data Service integratsiooni sisse või välja lülitamine](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="bd37a-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="bd37a-131">Andmete integratsiooni üksikasjade ülevaade</span><span class="sxs-lookup"><span data-stu-id="bd37a-131">View data integration details</span></span>

<span data-ttu-id="bd37a-132">Rakenduse **Common Data Service integratsiooni** lehe kiirkaardil **Haldamine** saate vaadata, kuidas on rakenduste Human Resources ja Common Data Service kirjed ühendatud.</span><span class="sxs-lookup"><span data-stu-id="bd37a-132">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="bd37a-133">Üksuse kirjete vaatamiseks valige väljal **CDS-üksuse nimi** olev üksus.</span><span class="sxs-lookup"><span data-stu-id="bd37a-133">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="bd37a-134">Ruudustik kuvab kõik kirjed, mis on seotud valitud üksusega.</span><span class="sxs-lookup"><span data-stu-id="bd37a-134">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="bd37a-135">[![Üksuse kirjete vaatamine](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="bd37a-135">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="bd37a-136">Kõik Common Data Service’i üksused pole praegu loetletud.</span><span class="sxs-lookup"><span data-stu-id="bd37a-136">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="bd37a-137">Ruudustikus kuvatakse ainult üksused, mis toetavad kohandatud väljade kasutamist.</span><span class="sxs-lookup"><span data-stu-id="bd37a-137">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="bd37a-138">Uued üksused muutuvad kättesaadavaks rakenduse Human Resources jätkuväljaannetes.</span><span class="sxs-lookup"><span data-stu-id="bd37a-138">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="bd37a-139">Ruudustik sisaldab järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="bd37a-139">The grid includes the following fields:</span></span>

- <span data-ttu-id="bd37a-140">**CDS-üksuse nimi** – üksuse nimi rakenduses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bd37a-140">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="bd37a-141">**CDS-üksuse viide** – identifikaator, mida Common Data Service kasutab kirje tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="bd37a-141">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="bd37a-142">See väärtus võrdub rakenduse Human Resources väärtusega **RecId**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-142">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="bd37a-143">Selle identifikaatori leiate, avades rakenduse Common Data Service üksuse Microsoft Excelis.</span><span class="sxs-lookup"><span data-stu-id="bd37a-143">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="bd37a-144">**Rakenduse Human Resources üksuse nimi** – üksus, mis viimasena sünkroonis andmeid rakendusega Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bd37a-144">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="bd37a-145">Üksusel võib olla kas Common Data Service’i eesliide või muu eesliide.</span><span class="sxs-lookup"><span data-stu-id="bd37a-145">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="bd37a-146">**Rakenduse Human Resources viide** – väärtus **RecId**, mis on seotud kirjega rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bd37a-146">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="bd37a-147">**Kustutati CDS-ist** – väärtus, mis näitab, kas kirje kustutati rakendusest Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bd37a-147">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="bd37a-148">Eemaldage rakendusest Common Data Service kirje seos rakendusega Human Resources</span><span class="sxs-lookup"><span data-stu-id="bd37a-148">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="bd37a-149">Kui teil tekib probleeme rakenduste Human Resources ja Common Data Service vahelise sünkroonimise ajal, saate neid lahendada, tühjendades jälgimise ja lastes jälgimise tabeli uuesti sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="bd37a-149">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="bd37a-150">Kui eemaldate seose ja seejärel muudate või kustutate kirje rakenduses Common Data Service, ei sünkroonita muudatusi rakendusega Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bd37a-150">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="bd37a-151">Kui teete muudatusi rakenduses Human Resources, luuakse uus jälgimise kirje ja kirje uuendatakse rakenduses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bd37a-151">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="bd37a-152">Kirje seose eemaldamiseks rakenduste Human Resources ja Common Data Service vahel, valige üksus väljal **CDS-üksuse nimi** ja seejärel käsk **Tühjenda jälgimise teave**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-152">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="bd37a-153">[![Jälgimisteabe kustutamine](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="bd37a-153">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="bd37a-154">Üksuse täieliku sünkroonimise käivitamiseks pärast jälgimise tühjendamist vaadake järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="bd37a-154">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="bd37a-155">Sünkroonige üksus rakenduste Human Resources ja Common Data Service vahel</span><span class="sxs-lookup"><span data-stu-id="bd37a-155">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="bd37a-156">Kasutage seda protseduuri, kui:</span><span class="sxs-lookup"><span data-stu-id="bd37a-156">Use this procedure when:</span></span>

- <span data-ttu-id="bd37a-157">Common Data Service'i muudatuste kuvamine rakenduses Human Resources võtab liiga kaua aega;</span><span class="sxs-lookup"><span data-stu-id="bd37a-157">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="bd37a-158">pärast jälitamise tühjendamist peate värskendama jälgimise tabelit.</span><span class="sxs-lookup"><span data-stu-id="bd37a-158">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="bd37a-159">Rakenduse Human Resources ja Common Data Service'i vahelise olemi täieliku sünkroonimise käivitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="bd37a-159">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="bd37a-160">Valige olem väljal **CDS-üksuse nimi**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-160">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="bd37a-161">Valige **Sünkrooni kohe**.</span><span class="sxs-lookup"><span data-stu-id="bd37a-161">Select **Sync now**.</span></span>

<span data-ttu-id="bd37a-162">[![Täieliku sünkroonimise käivitamine](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="bd37a-162">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


