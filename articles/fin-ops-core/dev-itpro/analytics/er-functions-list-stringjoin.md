---
title: ER-i funktsioon STRINGJOIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni STRINGJOIN.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: ac21651e0f5b5a1579b9335bb7f3217370c4d5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745517"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="f84b5-103">ER-i funktsioon STRINGJOIN</span><span class="sxs-lookup"><span data-stu-id="f84b5-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f84b5-104">Funktsioon `STRINGJOIN` tagastab *stringi* väärtuse, mis koosneb määratud loendi määratud välja liitväärtustest.</span><span class="sxs-lookup"><span data-stu-id="f84b5-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="f84b5-105">Väärtused saab eraldada määratud eraldajaga.</span><span class="sxs-lookup"><span data-stu-id="f84b5-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f84b5-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="f84b5-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="f84b5-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="f84b5-107">Arguments</span></span>

<span data-ttu-id="f84b5-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="f84b5-108">`list`: *Record list*</span></span>

<span data-ttu-id="f84b5-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="f84b5-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f84b5-110">`field`: *väli*</span><span class="sxs-lookup"><span data-stu-id="f84b5-110">`field`: *Field*</span></span>

<span data-ttu-id="f84b5-111">Andmetüübi *String* välja kehtiv tee määratud loendis.</span><span class="sxs-lookup"><span data-stu-id="f84b5-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="f84b5-112">`delimiter`: *string*</span><span class="sxs-lookup"><span data-stu-id="f84b5-112">`delimiter`: *String*</span></span>

<span data-ttu-id="f84b5-113">Eraldaja, mida kasutatakse alamstringide eraldamiseks.</span><span class="sxs-lookup"><span data-stu-id="f84b5-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="f84b5-114">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="f84b5-114">Return values</span></span>

<span data-ttu-id="f84b5-115">*String*</span><span class="sxs-lookup"><span data-stu-id="f84b5-115">*String*</span></span>

<span data-ttu-id="f84b5-116">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="f84b5-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f84b5-117">Näide</span><span class="sxs-lookup"><span data-stu-id="f84b5-117">Example</span></span>

<span data-ttu-id="f84b5-118">Kui sisestate olemi `SPLIT("abc" , 1)` andmeallikana **DS**, tagastab avaldis `STRINGJOIN (DS, DS.Value, "-")` tulemuse **„a-b-c”**.</span><span class="sxs-lookup"><span data-stu-id="f84b5-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f84b5-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f84b5-119">Additional resources</span></span>

[<span data-ttu-id="f84b5-120">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="f84b5-120">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]