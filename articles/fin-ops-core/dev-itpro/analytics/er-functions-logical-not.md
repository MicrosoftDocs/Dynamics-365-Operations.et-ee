---
title: ER-i funktsioon NOT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NOT
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 9b55b3d8930ece7e2f2925579821ca88749801f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565876"
---
# <a name="not-er-function"></a><span data-ttu-id="6f78f-103">ER-i funktsioon NOT</span><span class="sxs-lookup"><span data-stu-id="6f78f-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f78f-104">Funktsioon `NOT` annab määratud tingimuse pööratud loogilise väärtuse *kahendmuutuja* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="6f78f-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f78f-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6f78f-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="6f78f-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="6f78f-106">Arguments</span></span>

<span data-ttu-id="6f78f-107">`condition`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="6f78f-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="6f78f-108">Kehtiv tingimuslik avaldis, mis tuleb ennistada.</span><span class="sxs-lookup"><span data-stu-id="6f78f-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="6f78f-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6f78f-109">Return values</span></span>

<span data-ttu-id="6f78f-110">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="6f78f-110">*Boolean*</span></span>

<span data-ttu-id="6f78f-111">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="6f78f-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="6f78f-112">Näide</span><span class="sxs-lookup"><span data-stu-id="6f78f-112">Example</span></span>

<span data-ttu-id="6f78f-113">`NOT (TRUE)` tagastab väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6f78f-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f78f-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6f78f-114">Additional resources</span></span>

[<span data-ttu-id="6f78f-115">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6f78f-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]