---
title: Funktsioon ENDSWITH ER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse ENDSWITH elektroonilise aruandluse (ER) funktsiooni.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: bdd2f364e2d0b80d3df20592ec827dcabf99a06c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745397"
---
# <a name="endswith-er-function"></a><span data-ttu-id="16109-103">Funktsioon ENDSWITH ER</span><span class="sxs-lookup"><span data-stu-id="16109-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16109-104">See `ENDSWITH` funktsioon määratleb, kas määratud sisestus algab määratud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="16109-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="16109-105">See toob *Tõeväärtus* väärtuseks **Tõde** määratud sisestusteksti, kui see algab määratud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="16109-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="16109-106">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="16109-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="16109-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="16109-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="16109-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="16109-108">Arguments</span></span>

<span data-ttu-id="16109-109">`input`: *string*</span><span class="sxs-lookup"><span data-stu-id="16109-109">`input`: *String*</span></span>

<span data-ttu-id="16109-110">Andmeallika kehtiv üksuse tee *Stringi* tüüpi või stringikonstandi, mille väärtus võib algata teise argumendiga.</span><span class="sxs-lookup"><span data-stu-id="16109-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="16109-111">`start text`: *string*</span><span class="sxs-lookup"><span data-stu-id="16109-111">`start text`: *String*</span></span>

<span data-ttu-id="16109-112">Andmeallika kehtiv üksuse tee *Stringi* tüüpi või stringikonstandi, mille väärtus võib algata teise argumendiga.</span><span class="sxs-lookup"><span data-stu-id="16109-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="16109-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="16109-113">Return values</span></span>

<span data-ttu-id="16109-114">*Loogiline*</span><span class="sxs-lookup"><span data-stu-id="16109-114">*Boolean*</span></span>

<span data-ttu-id="16109-115">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="16109-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="16109-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="16109-116">Usage notes</span></span>

<span data-ttu-id="16109-117">Seda funktsiooni saab kasutada [FILTRI](er-functions-list-filter.md) funktsiooni tingimuseavaldise määramiseks ainult siis, kui vastav vastendamine on konfigureeritud [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) juurdepääsuks [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="16109-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="16109-118">Vastasel korral ilmneb erand kujundusajas.</span><span class="sxs-lookup"><span data-stu-id="16109-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="16109-119">Teile kuvatav teade soovitab teil kasutada tõhususe parandamiseks funktsiooni [WHERE](er-functions-list-where.md) funktsiooni `FILTER` funktsiooni asemel.</span><span class="sxs-lookup"><span data-stu-id="16109-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="16109-120">Näide 1</span><span class="sxs-lookup"><span data-stu-id="16109-120">Example 1</span></span>

<span data-ttu-id="16109-121">Avaldis `ENDSWITH ("abc", "d")` tagastab **väär** väärtuse, samas kui avaldis `ENDSWITH ("abc", "C")` tagastab väärtuse **tõene**.</span><span class="sxs-lookup"><span data-stu-id="16109-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="16109-122">Näide 2</span><span class="sxs-lookup"><span data-stu-id="16109-122">Example 2</span></span>

<span data-ttu-id="16109-123">Avaldis `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` tagastab väärtuse **tõene** kui mudeli andmeallika **aadressi** välja **mudeli** andmeallikas lõpeb stringiga **USA**.</span><span class="sxs-lookup"><span data-stu-id="16109-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="16109-124">Muidu tagastatakse väärtus **Väär**.</span><span class="sxs-lookup"><span data-stu-id="16109-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16109-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="16109-125">Additional resources</span></span>

[<span data-ttu-id="16109-126">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="16109-126">Logical functions</span></span>](er-functions-category-logical.md)
