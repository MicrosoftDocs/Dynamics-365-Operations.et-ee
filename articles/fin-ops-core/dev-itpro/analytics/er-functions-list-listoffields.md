---
title: ER-i funktsioon LISTOFFIELDS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LISTOFFIELDS.
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
ms.openlocfilehash: 91e4658043278b9b8d73766cc0deac5d50d51a59
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916150"
---
# <span data-ttu-id="d4e42-103"><a name="LISTOFFIELDS">ER-i funktsioon LISTOFFIELDS</a></span><span class="sxs-lookup"><span data-stu-id="d4e42-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4e42-104">Funktsioon `LISTOFFIELDS` tagastab *kirjete loendi* väärtuse, mis luuakse tüübi *Loetelu* või *Konteiner (kirje)* määratud argumendi struktuuri põhjal.</span><span class="sxs-lookup"><span data-stu-id="d4e42-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d4e42-105">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="d4e42-105">Syntax 1</span></span>

```
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="d4e42-106">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="d4e42-106">Syntax 2</span></span>

```
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="d4e42-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="d4e42-107">Arguments</span></span>

<span data-ttu-id="d4e42-108">`path`: andmeallika viide</span><span class="sxs-lookup"><span data-stu-id="d4e42-108">`path`: Data source reference</span></span>

<span data-ttu-id="d4e42-109">Ühe järgmistest andmetüüpidest andmeallika kehtiv viitetee.</span><span class="sxs-lookup"><span data-stu-id="d4e42-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="d4e42-110">Mudeli loetelu</span><span class="sxs-lookup"><span data-stu-id="d4e42-110">Model enumeration</span></span>
- <span data-ttu-id="d4e42-111">Vormingu loetelu</span><span class="sxs-lookup"><span data-stu-id="d4e42-111">Format enumeration</span></span>
- <span data-ttu-id="d4e42-112">Rakenduse loetelu</span><span class="sxs-lookup"><span data-stu-id="d4e42-112">Application enumeration</span></span>
- <span data-ttu-id="d4e42-113">Konteiner (kirje)</span><span class="sxs-lookup"><span data-stu-id="d4e42-113">Container (record)</span></span>

<span data-ttu-id="d4e42-114">`language`: *string*</span><span class="sxs-lookup"><span data-stu-id="d4e42-114">`language`: *String*</span></span>

<span data-ttu-id="d4e42-115">Keele koodi tähistav tekst.</span><span class="sxs-lookup"><span data-stu-id="d4e42-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="d4e42-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="d4e42-116">Return values</span></span>

<span data-ttu-id="d4e42-117">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="d4e42-117">*Record list*</span></span>

<span data-ttu-id="d4e42-118">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="d4e42-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d4e42-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="d4e42-119">Usage notes</span></span>

