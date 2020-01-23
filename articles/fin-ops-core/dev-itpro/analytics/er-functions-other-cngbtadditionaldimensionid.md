---
title: ER-i funktsioon CN_GBT_ADDITIONALDIMENSIONID
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CN_GBT_ADDITIONALDIMENSIONID.
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
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917024"
---
# <span data-ttu-id="e86ee-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">ER-i funktsioon CN_GBT_ADDITIONALDIMENSIONID</a></span><span class="sxs-lookup"><span data-stu-id="e86ee-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e86ee-104">Funktsioon `CN_GBT_ADDITIONALDIMENSIONID` tagastab *stringi* väärtuse, mis tähistab ühte finantsdimensiooni ID-d, mis on määratud stringist võetud.</span><span class="sxs-lookup"><span data-stu-id="e86ee-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="e86ee-105">Määratud string esitab kõik dimensioonid komadega eraldatud ID-de loendina.</span><span class="sxs-lookup"><span data-stu-id="e86ee-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86ee-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="e86ee-106">Syntax</span></span>

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="e86ee-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="e86ee-107">Arguments</span></span>

<span data-ttu-id="e86ee-108">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="e86ee-108">`text`: *String*</span></span>

<span data-ttu-id="e86ee-109">*String* väärtusm mis esitab kõik dimensioonid komadega eraldatud ID-de loendina.</span><span class="sxs-lookup"><span data-stu-id="e86ee-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="e86ee-110">`number`: täisarv</span><span class="sxs-lookup"><span data-stu-id="e86ee-110">`number`: Integer</span></span>

<span data-ttu-id="e86ee-111">*Täisarvu* väärtus, mis määratleb taotletud dimensiooni seeriakoodi määratud stringis.</span><span class="sxs-lookup"><span data-stu-id="e86ee-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="e86ee-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="e86ee-112">Return values</span></span>

<span data-ttu-id="e86ee-113">*String*</span><span class="sxs-lookup"><span data-stu-id="e86ee-113">*String*</span></span>

<span data-ttu-id="e86ee-114">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="e86ee-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e86ee-115">Näide</span><span class="sxs-lookup"><span data-stu-id="e86ee-115">Example</span></span>

<span data-ttu-id="e86ee-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` tagastab **„CC”**.</span><span class="sxs-lookup"><span data-stu-id="e86ee-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e86ee-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e86ee-117">Additional resources</span></span>

[<span data-ttu-id="e86ee-118">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="e86ee-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
