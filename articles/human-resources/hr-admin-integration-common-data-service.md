---
title: Dataverse'i integratsiooni konfigureerimine
description: Saate Microsoft Dataverse’i ja Dynamics 365 Human Resourcesi vahelise integratsiooni sisse või välja lülitada. Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja tabelit uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112270"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="2360a-104">Dataverse'i integratsiooni konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2360a-104">Configure Dataverse integration</span></span>

<span data-ttu-id="2360a-105">Saate Microsoft Dataverse’i ja Dynamics 365 Human Resourcesi vahelise integratsiooni sisse või välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="2360a-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="2360a-106">Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja tabelit uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.</span><span class="sxs-lookup"><span data-stu-id="2360a-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="2360a-107">Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="2360a-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="2360a-108">Kui lülitate integratsiooni välja, saavad kasutajad teha muudatusi rakenduses Human Resources või Dataverse, kuid neid muudatusi ei sünkroonita kahe keskkonna vahel.</span><span class="sxs-lookup"><span data-stu-id="2360a-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="2360a-109">Rakenduste Human Resources ja Dataverse vahelise andmete integratsioon on vaikimisi välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="2360a-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="2360a-110">Võib-olla soovite integratsiooni välja lülitada järgmistes olukordades.</span><span class="sxs-lookup"><span data-stu-id="2360a-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="2360a-111">Te täidate andmeid andmete halduse raamistiku kaudu ja peate andmeid õige oleku saavutamiseks mitu korda importima.</span><span class="sxs-lookup"><span data-stu-id="2360a-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="2360a-112">Andmed on seotud kas rakendusega Human Resources või Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2360a-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="2360a-113">Kui lülitate integratsiooni välja, saate kustutada kirje ühes keskkonnas, kustutamata seda teises.</span><span class="sxs-lookup"><span data-stu-id="2360a-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="2360a-114">Kui lülitate integratsiooni tagasi sisse, sünkroonitakse kirje keskkonnas, kus seda ei kustutatud, tagasi keskkonda, kus see kustutati.</span><span class="sxs-lookup"><span data-stu-id="2360a-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="2360a-115">Sünkroonimine algab järgmisel korral, kui käivitub rakenduse **Dataverse integratsioon vastamata nõude sünkroonimise** pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="2360a-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="2360a-116">Kui lülitate andmete integreerimise välja, veenduge, et te ei redigeeriks sama kirjet mõlemas keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="2360a-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="2360a-117">Kui lülitate integratsiooni uuesti sisse, sünkroonitakse viimati redigeeritud kirje.</span><span class="sxs-lookup"><span data-stu-id="2360a-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="2360a-118">Seega, kui te ei teinud mõlemas keskkonnas kirjes samu muudatusi, võib esineda andmekadu.</span><span class="sxs-lookup"><span data-stu-id="2360a-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="2360a-119">Juurdepääs rakenduse Dataverse integratsiooni lehele</span><span class="sxs-lookup"><span data-stu-id="2360a-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="2360a-120">Valige rakenduse Human Resources eksemplaris, kus soovite integratsiooni sätteid rakendusega Dataverse vaadata või konfigureerida, paan **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="2360a-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="2360a-121">[![Süsteemihalduse paan](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="2360a-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="2360a-122">Valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="2360a-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="2360a-123">[![Vahekaart Lingid](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="2360a-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="2360a-124">Valige jaotises **Integratsioonid** rakenduse **Dataverse konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="2360a-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="2360a-125">[![Dataverse’i konfiguratsiooni link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="2360a-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="2360a-126">Rakenduste Human Resources ja Dataverse vahelise andmete integratsiooni sisse ja välja lülitamine</span><span class="sxs-lookup"><span data-stu-id="2360a-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="2360a-127">Integratsiooni sisselülitamiseks määrake suvand **Luba Dataverse'i integratsioon** väärtusele **Jah** lehel **Microsoft Dataverse'i integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="2360a-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2360a-128">Kui lülitate integratsiooni sisse, sünkroonitakse andmed järgmisel korral, kui **Dataverse’i integratsiooni vastamata nõude sünkroonimise** pakett-töö käivitub.</span><span class="sxs-lookup"><span data-stu-id="2360a-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="2360a-129">Kõik andmed peaksid olema kättesaadavad pärast pakett-töö lõpetamist.</span><span class="sxs-lookup"><span data-stu-id="2360a-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="2360a-130">Integratsiooni väljalülitamiseks seadke suvandi väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="2360a-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="2360a-131">[![Rakenduse Dataverse integratsiooni sisse või välja lülitamine](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="2360a-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="2360a-132">Soovitame andmete migreerimisega tegeledes tungivalt Dataverse'i integratsiooni välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="2360a-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="2360a-133">Mahukate andmete üleslaadimine võib jõudlust oluliselt mõjutada.</span><span class="sxs-lookup"><span data-stu-id="2360a-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="2360a-134">Näiteks võib 2000 töötaja üleslaadimine võtta mitu tundi, kui integratsioon on lubatud, ja vähem kui üks tund, kui see on keelatud.</span><span class="sxs-lookup"><span data-stu-id="2360a-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="2360a-135">Näites toodud numbrid on mõeldud ainult selgitamiseks.</span><span class="sxs-lookup"><span data-stu-id="2360a-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="2360a-136">Kirjete importimiseks kuluv täpne aeg võib mitme teguri põhjal olla väga erinev.</span><span class="sxs-lookup"><span data-stu-id="2360a-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="2360a-137">Andmete integratsiooni üksikasjade ülevaade</span><span class="sxs-lookup"><span data-stu-id="2360a-137">View data integration details</span></span>

<span data-ttu-id="2360a-138">Rakenduse **Microsoft Dataverse integratsiooni** lehe kiirkaardil **Haldamine** saate vaadata, kuidas on rakenduste Human Resources ja Dataverse read ühendatud.</span><span class="sxs-lookup"><span data-stu-id="2360a-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="2360a-139">Tabeliridade vaatamiseks valige tabel väljalt **Dataverse'i tabel**.</span><span class="sxs-lookup"><span data-stu-id="2360a-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="2360a-140">Ruudustik kuvab kõik read, mis on seotud valitud tabeliga.</span><span class="sxs-lookup"><span data-stu-id="2360a-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="2360a-141">Kõik Dataverse’i tabelid pole praegu loetletud.</span><span class="sxs-lookup"><span data-stu-id="2360a-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="2360a-142">Ruudustikus kuvatakse ainult tabelid, mis toetavad kohandatud väljade kasutamist.</span><span class="sxs-lookup"><span data-stu-id="2360a-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="2360a-143">Uued tabelid muutuvad kättesaadavaks rakenduse Human Resources jätkuväljaannetes.</span><span class="sxs-lookup"><span data-stu-id="2360a-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="2360a-144">Ruudustik sisaldab järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="2360a-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="2360a-145">**Dataverse'i tabel** - tabeli nimi Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="2360a-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="2360a-146">**Dataverse'i tabeli viide** - identifikaator, mida Dataverse kasutab kirje tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="2360a-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="2360a-147">See väärtus võrdub rakenduse Human Resources väärtusega **RecId**.</span><span class="sxs-lookup"><span data-stu-id="2360a-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="2360a-148">Selle identifikaatori leiate, avades rakenduse Dataverse tabeli Microsoft Excelis.</span><span class="sxs-lookup"><span data-stu-id="2360a-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="2360a-149">**Rakenduse Human Resources üksuse nimi** - Human Resourcesi üksus, mis viimasena sünkroonis andmeid rakendusega Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2360a-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="2360a-150">Üksusel võib olla kas Dataverse’i eesliide või muu eesliide.</span><span class="sxs-lookup"><span data-stu-id="2360a-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="2360a-151">**Rakenduse Human Resources viide** – väärtus **RecId**, mis on seotud kirjega rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2360a-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="2360a-152">**Kustutati Dataverse'ist** - väärtus, mis näitab, kas rida kustutati Dataverse'ist.</span><span class="sxs-lookup"><span data-stu-id="2360a-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="2360a-153">Rakenduse Human Resources kirjed vastavad ridadele Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="2360a-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="2360a-154">Eemaldage rakenduse Dataverse realt kirje seos rakendusega Human Resources</span><span class="sxs-lookup"><span data-stu-id="2360a-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="2360a-155">Kui teil tekib probleeme rakenduste Human Resources ja Dataverse vahelise sünkroonimise ajal, saate neid lahendada, tühjendades jälgimise ja lastes jälgimise tabeli uuesti sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="2360a-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="2360a-156">Kui eemaldate seose ja seejärel muudate või kustutate rea rakenduses Dataverse, ei sünkroonita muudatusi rakendusega Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2360a-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="2360a-157">Kui teete muudatusi rakenduses Human Resources, luuakse uus jälgimise kirje ja rida uuendatakse rakenduses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2360a-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="2360a-158">Kirje seose eemaldamiseks rakenduste Human Resources ja Dataverse'i rea vahel, valige tabel väljal **Dataverse'i tabel** ja seejärel valige käsk **Tühjenda jälgimise teave**.</span><span class="sxs-lookup"><span data-stu-id="2360a-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="2360a-159">[![Jälgimisteabe kustutamine](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="2360a-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="2360a-160">Tabeli täieliku sünkroonimise käivitamiseks pärast jälgimise tühjendamist vaadake järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="2360a-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="2360a-161">Sünkroonige tabel rakenduste Human Resources ja Dataverse vahel</span><span class="sxs-lookup"><span data-stu-id="2360a-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="2360a-162">Kasutage seda protseduuri, kui:</span><span class="sxs-lookup"><span data-stu-id="2360a-162">Use this procedure when:</span></span>

- <span data-ttu-id="2360a-163">Dataverse'i muudatuste kuvamine rakenduses Human Resources võtab liiga kaua aega;</span><span class="sxs-lookup"><span data-stu-id="2360a-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="2360a-164">pärast jälitamise tühjendamist peate värskendama jälgimise tabelit.</span><span class="sxs-lookup"><span data-stu-id="2360a-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="2360a-165">Rakenduse Human Resources ja Dataverse'i vahelise tabeli täieliku sünkroonimise käivitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2360a-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="2360a-166">Valige tabel väljal **Dataverse'i tabel**.</span><span class="sxs-lookup"><span data-stu-id="2360a-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="2360a-167">Valige **Sünkrooni kohe**.</span><span class="sxs-lookup"><span data-stu-id="2360a-167">Select **Sync now**.</span></span>

<span data-ttu-id="2360a-168">[![Täieliku sünkroonimise käivitamine](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="2360a-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="2360a-169">Vt ka</span><span class="sxs-lookup"><span data-stu-id="2360a-169">See also</span></span>

[<span data-ttu-id="2360a-170">Dataverse'i tabelid</span><span class="sxs-lookup"><span data-stu-id="2360a-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="2360a-171">Dataverse'i virtuaalsete tabelite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2360a-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="2360a-172">Human Resourcesi virtuaaltabelite KKK</span><span class="sxs-lookup"><span data-stu-id="2360a-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="2360a-173">Mis on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="2360a-173">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="2360a-174">Terminoloogia uuendused</span><span class="sxs-lookup"><span data-stu-id="2360a-174">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
