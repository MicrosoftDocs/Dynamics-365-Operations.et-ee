---
title: ER-i funktsioon SPLIT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLIT.
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
ms.openlocfilehash: c171509353fed92b14ca0d7473742e4a9a54bad1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745269"
---
# <a name="split-er-function"></a><span data-ttu-id="4f378-103">ER-i funktsioon SPLIT</span><span class="sxs-lookup"><span data-stu-id="4f378-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f378-104">Funktsioon `SPLIT` tükeldab määratud sisendstringid alamstringideks ja tagastab tulemuse uue *kirjete loendi* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="4f378-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4f378-105">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="4f378-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="4f378-106">Seda süntakstit kasutatakse määratud sisendstringi jaotamiseks alamstringideks, millest igaühel on määratud pikkus.</span><span class="sxs-lookup"><span data-stu-id="4f378-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="4f378-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="4f378-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="4f378-108">Seda süntaksit kasutatakse määratud sisendstringi jaotamiseks määratletud eraldaja põhjal alamstringideks.</span><span class="sxs-lookup"><span data-stu-id="4f378-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="4f378-109">Argumendid</span><span class="sxs-lookup"><span data-stu-id="4f378-109">Arguments</span></span>

<span data-ttu-id="4f378-110">`input`: *string*</span><span class="sxs-lookup"><span data-stu-id="4f378-110">`input`: *String*</span></span>

<span data-ttu-id="4f378-111">Jaotatav tekst.</span><span class="sxs-lookup"><span data-stu-id="4f378-111">The text to split.</span></span>

<span data-ttu-id="4f378-112">`length`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="4f378-112">`length`: *Integer*</span></span>

<span data-ttu-id="4f378-113">Ühe alamstringi maksimaalne pikkus.</span><span class="sxs-lookup"><span data-stu-id="4f378-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="4f378-114">`delimiter`: *string*</span><span class="sxs-lookup"><span data-stu-id="4f378-114">`delimiter`: *String*</span></span>

<span data-ttu-id="4f378-115">Eraldaja, mida kasutatakse alamstringide eraldamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f378-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="4f378-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="4f378-116">Return values</span></span>

<span data-ttu-id="4f378-117">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="4f378-117">*Record list*</span></span>

<span data-ttu-id="4f378-118">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="4f378-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4f378-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="4f378-119">Usage notes</span></span>

<span data-ttu-id="4f378-120">Tagastatava loendi kirjete struktuur koosneb tüübi *String* väljast **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="4f378-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="4f378-121">Iga tagastatava loendi kirje sisaldab selle välja loodud alamstringe</span><span class="sxs-lookup"><span data-stu-id="4f378-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="4f378-122">Kui argument `delimiter` on tühi, koosneb uus loend, mis tagastati, ühest kirjest, millel on tüübi *String* väli **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="4f378-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="4f378-123">See väli sisaldab sisestusteksti.</span><span class="sxs-lookup"><span data-stu-id="4f378-123">This field contains the input text.</span></span>

<span data-ttu-id="4f378-124">Kui argument `input` on tühi, tagastatakse uus tühi loend.</span><span class="sxs-lookup"><span data-stu-id="4f378-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="4f378-125">Kui argument `input` või `delimiter` on määratlemata (null), ilmneb rakenduse erand.</span><span class="sxs-lookup"><span data-stu-id="4f378-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="4f378-126">Näide 1</span><span class="sxs-lookup"><span data-stu-id="4f378-126">Example 1</span></span>

<span data-ttu-id="4f378-127">`SPLIT ("abcd", 3)` tagastab uue loendi, mis koosneb kahest kirjest, millel on tüübi *String* väli **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="4f378-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="4f378-128">Esimese kirje väli **Väärtus** sisaldab teksti **„abc”** ja teise kirje väli **Väärtus** sisaldab teksti **„d”** </span><span class="sxs-lookup"><span data-stu-id="4f378-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4f378-129">Näide 2</span><span class="sxs-lookup"><span data-stu-id="4f378-129">Example 2</span></span>

<span data-ttu-id="4f378-130">`SPLIT ("XAb aBy", "aB")` tagastab uue loendi, mis koosneb kolmest kirjest, millel on tüübi *String* väli **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="4f378-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="4f378-131">Esimese kirje väli **Väärtus** sisaldab teskti **„X”**, välja **Väärtus** teisene kirje sisaldab teksti **„&nbsp;”** ja kolmanda kirje väli **Väärtus** sisaldab teksti **„y”**.</span><span class="sxs-lookup"><span data-stu-id="4f378-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4f378-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4f378-132">Additional resources</span></span>

[<span data-ttu-id="4f378-133">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="4f378-133">List functions</span></span>](er-functions-category-list.md)
