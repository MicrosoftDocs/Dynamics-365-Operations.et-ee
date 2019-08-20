---
title: Sisestamisdefinitsioonid
description: Selles artiklis antakse teavet sisestamisdefinitsioonide ning nende määratlemise ja linkimise kohta. Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a8dc69ac668da46ccaa470a4e0e7dcb2ce4d0ac
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835018"
---
# <a name="posting-definitions"></a><span data-ttu-id="1be0e-104">Sisestamisdefinitsioonid</span><span class="sxs-lookup"><span data-stu-id="1be0e-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1be0e-105">Selles artiklis antakse teavet sisestamisdefinitsioonide ning nende määratlemise ja linkimise kohta.</span><span class="sxs-lookup"><span data-stu-id="1be0e-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="1be0e-106">Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="1be0e-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="1be0e-107">Toetatud sisestustüüpide ja dokumentide puhul saab sisestusreeglite asemel kasutada raamatupidamiskirjete põhikontode ja finantsdimensioonide klassifitseerimiseks sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="1be0e-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="1be0e-108">Toetatud dokumente ja sisestustüüpe saate vaadata lehel **Kande sisestamisdefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1be0e-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="1be0e-109">Sisestamisdefinitsioonide kasutamise alustamiseks märkige valik**Kasuta sisestamisdefinitsioone** lehel **Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1be0e-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="1be0e-110">Isegi siis, kui kasutate sisestamisdefinitsioone, tuleb siiski määratleda algsete kirjete ning toetuseta sisestustüüpide ja dokumentide sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="1be0e-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="1be0e-111">Sisestamisdefinitsioone tuleb kasutada ostutellimuste pandiõiguse ja ostutaotluste eelpandiõiguse arvestuse lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="1be0e-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="1be0e-112">Sisestamisdefinitsioonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="1be0e-112">Defining posting definitions</span></span>
<span data-ttu-id="1be0e-113">Kasutage lehte**Sisestamisdefinitsioonid** vastendamise kriteeriumide määramiseks ja määratlege kirjed, mis tuleks luua, kui ilmneb vaste.</span><span class="sxs-lookup"><span data-stu-id="1be0e-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="1be0e-114">Vastendamiskriteeriume hinnatakse algsete kannete puhul arvestuse jaotustena.</span><span class="sxs-lookup"><span data-stu-id="1be0e-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="1be0e-115">Lehel **Sisestamisdefinitsioonid** saab määrata kirje ridadele ka prioriteedinumbreid, et juhtida ridade hindamise järjekorda.</span><span class="sxs-lookup"><span data-stu-id="1be0e-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="1be0e-116">Vähima prioriteedinumbriga ridu hinnatakse esimesena.</span><span class="sxs-lookup"><span data-stu-id="1be0e-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="1be0e-117">Näiteks hinnatakse kõigepealt kõiki ridu, mille prioriteet on 1, ja seejärel ridu, mille prioriteet on 2 jne.</span><span class="sxs-lookup"><span data-stu-id="1be0e-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="1be0e-118">Vaste leidmisel eiratakse teisi vastavusseviimise kriteeriume.</span><span class="sxs-lookup"><span data-stu-id="1be0e-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="1be0e-119">Lisaks loovad kirjeid ainult algsele kandele vastavad kriteeriumid grupis.</span><span class="sxs-lookup"><span data-stu-id="1be0e-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="1be0e-120">Saate kinnitada oma sisestamisdefinitsioonid, kasutades viisardit **Sisestamisdefinitsiooni testimine**.</span><span class="sxs-lookup"><span data-stu-id="1be0e-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="1be0e-121">Kui määratlete sisestamisdefinitsioonile algse kirje näidise, näete loodavaid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="1be0e-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="1be0e-122">Sisestamisdefinitsiooni versioone saab kasutada koos kehtivuskuupäevadega.</span><span class="sxs-lookup"><span data-stu-id="1be0e-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="1be0e-123">Näiteks saate luua sisestamisdefinitsiooni tulevase versiooni teise pearaamatukontosse sisestamiseks uuel finantsaastal.</span><span class="sxs-lookup"><span data-stu-id="1be0e-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="1be0e-124">Lehel **Kande sisestamisdefinitsioonid** saate määrata kandetüüpidele sisestamisdefinitsioonid.</span><span class="sxs-lookup"><span data-stu-id="1be0e-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="1be0e-125">Sisestamisdefinitsioonide sidumine</span><span class="sxs-lookup"><span data-stu-id="1be0e-125">Linking posting definitions</span></span>
<span data-ttu-id="1be0e-126">Sisestamisdefinitsioonide loomisel saate siduda ühe sisestamisdefinitsiooni teisega.</span><span class="sxs-lookup"><span data-stu-id="1be0e-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="1be0e-127">Seotud definitsiooni kriteeriume arvestatakse siis lisaks praeguse sisestamisdefinitsiooni kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="1be0e-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="1be0e-128">See funktsioon aitab aega säästa, kuna pole vaja sisestada uuesti praeguse sisestamisdefinitsiooni kriteeriume kiirkaardile **Kirjed** lehel **Sisestamisdefinitsioonid**, kui sisestasite need read juba teisele definitsioonile.</span><span class="sxs-lookup"><span data-stu-id="1be0e-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="1be0e-129">Lisage diagrammidele või tabelitele kõik lingid, mida võite kasutada.</span><span class="sxs-lookup"><span data-stu-id="1be0e-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="1be0e-130">Praeguse sisestamisdefinitsiooniga vastuolude vältimiseks veenduge, et seotavate sisestamisdefinitsioonide read oleksid kordumatud.</span><span class="sxs-lookup"><span data-stu-id="1be0e-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="1be0e-131">Sisestamisdefinitsioonide linkide loomisel kehtivad järgmised piirangud.</span><span class="sxs-lookup"><span data-stu-id="1be0e-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="1be0e-132">Antud sisestamisdefinitsioon võib olla lingitud teise sisestamisdefinitsiooniga või teisest sisestamisdefinitsioonist, kuid mitte mõlemat.</span><span class="sxs-lookup"><span data-stu-id="1be0e-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="1be0e-133">Kuid sisestamisdefinitsioon võib olla lingitud mitme sisestamisdefinitsiooniga.</span><span class="sxs-lookup"><span data-stu-id="1be0e-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="1be0e-134">Saate seadistada linke ainult samas moodulis olevate sisestamisdefinitsioonide vahel.</span><span class="sxs-lookup"><span data-stu-id="1be0e-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="1be0e-135">Sisestamisdefinitsiooni saab määrata igale kandetüübile, kuid kandetüüp peab olema sisestamisdefinitsiooniga samas moodulis.</span><span class="sxs-lookup"><span data-stu-id="1be0e-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="1be0e-136">Lehelt **Kande sisestamisdefinitsioonid** saate vaadata, millises moodulis kandetüüp on.</span><span class="sxs-lookup"><span data-stu-id="1be0e-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="1be0e-137">Lisateavet vaadake teemast [Sisestamisdefinitsioonide näited](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="1be0e-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 


