---
title: ER-i funktsioon VALUEINLARGE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUEINLARGE.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705139"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="6e538-103">ER-i funktsioon VALUEINLARGE</span><span class="sxs-lookup"><span data-stu-id="6e538-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e538-104">Funktsioon `VALUEINLARGE` määratleb, kas määratud *Int64* või *Täisarv*-tüüpi sisend vastab määratud loendis määratud üksuse mis tahes väärtusele.</span><span class="sxs-lookup"><span data-stu-id="6e538-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="6e538-105">Funktsioon tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul.</span><span class="sxs-lookup"><span data-stu-id="6e538-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="6e538-106">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="6e538-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="6e538-107">Erinevusest funktsiooniga `VALUEIN` aru saamiseks lugege selle teema hilisemat jaotist [Kasutusmärkus](#usage_note).</span><span class="sxs-lookup"><span data-stu-id="6e538-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e538-108">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6e538-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="6e538-109">Argumendid</span><span class="sxs-lookup"><span data-stu-id="6e538-109">Arguments</span></span>

<span data-ttu-id="6e538-110">`input`: *väli*</span><span class="sxs-lookup"><span data-stu-id="6e538-110">`input`: *Field*</span></span>

<span data-ttu-id="6e538-111">Tüübi *Kirjete loend* andmeallika üksuse kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="6e538-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="6e538-112">Selle üksuse väärtus vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="6e538-112">The value of this item will be matched.</span></span>

<span data-ttu-id="6e538-113">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="6e538-113">`list`: *Record list*</span></span>

<span data-ttu-id="6e538-114">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="6e538-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="6e538-115">`list item expression`: *Avaldis*</span><span class="sxs-lookup"><span data-stu-id="6e538-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="6e538-116">Kehtiv tingimuslik avaldist, mis osutab või sisaldab määratletud loendi üksikut välja, mida tuleks kasutada vastendamiseks.</span><span class="sxs-lookup"><span data-stu-id="6e538-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="6e538-117">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6e538-117">Return values</span></span>

<span data-ttu-id="6e538-118">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="6e538-118">*Boolean*</span></span>

<span data-ttu-id="6e538-119">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="6e538-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="6e538-120"><a name="usage_note">Kasutamise märkused</a></span><span class="sxs-lookup"><span data-stu-id="6e538-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="6e538-121">Kui määratud sisend tähistab *Int64* või *Täisarv* andmeallika tüüpi, mille kutse saab teisendada otseseks SQL-lauseks, teisendatakse määratud loend ajutiseks SQL-tabeliks ja vastendamine tehakse andmebaasis üksiku päringuga `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="6e538-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="6e538-122">Muul juhul toimib funktsioon nagu funktsioon [`VALUEIN`](er-functions-logical-valuein.md).</span><span class="sxs-lookup"><span data-stu-id="6e538-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="6e538-123">Kui määratud sisend tähistab andmeallika üksust, mis on ette nähtud muu kui *Int64* ja *Täisarv*-tüüpi üksusena, ilmneb kujundusajal tõrge, mis teatab, et funktsiooni `VALUEINLARGE` ei saa konfigureeritud ER-lause jaoks rakendada.</span><span class="sxs-lookup"><span data-stu-id="6e538-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="6e538-124">Kui täidetakse funktsiooni `VALUEINLARGE` avaldist ja selle täitmises ulatuses kasutatakse rohkem kui ühte ajutist tabelit, ilmneb käitusaja tõrge.</span><span class="sxs-lookup"><span data-stu-id="6e538-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="6e538-125">Näide</span><span class="sxs-lookup"><span data-stu-id="6e538-125">Example</span></span>

<span data-ttu-id="6e538-126">Määratlege oma mudelivastenduses järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="6e538-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="6e538-127">Tüübi *Tabeli kirjete* andmeallikas **Sisse**.</span><span class="sxs-lookup"><span data-stu-id="6e538-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="6e538-128">See andmeallikas viitab tabelile **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="6e538-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="6e538-129">Suvand **Kontsernisisene** seatakse väärtusele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="6e538-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="6e538-130">Tüübi *Arvutatud väli* andmeallikas **InMemory**.</span><span class="sxs-lookup"><span data-stu-id="6e538-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="6e538-131">See andmeallikas sisaldab avaldist `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="6e538-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="6e538-132">Tüübi *Arvutatud väli* andmeallikas **InFiltered**.</span><span class="sxs-lookup"><span data-stu-id="6e538-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="6e538-133">See andmeallikas sisaldab avaldist `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="6e538-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="6e538-134">Kui andmeallikas **InFiltered** kutsutakse ettevõtte **DEMF** kontekstis, luuakse rakenduse andmebaasis uus, ajutine tabel. Sellesse tabelisse lisatakse kirje ID-de mällu kogutud loend ja tabeli **Intrastat** filtreeritud kirjete tagastamiseks genereeritakse järgmine SQL-lause.</span><span class="sxs-lookup"><span data-stu-id="6e538-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="6e538-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6e538-135">Additional resources</span></span>

[<span data-ttu-id="6e538-136">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6e538-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="6e538-137">VALUEIN funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6e538-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)
