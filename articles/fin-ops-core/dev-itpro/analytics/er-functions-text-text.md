---
title: ER-i funktsioon TEXT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TEXT.
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
ms.openlocfilehash: 0694480f5d6892d13fe0c0d9ad191cdf2332dfec
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746095"
---
# <a name="text-er-function"></a><span data-ttu-id="6ce32-103">ER-i funktsioon TEXT</span><span class="sxs-lookup"><span data-stu-id="6ce32-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ce32-104">Funktsioon `TEXT` tagastab määratud arvu *stringi* väärtusena pärast seda, kui see on teisendatud tekstistringiks, mis on vormindatud praeguse rakenduse eksemplari serverilokaadi sätete kohaselt.</span><span class="sxs-lookup"><span data-stu-id="6ce32-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ce32-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6ce32-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="6ce32-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="6ce32-106">Arguments</span></span>

<span data-ttu-id="6ce32-107">`number`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="6ce32-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="6ce32-108">Number, mis tuleb teisendada tekstistringiks.</span><span class="sxs-lookup"><span data-stu-id="6ce32-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ce32-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6ce32-109">Return values</span></span>

<span data-ttu-id="6ce32-110">*String*</span><span class="sxs-lookup"><span data-stu-id="6ce32-110">*String*</span></span>

<span data-ttu-id="6ce32-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="6ce32-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6ce32-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="6ce32-112">Usage notes</span></span>

<span data-ttu-id="6ce32-113">Tüübi *Tõeline* väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.</span><span class="sxs-lookup"><span data-stu-id="6ce32-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="6ce32-114">Näide</span><span class="sxs-lookup"><span data-stu-id="6ce32-114">Example</span></span>

<span data-ttu-id="6ce32-115">Kui Microsoft Dynamics 365 Finance’i eksemplari serverilokaat on määratud kui **EN-US**, tagastab `TEXT (NOW ())` praeguse rakenduse Finance seansi kuupäeva 17. detsember 2015 tekstistringina **„12/17/2015 07:59:23 AM”**.</span><span class="sxs-lookup"><span data-stu-id="6ce32-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="6ce32-116">`TEXT (1/3)` tagastab **„0,33”**.</span><span class="sxs-lookup"><span data-stu-id="6ce32-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ce32-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6ce32-117">Additional resources</span></span>

[<span data-ttu-id="6ce32-118">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="6ce32-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]