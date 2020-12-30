---
title: ER-i funktsioon CASE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CASE
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69b76a06bcd3ba002d9543447e60afa14d5a6ce6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687022"
---
# <a name="case-er-function"></a><span data-ttu-id="576c6-103">ER-i funktsioon CASE</span><span class="sxs-lookup"><span data-stu-id="576c6-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="576c6-104">Funktsioon `CASE` arvutab määratud avaldise väärtuse määratud teise suvandi suhtes ja tagastab esimese suvandi tulemuse, mis on võrdne määratud avaldise väärtusega.</span><span class="sxs-lookup"><span data-stu-id="576c6-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="576c6-105">Vastasel juhul tagastab see valikulise vaikimisi tulemuse, kui vaikimisi tulemus on määratud kutsutud funktsiooni viimaseks argumendiks, millele ei eelne suvandit.</span><span class="sxs-lookup"><span data-stu-id="576c6-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="576c6-106">Tagastatav väärtus võib olla toetatud andmetüüpide mis tahes väärtus.</span><span class="sxs-lookup"><span data-stu-id="576c6-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="576c6-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="576c6-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="576c6-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="576c6-108">Arguments</span></span>

<span data-ttu-id="576c6-109">`expression`: *primitiivne andmetüüp* (kahendmuutuja, numbriline või tekst)</span><span class="sxs-lookup"><span data-stu-id="576c6-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="576c6-110">Kehtiv avaldis, mis tagastab primitiivse andmetüübi väärtuse.</span><span class="sxs-lookup"><span data-stu-id="576c6-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="576c6-111">`option 1`: *primitiivne andmetüüp* (kahendmuutuja, numbriline või tekst)</span><span class="sxs-lookup"><span data-stu-id="576c6-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="576c6-112">Kehtiv avaldis, mis tagastab sama primitiivse andmetüübi väärtuse kui kutsutud funktsiooni argument `expression`.</span><span class="sxs-lookup"><span data-stu-id="576c6-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="576c6-113">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="576c6-113">This argument is required.</span></span>

<span data-ttu-id="576c6-114">`result 1`: *mis tahes toetatud andmetüüp*</span><span class="sxs-lookup"><span data-stu-id="576c6-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="576c6-115">Tagastatav tulemus, mis vastab eelmisele valikule.</span><span class="sxs-lookup"><span data-stu-id="576c6-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="576c6-116">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="576c6-116">This argument is required.</span></span>

<span data-ttu-id="576c6-117">`option N`: *primitiivne andmetüüp* (kahendmuutuja, numbriline või tekst)</span><span class="sxs-lookup"><span data-stu-id="576c6-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="576c6-118">Kehtiv avaldis, mis tagastab sama primitiivse andmetüübi väärtuse kui kutsutud funktsiooni argument `expression`.</span><span class="sxs-lookup"><span data-stu-id="576c6-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="576c6-119">See argunent on valikuline.</span><span class="sxs-lookup"><span data-stu-id="576c6-119">This argument is optional.</span></span>

<span data-ttu-id="576c6-120">`result N`: *mis tahes toetatud andmetüüp*</span><span class="sxs-lookup"><span data-stu-id="576c6-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="576c6-121">Tagastatav tulemus, mis vastab eelmisele valikule.</span><span class="sxs-lookup"><span data-stu-id="576c6-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="576c6-122">See argunent on valikuline.</span><span class="sxs-lookup"><span data-stu-id="576c6-122">This argument is optional.</span></span>

<span data-ttu-id="576c6-123">`default result`: *mis tahes toetatud andmetüüp*</span><span class="sxs-lookup"><span data-stu-id="576c6-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="576c6-124">Tulemus, mis tuleks tagastada, kui vastet pole.</span><span class="sxs-lookup"><span data-stu-id="576c6-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="576c6-125">See argunent on valikuline.</span><span class="sxs-lookup"><span data-stu-id="576c6-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="576c6-126">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="576c6-126">Return values</span></span>

<span data-ttu-id="576c6-127">*Mis tahes toetatud andmetüüp*</span><span class="sxs-lookup"><span data-stu-id="576c6-127">*Any of the supported data types*</span></span>

<span data-ttu-id="576c6-128">Mis tahes toetatud andmetüübi tulemuseks olev väärtus.</span><span class="sxs-lookup"><span data-stu-id="576c6-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="576c6-129">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="576c6-129">Usage notes</span></span>

<span data-ttu-id="576c6-130">Käitusajal esitatakse erand, kui puudub vaste ja valikuline vaikimisi tulemus pole määratletud.</span><span class="sxs-lookup"><span data-stu-id="576c6-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="576c6-131">Kõik tulemused tuleb määrata sama andmetüüpi kasutades.</span><span class="sxs-lookup"><span data-stu-id="576c6-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="576c6-132">Kujundamise ajal esitatakse erand, kui konfigureeritud tulemuste andmetüübid ei ühti.</span><span class="sxs-lookup"><span data-stu-id="576c6-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="576c6-133">Kui esimese tulemuse väärtus ja *N*. tulemuse väärtus on andmetüübi *Konteiner (kirje)* või *Kirjete loend* väärtused, on tulemuses ainult väljad, mis eksisteerivad mõlemas väärtuses.</span><span class="sxs-lookup"><span data-stu-id="576c6-133">If the first result value and the *N* th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="576c6-134">Näide</span><span class="sxs-lookup"><span data-stu-id="576c6-134">Example</span></span>

<span data-ttu-id="576c6-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` tagastab stringi **„WINTER”**, kui praeguse rakenduse seansi kuupäev jääb vahemikku oktoober kuni detsember.</span><span class="sxs-lookup"><span data-stu-id="576c6-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="576c6-136">Muidu tagastatakse tühi string.</span><span class="sxs-lookup"><span data-stu-id="576c6-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="576c6-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="576c6-137">Additional resources</span></span>

[<span data-ttu-id="576c6-138">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="576c6-138">Logical functions</span></span>](er-functions-category-logical.md)
