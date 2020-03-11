---
title: ER-i funktsioon TRIM
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TRIM.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c95663f1aacaf93c1c4bfc8d36d9515f495bf61e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040821"
---
# <span data-ttu-id="ade9b-103"><a name="TRIM">ER-i funktsioon TRIM</a></span><span class="sxs-lookup"><span data-stu-id="ade9b-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ade9b-104">Funktsioon `TRIM` tagastab määratud tekstistringi *stringi* väärtusena pärast algus- ja lõputühikute kärpimist ning sõnade vahel olevate mitmekordsete tühikute eemaldamist.</span><span class="sxs-lookup"><span data-stu-id="ade9b-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade9b-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="ade9b-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="ade9b-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="ade9b-106">Arguments</span></span>

<span data-ttu-id="ade9b-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="ade9b-107">`text`: *String*</span></span>

<span data-ttu-id="ade9b-108">Tüübi *String* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="ade9b-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ade9b-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="ade9b-109">Return values</span></span>

<span data-ttu-id="ade9b-110">*String*</span><span class="sxs-lookup"><span data-stu-id="ade9b-110">*String*</span></span>

<span data-ttu-id="ade9b-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="ade9b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ade9b-112">Näide</span><span class="sxs-lookup"><span data-stu-id="ade9b-112">Example</span></span>

<span data-ttu-id="ade9b-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` tagastab tulemuse **„Näidistekst”**.</span><span class="sxs-lookup"><span data-stu-id="ade9b-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ade9b-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ade9b-114">Additional resources</span></span>

[<span data-ttu-id="ade9b-115">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="ade9b-115">Text functions</span></span>](er-functions-category-text.md)
