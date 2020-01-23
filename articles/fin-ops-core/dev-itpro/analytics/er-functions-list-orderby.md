---
title: ER-i funktsioon ORDERBY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ORDERBY.
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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916196"
---
# <span data-ttu-id="20251-103"><a name="ORDERBY">ER-i funktsioon ORDERBY</a></span><span class="sxs-lookup"><span data-stu-id="20251-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20251-104">Funktsioon `ORDERBY` tagastab määratud loendi *kirjete loendi* väärtusena, kui see on vastavalt määratud argumentidele sorditud.</span><span class="sxs-lookup"><span data-stu-id="20251-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="20251-105">Neid argumente saab määratleda avaldistena.</span><span class="sxs-lookup"><span data-stu-id="20251-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="20251-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="20251-106">Syntax</span></span>

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="20251-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="20251-107">Arguments</span></span>

<span data-ttu-id="20251-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="20251-108">`list`: *Record list*</span></span>

<span data-ttu-id="20251-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="20251-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="20251-110">`expression 1`: *väli*</span><span class="sxs-lookup"><span data-stu-id="20251-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="20251-111">Andmeallika välja kehtiv tee, millele viitab kutsutud funktsiooni argument `list`.</span><span class="sxs-lookup"><span data-stu-id="20251-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="20251-112">Viidatud väli peab olema primitiivse andmetüübi väli.</span><span class="sxs-lookup"><span data-stu-id="20251-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="20251-113">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="20251-113">This argument is required.</span></span>

<span data-ttu-id="20251-114">`expression N`: *väli*</span><span class="sxs-lookup"><span data-stu-id="20251-114">`expression N`: *Field*</span></span>

<span data-ttu-id="20251-115">Andmeallika välja kehtiv tee, millele viitab kutsutud funktsiooni argument `list`.</span><span class="sxs-lookup"><span data-stu-id="20251-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="20251-116">Viidatud väli peab olema primitiivse andmetüübi väli.</span><span class="sxs-lookup"><span data-stu-id="20251-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="20251-117">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="20251-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="20251-118">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="20251-118">Return values</span></span>

<span data-ttu-id="20251-119">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="20251-119">*Record list*</span></span>

<span data-ttu-id="20251-120">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="20251-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="20251-121">Näide 1</span><span class="sxs-lookup"><span data-stu-id="20251-121">Example 1</span></span>

<span data-ttu-id="20251-122">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("C|B|A", "|")`, tagastab avaldis `FIRST( ORDERBY( DS, DS. Value)).Value` teksti väärtuse **„A”**.</span><span class="sxs-lookup"><span data-stu-id="20251-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="20251-123">Näide 2</span><span class="sxs-lookup"><span data-stu-id="20251-123">Example 2</span></span>

<span data-ttu-id="20251-124">Kui **Hankija** on konfigureeritud elektroonilise aruandluse (ER) andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `ORDERBY (Vendors, Vendors.'name()')` hankijate loendi, mis on sorditud nimede järgi kasvavas järjestuses.</span><span class="sxs-lookup"><span data-stu-id="20251-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20251-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="20251-125">Additional resources</span></span>

[<span data-ttu-id="20251-126">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="20251-126">List functions</span></span>](er-functions-category-list.md)