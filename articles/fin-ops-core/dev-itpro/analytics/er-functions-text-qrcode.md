---
title: ER-i funktsioon QRCODE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni QRCODE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 92665936decc87b29f2fabb346f4d16745d0a30b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562657"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="b3cc4-103">ER-i funktsioon QRCODE</span><span class="sxs-lookup"><span data-stu-id="b3cc4-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3cc4-104">Funktsioon `QRCODE` tagastab *konteineri* väärtuse, mis esitab määratud stringi puhul binaarvormingus ruutkoodi (QR-koodi) pildi.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3cc4-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="b3cc4-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="b3cc4-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="b3cc4-106">Arguments</span></span>

<span data-ttu-id="b3cc4-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="b3cc4-107">`text`: *String*</span></span>

<span data-ttu-id="b3cc4-108">*Stringi* väärtus, mis tähistab algteksti.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b3cc4-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="b3cc4-109">Return values</span></span>

<span data-ttu-id="b3cc4-110">*Konteiner*</span><span class="sxs-lookup"><span data-stu-id="b3cc4-110">*Container*</span></span>

<span data-ttu-id="b3cc4-111">Tulemuseks olev binaarne voog.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="b3cc4-112">Näide</span><span class="sxs-lookup"><span data-stu-id="b3cc4-112">Example</span></span>

<span data-ttu-id="b3cc4-113">Saate konfigureerida elektroonilise aruandluse (ER) vormingu looma väljamineva dokumendi Microsoft Office’i vormingus (Exceli töövihikud või Wordi dokumendid), kasutades eelmääratletud malli.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="b3cc4-114">See mall võib sisaldada QR-koodi pildi kohatäitena objekti **Pilt** (Exceli töövihik) või **Pildisisu juhtelement** (Wordi dokument).</span><span class="sxs-lookup"><span data-stu-id="b3cc4-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="b3cc4-115">Peate lisama konfigureeritud ER-vormingule elemendi **Lahter**, mida kasutatakse selle kohatäite täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="b3cc4-116">Et määrata, millist teavet QR-koodis talletatakse, peate määrama sidumise sellele elemendile **Lahter**.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="b3cc4-117">Näiteks saate konfigureerida sellise sidumise, mis sisaldab järgmist avaldist:</span><span class="sxs-lookup"><span data-stu-id="b3cc4-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="b3cc4-118">Kui käitate konfigureeritud ER-vormingut, siis kasutatakse andmeallika **model.ListOfShelfLabels** välja **LabelText** teksti väärtust QR-koodi pildi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="b3cc4-119">See pilt asendab QR-koodi pildi kohatäite dokumendi mallis, mida kasutatakse väljamineva dokumendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="b3cc4-120">Kui loodud dokumendi pilt on skannitud, tagastab see teksti, mis võeti mudeli andmeallika **model.ListOfShelfLabels** väljalt **LabelText**.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="b3cc4-121">Lisateavet vt teemast [Piltide ja vormide manustamine ER-i abil loodavatesse dokumentidesse](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="b3cc4-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3cc4-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b3cc4-122">Additional resources</span></span>

[<span data-ttu-id="b3cc4-123">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="b3cc4-123">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]