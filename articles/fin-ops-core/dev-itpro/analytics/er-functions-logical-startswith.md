---
title: Funktsioon STARTSWITH ER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse STARTSWITH elektroonilise aruandluse (ER) funktsiooni.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 22e99d9e131410820abd12536b8d4f3e868c6863
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557513"
---
# <a name="startswith-er-function"></a><span data-ttu-id="f917c-103">Funktsioon STARTSWITH ER</span><span class="sxs-lookup"><span data-stu-id="f917c-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f917c-104">See `STARTSWITH` funktsioon määratleb, kas määratud sisestus algab määratud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="f917c-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="f917c-105">See toob *Tõeväärtus* väärtuseks **Tõde** määratud sisestusteksti, kui see algab määratud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="f917c-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="f917c-106">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="f917c-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f917c-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="f917c-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="f917c-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="f917c-108">Arguments</span></span>

<span data-ttu-id="f917c-109">`input`: *string*</span><span class="sxs-lookup"><span data-stu-id="f917c-109">`input`: *String*</span></span>

<span data-ttu-id="f917c-110">Andmeallika kehtiv üksuse tee *Stringi* tüüpi või stringikonstandi, mille väärtus võib algata teise argumendiga.</span><span class="sxs-lookup"><span data-stu-id="f917c-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="f917c-111">`start text`: *string*</span><span class="sxs-lookup"><span data-stu-id="f917c-111">`start text`: *String*</span></span>

<span data-ttu-id="f917c-112">Andmeallika kehtiv üksuse tee *Stringi* tüüpi või stringikonstandi, mille väärtus võib algata teise argumendiga.</span><span class="sxs-lookup"><span data-stu-id="f917c-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="f917c-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="f917c-113">Return values</span></span>

<span data-ttu-id="f917c-114">*Loogiline*</span><span class="sxs-lookup"><span data-stu-id="f917c-114">*Boolean*</span></span>

<span data-ttu-id="f917c-115">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="f917c-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f917c-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="f917c-116">Usage notes</span></span>

<span data-ttu-id="f917c-117">Seda funktsiooni saab kasutada [FILTRI](er-functions-list-filter.md) funktsiooni tingimuseavaldise määramiseks ainult siis, kui vastav vastendamine on konfigureeritud [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) juurdepääsuks [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="f917c-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="f917c-118">Vastasel korral ilmneb erand kujundusajas.</span><span class="sxs-lookup"><span data-stu-id="f917c-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="f917c-119">Teile kuvatav teade soovitab teil kasutada tõhususe parandamiseks funktsiooni [WHERE](er-functions-list-where.md) funktsiooni `FILTER` funktsiooni asemel.</span><span class="sxs-lookup"><span data-stu-id="f917c-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="f917c-120">Näide 1</span><span class="sxs-lookup"><span data-stu-id="f917c-120">Example 1</span></span>

<span data-ttu-id="f917c-121">Avaldis `STARTSWITH ("abc", "d")` tagastab **väär** väärtuse, samas kui avaldis `STARTSWITH ("abc", "A")` tagastab väärtuse **tõene**.</span><span class="sxs-lookup"><span data-stu-id="f917c-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f917c-122">Näide 2</span><span class="sxs-lookup"><span data-stu-id="f917c-122">Example 2</span></span>

<span data-ttu-id="f917c-123">Avaldis `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` tagastab väärtuse **tõene** kui mudeli andmeallika **aadressi** välja **mudeli** andmeallikas algab stringiga, mis algab **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="f917c-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="f917c-124">Muidu tagastatakse väärtus **Väär**.</span><span class="sxs-lookup"><span data-stu-id="f917c-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f917c-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f917c-125">Additional resources</span></span>

[<span data-ttu-id="f917c-126">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="f917c-126">Logical functions</span></span>](er-functions-category-logical.md)
