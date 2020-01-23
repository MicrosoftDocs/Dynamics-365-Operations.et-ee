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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 075b2e064641061adf5404591a784311b6d28697
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917323"
---
# <span data-ttu-id="58828-103"><a name="FIRSTORNULL">ER-i funktsioon FIRSTORNULL</a></span><span class="sxs-lookup"><span data-stu-id="58828-103"><a name="FIRSTORNULL">FIRSTORNULL ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58828-104">Funktsioon `FIRSTORNULL` tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see kirje pole tühi.</span><span class="sxs-lookup"><span data-stu-id="58828-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="58828-105">Kui kirje on tühi, tagastab see funktsioon *konteineri (kirje)* väärtuse null.</span><span class="sxs-lookup"><span data-stu-id="58828-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="58828-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="58828-106">Syntax</span></span>

```
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="58828-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="58828-107">Arguments</span></span>

<span data-ttu-id="58828-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="58828-108">`list`: *Record list*</span></span>

<span data-ttu-id="58828-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="58828-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="58828-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="58828-110">Return values</span></span>

<span data-ttu-id="58828-111">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="58828-111">*Container (record)*</span></span>

<span data-ttu-id="58828-112">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="58828-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="58828-113">Näide</span><span class="sxs-lookup"><span data-stu-id="58828-113">Example</span></span>

<span data-ttu-id="58828-114">Avaldis `FIRSTORNULL(SPLIT("",1)).Value` tagastab tühja stringi (**„”**).</span><span class="sxs-lookup"><span data-stu-id="58828-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58828-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="58828-115">Additional resources</span></span>

[<span data-ttu-id="58828-116">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="58828-116">List functions</span></span>](er-functions-category-list.md)
