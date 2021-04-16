---
title: ER-i funktsioon CN_GBT_ADDITIONALDIMENSIONID
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CN_GBT_ADDITIONALDIMENSIONID.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ac0b54476265171b3826e43600f99097701231e1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744387"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="1cace-103">ER-i funktsioon CN_GBT_ADDITIONALDIMENSIONID</span><span class="sxs-lookup"><span data-stu-id="1cace-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cace-104">Funktsioon `CN_GBT_ADDITIONALDIMENSIONID` tagastab *stringi* väärtuse, mis tähistab ühte finantsdimensiooni ID-d, mis on määratud stringist võetud.</span><span class="sxs-lookup"><span data-stu-id="1cace-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="1cace-105">Määratud string esitab kõik dimensioonid komadega eraldatud ID-de loendina.</span><span class="sxs-lookup"><span data-stu-id="1cace-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cace-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="1cace-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="1cace-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="1cace-107">Arguments</span></span>

<span data-ttu-id="1cace-108">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="1cace-108">`text`: *String*</span></span>

<span data-ttu-id="1cace-109">*String* väärtusm mis esitab kõik dimensioonid komadega eraldatud ID-de loendina.</span><span class="sxs-lookup"><span data-stu-id="1cace-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="1cace-110">`number`: täisarv</span><span class="sxs-lookup"><span data-stu-id="1cace-110">`number`: Integer</span></span>

<span data-ttu-id="1cace-111">*Täisarvu* väärtus, mis määratleb taotletud dimensiooni seeriakoodi määratud stringis.</span><span class="sxs-lookup"><span data-stu-id="1cace-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="1cace-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="1cace-112">Return values</span></span>

<span data-ttu-id="1cace-113">*String*</span><span class="sxs-lookup"><span data-stu-id="1cace-113">*String*</span></span>

<span data-ttu-id="1cace-114">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="1cace-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1cace-115">Näide</span><span class="sxs-lookup"><span data-stu-id="1cace-115">Example</span></span>

<span data-ttu-id="1cace-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` tagastab **„CC”**.</span><span class="sxs-lookup"><span data-stu-id="1cace-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1cace-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1cace-117">Additional resources</span></span>

[<span data-ttu-id="1cace-118">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="1cace-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]