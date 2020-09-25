---
title: ER-i funktsioon NULLCONTAINER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NULLCONTAINER.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: dac6283ec35d3d03f586ca157048bd3ecc4bfa8a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743923"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="97bca-103">ER-i funktsioon NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="97bca-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97bca-104">Funktsioon `NULLCONTAINER` tagastab *konteineri (kirje)* väärtuse null, millel on sama struktuur, kui määratud kirjete loendil või kirjel.</span><span class="sxs-lookup"><span data-stu-id="97bca-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="97bca-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="97bca-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="97bca-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="97bca-106">Arguments</span></span>

<span data-ttu-id="97bca-107">`list`: *kirjete loend* või *konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="97bca-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="97bca-108">Tüübi *Kirjete loend* või *Konteiner (kirje)* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="97bca-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="97bca-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="97bca-109">Return values</span></span>

<span data-ttu-id="97bca-110">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="97bca-110">*Container (record)*</span></span>

<span data-ttu-id="97bca-111">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="97bca-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="97bca-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="97bca-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="97bca-113">See funktsioon on aegunud.</span><span class="sxs-lookup"><span data-stu-id="97bca-113">This function is obsolete.</span></span> <span data-ttu-id="97bca-114">Kasutage selle asemel funktsiooni `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="97bca-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="97bca-115">Lisateavet vt [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="97bca-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="97bca-116">Näide</span><span class="sxs-lookup"><span data-stu-id="97bca-116">Example</span></span>

<span data-ttu-id="97bca-117">`NULLCONTAINER (SPLIT ("abc", 1))` tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="97bca-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="97bca-118">Lisateavet vt [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="97bca-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97bca-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="97bca-119">Additional resources</span></span>

[<span data-ttu-id="97bca-120">Kirje funktsioonid</span><span class="sxs-lookup"><span data-stu-id="97bca-120">Record functions</span></span>](er-functions-category-record.md)
