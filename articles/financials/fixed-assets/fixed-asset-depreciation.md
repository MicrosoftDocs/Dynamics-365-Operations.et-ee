---
title: "Põhivara kulum"
description: "Selles artiklis antakse ülevaade põhivara kulumiarvestusest."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 536acd6b2c9f046c2459aec27a1e3b1b56fd5cc9
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="fixed-asset-depreciation"></a><span data-ttu-id="d93ec-103">Põhivara kulum</span><span class="sxs-lookup"><span data-stu-id="d93ec-103">Fixed asset depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d93ec-104">Selles artiklis antakse ülevaade põhivara kulumiarvestusest.</span><span class="sxs-lookup"><span data-stu-id="d93ec-104">This article provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="d93ec-105">Kulum on perioodiline kanne, mis tavaliselt vähendab bilansis põhivara väärtust ning mis kantakse kuluna tulu ja kulu kontole.</span><span class="sxs-lookup"><span data-stu-id="d93ec-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="d93ec-106">Seetõttu kasutatakse bilansis perioodilise kulumi krediteerimiseks tavaliselt põhikontot.</span><span class="sxs-lookup"><span data-stu-id="d93ec-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="d93ec-107">Vastaskonto on kontoplaani tulude ja kulude osas olev konto.</span><span class="sxs-lookup"><span data-stu-id="d93ec-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="d93ec-108">Kulumi korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="d93ec-108">Depreciation adjustment</span></span>
<span data-ttu-id="d93ec-109">Tavaliselt sisestatakse kulumi korrigeerimisena ainult sisestatud kulumikande parandus.</span><span class="sxs-lookup"><span data-stu-id="d93ec-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="d93ec-110">Seetõttu seadistatakse nii põhikonto kui ka vastaskonto samamoodi kui kulumikontod.</span><span class="sxs-lookup"><span data-stu-id="d93ec-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="d93ec-111">Kulumit võidakse korrigeerida nii positiivse kui ka negatiivse summa võrra, kuid põhikonto (bilansikontona) ja vastaskonto funktsionaalsus (tavaliselt kasumi ja kahjumi kontona) funktsioon jääb samaks.</span><span class="sxs-lookup"><span data-stu-id="d93ec-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="d93ec-112">Plaaniväline kulum</span><span class="sxs-lookup"><span data-stu-id="d93ec-112">Extraordinary depreciation</span></span>
<span data-ttu-id="d93ec-113">Plaaniväline kulumi toimib samamoodi kui põhikulum.</span><span class="sxs-lookup"><span data-stu-id="d93ec-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="d93ec-114">Seetõttu kasutatakse kulumisumma krediteerimisel bilanssi ja põhivara väärtuse vähendamiseks põhikontot.</span><span class="sxs-lookup"><span data-stu-id="d93ec-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="d93ec-115">Vastaskonto on tulu ja kulu konto, kus rahandusperioodi jaoks arvutatud kulum arvestatakse kuluna.</span><span class="sxs-lookup"><span data-stu-id="d93ec-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="d93ec-116">Plaaniväline kulum toimib põhikulumist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="d93ec-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="d93ec-117">Kui teil on plaaniväline kulum kasutusel eraldi kandetüübina, saate plaanivälist kulumit sisestada ja selle kohta aruandeid koostada tavalisest põhikulumist eraldi.</span><span class="sxs-lookup"><span data-stu-id="d93ec-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="d93ec-118">Kulumi erihüvitis</span><span class="sxs-lookup"><span data-stu-id="d93ec-118">Special depreciation allowance</span></span>
<span data-ttu-id="d93ec-119">Kulumi erihüvitis võimaldab teil lisakulumi summasid arvestada vara esimesel kasulikul elu- ja amortisatsiooniaastal.</span><span class="sxs-lookup"><span data-stu-id="d93ec-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="d93ec-120">Kulumi erihüvitis tuleb võtta enne mis tahes muid kulumiarvutusi.</span><span class="sxs-lookup"><span data-stu-id="d93ec-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="d93ec-121">Kuna kulumi erihüvitised on sageli tundmatud kuni põhivara tööea hilisema järguni, on mõistlik kasutada seda tüüpi kulumit koos raamatuga, mis ei sisesta pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="d93ec-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="d93ec-122">Saate nende raamatute kandeajaloo kustutamiseks kasutada regulaarset funktsiooni Pearaamatusse sisestamata kannete kustutamine.</span><span class="sxs-lookup"><span data-stu-id="d93ec-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="d93ec-123">Seejärel saate kustutada põhivara raamatu kulumiajaloo, sisestada kulumi erihüvitise, kui see on teada, ja seejärel sisestada ülejäänud kulumikanded aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="d93ec-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="d93ec-124">Loodavate kulumi erihüvitise kirjete arv on piiramatu.</span><span class="sxs-lookup"><span data-stu-id="d93ec-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="d93ec-125">Pärast nende kirjete määramist varagrupi raamatule rakendatakse need sellele kulumiraamatule.</span><span class="sxs-lookup"><span data-stu-id="d93ec-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="d93ec-126">Kulumi erihüvitis sisestatakse protsendi või fikseeritud summana.</span><span class="sxs-lookup"><span data-stu-id="d93ec-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="d93ec-127">Kui sisestate kulumisoovitusi, sisestatakse kulumi erihüvitiste kanded raamatusse kulumikannetest eraldi kannetena.</span><span class="sxs-lookup"><span data-stu-id="d93ec-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="d93ec-128"> Kulumikalendrid</span><span class="sxs-lookup"><span data-stu-id="d93ec-128">Depreciation calendars</span></span>
<span data-ttu-id="d93ec-129">Igal raamatul on kalender, mida kasutatakse põhivarade kulumiarvestusel.</span><span class="sxs-lookup"><span data-stu-id="d93ec-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="d93ec-130">Kui te kalendrit raamatus ei näita, kasutab raamat vaikimisi pearaamatu rahanduskalendrit.</span><span class="sxs-lookup"><span data-stu-id="d93ec-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="d93ec-131">Raamatule tuleb valida rahanduskalender, kui raamatuga seotud kulumireeglid kasutavad kulumiarvestuseks rahandusaastat.</span><span class="sxs-lookup"><span data-stu-id="d93ec-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="d93ec-132">Saate luua ühiskasutusega kalendrid, kasutades pearaamatus lehte **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="d93ec-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="d93ec-133">Lisateavet leiate jaotisest [Kulumimeetodid ja kulumiarvestusreeglid](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="d93ec-133">For more informations, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>




