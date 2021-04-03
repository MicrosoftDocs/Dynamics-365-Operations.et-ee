---
title: ER-i funktsioon ISVALIDCHARACTERISO7064
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ISVALIDCHARACTERISO7064.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563362"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="b4031-103">ER-i funktsioon ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="b4031-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4031-104">Funktsioon `ISVALIDCHARACTERISO7064` tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud string tähistab kehtivat rahvusvahelist pangakonto numbrit (IBAN).</span><span class="sxs-lookup"><span data-stu-id="b4031-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="b4031-105">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="b4031-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4031-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="b4031-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="b4031-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="b4031-107">Arguments</span></span>

<span data-ttu-id="b4031-108">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="b4031-108">`text`: *String*</span></span>

<span data-ttu-id="b4031-109">IBAN-i tähistav teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="b4031-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="b4031-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="b4031-110">Return values</span></span>

<span data-ttu-id="b4031-111">*String*</span><span class="sxs-lookup"><span data-stu-id="b4031-111">*String*</span></span>

<span data-ttu-id="b4031-112">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="b4031-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b4031-113">Näide</span><span class="sxs-lookup"><span data-stu-id="b4031-113">Example</span></span>

<span data-ttu-id="b4031-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` tagastab väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b4031-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="b4031-115">`ISVALIDCHARACTERISO7064 ("AT61")` tagastab väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b4031-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4031-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b4031-116">Additional resources</span></span>

[<span data-ttu-id="b4031-117">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="b4031-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]