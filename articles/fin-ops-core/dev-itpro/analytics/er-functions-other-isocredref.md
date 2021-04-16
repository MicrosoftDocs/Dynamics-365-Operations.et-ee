---
title: ER-i funktsioon ISOCREDREF
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ISOCREDREF.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748313"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="486fa-103">ER-i funktsioon ISOCREDREF</span><span class="sxs-lookup"><span data-stu-id="486fa-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="486fa-104">Funktsioon `ISOCREDREF` tagastab *stringi* väärtuse, mis tähistab Rahvusvahelise Standardiorganisatsiooni (ISO) kreeditori viidet määratud arve numbri arvude ja tähestikus olevate sümbolite alusel.</span><span class="sxs-lookup"><span data-stu-id="486fa-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="486fa-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="486fa-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="486fa-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="486fa-106">Arguments</span></span>

<span data-ttu-id="486fa-107">`invoice number digits`: *string*</span><span class="sxs-lookup"><span data-stu-id="486fa-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="486fa-108">Teksti väärtus, mis tähistab arve numbri numbreid.</span><span class="sxs-lookup"><span data-stu-id="486fa-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="486fa-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="486fa-109">Return values</span></span>

<span data-ttu-id="486fa-110">*String*</span><span class="sxs-lookup"><span data-stu-id="486fa-110">*String*</span></span>

<span data-ttu-id="486fa-111">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="486fa-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="486fa-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="486fa-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="486fa-113">ISO-ga ühildumatute sümbolite tähestikust eemaldamiseks tuleb argument `invoice number digits` enne sellele funktsioonile edastamist tõlkida.</span><span class="sxs-lookup"><span data-stu-id="486fa-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="486fa-114">Näide</span><span class="sxs-lookup"><span data-stu-id="486fa-114">Example</span></span>

<span data-ttu-id="486fa-115">`ISOCredRef ("VEND-200002")` tagastab **„RF23VEND-200002”**.</span><span class="sxs-lookup"><span data-stu-id="486fa-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="486fa-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="486fa-116">Additional resources</span></span>

[<span data-ttu-id="486fa-117">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="486fa-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]