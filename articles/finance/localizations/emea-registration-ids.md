---
title: Registreerimise ID-d
description: See teema annab teavet registreerimise ID-de seadistamise ja kasutamise kohta.
author: ShylaThompson
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a0b978228e26ec70457a4bcb1c064070953909b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175374"
---
# <a name="registration-ids"></a><span data-ttu-id="a40f9-103">Registreerimise ID-d</span><span class="sxs-lookup"><span data-stu-id="a40f9-103">Registration IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a40f9-104">See teema annab teavet registreerimise ID-de seadistamise ja kasutamise kohta.</span><span class="sxs-lookup"><span data-stu-id="a40f9-104">This topic provides information about setting up and using registration IDs.</span></span>

<span data-ttu-id="a40f9-105">Paljudes riikides ja regioonides on erinevad määrused ja nõuded maksu registreerimisnumbrite ehk ID-de salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="a40f9-105">Many countries and regions have different regulations and requirements for recording registration numbers or IDs.</span></span> <span data-ttu-id="a40f9-106">See teema annab ülevaate nõutud sätetest ja toetatud registreerimistüüpide töötlemisest erinevates Euroopa riikides/piirkondadeds asuvate osapoolte puhul.</span><span class="sxs-lookup"><span data-stu-id="a40f9-106">This topic provides an overview of the required settings and processing of supported registration types for parties in different European countries/regions.</span></span> <span data-ttu-id="a40f9-107">Kõigis riikides/regioonides kehtivad oma nõuded mitmesuguste erinevate ametiasutuste registreerimisnumbritega seotud riigikohaste funktsioonide toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="a40f9-107">All countries/regions have their requirements for supporting various country-specific functionalities related to registration numbers provided by different state offices.</span></span> <span data-ttu-id="a40f9-108">Registreerimisnumbrid on näiteks isikukood (SSN), maksu ID-kood (TIN) ja Euroopa käibemaksukood (EL-i KMKR).</span><span class="sxs-lookup"><span data-stu-id="a40f9-108">Examples of registration numbers include, social security number (SSN), tax identification number (TIN), and European VAT identification (EU VAT ID).</span></span> <span data-ttu-id="a40f9-109">See funktsioon pakub ühtset raamisitikku kõigi piirkondade kõigile riikidele, võttes arvesse mõne Euroopa riigi riigikohaseid nõudeid.</span><span class="sxs-lookup"><span data-stu-id="a40f9-109">This feature provides unified framework for all countries in all regions taking into account country-specific requirements of some European countries.</span></span> <span data-ttu-id="a40f9-110">Järgmised jaotised kirjeldavad üldist teabevoogu, mida kasutatakse registreerimise ID-de seadistamiseks ja töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="a40f9-110">The following sections describe the overall flow of information that is used for setting up and processing registration IDs.</span></span>

## <a name="registration-type-creation"></a><span data-ttu-id="a40f9-111">Registreerimistüübi loomine</span><span class="sxs-lookup"><span data-stu-id="a40f9-111">Registration type creation</span></span>
<span data-ttu-id="a40f9-112">Enne registreerimise ID sisestamist peate seadistama erinevat tüüpi registreerimisnumbrite jaoks registreerimistüübid, mis igale osapoolele kehtivad.</span><span class="sxs-lookup"><span data-stu-id="a40f9-112">Before you can enter registration ID, you must set up registration types for the different types of registration numbers that each party is subject to.</span></span> <span data-ttu-id="a40f9-113">Erinevates riikides/regioonides asuvate hankijate, klientide, töötajate ja juriidiliste isikute jaoks registreerimistüüpide loomiseks ning haldamiseks minge lehele **Organisatsiooni haldus** &gt; **Globaalne aadressiraamat** &gt; **Registreerimistüübid** &gt; **Registreerimistüübid**.</span><span class="sxs-lookup"><span data-stu-id="a40f9-113">Go to **Organization administration** &gt; **Global address book** &gt; **Registration types** &gt; **Registration types**  page to create and manage registration types for vendors, customers, workers, and legal entities in different countries/regions.</span></span>

