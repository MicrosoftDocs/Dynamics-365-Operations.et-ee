---
title: "Organisatsioonihalduse kodulehekülg"
description: Teema viitab ressurssidele, mis aitavad teil Microsoft Dynamics 365 for Finance and Operationsit oma organisatsioonis kasutada.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 0a693529b55b66eb940f8215a336d5c4ae0acedd
ms.contentlocale: et-ee
ms.lasthandoff: 12/18/2018

---

# <a name="organization-administration-home-page"></a><span data-ttu-id="768eb-103">Organisatsioonihalduse kodulehekülg</span><span class="sxs-lookup"><span data-stu-id="768eb-103">Organization administration home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="768eb-104">Teema viitab sisule, mis aitavad lauskasutajatel ja administraatoritel konfigureerida rakendust Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="768eb-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="768eb-105">See sisu aitab neil konfigureerida süsteemi nii, et see töötaks teie organisatsiooni ja äritegevuse puhul sujuvalt ning tulemuslikult.</span><span class="sxs-lookup"><span data-stu-id="768eb-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="768eb-106">Suur osa siin nimetatud sisust kohaldub mooduli **Organisatsiooni haldus** funktsioonidele.</span><span class="sxs-lookup"><span data-stu-id="768eb-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="768eb-107">Kuid on mõned toimingud, nt kirje malli loomine ja kasutamine, mida saab rakendada mis tahes moodulis, et teie organisatsioon tõhusamalt toimiks.</span><span class="sxs-lookup"><span data-stu-id="768eb-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span>

## <a name="number-sequences"></a><span data-ttu-id="768eb-108">Numbriseeriad</span><span class="sxs-lookup"><span data-stu-id="768eb-108">Number sequences</span></span>

<span data-ttu-id="768eb-109">Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmete ja kannete kirjete jaoks, mis nõuavad identifikaatoreid.</span><span class="sxs-lookup"><span data-stu-id="768eb-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="768eb-110">Koondandmete kirjet või kandekirjet, mis nõuab ID-d, nimetatakse *viiteks*.</span><span class="sxs-lookup"><span data-stu-id="768eb-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="768eb-111">Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma.</span><span class="sxs-lookup"><span data-stu-id="768eb-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

