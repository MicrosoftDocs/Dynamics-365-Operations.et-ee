---
title: ER-i funktsioon NOT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NOT
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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041718"
---
# <span data-ttu-id="44e1c-103"><a name="NOT">ER-i funktsioon NOT</a></span><span class="sxs-lookup"><span data-stu-id="44e1c-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44e1c-104">Funktsioon `NOT` annab määratud tingimuse pööratud loogilise väärtuse *kahendmuutuja* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="44e1c-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e1c-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="44e1c-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="44e1c-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="44e1c-106">Arguments</span></span>

<span data-ttu-id="44e1c-107">`condition`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="44e1c-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="44e1c-108">Kehtiv tingimuslik avaldis, mis tuleb ennistada.</span><span class="sxs-lookup"><span data-stu-id="44e1c-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="44e1c-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="44e1c-109">Return values</span></span>

<span data-ttu-id="44e1c-110">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="44e1c-110">*Boolean*</span></span>

<span data-ttu-id="44e1c-111">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="44e1c-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="44e1c-112">Näide</span><span class="sxs-lookup"><span data-stu-id="44e1c-112">Example</span></span>

<span data-ttu-id="44e1c-113">`NOT (TRUE)` tagastab väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="44e1c-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44e1c-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="44e1c-114">Additional resources</span></span>

[<span data-ttu-id="44e1c-115">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="44e1c-115">Logical functions</span></span>](er-functions-category-logical.md)