|<span data-ttu-id="a40f9-114">Väli</span><span class="sxs-lookup"><span data-stu-id="a40f9-114">Field</span></span>                 |<span data-ttu-id="a40f9-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a40f9-115">Description</span></span>      |
|------------------------------|----------------------------|                                                                           
| <span data-ttu-id="a40f9-116">Nimi</span><span class="sxs-lookup"><span data-stu-id="a40f9-116">Name</span></span>                | <span data-ttu-id="a40f9-117">Registreerimistüübi nimi.</span><span class="sxs-lookup"><span data-stu-id="a40f9-117">The name of the registration type.</span></span> |                                                                           
| <span data-ttu-id="a40f9-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a40f9-118">Description</span></span>         | <span data-ttu-id="a40f9-119">Registreerimistüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="a40f9-119">The description of the registration type.</span></span> |
| <span data-ttu-id="a40f9-120">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-120">Country/region</span></span>      | <span data-ttu-id="a40f9-121">Riigi/regiooni kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="a40f9-121">The unique identifier of the country/region.</span></span>|
| <span data-ttu-id="a40f9-122">Maksuhaldur</span><span class="sxs-lookup"><span data-stu-id="a40f9-122">Tax authority</span></span>       | <span data-ttu-id="a40f9-123">Registreerimistüübiga seostatud maksuamet.</span><span class="sxs-lookup"><span data-stu-id="a40f9-123">The tax authority that is associated with the registration type.</span></span>|
| <span data-ttu-id="a40f9-124">Kitsendatud</span><span class="sxs-lookup"><span data-stu-id="a40f9-124">Restricted to</span></span>       | <span data-ttu-id="a40f9-125">Maksu registreerimistüübile kohalduva piirangu laad: Pole, Isik, Organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="a40f9-125">The kind of restriction that applies to the tax registration type: None, Person, Organization.</span></span>|
| <span data-ttu-id="a40f9-126">Vorming</span><span class="sxs-lookup"><span data-stu-id="a40f9-126">Format</span></span>              | <span data-ttu-id="a40f9-127">Registreerimistüübi kinnitusvorming.</span><span class="sxs-lookup"><span data-stu-id="a40f9-127">The validation format for the registration type.</span></span>|
| <span data-ttu-id="a40f9-128">Saab uuendada</span><span class="sxs-lookup"><span data-stu-id="a40f9-128">Can be updated</span></span>      | <span data-ttu-id="a40f9-129">Määratleb, kas registreerimistüübi registreerimisnumbrit saab pärast sisestamist värskendada.</span><span class="sxs-lookup"><span data-stu-id="a40f9-129">Defines if the registration number for the registration type can be updated after it is entered.</span></span>|
| <span data-ttu-id="a40f9-130">Kordumatu</span><span class="sxs-lookup"><span data-stu-id="a40f9-130">Unique</span></span>              | <span data-ttu-id="a40f9-131">Määratleb, kas registreerimistüübi registreerimisnumber on kordumatu.</span><span class="sxs-lookup"><span data-stu-id="a40f9-131">Defines if the registration number for the registration type is unique.</span></span> |
| <span data-ttu-id="a40f9-132">Riigi puhul esmane</span><span class="sxs-lookup"><span data-stu-id="a40f9-132">Primary for country</span></span> | <span data-ttu-id="a40f9-133">Kui mõni osapool on seostatud kindlas riigis ühe või mitme aadressiga ja registreerimise ID kehtib kõigi nende aadresside puhul, peate määrama ühe neist aadressidest selle riigi puhul peamise aadressina.</span><span class="sxs-lookup"><span data-stu-id="a40f9-133">If a party is associated with one or more addresses in particular country and the registration ID is valid for all these addresses, you must designate one address as primary for the country.</span></span> <span data-ttu-id="a40f9-134">Peamisena saab registreerida ainult ühe ID.</span><span class="sxs-lookup"><span data-stu-id="a40f9-134">You can only register one ID as primary.</span></span> <span data-ttu-id="a40f9-135">Määratleb, kas registreerimisnumbri saab sisestada ainult riigi primaarse aadressi puhul.</span><span class="sxs-lookup"><span data-stu-id="a40f9-135">Defines if the registration number can be entered only for primary for country address.</span></span> |

