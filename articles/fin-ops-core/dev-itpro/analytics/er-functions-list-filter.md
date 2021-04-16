---
title: ER-i funktsioon FILTER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FILTER.
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746599"
---
# <a name="filter-er-function"></a><span data-ttu-id="b7196-103">ER-i funktsioon FILTER</span><span class="sxs-lookup"><span data-stu-id="b7196-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7196-104">Funktsioon `FILTER` tagastab määratud loendi *kirjete loendi* väärtusena pärast seda, kui päringut on muudetud nii, et see filtreerib määratud tingimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="b7196-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7196-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="b7196-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="b7196-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="b7196-106">Arguments</span></span>

<span data-ttu-id="b7196-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="b7196-107">`list`: *Record list*</span></span>

<span data-ttu-id="b7196-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="b7196-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b7196-109">`condition`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="b7196-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="b7196-110">Kehtiv tingimuslik avaldis, mida kasutatakse määratud loendi kirjete filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b7196-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="b7196-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="b7196-111">Return values</span></span>

<span data-ttu-id="b7196-112">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="b7196-112">*Record list*</span></span>

<span data-ttu-id="b7196-113">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="b7196-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b7196-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="b7196-114">Usage notes</span></span>

<span data-ttu-id="b7196-115">Erinevalt funktsioonist [WHERE](er-functions-list-where.md) rakendatakse määratud tingimust andmebaasi tasemel kõigile tüübi *Tabeli kirjed* elektroonilise aruandluse (ER) andmeallikatele.</span><span class="sxs-lookup"><span data-stu-id="b7196-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="b7196-116">Loendi ja tingimuse saab määrata tabelite ja seoste abil.</span><span class="sxs-lookup"><span data-stu-id="b7196-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="b7196-117">Kui üks või mõlemad argumendid, mis on selle funktsiooni jaoks konfigureeritud (`list` ja `condition`), ei luba seda taotlust otsesesse SQL-kutsesse tõlkida, esitatakse kujundamise ajal erand.</span><span class="sxs-lookup"><span data-stu-id="b7196-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="b7196-118">See erand teavitab kasutajat, et funktsiooni `list` või `condition` ei saa andmebaasi päringuks kasutada.</span><span class="sxs-lookup"><span data-stu-id="b7196-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="b7196-119">Näide 1</span><span class="sxs-lookup"><span data-stu-id="b7196-119">Example 1</span></span>

<span data-ttu-id="b7196-120">Kui **Hankija** on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, tagastab avaldis `FILTER (Vendors, Vendors.VendGroup = "40")` loendi ainult hankijatega, mis kuuluvad hankijate gruppi 40.</span><span class="sxs-lookup"><span data-stu-id="b7196-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="b7196-121">Näide 2</span><span class="sxs-lookup"><span data-stu-id="b7196-121">Example 2</span></span>

<span data-ttu-id="b7196-122">Kui **Hankija** on konfigureeritud ER-i andmeallikana, mis viitab tabelile VendTable, ja kui **parmVendorBankGroup** on konfigureeritud ER-i andmeallikana, mis tagastab väärtuse andmetüübiga *String*, tagastab avaldis `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` loendi ainult nende hankijakontodega, mis kuuluvad kindlasse pangarühma.</span><span class="sxs-lookup"><span data-stu-id="b7196-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="b7196-123">Näide 3</span><span class="sxs-lookup"><span data-stu-id="b7196-123">Example 3</span></span>

<span data-ttu-id="b7196-124">Sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="b7196-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="b7196-125">Seejärel sisestage teine avaldis `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="b7196-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="b7196-126">Kui proovite salvestada selle avaldise ER-i valemikoostajas, esitatakse järgmine erand: „Valideerimise viga: funktsiooni FILTER avaldiste loend ei saa olla päringuobjekt”.</span><span class="sxs-lookup"><span data-stu-id="b7196-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7196-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b7196-127">Additional resources</span></span>

[<span data-ttu-id="b7196-128">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="b7196-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]