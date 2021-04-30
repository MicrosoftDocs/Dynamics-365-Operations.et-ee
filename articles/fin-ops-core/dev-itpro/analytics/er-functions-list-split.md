---
title: ER-i funktsioon SPLIT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLIT.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853439"
---
# <a name="split-er-function"></a><span data-ttu-id="fa0c1-103">ER-i funktsioon SPLIT</span><span class="sxs-lookup"><span data-stu-id="fa0c1-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa0c1-104">Funktsioon `SPLIT` tükeldab määratud sisendstringid alamstringideks ja tagastab tulemuse uue *kirjete loendi* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="fa0c1-105">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="fa0c1-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="fa0c1-106">Seda süntakstit kasutatakse määratud sisendstringi jaotamiseks alamstringideks, millest igaühel on määratud pikkus.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="fa0c1-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="fa0c1-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="fa0c1-108">Seda süntaksit kasutatakse määratud sisendstringi jaotamiseks määratletud eraldaja põhjal alamstringideks.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="fa0c1-109">Argumendid</span><span class="sxs-lookup"><span data-stu-id="fa0c1-109">Arguments</span></span>

<span data-ttu-id="fa0c1-110">`input`: *string*</span><span class="sxs-lookup"><span data-stu-id="fa0c1-110">`input`: *String*</span></span>

<span data-ttu-id="fa0c1-111">Jaotatav tekst.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-111">The text to split.</span></span>

<span data-ttu-id="fa0c1-112">`length`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="fa0c1-112">`length`: *Integer*</span></span>

<span data-ttu-id="fa0c1-113">Ühe alamstringi maksimaalne pikkus.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="fa0c1-114">`delimiter`: *string*</span><span class="sxs-lookup"><span data-stu-id="fa0c1-114">`delimiter`: *String*</span></span>

<span data-ttu-id="fa0c1-115">Eraldaja, mida kasutatakse alamstringide eraldamiseks.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="fa0c1-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="fa0c1-116">Return values</span></span>

<span data-ttu-id="fa0c1-117">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="fa0c1-117">*Record list*</span></span>

<span data-ttu-id="fa0c1-118">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fa0c1-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="fa0c1-119">Usage notes</span></span>

<span data-ttu-id="fa0c1-120">Tagastatava loendi kirjete struktuur koosneb tüübi *String* väljast **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="fa0c1-121">Iga tagastatava loendi kirje sisaldab selle välja loodud alamstringe</span><span class="sxs-lookup"><span data-stu-id="fa0c1-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="fa0c1-122">Kui argument `delimiter` on tühi, koosneb uus loend, mis tagastati, ühest kirjest, millel on tüübi *String* väli **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="fa0c1-123">See väli sisaldab sisestusteksti.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-123">This field contains the input text.</span></span>

<span data-ttu-id="fa0c1-124">Kui argument `input` on tühi, tagastatakse uus tühi loend.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="fa0c1-125">Kui argument `input` või `delimiter` on määratlemata (null), ilmneb rakenduse erand.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="fa0c1-126">Näide 1</span><span class="sxs-lookup"><span data-stu-id="fa0c1-126">Example 1</span></span>

<span data-ttu-id="fa0c1-127">`SPLIT ("abcd", 3)` tagastab uue loendi, mis koosneb kahest kirjest, millel on tüübi *String* väli **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="fa0c1-128">Esimese kirje väli **Väärtus** sisaldab teksti **„abc”** ja teise kirje väli **Väärtus** sisaldab teksti **„d”** </span><span class="sxs-lookup"><span data-stu-id="fa0c1-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fa0c1-129">Näide 2</span><span class="sxs-lookup"><span data-stu-id="fa0c1-129">Example 2</span></span>

<span data-ttu-id="fa0c1-130">`SPLIT ("XAb aBy", "aB")` tagastab uue loendi, mis koosneb kolmest kirjest, millel on tüübi *String* väli **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="fa0c1-131">Esimese kirje väli **Väärtus** sisaldab teskti **„X”**, välja **Väärtus** teisene kirje sisaldab teksti **„&nbsp;”** ja kolmanda kirje väli **Väärtus** sisaldab teksti **„y”**.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="fa0c1-132">Näide 3</span><span class="sxs-lookup"><span data-stu-id="fa0c1-132">Example 3</span></span>

<span data-ttu-id="fa0c1-133">Funktsiooni [INDEX](er-functions-list-index.md) abil pääsete juurde määratud sisendstringi üksikutele elementidele.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="fa0c1-134">Kui sisestate tüübi **Arvutatud väli** andmeallika **MyList** ja konfigureerida seda `SPLIT("abc", 1)` avaldisele, tagastab see `INDEX(MyList,2).Value` teksti väärtuse **„b”**.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="fa0c1-135">Näide 4</span><span class="sxs-lookup"><span data-stu-id="fa0c1-135">Example 4</span></span>

<span data-ttu-id="fa0c1-136">Funktsiooni [ENUMERATE](er-functions-list-enumerate.md) abil pääsete juurde määratud sisendstringi üksikutele elementidele.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="fa0c1-137">Kui sisestate esmalt tüübi **Arvutatud väli** andmeallika **MyList** ja konfigureerite selle `SPLIT("abc", 1)` avaldise ning seejärel sisestate tüübi **Arvutatud väli** andmetüübi **EnumeratedList** andmeallika ja konfigureerite selle `ENUMERATE(MyList)` avaldise, tagastab avaldis `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` teksti **„b”**.</span><span class="sxs-lookup"><span data-stu-id="fa0c1-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa0c1-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fa0c1-138">Additional resources</span></span>

[<span data-ttu-id="fa0c1-139">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="fa0c1-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
