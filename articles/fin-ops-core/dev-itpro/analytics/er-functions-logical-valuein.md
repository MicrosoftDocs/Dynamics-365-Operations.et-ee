---
title: ER-i funktsioon VALUEIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUEIN.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: e5a0ac314a61abce610407550e65479cbf5a6b5b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565828"
---
# <a name="valuein-er-function"></a><span data-ttu-id="440fd-103">ER-i funktsioon VALUEIN</span><span class="sxs-lookup"><span data-stu-id="440fd-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="440fd-104">Funktsioon `VALUEIN` määratleb, kas määratud sisend vastab määratud loendis määratud üksuse mis tahes väärtusele.</span><span class="sxs-lookup"><span data-stu-id="440fd-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="440fd-105">See tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul.</span><span class="sxs-lookup"><span data-stu-id="440fd-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="440fd-106">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="440fd-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="440fd-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="440fd-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="440fd-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="440fd-108">Arguments</span></span>

<span data-ttu-id="440fd-109">`input`: *väli*</span><span class="sxs-lookup"><span data-stu-id="440fd-109">`input`: *Field*</span></span>

<span data-ttu-id="440fd-110">Tüübi *Kirjete loend* andmeallika üksuse kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="440fd-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="440fd-111">Selle üksuse väärtus vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="440fd-111">The value of this item will be matched.</span></span>

<span data-ttu-id="440fd-112">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="440fd-112">`list`: *Record list*</span></span>

<span data-ttu-id="440fd-113">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="440fd-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="440fd-114">`list item expression`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="440fd-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="440fd-115">Kehtiv tingimuslik avaldist, mis osutab või sisaldab määratletud loendi üksikut välja, mida tuleks kasutada vastendamiseks.</span><span class="sxs-lookup"><span data-stu-id="440fd-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="440fd-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="440fd-116">Return values</span></span>

<span data-ttu-id="440fd-117">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="440fd-117">*Boolean*</span></span>

<span data-ttu-id="440fd-118">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="440fd-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="440fd-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="440fd-119">Usage notes</span></span>

<span data-ttu-id="440fd-120">Üldiselt on funktsioon `VALUEIN` tõlgitud kui tingimuste **OR** kogumit.</span><span class="sxs-lookup"><span data-stu-id="440fd-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="440fd-121">Kui tingimuste **OR** loend on suur ja SQL-lause maksimaalne kogupikkus võidakse ületada, kaaluge funktsiooni [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) kasutamist.</span><span class="sxs-lookup"><span data-stu-id="440fd-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="440fd-122">Mõnel juhul saab selle teisendada andmebaasi SQL-lauseks, kasutades `EXISTS JOIN` tehtemärki.</span><span class="sxs-lookup"><span data-stu-id="440fd-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="440fd-123">Näide 1</span><span class="sxs-lookup"><span data-stu-id="440fd-123">Example 1</span></span>

