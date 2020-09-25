---
title: ER-i funktsioon CONCATENATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CONCATENATE
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
ms.openlocfilehash: 1a21140e5636ebd96eca4be90308c915e77510e1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743899"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="49a5e-103">ER-i funktsioon CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="49a5e-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49a5e-104">Funktsioon `CONCATENATE` tagastab kõik määratud tekstistringi *stringi* väärtusena pärast nende üheks stringiks ühendamist.</span><span class="sxs-lookup"><span data-stu-id="49a5e-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a5e-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="49a5e-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="49a5e-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="49a5e-106">Arguments</span></span>

<span data-ttu-id="49a5e-107">`text 1`: *string*</span><span class="sxs-lookup"><span data-stu-id="49a5e-107">`text 1`: *String*</span></span>

<span data-ttu-id="49a5e-108">Viide andmetüübi *String* andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="49a5e-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="49a5e-109">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="49a5e-109">This argument is required.</span></span>

<span data-ttu-id="49a5e-110">`text N`: *string*</span><span class="sxs-lookup"><span data-stu-id="49a5e-110">`text N`: *String*</span></span>

<span data-ttu-id="49a5e-111">Viide andmetüübi *String* andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="49a5e-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="49a5e-112">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="49a5e-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="49a5e-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="49a5e-113">Return values</span></span>

<span data-ttu-id="49a5e-114">*String*</span><span class="sxs-lookup"><span data-stu-id="49a5e-114">*String*</span></span>

<span data-ttu-id="49a5e-115">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="49a5e-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="49a5e-116">Näide</span><span class="sxs-lookup"><span data-stu-id="49a5e-116">Example</span></span>

<span data-ttu-id="49a5e-117">`CONCATENATE ("abc", "def")` tagastab **„abcdef”**.</span><span class="sxs-lookup"><span data-stu-id="49a5e-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="49a5e-118">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="49a5e-118">Usage notes</span></span>

<span data-ttu-id="49a5e-119">Avaldis `"abc" & "def"` annab vastuseks samuti väärtuse **„abcdef”**.</span><span class="sxs-lookup"><span data-stu-id="49a5e-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49a5e-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="49a5e-120">Additional resources</span></span>

[<span data-ttu-id="49a5e-121">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="49a5e-121">Text functions</span></span>](er-functions-category-text.md)
