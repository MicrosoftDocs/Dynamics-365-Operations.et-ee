---
title: ER-i funktsioon NOT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NOT
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751704"
---
# <a name="not-er-function"></a><span data-ttu-id="80cfb-103">ER-i funktsioon NOT</span><span class="sxs-lookup"><span data-stu-id="80cfb-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80cfb-104">Funktsioon `NOT` annab määratud tingimuse pööratud loogilise väärtuse *kahendmuutuja* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="80cfb-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="80cfb-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="80cfb-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="80cfb-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="80cfb-106">Arguments</span></span>

<span data-ttu-id="80cfb-107">`condition`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="80cfb-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="80cfb-108">Kehtiv tingimuslik avaldis, mis tuleb ennistada.</span><span class="sxs-lookup"><span data-stu-id="80cfb-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="80cfb-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="80cfb-109">Return values</span></span>

<span data-ttu-id="80cfb-110">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="80cfb-110">*Boolean*</span></span>

<span data-ttu-id="80cfb-111">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="80cfb-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="80cfb-112">Näide</span><span class="sxs-lookup"><span data-stu-id="80cfb-112">Example</span></span>

<span data-ttu-id="80cfb-113">`NOT (TRUE)` tagastab väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="80cfb-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80cfb-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="80cfb-114">Additional resources</span></span>

[<span data-ttu-id="80cfb-115">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="80cfb-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]