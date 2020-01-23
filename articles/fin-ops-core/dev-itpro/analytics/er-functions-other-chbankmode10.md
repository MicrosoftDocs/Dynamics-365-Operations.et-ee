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
ms.openlocfilehash: 42a345fc48b0d87b353308060903a6b5156c0e62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915874"
---
# <span data-ttu-id="11724-103"><a name="CH_BANK_MOD_10">ER-i funktsioon CH_BANK_MOD_10</a></span><span class="sxs-lookup"><span data-stu-id="11724-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11724-104">Funktsioon `CH_BANK_MOD_10` tagastab *stringi* väärtuse, mis tähistab kreeditori viidet MOD10 avaldisena, mis põhineb määratud arve numbri numbritel.</span><span class="sxs-lookup"><span data-stu-id="11724-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="11724-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="11724-105">Syntax</span></span>

```
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="11724-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="11724-106">Arguments</span></span>

<span data-ttu-id="11724-107">`invoice number digits`: *string*</span><span class="sxs-lookup"><span data-stu-id="11724-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="11724-108">Teksti väärtus, mis tähistab arve numbri numbreid.</span><span class="sxs-lookup"><span data-stu-id="11724-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="11724-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="11724-109">Return values</span></span>

<span data-ttu-id="11724-110">*String*</span><span class="sxs-lookup"><span data-stu-id="11724-110">*String*</span></span>

<span data-ttu-id="11724-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="11724-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="11724-112">Näide</span><span class="sxs-lookup"><span data-stu-id="11724-112">Example</span></span>

<span data-ttu-id="11724-113">`CH_BANK_MOD_10 ("VEND-200002")` tagastab **3**.</span><span class="sxs-lookup"><span data-stu-id="11724-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11724-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="11724-114">Additional resources</span></span>

[<span data-ttu-id="11724-115">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="11724-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
