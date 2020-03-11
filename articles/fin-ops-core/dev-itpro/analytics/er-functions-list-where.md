---
title: ER-i funktsioon WHERE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni WHERE.
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
ms.openlocfilehash: 392cf7acebd7ad95bcc0f5d4b7a67500a412a795
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041827"
---
# <span data-ttu-id="b2b1d-103"><a name="WHERE">ER-i funktsioon WHERE</a></span><span class="sxs-lookup"><span data-stu-id="b2b1d-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2b1d-104">Funktsioon `WHERE` tagastab määratud loendi *kirjete loendi* väärtusena, kui see on vastavalt määratud tingimusele filtreeritud.</span><span class="sxs-lookup"><span data-stu-id="b2b1d-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b1d-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="b2b1d-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="b2b1d-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="b2b1d-106">Arguments</span></span>

<span data-ttu-id="b2b1d-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="b2b1d-107">`list`: *Record list*</span></span>

<span data-ttu-id="b2b1d-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="b2b1d-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b2b1d-109">`condition`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="b2b1d-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="b2b1d-110">Kehtiv tingimuslik avaldis, mida kasutatakse määratud loendi kirjete filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b2b1d-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="b2b1d-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="b2b1d-111">Return values</span></span>

<span data-ttu-id="b2b1d-112">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="b2b1d-112">*Record list*</span></span>

<span data-ttu-id="b2b1d-113">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="b2b1d-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b2b1d-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="b2b1d-114">Usage notes</span></span>

<span data-ttu-id="b2b1d-115">Erinevalt funktsioonist [FILTER](er-functions-list-filter.md) rakendatakse määratud tingimust kõigile tüübi *Kirjete loend* elektroonilise aruandluse (ER) andmeallikatele, mis asuvad mälus.</span><span class="sxs-lookup"><span data-stu-id="b2b1d-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="b2b1d-116">Kui argumendid, mis on selle funktsiooni jaoks konfigureeritud (`list` ja `condition`), võimaldavad selle taotluse otsesesse SQL-kutsesse tõlkida, esitatakse kujundamise ajal hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="b2b1d-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="b2b1d-117">See sõnum teavitab kasutajat, et jõudlust võib parandada, kui funktsiooni `WHERE` asemel kasutatakse funktsiooni [FILTER](er-functions-list-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b2b1d-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="b2b1d-118">Näide 1</span><span class="sxs-lookup"><span data-stu-id="b2b1d-118">Example 1</span></span>

<span data-ttu-id="b2b1d-119">Kui **Hankija** on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `WHERE (Vendors, Vendors.VendGroup = "40")` loendi ainult hankijatega, mis kuuluvad hankijate gruppi 40.</span><span class="sxs-lookup"><span data-stu-id="b2b1d-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="b2b1d-120">Näide 2</span><span class="sxs-lookup"><span data-stu-id="b2b1d-120">Example 2</span></span>

<span data-ttu-id="b2b1d-121">Kui sisestate andmeallika **DS** tüübile *Arvutatud väli* ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `WHERE( DS, DS.Value = "B")` loendi ainult ühe kirjega, mis sisaldab väljal **Väärtus** teksti **„B”**.</span><span class="sxs-lookup"><span data-stu-id="b2b1d-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2b1d-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b2b1d-122">Additional resources</span></span>

[<span data-ttu-id="b2b1d-123">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="b2b1d-123">List functions</span></span>](er-functions-category-list.md)
