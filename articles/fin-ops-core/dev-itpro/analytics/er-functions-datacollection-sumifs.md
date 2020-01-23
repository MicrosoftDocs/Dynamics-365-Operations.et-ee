---
title: ER-i funktsioon SUMIFS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SUMIFS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 6820be1976e722f7b108b3e9303c8ed4d822ae9b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917599"
---
# <span data-ttu-id="3c67e-103"><a name="SUMIFS">ER-i funktsioon SUMIFS</a></span><span class="sxs-lookup"><span data-stu-id="3c67e-103"><a name="SUMIFS">SUMIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c67e-104">Funktsioon `SUMIFS` tagastab *tegeliku* väärtuse, mis tähistab vorminguelementide sidumiste tagastatud väärtuste summat ja mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="3c67e-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="3c67e-105">Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="3c67e-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c67e-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="3c67e-106">Syntax</span></span>

```
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="3c67e-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="3c67e-107">Arguments</span></span>

<span data-ttu-id="3c67e-108">`key name for summing`: *string*</span><span class="sxs-lookup"><span data-stu-id="3c67e-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="3c67e-109">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme nimi**, mille puhul tuleb summeerimise eesmärgil kasutada siduvat väärtust.</span><span class="sxs-lookup"><span data-stu-id="3c67e-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="3c67e-110">Atribuudi **Kogutud andmete võtme nimi** saab konfigureerida kas ER-vormingu komponendile **Numbriline** või komponendile **String**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="3c67e-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="3c67e-111">`condition 1 range`: *string*</span><span class="sxs-lookup"><span data-stu-id="3c67e-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="3c67e-112">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme nimi**.</span><span class="sxs-lookup"><span data-stu-id="3c67e-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="3c67e-113">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="3c67e-113">This argument is mandatory.</span></span>

<span data-ttu-id="3c67e-114">Atribuudi **Kogutud andmete võtme nimi** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="3c67e-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="3c67e-115">`condition 1 value`: *string*</span><span class="sxs-lookup"><span data-stu-id="3c67e-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="3c67e-116">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme väärtus**.</span><span class="sxs-lookup"><span data-stu-id="3c67e-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="3c67e-117">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="3c67e-117">This argument is mandatory.</span></span>

<span data-ttu-id="3c67e-118">Atribuudi **Kogutud andmete võtme väärtus** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="3c67e-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="3c67e-119">`condition N range`: *string*</span><span class="sxs-lookup"><span data-stu-id="3c67e-119">`condition N range`: *String*</span></span>

<span data-ttu-id="3c67e-120">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme nimi**.</span><span class="sxs-lookup"><span data-stu-id="3c67e-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="3c67e-121">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="3c67e-121">These additional arguments are optional.</span></span>

<span data-ttu-id="3c67e-122">Atribuudi **Kogutud andmete võtme nimi** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="3c67e-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="3c67e-123">`condition N value`: *string*</span><span class="sxs-lookup"><span data-stu-id="3c67e-123">`condition N value`: *String*</span></span>

<span data-ttu-id="3c67e-124">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme väärtus**.</span><span class="sxs-lookup"><span data-stu-id="3c67e-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="3c67e-125">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="3c67e-125">These additional arguments are optional.</span></span>

<span data-ttu-id="3c67e-126">Atribuudi **Kogutud andmete võtme väärtus** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="3c67e-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="3c67e-127">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="3c67e-127">Return values</span></span>

<span data-ttu-id="3c67e-128">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="3c67e-128">*Real*</span></span>

<span data-ttu-id="3c67e-129">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="3c67e-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3c67e-130">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="3c67e-130">Usage notes</span></span>

<span data-ttu-id="3c67e-131">See funktsioon tagastab väärtuse **0** (null), kui praeguse komponendi **Üldine\\Fail** suvand **Kogu väljundi üksikasjad** on välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="3c67e-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="3c67e-132">Argumentides `condition range` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="3c67e-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="3c67e-133">Argumentides `condition value` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="3c67e-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="3c67e-134">Näide</span><span class="sxs-lookup"><span data-stu-id="3c67e-134">Example</span></span>

<span data-ttu-id="3c67e-135">Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest [ER-i loendamise ja liitmise vormingu väljundi kasutusandmed](tasks/er-format-counting-summing-1.md), mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa.</span><span class="sxs-lookup"><span data-stu-id="3c67e-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c67e-136">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3c67e-136">Additional resources</span></span>

[<span data-ttu-id="3c67e-137">Andmete kogumise funktsioonid</span><span class="sxs-lookup"><span data-stu-id="3c67e-137">Data collection functions</span></span>](er-functions-category-data-collection.md)