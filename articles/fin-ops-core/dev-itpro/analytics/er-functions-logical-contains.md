---
title: CONTAINS ER funktsioon
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni COUNTAINS.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048866"
---
# <a name="contains-er-function"></a><span data-ttu-id="2ae9d-103">CONTAINS ER funktsioon</span><span class="sxs-lookup"><span data-stu-id="2ae9d-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ae9d-104">See `CONTAINS` funktsioon määratleb, kas määratud sisestus algab määratud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="2ae9d-105">See toob *Tõeväärtus* väärtuseks **Tõde** määratud sisestusteksti, kui see algab määratud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="2ae9d-106">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae9d-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="2ae9d-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="2ae9d-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="2ae9d-108">Arguments</span></span>

<span data-ttu-id="2ae9d-109">`input`: *string*</span><span class="sxs-lookup"><span data-stu-id="2ae9d-109">`input`: *String*</span></span>

<span data-ttu-id="2ae9d-110">Andmeallika kehtiv üksuse tee *Stringi* tüüpi või stringikonstandi, mille väärtus võib algata teise argumendiga.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="2ae9d-111">`search text`: *string*</span><span class="sxs-lookup"><span data-stu-id="2ae9d-111">`search text`: *String*</span></span>

<span data-ttu-id="2ae9d-112">Andmeallika kehtiv üksuse tee *Stringi* tüüpi või stringikonstandi, mille väärtus võib algata teise argumendiga.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ae9d-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="2ae9d-113">Return values</span></span>

<span data-ttu-id="2ae9d-114">*Loogiline*</span><span class="sxs-lookup"><span data-stu-id="2ae9d-114">*Boolean*</span></span>

<span data-ttu-id="2ae9d-115">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2ae9d-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="2ae9d-116">Usage notes</span></span>

<span data-ttu-id="2ae9d-117">Seda funktsiooni saab kasutada [FILTRI](er-functions-list-filter.md) funktsiooni tingimuseavaldise määramiseks ainult siis, kui vastav vastendamine on konfigureeritud [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) juurdepääsuks [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="2ae9d-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="2ae9d-118">Vastasel korral ilmneb erand kujundusajas.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="2ae9d-119">Teile kuvatav teade soovitab teil kasutada tõhususe parandamiseks funktsiooni [WHERE](er-functions-list-where.md) funktsiooni `FILTER` funktsiooni asemel.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="2ae9d-120">Näide 1</span><span class="sxs-lookup"><span data-stu-id="2ae9d-120">Example 1</span></span>

<span data-ttu-id="2ae9d-121">Avaldis `CONTAINS ("abc", "d")` tagastab **väär** väärtuse, samas kui avaldis `CONTAINS ("abc", "C")` tagastab väärtuse **tõene**.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2ae9d-122">Näide 2</span><span class="sxs-lookup"><span data-stu-id="2ae9d-122">Example 2</span></span>

<span data-ttu-id="2ae9d-123">Avaldis `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` tagastab väärtuse **tõene** kui mudeli andmeallika **aadressi** välja **mudeli** andmeallikas algab stringiga, mis algab **DEU**.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="2ae9d-124">Muidu tagastatakse väärtus **Väär**.</span><span class="sxs-lookup"><span data-stu-id="2ae9d-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ae9d-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2ae9d-125">Additional resources</span></span>

[<span data-ttu-id="2ae9d-126">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="2ae9d-126">Logical functions</span></span>](er-functions-category-logical.md)
