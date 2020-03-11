---
title: ER-i funktsioon COUNTIFS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni COUNTIFS.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 9627c7835c8f3f1b6aedc1f691470dc29a11d6b5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042546"
---
# <span data-ttu-id="339d1-103"><a name="COUNTIFS">ER-i funktsioon COUNTIFS</a></span><span class="sxs-lookup"><span data-stu-id="339d1-103"><a name="COUNTIFS">COUNTIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="339d1-104">Funktsioon `COUNTIFS` tagastab *täisarvu* väärtuse, mis tähistab vorminguelementide arvu, mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="339d1-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="339d1-105">Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="339d1-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="339d1-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="339d1-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="339d1-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="339d1-107">Arguments</span></span>

<span data-ttu-id="339d1-108">`condition 1 range`: *string*</span><span class="sxs-lookup"><span data-stu-id="339d1-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="339d1-109">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud elektroonilise aruandluse (ER) vormingu komponendi atribuudis **Kogutud andmete võtme nimi**.</span><span class="sxs-lookup"><span data-stu-id="339d1-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="339d1-110">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="339d1-110">This argument is mandatory.</span></span>

<span data-ttu-id="339d1-111">`condition 1 value`: *string*</span><span class="sxs-lookup"><span data-stu-id="339d1-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="339d1-112">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme väärtus**.</span><span class="sxs-lookup"><span data-stu-id="339d1-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="339d1-113">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="339d1-113">This argument is mandatory.</span></span>

<span data-ttu-id="339d1-114">`condition N range`: *string*</span><span class="sxs-lookup"><span data-stu-id="339d1-114">`condition N range`: *String*</span></span>

<span data-ttu-id="339d1-115">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme nimi**.</span><span class="sxs-lookup"><span data-stu-id="339d1-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="339d1-116">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="339d1-116">These additional arguments are optional.</span></span>

<span data-ttu-id="339d1-117">`condition N value`: *string*</span><span class="sxs-lookup"><span data-stu-id="339d1-117">`condition N value`: *String*</span></span>

<span data-ttu-id="339d1-118">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme väärtus**.</span><span class="sxs-lookup"><span data-stu-id="339d1-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="339d1-119">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="339d1-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="339d1-120">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="339d1-120">Return values</span></span>

<span data-ttu-id="339d1-121">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="339d1-121">*Integer*</span></span>

<span data-ttu-id="339d1-122">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="339d1-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="339d1-123">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="339d1-123">Usage notes</span></span>

<span data-ttu-id="339d1-124">Atribuute **Kogutud andmete võtme nimi** ja **Kogutud andmete võtme väärtus** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="339d1-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="339d1-125">See funktsioon tagastab väärtuse **0** (null), kui praeguse komponendi **Üldine\\Fail** suvand **Kogu väljundi üksikasjad** on välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="339d1-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="339d1-126">Argumentides `condition range` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="339d1-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="339d1-127">Argumentides `condition value` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="339d1-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="339d1-128">Näide</span><span class="sxs-lookup"><span data-stu-id="339d1-128">Example</span></span>

<span data-ttu-id="339d1-129">Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest [ER-i loendamise ja liitmise vormingu väljundi kasutusandmed](tasks/er-format-counting-summing-1.md), mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa.</span><span class="sxs-lookup"><span data-stu-id="339d1-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="339d1-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="339d1-130">Additional resources</span></span>

[<span data-ttu-id="339d1-131">Andmete kogumise funktsioonid</span><span class="sxs-lookup"><span data-stu-id="339d1-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
