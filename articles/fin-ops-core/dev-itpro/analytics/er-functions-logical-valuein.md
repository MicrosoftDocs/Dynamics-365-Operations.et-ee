---
title: ER-i funktsioon VALUEIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUEIN.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d0df97234df41d11897473dea4e85354e82d36ec
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041695"
---
# <span data-ttu-id="0d225-103"><a name="VALUEIN">ER-i funktsioon VALUEIN</a></span><span class="sxs-lookup"><span data-stu-id="0d225-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d225-104">Funktsioon `VALUEIN` määratleb, kas määratud sisend vastab määratud loendis määratud üksuse mis tahes väärtusele.</span><span class="sxs-lookup"><span data-stu-id="0d225-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0d225-105">See tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul.</span><span class="sxs-lookup"><span data-stu-id="0d225-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0d225-106">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="0d225-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d225-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="0d225-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="0d225-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="0d225-108">Arguments</span></span>

<span data-ttu-id="0d225-109">`input`: *väli*</span><span class="sxs-lookup"><span data-stu-id="0d225-109">`input`: *Field*</span></span>

<span data-ttu-id="0d225-110">Tüübi *Kirjete loend* andmeallika üksuse kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="0d225-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="0d225-111">Selle üksuse väärtus vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="0d225-111">The value of this item will be matched.</span></span>

<span data-ttu-id="0d225-112">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="0d225-112">`list`: *Record list*</span></span>

<span data-ttu-id="0d225-113">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="0d225-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0d225-114">`list item expression`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="0d225-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="0d225-115">Kehtiv tingimuslik avaldist, mis osutab või sisaldab määratletud loendi üksikut välja, mida tuleks kasutada vastendamiseks.</span><span class="sxs-lookup"><span data-stu-id="0d225-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d225-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="0d225-116">Return values</span></span>

<span data-ttu-id="0d225-117">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="0d225-117">*Boolean*</span></span>

<span data-ttu-id="0d225-118">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="0d225-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0d225-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="0d225-119">Usage notes</span></span>

<span data-ttu-id="0d225-120">Üldiselt on funktsioon `VALUEIN` tõlgitud kui tingimuste **OR** kogumit.</span><span class="sxs-lookup"><span data-stu-id="0d225-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="0d225-121">Mõnel juhul saab selle teisendada andmebaasi SQL-lauseks, kasutades `EXISTS JOIN` tehtemärki.</span><span class="sxs-lookup"><span data-stu-id="0d225-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="0d225-122">Näide 1</span><span class="sxs-lookup"><span data-stu-id="0d225-122">Example 1</span></span>

