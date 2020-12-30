---
title: ER-i funktsioon SUMIF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SUMIF.
author: NickSelin
manager: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 52f9cdb78efa6fe0dbebd2ffd78cd6e9185d6b2e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685347"
---
# <a name="sumif-er-function"></a><span data-ttu-id="60ac1-103">ER-i funktsioon SUMIF</span><span class="sxs-lookup"><span data-stu-id="60ac1-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60ac1-104">Funktsioon `SUMIF` tagastab *tegeliku* väärtuse, mis tähistab vorminguelementide sidumiste tagastatud väärtuste summat ja mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="60ac1-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="60ac1-105">See tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="60ac1-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ac1-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="60ac1-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="60ac1-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="60ac1-107">Arguments</span></span>

<span data-ttu-id="60ac1-108">`key name for summing`: *string*</span><span class="sxs-lookup"><span data-stu-id="60ac1-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="60ac1-109">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme nimi**, mille puhul tuleb summeerimise eesmärgil kasutada siduvat väärtust.</span><span class="sxs-lookup"><span data-stu-id="60ac1-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="60ac1-110">Atribuudi **Kogutud andmete võtme väärtus** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="60ac1-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="60ac1-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="60ac1-111">Return values</span></span>

<span data-ttu-id="60ac1-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="60ac1-112">*Real*</span></span>

<span data-ttu-id="60ac1-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="60ac1-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="60ac1-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="60ac1-114">Usage notes</span></span>

<span data-ttu-id="60ac1-115">See funktsioon tagastab väärtuse **0** (null), kui praeguse komponendi **Üldine\\Fail** suvand **Kogu väljundi üksikasjad** on välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="60ac1-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="60ac1-116">Argumendis `condition range` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="60ac1-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="60ac1-117">Argumendis `condition value` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="60ac1-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="60ac1-118">Näide</span><span class="sxs-lookup"><span data-stu-id="60ac1-118">Example</span></span>

<span data-ttu-id="60ac1-119">Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest [ER-i loendamise ja liitmise vormingu väljundi kasutusandmed](tasks/er-format-counting-summing-1.md), mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa.</span><span class="sxs-lookup"><span data-stu-id="60ac1-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="60ac1-120">Selle funktsiooni kasutamise kohta lisateabe ja näidete saamiseks vt teemasid [ER-vormingu elementide järjestuse käivitamise edasilükkamine](er-defer-sequence-element.md#Example) ja [XML-elementide käivitamise edasilükkamine ER-vormingus](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="60ac1-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60ac1-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="60ac1-121">Additional resources</span></span>

[<span data-ttu-id="60ac1-122">Andmete kogumise funktsioonid</span><span class="sxs-lookup"><span data-stu-id="60ac1-122">Data collection functions</span></span>](er-functions-category-data-collection.md)
