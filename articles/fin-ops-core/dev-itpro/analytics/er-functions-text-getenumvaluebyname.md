---
title: ER-i funktsioon GETENUMVALUEBYNAME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni GETENUMVALUEBYNAME.
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916840"
---
# <span data-ttu-id="6f6bd-103"><a name="GETENUMVALUEBYNAME">ER-i funktsioon GETENUMVALUEBYNAME</a></span><span class="sxs-lookup"><span data-stu-id="6f6bd-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f6bd-104">Funktsioon `GETENUMVALUEBYNAME` otsib määratud *loetelu* andmeallikast konkreetset loetelu väärtust, kasutades loendi nime, mis on määratud *stringi* väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="6f6bd-105">Kui *loetelu* väärtus leitakse, tagastab funktsioon selle.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="6f6bd-106">Vastasel korral tagastab funktsioon loendamise väärtuse **null**.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6bd-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6f6bd-107">Syntax</span></span>

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="6f6bd-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="6f6bd-108">Arguments</span></span>

<span data-ttu-id="6f6bd-109">`enumeration data source path`: *loetelu*</span><span class="sxs-lookup"><span data-stu-id="6f6bd-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="6f6bd-110">Ühe järgmistest loenditüüpidest andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="6f6bd-111">Elektroonilise aruandluse (ER) mudeli loetelu</span><span class="sxs-lookup"><span data-stu-id="6f6bd-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="6f6bd-112">ER-vormingu loetelu</span><span class="sxs-lookup"><span data-stu-id="6f6bd-112">ER format enumeration</span></span>
- <span data-ttu-id="6f6bd-113">Microsoft Dynamics 365 Finance’i loetelu</span><span class="sxs-lookup"><span data-stu-id="6f6bd-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="6f6bd-114">`enumeration value text`: *string*</span><span class="sxs-lookup"><span data-stu-id="6f6bd-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="6f6bd-115">Stringi väärtus, mis tähistab ühe loetelu väärtuse nime.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="6f6bd-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6f6bd-116">Return values</span></span>

<span data-ttu-id="6f6bd-117">Nullitav *loetelu*</span><span class="sxs-lookup"><span data-stu-id="6f6bd-117">Nullable *Enum*</span></span>

<span data-ttu-id="6f6bd-118">Tulemiks saadud loetelu väärtus.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6f6bd-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="6f6bd-119">Usage notes</span></span>

<span data-ttu-id="6f6bd-120">Ühtegi erandit ei esitata, kui väärtust *Loetelu* ei leita, kasutades loetelu väärtuse nime, mis on määratud *stringi* väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="6f6bd-121">Näide</span><span class="sxs-lookup"><span data-stu-id="6f6bd-121">Example</span></span>

<span data-ttu-id="6f6bd-122">Järgmises näites on andmemudelis kasutusele võetud loetelu **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="6f6bd-123">Pange tähele, et loetelu väärtuste puhul on määratletud sildid.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="6f6bd-124">Järgmises näites on toodud järgmised üksikasjad:</span><span class="sxs-lookup"><span data-stu-id="6f6bd-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="6f6bd-125">Andmeallikas **$Direction** konfigureeritakse ER-i aruandes.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="6f6bd-126">See andmeallikas konfigureeritakse mudeli **ReportDirection** loetelu põhjal.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="6f6bd-127">Avaldis `$IsArrivals` on mõeldud kasutama mudeli loetelul põhinevat andmeallikat **$Direction** selle funktsiooni parameetrina.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="6f6bd-128">Võrdluse avaldise väärtus on **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="6f6bd-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="6f6bd-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6f6bd-129">Additional resources</span></span>

[<span data-ttu-id="6f6bd-130">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="6f6bd-130">Text functions</span></span>](er-functions-category-text.md)
