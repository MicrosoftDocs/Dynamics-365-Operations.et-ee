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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79c43b6ecdb307433b0c2091840c21a5ada3a689
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917438"
---
# <span data-ttu-id="c1350-103"><a name="ALLITEMS">ER-i funktsioon ALLITEMS</a></span><span class="sxs-lookup"><span data-stu-id="c1350-103"><a name="ALLITEMS">ALLITEMS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1350-104">Funktsioon `ALLITEMS` töötab mälusisese valikuna ja tagastab uue tasandatud *kirjete loendi* väärtuse kirjete loendina, mis tähistab kõiki määratud teele vastavaid üksuseid.</span><span class="sxs-lookup"><span data-stu-id="c1350-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1350-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="c1350-105">Syntax</span></span>

```
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="c1350-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="c1350-106">Arguments</span></span>

<span data-ttu-id="c1350-107">`path`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="c1350-107">`path`: *Record list*</span></span>

<span data-ttu-id="c1350-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="c1350-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c1350-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="c1350-109">Return values</span></span>

<span data-ttu-id="c1350-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="c1350-110">*Record list*</span></span>

<span data-ttu-id="c1350-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="c1350-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c1350-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="c1350-112">Usage notes</span></span>

<span data-ttu-id="c1350-113">Tee peab olema määratletud andmetüübi *Kirjete loend* andmeallika elemendi kehtiva andmeallika teena.</span><span class="sxs-lookup"><span data-stu-id="c1350-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="c1350-114">Andmeelemendid, nagu tee string või kuupäev, peaks elektroonilise aruandluse (ER) avaldisekoostajas andma koostamise ajal tõrke.</span><span class="sxs-lookup"><span data-stu-id="c1350-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="c1350-115">Seda funktsiooni ei ole soovitatav kandeandmete allikate puhul, mis võivad sisaldada suurt hulka andmeid.</span><span class="sxs-lookup"><span data-stu-id="c1350-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="c1350-116">Selle asemel kaaluge funktsiooni [ALLTEMSQUERY](er-functions-list-allitemsquery.md) kasutamist.</span><span class="sxs-lookup"><span data-stu-id="c1350-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="c1350-117">Näide 1</span><span class="sxs-lookup"><span data-stu-id="c1350-117">Example 1</span></span>

<span data-ttu-id="c1350-118">Kui sisestate olemi `SPLIT("abcdef" , 2)` andmeallikana **DS**, tagastab avaldis `COUNT( ALLITEMS (DS))` tulemuse **3**.</span><span class="sxs-lookup"><span data-stu-id="c1350-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c1350-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="c1350-119">Example 2</span></span>

<span data-ttu-id="c1350-120">Kui sisestate suvandi **Hankija** andmetüübi *Kirjete loend* andmeallikana, mis viitab rakendustabelile VendTable, tagastab avaldis `ALLITEMS (Vend.'<Relations'.ContactPerson)` tasandatud kirjete loendi, millel on tabeli struktuur **ContactPerson** ja sisaldab kõiki kontaktisikuid, kellele on võimalik pääseda juurde seost **ContactPerson.ContactForParty == VendTable.Party** kasutades, ning mis on saadaval kõikidele viidatud hankijatabeli hankijatele.</span><span class="sxs-lookup"><span data-stu-id="c1350-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1350-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c1350-121">Additional resources</span></span>

[<span data-ttu-id="c1350-122">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="c1350-122">List functions</span></span>](er-functions-category-list.md)