## <a name="assign-a-registration-type-to-a-registration-category"></a><span data-ttu-id="a40f9-136">Määrake registreerimistüüp registreerimiskategooriale</span><span class="sxs-lookup"><span data-stu-id="a40f9-136">Assign a registration type to a registration category</span></span>
<span data-ttu-id="a40f9-137">Registreerimiskategooria on riigi/regiooni registreerimise identifikaator, mis on heaks kiidetud kasutamiseks kindlas riigis/regioonis maksu-, tolli- ja muul otstarbel.</span><span class="sxs-lookup"><span data-stu-id="a40f9-137">Registration category is country/region registration identifier approved for using in particular country/region for tax, customs and other purposes.</span></span> <span data-ttu-id="a40f9-138">See kategooria määratleb kõnealuse registreerimise ID kinnitusreeglid (nt kontrollnmbrid jne) ja registreerimise ID kaasamise erinevates aruannetes.</span><span class="sxs-lookup"><span data-stu-id="a40f9-138">This category defines validation rules of particular registration ID (including check digits etc.) and inclusion registration ID in different reports.</span></span> <span data-ttu-id="a40f9-139">Kindla riigi registreerimistüübi määramiseks toetatud registreerimiskategooriasse kasutage lehte **Organisatsiooni haldus** &gt; **Globaalne aadressiraamat** &gt; **Registreerimistüübid** &gt; **Registreerimiskategooriad**.</span><span class="sxs-lookup"><span data-stu-id="a40f9-139">Use the page **Organization administration** &gt; **Global address book** &gt; **Registration types** &gt; **Registration categories** to assign registration type of particular country to supported registration category.</span></span>

| <span data-ttu-id="a40f9-140">Väli</span><span class="sxs-lookup"><span data-stu-id="a40f9-140">Field</span></span>            | <span data-ttu-id="a40f9-141">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a40f9-141">Description</span></span>|
|-----------------------|----------------|
| <span data-ttu-id="a40f9-142">Registreerimise tüüp</span><span class="sxs-lookup"><span data-stu-id="a40f9-142">Registration type</span></span>     | <span data-ttu-id="a40f9-143">Registreerimistüüp kõnealuses riigis/regioonis.</span><span class="sxs-lookup"><span data-stu-id="a40f9-143">The registration type in particular country/region.</span></span>|
| <span data-ttu-id="a40f9-144">Kitsendatud</span><span class="sxs-lookup"><span data-stu-id="a40f9-144">Restricted to</span></span>         | <span data-ttu-id="a40f9-145">Maksu registreerimistüübile kohaldub piirangu laad: Pole, Isik, Organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="a40f9-145">The kind of restriction applies to the tax registration type: None, Person, Organization.</span></span>|
| <span data-ttu-id="a40f9-146">Registreerimiskategooria</span><span class="sxs-lookup"><span data-stu-id="a40f9-146">Registration category</span></span> | <span data-ttu-id="a40f9-147">Riigis kasutamiseks heakskiidetud kordumatu registreerimise identifikaator.</span><span class="sxs-lookup"><span data-stu-id="a40f9-147">The unique registration identifier approved for using in the country.</span></span> <span data-ttu-id="a40f9-148">Toetatud kategooriate täielikku loendit kuvatakse selles teemas hiljem.</span><span class="sxs-lookup"><span data-stu-id="a40f9-148">The full list of supported categories is shown later in this topic.</span></span> |

## <a name="enter-registration-ids-for-global-address-book-records"></a><span data-ttu-id="a40f9-149">Sisestage registreerimise ID-d globaalse aadressiraamatu kirjete puhul</span><span class="sxs-lookup"><span data-stu-id="a40f9-149">Enter registration IDs for Global address book records</span></span>

