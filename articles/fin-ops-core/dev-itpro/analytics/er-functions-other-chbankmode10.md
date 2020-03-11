---
title: ER-i funktsioon CH_BANK_MOD_10
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CH_BANK_MOD_10.
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
ms.openlocfilehash: 808e328bfcc35c96091da9a69850429b82a71070
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070571"
---
# <span data-ttu-id="2f35e-103"><a name="CH_BANK_MOD_10">ER-i funktsioon CH_BANK_MOD_10</a></span><span class="sxs-lookup"><span data-stu-id="2f35e-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f35e-104">Funktsioon `CH_BANK_MOD_10` tagastab *stringi* väärtuse, mis tähistab kreeditori viidet MOD10 avaldisena, mis põhineb määratud arve numbri numbritel.</span><span class="sxs-lookup"><span data-stu-id="2f35e-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f35e-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="2f35e-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="2f35e-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="2f35e-106">Arguments</span></span>

<span data-ttu-id="2f35e-107">`invoice number digits`: *string*</span><span class="sxs-lookup"><span data-stu-id="2f35e-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="2f35e-108">Teksti väärtus, mis tähistab arve numbri numbreid.</span><span class="sxs-lookup"><span data-stu-id="2f35e-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="2f35e-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="2f35e-109">Return values</span></span>

<span data-ttu-id="2f35e-110">*String*</span><span class="sxs-lookup"><span data-stu-id="2f35e-110">*String*</span></span>

<span data-ttu-id="2f35e-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="2f35e-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2f35e-112">Näide</span><span class="sxs-lookup"><span data-stu-id="2f35e-112">Example</span></span>

<span data-ttu-id="2f35e-113">`CH_BANK_MOD_10 ("VEND-200002")` tagastab **3**.</span><span class="sxs-lookup"><span data-stu-id="2f35e-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f35e-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2f35e-114">Additional resources</span></span>

[<span data-ttu-id="2f35e-115">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="2f35e-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
