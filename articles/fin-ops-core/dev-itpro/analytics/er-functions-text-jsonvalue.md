---
title: ER-i funktsioon JSONVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni JSONVALUE.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746359"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="1f797-103">ER-i funktsioon JSONVALUE</span><span class="sxs-lookup"><span data-stu-id="1f797-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f797-104">Funktsioon `JSONVALUE` sõelub andmeid vormingus JavaScript Object Notation (JSON), millele pääseb juurde määratud tee kaudu ja see ekstraktib skalaarväärtuse, millel on määratud ID.</span><span class="sxs-lookup"><span data-stu-id="1f797-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="1f797-105">Seejärel tagastab see ekstraktitud skalaarväärtus *stringi* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="1f797-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f797-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="1f797-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="1f797-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="1f797-107">Arguments</span></span>

<span data-ttu-id="1f797-108">`input`: *string*</span><span class="sxs-lookup"><span data-stu-id="1f797-108">`input`: *String*</span></span>

<span data-ttu-id="1f797-109">Tüübi *String* andmeallika kehtiv tee, mis sisaldab JSON-andmeid.</span><span class="sxs-lookup"><span data-stu-id="1f797-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="1f797-110">`path`: *string*</span><span class="sxs-lookup"><span data-stu-id="1f797-110">`path`: *String*</span></span>

<span data-ttu-id="1f797-111">JSON-andmete skalaarväärtuse identifikaator.</span><span class="sxs-lookup"><span data-stu-id="1f797-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f797-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="1f797-112">Return values</span></span>

<span data-ttu-id="1f797-113">*String*</span><span class="sxs-lookup"><span data-stu-id="1f797-113">*String*</span></span>

<span data-ttu-id="1f797-114">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="1f797-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1f797-115">Näide</span><span class="sxs-lookup"><span data-stu-id="1f797-115">Example</span></span>

<span data-ttu-id="1f797-116">Andmeallikas **JsonField** sisaldab JSON-vormingus järgmisi andmeid: **{„BuildNumber”:„7.3.1234.1”, „KeyThumbprint”:„7366E”}**.</span><span class="sxs-lookup"><span data-stu-id="1f797-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="1f797-117">Sellisel juhul tagastab avaldis `JSONVALUE (JsonField, "BuildNumber")` järgmise andmetüübi *String* väärtuse: **„7.3.1234.1”**.</span><span class="sxs-lookup"><span data-stu-id="1f797-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f797-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1f797-118">Additional resources</span></span>

[<span data-ttu-id="1f797-119">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="1f797-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]