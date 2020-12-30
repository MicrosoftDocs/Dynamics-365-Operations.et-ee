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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 85530cf644c7b7ffe922a6fb3288f4e05c5df91c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685609"
---
# <a name="dual-write-overview"></a><span data-ttu-id="2f780-104">Topeltkirjutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="2f780-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="2f780-105">Mis on topeltkirjutus?</span><span class="sxs-lookup"><span data-stu-id="2f780-105">What is dual-write?</span></span>

<span data-ttu-id="2f780-106">Topeltkirjutus on valmiskujul infrastruktuur, mis pakub reaalaja lähedast suhtlust klientide kaasamise rakenduste ja Finance and Operationsi rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="2f780-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="2f780-107">Kui andmed klientide, toodete, inimeste ja operatsioonide kohta liiguvad rakenduse piiridest välja, omavad organisatsiooni kõik osakonnad võimalust.</span><span class="sxs-lookup"><span data-stu-id="2f780-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="2f780-108">Topeltkirjutus pakub tihedalt ühendatud, kahesuunalist integratsiooni Finance and Operationsi rakenduste ja teenuse Dataverse vahel.</span><span class="sxs-lookup"><span data-stu-id="2f780-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="2f780-109">Mis tahes andmete muudatus Finance and Operationsi rakendustes põhjustab kirjutamist teenusesse Dataverse ja mis tahes andmete muudatused teenuses Dataverse põhjustab kirjutamist Finance and Operationsi rakendustesse.</span><span class="sxs-lookup"><span data-stu-id="2f780-109">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="2f780-110">See automatiseeritud andmevoog pakub rakenduste vahel integreeritud kasutuskogemust.</span><span class="sxs-lookup"><span data-stu-id="2f780-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Andmete seos rakenduste vahel](media/dual-write-overview.jpg)

<span data-ttu-id="2f780-112">Topeltkirjutusel on kaks aspekti: *taristu* aspekt ja *rakenduse* aspekt.</span><span class="sxs-lookup"><span data-stu-id="2f780-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="2f780-113">Taristu</span><span class="sxs-lookup"><span data-stu-id="2f780-113">Infrastructure</span></span>

<span data-ttu-id="2f780-114">Topeltkirjutuse taristu on laiendatav ja usaldusväärne ning sisaldab järgmisi põhifunktsioone.</span><span class="sxs-lookup"><span data-stu-id="2f780-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="2f780-115">Sünkroonne ja kahesuunaline andmeedastus rakenduste vahel</span><span class="sxs-lookup"><span data-stu-id="2f780-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="2f780-116">Sünkroonimine koos esituse, peatamise ja järele jõudmise režiimidega, et toetada süsteemi veebipõhiste ja veebiväliste/asünkroonsete režiimide ajal.</span><span class="sxs-lookup"><span data-stu-id="2f780-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="2f780-117">Võime sünkroonida algandmeid rakenduste vahel</span><span class="sxs-lookup"><span data-stu-id="2f780-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="2f780-118">Tegevuse ja vigade logide kombineeritud vaade andmete administraatoritele</span><span class="sxs-lookup"><span data-stu-id="2f780-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="2f780-119">Võime konfigureerida kohandatud teatisi ja lävendeid ning tellida teatisi</span><span class="sxs-lookup"><span data-stu-id="2f780-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="2f780-120">Intuitiivne kasutajaliides (UI) filtreerimiseks ja teisendusteks</span><span class="sxs-lookup"><span data-stu-id="2f780-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="2f780-121">Võime määrata ja kuvada üksuse sõltuvusi ja seoseid</span><span class="sxs-lookup"><span data-stu-id="2f780-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="2f780-122">Laiendatavus nii standardsete kui ka kohandatud tabelite ja kaartide jaoks</span><span class="sxs-lookup"><span data-stu-id="2f780-122">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="2f780-123">Usaldusväärne rakenduse elutsükli haldus</span><span class="sxs-lookup"><span data-stu-id="2f780-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="2f780-124">Valmiskujul seadistuse kogemus uutele klientidele</span><span class="sxs-lookup"><span data-stu-id="2f780-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="2f780-125">Avaldus</span><span class="sxs-lookup"><span data-stu-id="2f780-125">Application</span></span>

