---
title: Andmebaasi logimise konfigureerimine ja haldamine
description: Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50346cc495fe08f49137dba59dbcbb3f7f838c7b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129275"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="48b41-103">Andmebaasi logimise konfigureerimine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="48b41-103">Configure and manage database logging</span></span>

<span data-ttu-id="48b41-104">Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.</span><span class="sxs-lookup"><span data-stu-id="48b41-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="48b41-105">Selles teemas käsitletakse järgmist.</span><span class="sxs-lookup"><span data-stu-id="48b41-105">This topic describes how to:</span></span>

- <span data-ttu-id="48b41-106">Andmebaasi logimise turbe ja jõudluse haldamine</span><span class="sxs-lookup"><span data-stu-id="48b41-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="48b41-107">Andmebaasi logimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="48b41-107">Set up database logging</span></span>
- <span data-ttu-id="48b41-108">Andmebaasilogide puhastamine</span><span class="sxs-lookup"><span data-stu-id="48b41-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="48b41-109">Andmebaasi logimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="48b41-109">Overview of database logging</span></span>

<span data-ttu-id="48b41-110">Andmebaasi logimine jälgib rakenduse Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.</span><span class="sxs-lookup"><span data-stu-id="48b41-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="48b41-111">Need muudatused hõlmavad lisamist, värskendamist või kustutamist.</span><span class="sxs-lookup"><span data-stu-id="48b41-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="48b41-112">Andmebaasi logimine salvestab tabeli või väljade muudatused andmebaasilogi tabelisse.</span><span class="sxs-lookup"><span data-stu-id="48b41-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="48b41-113">Andmebaasi logimise äriline kasutus hõlmab järgmist.</span><span class="sxs-lookup"><span data-stu-id="48b41-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="48b41-114">Auditikirje loomine kindlate tundlikku teavet sisaldavate tabelite muudatuste kohta.</span><span class="sxs-lookup"><span data-stu-id="48b41-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="48b41-115">Üksikute kannete jälgimine.</span><span class="sxs-lookup"><span data-stu-id="48b41-115">Tracking single transactions.</span></span> <span data-ttu-id="48b41-116">Andmebaasi logimine ei ole mõeldud pakett-töödes tehtavate automatiseeritud kannete jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="48b41-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="48b41-117">Andmebaasi logimise turve</span><span class="sxs-lookup"><span data-stu-id="48b41-117">Security for database logging</span></span>

<span data-ttu-id="48b41-118">Andmebaasilogid võivad sisaldada tundlikke andmeid.</span><span class="sxs-lookup"><span data-stu-id="48b41-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="48b41-119">Andke juurdepääs ainult sellistele turberollidele, mis vajavad logiandmetele juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="48b41-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="48b41-120">Andmebaasi logimine ja jõudlus</span><span class="sxs-lookup"><span data-stu-id="48b41-120">Database logging and performance</span></span>

<span data-ttu-id="48b41-121">Kuigi see on väärtuslik ärilisest vaatenurgast, võib andmebaasi logimine olla kulukas ressursikasutuse ja -halduse mõttes.</span><span class="sxs-lookup"><span data-stu-id="48b41-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="48b41-122">Andmebaasi logimise jõudluse tagajärjed hõlmavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="48b41-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="48b41-123">Andmebaasilogi tabel võib kasvada kiiresti ja põhjustada andmebaasi suurenemise.</span><span class="sxs-lookup"><span data-stu-id="48b41-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="48b41-124">Kasv sõltub logitud andmete hulgas, mida te otsustate säilitada.</span><span class="sxs-lookup"><span data-stu-id="48b41-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="48b41-125">Andmebaasilogi tabel säilitab vaikimisi ainult 30 päeva logiandmed.</span><span class="sxs-lookup"><span data-stu-id="48b41-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="48b41-126">Andmebaasi logimine võib negatiivselt mõjutada pikaajalisi automatiseeritud protsesse, näiteks pikaajalist andmete importimist.</span><span class="sxs-lookup"><span data-stu-id="48b41-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="48b41-127">Head tavad</span><span class="sxs-lookup"><span data-stu-id="48b41-127">Best practices</span></span>

