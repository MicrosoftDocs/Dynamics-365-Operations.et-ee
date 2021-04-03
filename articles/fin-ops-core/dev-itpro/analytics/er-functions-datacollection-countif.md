---
title: ER-i funktsioon COUNTIF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni COUNTIF.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 19ceb8d3023aadeb6307ed5d930587a8f00f63b7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561370"
---
# <a name="countif-er-function"></a><span data-ttu-id="bf037-103">ER-i funktsioon COUNTIF</span><span class="sxs-lookup"><span data-stu-id="bf037-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf037-104">Funktsioon `COUNTIF` tagastab *täisarvu* väärtuse, mis tähistab vorminguelementide arvu, mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="bf037-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="bf037-105">See tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="bf037-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf037-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="bf037-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="bf037-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="bf037-107">Arguments</span></span>

<span data-ttu-id="bf037-108">`condition range`: *string*</span><span class="sxs-lookup"><span data-stu-id="bf037-108">`condition range`: *String*</span></span>

<span data-ttu-id="bf037-109">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud elektroonilise aruandluse (ER) vormingu komponendi atribuudis **Kogutud andmete võtme nimi**.</span><span class="sxs-lookup"><span data-stu-id="bf037-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="bf037-110">`condition value`: *string*</span><span class="sxs-lookup"><span data-stu-id="bf037-110">`condition value`: *String*</span></span>

<span data-ttu-id="bf037-111">Väärtus, mis tagastatakse avaldise poolt, mis on konfigureeritud ER-vormingu komponendi atribuudis **Kogutud andmete võtme väärtus**.</span><span class="sxs-lookup"><span data-stu-id="bf037-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="bf037-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="bf037-112">Return values</span></span>

<span data-ttu-id="bf037-113">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="bf037-113">*Integer*</span></span>

<span data-ttu-id="bf037-114">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="bf037-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bf037-115">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="bf037-115">Usage notes</span></span>

<span data-ttu-id="bf037-116">Atribuute **Kogutud andmete võtme nimi** ja **Kogutud andmete võtme väärtus** saab konfigureerida kas ER-vormingu komponendile **Järjestus** või komponendile **XML-element**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="bf037-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="bf037-117">See funktsioon tagastab väärtuse **0** (null), kui praeguse komponendi **Üldine\\Fail** suvand **Kogu väljundi üksikasjad** on välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="bf037-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="bf037-118">Argumendis `condition range` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="bf037-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="bf037-119">Argumendis `condition value` saab kasutada metamärki **„\*”**, et tähistada mis tahes märki mitmete seast.</span><span class="sxs-lookup"><span data-stu-id="bf037-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="bf037-120">Näide</span><span class="sxs-lookup"><span data-stu-id="bf037-120">Example</span></span>

<span data-ttu-id="bf037-121">Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest [ER-i loendamise ja liitmise vormingu väljundi kasutusandmed](tasks/er-format-counting-summing-1.md), mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa.</span><span class="sxs-lookup"><span data-stu-id="bf037-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf037-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="bf037-122">Additional resources</span></span>

[<span data-ttu-id="bf037-123">Andmete kogumise funktsioonid</span><span class="sxs-lookup"><span data-stu-id="bf037-123">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]