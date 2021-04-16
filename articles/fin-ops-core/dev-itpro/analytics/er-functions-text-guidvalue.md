---
title: ER-i funktsioon GUIDVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni GUIDVALUE.
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
ms.openlocfilehash: ec8222708b999a17794a396b5bf807dab037799d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746383"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="2e345-103">ER-i funktsioon GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="2e345-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e345-104">Funktsioon `GUIDVALUE` teisendab *stringi* tüübi määratud sisendi andmeüksuseks tüübiga *GUID*.</span><span class="sxs-lookup"><span data-stu-id="2e345-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e345-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="2e345-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="2e345-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="2e345-106">Arguments</span></span>

<span data-ttu-id="2e345-107">`input`: *string*</span><span class="sxs-lookup"><span data-stu-id="2e345-107">`input`: *String*</span></span>

<span data-ttu-id="2e345-108">Tüübi *String* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="2e345-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2e345-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="2e345-109">Return values</span></span>

<span data-ttu-id="2e345-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2e345-110">*GUID*</span></span>

<span data-ttu-id="2e345-111">Tulemuseks olev globaalselt kordumatu ID (GUID) väärtus.</span><span class="sxs-lookup"><span data-stu-id="2e345-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2e345-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="2e345-112">Usage notes</span></span>

<span data-ttu-id="2e345-113">Selleks, et teisendada vastupidises suunas (see tähendab andmetüübi *GUID* määratletud sisendi teisendamiseks andmetüübi *String* andmeüksuseks), saate kasutada funktsiooni [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="2e345-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="2e345-114">Näide</span><span class="sxs-lookup"><span data-stu-id="2e345-114">Example</span></span>

<span data-ttu-id="2e345-115">Määratlege oma mudelivastenduses järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="2e345-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="2e345-116">Tüübi *Arvutatud väli* andmeallikas **myID**, mis sisaldab avaldist `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="2e345-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="2e345-117">Tüübi **Tabelikirjed** andmeallikas *Kasutajad*, mis viitab tabelile UserInfo</span><span class="sxs-lookup"><span data-stu-id="2e345-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="2e345-118">Seejärel saate kasutada avaldist, näiteks `FILTER (Users, Users.objectId = myID)`, tabeli UserInfo filtreerimiseks andmetüübi *GUID* välja **objectId** alusel.</span><span class="sxs-lookup"><span data-stu-id="2e345-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e345-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2e345-119">Additional resources</span></span>

[<span data-ttu-id="2e345-120">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="2e345-120">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]