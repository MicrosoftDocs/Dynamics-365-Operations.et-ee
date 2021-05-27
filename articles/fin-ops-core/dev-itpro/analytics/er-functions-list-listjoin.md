---
title: ER-i funktsioon LISTJOIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LISTJOIN.
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b300cef0a508f7cc37397480738091158efdead
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027911"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="2bf43-103">ER-i funktsioon LISTJOIN</span><span class="sxs-lookup"><span data-stu-id="2bf43-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bf43-104">`LISTJOIN` funktsioon tagastab *kirjete loendi* väärtuse, mis tähistab määratud argumentidest loodud uut ühendatud kirjete loendit.</span><span class="sxs-lookup"><span data-stu-id="2bf43-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf43-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="2bf43-105">Syntax</span></span>

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="2bf43-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="2bf43-106">Arguments</span></span>

<span data-ttu-id="2bf43-107">`list 1`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="2bf43-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="2bf43-108">Viide andmetüübi *Kirjete loend* andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="2bf43-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="2bf43-109">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="2bf43-109">This argument is mandatory.</span></span>

<span data-ttu-id="2bf43-110">`list N`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="2bf43-110">`list N`: *Record list*</span></span>

<span data-ttu-id="2bf43-111">Viide andmetüübi *Kirjete loend* andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="2bf43-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="2bf43-112">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="2bf43-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2bf43-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="2bf43-113">Return values</span></span>

<span data-ttu-id="2bf43-114">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="2bf43-114">*Record list*</span></span>

<span data-ttu-id="2bf43-115">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="2bf43-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2bf43-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="2bf43-116">Usage notes</span></span>

<span data-ttu-id="2bf43-117">Loodud loendi struktuur sisaldab ainult neid välju, mis on esitatud argumentides mainitud iga kirjete loendi struktuuris.</span><span class="sxs-lookup"><span data-stu-id="2bf43-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="2bf43-118">Näide</span><span class="sxs-lookup"><span data-stu-id="2bf43-118">Example</span></span>

<span data-ttu-id="2bf43-119">Sisestate tüübi `Container` andmeallika **Kirje 1**.</span><span class="sxs-lookup"><span data-stu-id="2bf43-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="2bf43-120">See andmeallikas sisaldab tüübi `Calculated field` järgmisi pesastatud välju:</span><span class="sxs-lookup"><span data-stu-id="2bf43-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="2bf43-121">**Kood**: see väli sisaldab avaldist, mis tagastab tüübi `String` väärtuse.</span><span class="sxs-lookup"><span data-stu-id="2bf43-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="2bf43-122">**Summa**: see väli sisaldab avaldist, mis tagastab tüübi `Real` väärtuse.</span><span class="sxs-lookup"><span data-stu-id="2bf43-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="2bf43-123">Seejärel sisestate tüübi `Container` andmeallika **Kirje 2**.</span><span class="sxs-lookup"><span data-stu-id="2bf43-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="2bf43-124">See andmeallikas sisaldab tüübi `Calculated field` järgmisi pesastatud välju:</span><span class="sxs-lookup"><span data-stu-id="2bf43-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="2bf43-125">**Summa**: see väli sisaldab avaldist, mis tagastab tüübi `Real` väärtuse.</span><span class="sxs-lookup"><span data-stu-id="2bf43-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="2bf43-126">**IsValid**: see väli sisaldab avaldist, mis tagastab tüübi `Boolean` väärtuse.</span><span class="sxs-lookup"><span data-stu-id="2bf43-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER-i mudelivastenduse koostaja leht](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="2bf43-128">Sel juhul tagastab avaldis `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` uue loendi, mis sisaldab kaht kirjet.</span><span class="sxs-lookup"><span data-stu-id="2bf43-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![ER-i mudelivastenduse koostaja leht kahe kirjega](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="2bf43-130">Selle loendi struktuur koosneb ühest tüübi `Real` väljast **Summa**, kuna see väli on ainuke väli, mis on esitatud kutsutud funktsiooni igas argumendis.</span><span class="sxs-lookup"><span data-stu-id="2bf43-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ER-i mudelivastenduse koostaja lehe summaväli](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="2bf43-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2bf43-132">Additional resources</span></span>

[<span data-ttu-id="2bf43-133">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="2bf43-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="2bf43-134">Käivitatud ER-vormingu andmeallikate silumine andmevoo ja teisenduse analüüsimiseks</span><span class="sxs-lookup"><span data-stu-id="2bf43-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
