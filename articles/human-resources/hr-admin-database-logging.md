---
title: Andmebaasi logimise konfigureerimine ja haldamine
description: Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae974436469c00a3df6fd40d9d60521a0883a917
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054808"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="07792-103">Andmebaasi logimise konfigureerimine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="07792-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="07792-104">Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.</span><span class="sxs-lookup"><span data-stu-id="07792-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="07792-105">Selles teemas käsitletakse järgmist.</span><span class="sxs-lookup"><span data-stu-id="07792-105">This topic describes how to:</span></span>

- <span data-ttu-id="07792-106">Andmebaasi logimise turbe ja jõudluse haldamine</span><span class="sxs-lookup"><span data-stu-id="07792-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="07792-107">Andmebaasi logimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="07792-107">Set up database logging</span></span>
- <span data-ttu-id="07792-108">Andmebaasilogide puhastamine</span><span class="sxs-lookup"><span data-stu-id="07792-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="07792-109">Andmebaasi logimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="07792-109">Overview of database logging</span></span>

<span data-ttu-id="07792-110">Andmebaasi logimine jälgib rakenduse Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.</span><span class="sxs-lookup"><span data-stu-id="07792-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="07792-111">Need muudatused hõlmavad lisamist, värskendamist või kustutamist.</span><span class="sxs-lookup"><span data-stu-id="07792-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="07792-112">Andmebaasi logimine salvestab tabeli või väljade muudatused andmebaasilogi tabelisse.</span><span class="sxs-lookup"><span data-stu-id="07792-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="07792-113">Andmebaasi logimise äriline kasutus hõlmab järgmist.</span><span class="sxs-lookup"><span data-stu-id="07792-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="07792-114">Auditikirje loomine kindlate tundlikku teavet sisaldavate tabelite muudatuste kohta.</span><span class="sxs-lookup"><span data-stu-id="07792-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="07792-115">Üksikute kannete jälgimine.</span><span class="sxs-lookup"><span data-stu-id="07792-115">Tracking single transactions.</span></span> <span data-ttu-id="07792-116">Andmebaasi logimine ei ole mõeldud pakett-töödes tehtavate automatiseeritud kannete jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="07792-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="07792-117">Andmebaasi logimise turve</span><span class="sxs-lookup"><span data-stu-id="07792-117">Security for database logging</span></span>

<span data-ttu-id="07792-118">Andmebaasilogid võivad sisaldada tundlikke andmeid.</span><span class="sxs-lookup"><span data-stu-id="07792-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="07792-119">Andke juurdepääs ainult sellistele turberollidele, mis vajavad logiandmetele juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="07792-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="07792-120">Andmebaasi logimine ja jõudlus</span><span class="sxs-lookup"><span data-stu-id="07792-120">Database logging and performance</span></span>

<span data-ttu-id="07792-121">Kuigi see on väärtuslik ärilisest vaatenurgast, võib andmebaasi logimine olla kulukas ressursikasutuse ja -halduse mõttes.</span><span class="sxs-lookup"><span data-stu-id="07792-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="07792-122">Andmebaasi logimise jõudluse tagajärjed hõlmavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="07792-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="07792-123">Andmebaasilogi tabel võib kasvada kiiresti ja põhjustada andmebaasi suurenemise.</span><span class="sxs-lookup"><span data-stu-id="07792-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="07792-124">Kasv sõltub logitud andmete hulgas, mida te otsustate säilitada.</span><span class="sxs-lookup"><span data-stu-id="07792-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="07792-125">Andmebaasilogi tabel säilitab vaikimisi ainult 30 päeva logiandmed.</span><span class="sxs-lookup"><span data-stu-id="07792-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="07792-126">Andmebaasi logimine võib negatiivselt mõjutada pikaajalisi automatiseeritud protsesse, näiteks pikaajalist andmete importimist.</span><span class="sxs-lookup"><span data-stu-id="07792-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="07792-127">Head tavad</span><span class="sxs-lookup"><span data-stu-id="07792-127">Best practices</span></span>

<span data-ttu-id="07792-128">Jõudluse parandamiseks piirake logikirjeid, valides logimiseks tervete tabelite asemel konkreetsed väljad.</span><span class="sxs-lookup"><span data-stu-id="07792-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="07792-129">Üldise jõudluse säilitamiseks saab andmebaasi logimine logida kuni 20 tabelit.</span><span class="sxs-lookup"><span data-stu-id="07792-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="07792-130">Üksikute väljade puhul saab logisse kanda ainult värskendusi.</span><span class="sxs-lookup"><span data-stu-id="07792-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="07792-131">Andmebaasi logimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="07792-131">Set up database logging</span></span>

