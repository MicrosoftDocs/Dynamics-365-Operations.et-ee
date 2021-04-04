---
title: ER-i funktsioon ADDDAYS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ADDDAYS.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 85ad6508c0d16796efbf1ad81e25d74365de8f30
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570768"
---
# <a name="adddays-er-function"></a><span data-ttu-id="79c8a-103">ER-i funktsioon ADDDAYS</span><span class="sxs-lookup"><span data-stu-id="79c8a-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79c8a-104">Funktsioon `ADDDAYS` arvutab *kuupäeva ja kellaaja* väärtuse, mis on määratud alguskuupäevast varasemate või hilisemate päevade arv.</span><span class="sxs-lookup"><span data-stu-id="79c8a-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c8a-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="79c8a-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="79c8a-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="79c8a-106">Arguments</span></span>

<span data-ttu-id="79c8a-107">`datetime`: *kuupäev ja kellaaeg*</span><span class="sxs-lookup"><span data-stu-id="79c8a-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="79c8a-108">Kuupäeva/kellaaja väärtus, mis tähistab alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="79c8a-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="79c8a-109">`days`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="79c8a-109">`days`: *Integer*</span></span>

<span data-ttu-id="79c8a-110">Päevade arv enne või pärast väärtust `datetime`.</span><span class="sxs-lookup"><span data-stu-id="79c8a-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="79c8a-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="79c8a-111">Return values</span></span>

<span data-ttu-id="79c8a-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="79c8a-112">*DateTime*</span></span>

<span data-ttu-id="79c8a-113">Tulemiks saadud kuupäeva/kellaaja väärtus.</span><span class="sxs-lookup"><span data-stu-id="79c8a-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="79c8a-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="79c8a-114">Usage notes</span></span>

<span data-ttu-id="79c8a-115">Suvandi `days` positiivne väärtus annab tulemuseks kuupäeva tulevikus.</span><span class="sxs-lookup"><span data-stu-id="79c8a-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="79c8a-116">Negatiivne väärtus annab kuupäeva minevikus.</span><span class="sxs-lookup"><span data-stu-id="79c8a-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="79c8a-117">Näide 1</span><span class="sxs-lookup"><span data-stu-id="79c8a-117">Example 1</span></span>

<span data-ttu-id="79c8a-118">`ADDDAYS (NOW(), 7)` tagastab kuupäeva ja kellaaja seitsme päeva pärast.</span><span class="sxs-lookup"><span data-stu-id="79c8a-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="79c8a-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="79c8a-119">Example 2</span></span>

<span data-ttu-id="79c8a-120">`ADDDAYS (NOW(), -3)` tagastab kuupäeva ja kellaaja kolme päeva eest.</span><span class="sxs-lookup"><span data-stu-id="79c8a-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79c8a-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="79c8a-121">Additional resources</span></span>

[<span data-ttu-id="79c8a-122">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="79c8a-122">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]