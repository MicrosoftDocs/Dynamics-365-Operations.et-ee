---
title: ER-i funktsioon SUMIF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SUMIF.
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
ms.openlocfilehash: 374569d3bbe59f1b96eee9c789b97b7b2a6004bf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042477"
---
# <span data-ttu-id="fcdb8-103"><a name="SUMIF">ER-i funktsioon SUMIF</a></span><span class="sxs-lookup"><span data-stu-id="fcdb8-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcdb8-104">Funktsioon `SUMIF` tagastab *tegeliku* väärtuse, mis tähistab vorminguelementide sidumiste tagastatud väärtuste summat ja mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="fcdb8-105">See tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcdb8-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="fcdb8-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="fcdb8-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="fcdb8-107">Arguments</span></span>

<span data-ttu-id="fcdb8-108">`key name for summing`: *string*</span><span class="sxs-lookup"><span data-stu-id="fcdb8-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="fcdb8-109">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme nimi**, mille puhul tuleb summeerimise eesmärgil kasutada siduvat väärtust.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="fcdb8-110">Atribuudi **Kogutud andmete võtme väärtus** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="fcdb8-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="fcdb8-111">Return values</span></span>

<span data-ttu-id="fcdb8-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="fcdb8-112">*Real*</span></span>

<span data-ttu-id="fcdb8-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fcdb8-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="fcdb8-114">Usage notes</span></span>

<span data-ttu-id="fcdb8-115">See funktsioon tagastab väärtuse **0** (null), kui praeguse komponendi **Üldine\\Fail** suvand **Kogu väljundi üksikasjad** on välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="fcdb8-116">Argumendis `condition range` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="fcdb8-117">Argumendis `condition value` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="fcdb8-118">Näide</span><span class="sxs-lookup"><span data-stu-id="fcdb8-118">Example</span></span>

<span data-ttu-id="fcdb8-119">Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest [ER-i loendamise ja liitmise vormingu väljundi kasutusandmed](tasks/er-format-counting-summing-1.md), mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa.</span><span class="sxs-lookup"><span data-stu-id="fcdb8-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcdb8-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fcdb8-120">Additional resources</span></span>

[<span data-ttu-id="fcdb8-121">Andmete kogumise funktsioonid</span><span class="sxs-lookup"><span data-stu-id="fcdb8-121">Data collection functions</span></span>](er-functions-category-data-collection.md)
