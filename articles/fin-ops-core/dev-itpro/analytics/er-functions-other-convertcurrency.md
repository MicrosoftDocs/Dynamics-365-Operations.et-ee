---
title: ER-i funktsioon CONVERTCURRENCY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni CONVERTCURRENCY.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6e0069c6e9227d4cf1045eeebbb825a2f943c3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744307"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="7e7d6-103">ER-i funktsioon CONVERTCURRENCY</span><span class="sxs-lookup"><span data-stu-id="7e7d6-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e7d6-104">Funktsioon `CONVERTCURRENCY` tagastab *tegeliku* väärtuse, mis kajastab määratud rahasumma määratud lähtevaluutast määratud sihtvaluutaks konverteerimise tulemust, kasutades määratud kuupäeval määratud ettevõtte sätteid.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7d6-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="7e7d6-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="7e7d6-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="7e7d6-106">Arguments</span></span>

<span data-ttu-id="7e7d6-107">`amount`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="7e7d6-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="7e7d6-108">Numbriline väärtus, mis tähistab rahasummat, mis tuleb teisendada.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="7e7d6-109">`source currency`: *string*</span><span class="sxs-lookup"><span data-stu-id="7e7d6-109">`source currency`: *String*</span></span>

<span data-ttu-id="7e7d6-110">Lähtevaluuta kood.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-110">The code of the source currency.</span></span>

<span data-ttu-id="7e7d6-111">`target currency`: *string*</span><span class="sxs-lookup"><span data-stu-id="7e7d6-111">`target currency`: *String*</span></span>

<span data-ttu-id="7e7d6-112">Sihtvaluuta kood.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-112">The code of the target currency.</span></span>

<span data-ttu-id="7e7d6-113">`date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="7e7d6-113">`date`: *Date*</span></span>

<span data-ttu-id="7e7d6-114">*Kuupäeva* väärtus, mis tähistab kuupäeva, mida kasutatakse teisendamise vahetuskursi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="7e7d6-115">`company`: *string*</span><span class="sxs-lookup"><span data-stu-id="7e7d6-115">`company`: *String*</span></span>

<span data-ttu-id="7e7d6-116">*Stringi* väärtus, mis tähistab ettevõtte koodi, mis varustab teisenduseks kasutatavate sätetega.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e7d6-117">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="7e7d6-117">Return values</span></span>

<span data-ttu-id="7e7d6-118">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="7e7d6-118">*Real*</span></span>

<span data-ttu-id="7e7d6-119">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7e7d6-120">Näide</span><span class="sxs-lookup"><span data-stu-id="7e7d6-120">Example</span></span>

<span data-ttu-id="7e7d6-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` tagastab ühe euroga võrdse väärtuse USA dollarites praeguse seansi kuupäeval **DEMF**-i ettevõtte sätete alusel.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e7d6-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7e7d6-122">Additional resources</span></span>

[<span data-ttu-id="7e7d6-123">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="7e7d6-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
