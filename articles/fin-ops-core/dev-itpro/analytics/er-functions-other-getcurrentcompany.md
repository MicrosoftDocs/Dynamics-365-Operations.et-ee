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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d91caff1a1b89e060a16833e53f3647208ed3826
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041419"
---
# <span data-ttu-id="d0b5f-103"><a name="GETCURRENTCOMPANY">ER-i funktsioon GETCURRENTCOMPANY</a></span><span class="sxs-lookup"><span data-stu-id="d0b5f-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0b5f-104">Funktsioon `GETCURRENTCOMPANY` tagastab *stringi* väärtuse, mis tähistab juriidilise isiku (ettevõtte) koodi, kuhu kasutaja on praegu sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="d0b5f-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b5f-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="d0b5f-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="d0b5f-106">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="d0b5f-106">Return values</span></span>

<span data-ttu-id="d0b5f-107">*String*</span><span class="sxs-lookup"><span data-stu-id="d0b5f-107">*String*</span></span>

<span data-ttu-id="d0b5f-108">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="d0b5f-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d0b5f-109">Näide</span><span class="sxs-lookup"><span data-stu-id="d0b5f-109">Example</span></span>

<span data-ttu-id="d0b5f-110">`GETCURRENTCOMPANY ()` tagastab **USMF**-i kasutaja puhul, kes on logitud sisse ettevõttesse **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="d0b5f-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0b5f-111">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d0b5f-111">Additional resources</span></span>

[<span data-ttu-id="d0b5f-112">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="d0b5f-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