<span data-ttu-id="a40f9-150">Globaalne aadressiraamat (GAB) sisaldab konsolideeritud aadressiteavet klientide, hankijate, kontaktide, ärisuhete ja juriidiliste isikute kohta.</span><span class="sxs-lookup"><span data-stu-id="a40f9-150">The global address book (GAB) contains consolidated address information for customers, vendors, contacts, business relations, and legal entities.</span></span> <span data-ttu-id="a40f9-151">Lisateavet vt teemast [Globaalse aadressiraamatu ülevaade](../../fin-and-ops/organization-administration/overview-global-address-book.md).</span><span class="sxs-lookup"><span data-stu-id="a40f9-151">For more information see, [Global address book overview](../../fin-and-ops/organization-administration/overview-global-address-book.md).</span></span> <span data-ttu-id="a40f9-152">Osapoole kirjed, mis on salvestatud globaalsesse aadressiraamatusse, võivad sisaldada üht või mitut aadressikirjet.</span><span class="sxs-lookup"><span data-stu-id="a40f9-152">The party records that are stored in the global address book can contain one or more address records.</span></span> <span data-ttu-id="a40f9-153">Neid aadresse kasutatakse erinevatel eesmärkidel, näiteks arvete või tarnimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="a40f9-153">These addresses are used for different purposes, such as billing or delivery.</span></span> <span data-ttu-id="a40f9-154">Saate määrata aadressiteabe jaoks registreerimise ID-d klientidele, hankijatele, töötajatele ja juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="a40f9-154">You can set up registration IDs for address information for customers, vendors, workers, and legal entities.</span></span> <span data-ttu-id="a40f9-155">Leidke osapoole (juriidiline isik, hankija, klient, töötaja) kirje, mille jaoks soovite registreerimise ID-d sisestada, ja klõpsake osapoole, juriidilise isiku, hankija, kliendi või töötajaga seotud vormidel valikut **Registreerimise ID-d**, et avada leht **Aadresside haldamine**.</span><span class="sxs-lookup"><span data-stu-id="a40f9-155">Find the party (legal entity, vendor, customer, worker) record for which you want to enter the register ID, and then click **Registration IDs** on forms related to party, legal entity, vendor, customer, worker to open the **Manage addresses** page.</span></span> <span data-ttu-id="a40f9-156">Klõpsake vahekaardil **Maksu registreerimine** nuppu **Lisa** ja sisestage registreerimise ID kohta järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="a40f9-156">On the **Tax registration** tab, click **Add**, and enter following information about the registration ID.</span></span>


|<span data-ttu-id="a40f9-157">Väli</span><span class="sxs-lookup"><span data-stu-id="a40f9-157">Field</span></span>                |<span data-ttu-id="a40f9-158">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a40f9-158">Description</span></span>                                                |
|---------------------|-----------------------------------------------------------|
| <span data-ttu-id="a40f9-159">Registreerimise tüüp</span><span class="sxs-lookup"><span data-stu-id="a40f9-159">Registration type</span></span>   | <span data-ttu-id="a40f9-160">Registreerimistüüp valitud riigis/regioonis.</span><span class="sxs-lookup"><span data-stu-id="a40f9-160">The registration type in the selected country/region.</span></span>     |
| <span data-ttu-id="a40f9-161">Registreerimiskood</span><span class="sxs-lookup"><span data-stu-id="a40f9-161">Registration number</span></span> | <span data-ttu-id="a40f9-162">Osapoole registreerimise ID.</span><span class="sxs-lookup"><span data-stu-id="a40f9-162">The party registration ID.</span></span>                                |
| <span data-ttu-id="a40f9-163">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a40f9-163">Description</span></span>         | <span data-ttu-id="a40f9-164">Registreerimisnumbri kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="a40f9-164">The description of the registration number.</span></span>               |
| <span data-ttu-id="a40f9-165">Lõik</span><span class="sxs-lookup"><span data-stu-id="a40f9-165">Section</span></span>             | <span data-ttu-id="a40f9-166">Lisateave registreerimisnumbri kohta.</span><span class="sxs-lookup"><span data-stu-id="a40f9-166">The additional information about the registration number.</span></span> |
| <span data-ttu-id="a40f9-167">Väljaandev asutus</span><span class="sxs-lookup"><span data-stu-id="a40f9-167">Issuing agency</span></span>      | <span data-ttu-id="a40f9-168">Registreerimisnumbri väljastanud asutus.</span><span class="sxs-lookup"><span data-stu-id="a40f9-168">The authority that issued the registration number.</span></span>        |
| <span data-ttu-id="a40f9-169">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="a40f9-169">Issued date</span></span>         | <span data-ttu-id="a40f9-170">Registreerimisnumbri väljastamiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a40f9-170">The issued date for the registration number.</span></span>              |
| <span data-ttu-id="a40f9-171">Jõustunud</span><span class="sxs-lookup"><span data-stu-id="a40f9-171">Effective</span></span>           | <span data-ttu-id="a40f9-172">Registreerimisnumbri kehtivuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a40f9-172">The effective date for the registration number.</span></span>           |
| <span data-ttu-id="a40f9-173">Aegumine</span><span class="sxs-lookup"><span data-stu-id="a40f9-173">Expiration</span></span>          | <span data-ttu-id="a40f9-174">Registreerimisnumbri aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a40f9-174">The expiration date for the registration number.</span></span>          |

