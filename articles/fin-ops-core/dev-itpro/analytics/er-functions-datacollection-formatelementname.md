---
title: ER-i funktsioon FORMATELEMENTNAME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FORMATELEMENTNAME.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561298"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="9efae-103">ER-i funktsioon FORMATELEMENTNAME</span><span class="sxs-lookup"><span data-stu-id="9efae-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9efae-104">Funktsioon `FORMATELEMENTNAME` tagastab *stringi* väärtuse, mis tähistab praeguse elektroonilise aruandluse (ER) vormingu elemendi nime.</span><span class="sxs-lookup"><span data-stu-id="9efae-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="9efae-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="9efae-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="9efae-106">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="9efae-106">Return values</span></span>

<span data-ttu-id="9efae-107">*String*</span><span class="sxs-lookup"><span data-stu-id="9efae-107">*String*</span></span>

<span data-ttu-id="9efae-108">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="9efae-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9efae-109">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="9efae-109">Usage notes</span></span>

<span data-ttu-id="9efae-110">Seda funktsiooni saab kutsuda ER-i avaldistes, mis konfigureeriti atribuutidele **Kogutud andmete võtme nimi** ja **Kogutud andmete võtme väärtus** ER-vormingu komponendile rühmast **Tekst**, mis paikneb komponendi **Üldine\\Fail** all, kus suvand **Kogu väljundi üksikasjad** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="9efae-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="9efae-111">Näide</span><span class="sxs-lookup"><span data-stu-id="9efae-111">Example</span></span>

<span data-ttu-id="9efae-112">Lisateavet selle funktsiooni kasutamise kohta vaadake tegevuse juhisest [ER-i loendamise ja liitmise vormingu väljundi kasutusandmed](tasks/er-format-counting-summing-1.md), mis on äriprotsessi **IT-teenuse/-lahenduse komponentide hankimine/arendamine** osa.</span><span class="sxs-lookup"><span data-stu-id="9efae-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9efae-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9efae-113">Additional resources</span></span>

[<span data-ttu-id="9efae-114">Andmete kogumise funktsioonid</span><span class="sxs-lookup"><span data-stu-id="9efae-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]