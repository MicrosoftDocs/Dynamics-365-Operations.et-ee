---
title: ER-i funktsioon FA_SUM
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FA_SUM.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c46f945a9caae2836886d051da820658e8be9af
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687692"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="35fdc-103">ER-i funktsioon FA_SUM</span><span class="sxs-lookup"><span data-stu-id="35fdc-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35fdc-104">Funktsioon `FA_SUM` tagastab *konteineri (kirje)* väärtuse, mis koosneb põhivara summade andmetest määratud põhivara kauba, väärtusmudeli koodi ja kuupäevade perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="35fdc-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fdc-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="35fdc-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="35fdc-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="35fdc-106">Arguments</span></span>

<span data-ttu-id="35fdc-107">`fixed asset code`: *string*</span><span class="sxs-lookup"><span data-stu-id="35fdc-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="35fdc-108">*Stringi* väärtus, mis tähistab põhivara kauba koodi, mille jaoks saldo arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="35fdc-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="35fdc-109">`value model code`: *string*</span><span class="sxs-lookup"><span data-stu-id="35fdc-109">`value model code`: *String*</span></span>

<span data-ttu-id="35fdc-110">*Stringi* väärtus, mis tähistab väärtusmudeli koodi, mille jaoks saldo arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="35fdc-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="35fdc-111">`start date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="35fdc-111">`start date`: *Date*</span></span>

<span data-ttu-id="35fdc-112">*Kuupäeva* väärtus, mis tähistab selle perioodi alguskuupäeva, mille kohta põhivara summad arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="35fdc-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="35fdc-113">`end date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="35fdc-113">`end date`: *Date*</span></span>

<span data-ttu-id="35fdc-114">*Kuupäeva* väärtus, mis tähistab selle perioodi lõpukuupäeva, mille kohta põhivara summad arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="35fdc-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="35fdc-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="35fdc-115">Return values</span></span>

<span data-ttu-id="35fdc-116">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="35fdc-116">*Container (record)*</span></span>

<span data-ttu-id="35fdc-117">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="35fdc-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="35fdc-118">Näide</span><span class="sxs-lookup"><span data-stu-id="35fdc-118">Example</span></span>

<span data-ttu-id="35fdc-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` tagastab põhivara **COMP-000001** andmekonteineri,m mis on valmistatud ette väärtuse mudelile **Praegune** ja ajavahemikule alates **Date1** kuni **Date2**.</span><span class="sxs-lookup"><span data-stu-id="35fdc-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35fdc-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="35fdc-120">Additional resources</span></span>

[<span data-ttu-id="35fdc-121">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="35fdc-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
