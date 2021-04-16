---
title: ER-i funktsioon REVERSE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni REVERSE.
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755200"
---
# <a name="reverse-er-function"></a><span data-ttu-id="5967b-103">ER-i funktsioon REVERSE</span><span class="sxs-lookup"><span data-stu-id="5967b-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5967b-104">Funktsioon `REVERSE` tagastab määratud loendi *kirjete loendi* väärtusena pööratud sortimisjärjestuses.</span><span class="sxs-lookup"><span data-stu-id="5967b-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5967b-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="5967b-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="5967b-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="5967b-106">Arguments</span></span>

<span data-ttu-id="5967b-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="5967b-107">`list`: *Record list*</span></span>

<span data-ttu-id="5967b-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="5967b-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5967b-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="5967b-109">Return values</span></span>

<span data-ttu-id="5967b-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="5967b-110">*Record list*</span></span>

<span data-ttu-id="5967b-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="5967b-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="5967b-112">Näide 1</span><span class="sxs-lookup"><span data-stu-id="5967b-112">Example 1</span></span>

<span data-ttu-id="5967b-113">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("C|B|A", "|")`, tagastab avaldis `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` teksti väärtuse **„C”**.</span><span class="sxs-lookup"><span data-stu-id="5967b-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="5967b-114">Näide 2</span><span class="sxs-lookup"><span data-stu-id="5967b-114">Example 2</span></span>

<span data-ttu-id="5967b-115">Kui **Hankija** on konfigureeritud elektroonilise aruandluse (ER) andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` hankijate loendi, mis on sorditud nimede järgi kahanevas järjestuses.</span><span class="sxs-lookup"><span data-stu-id="5967b-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5967b-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5967b-116">Additional resources</span></span>

[<span data-ttu-id="5967b-117">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="5967b-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]