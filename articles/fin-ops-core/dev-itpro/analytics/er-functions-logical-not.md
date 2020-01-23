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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916035"
---
# <span data-ttu-id="1b8f7-103"><a name="NOT">ER-i funktsioon NOT</a></span><span class="sxs-lookup"><span data-stu-id="1b8f7-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b8f7-104">Funktsioon `NOT` annab määratud tingimuse pööratud loogilise väärtuse *kahendmuutuja* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b8f7-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="1b8f7-105">Syntax</span></span>

```
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="1b8f7-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="1b8f7-106">Arguments</span></span>

<span data-ttu-id="1b8f7-107">`condition`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="1b8f7-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="1b8f7-108">Kehtiv tingimuslik avaldis, mis tuleb ennistada.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b8f7-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="1b8f7-109">Return values</span></span>

<span data-ttu-id="1b8f7-110">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="1b8f7-110">*Boolean*</span></span>

<span data-ttu-id="1b8f7-111">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="1b8f7-112">Näide</span><span class="sxs-lookup"><span data-stu-id="1b8f7-112">Example</span></span>

<span data-ttu-id="1b8f7-113">`NOT (TRUE)` tagastab väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="1b8f7-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b8f7-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1b8f7-114">Additional resources</span></span>

[<span data-ttu-id="1b8f7-115">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="1b8f7-115">Logical functions</span></span>](er-functions-category-logical.md)