<span data-ttu-id="0d225-123">Mudeli vastendamises saate määratleda tüübi *Arvutatud väli* andmeallika **Loend**.</span><span class="sxs-lookup"><span data-stu-id="0d225-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="0d225-124">See andmeallikas sisaldab avaldist `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="0d225-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="0d225-125">Andmeallika kutsumisel, kui see on konfigureeritud avaldisena `VALUEIN ("B", List, List.Value)`, tagastab see väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="0d225-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="0d225-126">Sellisel juhul on funktsioon `VALUEIN` tõlgitud järgmiseks tingimuste kogumiks: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, kus `("B" = "b")` on võrdne tulemusega **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="0d225-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="0d225-127">Andmeallika kutsumisel, kui see on konfigureeritud avaldisena `VALUEIN ("B", List, LEFT(List.Value, 0))`, tagastab see väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0d225-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="0d225-128">Sellisel juhul on funktsioon `VALUEIN` tõlgitud järgmiseks tingimuseks: `("B" = "")`, mis ei ole võrdne tulemusega **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="0d225-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="0d225-129">Taolise tingimuse teksti tähemärkide arvu ülempiir on 32 768 tähemärki.</span><span class="sxs-lookup"><span data-stu-id="0d225-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="0d225-130">Seetõttu ei tohiks te luua andmeallikaid, mis võivad käitusajal seda piirangut ületada.</span><span class="sxs-lookup"><span data-stu-id="0d225-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="0d225-131">Kui piirang ületatakse, lõpetab rakendus töötamise ja esitatakse erand.</span><span class="sxs-lookup"><span data-stu-id="0d225-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="0d225-132">Selline olukord võib tekkida näiteks siis kui andmeallikas konfigureeritakse kui `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` ja loendid **Loend1** ning **Loend2** sisaldavad suurt hulka kirjeid.</span><span class="sxs-lookup"><span data-stu-id="0d225-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="0d225-133">Mõnel juhul tõlgitakse funktsioon `VALUEIN` andmebaasi aruandeks, kasutades `EXISTS JOIN` tehtemärki.</span><span class="sxs-lookup"><span data-stu-id="0d225-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="0d225-134">See juhtub, kui kasutatakse funktsiooni [FILTER](er-functions-list-filter.md) ja järgmised tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="0d225-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="0d225-135">Suvand **ASK FOR QUERY** on funktsiooni `VALUEIN` andmeallika jaoks välja lülitatud, mis viitab kirjete loendile.</span><span class="sxs-lookup"><span data-stu-id="0d225-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="0d225-136">Sellele andmeallikale ei rakendada käitusajal lisatingimusi.</span><span class="sxs-lookup"><span data-stu-id="0d225-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="0d225-137">Pesastatud avaldisi ei ole andmeallika funktsiooni `VALUEIN` jaoks konfigureeritud, mis viitab kirjete loendile.</span><span class="sxs-lookup"><span data-stu-id="0d225-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="0d225-138">Funktsiooni `VALUEIN` loendi üksus viitab määratletud andmeallika väljale, mitte avaldisele ega meetodile.</span><span class="sxs-lookup"><span data-stu-id="0d225-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="0d225-139">Kaaluge selle suvandi kasutamist funktsiooni [WHERE](er-functions-list-where.md) asemel, nagu selles näites varasemalt kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="0d225-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="0d225-140">Näide 2</span><span class="sxs-lookup"><span data-stu-id="0d225-140">Example 2</span></span>

<span data-ttu-id="0d225-141">Määratlege oma mudelivastenduses järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="0d225-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="0d225-142">Tüübi *Tabeli kirjete* andmeallikas **Sisse**.</span><span class="sxs-lookup"><span data-stu-id="0d225-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="0d225-143">See andmeallikas viitab intrastati tabelile.</span><span class="sxs-lookup"><span data-stu-id="0d225-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="0d225-144">Tüübi *Tabeli kirjete* andmeallikas **Port**.</span><span class="sxs-lookup"><span data-stu-id="0d225-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="0d225-145">See andmeallikas viitab tabelile IntrastatPort.</span><span class="sxs-lookup"><span data-stu-id="0d225-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="0d225-146">Kui kutsutakse andmeallikas, mis on konfigureeritud kui avaldis `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, luuakse intrastati tabeli filtreeritud kirjete tagastamiseks järgmine SQL-lause.</span><span class="sxs-lookup"><span data-stu-id="0d225-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="0d225-147">Väljade **dataAreaId** jaoks luuakse lõplik SQL-lause, kasutades tehtemärki `IN`.</span><span class="sxs-lookup"><span data-stu-id="0d225-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="0d225-148">Näide 3</span><span class="sxs-lookup"><span data-stu-id="0d225-148">Example 3</span></span>

<span data-ttu-id="0d225-149">Määratlege oma mudelivastenduses järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="0d225-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="0d225-150">Tüübi *Arvutatud väli* andmeallikas **Le**.</span><span class="sxs-lookup"><span data-stu-id="0d225-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="0d225-151">See andmeallikas sisaldab avaldist `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="0d225-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="0d225-152">Tüübi *Tabeli kirjete* andmeallikas **Sisse**.</span><span class="sxs-lookup"><span data-stu-id="0d225-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="0d225-153">See andmeallikas viitab intrastati tabelile ja suvand **Ettevõtteülene** on selle jaoks sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="0d225-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="0d225-154">Kui kutsutakse andmeallikas, mis on konfigureeritud avaldisena `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, sisaldab lõplik SQL-i aruanne järgmist tingimust.</span><span class="sxs-lookup"><span data-stu-id="0d225-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="0d225-155">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0d225-155">Additional resources</span></span>

[<span data-ttu-id="0d225-156">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="0d225-156">Logical functions</span></span>](er-functions-category-logical.md)
