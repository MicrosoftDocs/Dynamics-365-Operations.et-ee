---
title: ER-i funktsioon NULLDATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NULLDATE.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563458"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="409ec-103">ER-i funktsioon NULLDATE</span><span class="sxs-lookup"><span data-stu-id="409ec-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="409ec-104">Funktsioon `NULLDATE` tagastab *kuupäeva* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuar 1900).</span><span class="sxs-lookup"><span data-stu-id="409ec-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="409ec-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="409ec-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="409ec-106">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="409ec-106">Return values</span></span>

<span data-ttu-id="409ec-107">*Kuupäev*</span><span class="sxs-lookup"><span data-stu-id="409ec-107">*Date*</span></span>

<span data-ttu-id="409ec-108">Tulemiks saadud kuupäeva väärtus.</span><span class="sxs-lookup"><span data-stu-id="409ec-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="409ec-109">Näide 1</span><span class="sxs-lookup"><span data-stu-id="409ec-109">Example 1</span></span>

<span data-ttu-id="409ec-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` tagastab kuupäeva **null** (1. jaanuar 1900) kujul **„1900-01-01”**, mis põhineb määratletud kohandatud vormingul.</span><span class="sxs-lookup"><span data-stu-id="409ec-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="409ec-111">Näide 2</span><span class="sxs-lookup"><span data-stu-id="409ec-111">Example 2</span></span>

<span data-ttu-id="409ec-112">Avaldis `IF( Invoice.DocumentDate = NULLDATE(), true, false)` tagastab väärtuse **tõene**, kui välja **DocumentDate** väärtus on võrdne kuupäevaga **null**.</span><span class="sxs-lookup"><span data-stu-id="409ec-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="409ec-113">Selles näites on **Invoice** tüübi **Finance / tabeli kirjed** elektrilise aruandluse (ER) andmeallikas ja see viitab tabelile CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="409ec-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="409ec-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="409ec-114">Additional resources</span></span>

[<span data-ttu-id="409ec-115">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="409ec-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]