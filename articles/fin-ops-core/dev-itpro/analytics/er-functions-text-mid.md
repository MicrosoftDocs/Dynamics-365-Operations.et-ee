---
title: ER-i funktsioon MID
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni MID.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746263"
---
# <a name="mid-er-function"></a><span data-ttu-id="feb91-103">ER-i funktsioon MID</span><span class="sxs-lookup"><span data-stu-id="feb91-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="feb91-104">Funktsioon `MID` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringist, alustades määratud kohast.</span><span class="sxs-lookup"><span data-stu-id="feb91-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb91-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="feb91-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="feb91-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="feb91-106">Arguments</span></span>

<span data-ttu-id="feb91-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="feb91-107">`text`: *String*</span></span>

<span data-ttu-id="feb91-108">*Stringi* väärtus, mis määrab teksti, millest märke tagastada.</span><span class="sxs-lookup"><span data-stu-id="feb91-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="feb91-109">`starting position`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="feb91-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="feb91-110">*Täisarvu* väärtus, mis määrab esimese märgi ametikoha, mis tuleb määratud tekstist tagastada.</span><span class="sxs-lookup"><span data-stu-id="feb91-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="feb91-111">`number of characters`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="feb91-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="feb91-112">*Täisarvu* väärtus, mis määrab märkide arvu, mis tuleb tagastada, alustades määratud lähtepositsioonist.</span><span class="sxs-lookup"><span data-stu-id="feb91-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="feb91-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="feb91-113">Return values</span></span>

<span data-ttu-id="feb91-114">*String*</span><span class="sxs-lookup"><span data-stu-id="feb91-114">*String*</span></span>

<span data-ttu-id="feb91-115">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="feb91-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="feb91-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="feb91-116">Usage notes</span></span>

<span data-ttu-id="feb91-117">Kui argumendi `starting position` väärtus on väiksem kui 0 (null), loendatakse tagastatavaid märke määratud stringi esimesest positsioonist.</span><span class="sxs-lookup"><span data-stu-id="feb91-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="feb91-118">Kui argumendi `starting position` väärtus ületab määratud stringi pikkust, tagastatakse tühi string.</span><span class="sxs-lookup"><span data-stu-id="feb91-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="feb91-119">Näide</span><span class="sxs-lookup"><span data-stu-id="feb91-119">Example</span></span>

<span data-ttu-id="feb91-120">`MID ("Sample", 2, 3)` tagastab **„amp”**.</span><span class="sxs-lookup"><span data-stu-id="feb91-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="feb91-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="feb91-121">Additional resources</span></span>

[<span data-ttu-id="feb91-122">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="feb91-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]