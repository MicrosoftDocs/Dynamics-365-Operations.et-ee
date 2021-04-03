---
title: ER-i funktsioon LIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LIST
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 4945ffd0e7bb7bbd238e2d3156c5599d3d423046
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563844"
---
# <a name="list-er-function"></a><span data-ttu-id="1434c-103">ER-i funktsioon LIST</span><span class="sxs-lookup"><span data-stu-id="1434c-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1434c-104">Funktsioon `LIST` tagastab *kirjete loendi* väärtuse, mis koosneb määratud argumentidest loodud uuest kirjete loendist.</span><span class="sxs-lookup"><span data-stu-id="1434c-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="1434c-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="1434c-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="1434c-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="1434c-106">Arguments</span></span>

<span data-ttu-id="1434c-107">`record 1`: *konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="1434c-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="1434c-108">Viide andmetüübi *Kirje* andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="1434c-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="1434c-109">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="1434c-109">This argument is required.</span></span>

<span data-ttu-id="1434c-110">`record N`: *konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="1434c-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="1434c-111">Viide andmetüübi *Kirje* andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="1434c-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="1434c-112">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="1434c-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1434c-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="1434c-113">Return values</span></span>

<span data-ttu-id="1434c-114">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="1434c-114">*Record list*</span></span>

<span data-ttu-id="1434c-115">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="1434c-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1434c-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="1434c-116">Usage notes</span></span>

<span data-ttu-id="1434c-117">Loodud loendi struktuur sisaldab ainult neid välju, mis on esitatud argumentides mainitud iga kirje struktuuris.</span><span class="sxs-lookup"><span data-stu-id="1434c-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="1434c-118">Näide</span><span class="sxs-lookup"><span data-stu-id="1434c-118">Example</span></span>

<span data-ttu-id="1434c-119">Sisestate tüübi *Konteiner* andmeallika **Kirje 1**.</span><span class="sxs-lookup"><span data-stu-id="1434c-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="1434c-120">See andmeallikas sisaldab tüübi *Arvutatud välja* järgmisi pesastatud välju:</span><span class="sxs-lookup"><span data-stu-id="1434c-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="1434c-121">**Kood:** see väli sisaldab avaldist, mis tagastab tüübi *String* väärtuse.</span><span class="sxs-lookup"><span data-stu-id="1434c-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="1434c-122">**Kogus:** see väli sisaldab avaldist, mis tagastab tüübi *Tegelik* väärtuse.</span><span class="sxs-lookup"><span data-stu-id="1434c-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="1434c-123">Seejärel sisestate tüübi *Konteiner* andmeallika **Kirje 2**.</span><span class="sxs-lookup"><span data-stu-id="1434c-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="1434c-124">See andmeallikas sisaldab tüübi *Arvutatud välja* järgmisi pesastatud välju:</span><span class="sxs-lookup"><span data-stu-id="1434c-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="1434c-125">**Kogus:** see väli sisaldab avaldist, mis tagastab tüübi *Tegelik* väärtuse.</span><span class="sxs-lookup"><span data-stu-id="1434c-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="1434c-126">**IsValid:** see väli sisaldab avaldist, mis tagastab tüübi *Kahendmuutuja* väärtuse.</span><span class="sxs-lookup"><span data-stu-id="1434c-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="1434c-127">Sel juhul tagastab avaldis `LIST('Record 1', 'Record 2')` uue loendi, mis sisaldab kaht kirjet.</span><span class="sxs-lookup"><span data-stu-id="1434c-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="1434c-128">Selle loendi struktuur koosneb ühest tüübi *Tegelik* väljast **Summa**, kuna see väli on ainuke väli, mis on esitatud kutsutud funktsiooni igas argumendis.</span><span class="sxs-lookup"><span data-stu-id="1434c-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1434c-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1434c-129">Additional resources</span></span>

[<span data-ttu-id="1434c-130">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="1434c-130">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]