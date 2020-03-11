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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92150bb23e76f82907e0f3e8f0738b25801958bf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041557"
---
# <span data-ttu-id="68b3c-103"><a name="ROUNDDOWN">ER-i funktsioon ROUNDDOWN</a></span><span class="sxs-lookup"><span data-stu-id="68b3c-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68b3c-104">Funktsioon `ROUNDDOWN` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist allapoole määratud arvu komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="68b3c-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b3c-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="68b3c-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="68b3c-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="68b3c-106">Arguments</span></span>

<span data-ttu-id="68b3c-107">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="68b3c-107">`number`: *Real*</span></span>

<span data-ttu-id="68b3c-108">Numbriline väärtus, mis tuleb ümardada allapoole.</span><span class="sxs-lookup"><span data-stu-id="68b3c-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="68b3c-109">`decimals`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="68b3c-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="68b3c-110">Arvuline väärtus, mis tähistab kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="68b3c-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="68b3c-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="68b3c-111">Return values</span></span>

<span data-ttu-id="68b3c-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="68b3c-112">*Real*</span></span>

<span data-ttu-id="68b3c-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="68b3c-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="68b3c-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="68b3c-114">Usage notes</span></span>

<span data-ttu-id="68b3c-115">See funktsioon toimib nagu [ROUND](er-functions-mathematical-round.md), kuid see ümardab alati määratud numbrit allapoole (nulli poole).</span><span class="sxs-lookup"><span data-stu-id="68b3c-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="68b3c-116">Näide 1</span><span class="sxs-lookup"><span data-stu-id="68b3c-116">Example 1</span></span>

<span data-ttu-id="68b3c-117">`ROUNDDOWN (1200.767, 2)` ümardab allapoole kahe komakohani ja tagastab väärtuse **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="68b3c-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="68b3c-118">Näide 2</span><span class="sxs-lookup"><span data-stu-id="68b3c-118">Example 2</span></span>

<span data-ttu-id="68b3c-119">`ROUNDDOWN (1700.767, -3)` ümardab allapoole lähima 1000 kordseni ja tagastab väärtuse **1000**.</span><span class="sxs-lookup"><span data-stu-id="68b3c-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68b3c-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="68b3c-120">Additional resources</span></span>

[<span data-ttu-id="68b3c-121">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="68b3c-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
