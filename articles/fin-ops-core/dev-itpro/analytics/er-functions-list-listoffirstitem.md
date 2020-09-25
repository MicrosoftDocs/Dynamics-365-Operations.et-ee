---
title: ER-i funktsioon LISTOFFIRSTITEM
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LISTOFFIRSTITEM.
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
ms.openlocfilehash: 069ec0c6d5578ca6ab68814adf325bd79e73b9e8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745053"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="8ae41-103">ER-i funktsioon LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="8ae41-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ae41-104">Funktsioon `LISTOFFIRSTITEM` tagastab *kirjete loendi* väärtuse, mis koosneb ainult määratud loendi esimesest kirjest.</span><span class="sxs-lookup"><span data-stu-id="8ae41-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae41-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="8ae41-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="8ae41-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="8ae41-106">Arguments</span></span>

<span data-ttu-id="8ae41-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="8ae41-107">`list`: *Record list*</span></span>

<span data-ttu-id="8ae41-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="8ae41-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8ae41-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="8ae41-109">Return values</span></span>

<span data-ttu-id="8ae41-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="8ae41-110">*Record list*</span></span>

<span data-ttu-id="8ae41-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="8ae41-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="8ae41-112">Näide</span><span class="sxs-lookup"><span data-stu-id="8ae41-112">Example</span></span>

<span data-ttu-id="8ae41-113">Avaldis `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` tagastab tekstiväärtuse **„A”**.</span><span class="sxs-lookup"><span data-stu-id="8ae41-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ae41-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8ae41-114">Additional resources</span></span>

[<span data-ttu-id="8ae41-115">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="8ae41-115">List functions</span></span>](er-functions-category-list.md)