<span data-ttu-id="440fd-124">Mudeli vastendamises saate määratleda tüübi *Arvutatud väli* andmeallika **Loend**.</span><span class="sxs-lookup"><span data-stu-id="440fd-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="440fd-125">See andmeallikas sisaldab avaldist `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="440fd-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="440fd-126">Andmeallika kutsumisel, kui see on konfigureeritud avaldisena `VALUEIN ("B", List, List.Value)`, tagastab see väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="440fd-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="440fd-127">Sellisel juhul on funktsioon `VALUEIN` tõlgitud järgmiseks tingimuste kogumiks: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, kus `("B" = "b")` on võrdne tulemusega **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="440fd-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="440fd-128">Andmeallika kutsumisel, kui see on konfigureeritud avaldisena `VALUEIN ("B", List, LEFT(List.Value, 0))`, tagastab see väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="440fd-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="440fd-129">Sellisel juhul on funktsioon `VALUEIN` tõlgitud järgmiseks tingimuseks: `("B" = "")`, mis ei ole võrdne tulemusega **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="440fd-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="440fd-130">Taolise tingimuse teksti tähemärkide arvu ülempiir on 32 768 tähemärki.</span><span class="sxs-lookup"><span data-stu-id="440fd-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="440fd-131">Seetõttu ei tohiks te luua andmeallikaid, mis võivad käitusajal seda piirangut ületada.</span><span class="sxs-lookup"><span data-stu-id="440fd-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="440fd-132">Kui piirang ületatakse, lõpetab rakendus töötamise ja esitatakse erand.</span><span class="sxs-lookup"><span data-stu-id="440fd-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="440fd-133">Selline olukord võib tekkida näiteks siis kui andmeallikas konfigureeritakse kui `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` ja loendid **Loend1** ning **Loend2** sisaldavad suurt hulka kirjeid.</span><span class="sxs-lookup"><span data-stu-id="440fd-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="440fd-134">Mõnel juhul tõlgitakse funktsioon `VALUEIN` andmebaasi aruandeks, kasutades `EXISTS JOIN` tehtemärki.</span><span class="sxs-lookup"><span data-stu-id="440fd-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="440fd-135">See juhtub, kui kasutatakse funktsiooni [`FILTER`](er-functions-list-filter.md) ja järgmised tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="440fd-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="440fd-136">Suvand **ASK FOR QUERY** on funktsiooni `VALUEIN` andmeallika jaoks välja lülitatud, mis viitab kirjete loendile.</span><span class="sxs-lookup"><span data-stu-id="440fd-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="440fd-137">Sellele andmeallikale ei rakendada käitusajal lisatingimusi.</span><span class="sxs-lookup"><span data-stu-id="440fd-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="440fd-138">Pesastatud avaldisi ei ole andmeallika funktsiooni `VALUEIN` jaoks konfigureeritud, mis viitab kirjete loendile.</span><span class="sxs-lookup"><span data-stu-id="440fd-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="440fd-139">Funktsiooni `VALUEIN` loendi üksus viitab määratletud andmeallika väljale, mitte avaldisele ega meetodile.</span><span class="sxs-lookup"><span data-stu-id="440fd-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="440fd-140">Kaaluge selle suvandi kasutamist funktsiooni [`WHERE`](er-functions-list-where.md) asemel, nagu selles näites varasemalt kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="440fd-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="440fd-141">Näide 2</span><span class="sxs-lookup"><span data-stu-id="440fd-141">Example 2</span></span>

<span data-ttu-id="440fd-142">Määratlege oma mudelivastenduses järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="440fd-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="440fd-143">Tüübi *Tabeli kirjete* andmeallikas **Sisse**.</span><span class="sxs-lookup"><span data-stu-id="440fd-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="440fd-144">See andmeallikas viitab intrastati tabelile.</span><span class="sxs-lookup"><span data-stu-id="440fd-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="440fd-145">Tüübi *Tabeli kirjete* andmeallikas **Port**.</span><span class="sxs-lookup"><span data-stu-id="440fd-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="440fd-146">See andmeallikas viitab tabelile IntrastatPort.</span><span class="sxs-lookup"><span data-stu-id="440fd-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="440fd-147">Kui kutsutakse andmeallikas, mis on konfigureeritud kui avaldis `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, luuakse intrastati tabeli filtreeritud kirjete tagastamiseks järgmine SQL-lause.</span><span class="sxs-lookup"><span data-stu-id="440fd-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="440fd-148">Väljade **dataAreaId** jaoks luuakse lõplik SQL-lause, kasutades tehtemärki `IN`.</span><span class="sxs-lookup"><span data-stu-id="440fd-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="440fd-149">Näide 3</span><span class="sxs-lookup"><span data-stu-id="440fd-149">Example 3</span></span>

<span data-ttu-id="440fd-150">Määratlege oma mudelivastenduses järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="440fd-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="440fd-151">Tüübi *Arvutatud väli* andmeallikas **Le**.</span><span class="sxs-lookup"><span data-stu-id="440fd-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="440fd-152">See andmeallikas sisaldab avaldist `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="440fd-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="440fd-153">Tüübi *Tabeli kirjete* andmeallikas **Sisse**.</span><span class="sxs-lookup"><span data-stu-id="440fd-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="440fd-154">See andmeallikas viitab intrastati tabelile ja suvand **Ettevõtteülene** on selle jaoks sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="440fd-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="440fd-155">Kui kutsutakse andmeallikas, mis on konfigureeritud avaldisena `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, sisaldab lõplik SQL-i aruanne järgmist tingimust.</span><span class="sxs-lookup"><span data-stu-id="440fd-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="440fd-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="440fd-156">Additional resources</span></span>

[<span data-ttu-id="440fd-157">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="440fd-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="440fd-158">VALUEINLARGE funktsioonid</span><span class="sxs-lookup"><span data-stu-id="440fd-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]