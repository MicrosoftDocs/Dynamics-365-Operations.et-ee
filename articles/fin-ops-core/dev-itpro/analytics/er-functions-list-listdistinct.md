---
title: ER-i funktsioon LISTDISTINCT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LISTDISTINCT.
author: NickSelin
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 9ab9354b0fdb1c08c192b90e6bab303cb85ea41a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743819"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="04490-103">ER-i funktsioon LISTDISTINCT</span><span class="sxs-lookup"><span data-stu-id="04490-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="04490-104">Funktsioon `LISTDISTINCT` arvutab määratud avaldise valijana iga kirje jaoks, mis asub määratud loendis.</span><span class="sxs-lookup"><span data-stu-id="04490-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="04490-105">See tagastab uue väärtuse *Kirjete loend*, mis sisaldab ühte kirjet iga kordumatu valija väärtuse kohta.</span><span class="sxs-lookup"><span data-stu-id="04490-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="04490-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="04490-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="04490-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="04490-107">Arguments</span></span>

<span data-ttu-id="04490-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="04490-108">`list`: *Record list*</span></span>

<span data-ttu-id="04490-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="04490-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="04490-110">`selector`: *primitiivne andmetüüp*</span><span class="sxs-lookup"><span data-stu-id="04490-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="04490-111">Sobiv avaldis, mida kasutatakse valija väärtuse arvutamiseks määratud loendi iga kirje jaoks.</span><span class="sxs-lookup"><span data-stu-id="04490-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="04490-112">Selle parameetri puhul toetatakse järgmisi andmetüüpe.</span><span class="sxs-lookup"><span data-stu-id="04490-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="04490-113">Kahendmuutuja</span><span class="sxs-lookup"><span data-stu-id="04490-113">Boolean</span></span>
- <span data-ttu-id="04490-114">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="04490-114">Date</span></span>
- <span data-ttu-id="04490-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="04490-115">DateTime</span></span>
- <span data-ttu-id="04490-116">GUID</span><span class="sxs-lookup"><span data-stu-id="04490-116">GUID</span></span>
- <span data-ttu-id="04490-117">Täisarv</span><span class="sxs-lookup"><span data-stu-id="04490-117">Integer</span></span>
- <span data-ttu-id="04490-118">Int64</span><span class="sxs-lookup"><span data-stu-id="04490-118">Int64</span></span>
- <span data-ttu-id="04490-119">Tegelik</span><span class="sxs-lookup"><span data-stu-id="04490-119">Real</span></span>
- <span data-ttu-id="04490-120">String</span><span class="sxs-lookup"><span data-stu-id="04490-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="04490-121">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="04490-121">Return values</span></span>

<span data-ttu-id="04490-122">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="04490-122">*Record list*</span></span>

<span data-ttu-id="04490-123">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="04490-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="04490-124">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="04490-124">Usage notes</span></span>

<span data-ttu-id="04490-125">Loodud loendi struktuur ühtib määratud loendi struktuuriga.</span><span class="sxs-lookup"><span data-stu-id="04490-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="04490-126">Samasugust valija väärtust võib arvutada määratud loendis mitme kirje jaoks.</span><span class="sxs-lookup"><span data-stu-id="04490-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="04490-127">Sel juhul on loodud loendi asjaomase kirje väljade väärtused võrdsed määratud loendi esimese kirje väärtustega, mille jaoks valija väärtus arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="04490-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="04490-128">Seda funktsiooni kasutatakse kõikide [elektroonilise aruandluse (ER)](general-electronic-reporting.md) andmeallikate puhul, mille tüüp on *Kirjete loend* ja mis on mälus olemas.</span><span class="sxs-lookup"><span data-stu-id="04490-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="04490-129">Andmeallikat **GROUPBY** saab kasutada ka nende kirjete loendi loomiseks, mille jaoks arvutatakse eristatavate väärtustega valija.</span><span class="sxs-lookup"><span data-stu-id="04490-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="04490-130">Kuid jõudluse ja mälu tarbimise vaatenurgast on parem kasutada funktsiooni `LISTDISTINCT`, mitte andmeallikat **GROUBPY**, sest funktsioon käivitatakse mälus.</span><span class="sxs-lookup"><span data-stu-id="04490-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="04490-131">Näide</span><span class="sxs-lookup"><span data-stu-id="04490-131">Example</span></span>

<span data-ttu-id="04490-132">Järgmises näites on näha, kuidas saada loend kordumatutest kliendi kontonumbritest, millele on väljastatud kindla perioodi jooksul vähemalt üks müügi- või projektiarve.</span><span class="sxs-lookup"><span data-stu-id="04490-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="04490-133">Sisestage andmeallikas **SalesInvoice**, mille tüüp on `Record list` ning mis viitab rakendustabelile **CustInvoiceJour** ja filtreerib kindlate perioodide müügiarveid.</span><span class="sxs-lookup"><span data-stu-id="04490-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="04490-134">Selle andmeallika väli `InvoiceAccount` tagastab arveldatud kliendi kontonumbri.</span><span class="sxs-lookup"><span data-stu-id="04490-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="04490-135">Sisestage andmeallikas **ProjectInvoice**, mille tüüp on `Record list` ning mis viitab rakendustabelile **ProjInvoiceJour** ja filtreerib kindlate perioodide projektiarveid.</span><span class="sxs-lookup"><span data-stu-id="04490-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="04490-136">Selle andmeallika väli `InvoiceAccount` tagastab arveldatud kliendi kontonumbri.</span><span class="sxs-lookup"><span data-stu-id="04490-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="04490-137">Konfigureerige andmeallikas **AllInvoices**, mille tüüp on `Calculated field` ja mis sisaldab avaldist `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="04490-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="04490-138">See andmeallikas tagastab müügi- ja projektiarvete ühendatud loendi.</span><span class="sxs-lookup"><span data-stu-id="04490-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="04490-139">Konfigureerige andmeallikas **InvoicedCustomer**, mille tüüp on `Record list` ja mis sisaldab avaldist `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="04490-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="04490-140">See andmeallikas tagastab uue loendi, mis sisaldab ühte kirjet iga kordumatu kliendi kohta, kellega on perioodi jooksul arveldatud.</span><span class="sxs-lookup"><span data-stu-id="04490-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="04490-141">Selle loendi väli `InvoiceAccount` sisaldab kliendi kontonumbrit.</span><span class="sxs-lookup"><span data-stu-id="04490-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04490-142">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="04490-142">Additional resources</span></span>

[<span data-ttu-id="04490-143">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="04490-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]