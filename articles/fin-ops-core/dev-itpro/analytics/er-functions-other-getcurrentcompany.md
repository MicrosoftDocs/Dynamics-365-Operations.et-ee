---
title: ER-i funktsioon GETCURRENTCOMPANY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni GETCURRENTCOMPANY.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e14c6a8aaff0a32a115117938d0e853bb34bb14
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684855"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="c3fa5-103">ER-i funktsioon GETCURRENTCOMPANY</span><span class="sxs-lookup"><span data-stu-id="c3fa5-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3fa5-104">Funktsioon `GETCURRENTCOMPANY` tagastab *stringi* väärtuse, mis tähistab juriidilise isiku (ettevõtte) koodi, kuhu kasutaja on praegu sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3fa5-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="c3fa5-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="c3fa5-106">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="c3fa5-106">Return values</span></span>

<span data-ttu-id="c3fa5-107">*String*</span><span class="sxs-lookup"><span data-stu-id="c3fa5-107">*String*</span></span>

<span data-ttu-id="c3fa5-108">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c3fa5-109">Näide</span><span class="sxs-lookup"><span data-stu-id="c3fa5-109">Example</span></span>

<span data-ttu-id="c3fa5-110">`GETCURRENTCOMPANY ()` tagastab **USMF**-i kasutaja puhul, kes on logitud sisse ettevõttesse **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="c3fa5-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3fa5-111">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c3fa5-111">Additional resources</span></span>

[<span data-ttu-id="c3fa5-112">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="c3fa5-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
