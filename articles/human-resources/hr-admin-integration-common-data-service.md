---
title: Common Data Service'i integratsiooni konfigureerimine
description: Saate Common Data Service’i ja Microsoft Dynamics 365 Human Resourcesi eksemplari vahelise integratsiooni sisse või välja lülitada. Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja üksust uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008724"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="cf1e4-104">Common Data Service'i integratsiooni konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="cf1e4-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="cf1e4-105">Saate Common Data Service’i ja Microsoft Dynamics 365 Human Resourcesi eksemplari vahelise integratsiooni sisse või välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="cf1e4-106">Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja üksust uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="cf1e4-107">Kui lülitate integratsiooni välja, saavad kasutajad teha muudatusi rakenduses Human Resources või Common Data Service, kuid neid muudatusi ei sünkroonita kahe keskkonna vahel.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="cf1e4-108">Vaikimisi on rakenduste Human Resources ja Common Data Service vaheline integratsioon välja või sisse lülitatud, olenevalt keskkondade demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="cf1e4-109">**Välja** lülitatud uute keskkondade puhul, mis ei sisalda demo andmeid</span><span class="sxs-lookup"><span data-stu-id="cf1e4-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="cf1e4-110">**Sisse** lülitatud uute keskkondade puhul, mis sisaldavad demo andmeid</span><span class="sxs-lookup"><span data-stu-id="cf1e4-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="cf1e4-111">Uued keskkonnad, mis sisaldavad demoandmeid, hakkavad andmeid nende ettevalmistamisel sünkroonima.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="cf1e4-112">Võib-olla soovite integratsiooni välja lülitada järgmistes olukordades.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="cf1e4-113">Te täidate andmeid andmete halduse raamistiku kaudu ja peate andmeid õige oleku saavutamiseks mitu korda importima.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="cf1e4-114">Andmed on seotud kas rakendusega Human Resources või Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="cf1e4-115">Kui lülitate integratsiooni välja, saate kustutada kirje ühes keskkonnas, kustutamata seda teises.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="cf1e4-116">Kui lülitate integratsiooni tagasi sisse, sünkroonitakse kirje keskkonnas, kus seda ei kustutatud, tagasi keskkonda, kus see kustutati.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="cf1e4-117">Sünkroonimine algab järgmisel korral, kui käivitub rakenduse **Common Data Service integratsioon vastamata nõude sünkroonimise** pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="cf1e4-118">Kui lülitate andmete integreerimise välja, veenduge, et te ei redigeeriks sama kirjet mõlemas keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="cf1e4-119">Kui lülitate integratsiooni uuesti sisse, sünkroonitakse viimati redigeeritud kirje.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="cf1e4-120">Seega, kui te ei teinud mõlemas keskkonnas kirjes samu muudatusi, võib esineda andmekadu.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="cf1e4-121">Juurdepääs rakenduse Common Data Service integratsiooni lehele</span><span class="sxs-lookup"><span data-stu-id="cf1e4-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="cf1e4-122">Valige rakenduse Human Resources eksemplaris, kus soovite integratsiooni sätteid rakendusega Common Data Service vaadata või konfigureerida, paan **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="cf1e4-123">[![Süsteemihalduse paan](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="cf1e4-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="cf1e4-124">Valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="cf1e4-125">[![Vahekaart Lingid](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="cf1e4-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="cf1e4-126">Valige jaotises **Integratsioonid** rakenduse **Common Data Service konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="cf1e4-127">[![Common Data Service’i konfiguratsiooni link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="cf1e4-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="cf1e4-128">Rakenduste Human Resources ja Common Data Service vahelise andmete integratsiooni sisse ja välja lülitamine</span><span class="sxs-lookup"><span data-stu-id="cf1e4-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="cf1e4-129">Integratsiooni sisselülitamiseks seadke **Luba integreerimine rakendusele Common Data Service** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cf1e4-130">Kui lülitate integratsiooni sisse, sünkroonitakse andmed järgmisel korral, kui **Common Data Service’i integratsiooni vastamata nõude sünkroonimise** pakett-töö käivitub.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="cf1e4-131">Kõik andmed peaksid olema kättesaadavad pärast pakett-töö lõpetamist.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="cf1e4-132">Integratsiooni väljalülitamiseks seadke suvandi väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="cf1e4-133">[![Rakenduse Common Data Service integratsiooni sisse või välja lülitamine](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="cf1e4-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="cf1e4-134">Andmete integratsiooni üksikasjade ülevaade</span><span class="sxs-lookup"><span data-stu-id="cf1e4-134">View data integration details</span></span>

<span data-ttu-id="cf1e4-135">Rakenduse **Common Data Service integratsiooni** lehe kiirkaardil **Haldamine** saate vaadata, kuidas on rakenduste Human Resources ja Common Data Service kirjed ühendatud.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="cf1e4-136">Üksuse kirjete vaatamiseks valige väljal **CDS-üksuse nimi** olev üksus.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="cf1e4-137">Ruudustik kuvab kõik kirjed, mis on seotud valitud üksusega.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="cf1e4-138">[![Üksuse kirjete vaatamine](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="cf1e4-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="cf1e4-139">Kõik Common Data Service’i üksused pole praegu loetletud.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="cf1e4-140">Ruudustikus kuvatakse ainult üksused, mis toetavad kohandatud väljade kasutamist.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="cf1e4-141">Uued üksused muutuvad kättesaadavaks rakenduse Human Resources jätkuväljaannetes.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="cf1e4-142">Ruudustik sisaldab järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="cf1e4-143">**CDS-üksuse nimi** – üksuse nimi rakenduses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="cf1e4-144">**CDS-üksuse viide** – identifikaator, mida Common Data Service kasutab kirje tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="cf1e4-145">See väärtus võrdub rakenduse Human Resources väärtusega **RecId**.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="cf1e4-146">Selle identifikaatori leiate, avades rakenduse Common Data Service üksuse Microsoft Excelis.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="cf1e4-147">**Rakenduse Human Resources üksuse nimi** – üksus, mis viimasena sünkroonis andmeid rakendusega Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="cf1e4-148">Üksusel võib olla kas Common Data Service’i eesliide või muu eesliide.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="cf1e4-149">**Rakenduse Human Resources viide** – väärtus **RecId**, mis on seotud kirjega rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="cf1e4-150">**Kustutati CDS-ist** – väärtus, mis näitab, kas kirje kustutati rakendusest Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="cf1e4-151">Eemaldage rakendusest Common Data Service kirje seos rakendusega Human Resources</span><span class="sxs-lookup"><span data-stu-id="cf1e4-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="cf1e4-152">Kui teil tekib probleeme rakenduste Human Resources ja Common Data Service vahelise sünkroonimise ajal, saate neid lahendada, tühjendades jälgimise ja lastes jälgimise tabeli uuesti sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="cf1e4-153">Kui eemaldate seose ja seejärel muudate või kustutate kirje rakenduses Common Data Service, ei sünkroonita muudatusi rakendusega Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="cf1e4-154">Kui teete muudatusi rakenduses Human Resources, luuakse uus jälgimise kirje ja kirje uuendatakse rakenduses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="cf1e4-155">Kirje seose eemaldamiseks rakenduste Human Resources ja Common Data Service vahel, valige üksus väljal **CDS-üksuse nimi** ja seejärel käsk **Tühjenda jälgimise teave**.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="cf1e4-156">[![Jälgimisteabe kustutamine](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="cf1e4-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="cf1e4-157">Üksuse täieliku sünkroonimise käivitamiseks pärast jälgimise tühjendamist vaadake järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="cf1e4-158">Sünkroonige üksus rakenduste Human Resources ja Common Data Service vahel</span><span class="sxs-lookup"><span data-stu-id="cf1e4-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="cf1e4-159">Kasutage seda protseduuri, kui muudatused rakenduses Common Data Service võtavad liiga kaua aega, et ilmuda rakenduses Human Resources, või kui peate pärast jälgimise tühjendamist värskendama jälgimise tabelit.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="cf1e4-160">Üksuse täieliku sünkroonimise käivitamiseks rakenduste Human Resources ja Common Data Service vahel valige üksus väljal **CDS-üksuse nimi** ja seejärel käsk **Sünkrooni kohe**.</span><span class="sxs-lookup"><span data-stu-id="cf1e4-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="cf1e4-161">[![Täieliku sünkroonimise käivitamine](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="cf1e4-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


