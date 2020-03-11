---
title: ER-i funktsioon REPLACE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni REPLACE.
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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040982"
---
# <span data-ttu-id="88805-103"><a name="REPLACE">ER-i funktsioon REPLACE</a></span><span class="sxs-lookup"><span data-stu-id="88805-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88805-104">Funktsioon `REPLACE` tagastab määratud tekstistringi *stringi* väärtusena pärast seda, kui kõik või osa sellest on asendatud teise stringiga.</span><span class="sxs-lookup"><span data-stu-id="88805-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="88805-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="88805-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="88805-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="88805-106">Arguments</span></span>

<span data-ttu-id="88805-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="88805-107">`text`: *String*</span></span>

<span data-ttu-id="88805-108">Tüübi *String* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="88805-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="88805-109">`pattern`: *string*</span><span class="sxs-lookup"><span data-stu-id="88805-109">`pattern`: *String*</span></span>

<span data-ttu-id="88805-110">Kui argumendi `regular expression flag` tulem on **FALSE**, sisaldab see argument teksti, mis tuleb asendada.</span><span class="sxs-lookup"><span data-stu-id="88805-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="88805-111">Kui argumendi `regular expression flag` tulem on **TÕENE**, sisaldab see argument tavalist avaldist, mis määratleb nii otsingumustri kui ka asendusteksti.</span><span class="sxs-lookup"><span data-stu-id="88805-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="88805-112">`replacement`: *string*</span><span class="sxs-lookup"><span data-stu-id="88805-112">`replacement`: *String*</span></span>

<span data-ttu-id="88805-113">Kui argumendi `regular expression flag` tulem on **FALSE**, sisaldab see argument asendamiseks kasutatavat teksti.</span><span class="sxs-lookup"><span data-stu-id="88805-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="88805-114">Kui argumendi `regular expression flag` tulem on **TRUE**, siis seda argumenti ei kasutata.</span><span class="sxs-lookup"><span data-stu-id="88805-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="88805-115">`regular expression flag`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="88805-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="88805-116">*Kahendmuutuja* väärtus, mis näitab, kas asendamiseks kasutatakse tavalist avaldist.</span><span class="sxs-lookup"><span data-stu-id="88805-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="88805-117">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="88805-117">Return values</span></span>

<span data-ttu-id="88805-118">*String*</span><span class="sxs-lookup"><span data-stu-id="88805-118">*String*</span></span>

<span data-ttu-id="88805-119">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="88805-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="88805-120">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="88805-120">Usage notes</span></span>

<span data-ttu-id="88805-121">Kui argumendi `regular expression flag` tulem on **TRUE**, tagastab see funktsioon määratud stringi pärast selle muutmist, rakendades tavalise avaldise, mis on argumendiga `pattern` määratud.</span><span class="sxs-lookup"><span data-stu-id="88805-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="88805-122">Tavalist avaldist kasutatakse asendatavate tähemärkide otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="88805-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="88805-123">Kui argumendi `regular expression flag` tulem on **FALSE**, käitub see funktsioon sarnaselt funktsioonile [TRANSLATE](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="88805-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="88805-124">Argumendi `replacement` määratletud tähemärke kasutatakse leitud tähemärkide asendamiseks.</span><span class="sxs-lookup"><span data-stu-id="88805-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="88805-125">Näide 1</span><span class="sxs-lookup"><span data-stu-id="88805-125">Example 1</span></span>

<span data-ttu-id="88805-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` rakendab regulaaravaldist, mis eemaldab kõik mittearvulised sümbolid, ja see tagastab väärtuse **„19234564971”**.</span><span class="sxs-lookup"><span data-stu-id="88805-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="88805-127">Näide 2</span><span class="sxs-lookup"><span data-stu-id="88805-127">Example 2</span></span>

<span data-ttu-id="88805-128">`REPLACE ("abcdef", "cd", "GH", false)` asendab mustri **„cd”** stringiga **„GH”** ja tagastab väärtuse **„abGHef”**.</span><span class="sxs-lookup"><span data-stu-id="88805-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88805-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="88805-129">Additional resources</span></span>

[<span data-ttu-id="88805-130">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="88805-130">Text functions</span></span>](er-functions-category-text.md)