<span data-ttu-id="d4e42-120">Loodud loend koosneb järgmiste väljadega kirjetest:</span><span class="sxs-lookup"><span data-stu-id="d4e42-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="d4e42-121">**Nimi** (andmetüüp *String*)</span><span class="sxs-lookup"><span data-stu-id="d4e42-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="d4e42-122">**Silt** (andmetüüp *String*)</span><span class="sxs-lookup"><span data-stu-id="d4e42-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="d4e42-123">**Kirjeldus** (andmetüüp *String*)</span><span class="sxs-lookup"><span data-stu-id="d4e42-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="d4e42-124">**IsTranslated** (andmetüüp *kahendmuutuja*)</span><span class="sxs-lookup"><span data-stu-id="d4e42-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="d4e42-125">Kui argument `path` viitab tüübi *Konteiner (kirje)* andmeallikale, lisatakse loodavasse loendisse iga viidatud konteineri kirje välja jaoks uus kirje.</span><span class="sxs-lookup"><span data-stu-id="d4e42-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="d4e42-126">Iga loodud kirje puhul tagastab väli **Nimi** välja nime viidatud konteineri kirje jaoks, mille jaoks praegune kirje loodi.</span><span class="sxs-lookup"><span data-stu-id="d4e42-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="d4e42-127">Kui argument `path` viitab ühele tüübi *Loetelu* andmeallikale, lisatakse loodavasse loendisse iga viidatud loendi loetelu väärtuse jaoks uus kirje.</span><span class="sxs-lookup"><span data-stu-id="d4e42-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="d4e42-128">Iga loodud kirje kohta tagastab väli **Nimi** viidatud loendi väärtuse, mille jaoks praegune kirje koostati, väli **Kirjeldus** tagastab selle loendi kirjelduse ja väli **Silt** tagastab selle loendi sildi.</span><span class="sxs-lookup"><span data-stu-id="d4e42-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="d4e42-129">Kui käitusajal kasutataks süntaksit 1, peavad väljad **Silt** ja **Kirjeldus** tagastama väärtused, mis põhinevad töötava elektroonilise aruandluse (ER) keelesätetel.</span><span class="sxs-lookup"><span data-stu-id="d4e42-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="d4e42-130">Kui taotletud keele sildid ja kirjeldused on saadaval, tagastavad väljad **Silt** ja **Kirjeldus** väärtused, mis põhinevad sellel keelel, ja väli **IsTranslated** tagastab väärtuse **True**.</span><span class="sxs-lookup"><span data-stu-id="d4e42-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="d4e42-131">Kui taotletud keele sildid ja kirjeldused ei ole saadaval, tagastavad väljad **Silt** ja **Kirjeldus** väärtused, mis põhinevad vaikekeelel **EN-US**, ja väli **IsTranslated** tagastab väärtuse **False**.</span><span class="sxs-lookup"><span data-stu-id="d4e42-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="d4e42-132">Kui käitusajal kasutataks süntaksit 2, peavad väljad **Silt** ja **Kirjeldus** tagastama väärtused, mis põhinevad keelel, mis on määratletud kutsutud funktsiooni teise argumendina.</span><span class="sxs-lookup"><span data-stu-id="d4e42-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="d4e42-133">Kui taotletud keele sildid ja kirjeldused on saadaval, tagastavad väljad **Silt** ja **Kirjeldus** väärtused, mis põhinevad sellel keelel, ja väli **IsTranslated** tagastab väärtuse **True**.</span><span class="sxs-lookup"><span data-stu-id="d4e42-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="d4e42-134">Kui taotletud keele sildid ja kirjeldused ei ole saadaval, tagastavad väljad **Silt** ja **Kirjeldus** väärtused, mis põhinevad keelel **EN-US**, ja väli **IsTranslated** tagastab väärtuse **False**.</span><span class="sxs-lookup"><span data-stu-id="d4e42-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="d4e42-135">Näide 1</span><span class="sxs-lookup"><span data-stu-id="d4e42-135">Example 1</span></span>

<span data-ttu-id="d4e42-136">Järgmises näites on ER-i andmemudelis kasutusele võetud loetelu.</span><span class="sxs-lookup"><span data-stu-id="d4e42-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="d4e42-137">Järgmises näites on toodud järgmised üksikasjad:</span><span class="sxs-lookup"><span data-stu-id="d4e42-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="d4e42-138">mudeli loetelu on aruandesse sisestatud andmeallikana;</span><span class="sxs-lookup"><span data-stu-id="d4e42-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="d4e42-139">ER-i avaldis kasutab mudeli loetelu funktsiooni `LISTOFFIELDS` parameetrina;</span><span class="sxs-lookup"><span data-stu-id="d4e42-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="d4e42-140">tüübi *Kirjete loend* andmeallikas on sisestatud aruandesse loodud ER-i avaldise abil.</span><span class="sxs-lookup"><span data-stu-id="d4e42-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="d4e42-141">Järgmises näites kirjeldatakse ER-i vormingu elemente, mis on seotud funktsiooniga `LISTOFFIELDS` loodud tüübi *Kirjete loend* andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="d4e42-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="d4e42-142">Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.</span><span class="sxs-lookup"><span data-stu-id="d4e42-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="d4e42-143">Siltide ja kirjelduste tõlgitud tekst sisestatakse ER-i vormingu väljundis vormingu peaelementide **FAIL** ja **KAUST** jaoks konfigureeritud keelesätete kohaselt.</span><span class="sxs-lookup"><span data-stu-id="d4e42-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="d4e42-144">Näide 2</span><span class="sxs-lookup"><span data-stu-id="d4e42-144">Example 2</span></span>

<span data-ttu-id="d4e42-145">Kasutate andmeallika tüüpi *Arvutatud väli* andmeallikate **enumType\_de** ja **enumTypede\_deCH** konfigureerimiseks andmemudeli loetelu **enumType** jaoks:</span><span class="sxs-lookup"><span data-stu-id="d4e42-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="d4e42-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="d4e42-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="d4e42-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="d4e42-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="d4e42-148">Sel juhul saate järgmist avaldist kasutada Šveitsi saksa keele loeteluväärtuse sildi saamiseks, kui see tõlge on olemas.</span><span class="sxs-lookup"><span data-stu-id="d4e42-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="d4e42-149">Kui šveitsi-saksa tõlge ei ole saadaval, on silt saksa keeles.</span><span class="sxs-lookup"><span data-stu-id="d4e42-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="d4e42-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d4e42-150">Additional resources</span></span>

[<span data-ttu-id="d4e42-151">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="d4e42-151">List functions</span></span>](er-functions-category-list.md)
