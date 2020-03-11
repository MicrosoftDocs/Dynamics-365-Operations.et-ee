---
title: ER-i funktsioon TEXT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TEXT.
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
ms.openlocfilehash: c08aca949ffc7e62009bf3f6c664d96b368f43e7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040890"
---
# <span data-ttu-id="f6bfa-103"><a name="TEXT">ER-i funktsioon TEXT</a></span><span class="sxs-lookup"><span data-stu-id="f6bfa-103"><a name="TEXT">TEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6bfa-104">Funktsioon `TEXT` tagastab määratud arvu *stringi* väärtusena pärast seda, kui see on teisendatud tekstistringiks, mis on vormindatud praeguse rakenduse eksemplari serverilokaadi sätete kohaselt.</span><span class="sxs-lookup"><span data-stu-id="f6bfa-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6bfa-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="f6bfa-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="f6bfa-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="f6bfa-106">Arguments</span></span>

<span data-ttu-id="f6bfa-107">`number`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="f6bfa-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="f6bfa-108">Number, mis tuleb teisendada tekstistringiks.</span><span class="sxs-lookup"><span data-stu-id="f6bfa-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="f6bfa-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="f6bfa-109">Return values</span></span>

<span data-ttu-id="f6bfa-110">*String*</span><span class="sxs-lookup"><span data-stu-id="f6bfa-110">*String*</span></span>

<span data-ttu-id="f6bfa-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="f6bfa-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f6bfa-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="f6bfa-112">Usage notes</span></span>

<span data-ttu-id="f6bfa-113">Tüübi *Tõeline* väärtuste puhul on stringi teisendamine piiratud kahe kümnendkohaga.</span><span class="sxs-lookup"><span data-stu-id="f6bfa-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="f6bfa-114">Näide</span><span class="sxs-lookup"><span data-stu-id="f6bfa-114">Example</span></span>

<span data-ttu-id="f6bfa-115">Kui Microsoft Dynamics 365 Finance’i eksemplari serverilokaat on määratud kui **EN-US**, tagastab `TEXT (NOW ())` praeguse rakenduse Finance seansi kuupäeva 17. detsember 2015 tekstistringina **„12/17/2015 07:59:23 AM”**.</span><span class="sxs-lookup"><span data-stu-id="f6bfa-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="f6bfa-116">`TEXT (1/3)` tagastab **„0,33”**.</span><span class="sxs-lookup"><span data-stu-id="f6bfa-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6bfa-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f6bfa-117">Additional resources</span></span>

[<span data-ttu-id="f6bfa-118">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="f6bfa-118">Text functions</span></span>](er-functions-category-text.md)
