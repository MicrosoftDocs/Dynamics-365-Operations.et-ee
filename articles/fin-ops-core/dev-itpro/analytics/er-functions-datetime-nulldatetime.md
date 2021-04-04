---
title: ER-i funktsioon NULLDATETIME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NULLDATETIME.
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
ms.openlocfilehash: 159abe09f158565fa9c38da530498329ff183fba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563434"
---
# <a name="nulldatetime-er-function"></a><span data-ttu-id="33045-103">ER-i funktsioon NULLDATETIME</span><span class="sxs-lookup"><span data-stu-id="33045-103">NULLDATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33045-104">Funktsioon `NULLDATETIME` tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuar 1900) koordineeritud maailmaajas (Greenwichi aeg \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="33045-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="33045-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="33045-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="33045-106">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="33045-106">Return values</span></span>

<span data-ttu-id="33045-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="33045-107">*DateTime*</span></span>

<span data-ttu-id="33045-108">Tulemiks saadud kuupäeva/kellaaja väärtus.</span><span class="sxs-lookup"><span data-stu-id="33045-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="33045-109">Näide</span><span class="sxs-lookup"><span data-stu-id="33045-109">Example</span></span>

<span data-ttu-id="33045-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` tagastab stringi väärtuse **1900-01-01T00:00:00.0000000+00:00**, kui see kutsutakse toimigu ajal, mis käivitati rakenduse kasutaja poolt, kelle ajavööndi väärtus on **(GMT) koordineeritud maailmaaeg** jaotises **Keele ja riigi/regiooni eelistused**.</span><span class="sxs-lookup"><span data-stu-id="33045-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33045-111">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="33045-111">Additional resources</span></span>

[<span data-ttu-id="33045-112">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="33045-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]