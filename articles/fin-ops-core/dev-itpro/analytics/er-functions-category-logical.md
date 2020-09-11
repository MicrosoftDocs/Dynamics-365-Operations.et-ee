---
title: ER-i funktsioonide loend loogilises kategoorias
description: See teema annab teavet loogiliste funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705091"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="83cec-103">ER-i funktsioonide loend loogilises kategoorias</span><span class="sxs-lookup"><span data-stu-id="83cec-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83cec-104">Elektroonilise aruandluse (ER) loogilisi funktsioone saab kasutada loogiliste väärtustega töötamiseks, et teostada rohkem kui ühe võrdluse ühe avaldisega või mitme tingimuse testimiseks.</span><span class="sxs-lookup"><span data-stu-id="83cec-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="83cec-105">See teema sisaldab järgmiste funktsioonide kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="83cec-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="83cec-106">Toetatud funktsioonide loend</span><span class="sxs-lookup"><span data-stu-id="83cec-106">List of supported functions</span></span>

| <span data-ttu-id="83cec-107">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="83cec-107">Function</span></span> | <span data-ttu-id="83cec-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="83cec-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="83cec-109">Ja</span><span class="sxs-lookup"><span data-stu-id="83cec-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="83cec-110">Kui kõik määratud tingimused on tõesed, tagastab see funktsioon *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="83cec-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="83cec-111">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="83cec-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="83cec-112">Kast</span><span class="sxs-lookup"><span data-stu-id="83cec-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="83cec-113">See funktsioon arvutab määratud avaldise väärtuse määratud teise suvandi suhtes ja tagastab esimese suvandi tulemuse, mis on võrdne määratud avaldise väärtusega.</span><span class="sxs-lookup"><span data-stu-id="83cec-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="83cec-114">Vastasel juhul tagastab see valikulise vaikimisi tulemuse, kui vaikimisi tulemus on määratud kutsutud funktsiooni viimaseks argumendiks, millele ei eelne suvandit.</span><span class="sxs-lookup"><span data-stu-id="83cec-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="83cec-115">Tagastatav väärtus võib olla toetatud andmetüüpide mis tahes väärtus.</span><span class="sxs-lookup"><span data-stu-id="83cec-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="83cec-116">Kui</span><span class="sxs-lookup"><span data-stu-id="83cec-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="83cec-117">See funktsioon annab vastuseks esimese määratud väärtuse, kui määratud tingimus on täidetud.</span><span class="sxs-lookup"><span data-stu-id="83cec-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="83cec-118">Muul juhul annab see vastuseks teise määratud väärtuse.</span><span class="sxs-lookup"><span data-stu-id="83cec-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="83cec-119">Tagastatav väärtus võib olla toetatud andmetüüpide mis tahes väärtus.</span><span class="sxs-lookup"><span data-stu-id="83cec-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="83cec-120">Ei ole</span><span class="sxs-lookup"><span data-stu-id="83cec-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="83cec-121">See funktsioon annab määratud tingimuse pööratud loogilise väärtuse *kahendmuutuja* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="83cec-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="83cec-122">Or</span><span class="sxs-lookup"><span data-stu-id="83cec-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="83cec-123">Kui kõik määratud tingimused on väärad, tagastab see funktsioon *kahendmuutuja* väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="83cec-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="83cec-124">Kui mõni määratud tingimustest on tõene, tagastab funktsioon *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="83cec-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="83cec-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="83cec-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="83cec-126">See funktsioon määratleb, kas määratud sisend vastab määratud loendis määratud üksuse mis tahes väärtusele.</span><span class="sxs-lookup"><span data-stu-id="83cec-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="83cec-127">See tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul.</span><span class="sxs-lookup"><span data-stu-id="83cec-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="83cec-128">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="83cec-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="83cec-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="83cec-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="83cec-130">See funktsioon määratleb, kas määratud *Int64* või *Täisarv*-tüüpi sisend vastab määratud loendis määratud üksuse mis tahes väärtusele.</span><span class="sxs-lookup"><span data-stu-id="83cec-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="83cec-131">See tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud sisestus ühtib määratud avaldise käivitamise tulemusega vähemalt ühe määratud loendi kirje puhul.</span><span class="sxs-lookup"><span data-stu-id="83cec-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="83cec-132">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="83cec-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="83cec-133">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="83cec-133">Additional resources</span></span>

[<span data-ttu-id="83cec-134">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="83cec-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="83cec-135">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="83cec-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="83cec-136">Elektroonilise aruandluse valemi keel</span><span class="sxs-lookup"><span data-stu-id="83cec-136">Electronic reporting formula language</span></span>](er-formula-language.md)
