---
title: Andmebaasi logimise konfigureerimine ja haldamine
description: Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.
author: Darinkramer
manager: AnnBe
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
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418152"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="d6d50-103">Andmebaasi logimise konfigureerimine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="d6d50-103">Configure and manage database logging</span></span>

<span data-ttu-id="d6d50-104">Andmebaasi logimise abil saate jälgida rakenduses Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.</span><span class="sxs-lookup"><span data-stu-id="d6d50-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="d6d50-105">Selles teemas käsitletakse järgmist.</span><span class="sxs-lookup"><span data-stu-id="d6d50-105">This topic describes how to:</span></span>

- <span data-ttu-id="d6d50-106">Andmebaasi logimise turbe ja jõudluse haldamine</span><span class="sxs-lookup"><span data-stu-id="d6d50-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="d6d50-107">Andmebaasi logimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d6d50-107">Set up database logging</span></span>
- <span data-ttu-id="d6d50-108">Andmebaasilogide puhastamine</span><span class="sxs-lookup"><span data-stu-id="d6d50-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="d6d50-109">Andmebaasi logimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="d6d50-109">Overview of database logging</span></span>

<span data-ttu-id="d6d50-110">Andmebaasi logimine jälgib rakenduse Microsoft Dynamics 365 Human Resources tabelite ja väljade muudatusi.</span><span class="sxs-lookup"><span data-stu-id="d6d50-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="d6d50-111">Need muudatused hõlmavad lisamist, värskendamist või kustutamist.</span><span class="sxs-lookup"><span data-stu-id="d6d50-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="d6d50-112">Andmebaasi logimine salvestab tabeli või väljade muudatused andmebaasilogi tabelisse.</span><span class="sxs-lookup"><span data-stu-id="d6d50-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="d6d50-113">Andmebaasi logimise äriline kasutus hõlmab järgmist.</span><span class="sxs-lookup"><span data-stu-id="d6d50-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="d6d50-114">Auditikirje loomine kindlate tundlikku teavet sisaldavate tabelite muudatuste kohta.</span><span class="sxs-lookup"><span data-stu-id="d6d50-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="d6d50-115">Üksikute kannete jälgimine.</span><span class="sxs-lookup"><span data-stu-id="d6d50-115">Tracking single transactions.</span></span> <span data-ttu-id="d6d50-116">Andmebaasi logimine ei ole mõeldud pakett-töödes tehtavate automatiseeritud kannete jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="d6d50-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="d6d50-117">Andmebaasi logimise turve</span><span class="sxs-lookup"><span data-stu-id="d6d50-117">Security for database logging</span></span>

<span data-ttu-id="d6d50-118">Andmebaasilogid võivad sisaldada tundlikke andmeid.</span><span class="sxs-lookup"><span data-stu-id="d6d50-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="d6d50-119">Andke juurdepääs ainult sellistele turberollidele, mis vajavad logiandmetele juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="d6d50-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="d6d50-120">Andmebaasi logimine ja jõudlus</span><span class="sxs-lookup"><span data-stu-id="d6d50-120">Database logging and performance</span></span>

<span data-ttu-id="d6d50-121">Kuigi see on väärtuslik ärilisest vaatenurgast, võib andmebaasi logimine olla kulukas ressursikasutuse ja -halduse mõttes.</span><span class="sxs-lookup"><span data-stu-id="d6d50-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="d6d50-122">Andmebaasi logimise jõudluse tagajärjed hõlmavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="d6d50-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="d6d50-123">Andmebaasilogi tabel võib kasvada kiiresti ja põhjustada andmebaasi suurenemise.</span><span class="sxs-lookup"><span data-stu-id="d6d50-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="d6d50-124">Kasv sõltub logitud andmete hulgas, mida te otsustate säilitada.</span><span class="sxs-lookup"><span data-stu-id="d6d50-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="d6d50-125">Andmebaasilogi tabel säilitab vaikimisi ainult 30 päeva logiandmed.</span><span class="sxs-lookup"><span data-stu-id="d6d50-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="d6d50-126">Andmebaasi logimine võib negatiivselt mõjutada pikaajalisi automatiseeritud protsesse, näiteks pikaajalist andmete importimist.</span><span class="sxs-lookup"><span data-stu-id="d6d50-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="d6d50-127">Head tavad</span><span class="sxs-lookup"><span data-stu-id="d6d50-127">Best practices</span></span>

