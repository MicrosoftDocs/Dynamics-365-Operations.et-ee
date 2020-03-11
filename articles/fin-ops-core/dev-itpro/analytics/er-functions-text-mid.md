---
title: ER-i funktsioon MID
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni MID.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 6fbaf5952222d90a855956fb93713e0f9ef81305
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041024"
---
# <span data-ttu-id="67e72-103"><a name="MID">ER-i funktsioon MID</a></span><span class="sxs-lookup"><span data-stu-id="67e72-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67e72-104">Funktsioon `MID` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringist, alustades määratud kohast.</span><span class="sxs-lookup"><span data-stu-id="67e72-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="67e72-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="67e72-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="67e72-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="67e72-106">Arguments</span></span>

<span data-ttu-id="67e72-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="67e72-107">`text`: *String*</span></span>

<span data-ttu-id="67e72-108">*Stringi* väärtus, mis määrab teksti, millest märke tagastada.</span><span class="sxs-lookup"><span data-stu-id="67e72-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="67e72-109">`starting position`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="67e72-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="67e72-110">*Täisarvu* väärtus, mis määrab esimese märgi ametikoha, mis tuleb määratud tekstist tagastada.</span><span class="sxs-lookup"><span data-stu-id="67e72-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="67e72-111">`number of characters`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="67e72-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="67e72-112">*Täisarvu* väärtus, mis määrab märkide arvu, mis tuleb tagastada, alustades määratud lähtepositsioonist.</span><span class="sxs-lookup"><span data-stu-id="67e72-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="67e72-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="67e72-113">Return values</span></span>

<span data-ttu-id="67e72-114">*String*</span><span class="sxs-lookup"><span data-stu-id="67e72-114">*String*</span></span>

<span data-ttu-id="67e72-115">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="67e72-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="67e72-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="67e72-116">Usage notes</span></span>

<span data-ttu-id="67e72-117">Kui argumendi `starting position` väärtus on väiksem kui 0 (null), loendatakse tagastatavaid märke määratud stringi esimesest positsioonist.</span><span class="sxs-lookup"><span data-stu-id="67e72-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="67e72-118">Kui argumendi `starting position` väärtus ületab määratud stringi pikkust, tagastatakse tühi string.</span><span class="sxs-lookup"><span data-stu-id="67e72-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="67e72-119">Näide</span><span class="sxs-lookup"><span data-stu-id="67e72-119">Example</span></span>

<span data-ttu-id="67e72-120">`MID ("Sample", 2, 3)` tagastab **„amp”**.</span><span class="sxs-lookup"><span data-stu-id="67e72-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67e72-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="67e72-121">Additional resources</span></span>

[<span data-ttu-id="67e72-122">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="67e72-122">Text functions</span></span>](er-functions-category-text.md)
