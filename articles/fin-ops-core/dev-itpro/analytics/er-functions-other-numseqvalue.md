---
title: ER-i funktsioon NUMSEQVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMSEQVALUE.
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
ms.openlocfilehash: d68784524a5639d8d447daa2cda940680d795542
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915828"
---
# <span data-ttu-id="fb07e-103"><a name="NUMSEQVALUE">ER-i funktsioon NUMSEQVALUE</a></span><span class="sxs-lookup"><span data-stu-id="fb07e-103"><a name="NUMSEQVALUE">NUMSEQVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb07e-104">Funktsioon `NUMSEQVALUE` tagastab *stringi* väärtuse, mis tähistab numbriseeria uue loodud väärtuse, põhinedes määratletud numbriseerial, ulatusel ja ulatuse ID-l.</span><span class="sxs-lookup"><span data-stu-id="fb07e-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="fb07e-105">Ulatuse ID on võrdne ettevõtte koodiga, mille varustab elektroonilise aruandluse (ER) vormingu käitamise kontekst.</span><span class="sxs-lookup"><span data-stu-id="fb07e-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="fb07e-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="fb07e-106">Syntax 1</span></span>

```
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="fb07e-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="fb07e-107">Syntax 2</span></span>

```
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="fb07e-108">Süntaks 3</span><span class="sxs-lookup"><span data-stu-id="fb07e-108">Syntax 3</span></span>

```
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="fb07e-109">Argumendid</span><span class="sxs-lookup"><span data-stu-id="fb07e-109">Arguments</span></span>

<span data-ttu-id="fb07e-110">`number sequence code`: *string*</span><span class="sxs-lookup"><span data-stu-id="fb07e-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="fb07e-111">Teksti väärtus, mis tähistab numbriseeria koodi, milles on nõutav uus väärtus.</span><span class="sxs-lookup"><span data-stu-id="fb07e-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="fb07e-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="fb07e-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="fb07e-113">Väärtus *Int64*, mis tähistab kirje kirde ID-d tabelis NumberSequenceTable, mis sisaldab numbriseeria definitsiooni, milles on nõutav uus väärtus.</span><span class="sxs-lookup"><span data-stu-id="fb07e-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="fb07e-114">`scope type`: *loetelu väärtus*</span><span class="sxs-lookup"><span data-stu-id="fb07e-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="fb07e-115">Loetelu **ERExpressionNumberSequenceScopeType** loetelu väärtus, mis määratleb numbriseeria ulatuse, milles on nõutav uus väärtus.</span><span class="sxs-lookup"><span data-stu-id="fb07e-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="fb07e-116">Saadaolevad ulatuse tüübid on **Ühiskasutuses**, **Juriidiline isiku**ja **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="fb07e-117">`scope ID`: *string*</span><span class="sxs-lookup"><span data-stu-id="fb07e-117">`scope ID`: *String*</span></span>

<span data-ttu-id="fb07e-118">*Stringi* väärtus, mis tuvastab määratud ulatuse tüübi põhjal ulatuse.</span><span class="sxs-lookup"><span data-stu-id="fb07e-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb07e-119">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="fb07e-119">Return values</span></span>

<span data-ttu-id="fb07e-120">*String*</span><span class="sxs-lookup"><span data-stu-id="fb07e-120">*String*</span></span>

<span data-ttu-id="fb07e-121">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="fb07e-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fb07e-122">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="fb07e-122">Usage notes</span></span>

<span data-ttu-id="fb07e-123">Määratlege ülatuse tüübi **Ühiskasutuses** jaoks tühi string ulatuse ID-ks.</span><span class="sxs-lookup"><span data-stu-id="fb07e-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="fb07e-124">Määratlege ulatuse tüüpide **Ettevõtte** ja **Juriidiline isik** jaoks ettevõtte kood ulatuse ID-ks.</span><span class="sxs-lookup"><span data-stu-id="fb07e-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="fb07e-125">Kui määratlete nendele ulatuse tüüpidele ulatuse ID-ks tühja stringi, kasutatakse praegust ettevõtte koodi.</span><span class="sxs-lookup"><span data-stu-id="fb07e-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="fb07e-126">Kui kasutatakse süntaksit 1, taotletakse ulatuse tüübile **Ettevõte** numbriseeriat ja ettevõtte kood tuleb kontekstist, kus ER-vormingut käitatakse.</span><span class="sxs-lookup"><span data-stu-id="fb07e-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="fb07e-127">Näide 1</span><span class="sxs-lookup"><span data-stu-id="fb07e-127">Example 1</span></span>

<span data-ttu-id="fb07e-128">Oma ER-vormingus määratlete tüübi *Kasutaja sisendparameeter* andmeallika **AskNumSeq**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="fb07e-129">See andmeallikas viitab laiendatud andmetüübile (EDT) **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="fb07e-130">Järgmisena määratlete tüübi *Arvutatud väli* andmeallika **NumSeq**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="fb07e-131">See andmeallikas sisaldab avaldist `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="fb07e-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="fb07e-132">Kui kutsutakse andmeallikat **NumSeq**, tagastab see numbriseeria uue loodud väärtuse, mis määrati käitusajal, sisestades selle koodi dialoogiboksi.</span><span class="sxs-lookup"><span data-stu-id="fb07e-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="fb07e-133">Numbriseeriat taotletakse ulatuse tüübile **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="fb07e-134">Ettevõtte koodi varustab ER-vormingu käitamise kontekst.</span><span class="sxs-lookup"><span data-stu-id="fb07e-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="fb07e-135">Näide 2</span><span class="sxs-lookup"><span data-stu-id="fb07e-135">Example 2</span></span>

