---
title: ER-i funktsioon SESSIONTODAY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SESSIONTODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042257"
---
# <span data-ttu-id="19070-103"><a name="SESSIONTODAY">ER-i funktsioon SESSIONTODAY</a></span><span class="sxs-lookup"><span data-stu-id="19070-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19070-104">Funktsioon `SESSIONTODAY` tagastab *kuupäeva* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="19070-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="19070-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="19070-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="19070-106">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="19070-106">Return values</span></span>

<span data-ttu-id="19070-107">*Kuupäev*</span><span class="sxs-lookup"><span data-stu-id="19070-107">*Date*</span></span>

<span data-ttu-id="19070-108">Tulemiks saadud kuupäeva väärtus.</span><span class="sxs-lookup"><span data-stu-id="19070-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="19070-109">Näide</span><span class="sxs-lookup"><span data-stu-id="19070-109">Example</span></span>

<span data-ttu-id="19070-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva 24. detsember 2015 stringina **„24-12-2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="19070-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19070-111">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="19070-111">Additional resources</span></span>

[<span data-ttu-id="19070-112">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="19070-112">Date and time functions</span></span>](er-functions-category-datetime.md)
