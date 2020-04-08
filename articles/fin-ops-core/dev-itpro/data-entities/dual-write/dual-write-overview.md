---
title: Topeltkirjutuse ülevaade
description: See teema annab topeltkirjutamisest ülevaate. Topeltkirjutus on infrastruktuur, mis pakub reaalaja lähedast suhtlust Microsoft Dynamics 365 mudelipõhiste rakenduste ja Finance and Operationsi rakenduste vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172780"
---
# <a name="dual-write-overview"></a><span data-ttu-id="72b4b-104">Topeltkirjutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="72b4b-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="72b4b-105">Mis on topeltkirjutus?</span><span class="sxs-lookup"><span data-stu-id="72b4b-105">What is dual-write?</span></span>

<span data-ttu-id="72b4b-106">Topeltkirjutus on valmiskujul infrastruktuur, mis pakub reaalaja lähedast suhtlust Microsoft Dynamics 365 mudelipõhiste rakenduste ja Finance and Operationsi rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="72b4b-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="72b4b-107">Kui andmed klientide, toodete, inimeste ja operatsioonide kohta liiguvad rakenduse piiridest välja, omavad organisatsiooni kõik osakonnad võimalust.</span><span class="sxs-lookup"><span data-stu-id="72b4b-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="72b4b-108">Topeltkirjutus pakub tihedalt ühendatud, kahesuunalist integratsiooni Finance and Operationsi rakenduste ja teenuse Common Data Service vahel.</span><span class="sxs-lookup"><span data-stu-id="72b4b-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="72b4b-109">Mis tahes andmete muudatus Finance and Operationsi rakendustes põhjustab kirjutamist teenusesse Common Data Service ja mis tahes andmete muudatused teenuses Common Data Service põhjustab kirjutamist Finance and Operationsi rakendustesse.</span><span class="sxs-lookup"><span data-stu-id="72b4b-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="72b4b-110">See automatiseeritud andmevoog pakub rakenduste vahel integreeritud kasutuskogemust.</span><span class="sxs-lookup"><span data-stu-id="72b4b-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Andmete seos rakenduste vahel](media/dual-write-overview.jpg)

<span data-ttu-id="72b4b-112">Topeltkirjutusel on kaks aspekti: *taristu* aspekt ja *rakenduse* aspekt.</span><span class="sxs-lookup"><span data-stu-id="72b4b-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="72b4b-113">Taristu</span><span class="sxs-lookup"><span data-stu-id="72b4b-113">Infrastructure</span></span>

<span data-ttu-id="72b4b-114">Topeltkirjutuse taristu on laiendatav ja usaldusväärne ning sisaldab järgmisi põhifunktsioone.</span><span class="sxs-lookup"><span data-stu-id="72b4b-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="72b4b-115">Sünkroonne ja kahesuunaline andmeedastus rakenduste vahel</span><span class="sxs-lookup"><span data-stu-id="72b4b-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="72b4b-116">Sünkroonimine koos esituse, peatamise ja järele jõudmise režiimidega, et toetada süsteemi veebipõhiste ja veebiväliste/asünkroonsete režiimide ajal.</span><span class="sxs-lookup"><span data-stu-id="72b4b-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="72b4b-117">Võime sünkroonida algandmeid rakenduste vahel</span><span class="sxs-lookup"><span data-stu-id="72b4b-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="72b4b-118">Tegevuse ja vigade logide konsolideeritud vaade andmete administraatoritele</span><span class="sxs-lookup"><span data-stu-id="72b4b-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="72b4b-119">Võime konfigureerida kohandatud teatisi ja lävendeid ning tellida teatisi</span><span class="sxs-lookup"><span data-stu-id="72b4b-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="72b4b-120">Intuitiivne kasutajaliides (UI) filtreerimiseks ja teisendusteks</span><span class="sxs-lookup"><span data-stu-id="72b4b-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="72b4b-121">Võime määrata ja kuvada üksuse sõltuvusi ja seoseid</span><span class="sxs-lookup"><span data-stu-id="72b4b-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="72b4b-122">Laiendatavus nii standardsete kui ka kohandatud üksuste ja kaartide jaoks</span><span class="sxs-lookup"><span data-stu-id="72b4b-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="72b4b-123">Usaldusväärne rakenduse elutsükli haldus</span><span class="sxs-lookup"><span data-stu-id="72b4b-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="72b4b-124">Valmiskujul seadistuse kogemus uutele klientidele</span><span class="sxs-lookup"><span data-stu-id="72b4b-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="72b4b-125">Avaldus</span><span class="sxs-lookup"><span data-stu-id="72b4b-125">Application</span></span>

