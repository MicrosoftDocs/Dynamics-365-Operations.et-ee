---
title: ER-i funktsioon CHAR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CHAR.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a621328817171be7df0622507c84f5c6f6fe90a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746431"
---
# <a name="char-er-function"></a><span data-ttu-id="4b706-103">ER-i funktsioon CHAR</span><span class="sxs-lookup"><span data-stu-id="4b706-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b706-104">Funktsioon `CHAR` tagastab *stringi* väärtuse, mis kujutab üksikut märki, millele viitab määratud Unicode’i number.</span><span class="sxs-lookup"><span data-stu-id="4b706-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b706-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="4b706-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="4b706-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="4b706-106">Arguments</span></span>

<span data-ttu-id="4b706-107">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="4b706-107">`number`: *Integer*</span></span>

<span data-ttu-id="4b706-108">Arv, mis vastab eeldatavale üksikule märgile.</span><span class="sxs-lookup"><span data-stu-id="4b706-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="4b706-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="4b706-109">Return values</span></span>

<span data-ttu-id="4b706-110">*String*</span><span class="sxs-lookup"><span data-stu-id="4b706-110">*String*</span></span>

<span data-ttu-id="4b706-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="4b706-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4b706-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="4b706-112">Usage notes</span></span>

<span data-ttu-id="4b706-113">Selle funktsiooni tagastatud string sõltub vormingu **FILE** ülemelemendis valitud kodeeringust.</span><span class="sxs-lookup"><span data-stu-id="4b706-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="4b706-114">Toetatud kodeeringute loendi leiate teemast [Kodeeringuklass](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="4b706-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="4b706-115">Näide</span><span class="sxs-lookup"><span data-stu-id="4b706-115">Example</span></span>

<span data-ttu-id="4b706-116">`CHAR (255)` tagastab **„ÿ”**.</span><span class="sxs-lookup"><span data-stu-id="4b706-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b706-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4b706-117">Additional resources</span></span>

[<span data-ttu-id="4b706-118">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="4b706-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]