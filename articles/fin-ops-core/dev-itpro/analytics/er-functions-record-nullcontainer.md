---
title: ER-i funktsioon NULLCONTAINER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NULLCONTAINER.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746503"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="04538-103">ER-i funktsioon NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="04538-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04538-104">Funktsioon `NULLCONTAINER` tagastab *konteineri (kirje)* väärtuse null, millel on sama struktuur, kui määratud kirjete loendil või kirjel.</span><span class="sxs-lookup"><span data-stu-id="04538-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="04538-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="04538-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="04538-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="04538-106">Arguments</span></span>

<span data-ttu-id="04538-107">`list`: *kirjete loend* või *konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="04538-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="04538-108">Tüübi *Kirjete loend* või *Konteiner (kirje)* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="04538-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="04538-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="04538-109">Return values</span></span>

<span data-ttu-id="04538-110">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="04538-110">*Container (record)*</span></span>

<span data-ttu-id="04538-111">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="04538-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="04538-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="04538-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="04538-113">See funktsioon on aegunud.</span><span class="sxs-lookup"><span data-stu-id="04538-113">This function is obsolete.</span></span> <span data-ttu-id="04538-114">Kasutage selle asemel funktsiooni `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="04538-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="04538-115">Lisateavet vt [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="04538-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="04538-116">Näide</span><span class="sxs-lookup"><span data-stu-id="04538-116">Example</span></span>

<span data-ttu-id="04538-117">`NULLCONTAINER (SPLIT ("abc", 1))` tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="04538-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="04538-118">Lisateavet vt [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="04538-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04538-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="04538-119">Additional resources</span></span>

[<span data-ttu-id="04538-120">Kirje funktsioonid</span><span class="sxs-lookup"><span data-stu-id="04538-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]