---
title: ER-i funktsioon IF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni IF.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686998"
---
# <a name="if-er-function"></a><span data-ttu-id="f6c70-103">ER-i funktsioon IF</span><span class="sxs-lookup"><span data-stu-id="f6c70-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6c70-104">Funktsioon `IF` annab vastuseks esimese määratud väärtuse, kui määratud tingimus on täidetud.</span><span class="sxs-lookup"><span data-stu-id="f6c70-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="f6c70-105">Muul juhul annab see vastuseks teise määratud väärtuse.</span><span class="sxs-lookup"><span data-stu-id="f6c70-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="f6c70-106">Tagastatav väärtus võib olla toetatud andmetüüpide mis tahes väärtus.</span><span class="sxs-lookup"><span data-stu-id="f6c70-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c70-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="f6c70-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="f6c70-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="f6c70-108">Arguments</span></span>

<span data-ttu-id="f6c70-109">`condition`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="f6c70-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="f6c70-110">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="f6c70-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="f6c70-111">`first value`: *mis tahes toetatud andmetüüp*</span><span class="sxs-lookup"><span data-stu-id="f6c70-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="f6c70-112">Tagastatav tulemus, kui tingimus on täidetud.</span><span class="sxs-lookup"><span data-stu-id="f6c70-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="f6c70-113">`second value`: *mis tahes toetatud andmetüüp*</span><span class="sxs-lookup"><span data-stu-id="f6c70-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="f6c70-114">Tagastatav tulemus, kui tingimus ei ole täidetud.</span><span class="sxs-lookup"><span data-stu-id="f6c70-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="f6c70-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="f6c70-115">Return values</span></span>

<span data-ttu-id="f6c70-116">*Mis tahes toetatud andmetüüp*</span><span class="sxs-lookup"><span data-stu-id="f6c70-116">*Any of the supported data types*</span></span>

<span data-ttu-id="f6c70-117">Mis tahes toetatud andmetüübi tulemuseks olev väärtus.</span><span class="sxs-lookup"><span data-stu-id="f6c70-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f6c70-118">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="f6c70-118">Usage notes</span></span>

<span data-ttu-id="f6c70-119">Argumendid `first value` ja `second value` tuleb määrata sama andmetüüpi kasutades.</span><span class="sxs-lookup"><span data-stu-id="f6c70-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="f6c70-120">Kujundamise ajal esitatakse erand, kui konfigureeritud väärtuste andmetüübid ei ühti.</span><span class="sxs-lookup"><span data-stu-id="f6c70-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="f6c70-121">Kui esimene väärtus ja teine vöörtus on andmetüübi *Konteiner (kirje)* või *Kirjete loend* väärtused, on tulemuses ainult väljad, mis eksisteerivad mõlemas väärtuses.</span><span class="sxs-lookup"><span data-stu-id="f6c70-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="f6c70-122">Näide</span><span class="sxs-lookup"><span data-stu-id="f6c70-122">Example</span></span>

<span data-ttu-id="f6c70-123">`IF (1=2, "condition is met", "condition is not met")` tagastab stringi **„tingimus ei ole täidetud”**.</span><span class="sxs-lookup"><span data-stu-id="f6c70-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6c70-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f6c70-124">Additional resources</span></span>

[<span data-ttu-id="f6c70-125">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="f6c70-125">Logical functions</span></span>](er-functions-category-logical.md)
