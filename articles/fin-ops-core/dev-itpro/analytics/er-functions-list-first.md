---
title: ER-i funktsioon FIRST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FIRST.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679410"
---
# <a name="first-er-function"></a><span data-ttu-id="f1b99-103">ER-i funktsioon FIRST</span><span class="sxs-lookup"><span data-stu-id="f1b99-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1b99-104">Funktsioon `FIRST` tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see loend pole tühi.</span><span class="sxs-lookup"><span data-stu-id="f1b99-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="f1b99-105">Kui loend on tühi, esitab see funktsioon erandi.</span><span class="sxs-lookup"><span data-stu-id="f1b99-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b99-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="f1b99-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="f1b99-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="f1b99-107">Arguments</span></span>

<span data-ttu-id="f1b99-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="f1b99-108">`list`: *Record list*</span></span>

<span data-ttu-id="f1b99-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="f1b99-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1b99-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="f1b99-110">Return values</span></span>

<span data-ttu-id="f1b99-111">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="f1b99-111">*Container (record)*</span></span>

<span data-ttu-id="f1b99-112">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="f1b99-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f1b99-113">Näide 1</span><span class="sxs-lookup"><span data-stu-id="f1b99-113">Example 1</span></span>

<span data-ttu-id="f1b99-114">Avaldis `FIRST(SPLIT("ABC",1)).Value` tagastab tekstiväärtuse **„A”**.</span><span class="sxs-lookup"><span data-stu-id="f1b99-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f1b99-115">Näide 2</span><span class="sxs-lookup"><span data-stu-id="f1b99-115">Example 2</span></span>

<span data-ttu-id="f1b99-116">Avaldis `FIRST(SPLIT("",1)).Value` tagastab käitusaja erandi.</span><span class="sxs-lookup"><span data-stu-id="f1b99-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1b99-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f1b99-117">Additional resources</span></span>

[<span data-ttu-id="f1b99-118">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="f1b99-118">List functions</span></span>](er-functions-category-list.md)
