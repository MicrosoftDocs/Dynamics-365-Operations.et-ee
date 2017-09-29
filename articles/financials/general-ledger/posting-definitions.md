---
title: Sisestamisdefinitsioonid
description: "Selles artiklis antakse teavet sisestamisdefinitsioonide ning nende määratlemise ja linkimise kohta. Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 9c49e4abe28078f62f46b4eea4e22a268339b569
ms.contentlocale: et-ee
ms.lasthandoff: 06/29/2017


---

# <a name="posting-definitions"></a><span data-ttu-id="6d10f-104">Sisestamisdefinitsioonid</span><span class="sxs-lookup"><span data-stu-id="6d10f-104">Posting definitions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6d10f-105">Selles artiklis antakse teavet sisestamisdefinitsioonide ning nende määratlemise ja linkimise kohta.</span><span class="sxs-lookup"><span data-stu-id="6d10f-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="6d10f-106">Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="6d10f-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="6d10f-107">Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="6d10f-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="6d10f-108">Toetatud dokumente ja sisestustüüpe saate vaadata lehel **Kande sisestamisdefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="6d10f-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="6d10f-109">Sisestamisdefinitsioonide kasutamise alustamiseks märkige valik**Kasuta sisestamisdefinitsioone** lehel **Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="6d10f-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="6d10f-110">Isegi siis, kui kasutate sisestamisdefinitsioone, tuleb siiski määratleda algsete kirjete ning toetuseta sisestustüüpide ja dokumentide sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="6d10f-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="6d10f-111">Sisestamisdefinitsioone tuleb kasutada ostutellimuste pandiõiguse ja ostutaotluste eelpandiõiguse arvestuse lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="6d10f-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="6d10f-112">Sisestamisdefinitsioonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d10f-112">Defining posting definitions</span></span>
<span data-ttu-id="6d10f-113">Kasutage lehte**Sisestamisdefinitsioonid** vastendamise kriteeriumide määramiseks ja määratlege kirjed, mis tuleks luua, kui ilmneb vaste.</span><span class="sxs-lookup"><span data-stu-id="6d10f-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="6d10f-114">Vastendamiskriteeriume hinnatakse algsete kannete puhul arvestuse jaotustena.</span><span class="sxs-lookup"><span data-stu-id="6d10f-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="6d10f-115">Lehel **Sisestamisdefinitsioonid** saab määrata kirje ridadele ka prioriteedinumbreid, et juhtida ridade hindamise järjekorda.</span><span class="sxs-lookup"><span data-stu-id="6d10f-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="6d10f-116">Vähima prioriteedinumbriga ridu hinnatakse esimesena.</span><span class="sxs-lookup"><span data-stu-id="6d10f-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="6d10f-117">Näiteks hinnatakse kõigepealt kõiki ridu, mille prioriteet on 1, ja seejärel ridu, mille prioriteet on 2 jne.</span><span class="sxs-lookup"><span data-stu-id="6d10f-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="6d10f-118">Vaste leidmisel eiratakse teisi vastavusseviimise kriteeriume.</span><span class="sxs-lookup"><span data-stu-id="6d10f-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="6d10f-119">Lisaks loovad kirjeid ainult algsele kandele vastavad kriteeriumid grupis.</span><span class="sxs-lookup"><span data-stu-id="6d10f-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="6d10f-120">Saate kinnitada oma sisestamisdefinitsioonid, kasutades viisardit **Sisestamisdefinitsiooni testimine**.</span><span class="sxs-lookup"><span data-stu-id="6d10f-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="6d10f-121">Kui määratlete sisestamisdefinitsioonile algse kirje näidise, näete loodavaid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="6d10f-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="6d10f-122">Sisestamisdefinitsiooni versioone saab kasutada koos kehtivuskuupäevadega.</span><span class="sxs-lookup"><span data-stu-id="6d10f-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="6d10f-123">Näiteks saate luua sisestamisdefinitsiooni tulevase versiooni teise pearaamatukontosse sisestamiseks uuel finantsaastal.</span><span class="sxs-lookup"><span data-stu-id="6d10f-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="6d10f-124">Lehel **Kande sisestamisdefinitsioonid** saate määrata kandetüüpidele sisestamisdefinitsioonid.</span><span class="sxs-lookup"><span data-stu-id="6d10f-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="6d10f-125">Sisestamisdefinitsioonide sidumine</span><span class="sxs-lookup"><span data-stu-id="6d10f-125">Linking posting definitions</span></span>
<span data-ttu-id="6d10f-126">Sisestamisdefinitsioonide loomisel saate siduda ühe sisestamisdefinitsiooni teisega.</span><span class="sxs-lookup"><span data-stu-id="6d10f-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="6d10f-127">Seotud definitsiooni kriteeriume arvestatakse siis lisaks praeguse sisestamisdefinitsiooni kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="6d10f-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="6d10f-128">See funktsioon aitab aega säästa, kuna pole vaja sisestada uuesti praeguse sisestamisdefinitsiooni kriteeriume kiirkaardile **Kirjed** lehel **Sisestamisdefinitsioonid**, kui sisestasite need read juba teisele definitsioonile.</span><span class="sxs-lookup"><span data-stu-id="6d10f-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="6d10f-129">Lisage diagrammidele või tabelitele kõik lingid, mida võite kasutada.</span><span class="sxs-lookup"><span data-stu-id="6d10f-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="6d10f-130">Praeguse sisestamisdefinitsiooniga vastuolude vältimiseks veenduge, et seotavate sisestamisdefinitsioonide read oleksid kordumatud.</span><span class="sxs-lookup"><span data-stu-id="6d10f-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="6d10f-131">Sisestamisdefinitsioonide linkide loomisel kehtivad järgmised piirangud.</span><span class="sxs-lookup"><span data-stu-id="6d10f-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="6d10f-132">Antud sisestamisdefinitsioon võib olla lingitud teise sisestamisdefinitsiooniga või teisest sisestamisdefinitsioonist, kuid mitte mõlemat.</span><span class="sxs-lookup"><span data-stu-id="6d10f-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="6d10f-133">Kuid sisestamisdefinitsioon võib olla lingitud mitme sisestamisdefinitsiooniga.</span><span class="sxs-lookup"><span data-stu-id="6d10f-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="6d10f-134">Saate seadistada linke ainult samas moodulis olevate sisestamisdefinitsioonide vahel.</span><span class="sxs-lookup"><span data-stu-id="6d10f-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="6d10f-135">Sisestamisdefinitsiooni saab määrata igale kandetüübile, kuid kandetüüp peab olema sisestamisdefinitsiooniga samas moodulis.</span><span class="sxs-lookup"><span data-stu-id="6d10f-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="6d10f-136">Lehelt **Kande sisestamisdefinitsioonid** saate vaadata, millises moodulis kandetüüp on.</span><span class="sxs-lookup"><span data-stu-id="6d10f-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="6d10f-137">Lisateavet vaadake teemast [Sisestamisdefinitsioonide näited](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="6d10f-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 



