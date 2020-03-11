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
ms.openlocfilehash: a6134ae7eb1a8044cf906f2a8d02eb153522a6cf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041925"
---
# <span data-ttu-id="6034d-103"><a name="REVERSE">ER-i funktsioon REVERSE</a></span><span class="sxs-lookup"><span data-stu-id="6034d-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6034d-104">Funktsioon `REVERSE` tagastab määratud loendi *kirjete loendi* väärtusena pööratud sortimisjärjestuses.</span><span class="sxs-lookup"><span data-stu-id="6034d-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6034d-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6034d-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="6034d-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="6034d-106">Arguments</span></span>

<span data-ttu-id="6034d-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="6034d-107">`list`: *Record list*</span></span>

<span data-ttu-id="6034d-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="6034d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="6034d-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6034d-109">Return values</span></span>

<span data-ttu-id="6034d-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="6034d-110">*Record list*</span></span>

<span data-ttu-id="6034d-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="6034d-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="6034d-112">Näide 1</span><span class="sxs-lookup"><span data-stu-id="6034d-112">Example 1</span></span>

<span data-ttu-id="6034d-113">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("C|B|A", "|")`, tagastab avaldis `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` teksti väärtuse **„C”**.</span><span class="sxs-lookup"><span data-stu-id="6034d-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6034d-114">Näide 2</span><span class="sxs-lookup"><span data-stu-id="6034d-114">Example 2</span></span>

<span data-ttu-id="6034d-115">Kui **Hankija** on konfigureeritud elektroonilise aruandluse (ER) andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` hankijate loendi, mis on sorditud nimede järgi kahanevas järjestuses.</span><span class="sxs-lookup"><span data-stu-id="6034d-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6034d-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6034d-116">Additional resources</span></span>

[<span data-ttu-id="6034d-117">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6034d-117">List functions</span></span>](er-functions-category-list.md)
