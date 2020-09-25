---
title: ER-i funktsioon FORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni FORMAT.
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
ms.openlocfilehash: 3f3e8e5f6676c26b8d604ed950470463f04c0473
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743875"
---
# <a name="format-er-function"></a><span data-ttu-id="076b7-103">ER-i funktsioon FORMAT</span><span class="sxs-lookup"><span data-stu-id="076b7-103">FORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="076b7-104">Funktsioon `FORMAT` tagastab määratud stringi *stringi* väärtusena pärast seda, kui see vormindati, asendades **%N** esinemiskorrad *N.* argumendiga.</span><span class="sxs-lookup"><span data-stu-id="076b7-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="076b7-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="076b7-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="076b7-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="076b7-106">Arguments</span></span>

<span data-ttu-id="076b7-107">`string`: *string*</span><span class="sxs-lookup"><span data-stu-id="076b7-107">`string`: *String*</span></span>

<span data-ttu-id="076b7-108">Viide tüübi *String* andmeallikale, mis tuleb vormindada.</span><span class="sxs-lookup"><span data-stu-id="076b7-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="076b7-109">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="076b7-109">This argument is required.</span></span>

<span data-ttu-id="076b7-110">`argument 1`: *string*</span><span class="sxs-lookup"><span data-stu-id="076b7-110">`argument 1`: *String*</span></span>

<span data-ttu-id="076b7-111">Esimene argument, mida kasutatakse **%1** esinemiste asendamiseks.</span><span class="sxs-lookup"><span data-stu-id="076b7-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="076b7-112">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="076b7-112">This argument is required.</span></span>

<span data-ttu-id="076b7-113">`argument N`: *string*</span><span class="sxs-lookup"><span data-stu-id="076b7-113">`argument N`: *String*</span></span>

<span data-ttu-id="076b7-114">*N*. argument, mida kasutatakse **%2**, **%3** jne esinemiste asendamiseks.</span><span class="sxs-lookup"><span data-stu-id="076b7-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="076b7-115">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="076b7-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="076b7-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="076b7-116">Return values</span></span>

<span data-ttu-id="076b7-117">*String*</span><span class="sxs-lookup"><span data-stu-id="076b7-117">*String*</span></span>

<span data-ttu-id="076b7-118">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="076b7-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="076b7-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="076b7-119">Usage notes</span></span>

<span data-ttu-id="076b7-120">Kui parameetril ei ole argumenti, tagastatakse parameeter stringis kui **"%N"**.</span><span class="sxs-lookup"><span data-stu-id="076b7-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="076b7-121">Tüübi *Tõeline* väärtuste puhul on vaikimisi stringi teisendamine piiratud kahe kümnendkohaga.</span><span class="sxs-lookup"><span data-stu-id="076b7-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="076b7-122">Näide</span><span class="sxs-lookup"><span data-stu-id="076b7-122">Example</span></span>

<span data-ttu-id="076b7-123">Järgmisel joonisel tagastab andmeallikas **PaymentModel** kliendi kirjete loendi, kasutades komponenti **Klient**.</span><span class="sxs-lookup"><span data-stu-id="076b7-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="076b7-124">See tagastab töötlemiskuupäeva väärtuse, kasutades välja **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="076b7-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="076b7-125">Elektroonilise aruandluse (ER) vormingus, mis on mõeldud looma valitud klientidele elektroonilist faili, valitakse **PaymentModel** andmeallikana ja see juhib protsessi voogu.</span><span class="sxs-lookup"><span data-stu-id="076b7-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="076b7-126">Kui valitud klient on peatatud kuupäeval, millal aruannet töödeldaks, ilmub kasutaja teavitamiseks erand.</span><span class="sxs-lookup"><span data-stu-id="076b7-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="076b7-127">Seda tüüpi töötlemise juhtimiseks koostatud valem saab kasutada järgmisi ressursse.</span><span class="sxs-lookup"><span data-stu-id="076b7-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="076b7-128">Silt SYS70894, millel on järgmine tekst.</span><span class="sxs-lookup"><span data-stu-id="076b7-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="076b7-129">**Inglise keeles:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="076b7-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="076b7-130">**Saksa keeles:** Nichts zu drucken</span><span class="sxs-lookup"><span data-stu-id="076b7-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="076b7-131">Silt SYS18389, millel on järgmine tekst.</span><span class="sxs-lookup"><span data-stu-id="076b7-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="076b7-132">**USA inglise keeles:** „Customer %1 is stopped for %2.”</span><span class="sxs-lookup"><span data-stu-id="076b7-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="076b7-133">**Saksa keeles:** „Debitor '%1' wird für %2 gesperrt.”</span><span class="sxs-lookup"><span data-stu-id="076b7-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="076b7-134">Koostada saab järgmise avaldise.</span><span class="sxs-lookup"><span data-stu-id="076b7-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="076b7-135">Kui töödeldakse kliendi **Litware Retaili** aruannet 17. detsembril 2015 kultuuris **ET-EE** ja keeles **ET-EE**, annab see valem vastuseks järgmise teksti, mida saab kasutajale erandliku teatena esitada.</span><span class="sxs-lookup"><span data-stu-id="076b7-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="076b7-136">*Pole midagi printida. Litware Retaili klient on peatatud 17.12.2015.*</span><span class="sxs-lookup"><span data-stu-id="076b7-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="076b7-137">Kui sama aruannet töödeldakse kliendi **Litware Retail** jaoks 17. detsembril 2015 kultuuris **DE** ja keeles **DE**, tagastab valem järgmise teksti, mis kasutab erinevat andmevormingut:</span><span class="sxs-lookup"><span data-stu-id="076b7-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="076b7-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="076b7-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="076b7-139">Siltidele mõeldud ER-i valemites rakendatakse järgmist süntaksit.</span><span class="sxs-lookup"><span data-stu-id="076b7-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="076b7-140">**Rakenduse Microsoft Dynamics 365 Finance ressursside siltide puhul:** **\@X**, kus **X** on sildi ID rakendusobjektide puus (Application Object Tree (AOT))</span><span class="sxs-lookup"><span data-stu-id="076b7-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="076b7-141">**ER-i konfiguratsioonides asuvate siltide puhul:** **@„GER_LABEL:X”**, kus **X** on sildi ID ER-i konfiguratsioonis</span><span class="sxs-lookup"><span data-stu-id="076b7-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="076b7-142">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="076b7-142">Additional resources</span></span>

[<span data-ttu-id="076b7-143">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="076b7-143">Text functions</span></span>](er-functions-category-text.md)
