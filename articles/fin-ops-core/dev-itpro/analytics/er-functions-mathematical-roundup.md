---
title: ER-i funktsioon ROUNDUP
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ROUNDUP.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744435"
---
# <a name="roundup-er-function"></a><span data-ttu-id="a1627-103">ER-i funktsioon ROUNDUP</span><span class="sxs-lookup"><span data-stu-id="a1627-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1627-104">Funktsioon `ROUNDUP` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist ülespoole määratud arvu komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="a1627-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1627-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="a1627-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="a1627-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="a1627-106">Arguments</span></span>

<span data-ttu-id="a1627-107">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="a1627-107">`number`: *Real*</span></span>

<span data-ttu-id="a1627-108">Numbriline väärtus, mis tuleb ümardada ülespoole.</span><span class="sxs-lookup"><span data-stu-id="a1627-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="a1627-109">`decimals`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="a1627-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="a1627-110">Arvuline väärtus, mis tähistab kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="a1627-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="a1627-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="a1627-111">Return values</span></span>

<span data-ttu-id="a1627-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="a1627-112">*Real*</span></span>

<span data-ttu-id="a1627-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="a1627-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a1627-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="a1627-114">Usage notes</span></span>

<span data-ttu-id="a1627-115">See funktsioon toimib nagu [ROUND](er-functions-mathematical-round.md), kuid see ümardab alati määratud numbrit ülespoole (nullist kaugemale).</span><span class="sxs-lookup"><span data-stu-id="a1627-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="a1627-116">Näide 1</span><span class="sxs-lookup"><span data-stu-id="a1627-116">Example 1</span></span>

<span data-ttu-id="a1627-117">`ROUNDUP (1200.763, 2)` ümardab ülespoole kahe komakohani ja tagastab väärtuse **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="a1627-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a1627-118">Näide 2</span><span class="sxs-lookup"><span data-stu-id="a1627-118">Example 2</span></span>

<span data-ttu-id="a1627-119">`ROUNDUP (1200.767, -3)` ümardab ülespoole lähima 1000 kordseni ja tagastab väärtuse **2000**.</span><span class="sxs-lookup"><span data-stu-id="a1627-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1627-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a1627-120">Additional resources</span></span>

[<span data-ttu-id="a1627-121">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="a1627-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]