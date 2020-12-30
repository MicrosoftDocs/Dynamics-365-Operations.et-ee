---
title: ER-i funktsioon ALLITEMS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ALLITEMS.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15ab88512e49b51dbefa19056c3e1846715dcadb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687764"
---
# <a name="allitems-er-function"></a><span data-ttu-id="5da59-103">ER-i funktsioon ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="5da59-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5da59-104">Funktsioon `ALLITEMS` töötab mälusisese valikuna ja tagastab uue tasandatud *kirjete loendi* väärtuse kirjete loendina, mis tähistab kõiki määratud teele vastavaid üksuseid.</span><span class="sxs-lookup"><span data-stu-id="5da59-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da59-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="5da59-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="5da59-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="5da59-106">Arguments</span></span>

<span data-ttu-id="5da59-107">`path`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="5da59-107">`path`: *Record list*</span></span>

<span data-ttu-id="5da59-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="5da59-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5da59-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="5da59-109">Return values</span></span>

<span data-ttu-id="5da59-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="5da59-110">*Record list*</span></span>

<span data-ttu-id="5da59-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="5da59-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5da59-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="5da59-112">Usage notes</span></span>

<span data-ttu-id="5da59-113">Tee peab olema määratletud andmetüübi *Kirjete loend* andmeallika elemendi kehtiva andmeallika teena.</span><span class="sxs-lookup"><span data-stu-id="5da59-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="5da59-114">Andmeelemendid, nagu tee string või kuupäev, peaks elektroonilise aruandluse (ER) avaldisekoostajas andma koostamise ajal tõrke.</span><span class="sxs-lookup"><span data-stu-id="5da59-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="5da59-115">Seda funktsiooni ei ole soovitatav kandeandmete allikate puhul, mis võivad sisaldada suurt hulka andmeid.</span><span class="sxs-lookup"><span data-stu-id="5da59-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="5da59-116">Selle asemel kaaluge funktsiooni [ALLTEMSQUERY](er-functions-list-allitemsquery.md) kasutamist.</span><span class="sxs-lookup"><span data-stu-id="5da59-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="5da59-117">Näide 1</span><span class="sxs-lookup"><span data-stu-id="5da59-117">Example 1</span></span>

<span data-ttu-id="5da59-118">Kui sisestate olemi `SPLIT("abcdef" , 2)` andmeallikana **DS**, tagastab avaldis `COUNT( ALLITEMS (DS))` tulemuse **3**.</span><span class="sxs-lookup"><span data-stu-id="5da59-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="5da59-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="5da59-119">Example 2</span></span>

<span data-ttu-id="5da59-120">Kui sisestate suvandi **Hankija** andmetüübi *Kirjete loend* andmeallikana, mis viitab rakendustabelile VendTable, tagastab avaldis `ALLITEMS (Vend.'<Relations'.ContactPerson)` tasandatud kirjete loendi, millel on tabeli struktuur **ContactPerson** ja sisaldab kõiki kontaktisikuid, kellele on võimalik pääseda juurde seost **ContactPerson.ContactForParty == VendTable.Party** kasutades, ning mis on saadaval kõikidele viidatud hankijatabeli hankijatele.</span><span class="sxs-lookup"><span data-stu-id="5da59-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5da59-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5da59-121">Additional resources</span></span>

[<span data-ttu-id="5da59-122">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="5da59-122">List functions</span></span>](er-functions-category-list.md)