> [!NOTE]
> <span data-ttu-id="a40f9-175">Juriidilise isiku, hankija või kliendi maksukohuslase koodi saab valida KMKR-iga seotud registreerimise ID-de seast ja osapoole jaoks sisestada.</span><span class="sxs-lookup"><span data-stu-id="a40f9-175">The tax exempt number of legal entity, vendor, customer can be selected from registration IDs related to the VAT ID and entered for the party.</span></span>

## <a name="search-for-records-by-registration-id"></a><span data-ttu-id="a40f9-176">Kirjete otsing registreerimise ID alusel</span><span class="sxs-lookup"><span data-stu-id="a40f9-176">Search for records by registration ID</span></span>
<span data-ttu-id="a40f9-177">Osapoolte kirjete otsimine registreerimise ID alusel on võimalik osapoole, juriidilise isiku, hankija, kliendi ja töötajaga seotud vormidel.</span><span class="sxs-lookup"><span data-stu-id="a40f9-177">Search for party records based on a registration ID is available on forms related to party, legal entity, vendor, customer, and worker.</span></span> <span data-ttu-id="a40f9-178">Klõpsake valikut **Registreerimise ID otsing**, et avada leht **Registreerimise ID otsingukriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="a40f9-178">Click **Registration ID search** to open the **Registration ID search criteria** page.</span></span> <span data-ttu-id="a40f9-179">Määrake otsingukriteeriumid ja klõpsake nuppu **Leia**.</span><span class="sxs-lookup"><span data-stu-id="a40f9-179">Specify search criteria and click **Find**.</span></span> <span data-ttu-id="a40f9-180">Süsteem kuvab valitud kirjed globaalsest aadressiraamatust ja seostatud tüüpi osapoole kirjed.</span><span class="sxs-lookup"><span data-stu-id="a40f9-180">The system will display the selected records from the global address book and the associated types of party record.</span></span>

## <a name="supported-registration-categories"></a><span data-ttu-id="a40f9-181">Toetatud registreerimiskategooriad</span><span class="sxs-lookup"><span data-stu-id="a40f9-181">Supported registration categories</span></span>
<span data-ttu-id="a40f9-182">Järgnevas tabelis loetletakse toetatud registreerimistüübid.</span><span class="sxs-lookup"><span data-stu-id="a40f9-182">The following table lists the supported registration types.</span></span> <span data-ttu-id="a40f9-183">Kui olete Microsoft Dynamics AX 2012 registreerimise ID väljadega tuttav, leiate sellest tabelist ka nende väljade vasted Dynamics 365 Finance registreerimiskategooriatele.</span><span class="sxs-lookup"><span data-stu-id="a40f9-183">If you're familiar with the Microsoft Dynamics AX 2012 fields for registration IDs, this table also maps those fields to the Dynamics 365 Finance registration categories.</span></span>

