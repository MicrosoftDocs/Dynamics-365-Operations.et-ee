---
title: ER-i funktsioon LISTJOIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249031"
---
# <a name=""></a><span data-ttu-id="3e359-103"><a name="LISTJOIN">ER-i funktsioon LISTJOIN</a></span><span class="sxs-lookup"><span data-stu-id="3e359-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e359-104">`LISTJOIN` funktsioon tagastab *kirjete loendi* väärtuse, mis tähistab määratud argumentidest loodud uut ühendatud kirjete loendit.</span><span class="sxs-lookup"><span data-stu-id="3e359-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e359-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="3e359-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="3e359-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="3e359-106">Arguments</span></span>

<span data-ttu-id="3e359-107">`list 1`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="3e359-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="3e359-108">Viide andmetüübi *Kirjete loend* andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="3e359-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="3e359-109">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="3e359-109">This argument is mandatory.</span></span>

<span data-ttu-id="3e359-110">`list N`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="3e359-110">`list N`: *Record list*</span></span>

<span data-ttu-id="3e359-111">Viide andmetüübi *Kirjete loend* andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="3e359-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="3e359-112">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="3e359-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="3e359-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="3e359-113">Return values</span></span>

<span data-ttu-id="3e359-114">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="3e359-114">*Record list*</span></span>

<span data-ttu-id="3e359-115">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="3e359-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3e359-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="3e359-116">Usage notes</span></span>

<span data-ttu-id="3e359-117">Loodud loendi struktuur sisaldab ainult neid välju, mis on esitatud argumentides mainitud iga kirjete loendi struktuuris.</span><span class="sxs-lookup"><span data-stu-id="3e359-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="3e359-118">Näide</span><span class="sxs-lookup"><span data-stu-id="3e359-118">Example</span></span>

<span data-ttu-id="3e359-119">Sisestate tüübi `Container` andmeallika **Kirje 1**.</span><span class="sxs-lookup"><span data-stu-id="3e359-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="3e359-120">See andmeallikas sisaldab tüübi `Calculated field` järgmisi pesastatud välju:</span><span class="sxs-lookup"><span data-stu-id="3e359-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="3e359-121">**Kood**: see väli sisaldab avaldist, mis tagastab tüübi `String` väärtuse.</span><span class="sxs-lookup"><span data-stu-id="3e359-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="3e359-122">**Summa**: see väli sisaldab avaldist, mis tagastab tüübi `Real` väärtuse.</span><span class="sxs-lookup"><span data-stu-id="3e359-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="3e359-123">Seejärel sisestate tüübi `Container` andmeallika **Kirje 2**.</span><span class="sxs-lookup"><span data-stu-id="3e359-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="3e359-124">See andmeallikas sisaldab tüübi `Calculated field` järgmisi pesastatud välju:</span><span class="sxs-lookup"><span data-stu-id="3e359-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="3e359-125">**Summa**: see väli sisaldab avaldist, mis tagastab tüübi `Real` väärtuse.</span><span class="sxs-lookup"><span data-stu-id="3e359-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="3e359-126">**IsValid**: see väli sisaldab avaldist, mis tagastab tüübi `Boolean` väärtuse.</span><span class="sxs-lookup"><span data-stu-id="3e359-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="3e359-127">Sel juhul tagastab avaldis `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` uue loendi, mis sisaldab kaht kirjet.</span><span class="sxs-lookup"><span data-stu-id="3e359-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="3e359-128">Selle loendi struktuur koosneb ühest tüübi `Real` väljast **Summa**, kuna see väli on ainuke väli, mis on esitatud kutsutud funktsiooni igas argumendis.</span><span class="sxs-lookup"><span data-stu-id="3e359-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e359-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3e359-129">Additional resources</span></span>

[<span data-ttu-id="3e359-130">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="3e359-130">List functions</span></span>](er-functions-category-list.md)
