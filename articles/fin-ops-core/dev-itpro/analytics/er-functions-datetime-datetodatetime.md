---
title: ER-i funktsioon DATETODATETIME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATETODATETIME.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 961ccd18e70d4f9851027492366a7d9408a668c5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042408"
---
# <span data-ttu-id="0c6b8-103"><a name="DATETODATETIME">ER-i funktsioon DATETODATETIME</a></span><span class="sxs-lookup"><span data-stu-id="0c6b8-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c6b8-104">Funktsioon `DATETODATETIME` tagastab *kuupäeva ja kellaaja* väärtuse, mis teisendatakse määratud kuupäeva väärtusest kuupäeva/kellaaja väärtuseks koordineeritud maailmaajas (Greenwichi aeg \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="0c6b8-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c6b8-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="0c6b8-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="0c6b8-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="0c6b8-106">Arguments</span></span>

<span data-ttu-id="0c6b8-107">`date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="0c6b8-107">`date`: *Date*</span></span>

<span data-ttu-id="0c6b8-108">Kuupäeva väärtus, mis tähistab teisendatavat kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="0c6b8-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c6b8-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="0c6b8-109">Return values</span></span>

<span data-ttu-id="0c6b8-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="0c6b8-110">*DateTime*</span></span>

<span data-ttu-id="0c6b8-111">Tulemiks saadud kuupäeva/kellaaja väärtus.</span><span class="sxs-lookup"><span data-stu-id="0c6b8-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0c6b8-112">Näide 1</span><span class="sxs-lookup"><span data-stu-id="0c6b8-112">Example 1</span></span>

<span data-ttu-id="0c6b8-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` tagastab jooksva Dynamics 365 Finance’i seansi 24. detsembril 2015 kujul **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="0c6b8-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="0c6b8-114">Selles näites on **CompInfo** tüübi **Finance and Operations / tabel** elektroonilise aruandluse (ER) andmeallikas ja see viitab tabelile CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="0c6b8-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="0c6b8-115">Näide 2</span><span class="sxs-lookup"><span data-stu-id="0c6b8-115">Example 2</span></span>

<span data-ttu-id="0c6b8-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` tagastab kuupäeva/kellaaja väärtuse **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="0c6b8-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c6b8-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0c6b8-117">Additional resources</span></span>

[<span data-ttu-id="0c6b8-118">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="0c6b8-118">Date and time functions</span></span>](er-functions-category-datetime.md)
