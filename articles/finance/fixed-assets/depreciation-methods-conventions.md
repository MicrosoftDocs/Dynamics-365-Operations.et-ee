---
title: Kulumimeetodid ja kulumiarvestusreeglid
description: See artikkel annab ülevaate Microsoft Dynamics 365 Finance'is toetatud kulumiarvestusreeglitest ja -meetoditest.
author: ShylaThompson
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 76b20c895519edb7316c2b9a6b223a109a307e77
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189393"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="55196-103">Kulumimeetodid ja kulumiarvestusreeglid</span><span class="sxs-lookup"><span data-stu-id="55196-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55196-104">See artikkel annab ülevaate toetatud kulumiarvestusreeglitest ja -meetoditest.</span><span class="sxs-lookup"><span data-stu-id="55196-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="55196-105">Saate valida mitmesuguste kulumimeetodite ja kulumiarvestusreeglite hulgast.</span><span class="sxs-lookup"><span data-stu-id="55196-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="55196-106">Meetodi eesmärk on põhivara amortiseeruva väärtuse jaotamine rahandusperioodidele.</span><span class="sxs-lookup"><span data-stu-id="55196-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="55196-107">Põhivara amortiseeruv väärtus on mahakandmismaksumuse võrra (kui see on kasutusel) vähendatud soetamismaksumus.</span><span class="sxs-lookup"><span data-stu-id="55196-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="55196-108">Kui kasutate kulumiarvestusreegleid ja muudate vara viimase kulumiarvestuse käituskuupäeva, mis seejärel põhjustab mõne kulumi vahelejätmist, võib viimase aasta kulum olla oodatust suurem või väiksem.</span><span class="sxs-lookup"><span data-stu-id="55196-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="55196-109">Kulumit korrigeeritakse viimase kulumikäituskuupäeva muutmisega mõjutatavate kulumiperioodide arvuga.</span><span class="sxs-lookup"><span data-stu-id="55196-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="55196-110">Näiteks kui kasutate poolaasta kulumireeglit kolme aasta puhul, kestab kulumiarvestus tavaliselt 3 1/2 aastat.</span><span class="sxs-lookup"><span data-stu-id="55196-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="55196-111">Kui muudate 3 1/2 aasta jooksul viimast kulumiarvestuskuupäeva, siis viimasel kulumiaastal mõjutatud perioodide arv suureneb.</span><span class="sxs-lookup"><span data-stu-id="55196-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="55196-112">Kui viite kuupäeva edasi kolme kuu võrra, arvestatakse viimasel aastal kulumit tavalise kuue kuu asemel üheksa kuu eest.</span><span class="sxs-lookup"><span data-stu-id="55196-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="55196-113">Kulumiarvestusreegli saate valida järgmisest loendist.</span><span class="sxs-lookup"><span data-stu-id="55196-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="55196-114">Poolaasta</span><span class="sxs-lookup"><span data-stu-id="55196-114">Half year</span></span>
-   <span data-ttu-id="55196-115">Terve kuu</span><span class="sxs-lookup"><span data-stu-id="55196-115">Full month</span></span>
-   <span data-ttu-id="55196-116">Kvartali keskel</span><span class="sxs-lookup"><span data-stu-id="55196-116">Mid quarter</span></span>
-   <span data-ttu-id="55196-117">Kuu keskel (kuu 1. päev)</span><span class="sxs-lookup"><span data-stu-id="55196-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="55196-118">Kuu keskel (kuu 15. päev)</span><span class="sxs-lookup"><span data-stu-id="55196-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="55196-119">Poolaasta (aasta algus)</span><span class="sxs-lookup"><span data-stu-id="55196-119">Half year (start of year)</span></span>
-   <span data-ttu-id="55196-120">Poolaasta (järgmine aasta)</span><span class="sxs-lookup"><span data-stu-id="55196-120">Half year (next year)</span></span>

<span data-ttu-id="55196-121">Saate valida järgmiste kulumimeetodite hulgast.</span><span class="sxs-lookup"><span data-stu-id="55196-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="55196-122">Lineaarne kasulik eluiga</span><span class="sxs-lookup"><span data-stu-id="55196-122">Straight line service life</span></span>
-   <span data-ttu-id="55196-123">Vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="55196-123">Reducing balance</span></span>
-   <span data-ttu-id="55196-124">Manuaal</span><span class="sxs-lookup"><span data-stu-id="55196-124">Manual</span></span>
-   <span data-ttu-id="55196-125">Tegur</span><span class="sxs-lookup"><span data-stu-id="55196-125">Factor</span></span>
-   <span data-ttu-id="55196-126">Tarbimine</span><span class="sxs-lookup"><span data-stu-id="55196-126">Consumption</span></span>
-   <span data-ttu-id="55196-127">Allesjäänud lineaarne eluiga</span><span class="sxs-lookup"><span data-stu-id="55196-127">Straight line life remaining</span></span>
-   <span data-ttu-id="55196-128">200% vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="55196-128">200% reducing balance</span></span>
-   <span data-ttu-id="55196-129">175% vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="55196-129">175% reducing balance</span></span>
-   <span data-ttu-id="55196-130">150% vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="55196-130">150% reducing balance</span></span>
-   <span data-ttu-id="55196-131">125% vähenev saldo</span><span class="sxs-lookup"><span data-stu-id="55196-131">125% reducing balance</span></span>





## <a name="additional-resources"></a><span data-ttu-id="55196-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="55196-132">Additional resources</span></span>

[<span data-ttu-id="55196-133">Põhivara kulum</span><span class="sxs-lookup"><span data-stu-id="55196-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="55196-134">Kasuliku eluea lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="55196-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="55196-135">Väheneva jääkväärtuse kuluarvestusmeetod</span><span class="sxs-lookup"><span data-stu-id="55196-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="55196-136">Käsitsi kulumiarvestus</span><span class="sxs-lookup"><span data-stu-id="55196-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="55196-137">Kulumiarvestus kordaja alusel</span><span class="sxs-lookup"><span data-stu-id="55196-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="55196-138">Tarbimise kulum</span><span class="sxs-lookup"><span data-stu-id="55196-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="55196-139">Allesjäänud eluea lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="55196-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="55196-140">125 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="55196-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="55196-141">150 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="55196-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="55196-142">175 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="55196-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="55196-143">200 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="55196-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]