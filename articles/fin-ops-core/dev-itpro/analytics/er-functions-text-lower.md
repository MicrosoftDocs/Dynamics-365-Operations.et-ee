---
title: ER-i funktsioon LOWER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LOWER.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e684883d4262e4c3cd8a84d0a1c6f1d685bb650b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746287"
---
# <a name="lower-er-function"></a><span data-ttu-id="55537-103">ER-i funktsioon LOWER</span><span class="sxs-lookup"><span data-stu-id="55537-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55537-104">Funktsioon `LOWER` tagastab *stringi* väärtusena määratud tekstistringi pärast selle teisendamist väiketäheliseks.</span><span class="sxs-lookup"><span data-stu-id="55537-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="55537-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="55537-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="55537-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="55537-106">Arguments</span></span>

<span data-ttu-id="55537-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="55537-107">`text`: *String*</span></span>

<span data-ttu-id="55537-108">*Stringi* väärtus, mis määrab teksti.</span><span class="sxs-lookup"><span data-stu-id="55537-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="55537-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="55537-109">Return values</span></span>

<span data-ttu-id="55537-110">*String*</span><span class="sxs-lookup"><span data-stu-id="55537-110">*String*</span></span>

<span data-ttu-id="55537-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="55537-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="55537-112">Näide</span><span class="sxs-lookup"><span data-stu-id="55537-112">Example</span></span>

<span data-ttu-id="55537-113">`LOWER ("Sample")` tagastab tulemuse **„näidis”**.</span><span class="sxs-lookup"><span data-stu-id="55537-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55537-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="55537-114">Additional resources</span></span>

[<span data-ttu-id="55537-115">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="55537-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]