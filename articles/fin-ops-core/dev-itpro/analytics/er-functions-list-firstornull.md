---
title: ER-i funktsioon FIRSTORNULL
description: Selles teemas selgitatakse, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FIRSTORNULL
author: NickSelin
manager: kfend
ms.date: 11/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3547eeea3c6fef5cca0699002cc0c35cffd940b3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688039"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="4e8c4-103">ER-i funktsioon FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="4e8c4-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e8c4-104">Funktsioon `FIRSTORNULL` tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see kirje pole tühi.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="4e8c4-105">Kui kirje on tühi, tagastab see funktsioon *konteineri (kirje)* väärtuse null.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e8c4-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="4e8c4-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="4e8c4-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="4e8c4-107">Arguments</span></span>

<span data-ttu-id="4e8c4-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="4e8c4-108">`list`: *Record list*</span></span>

<span data-ttu-id="4e8c4-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4e8c4-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="4e8c4-110">Return values</span></span>

<span data-ttu-id="4e8c4-111">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="4e8c4-111">*Container (record)*</span></span>

<span data-ttu-id="4e8c4-112">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="4e8c4-113">Näide</span><span class="sxs-lookup"><span data-stu-id="4e8c4-113">Example</span></span>

<span data-ttu-id="4e8c4-114">Avaldis `FIRSTORNULL(SPLIT("",1)).Value` tagastab tühja stringi (**„”**).</span><span class="sxs-lookup"><span data-stu-id="4e8c4-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e8c4-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4e8c4-115">Additional resources</span></span>

[<span data-ttu-id="4e8c4-116">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="4e8c4-116">List functions</span></span>](er-functions-category-list.md)