| <span data-ttu-id="a40f9-184">Finance'i registreerimiskategooria</span><span class="sxs-lookup"><span data-stu-id="a40f9-184">Finance Registration category</span></span>         |<span data-ttu-id="a40f9-185">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-185">Country/Region</span></span>  | <span data-ttu-id="a40f9-186">Dynamics AX 2012 mõiste/väli</span><span class="sxs-lookup"><span data-stu-id="a40f9-186">Dynamics AX 2012 term/field</span></span>|
|---------------------------------------------------------------|---------------------|---------------------------------|
| <span data-ttu-id="a40f9-187">KM-i ID</span><span class="sxs-lookup"><span data-stu-id="a40f9-187">VAT ID</span></span>                                                        | <span data-ttu-id="a40f9-188">Kõik Euroopa Liidu (EL) riigid</span><span class="sxs-lookup"><span data-stu-id="a40f9-188">All countries of the European Union (EU)</span></span>|  <span data-ttu-id="a40f9-189">Maksukohustuslase kood (seadusjärgset tüüpi TAX ID rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-189">Tax exempt number (Legislative type TAX ID in AX 2012 R3)</span></span>|
| <span data-ttu-id="a40f9-190">Ettevõtte ID (COID)</span><span class="sxs-lookup"><span data-stu-id="a40f9-190">Enterprise ID (COID)</span></span>                                          | <span data-ttu-id="a40f9-191">Belgia, Tšehhi Vabariik, Eesti, Ungari, Läti, Leedu, Poola, Šveits</span><span class="sxs-lookup"><span data-stu-id="a40f9-191">Belgium Czech Republic Estonia Hungary Latvia Lithuania Poland Switzerland</span></span> | <span data-ttu-id="a40f9-192">Ettevõtte number (EnterpriseNumber) Registreerimisnumber (RegNum\_W) Registreerimisnumber (RegNum\_W) Registreerimisnumber (RegNum\_W) Registreerimisnumber (RegNum\_W) Ettevõtet kood (EnterpriseCode) Registreerimisnumber (RegNum\_W) UID (Seadusjärgset tüüpi UID rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-192">Enterprise number (EnterpriseNumber) Registration number (RegNum\_W) Registration number (RegNum\_W) Registration number (RegNum\_W) Registration number (RegNum\_W) Enterprise code (EnterpriseCode) Registration number (RegNum\_W) UID (Legislative type UID in AX 2012 R3)</span></span> |
| <span data-ttu-id="a40f9-193">Haru ID</span><span class="sxs-lookup"><span data-stu-id="a40f9-193">Branch ID</span></span>                                                     | <span data-ttu-id="a40f9-194">Belgia</span><span class="sxs-lookup"><span data-stu-id="a40f9-194">Belgium</span></span>            | <span data-ttu-id="a40f9-195">Filiaali kood (BranchNumber)</span><span class="sxs-lookup"><span data-stu-id="a40f9-195">Branch number (BranchNumber)</span></span>|
| <span data-ttu-id="a40f9-196">Spisová značka (registreerimisnumber, väljaandev asutus, sektsioon)</span><span class="sxs-lookup"><span data-stu-id="a40f9-196">Spisová značka (Registration number, Issuing agency, Section)</span></span> | <span data-ttu-id="a40f9-197">Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="a40f9-197">Czech Republic</span></span>     | <span data-ttu-id="a40f9-198">Sisestatud number (CommercialRegisterInsetNumber) Säilitatud äriregistris (CommercialRegister) Äriregistri sektsioon (CommercialRegisterSection)</span><span class="sxs-lookup"><span data-stu-id="a40f9-198">Inset number (CommercialRegisterInsetNumber) Kept at commercial register (CommercialRegister) Section of commercial register (CommercialRegisterSection)</span></span>|
| <span data-ttu-id="a40f9-199">Tollikliendi ID</span><span class="sxs-lookup"><span data-stu-id="a40f9-199">Customs customer ID</span></span>                                           | <span data-ttu-id="a40f9-200">Soome</span><span class="sxs-lookup"><span data-stu-id="a40f9-200">Finland</span></span> | <span data-ttu-id="a40f9-201">Tollikliendi number (CustomsCustomerNumber\_FI)</span><span class="sxs-lookup"><span data-stu-id="a40f9-201">Customs customer number (CustomsCustomerNumber\_FI)</span></span>|
| <span data-ttu-id="a40f9-202">INN</span><span class="sxs-lookup"><span data-stu-id="a40f9-202">INN</span></span>                                                           | <span data-ttu-id="a40f9-203">Venemaa Föderatsioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-203">Russian Federation</span></span>| <span data-ttu-id="a40f9-204">INN (seadusjärgset tüüpi INN rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-204">INN (Legislative type INN in AX 2012 R3)</span></span>|
| <span data-ttu-id="a40f9-205">RRC</span><span class="sxs-lookup"><span data-stu-id="a40f9-205">RRC</span></span>                                                           | <span data-ttu-id="a40f9-206">Venemaa Föderatsioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-206">Russian Federation</span></span>| <span data-ttu-id="a40f9-207">RRC (seadusjärgset tüüpi RRC rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-207">RRC (Legislative type RRC in AX 2012 R3)</span></span>|
| <span data-ttu-id="a40f9-208">OKDP</span><span class="sxs-lookup"><span data-stu-id="a40f9-208">OKDP</span></span>                                                          | <span data-ttu-id="a40f9-209">Venemaa Föderatsioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-209">Russian Federation</span></span>| <span data-ttu-id="a40f9-210">OKDP (seadusjärgset tüüpi OKDP rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-210">OKDP (Legislative type OKDP in AX 2012 R3)</span></span>|
| <span data-ttu-id="a40f9-211">OKPO</span><span class="sxs-lookup"><span data-stu-id="a40f9-211">OKPO</span></span>                                                          | <span data-ttu-id="a40f9-212">Venemaa Föderatsioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-212">Russian Federation</span></span>| <span data-ttu-id="a40f9-213">OKPO (seadusjärgset tüüpi OKPO rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-213">OKPO (Legislative type OKPO in AX 2012 R3)</span></span>|
| <span data-ttu-id="a40f9-214">RCOAD</span><span class="sxs-lookup"><span data-stu-id="a40f9-214">RCOAD</span></span>                                                         | <span data-ttu-id="a40f9-215">Venemaa Föderatsioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-215">Russian Federation</span></span>| <span data-ttu-id="a40f9-216">RCOAD (seadusjärgset tüüpi RCOAD rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-216">RCOAD (Legislative type RCOAD in AX 2012 R3)</span></span>|
| <span data-ttu-id="a40f9-217">OGRN</span><span class="sxs-lookup"><span data-stu-id="a40f9-217">OGRN</span></span>                                                          | <span data-ttu-id="a40f9-218">Venemaa Föderatsioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-218">Russian Federation</span></span>| <span data-ttu-id="a40f9-219">OGRN (seadusjärgset tüüpi OGRN rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-219">OGRN (Legislative type OGRN in AX 2012 R3)</span></span> |
| <span data-ttu-id="a40f9-220">SNILS</span><span class="sxs-lookup"><span data-stu-id="a40f9-220">SNILS</span></span>                                                         | <span data-ttu-id="a40f9-221">Venemaa Föderatsioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-221">Russian Federation</span></span>| <span data-ttu-id="a40f9-222">SNILS (seadusjärgset tüüpi SNILS rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-222">SNILS (Legislative type SNILS in AX 2012 R3)</span></span>|
| <span data-ttu-id="a40f9-223">CIFTS</span><span class="sxs-lookup"><span data-stu-id="a40f9-223">CIFTS</span></span>                                                         | <span data-ttu-id="a40f9-224">Venemaa Föderatsioon</span><span class="sxs-lookup"><span data-stu-id="a40f9-224">Russian Federation</span></span>| <span data-ttu-id="a40f9-225">CIFTS (seadusjärgset tüüpi CIFTS rakenduses AX 2012 R3)</span><span class="sxs-lookup"><span data-stu-id="a40f9-225">CIFTS (Legislative type CIFTS in AX 2012 R3)</span></span>|
| <span data-ttu-id="a40f9-226">Pass</span><span class="sxs-lookup"><span data-stu-id="a40f9-226">Passport</span></span>                                                      | <span data-ttu-id="a40f9-227">Hispaania</span><span class="sxs-lookup"><span data-stu-id="a40f9-227">Spain</span></span>             | <span data-ttu-id="a40f9-228">Pass</span><span class="sxs-lookup"><span data-stu-id="a40f9-228">Passport</span></span>|
| <span data-ttu-id="a40f9-229">Ametlik identifitseerimisdokument</span><span class="sxs-lookup"><span data-stu-id="a40f9-229">Official identification document</span></span>                              | <span data-ttu-id="a40f9-230">Hispaania</span><span class="sxs-lookup"><span data-stu-id="a40f9-230">Spain</span></span>             | <span data-ttu-id="a40f9-231">Ametlik identifitseerimisdokument</span><span class="sxs-lookup"><span data-stu-id="a40f9-231">Official identification document</span></span>|
| <span data-ttu-id="a40f9-232">Elukohatõend</span><span class="sxs-lookup"><span data-stu-id="a40f9-232">Residence certificate</span></span>                                         | <span data-ttu-id="a40f9-233">Hispaania</span><span class="sxs-lookup"><span data-stu-id="a40f9-233">Spain</span></span>             | <span data-ttu-id="a40f9-234">Elukohatõend</span><span class="sxs-lookup"><span data-stu-id="a40f9-234">Residence certificate</span></span>|
| <span data-ttu-id="a40f9-235">Muu identifitseerimisdokument</span><span class="sxs-lookup"><span data-stu-id="a40f9-235">Other identification document</span></span>                                 | <span data-ttu-id="a40f9-236">Hispaania</span><span class="sxs-lookup"><span data-stu-id="a40f9-236">Spain</span></span>             | <span data-ttu-id="a40f9-237">Muu identifitseerimisdokument</span><span class="sxs-lookup"><span data-stu-id="a40f9-237">Other identification document</span></span>|
| <span data-ttu-id="a40f9-238">Pole loendatud</span><span class="sxs-lookup"><span data-stu-id="a40f9-238">Not censused</span></span>                                                  | <span data-ttu-id="a40f9-239">Hispaania</span><span class="sxs-lookup"><span data-stu-id="a40f9-239">Spain</span></span>             | <span data-ttu-id="a40f9-240">Pole rakenduses AX 2012 R3 saadaval</span><span class="sxs-lookup"><span data-stu-id="a40f9-240">Not available in AX 2012 R3</span></span>|


<span data-ttu-id="a40f9-241">Lisateavet registreerimise ID-de töötlemise kohta, sealhulgas nõutavad eeltingimused, leiate järgmistest elutsükliteenuste (LCS) KMKR-i tegevuste salvestistest.</span><span class="sxs-lookup"><span data-stu-id="a40f9-241">For more information about registration IDs processing, including required prerequisites, see the following task recordings for VAT ID in Lifecycle Services (LCS):</span></span>

-   <span data-ttu-id="a40f9-242">KM ID seadistamine</span><span class="sxs-lookup"><span data-stu-id="a40f9-242">Set up VAT ID</span></span>
-   <span data-ttu-id="a40f9-243">Hankija KMKR-i registreerimine</span><span class="sxs-lookup"><span data-stu-id="a40f9-243">VAT ID registration of vendor</span></span>
-   <span data-ttu-id="a40f9-244"> Osapoole otsing KM ID abil</span><span class="sxs-lookup"><span data-stu-id="a40f9-244">Party search using VAT ID</span></span>



