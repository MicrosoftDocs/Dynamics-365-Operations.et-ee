---
title: ER-i funktsioon TABLENAME2ID
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TABLENAME2ID.
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
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041259"
---
# <span data-ttu-id="ff5dc-103"><a name="TABLENAME2ID">ER-i funktsioon TABLENAME2ID</a></span><span class="sxs-lookup"><span data-stu-id="ff5dc-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff5dc-104">Funktsioon `TABLENAME2ID` tagastab määratud tabeli nime tabeli ID numbrilise esituse *täisarvulise* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="ff5dc-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5dc-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="ff5dc-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="ff5dc-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="ff5dc-106">Arguments</span></span>

<span data-ttu-id="ff5dc-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="ff5dc-107">`text`: *String*</span></span>

<span data-ttu-id="ff5dc-108">Teksti väärtus, mis tähistab kehtivat tabeli nime.</span><span class="sxs-lookup"><span data-stu-id="ff5dc-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff5dc-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="ff5dc-109">Return values</span></span>

<span data-ttu-id="ff5dc-110">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="ff5dc-110">*Integer*</span></span>

<span data-ttu-id="ff5dc-111">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="ff5dc-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ff5dc-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="ff5dc-112">Usage notes</span></span>

<span data-ttu-id="ff5dc-113">Selle funktsiooni käitamisel võivad teenuse Microsoft Dynamics 365 Finance erinevatel eksemplaridel olla erinevad tulemused, isegi kui kasutatakse sama ettevõtte nime.</span><span class="sxs-lookup"><span data-stu-id="ff5dc-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="ff5dc-114">Näide</span><span class="sxs-lookup"><span data-stu-id="ff5dc-114">Example</span></span>

<span data-ttu-id="ff5dc-115">`TABLENAME2ID ("Intrastat")` tagastab **1510**.</span><span class="sxs-lookup"><span data-stu-id="ff5dc-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff5dc-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ff5dc-116">Additional resources</span></span>

[<span data-ttu-id="ff5dc-117">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="ff5dc-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