<span data-ttu-id="07792-132">Andmebaasi logimise seadistamiseks saate kasutada viisardit **Andmebaasi muudatuste logimine**.</span><span class="sxs-lookup"><span data-stu-id="07792-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="07792-133">Viisard pakub paindlikku viisi tabelite või väljade logimise seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="07792-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="07792-134">Avage **Süsteemihaldus > Lingid > Andmebaas > Andmebaasilogi seadistus**.</span><span class="sxs-lookup"><span data-stu-id="07792-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="07792-135">Valige **Uus**, et käivitada viisard **Andmebaasi muudatuste logimine**.</span><span class="sxs-lookup"><span data-stu-id="07792-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="07792-136">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="07792-136">Select **Next**.</span></span> 
3. <span data-ttu-id="07792-137">Viisardi **Tabelite ja väljade** lehel valige tabelid ja väljad, millel soovite andmebaasi logimist toetada ja valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="07792-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="07792-138">Andmebaasi logimine ei ole saadaval kõigis inimressursside andmebaasi tabelites.</span><span class="sxs-lookup"><span data-stu-id="07792-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="07792-139">Valides **Näita kõiki tabeleid** loendi all laiendab tabelite ja väljade loendit, et näidata kõiki andmebaasi tabeleid, mille jaoks andmebaasi logimine on kättesaadav, aga see on täieliku andmebaasi tabelite alamkogum.</span><span class="sxs-lookup"><span data-stu-id="07792-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="07792-140">Viisardi **Muutuse tüübid** lehel valige andmeoperatsioonid mille jaoks te soovite iga tabeli ja välja jaoks muudatusi jälgida ja valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="07792-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="07792-141">Logimiseks saadavalolevate andmetoimingute kirjeldusi vt järgmisest tabelist.</span><span class="sxs-lookup"><span data-stu-id="07792-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="07792-142">Lehel **Lõpeta** vaadake tehtud muudatused üle ja valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="07792-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="07792-143">Toiming</span><span class="sxs-lookup"><span data-stu-id="07792-143">Operation</span></span> | <span data-ttu-id="07792-144">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="07792-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="07792-145">Jälgi uusi kandeid</span><span class="sxs-lookup"><span data-stu-id="07792-145">Track new transactions</span></span> | <span data-ttu-id="07792-146">Looge logi uutele tabelis loodud kirjetele.</span><span class="sxs-lookup"><span data-stu-id="07792-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="07792-147">Värskendus</span><span class="sxs-lookup"><span data-stu-id="07792-147">Update</span></span> | <span data-ttu-id="07792-148">Looge logi tabelikirjete uuenduste jaoks või värskendage tabeli üksikult valitud väljad.</span><span class="sxs-lookup"><span data-stu-id="07792-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="07792-149">Kui valite tabeli uuenduste logimise, luuakse logikirje iga kord, kui uuendatakse mis tahes tabeli kirje välja.</span><span class="sxs-lookup"><span data-stu-id="07792-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="07792-150">Kui valite logi uuendused konkreetsetele väljadele, luuakse logikirje ainult siis, kui neid tabelikirjete välju uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="07792-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="07792-151">Kustutamine</span><span class="sxs-lookup"><span data-stu-id="07792-151">Delete</span></span> | <span data-ttu-id="07792-152">Looge tabelist kustutatud kirjete logi.</span><span class="sxs-lookup"><span data-stu-id="07792-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="07792-153">Nimeta võti ümber</span><span class="sxs-lookup"><span data-stu-id="07792-153">Rename key</span></span> | <span data-ttu-id="07792-154">Logikirje loomine tabelivõtme ümbernimetamise korral.</span><span class="sxs-lookup"><span data-stu-id="07792-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="07792-155">Andmebaasilogide puhastamine</span><span class="sxs-lookup"><span data-stu-id="07792-155">Clean up database logs</span></span>

<span data-ttu-id="07792-156">Järgmiste võimaluste abil saate kustutada kõik andmebaasilogid või osa neist.</span><span class="sxs-lookup"><span data-stu-id="07792-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="07792-157">Valige kõik logid kindla tabeli jaoks.</span><span class="sxs-lookup"><span data-stu-id="07792-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="07792-158">Valige kindlat tüüpi andmebaasilogid.</span><span class="sxs-lookup"><span data-stu-id="07792-158">Select specific types of database log.</span></span>
- <span data-ttu-id="07792-159">Valige logi loomise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="07792-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="07792-160">Andmebaasilogi puhastamise seadistamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="07792-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="07792-161">Avage **Süsteemihaldus > Lingid > Andmebaas > Andmebaasilogi**.</span><span class="sxs-lookup"><span data-stu-id="07792-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="07792-162">Valige **Puhasta logi**.</span><span class="sxs-lookup"><span data-stu-id="07792-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="07792-163">Valige kustutamiseks mõeldud logide valimise meetod, sisestades ühe järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="07792-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="07792-164">Tabeli kood</span><span class="sxs-lookup"><span data-stu-id="07792-164">Table ID</span></span>
   - <span data-ttu-id="07792-165">Logi tüüp</span><span class="sxs-lookup"><span data-stu-id="07792-165">Type of log</span></span>
   - <span data-ttu-id="07792-166">Loomise kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="07792-166">Created date and time</span></span>

3. <span data-ttu-id="07792-167">Kasutage vahekaarti **Andmebaasilogi puhastamine**, et määrata, millal käitada logi puhastamise ülesanne.</span><span class="sxs-lookup"><span data-stu-id="07792-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="07792-168">Vaikimisi on andmebaasilogid saadaval 30 päeva.</span><span class="sxs-lookup"><span data-stu-id="07792-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
