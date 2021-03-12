---
title: Kulumimeetodid ja kulumiarvestusreeglid
description: See artikkel annab ülevaate Microsoft Dynamics 365 Finance'is toetatud kulumiarvestusreeglitest ja -meetoditest.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af1c1a222981a0bcf9d7341cde5b83dd720da802
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994961"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="e922f-103">Kulumimeetodid ja kulumiarvestusreeglid</span><span class="sxs-lookup"><span data-stu-id="e922f-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e922f-104">See artikkel annab ülevaate toetatud kulumiarvestusreeglitest ja -meetoditest.</span><span class="sxs-lookup"><span data-stu-id="e922f-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="e922f-105">Saate valida mitmesuguste kulumimeetodite ja kulumiarvestusreeglite hulgast.</span><span class="sxs-lookup"><span data-stu-id="e922f-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="e922f-106">Meetodi eesmärk on põhivara amortiseeruva väärtuse jaotamine rahandusperioodidele.</span><span class="sxs-lookup"><span data-stu-id="e922f-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="e922f-107">Põhivara amortiseeruv väärtus on mahakandmismaksumuse võrra (kui see on kasutusel) vähendatud soetamismaksumus.</span><span class="sxs-lookup"><span data-stu-id="e922f-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="e922f-108">Kui kasutate kulumiarvestusreegleid ja muudate vara viimase kulumiarvestuse käituskuupäeva, mis seejärel põhjustab mõne kulumi vahelejätmist, võib viimase aasta kulum olla oodatust suurem või väiksem.</span><span class="sxs-lookup"><span data-stu-id="e922f-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="e922f-109">Kulumit korrigeeritakse viimase kulumikäituskuupäeva muutmisega mõjutatavate kulumiperioodide arvuga.</span><span class="sxs-lookup"><span data-stu-id="e922f-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="e922f-110">Näiteks kui kasutate poolaasta kulumireeglit kolme aasta puhul, kestab kulumiarvestus tavaliselt 3 1/2 aastat.</span><span class="sxs-lookup"><span data-stu-id="e922f-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="e922f-111">Kui muudate 3 1/2 aasta jooksul viimast kulumiarvestuskuupäeva, siis viimasel kulumiaastal mõjutatud perioodide arv suureneb.</span><span class="sxs-lookup"><span data-stu-id="e922f-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="e922f-112">Kui viite kuupäeva edasi kolme kuu võrra, arvestatakse viimasel aastal kulumit tavalise kuue kuu asemel üheksa kuu eest.</span><span class="sxs-lookup"><span data-stu-id="e922f-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="e922f-113">Kulumiarvestusreegli saate valida järgmisest loendist.</span><span class="sxs-lookup"><span data-stu-id="e922f-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="e922f-114">Poolaasta</span><span class="sxs-lookup"><span data-stu-id="e922f-114">Half year</span></span>
-   <span data-ttu-id="e922f-115">Terve kuu</span><span class="sxs-lookup"><span data-stu-id="e922f-115">Full month</span></span>
-   <span data-ttu-id="e922f-116">Kvartali keskel</span><span class="sxs-lookup"><span data-stu-id="e922f-116">Mid quarter</span></span>
-   <span data-ttu-id="e922f-117">Kuu keskel (kuu 1. päev)</span><span class="sxs-lookup"><span data-stu-id="e922f-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="e922f-118">Kuu keskel (kuu 15. päev)</span><span class="sxs-lookup"><span data-stu-id="e922f-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="e922f-119">Poolaasta (aasta algus)</span><span class="sxs-lookup"><span data-stu-id="e922f-119">Half year (start of year)</span></span>
-   <span data-ttu-id="e922f-120">Poolaasta (järgmine aasta)</span><span class="sxs-lookup"><span data-stu-id="e922f-120">Half year (next year)</span></span>

<span data-ttu-id="e922f-121">Saate valida järgmiste kulumimeetodite hulgast.</span><span class="sxs-lookup"><span data-stu-id="e922f-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="e922f-122">Lineaarne kasulik eluiga</span><span class="sxs-lookup"><span data-stu-id="e922f-122">Straight line service life</span></span>
-   <span data-ttu-id="e922f-123">Vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="e922f-123">Reducing balance</span></span>
-   <span data-ttu-id="e922f-124">Manuaal</span><span class="sxs-lookup"><span data-stu-id="e922f-124">Manual</span></span>
-   <span data-ttu-id="e922f-125">Tegur</span><span class="sxs-lookup"><span data-stu-id="e922f-125">Factor</span></span>
-   <span data-ttu-id="e922f-126">Tarbimine</span><span class="sxs-lookup"><span data-stu-id="e922f-126">Consumption</span></span>
-   <span data-ttu-id="e922f-127">Allesjäänud lineaarne eluiga</span><span class="sxs-lookup"><span data-stu-id="e922f-127">Straight line life remaining</span></span>
-   <span data-ttu-id="e922f-128">200% vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="e922f-128">200% reducing balance</span></span>
-   <span data-ttu-id="e922f-129">175% vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="e922f-129">175% reducing balance</span></span>
-   <span data-ttu-id="e922f-130">150% vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="e922f-130">150% reducing balance</span></span>
-   <span data-ttu-id="e922f-131">125% vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="e922f-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="e922f-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e922f-132">Additional resources</span></span>
--------

[<span data-ttu-id="e922f-133">Põhivara kulum</span><span class="sxs-lookup"><span data-stu-id="e922f-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="e922f-134">Kasuliku eluea lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="e922f-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="e922f-135">Väheneva jääkväärtuse kuluarvestusmeetod</span><span class="sxs-lookup"><span data-stu-id="e922f-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="e922f-136">Käsitsi kulumiarvestus</span><span class="sxs-lookup"><span data-stu-id="e922f-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="e922f-137">Kulumiarvestus kordaja alusel</span><span class="sxs-lookup"><span data-stu-id="e922f-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="e922f-138">Tarbimise kulum</span><span class="sxs-lookup"><span data-stu-id="e922f-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="e922f-139">Allesjäänud eluea lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="e922f-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="e922f-140">125 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="e922f-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="e922f-141">150 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="e922f-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="e922f-142">175 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="e922f-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="e922f-143">200 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="e922f-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



