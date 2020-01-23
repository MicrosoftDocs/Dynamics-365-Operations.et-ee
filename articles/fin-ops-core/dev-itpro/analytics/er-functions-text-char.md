---
title: ER-i funktsioon CHAR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CHAR.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915736"
---
# <span data-ttu-id="32507-103"><a name="CHAR">ER-i funktsioon CHAR</a></span><span class="sxs-lookup"><span data-stu-id="32507-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32507-104">Funktsioon `CHAR` tagastab *stringi* väärtuse, mis kujutab üksikut märki, millele viitab määratud Unicode’i number.</span><span class="sxs-lookup"><span data-stu-id="32507-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="32507-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="32507-105">Syntax</span></span>

```
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="32507-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="32507-106">Arguments</span></span>

<span data-ttu-id="32507-107">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="32507-107">`number`: *Integer*</span></span>

<span data-ttu-id="32507-108">Arv, mis vastab eeldatavale üksikule märgile.</span><span class="sxs-lookup"><span data-stu-id="32507-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="32507-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="32507-109">Return values</span></span>

<span data-ttu-id="32507-110">*String*</span><span class="sxs-lookup"><span data-stu-id="32507-110">*String*</span></span>

<span data-ttu-id="32507-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="32507-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="32507-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="32507-112">Usage notes</span></span>

<span data-ttu-id="32507-113">Selle funktsiooni tagastatud string sõltub vormingu **FILE** ülemelemendis valitud kodeeringust.</span><span class="sxs-lookup"><span data-stu-id="32507-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="32507-114">Toetatud kodeeringute loendi leiate teemast [Kodeeringuklass](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="32507-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="32507-115">Näide</span><span class="sxs-lookup"><span data-stu-id="32507-115">Example</span></span>

<span data-ttu-id="32507-116">`CHAR (255)` tagastab **„ÿ”**.</span><span class="sxs-lookup"><span data-stu-id="32507-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32507-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="32507-117">Additional resources</span></span>

[<span data-ttu-id="32507-118">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="32507-118">Text functions</span></span>](er-functions-category-text.md)