<span data-ttu-id="fb07e-136">Teie mudelivastenduses on määratletud järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="fb07e-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="fb07e-137">Tüübi *Tabel* andmeallikas **LedgerParms**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="fb07e-138">See andmeallikas viitab tabelile LedgerParameters.</span><span class="sxs-lookup"><span data-stu-id="fb07e-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="fb07e-139">Tüübi *Arvutatud väli* andmeallikas **NumSeq**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="fb07e-140">See andmeallikas sisaldab avaldist `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="fb07e-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="fb07e-141">Kui kutsutakse **NumSeq** andmeallikat, tagastatakse numbriseeria uus loodud väärtus, mis on konfigureeritud pearaamatu parameetrites selle ettevõtte jaoks, mis varustab ER-vormingu käitamise konteksti.</span><span class="sxs-lookup"><span data-stu-id="fb07e-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="fb07e-142">See numbriseeria tuvastab kordumatult töölehed ja toimingud partiinumbrina, mis seob kanded omavahel.</span><span class="sxs-lookup"><span data-stu-id="fb07e-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="fb07e-143">Näide 3</span><span class="sxs-lookup"><span data-stu-id="fb07e-143">Example 3</span></span>

<span data-ttu-id="fb07e-144">Teie mudelivastenduses on määratletud järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="fb07e-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="fb07e-145">Teenuse Microsoft Dynamics 365 Finance *loetelu* tüübi andmeallikas **enumScope**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="fb07e-146">See andmeallikas viitab laiendatud loetelule **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="fb07e-147">Tüübi *Arvutatud väli* andmeallikas **NumSeq**.</span><span class="sxs-lookup"><span data-stu-id="fb07e-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="fb07e-148">See andmeallikas sisaldab avaldist `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="fb07e-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="fb07e-149">Kui kutsutakse **NumSeq** andmeallikat, tagastatakse numbriseeria **Gene\_1** uus loodud väärtus, mis on konfigureeritud selle ettevõtte jaoks, mis varustab ER-vormingu käitamise konteksti.</span><span class="sxs-lookup"><span data-stu-id="fb07e-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb07e-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fb07e-150">Additional resources</span></span>

[<span data-ttu-id="fb07e-151">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="fb07e-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
