---
title: ER-i funktsioon STRINGJOIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni STRINGJOIN.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917185"
---
# <span data-ttu-id="b1799-103"><a name="STRINGJOIN">ER-i funktsioon STRINGJOIN</a></span><span class="sxs-lookup"><span data-stu-id="b1799-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1799-104">Funktsioon `STRINGJOIN` tagastab *stringi* väärtuse, mis koosneb määratud loendi määratud välja liitväärtustest.</span><span class="sxs-lookup"><span data-stu-id="b1799-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="b1799-105">Väärtused saab eraldada määratud eraldajaga.</span><span class="sxs-lookup"><span data-stu-id="b1799-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1799-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="b1799-106">Syntax</span></span>

```
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="b1799-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="b1799-107">Arguments</span></span>

<span data-ttu-id="b1799-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="b1799-108">`list`: *Record list*</span></span>

<span data-ttu-id="b1799-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="b1799-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b1799-110">`field`: *väli*</span><span class="sxs-lookup"><span data-stu-id="b1799-110">`field`: *Field*</span></span>

<span data-ttu-id="b1799-111">Andmetüübi *String* välja kehtiv tee määratud loendis.</span><span class="sxs-lookup"><span data-stu-id="b1799-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="b1799-112">`delimiter`: *string*</span><span class="sxs-lookup"><span data-stu-id="b1799-112">`delimiter`: *String*</span></span>

<span data-ttu-id="b1799-113">Eraldaja, mida kasutatakse alamstringide eraldamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1799-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1799-114">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="b1799-114">Return values</span></span>

<span data-ttu-id="b1799-115">*String*</span><span class="sxs-lookup"><span data-stu-id="b1799-115">*String*</span></span>

<span data-ttu-id="b1799-116">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="b1799-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b1799-117">Näide</span><span class="sxs-lookup"><span data-stu-id="b1799-117">Example</span></span>

<span data-ttu-id="b1799-118">Kui sisestate olemi `SPLIT("abc" , 1)` andmeallikana **DS**, tagastab avaldis `STRINGJOIN (DS, DS.Value, "-")` tulemuse **„a-b-c”**.</span><span class="sxs-lookup"><span data-stu-id="b1799-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1799-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b1799-119">Additional resources</span></span>

[<span data-ttu-id="b1799-120">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="b1799-120">List functions</span></span>](er-functions-category-list.md)