- [<span data-ttu-id="768eb-112">Numbriseeriate ülevaade</span><span class="sxs-lookup"><span data-stu-id="768eb-112">Number sequence overview</span></span>](number-sequence-overview.md)
- <span data-ttu-id="768eb-113">[Numbriseeriate seadistamine viisardit kasutades](tasks/set-up-number-sequences-wizard.md) (tegevusjuhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
- <span data-ttu-id="768eb-114">[Eraldi numbriseeriate seadistamine](tasks/set-up-number-sequences-individual-basis.md) (tegevusjuhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="768eb-115">Organisatsioonid</span><span class="sxs-lookup"><span data-stu-id="768eb-115">Organizations</span></span>

<span data-ttu-id="768eb-116">Organisatsiooni on grupp inimesi, kes töötavad koos äriprotsessi või eesmärgi saavutamiseks.</span><span class="sxs-lookup"><span data-stu-id="768eb-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="768eb-117">Organisatsiooni hierarhia kajastab teie ettevõttesse kuuluvate organisatsioonide vahelisi seoseid.</span><span class="sxs-lookup"><span data-stu-id="768eb-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="768eb-118">Organisatsioonide ja organisatsiooni hierarhiate seadistamiseks rakenduses Finance and Operations plaanige kindlasti oma ettevõtte mudel.</span><span class="sxs-lookup"><span data-stu-id="768eb-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="768eb-119">Organisatsioonimudelil on rakenduse Dynamics 365 for Finance and Operations juurutamisele ja äriprotsessidele oluline mõju.</span><span class="sxs-lookup"><span data-stu-id="768eb-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

- [<span data-ttu-id="768eb-120">Organisatsioonid ja organisatsiooni hierarhiad</span><span class="sxs-lookup"><span data-stu-id="768eb-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
- [<span data-ttu-id="768eb-121">Organisatsiooni hierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="768eb-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
- <span data-ttu-id="768eb-122">[Organisatsiooni hierarhia loomine](tasks/create-organization-hierarchy.md) (tegevusjuhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
- <span data-ttu-id="768eb-123">[Juriidilise isiku loomine](tasks/create-legal-entity.md) (tegevusjuhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
- <span data-ttu-id="768eb-124">[Tootmisüksuse loomine](tasks/create-operating-unit.md) (tegevusjuhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="768eb-125">Aadressiraamatud</span><span class="sxs-lookup"><span data-stu-id="768eb-125">Address books</span></span>

<span data-ttu-id="768eb-126">Globaalne aadressiraamat on tsentraalne hoidla, kus hoitakse koondandmeid, mida on vaja säilitada kõigi ettevõttesiseste ja väliste isikute ning organisatsioonide kohta, kellega ettevõte suhtleb.</span><span class="sxs-lookup"><span data-stu-id="768eb-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="768eb-127">Osapoole kirjetega seotud andmete hulka kuuluvad osapoole nimi, aadress ja kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="768eb-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span>

<span data-ttu-id="768eb-128">Pärast globaalse aadressiraamatu loomist, saate luua vajaduse järgi täiendavaid aadressiraamatuid, näiteks eraldi aadressiraamatu iga ettevõtte jaoks oma organisatsioonis või iga tegevusala jaoks.</span><span class="sxs-lookup"><span data-stu-id="768eb-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span>

- [<span data-ttu-id="768eb-129">Globaalne aadressiraamat</span><span class="sxs-lookup"><span data-stu-id="768eb-129">Global address book</span></span>](overview-global-address-book.md)
- [<span data-ttu-id="768eb-130">Globaalse aadressiraamatu ja täiendavate aadressiraamatute konfigureerimise plaan</span><span class="sxs-lookup"><span data-stu-id="768eb-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="768eb-131">Globaalse aadressiraamatu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="768eb-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
- [<span data-ttu-id="768eb-132">Aadressiraamatute KKK</span><span class="sxs-lookup"><span data-stu-id="768eb-132">Address books FAQ</span></span>](qa-address-books.md)

## <a name="workflow"></a><span data-ttu-id="768eb-133">Töövoog</span><span class="sxs-lookup"><span data-stu-id="768eb-133">Workflow</span></span>

<span data-ttu-id="768eb-134">Töövoog on Finance and Operationsisse installitud süsteem, mida saab kasutada eraldi töövoogude või äriprotsesside loomiseks.</span><span class="sxs-lookup"><span data-stu-id="768eb-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="768eb-135">Töövoo loomisel määratlete dokumendi liikumise või teekonna läbi süsteemi, näidates, kes peab ülesande täitma, otsuse tegema või dokumendi kinnitama.</span><span class="sxs-lookup"><span data-stu-id="768eb-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span>

- [<span data-ttu-id="768eb-136">Töövoo ülevaade</span><span class="sxs-lookup"><span data-stu-id="768eb-136">Workflow overview</span></span>](overview-workflow-system.md)
- [<span data-ttu-id="768eb-137">Töövoo elemendid</span><span class="sxs-lookup"><span data-stu-id="768eb-137">Workflow elements</span></span>](workflow-elements.md)
- [<span data-ttu-id="768eb-138">Töövoo tegevused</span><span class="sxs-lookup"><span data-stu-id="768eb-138">Workflow actions</span></span>](workflow-actions.md)
- [<span data-ttu-id="768eb-139">Töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="768eb-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="768eb-140">Digitaalallkirjad</span><span class="sxs-lookup"><span data-stu-id="768eb-140">Electronic signatures</span></span>

<span data-ttu-id="768eb-141">Elektronallkiri kinnitab isiku, kes käivitab või kinnitab protsessi.</span><span class="sxs-lookup"><span data-stu-id="768eb-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="768eb-142">Mõnes tööstuses on elektronallkiri juriidiliselt sama siduv kui käsitsi kirjutatud allkiri.</span><span class="sxs-lookup"><span data-stu-id="768eb-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="768eb-143">Elektronallkirjad on määrustele vastavuse nõue mitmes reguleeritud tööstusharus, nt farmaatsia-, toiduainete- ja joogi-, ja lennundus ja kaitsetööstuses.</span><span class="sxs-lookup"><span data-stu-id="768eb-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="768eb-144">Finance and Operationsis saate kasutada tähtsateks äriprotsessideks elektronallkirju.</span><span class="sxs-lookup"><span data-stu-id="768eb-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="768eb-145">Mõnedel protsessidel on sisseehitatud elektronallkirja võimalused.</span><span class="sxs-lookup"><span data-stu-id="768eb-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="768eb-146">Igale andmebaasi tabelile või väljale saate luua ka allkirjanõuded.</span><span class="sxs-lookup"><span data-stu-id="768eb-146">You can also create custom signature requirements for any database table and field.</span></span>

- [<span data-ttu-id="768eb-147">Digitaalallkirja ülevaade</span><span class="sxs-lookup"><span data-stu-id="768eb-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
- <span data-ttu-id="768eb-148">[Digitaalallkirjade seadistamine](tasks/set-up-electronic-signatures.md) (tegevusjuhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="768eb-149">Juhtumihaldus</span><span class="sxs-lookup"><span data-stu-id="768eb-149">Case management</span></span>

<span data-ttu-id="768eb-150">Juhtumite plaanimise, jälgimise ja analüüsimisega saate arendada tõhusaid lahendusi, mida sarnaste probleemide puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="768eb-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="768eb-151">Näiteks kui klienditeeninduse esindajad või inimressursside spetsialistid loovad juhtumeid, leiavad nad teadmusartiklitest teavet, mis aitab neil juhtumitega tõhusamalt töötada või neid lahendada.</span><span class="sxs-lookup"><span data-stu-id="768eb-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span>

- [<span data-ttu-id="768eb-152">Juhtumihalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="768eb-152">Case management overview</span></span>](cases.md)
- [<span data-ttu-id="768eb-153">Juhtumi turbe, protsesside ja kategooriate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="768eb-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="768eb-154">Kirjemallid</span><span class="sxs-lookup"><span data-stu-id="768eb-154">Record templates</span></span>

<span data-ttu-id="768eb-155">Kirjemallid võivad aidata kiiremini kirjeid luua.</span><span class="sxs-lookup"><span data-stu-id="768eb-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="768eb-156">Saate luua kirje malli nii, et sageli kasutatavaid välja väärtuseid ei pea iga uue kirje jaoks sõnaselgelt sisestama.</span><span class="sxs-lookup"><span data-stu-id="768eb-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span>

- [<span data-ttu-id="768eb-157">Kirjemallid</span><span class="sxs-lookup"><span data-stu-id="768eb-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="768eb-158">[Andmesisestuse hõlbustamiseks kirje malli loomine](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (tegevuse juhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="768eb-159">[Kirje malli abil uue kirje loomine](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (tegevuse juhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="768eb-160">Üdine organisatsiooni haldus</span><span class="sxs-lookup"><span data-stu-id="768eb-160">General organization administration</span></span>

- <span data-ttu-id="768eb-161">[Ribareklaami või logo muutmine](../get-started/tasks/change-banner-or-logo.md) (tegevusjuhis)</span><span class="sxs-lookup"><span data-stu-id="768eb-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="768eb-162">Dokumendihalduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="768eb-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="768eb-163">Meilisõnumi konfigureerimine ja saatmine</span><span class="sxs-lookup"><span data-stu-id="768eb-163">Configure and send email</span></span>](configure-email.md)
- [<span data-ttu-id="768eb-164">Kuupäeva/kellaaja andmed ja ajavööndid</span><span class="sxs-lookup"><span data-stu-id="768eb-164">Date/time data and time zones</span></span>](date-time-zones.md)

