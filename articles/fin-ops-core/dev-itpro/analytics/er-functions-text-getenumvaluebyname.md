---
title: ER-i funktsioon GETENUMVALUEBYNAME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570586"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="92b17-103">ER-i funktsioon GETENUMVALUEBYNAME</span><span class="sxs-lookup"><span data-stu-id="92b17-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92b17-104">Funktsioon `GETENUMVALUEBYNAME` otsib määratud *loetelu* andmeallikast konkreetset loetelu väärtust, kasutades loendi nime, mis on määratud *stringi* väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="92b17-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="92b17-105">Kui *loetelu* väärtus leitakse, tagastab funktsioon selle.</span><span class="sxs-lookup"><span data-stu-id="92b17-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="92b17-106">Vastasel korral tagastab funktsioon loendamise väärtuse **null**.</span><span class="sxs-lookup"><span data-stu-id="92b17-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b17-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="92b17-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="92b17-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="92b17-108">Arguments</span></span>

<span data-ttu-id="92b17-109">`enumeration data source path`: *loetelu*</span><span class="sxs-lookup"><span data-stu-id="92b17-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="92b17-110">Ühe järgmistest loenditüüpidest andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="92b17-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="92b17-111">Elektroonilise aruandluse (ER) mudeli loetelu</span><span class="sxs-lookup"><span data-stu-id="92b17-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="92b17-112">ER-vormingu loetelu</span><span class="sxs-lookup"><span data-stu-id="92b17-112">ER format enumeration</span></span>
- <span data-ttu-id="92b17-113">Microsoft Dynamics 365 Finance’i loetelu</span><span class="sxs-lookup"><span data-stu-id="92b17-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="92b17-114">`enumeration value text`: *string*</span><span class="sxs-lookup"><span data-stu-id="92b17-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="92b17-115">Stringi väärtus, mis tähistab ühe loetelu väärtuse nime.</span><span class="sxs-lookup"><span data-stu-id="92b17-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="92b17-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="92b17-116">Return values</span></span>

<span data-ttu-id="92b17-117">Nullitav *loetelu*</span><span class="sxs-lookup"><span data-stu-id="92b17-117">Nullable *Enum*</span></span>

<span data-ttu-id="92b17-118">Tulemiks saadud loetelu väärtus.</span><span class="sxs-lookup"><span data-stu-id="92b17-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="92b17-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="92b17-119">Usage notes</span></span>

<span data-ttu-id="92b17-120">Ühtegi erandit ei esitata, kui väärtust *Loetelu* ei leita, kasutades loetelu väärtuse nime, mis on määratud *stringi* väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="92b17-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="92b17-121">Näide 1</span><span class="sxs-lookup"><span data-stu-id="92b17-121">Example 1</span></span>

<span data-ttu-id="92b17-122">Järgmises näites on andmemudelis kasutusele võetud loetelu **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="92b17-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="92b17-123">Pange tähele, et loetelu väärtuste puhul on määratletud sildid.</span><span class="sxs-lookup"><span data-stu-id="92b17-123">Notice that labels are defined for the enumeration values.</span></span>