<span data-ttu-id="48b41-128">Jõudluse parandamiseks piirake logikirjeid, valides logimiseks tervete tabelite asemel konkreetsed väljad.</span><span class="sxs-lookup"><span data-stu-id="48b41-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="48b41-129">Üldise jõudluse säilitamiseks saab andmebaasi logimine logida kuni 20 tabelit.</span><span class="sxs-lookup"><span data-stu-id="48b41-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="48b41-130">Üksikute väljade puhul saab logisse kanda ainult värskendusi.</span><span class="sxs-lookup"><span data-stu-id="48b41-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="48b41-131">Andmebaasi logimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="48b41-131">Set up database logging</span></span>

<span data-ttu-id="48b41-132">Andmebaasi logimise seadistamiseks saate kasutada viisardit **Andmebaasi muudatuste logimine**.</span><span class="sxs-lookup"><span data-stu-id="48b41-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="48b41-133">Viisard pakub paindlikku viisi tabelite või väljade logimise seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="48b41-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="48b41-134">Avage **Süsteemihaldus > Lingid > Andmebaas > Andmebaasilogi seadistus**.</span><span class="sxs-lookup"><span data-stu-id="48b41-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="48b41-135">Valige **Uus**, et käivitada viisard **Andmebaasi muudatuste logimine**.</span><span class="sxs-lookup"><span data-stu-id="48b41-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="48b41-136">Täitke viisardi juhised.</span><span class="sxs-lookup"><span data-stu-id="48b41-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="48b41-137">Andmebaasilogide puhastamine</span><span class="sxs-lookup"><span data-stu-id="48b41-137">Clean up database logs</span></span>

<span data-ttu-id="48b41-138">Järgmiste võimaluste abil saate kustutada kõik andmebaasilogid või osa neist.</span><span class="sxs-lookup"><span data-stu-id="48b41-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="48b41-139">Valige kõik logid kindla tabeli jaoks.</span><span class="sxs-lookup"><span data-stu-id="48b41-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="48b41-140">Valige kindlat tüüpi andmebaasilogid.</span><span class="sxs-lookup"><span data-stu-id="48b41-140">Select specific types of database log.</span></span>
- <span data-ttu-id="48b41-141">Valige logi loomise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="48b41-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="48b41-142">Andmebaasilogi puhastamise seadistamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="48b41-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="48b41-143">Avage **Süsteemihaldus > Lingid > Andmebaas > Andmebaasilogi**.</span><span class="sxs-lookup"><span data-stu-id="48b41-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="48b41-144">Valige **Puhasta logi**.</span><span class="sxs-lookup"><span data-stu-id="48b41-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="48b41-145">Valige kustutamiseks mõeldud logide valimise meetod, sisestades ühe järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="48b41-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="48b41-146">Tabeli kood</span><span class="sxs-lookup"><span data-stu-id="48b41-146">Table ID</span></span>
   - <span data-ttu-id="48b41-147">Logi tüüp</span><span class="sxs-lookup"><span data-stu-id="48b41-147">Type of log</span></span>
   - <span data-ttu-id="48b41-148">Loomise kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="48b41-148">Created date and time</span></span>

3. <span data-ttu-id="48b41-149">Kasutage vahekaarti **Andmebaasilogi puhastamine**, et määrata, millal käitada logi puhastamise ülesanne.</span><span class="sxs-lookup"><span data-stu-id="48b41-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="48b41-150">Vaikimisi on andmebaasilogid saadaval 30 päeva.</span><span class="sxs-lookup"><span data-stu-id="48b41-150">By default, database logs are available for 30 days.</span></span>