<span data-ttu-id="d6d50-128">Jõudluse parandamiseks piirake logikirjeid, valides logimiseks tervete tabelite asemel konkreetsed väljad.</span><span class="sxs-lookup"><span data-stu-id="d6d50-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="d6d50-129">Üldise jõudluse säilitamiseks saab andmebaasi logimine logida kuni 20 tabelit.</span><span class="sxs-lookup"><span data-stu-id="d6d50-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="d6d50-130">Üksikute väljade puhul saab logisse kanda ainult värskendusi.</span><span class="sxs-lookup"><span data-stu-id="d6d50-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="d6d50-131">Andmebaasi logimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d6d50-131">Set up database logging</span></span>

<span data-ttu-id="d6d50-132">Andmebaasi logimise seadistamiseks saate kasutada viisardit **Andmebaasi muudatuste logimine**.</span><span class="sxs-lookup"><span data-stu-id="d6d50-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="d6d50-133">Viisard pakub paindlikku viisi tabelite või väljade logimise seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="d6d50-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="d6d50-134">Avage **Süsteemihaldus > Lingid > Andmebaas > Andmebaasilogi seadistus**.</span><span class="sxs-lookup"><span data-stu-id="d6d50-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="d6d50-135">Valige **Uus**, et käivitada viisard **Andmebaasi muudatuste logimine**.</span><span class="sxs-lookup"><span data-stu-id="d6d50-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="d6d50-136">Täitke viisardi juhised.</span><span class="sxs-lookup"><span data-stu-id="d6d50-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="d6d50-137">Andmebaasilogide puhastamine</span><span class="sxs-lookup"><span data-stu-id="d6d50-137">Clean up database logs</span></span>

<span data-ttu-id="d6d50-138">Järgmiste võimaluste abil saate kustutada kõik andmebaasilogid või osa neist.</span><span class="sxs-lookup"><span data-stu-id="d6d50-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="d6d50-139">Valige kõik logid kindla tabeli jaoks.</span><span class="sxs-lookup"><span data-stu-id="d6d50-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="d6d50-140">Valige kindlat tüüpi andmebaasilogid.</span><span class="sxs-lookup"><span data-stu-id="d6d50-140">Select specific types of database log.</span></span>
- <span data-ttu-id="d6d50-141">Valige logi loomise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="d6d50-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="d6d50-142">Andmebaasilogi puhastamise seadistamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="d6d50-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="d6d50-143">Avage **Süsteemihaldus > Lingid > Andmebaas > Andmebaasilogi**.</span><span class="sxs-lookup"><span data-stu-id="d6d50-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="d6d50-144">Valige **Puhasta logi**.</span><span class="sxs-lookup"><span data-stu-id="d6d50-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="d6d50-145">Valige kustutamiseks mõeldud logide valimise meetod, sisestades ühe järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="d6d50-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="d6d50-146">Tabeli kood</span><span class="sxs-lookup"><span data-stu-id="d6d50-146">Table ID</span></span>
   - <span data-ttu-id="d6d50-147">Logi tüüp</span><span class="sxs-lookup"><span data-stu-id="d6d50-147">Type of log</span></span>
   - <span data-ttu-id="d6d50-148">Loomise kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="d6d50-148">Created date and time</span></span>

3. <span data-ttu-id="d6d50-149">Kasutage vahekaarti **Andmebaasilogi puhastamine**, et määrata, millal käitada logi puhastamise ülesanne.</span><span class="sxs-lookup"><span data-stu-id="d6d50-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="d6d50-150">Vaikimisi on andmebaasilogid saadaval 30 päeva.</span><span class="sxs-lookup"><span data-stu-id="d6d50-150">By default, database logs are available for 30 days.</span></span>