![Andmemudeli loetelu jaoks saadaolevad väärtused](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="92b17-125">Järgmises näites on toodud järgmised üksikasjad:</span><span class="sxs-lookup"><span data-stu-id="92b17-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="92b17-126">Andmeallikas **$Direction** konfigureeritakse ER-i aruandes.</span><span class="sxs-lookup"><span data-stu-id="92b17-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="92b17-127">See andmeallikas konfigureeritakse mudeli **ReportDirection** loetelu põhjal.</span><span class="sxs-lookup"><span data-stu-id="92b17-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="92b17-128">Avaldis `$IsArrivals` on mõeldud kasutama mudeli loetelul põhinevat andmeallikat **$Direction** selle funktsiooni parameetrina.</span><span class="sxs-lookup"><span data-stu-id="92b17-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="92b17-129">Võrdluse avaldise väärtus on **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="92b17-129">The value of this comparison expression is **TRUE**.</span></span>

![Andmemudeli loetelu näide](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="92b17-131">Näide 2</span><span class="sxs-lookup"><span data-stu-id="92b17-131">Example 2</span></span>

<span data-ttu-id="92b17-132">Funktsioonid `GETENUMVALUEBYNAME` ja [`LISTOFFIELDS`](er-functions-list-listoffields.md) võimaldavad teil tuua toetatud loetelude väärtuseid ja silte tekstiväärtustena.</span><span class="sxs-lookup"><span data-stu-id="92b17-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="92b17-133">(Toetatud loetelud on rakenduse loetelud, andmemudeli loetelud ja vormingu loetelud.)</span><span class="sxs-lookup"><span data-stu-id="92b17-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="92b17-134">Järgmises näites on mudelivastenduses kasutusele võetud andmeallikas **TransType**.</span><span class="sxs-lookup"><span data-stu-id="92b17-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="92b17-135">See andmeallikas viitab rakenduse loetelule **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="92b17-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Mudelivastenduse andmeallikas, mis viitab rakenduse loetelule](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="92b17-137">Järgmises näites on näha andmeallikas **TransTypeList**, mis on konfigureeritud mudelivastenduses.</span><span class="sxs-lookup"><span data-stu-id="92b17-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="92b17-138">See andmeallikas konfigureeritakse rakenduse loetelu **TransType** põhjal.</span><span class="sxs-lookup"><span data-stu-id="92b17-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="92b17-139">Funktsiooni `LISTOFFIELDS` kasutatakse selleks, et tagastada kõik loetelu väärtused välju sisaldavate kirjete loendina.</span><span class="sxs-lookup"><span data-stu-id="92b17-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="92b17-140">Sel viisil on iga loetelu väärtuse üksikasjad nähtaval.</span><span class="sxs-lookup"><span data-stu-id="92b17-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="92b17-141">Väli **EnumValue** konfigureeritakse andmeallika **TransTypeList** jaoks avaldise `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` abil.</span><span class="sxs-lookup"><span data-stu-id="92b17-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="92b17-142">See väli tagastab loetelu väärtuse iga selles loendis oleva kirje jaoks.</span><span class="sxs-lookup"><span data-stu-id="92b17-142">This field returns an enumeration value for every record in this list.</span></span>

![Mudelivastenduse andmeallikas, mis tagastab valitud loetelu kõik loetelu väärtused kirjete loendina](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="92b17-144">Järgmises näites on näha andmeallikas **VendTrans**, mis on konfigureeritud mudelivastenduses.</span><span class="sxs-lookup"><span data-stu-id="92b17-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="92b17-145">See andmeallikas tagastab rakenduse tabelist **VendTrans** pärit hankija kandekirjed.</span><span class="sxs-lookup"><span data-stu-id="92b17-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="92b17-146">Iga kande pearaamatu tüüp määratletakse välja **TransType** väärtuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="92b17-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="92b17-147">Väli **TransTypeTitle** konfigureeritakse andmeallika **VendTrans** jaoks avaldise `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` abil.</span><span class="sxs-lookup"><span data-stu-id="92b17-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="92b17-148">See väli tagastab praeguse kande loetelu väärtuse sildi tekstina, kui see loetelu väärtus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92b17-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="92b17-149">Muidu tagastatakse tühja stringi väärtus.</span><span class="sxs-lookup"><span data-stu-id="92b17-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="92b17-150">Väli **TransTypeTitle** on seotud väljaga **LedgerType**, mis kuulub andmemudelisse, mis võimaldab seda teavet kasutada igas ER-i vormingus, mis kasutab seda andmemudelit andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="92b17-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Mudelivastenduse andmeallikas, mis tagastab hankija kanded](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="92b17-152">Järgmisel joonisel on näha, kuidas saate kasutada [andmeallika silurit](er-debug-data-sources.md) konfigureeritud mudelivastenduse testimiseks.</span><span class="sxs-lookup"><span data-stu-id="92b17-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Andmeallika siluri kasutamine konfigureeritud mudelivastenduse testimiseks](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="92b17-154">Andmeallika väli **LedgerType** muudab kandetüüpide sildid ootuspäraselt nähtavaks.</span><span class="sxs-lookup"><span data-stu-id="92b17-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="92b17-155">Kui kavatsete kasutada seda meetodit suure hulga kandeandmete jaoks, peate võtma arvesse käitamise jõudlust.</span><span class="sxs-lookup"><span data-stu-id="92b17-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="92b17-156">Lisateavet leiate teemast [Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="92b17-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92b17-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="92b17-157">Additional resources</span></span>

[<span data-ttu-id="92b17-158">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="92b17-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="92b17-159">Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsinguks</span><span class="sxs-lookup"><span data-stu-id="92b17-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="92b17-160">ER-i funktsioon LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="92b17-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="92b17-161">ER-i funktsioon FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="92b17-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="92b17-162">ER-i funktsioon WHERE</span><span class="sxs-lookup"><span data-stu-id="92b17-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]