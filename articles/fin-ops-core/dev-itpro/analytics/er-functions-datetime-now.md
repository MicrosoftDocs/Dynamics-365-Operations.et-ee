---
title: ER-i funktsioon NOW
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NOW.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: cb5b2fa1b8c466582b15d60a56260f0f7111ebd9
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042339"
---
# <span data-ttu-id="6e9e2-103"><a name="NOW">ER-i funktsioon NOW</a></span><span class="sxs-lookup"><span data-stu-id="6e9e2-103"><a name="NOW">NOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e9e2-104">Funktsioon `NOW` tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakendusserveri praegust kuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e9e2-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6e9e2-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="6e9e2-106">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6e9e2-106">Return values</span></span>

<span data-ttu-id="6e9e2-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="6e9e2-107">*DateTime*</span></span>

<span data-ttu-id="6e9e2-108">Tulemiks saadud kuupäeva/kellaaja väärtus.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="6e9e2-109">Näide</span><span class="sxs-lookup"><span data-stu-id="6e9e2-109">Example</span></span>

<span data-ttu-id="6e9e2-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` annab vastuseks praeguse rakendusserveri kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24-12-2015”** määratud kohandatud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="6e9e2-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e9e2-111">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6e9e2-111">Additional resources</span></span>

[<span data-ttu-id="6e9e2-112">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6e9e2-112">Date and time functions</span></span>](er-functions-category-datetime.md)
