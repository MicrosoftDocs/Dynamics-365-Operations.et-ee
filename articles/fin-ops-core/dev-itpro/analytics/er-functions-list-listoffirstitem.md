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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041971"
---
# <span data-ttu-id="6915c-103"><a name="LISTOFFIRSTITEM">ER-i funktsioon LISTOFFIRSTITEM</a></span><span class="sxs-lookup"><span data-stu-id="6915c-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6915c-104">Funktsioon `LISTOFFIRSTITEM` tagastab *kirjete loendi* väärtuse, mis koosneb ainult määratud loendi esimesest kirjest.</span><span class="sxs-lookup"><span data-stu-id="6915c-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6915c-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6915c-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="6915c-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="6915c-106">Arguments</span></span>

<span data-ttu-id="6915c-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="6915c-107">`list`: *Record list*</span></span>

<span data-ttu-id="6915c-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="6915c-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="6915c-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6915c-109">Return values</span></span>

<span data-ttu-id="6915c-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="6915c-110">*Record list*</span></span>

<span data-ttu-id="6915c-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="6915c-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="6915c-112">Näide</span><span class="sxs-lookup"><span data-stu-id="6915c-112">Example</span></span>

<span data-ttu-id="6915c-113">Avaldis `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` tagastab tekstiväärtuse **„A”**.</span><span class="sxs-lookup"><span data-stu-id="6915c-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6915c-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6915c-114">Additional resources</span></span>

[<span data-ttu-id="6915c-115">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6915c-115">List functions</span></span>](er-functions-category-list.md)
