---
title: ER-i funktsioon ADDDAYS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ADDDAYS.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688439"
---
# <a name="adddays-er-function"></a><span data-ttu-id="cacb6-103">ER-i funktsioon ADDDAYS</span><span class="sxs-lookup"><span data-stu-id="cacb6-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cacb6-104">Funktsioon `ADDDAYS` arvutab *kuupäeva ja kellaaja* väärtuse, mis on määratud alguskuupäevast varasemate või hilisemate päevade arv.</span><span class="sxs-lookup"><span data-stu-id="cacb6-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="cacb6-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="cacb6-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="cacb6-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="cacb6-106">Arguments</span></span>

<span data-ttu-id="cacb6-107">`datetime`: *kuupäev ja kellaaeg*</span><span class="sxs-lookup"><span data-stu-id="cacb6-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="cacb6-108">Kuupäeva/kellaaja väärtus, mis tähistab alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="cacb6-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="cacb6-109">`days`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="cacb6-109">`days`: *Integer*</span></span>

<span data-ttu-id="cacb6-110">Päevade arv enne või pärast väärtust `datetime`.</span><span class="sxs-lookup"><span data-stu-id="cacb6-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="cacb6-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="cacb6-111">Return values</span></span>

<span data-ttu-id="cacb6-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="cacb6-112">*DateTime*</span></span>

<span data-ttu-id="cacb6-113">Tulemiks saadud kuupäeva/kellaaja väärtus.</span><span class="sxs-lookup"><span data-stu-id="cacb6-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cacb6-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="cacb6-114">Usage notes</span></span>

<span data-ttu-id="cacb6-115">Suvandi `days` positiivne väärtus annab tulemuseks kuupäeva tulevikus.</span><span class="sxs-lookup"><span data-stu-id="cacb6-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="cacb6-116">Negatiivne väärtus annab kuupäeva minevikus.</span><span class="sxs-lookup"><span data-stu-id="cacb6-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="cacb6-117">Näide 1</span><span class="sxs-lookup"><span data-stu-id="cacb6-117">Example 1</span></span>

<span data-ttu-id="cacb6-118">`ADDDAYS (NOW(), 7)` tagastab kuupäeva ja kellaaja seitsme päeva pärast.</span><span class="sxs-lookup"><span data-stu-id="cacb6-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="cacb6-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="cacb6-119">Example 2</span></span>

<span data-ttu-id="cacb6-120">`ADDDAYS (NOW(), -3)` tagastab kuupäeva ja kellaaja kolme päeva eest.</span><span class="sxs-lookup"><span data-stu-id="cacb6-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cacb6-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="cacb6-121">Additional resources</span></span>

[<span data-ttu-id="cacb6-122">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="cacb6-122">Date and time functions</span></span>](er-functions-category-datetime.md)
