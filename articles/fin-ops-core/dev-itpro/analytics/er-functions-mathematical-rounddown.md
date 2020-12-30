---
title: ER-i funktsioon ROUNDDOWN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ROUNDDOWN.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686878"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="80f27-103">ER-i funktsioon ROUNDDOWN</span><span class="sxs-lookup"><span data-stu-id="80f27-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80f27-104">Funktsioon `ROUNDDOWN` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist allapoole määratud arvu komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="80f27-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="80f27-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="80f27-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="80f27-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="80f27-106">Arguments</span></span>

<span data-ttu-id="80f27-107">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="80f27-107">`number`: *Real*</span></span>

<span data-ttu-id="80f27-108">Numbriline väärtus, mis tuleb ümardada allapoole.</span><span class="sxs-lookup"><span data-stu-id="80f27-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="80f27-109">`decimals`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="80f27-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="80f27-110">Arvuline väärtus, mis tähistab kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="80f27-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="80f27-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="80f27-111">Return values</span></span>

<span data-ttu-id="80f27-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="80f27-112">*Real*</span></span>

<span data-ttu-id="80f27-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="80f27-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="80f27-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="80f27-114">Usage notes</span></span>

<span data-ttu-id="80f27-115">See funktsioon toimib nagu [ROUND](er-functions-mathematical-round.md), kuid see ümardab alati määratud numbrit allapoole (nulli poole).</span><span class="sxs-lookup"><span data-stu-id="80f27-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="80f27-116">Näide 1</span><span class="sxs-lookup"><span data-stu-id="80f27-116">Example 1</span></span>

<span data-ttu-id="80f27-117">`ROUNDDOWN (1200.767, 2)` ümardab allapoole kahe komakohani ja tagastab väärtuse **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="80f27-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="80f27-118">Näide 2</span><span class="sxs-lookup"><span data-stu-id="80f27-118">Example 2</span></span>

<span data-ttu-id="80f27-119">`ROUNDDOWN (1700.767, -3)` ümardab allapoole lähima 1000 kordseni ja tagastab väärtuse **1000**.</span><span class="sxs-lookup"><span data-stu-id="80f27-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80f27-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="80f27-120">Additional resources</span></span>

[<span data-ttu-id="80f27-121">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="80f27-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
