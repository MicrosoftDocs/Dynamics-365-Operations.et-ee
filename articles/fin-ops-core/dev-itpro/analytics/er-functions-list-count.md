---
title: ER-i funktsioon COUNT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni COUNT.
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
ms.openlocfilehash: c48483a6677aaeb36eac57a57cec71bf54c7991d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745341"
---
# <a name="count-er-function"></a><span data-ttu-id="7087c-103">ER-i funktsioon COUNT</span><span class="sxs-lookup"><span data-stu-id="7087c-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7087c-104">Funktsioon `COUNT` tagastab *täisarvu* väärtuse, mis tähistab kirjete arvu määratud loendis, kui loend pole tühi.</span><span class="sxs-lookup"><span data-stu-id="7087c-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="7087c-105">Kui loend on tühi, tagastab funktsioon väärtuse **0** (null).</span><span class="sxs-lookup"><span data-stu-id="7087c-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="7087c-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="7087c-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="7087c-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="7087c-107">Arguments</span></span>

<span data-ttu-id="7087c-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="7087c-108">`list`: *Record list*</span></span>

<span data-ttu-id="7087c-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="7087c-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7087c-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="7087c-110">Return values</span></span>

<span data-ttu-id="7087c-111">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="7087c-111">*Integer*</span></span>

<span data-ttu-id="7087c-112">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="7087c-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7087c-113">Näide</span><span class="sxs-lookup"><span data-stu-id="7087c-113">Example</span></span>

<span data-ttu-id="7087c-114">`COUNT (SPLIT("abcd" , 3))` tagastab väärtuse **2**, kuna funktsioon `SPLIT`, mida selles näites kasutatakse, loob loendi, mis koosneb kahest kirjest.</span><span class="sxs-lookup"><span data-stu-id="7087c-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7087c-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7087c-115">Additional resources</span></span>

[<span data-ttu-id="7087c-116">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="7087c-116">List functions</span></span>](er-functions-category-list.md)
