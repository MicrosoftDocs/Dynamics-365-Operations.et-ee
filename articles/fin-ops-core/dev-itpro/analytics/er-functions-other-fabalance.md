---
title: ER-i funktsioon FA_BALANCE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FA_BALANCE.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916012"
---
# <span data-ttu-id="8a324-103"><a name="FA_BALANCE">ER-i funktsioon FA_BALANCE</a></span><span class="sxs-lookup"><span data-stu-id="8a324-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a324-104">Funktsioon `FA_BALANCE` tagastab *konteineri (kirje)* väärtuse, mis koosneb põhivara saldo andmetest määratud põhivara kauba, väärtusmudeli koodi, aruandeaasta ja aruandluse kuupäeva kohta.</span><span class="sxs-lookup"><span data-stu-id="8a324-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a324-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="8a324-105">Syntax</span></span>

```
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="8a324-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="8a324-106">Arguments</span></span>

<span data-ttu-id="8a324-107">`fixed asset code`: *string*</span><span class="sxs-lookup"><span data-stu-id="8a324-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="8a324-108">*Stringi* väärtus, mis tähistab põhivara kauba koodi, mille jaoks saldo arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="8a324-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="8a324-109">`value model code`: *string*</span><span class="sxs-lookup"><span data-stu-id="8a324-109">`value model code`: *String*</span></span>

<span data-ttu-id="8a324-110">*Stringi* väärtus, mis tähistab väärtusmudeli koodi, mille jaoks saldo arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="8a324-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="8a324-111">`reporting year`: *loetelu väärtus*</span><span class="sxs-lookup"><span data-stu-id="8a324-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="8a324-112">Rakenduse loetelu **AssetYear** loendamise väärtus, mis määratleb saldo arvutamise perioodi.</span><span class="sxs-lookup"><span data-stu-id="8a324-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="8a324-113">`reporting date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="8a324-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="8a324-114">*Kuupäeva* väärtus, mis määratleb saldo arvutamise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="8a324-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="8a324-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="8a324-115">Return values</span></span>

<span data-ttu-id="8a324-116">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="8a324-116">*Container (record)*</span></span>

<span data-ttu-id="8a324-117">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="8a324-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="8a324-118">Näide</span><span class="sxs-lookup"><span data-stu-id="8a324-118">Example</span></span>

<span data-ttu-id="8a324-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` annab vastuseks põhivara **COMP-000001** väärtusmudeli **Praegune** jaoks ette valmistatud saldode andmekonteineri praegusel rakenduse seansi kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="8a324-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a324-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8a324-120">Additional resources</span></span>

[<span data-ttu-id="8a324-121">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="8a324-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)