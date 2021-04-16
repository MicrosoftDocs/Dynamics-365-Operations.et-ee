---
title: ER-i funktsioon FIRSTORNULL
description: Selles teemas selgitatakse, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FIRSTORNULL
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753212"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="f6486-103">ER-i funktsioon FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="f6486-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6486-104">Funktsioon `FIRSTORNULL` tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see kirje pole tühi.</span><span class="sxs-lookup"><span data-stu-id="f6486-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="f6486-105">Kui kirje on tühi, tagastab see funktsioon *konteineri (kirje)* väärtuse null.</span><span class="sxs-lookup"><span data-stu-id="f6486-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6486-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="f6486-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="f6486-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="f6486-107">Arguments</span></span>

<span data-ttu-id="f6486-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="f6486-108">`list`: *Record list*</span></span>

<span data-ttu-id="f6486-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="f6486-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f6486-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="f6486-110">Return values</span></span>

<span data-ttu-id="f6486-111">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="f6486-111">*Container (record)*</span></span>

<span data-ttu-id="f6486-112">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="f6486-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="f6486-113">Näide</span><span class="sxs-lookup"><span data-stu-id="f6486-113">Example</span></span>

<span data-ttu-id="f6486-114">Avaldis `FIRSTORNULL(SPLIT("",1)).Value` tagastab tühja stringi (**„”**).</span><span class="sxs-lookup"><span data-stu-id="f6486-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6486-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f6486-115">Additional resources</span></span>

[<span data-ttu-id="f6486-116">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="f6486-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]