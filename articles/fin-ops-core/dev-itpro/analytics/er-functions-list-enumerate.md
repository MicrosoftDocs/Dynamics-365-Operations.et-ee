---
title: ER-i funktsioon ENUMERATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ENUMERATE.
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746647"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="07d1a-103">ER-i funktsioon ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="07d1a-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07d1a-104">Funktsioon `ENUMERATE` tagastab uue *kirjete loendi* väärtuse, mis koosneb määratud loendi nummerdatud kirjetest.</span><span class="sxs-lookup"><span data-stu-id="07d1a-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d1a-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="07d1a-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="07d1a-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="07d1a-106">Arguments</span></span>

<span data-ttu-id="07d1a-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="07d1a-107">`list`: *Record list*</span></span>

<span data-ttu-id="07d1a-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="07d1a-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="07d1a-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="07d1a-109">Return values</span></span>

<span data-ttu-id="07d1a-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="07d1a-110">*Record list*</span></span>

<span data-ttu-id="07d1a-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="07d1a-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="07d1a-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="07d1a-112">Usage notes</span></span>

<span data-ttu-id="07d1a-113">Tagastatav nummerdatud kirjete loend näitab järgmisi täiendavaid elemente.</span><span class="sxs-lookup"><span data-stu-id="07d1a-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="07d1a-114">Väljade kirje(komponent **Väärtus**)</span><span class="sxs-lookup"><span data-stu-id="07d1a-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="07d1a-115">Praegune kirje indeks (komponent **Number**)</span><span class="sxs-lookup"><span data-stu-id="07d1a-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="07d1a-116">Näide</span><span class="sxs-lookup"><span data-stu-id="07d1a-116">Example</span></span>

<span data-ttu-id="07d1a-117">Järgmises näites on andmeallikas **Nummerdatud** loodud andmeallika **Hankijad hankijate** kirjete nummerdatud loendina, mis viitab tabelile VendTable.</span><span class="sxs-lookup"><span data-stu-id="07d1a-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="07d1a-118">Järgmine joonis näitab elektroonilise aruandluse (ER) vormingut.</span><span class="sxs-lookup"><span data-stu-id="07d1a-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="07d1a-119">Selles vormingus luuakse andmesidemed, et luua XML-vormingus väljund.</span><span class="sxs-lookup"><span data-stu-id="07d1a-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="07d1a-120">Selle väljund esitab üksikuid hankijaid nummerdatud sõlmedena.</span><span class="sxs-lookup"><span data-stu-id="07d1a-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="07d1a-121">Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.</span><span class="sxs-lookup"><span data-stu-id="07d1a-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="07d1a-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="07d1a-122">Additional resources</span></span>

[<span data-ttu-id="07d1a-123">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="07d1a-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]