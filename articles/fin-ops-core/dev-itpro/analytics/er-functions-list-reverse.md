---
title: ER-i funktsioon REVERSE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni REVERSE.
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
ms.openlocfilehash: ab953136b7500665bdb13e6ff585e3b76896c9ee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744981"
---
# <a name="reverse-er-function"></a><span data-ttu-id="b4c4f-103">ER-i funktsioon REVERSE</span><span class="sxs-lookup"><span data-stu-id="b4c4f-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4c4f-104">Funktsioon `REVERSE` tagastab määratud loendi *kirjete loendi* väärtusena pööratud sortimisjärjestuses.</span><span class="sxs-lookup"><span data-stu-id="b4c4f-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c4f-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="b4c4f-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="b4c4f-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="b4c4f-106">Arguments</span></span>

<span data-ttu-id="b4c4f-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="b4c4f-107">`list`: *Record list*</span></span>

<span data-ttu-id="b4c4f-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="b4c4f-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b4c4f-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="b4c4f-109">Return values</span></span>

<span data-ttu-id="b4c4f-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="b4c4f-110">*Record list*</span></span>

<span data-ttu-id="b4c4f-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="b4c4f-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="b4c4f-112">Näide 1</span><span class="sxs-lookup"><span data-stu-id="b4c4f-112">Example 1</span></span>

<span data-ttu-id="b4c4f-113">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("C|B|A", "|")`, tagastab avaldis `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` teksti väärtuse **„C”**.</span><span class="sxs-lookup"><span data-stu-id="b4c4f-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b4c4f-114">Näide 2</span><span class="sxs-lookup"><span data-stu-id="b4c4f-114">Example 2</span></span>

<span data-ttu-id="b4c4f-115">Kui **Hankija** on konfigureeritud elektroonilise aruandluse (ER) andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` hankijate loendi, mis on sorditud nimede järgi kahanevas järjestuses.</span><span class="sxs-lookup"><span data-stu-id="b4c4f-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4c4f-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b4c4f-116">Additional resources</span></span>

[<span data-ttu-id="b4c4f-117">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="b4c4f-117">List functions</span></span>](er-functions-category-list.md)
