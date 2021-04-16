---
title: ER-i funktsioon DAYOFYEAR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DAYOFYEAR.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746911"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="eab11-103">ER-i funktsioon DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="eab11-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eab11-104">Funktsioon `DAYOFYEAR` tagastab *täisarvu* väärtuse, mis tähistab 1. jaanuari ja määratud kuupäeva vahelise päevade arvu täisarvuna.</span><span class="sxs-lookup"><span data-stu-id="eab11-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab11-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="eab11-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="eab11-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="eab11-106">Arguments</span></span>

<span data-ttu-id="eab11-107">`date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="eab11-107">`date`: *Date*</span></span>

<span data-ttu-id="eab11-108">Kuupäeva väärtus, mis tähistab päevade arvu arvutamiseks kasutatavat kuupäeva</span><span class="sxs-lookup"><span data-stu-id="eab11-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="eab11-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="eab11-109">Return values</span></span>

<span data-ttu-id="eab11-110">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="eab11-110">*Integer*</span></span>

<span data-ttu-id="eab11-111">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="eab11-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="eab11-112">Näide 1</span><span class="sxs-lookup"><span data-stu-id="eab11-112">Example 1</span></span>

<span data-ttu-id="eab11-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` tagastab **61**.</span><span class="sxs-lookup"><span data-stu-id="eab11-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="eab11-114">Näide 2</span><span class="sxs-lookup"><span data-stu-id="eab11-114">Example 2</span></span>

<span data-ttu-id="eab11-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` tagastab **1**.</span><span class="sxs-lookup"><span data-stu-id="eab11-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eab11-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="eab11-116">Additional resources</span></span>

[<span data-ttu-id="eab11-117">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="eab11-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]