---
title: ER-i funktsioon MOD_97
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni MOD_97.
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
ms.openlocfilehash: ce2192c7bc849996e08573d71d8ed43956c8fb89
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070525"
---
# <span data-ttu-id="51ad9-103"><a name="MOD_97">ER-i funktsioon MOD_97</a></span><span class="sxs-lookup"><span data-stu-id="51ad9-103"><a name="MOD_97">MOD_97 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51ad9-104">Funktsioon `MOD_97` tagastab *stringi* väärtuse, mis tähistab kreeditori viidet MOD97 avaldisena, mis põhineb määratud arve numbri numbritel.</span><span class="sxs-lookup"><span data-stu-id="51ad9-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ad9-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="51ad9-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="51ad9-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="51ad9-106">Arguments</span></span>

<span data-ttu-id="51ad9-107">`invoice number digits`: *string*</span><span class="sxs-lookup"><span data-stu-id="51ad9-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="51ad9-108">Teksti väärtus, mis tähistab arve numbri numbreid.</span><span class="sxs-lookup"><span data-stu-id="51ad9-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="51ad9-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="51ad9-109">Return values</span></span>

<span data-ttu-id="51ad9-110">*String*</span><span class="sxs-lookup"><span data-stu-id="51ad9-110">*String*</span></span>

<span data-ttu-id="51ad9-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="51ad9-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="51ad9-112">Näide</span><span class="sxs-lookup"><span data-stu-id="51ad9-112">Example</span></span>

<span data-ttu-id="51ad9-113">`MOD_97 ("VEND-200002")` tagastab **„20000285”**.</span><span class="sxs-lookup"><span data-stu-id="51ad9-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51ad9-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="51ad9-114">Additional resources</span></span>

[<span data-ttu-id="51ad9-115">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="51ad9-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