<span data-ttu-id="2f780-126">Topeltkirjutus loob vastenduse Finance and Operationsi rakenduste kontseptsioonide ja klientide kaasamise rakenduste kontseptsioonide vahel.</span><span class="sxs-lookup"><span data-stu-id="2f780-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="2f780-127">See integratsioon toetab järgmisi stsenaariumeid.</span><span class="sxs-lookup"><span data-stu-id="2f780-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="2f780-128">Integreeritud kliendi koondandmed</span><span class="sxs-lookup"><span data-stu-id="2f780-128">Integrated customer master</span></span>
+ <span data-ttu-id="2f780-129">Juurdepääs kliendi kliendikaartidele ja preemiapunktidele</span><span class="sxs-lookup"><span data-stu-id="2f780-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="2f780-130">Ühendatud tooteetaloni kasutusfunktsionaalsus</span><span class="sxs-lookup"><span data-stu-id="2f780-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="2f780-131">Organisatsiooni hierarhia teadlikkus</span><span class="sxs-lookup"><span data-stu-id="2f780-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="2f780-132">Integreeritud hankija koondandmed</span><span class="sxs-lookup"><span data-stu-id="2f780-132">Integrated vendor master</span></span>
+ <span data-ttu-id="2f780-133">Juurdepääs finantsilistele ja maksude viiteandmetele</span><span class="sxs-lookup"><span data-stu-id="2f780-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="2f780-134">Nõudmisel hinnakujunduse mootori kogemus</span><span class="sxs-lookup"><span data-stu-id="2f780-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="2f780-135">Integreeritud potentsiaalse kliendi sularaha kogemus</span><span class="sxs-lookup"><span data-stu-id="2f780-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="2f780-136">Võime teenindada nii majasiseseid varasid kui ka väliagentide kaudu kliendi varasid</span><span class="sxs-lookup"><span data-stu-id="2f780-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="2f780-137">Integreeritud maksmiseks hankimise kogemus</span><span class="sxs-lookup"><span data-stu-id="2f780-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="2f780-138">Kliendiandmetele ja dokumentide integreeritud tegevused ja märkused</span><span class="sxs-lookup"><span data-stu-id="2f780-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="2f780-139">Võimalus otsida vabade varade saadavust ja üksikasju</span><span class="sxs-lookup"><span data-stu-id="2f780-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="2f780-140">Projektist sularahaks kogemus</span><span class="sxs-lookup"><span data-stu-id="2f780-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="2f780-141">Võime käsitseda osapoole kontseptsiooni kaudu mitut aadressi ja rolli</span><span class="sxs-lookup"><span data-stu-id="2f780-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="2f780-142">Kasutajate ühe allika haldamine</span><span class="sxs-lookup"><span data-stu-id="2f780-142">Single source management for users</span></span>
+ <span data-ttu-id="2f780-143">Jaemüügi ja turunduse integreeritud kanalid</span><span class="sxs-lookup"><span data-stu-id="2f780-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="2f780-144">Kampaaniate ja allahindluste nähtavus</span><span class="sxs-lookup"><span data-stu-id="2f780-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="2f780-145">Teenusetaotluse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="2f780-145">Request-for-service functions</span></span>
+ <span data-ttu-id="2f780-146">Sujuvad teenusetoimingud</span><span class="sxs-lookup"><span data-stu-id="2f780-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="2f780-147">Topeltkirjutuse kasutamise peamised põhjused</span><span class="sxs-lookup"><span data-stu-id="2f780-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="2f780-148">Topeltkirjutus võimaldab Microsoft Dynamics 365 rakenduste üleselt andmete integreerimist.</span><span class="sxs-lookup"><span data-stu-id="2f780-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="2f780-149">See jõuline raamistik ühendab keskkondasid ja võimaldab erinevatel ärirakendustel koos töötada.</span><span class="sxs-lookup"><span data-stu-id="2f780-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="2f780-150">Siin on peamised põhjused, miks peaksite topeltkirjutust kasutama.</span><span class="sxs-lookup"><span data-stu-id="2f780-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="2f780-151">Topeltkirjutus pakub tihedalt ühendatud, peaaegu reaalajas ja kahesuunalist integratsiooni Finance and Operationsi rakenduste ja Dynamics 365 mudelipõhiste rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="2f780-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="2f780-152">See integratsioon muudab Microsoft Dynamics 365 ühe peatuse poeks kõigi teie ärilahenduste jaoks.</span><span class="sxs-lookup"><span data-stu-id="2f780-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="2f780-153">Kliendid, kes kasutavad rakendusi Dynamics 365 Finance ja Dynamics 365 Supply Chain Management, kuid kasutavad kliendisuhte halduseks (CRM) mitte-Microsofti lahendusi, liiguvad Dynamics 365 suunas selle topeltkirjutamise toe jaoks.</span><span class="sxs-lookup"><span data-stu-id="2f780-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="2f780-154">Klientide, toodete, operatsioonide, projektide ja asjade Interneti (IoT) andmed voolavad automaatselt topeltkirjutuse kaudu teenusesse Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2f780-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="2f780-155">See ühendus on kasulik ettevõtetele, kes on huvitatud Power Platformi laiendustest.</span><span class="sxs-lookup"><span data-stu-id="2f780-155">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="2f780-156">Topeltkirjutuse infrastruktuur järgib puuduva koodi / vähese koodi põhimõtet.</span><span class="sxs-lookup"><span data-stu-id="2f780-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="2f780-157">Standardsete tabelist tabelisse kaartide laiendamiseks ja kohandatud kaartide kaasamiseks on vajalik minimaalne projekteerimise panus.</span><span class="sxs-lookup"><span data-stu-id="2f780-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="2f780-158">Topeltkirjutus toetab nii ühendusega režiimi kui ka võrguühenduseta režiimi.</span><span class="sxs-lookup"><span data-stu-id="2f780-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="2f780-159">Microsoft on ainus ettevõte, mis pakub ühendusega ja võrguühenduseta režiimide tuge.</span><span class="sxs-lookup"><span data-stu-id="2f780-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="2f780-160">Mida tähendab topeltkirjutus klientide kaasamise rakenduste arendajate ja arhitektide jaoks?</span><span class="sxs-lookup"><span data-stu-id="2f780-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="2f780-161">Topeltkirjutus automatiseerib andmevoo Finance and Operationsi rakenduste ja klientide kaasamise rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="2f780-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="2f780-162">Topeltkirjutamine koosneb kahest AppSource'i lahendusest, mis on installitud Dataverse'isse.</span><span class="sxs-lookup"><span data-stu-id="2f780-162">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="2f780-163">Lahendused laiendavad Dataverse'i üksuse skeemi, lisandmooduleid ja töövooge, et neid saaks sobitada ERP suurusega.</span><span class="sxs-lookup"><span data-stu-id="2f780-163">The solutions expand the entity schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="2f780-164">Edukaks rakendamiseks peavad klientide kaasamise rakenduste arendajad ja arhitektid neid muudatusi mõistma ning tegema koostööd oma kolleegidega Finance and Operationsi rakendustega seoses.</span><span class="sxs-lookup"><span data-stu-id="2f780-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="2f780-165">Finance and Operationsi rakenduste paarsuse loomiseks teeb topeltkirjutamine Dataverse'i skeemis mõned olulised muudatused.</span><span class="sxs-lookup"><span data-stu-id="2f780-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="2f780-166">Kui te seda plaani mõistate, saate tulevikus vältida mõnda kujundamise ja arendamisega seotud taastöötlust.</span><span class="sxs-lookup"><span data-stu-id="2f780-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="2f780-167">Kui AppSource'i topeltkirjutamisega pakett on installitud, on Dataverse'il uued mõisted (nt ettevõte ja osapool).</span><span class="sxs-lookup"><span data-stu-id="2f780-167">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="2f780-168">Need mõisted aitavad Dataverse'il (sh Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ja Dynamics 365 Field Service) põhinevatel rakendustel Finance and Operationsi rakendustega sujuvalt suhelda.</span><span class="sxs-lookup"><span data-stu-id="2f780-168">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="2f780-169">Tegevused ja märkmed on ühtlustatud ning laiendatud, et toetada nii C1-sid (süsteemi kasutajaid) kui ka C2-sid (süsteemi kliendid).</span><span class="sxs-lookup"><span data-stu-id="2f780-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="2f780-170">Selleks et vältida andmete kaotsiminekut valuuta ülekandmisel Finance and Operationsi rakenduste ning Dataverse'i vahel, saate klientide kaasamise rakenduste valuuta andmetüübi kümnendkohtade arvu suurendada.</span><span class="sxs-lookup"><span data-stu-id="2f780-170">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="2f780-171">Funktsioon teisendab metaandmete kihis olemasolevad read uude laiendatud olekusse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="2f780-171">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="2f780-172">Selle protsessi käigus teisendatakse valuuta väärtus raha andmetüübi asemel kümnendkoha andmetüübiks ja valuuta väärtus toetab 10 kümnendkohta.</span><span class="sxs-lookup"><span data-stu-id="2f780-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="2f780-173">See funktsioon on valikuline ja organisatsioonid, kes ei vaja rohkem kui nelja kümnendkohta, ei pea seda kasutama.</span><span class="sxs-lookup"><span data-stu-id="2f780-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="2f780-174">Lisateavet vt [Valuuta andmetüübi migratsioon topeltkirjutamise jaoks](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="2f780-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="2f780-175">[Kuupäeva jõustumine](../../dev-tools/date-effectivity.md) lisatakse Dataverse'isse.</span><span class="sxs-lookup"><span data-stu-id="2f780-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="2f780-176">See toetab samas üksuses mineviku, oleviku ja tuleviku andmeid.</span><span class="sxs-lookup"><span data-stu-id="2f780-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="2f780-177">Toodete, pakkumiste, tellimuste ja arvete korral toetatakse toote [ühiku teisendusi](../../../../supply-chain/pim/tasks/manage-unit-measure.md).</span><span class="sxs-lookup"><span data-stu-id="2f780-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="2f780-178">Lisateavet eelseisvate muudatuste kohta leiate teemast [Mis on uut või mida on muudetud topeltkirjutuses?](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="2f780-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

