---
title: ER-i funktsioon FIRST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FIRST.
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
ms.openlocfilehash: d30c8481866ccf3f7080197b37586a0460a4ad2c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746575"
---
# <a name="first-er-function"></a><span data-ttu-id="7e64f-103">ER-i funktsioon FIRST</span><span class="sxs-lookup"><span data-stu-id="7e64f-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e64f-104">Funktsioon `FIRST` tagastab määratud loendi esimese kirje *konteineri (kirje)* väärtusena, kui see loend pole tühi.</span><span class="sxs-lookup"><span data-stu-id="7e64f-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="7e64f-105">Kui loend on tühi, esitab see funktsioon erandi.</span><span class="sxs-lookup"><span data-stu-id="7e64f-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e64f-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="7e64f-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="7e64f-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="7e64f-107">Arguments</span></span>

<span data-ttu-id="7e64f-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="7e64f-108">`list`: *Record list*</span></span>

<span data-ttu-id="7e64f-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="7e64f-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e64f-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="7e64f-110">Return values</span></span>

<span data-ttu-id="7e64f-111">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="7e64f-111">*Container (record)*</span></span>

<span data-ttu-id="7e64f-112">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="7e64f-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="7e64f-113">Näide 1</span><span class="sxs-lookup"><span data-stu-id="7e64f-113">Example 1</span></span>

<span data-ttu-id="7e64f-114">Avaldis `FIRST(SPLIT("ABC",1)).Value` tagastab tekstiväärtuse **„A”**.</span><span class="sxs-lookup"><span data-stu-id="7e64f-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7e64f-115">Näide 2</span><span class="sxs-lookup"><span data-stu-id="7e64f-115">Example 2</span></span>

<span data-ttu-id="7e64f-116">Avaldis `FIRST(SPLIT("",1)).Value` tagastab käitusaja erandi.</span><span class="sxs-lookup"><span data-stu-id="7e64f-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e64f-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7e64f-117">Additional resources</span></span>

[<span data-ttu-id="7e64f-118">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="7e64f-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]