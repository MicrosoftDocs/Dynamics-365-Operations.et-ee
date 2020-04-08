---
title: " Püsikliendi preemiapunktide korrigeerimise töötlemine"
description: See protseduur selgitab, kuidas otsida kliendikaardi teavet ja korrigeerida püsikliendi preemiapunkte.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdbd9fa60fe4d000359e4695a9fb034fae3ca1b0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140721"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="6603d-103"> Püsikliendi preemiapunktide korrigeerimise töötlemine</span><span class="sxs-lookup"><span data-stu-id="6603d-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6603d-104">See protseduur selgitab, kuidas otsida kliendikaardi teavet ja korrigeerida püsikliendi preemiapunkte.</span><span class="sxs-lookup"><span data-stu-id="6603d-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="6603d-105">Selle tegevuse loomisel kasutati demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="6603d-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="6603d-106">See ülesanne on mõeldud Commerce’i töödejuhataja rollile või klienditeeninduse juhi rollile.</span><span class="sxs-lookup"><span data-stu-id="6603d-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="6603d-107">Minge jaotisse Kliendikaardid.</span><span class="sxs-lookup"><span data-stu-id="6603d-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="6603d-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6603d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6603d-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6603d-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6603d-110">Klõpsake suvandit Kaardi kanded.</span><span class="sxs-lookup"><span data-stu-id="6603d-110">Click Card transactions.</span></span>
    * <span data-ttu-id="6603d-111">Sellel lehel kuvatakse kõik valitud kliendikaardi kliendikaardikanded.</span><span class="sxs-lookup"><span data-stu-id="6603d-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="6603d-112">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6603d-112">Close the page.</span></span>
6. <span data-ttu-id="6603d-113">Klõpsake suvandit Kaardi korrigeerimised.</span><span class="sxs-lookup"><span data-stu-id="6603d-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="6603d-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6603d-114">Click New.</span></span>
8. <span data-ttu-id="6603d-115">Sisestage või valige väärtus väljal Preemiapunktid.</span><span class="sxs-lookup"><span data-stu-id="6603d-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="6603d-116">Sisestage number väljale Summa või kogus.</span><span class="sxs-lookup"><span data-stu-id="6603d-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="6603d-117">Saate lisada kliendikaardile punkte või neid sealt eemaldada, kasutades positiivseid või negatiivseid summasid.</span><span class="sxs-lookup"><span data-stu-id="6603d-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="6603d-118">Sisestage või valige väärtus väljal Püsikliendi programm.</span><span class="sxs-lookup"><span data-stu-id="6603d-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="6603d-119">Sisestage väärtus väljale Kommentaar.</span><span class="sxs-lookup"><span data-stu-id="6603d-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="6603d-120">Klõpsake suvandit Sisesta korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="6603d-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="6603d-121">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="6603d-121">Click Yes.</span></span>
14. <span data-ttu-id="6603d-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6603d-122">Close the page.</span></span>
    * <span data-ttu-id="6603d-123">Tavaliselt tuleks siinkohal lehte värskendada, et näeksite preemiapunktide korrigeerimist vahekaardil Preemiapunktide kokkuvõte. Ent kui aga käitate seda ülesandejuhendina, siis ärge praegu värskendage, muidu ülesandejuhend peatub.</span><span class="sxs-lookup"><span data-stu-id="6603d-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="6603d-124">Klõpsake suvandit Kaardi kanded.</span><span class="sxs-lookup"><span data-stu-id="6603d-124">Click Card transactions.</span></span>
16. <span data-ttu-id="6603d-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6603d-125">Close the page.</span></span>

