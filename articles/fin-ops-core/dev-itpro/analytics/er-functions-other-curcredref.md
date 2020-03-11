---
title: ER-i funktsioon CURCREDREF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CURCREDREF.
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
ms.openlocfilehash: 6e684a8e063cb3c049d13005cbcf6ebbe688af00
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041488"
---
# <span data-ttu-id="52b65-103"><a name="CURCREDREF">ER-i funktsioon CURCREDREF</a></span><span class="sxs-lookup"><span data-stu-id="52b65-103"><a name="CURCREDREF">CURCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52b65-104">Funktsioon `CURCREDREF` tagastab *stringi* väärtuse, mis tähistab kreeditori viidet, mis põhineb määratud arve numbri numbritel.</span><span class="sxs-lookup"><span data-stu-id="52b65-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b65-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="52b65-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="52b65-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="52b65-106">Arguments</span></span>

<span data-ttu-id="52b65-107">`invoice number digits`: *string*</span><span class="sxs-lookup"><span data-stu-id="52b65-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="52b65-108">Teksti väärtus, mis tähistab arve numbri numbreid.</span><span class="sxs-lookup"><span data-stu-id="52b65-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="52b65-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="52b65-109">Return values</span></span>

<span data-ttu-id="52b65-110">*String*</span><span class="sxs-lookup"><span data-stu-id="52b65-110">*String*</span></span>

<span data-ttu-id="52b65-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="52b65-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="52b65-112">Näide</span><span class="sxs-lookup"><span data-stu-id="52b65-112">Example</span></span>

<span data-ttu-id="52b65-113">`CURCredRef ("VEND-200002")` tagastab **„2200002”**.</span><span class="sxs-lookup"><span data-stu-id="52b65-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52b65-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="52b65-114">Additional resources</span></span>

[<span data-ttu-id="52b65-115">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="52b65-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
