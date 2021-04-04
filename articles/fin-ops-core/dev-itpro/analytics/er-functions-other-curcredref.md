---
title: ER-i funktsioon CURCREDREF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CURCREDREF.
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
ms.openlocfilehash: d5f126d71abdc9e3e488b4e8476850dc7763fe5a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567612"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="7d627-103">ER-i funktsioon CURCREDREF</span><span class="sxs-lookup"><span data-stu-id="7d627-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d627-104">Funktsioon `CURCREDREF` tagastab *stringi* väärtuse, mis tähistab kreeditori viidet, mis põhineb määratud arve numbri numbritel.</span><span class="sxs-lookup"><span data-stu-id="7d627-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d627-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="7d627-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="7d627-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="7d627-106">Arguments</span></span>

<span data-ttu-id="7d627-107">`invoice number digits`: *string*</span><span class="sxs-lookup"><span data-stu-id="7d627-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="7d627-108">Teksti väärtus, mis tähistab arve numbri numbreid.</span><span class="sxs-lookup"><span data-stu-id="7d627-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="7d627-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="7d627-109">Return values</span></span>

<span data-ttu-id="7d627-110">*String*</span><span class="sxs-lookup"><span data-stu-id="7d627-110">*String*</span></span>

<span data-ttu-id="7d627-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="7d627-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7d627-112">Näide</span><span class="sxs-lookup"><span data-stu-id="7d627-112">Example</span></span>

<span data-ttu-id="7d627-113">`CURCredRef ("VEND-200002")` tagastab **„2200002”**.</span><span class="sxs-lookup"><span data-stu-id="7d627-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d627-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7d627-114">Additional resources</span></span>

[<span data-ttu-id="7d627-115">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="7d627-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]