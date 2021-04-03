---
title: ER-i funktsioon SESSIONNOW
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SESSIONNOW.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: a79e8055a4b5025e1b1c4ab91875cf165fa8b354
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563387"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="980f1-103">ER-i funktsioon SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="980f1-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="980f1-104">Funktsioon `SESSIONNOW` tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="980f1-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="980f1-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="980f1-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="980f1-106">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="980f1-106">Return values</span></span>

<span data-ttu-id="980f1-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="980f1-107">*DateTime*</span></span>

<span data-ttu-id="980f1-108">Tulemiks saadud kuupäeva/kellaaja väärtus.</span><span class="sxs-lookup"><span data-stu-id="980f1-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="980f1-109">Näide</span><span class="sxs-lookup"><span data-stu-id="980f1-109">Example</span></span>

<span data-ttu-id="980f1-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24.12.2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="980f1-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="980f1-111">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="980f1-111">Additional resources</span></span>

[<span data-ttu-id="980f1-112">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="980f1-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]