<span data-ttu-id="72b4b-126">Topeltkirjutus loob vastenduse Finance and Operationsi rakenduste kontseptsioonide ja Dynamics 365 mudelipõhiste rakenduste kontseptsioonide vahel.</span><span class="sxs-lookup"><span data-stu-id="72b4b-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="72b4b-127">See integratsioon toetab järgmisi stsenaariumeid.</span><span class="sxs-lookup"><span data-stu-id="72b4b-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="72b4b-128">Integreeritud kliendi koondandmed</span><span class="sxs-lookup"><span data-stu-id="72b4b-128">Integrated customer master</span></span>
+ <span data-ttu-id="72b4b-129">Juurdepääs kliendi kliendikaartidele ja preemiapunktidele</span><span class="sxs-lookup"><span data-stu-id="72b4b-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="72b4b-130">Ühendatud tooteetaloni kasutusfunktsionaalsus</span><span class="sxs-lookup"><span data-stu-id="72b4b-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="72b4b-131">Organisatsiooni hierarhia teadlikkus</span><span class="sxs-lookup"><span data-stu-id="72b4b-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="72b4b-132">Integreeritud hankija koondandmed</span><span class="sxs-lookup"><span data-stu-id="72b4b-132">Integrated vendor master</span></span>
+ <span data-ttu-id="72b4b-133">Juurdepääs finantsilistele ja maksude viiteandmetele</span><span class="sxs-lookup"><span data-stu-id="72b4b-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="72b4b-134">Nõudmisel hinnakujunduse mootori kogemus</span><span class="sxs-lookup"><span data-stu-id="72b4b-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="72b4b-135">Integreeritud potentsiaalse kliendi sularaha kogemus</span><span class="sxs-lookup"><span data-stu-id="72b4b-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="72b4b-136">Võime teenindada nii majasiseseid varasid kui ka väliagentide kaudu kliendi varasid</span><span class="sxs-lookup"><span data-stu-id="72b4b-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="72b4b-137">Integreeritud maksmiseks hankimise kogemus</span><span class="sxs-lookup"><span data-stu-id="72b4b-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="72b4b-138">Kliendiandmetele ja dokumentide integreeritud tegevused ja märkused</span><span class="sxs-lookup"><span data-stu-id="72b4b-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="72b4b-139">Võimalus otsida vabade varade saadavust ja üksikasju</span><span class="sxs-lookup"><span data-stu-id="72b4b-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="72b4b-140">Projektist sularahaks kogemus</span><span class="sxs-lookup"><span data-stu-id="72b4b-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="72b4b-141">Võime käsitseda osapoole kontseptsiooni kaudu mitut aadressi ja rolli</span><span class="sxs-lookup"><span data-stu-id="72b4b-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="72b4b-142">Kasutajate ühe allika haldamine</span><span class="sxs-lookup"><span data-stu-id="72b4b-142">Single source management for users</span></span>
+ <span data-ttu-id="72b4b-143">Jaemüügi ja turunduse integreeritud kanalid</span><span class="sxs-lookup"><span data-stu-id="72b4b-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="72b4b-144">Kampaaniate ja allahindluste nähtavus</span><span class="sxs-lookup"><span data-stu-id="72b4b-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="72b4b-145">Teenusetaotluse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="72b4b-145">Request-for-service functions</span></span>
+ <span data-ttu-id="72b4b-146">Sujuvad teenusetoimingud</span><span class="sxs-lookup"><span data-stu-id="72b4b-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="72b4b-147">Topeltkirjutuse kasutamise peamised põhjused</span><span class="sxs-lookup"><span data-stu-id="72b4b-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="72b4b-148">Topeltkirjutus võimaldab Microsoft Dynamics 365 rakenduste üleselt andmete integreerimist.</span><span class="sxs-lookup"><span data-stu-id="72b4b-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="72b4b-149">See jõuline raamistik ühendab keskkondasid ja võimaldab erinevatel ärirakendustel koos töötada.</span><span class="sxs-lookup"><span data-stu-id="72b4b-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="72b4b-150">Siin on peamised põhjused, miks peaksite topeltkirjutust kasutama.</span><span class="sxs-lookup"><span data-stu-id="72b4b-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="72b4b-151">Topeltkirjutus pakub tihedalt ühendatud, peaaegu reaalajas ja kahesuunalist integratsiooni Finance and Operationsi rakenduste ja Dynamics 365 mudelipõhiste rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="72b4b-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="72b4b-152">See integratsioon muudab Microsoft Dynamics 365 ühe peatuse poeks kõigi teie ärilahenduste jaoks.</span><span class="sxs-lookup"><span data-stu-id="72b4b-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="72b4b-153">Kliendid, kes kasutavad rakendusi Dynamics 365 Finance ja Dynamics 365 Supply Chain Management, kuid kasutavad kliendisuhte halduseks (CRM) mitte-Microsofti lahendusi, liiguvad Dynamics 365 suunas selle topeltkirjutamise toe jaoks.</span><span class="sxs-lookup"><span data-stu-id="72b4b-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="72b4b-154">Klientide, toodete, operatsioonide, projektide ja asjade Interneti (IoT) andmed voolavad automaatselt topeltkirjutuse kaudu teenusesse Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="72b4b-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="72b4b-155">See ühendus on väga kasulik ettevõtetele, kes on huvitatud Microsoft Power Platformi laiendustest.</span><span class="sxs-lookup"><span data-stu-id="72b4b-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="72b4b-156">Topeltkirjutuse infrastruktuur järgib puuduva koodi / vähese koodi põhimõtet.</span><span class="sxs-lookup"><span data-stu-id="72b4b-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="72b4b-157">Standardsete tabelist tabelisse kaartide laiendamiseks ja kohandatud kaartide kaasamiseks on vajalik minimaalne projekteerimise panus.</span><span class="sxs-lookup"><span data-stu-id="72b4b-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="72b4b-158">Topeltkirjutus toetab nii ühendusega režiimi kui ka võrguühenduseta režiimi.</span><span class="sxs-lookup"><span data-stu-id="72b4b-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="72b4b-159">Microsoft on ainus ettevõte, mis pakub ühendusega ja võrguühenduseta režiimide tuge.</span><span class="sxs-lookup"><span data-stu-id="72b4b-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="72b4b-160">Mida tähendab topeltkirjutus CRM-i toodete kasutajate ja arhitektide jaoks?</span><span class="sxs-lookup"><span data-stu-id="72b4b-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="72b4b-161">Topeltkirjutus automatiseerib andmevoo Finance and Operationsi rakenduste ja teenuse Common Data Service vahel.</span><span class="sxs-lookup"><span data-stu-id="72b4b-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="72b4b-162">Tulevastes väljaannetes on Dynamics 365 mudelipõhiste rakenduste kontseptsioonid (nt klient, kontakt, pakkumine ja tellimus) muudetud keskmise turu ja ülemise keskmise turu klientidele sobivaks.</span><span class="sxs-lookup"><span data-stu-id="72b4b-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="72b4b-163">Esimeses väljalaskes käsitsevad enamikku automatiseerimisest topeltkirjutuse lahendused.</span><span class="sxs-lookup"><span data-stu-id="72b4b-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="72b4b-164">Tulevastes väljaannetes muutuvad need lahendused teenuse Common Data Service osaks.</span><span class="sxs-lookup"><span data-stu-id="72b4b-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="72b4b-165">Teenuse Common Data Service tulevaste muudatuste mõistmisega saate pikemas perspektiivis oma jõupingutusi säästa.</span><span class="sxs-lookup"><span data-stu-id="72b4b-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="72b4b-166">Siin on mõned uued olulised muudatused.</span><span class="sxs-lookup"><span data-stu-id="72b4b-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="72b4b-167">Common Data Service omab uusi kontseptsioone, nt ettevõte ja osapool.</span><span class="sxs-lookup"><span data-stu-id="72b4b-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="72b4b-168">Need kontseptsioonid mõjutavad kõiki rakendusi, mis on teenuse Common Data Service peale ehitatud, nagu Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ja Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="72b4b-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="72b4b-169">Tegevused ja märkmed on ühtlustatud ning laiendatud, et toetada nii C1-sid (süsteemi kasutajaid) kui ka C2-sid (süsteemi kliendid).</span><span class="sxs-lookup"><span data-stu-id="72b4b-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="72b4b-170">Siin on mõned teenuse Common Data Service tulevased muudatused.</span><span class="sxs-lookup"><span data-stu-id="72b4b-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="72b4b-171">Kümnendkoha andmetüüp asendab raha andmetüübi.</span><span class="sxs-lookup"><span data-stu-id="72b4b-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="72b4b-172">Kuupäeva jõustumine toetab samas kohas mineviku, oleviku ja tuleviku andmeid.</span><span class="sxs-lookup"><span data-stu-id="72b4b-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="72b4b-173">Valuuta ja vahetuskursside jaoks on rohkem tuge ning rakenduse programmeerimisliides (API) **Vahetuskurss** vaadatakse üle.</span><span class="sxs-lookup"><span data-stu-id="72b4b-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="72b4b-174">Toetatakse ühiku teisendusi.</span><span class="sxs-lookup"><span data-stu-id="72b4b-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="72b4b-175">Lisateavet eelseisvate muudatuste kohta vt teemast [Teenuse Common Data Service andmed – 1. ja 2. faas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span><span class="sxs-lookup"><span data-stu-id="72b4b-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>
