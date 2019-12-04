---
title: Kulumiarvutuste ümardatav summa
description: See artikkel käsitleb kulumi ümardamise välja raamatu seadistamise lehtedel.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40fd019b1b5900fbd15866d9d3c32ed6d88147b4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187080"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="051b6-103">Kulumiarvutuste ümardatav summa</span><span class="sxs-lookup"><span data-stu-id="051b6-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="051b6-104">See artikkel käsitleb kulumi ümardamise välja raamatu seadistamise lehtedel.</span><span class="sxs-lookup"><span data-stu-id="051b6-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="051b6-105">Kulumi ümardamise summad seadistatakse igale raamatule.</span><span class="sxs-lookup"><span data-stu-id="051b6-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="051b6-106">Kulumi ümardamise summasid kasutatakse põhivara kulumireeglites, kus näidatakse edaspidist kulumit ja põhivara väärtust, samuti kulumisoovitustes.</span><span class="sxs-lookup"><span data-stu-id="051b6-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="051b6-107">Sisestage väikseim raamatu puhul lubatud kulumisumma.</span><span class="sxs-lookup"><span data-stu-id="051b6-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="051b6-108">Olenemata ümardamise seadistusest ei ümardata viimase kulumiperioodi kulumisummat.</span><span class="sxs-lookup"><span data-stu-id="051b6-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="051b6-109">Viimase kulumiperioodi lõpus peab põhivara väärtus olema 0 (null) või mahakandmismaksumus, kui mahakandmismaksumust kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="051b6-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="051b6-110">Näide</span><span class="sxs-lookup"><span data-stu-id="051b6-110">Example</span></span>

<span data-ttu-id="051b6-111">Kulum ilma ümardamiseta arvutatakse kui 2444,44.</span><span class="sxs-lookup"><span data-stu-id="051b6-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="051b6-112">Nagu tabelist näha, varieeruvad pakutavad summad olenevalt ümardamise seadistustest.</span><span class="sxs-lookup"><span data-stu-id="051b6-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="051b6-113">Ümardamismeetod</span><span class="sxs-lookup"><span data-stu-id="051b6-113">Rounding method</span></span> | <span data-ttu-id="051b6-114">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="051b6-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="051b6-115">Ümardamine 0,1</span><span class="sxs-lookup"><span data-stu-id="051b6-115">Rounding 0.1</span></span>    | <span data-ttu-id="051b6-116">2444,40</span><span class="sxs-lookup"><span data-stu-id="051b6-116">2,444.40</span></span>            |
| <span data-ttu-id="051b6-117">Ümardamine 1,00</span><span class="sxs-lookup"><span data-stu-id="051b6-117">Rounding 1.00</span></span>   | <span data-ttu-id="051b6-118">2444,00</span><span class="sxs-lookup"><span data-stu-id="051b6-118">2,444.00</span></span>            |
| <span data-ttu-id="051b6-119">Ümardamine 10,00</span><span class="sxs-lookup"><span data-stu-id="051b6-119">Rounding 10.00</span></span>  | <span data-ttu-id="051b6-120">2440,00</span><span class="sxs-lookup"><span data-stu-id="051b6-120">2,440.00</span></span>            |
| <span data-ttu-id="051b6-121">Ümardamine 100,00</span><span class="sxs-lookup"><span data-stu-id="051b6-121">Rounding 100.00</span></span> | <span data-ttu-id="051b6-122">2400,00</span><span class="sxs-lookup"><span data-stu-id="051b6-122">2,400.00</span></span>            |




