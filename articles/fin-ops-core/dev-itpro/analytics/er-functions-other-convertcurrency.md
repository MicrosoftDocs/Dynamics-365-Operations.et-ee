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
ms.openlocfilehash: 1d0c168e07252f7c423271bc808f3fca3834077f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041511"
---
# <span data-ttu-id="3ac27-103"><a name="CONVERTCURRENCY">ER-i funktsioon CONVERTCURRENCY</a></span><span class="sxs-lookup"><span data-stu-id="3ac27-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ac27-104">Funktsioon `CONVERTCURRENCY` tagastab *tegeliku* väärtuse, mis kajastab määratud rahasumma määratud lähtevaluutast määratud sihtvaluutaks konverteerimise tulemust, kasutades määratud kuupäeval määratud ettevõtte sätteid.</span><span class="sxs-lookup"><span data-stu-id="3ac27-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac27-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="3ac27-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="3ac27-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="3ac27-106">Arguments</span></span>

<span data-ttu-id="3ac27-107">`amount`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="3ac27-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="3ac27-108">Numbriline väärtus, mis tähistab rahasummat, mis tuleb teisendada.</span><span class="sxs-lookup"><span data-stu-id="3ac27-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="3ac27-109">`source currency`: *string*</span><span class="sxs-lookup"><span data-stu-id="3ac27-109">`source currency`: *String*</span></span>

<span data-ttu-id="3ac27-110">Lähtevaluuta kood.</span><span class="sxs-lookup"><span data-stu-id="3ac27-110">The code of the source currency.</span></span>

<span data-ttu-id="3ac27-111">`target currency`: *string*</span><span class="sxs-lookup"><span data-stu-id="3ac27-111">`target currency`: *String*</span></span>

<span data-ttu-id="3ac27-112">Sihtvaluuta kood.</span><span class="sxs-lookup"><span data-stu-id="3ac27-112">The code of the target currency.</span></span>

<span data-ttu-id="3ac27-113">`date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="3ac27-113">`date`: *Date*</span></span>

<span data-ttu-id="3ac27-114">*Kuupäeva* väärtus, mis tähistab kuupäeva, mida kasutatakse teisendamise vahetuskursi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="3ac27-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="3ac27-115">`company`: *string*</span><span class="sxs-lookup"><span data-stu-id="3ac27-115">`company`: *String*</span></span>

<span data-ttu-id="3ac27-116">*Stringi* väärtus, mis tähistab ettevõtte koodi, mis varustab teisenduseks kasutatavate sätetega.</span><span class="sxs-lookup"><span data-stu-id="3ac27-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="3ac27-117">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="3ac27-117">Return values</span></span>

<span data-ttu-id="3ac27-118">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="3ac27-118">*Real*</span></span>

<span data-ttu-id="3ac27-119">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="3ac27-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="3ac27-120">Näide</span><span class="sxs-lookup"><span data-stu-id="3ac27-120">Example</span></span>

<span data-ttu-id="3ac27-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` tagastab ühe euroga võrdse väärtuse USA dollarites praeguse seansi kuupäeval **DEMF**-i ettevõtte sätete alusel.</span><span class="sxs-lookup"><span data-stu-id="3ac27-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ac27-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3ac27-122">Additional resources</span></span>

[<span data-ttu-id="3ac27-123">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="3ac27-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
