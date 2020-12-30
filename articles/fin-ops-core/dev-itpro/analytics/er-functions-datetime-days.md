---
title: ER-i funktsioon DAYS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DAYS
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682337"
---
# <a name="days-er-function"></a><span data-ttu-id="03ad6-103">ER-i funktsioon DAYS</span><span class="sxs-lookup"><span data-stu-id="03ad6-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03ad6-104">Funktsioon `DAYS` tagastab *täisarvu* väärtuse, mis tähistab ühe määratud kuupäeva ja teise määratud kuupäeva vahelise päevade arvu täisarvuna.</span><span class="sxs-lookup"><span data-stu-id="03ad6-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ad6-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="03ad6-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="03ad6-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="03ad6-106">Arguments</span></span>

<span data-ttu-id="03ad6-107">`date 1`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="03ad6-107">`date 1`: *Date*</span></span>

<span data-ttu-id="03ad6-108">Kuupäeva väärtus, mis tähistab päevade arvu arvutamiseks kasutatavat alguskuupäeva</span><span class="sxs-lookup"><span data-stu-id="03ad6-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="03ad6-109">`date 2`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="03ad6-109">`date 2`: *Date*</span></span>

<span data-ttu-id="03ad6-110">Kuupäeva väärtus, mis tähistab päevade arvu arvutamiseks kasutatavat lõpukuupäeva</span><span class="sxs-lookup"><span data-stu-id="03ad6-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="03ad6-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="03ad6-111">Return values</span></span>

<span data-ttu-id="03ad6-112">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="03ad6-112">*Integer*</span></span>

<span data-ttu-id="03ad6-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="03ad6-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="03ad6-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="03ad6-114">Usage notes</span></span>

<span data-ttu-id="03ad6-115">Funktsioon `DAYS` tagastab vastuseks positiivse väärtuse, kui esimene kuupäev on hilisem kui teine kuupäev, see tagastab väärtuse **0 (null)**, kui esimene kuupäev võrdub teise kuupäevaga, ja see tagastab vastuseks negatiivse väärtuse, kui esimene kuupäev on varasem kui teine kuupäev.</span><span class="sxs-lookup"><span data-stu-id="03ad6-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="03ad6-116">Näide</span><span class="sxs-lookup"><span data-stu-id="03ad6-116">Example</span></span>

<span data-ttu-id="03ad6-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` tagastab **–1**.</span><span class="sxs-lookup"><span data-stu-id="03ad6-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03ad6-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="03ad6-118">Additional resources</span></span>

[<span data-ttu-id="03ad6-119">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="03ad6-119">Date and time functions</span></span>](er-functions-category-datetime.md)
