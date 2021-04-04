---
title: ER-i funktsioon UPPER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni UPPER.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 8fb89ca48c0035e672b2de6820d6ef08d36c02af
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559985"
---
# <a name="upper-er-function"></a><span data-ttu-id="dcbd7-103">ER-i funktsioon UPPER</span><span class="sxs-lookup"><span data-stu-id="dcbd7-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcbd7-104">Funktsioon `UPPER` tagastab *stringi* väärtusena määratud tekstistringi pärast selle teisendamist suurtäheliseks.</span><span class="sxs-lookup"><span data-stu-id="dcbd7-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcbd7-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="dcbd7-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="dcbd7-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="dcbd7-106">Arguments</span></span>

<span data-ttu-id="dcbd7-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="dcbd7-107">`text`: *String*</span></span>

<span data-ttu-id="dcbd7-108">Tüübi *String* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="dcbd7-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="dcbd7-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="dcbd7-109">Return values</span></span>

<span data-ttu-id="dcbd7-110">*String*</span><span class="sxs-lookup"><span data-stu-id="dcbd7-110">*String*</span></span>

<span data-ttu-id="dcbd7-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="dcbd7-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="dcbd7-112">Näide</span><span class="sxs-lookup"><span data-stu-id="dcbd7-112">Example</span></span>

<span data-ttu-id="dcbd7-113">`UPPER ("Sample")` tagastab tulemuse **„SAMPLE”**.</span><span class="sxs-lookup"><span data-stu-id="dcbd7-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dcbd7-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="dcbd7-114">Additional resources</span></span>

[<span data-ttu-id="dcbd7-115">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="dcbd7-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]