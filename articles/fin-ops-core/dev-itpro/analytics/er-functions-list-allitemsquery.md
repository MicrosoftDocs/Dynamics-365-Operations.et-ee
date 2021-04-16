---
title: ER-i funktsioon ALLITEMSQUERY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ALLITEMSQUERY.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 7995b497a2bd95d4aec9ae6d5f1c3cb790823ea0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746695"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="bf692-103">ER-i funktsioon ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="bf692-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf692-104">Funktsioon `ALLITEMSQUERY` töötab liidetud SQL-päringuna.</span><span class="sxs-lookup"><span data-stu-id="bf692-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="bf692-105">See tagastab uue tasandatud *kirjete loendi* väärtuse, mis koosneb kirjete, mis tähistavad kõiki määratud teele vastavaid üksuseid, loendist.</span><span class="sxs-lookup"><span data-stu-id="bf692-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf692-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="bf692-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="bf692-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="bf692-107">Arguments</span></span>

<span data-ttu-id="bf692-108">`path`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="bf692-108">`path`: *Record list*</span></span>

<span data-ttu-id="bf692-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="bf692-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="bf692-110">See peab sisaldama vähemalt ühte seost.</span><span class="sxs-lookup"><span data-stu-id="bf692-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="bf692-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="bf692-111">Return values</span></span>

<span data-ttu-id="bf692-112">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="bf692-112">*Record list*</span></span>

<span data-ttu-id="bf692-113">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="bf692-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bf692-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="bf692-114">Usage notes</span></span>

<span data-ttu-id="bf692-115">Määratud tee peab olema määratletud andmetüübi *Kirjete loend* andmeallika elemendi kehtiva andmeallika teena.</span><span class="sxs-lookup"><span data-stu-id="bf692-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="bf692-116">Lisaks peab see sisaldama vähemalt ühte seost.</span><span class="sxs-lookup"><span data-stu-id="bf692-116">It must also contain at least one relation.</span></span> <span data-ttu-id="bf692-117">Andmeelemendid, nagu tee *string* või *kuupäev*, peaks elektroonilise aruandluse (ER) avaldisekoostajas andma koostamise ajal tõrke.</span><span class="sxs-lookup"><span data-stu-id="bf692-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="bf692-118">Kui seda funktsiooni rakendatakse andmetüübi *Kirjete loend* andmeallikatele, mis viitavad rakendusobjektile, mida saab SQL-i abil otse kutsuda (nt tabel, üksus või päring), töötab see ühendatud SQL-päringuna.</span><span class="sxs-lookup"><span data-stu-id="bf692-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="bf692-119">Vastasel juhul töötab see mälus funktsioonina [ALLITEMS](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="bf692-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="bf692-120">Näide</span><span class="sxs-lookup"><span data-stu-id="bf692-120">Example</span></span>

<span data-ttu-id="bf692-121">Määratlege oma mudelivastenduses järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="bf692-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="bf692-122">Tüübi **Tabelikirjed** andmeallikas *CustInv*, mis viitab tabelile CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="bf692-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="bf692-123">Tüübi *Arvutatud väli* andmeallikas **FilteredInv**, mis sisaldab avaldist `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="bf692-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="bf692-124">Tüübi *Arvutatud väli* andmeallikas **JourLines**, mis sisaldab avaldist `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="bf692-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="bf692-125">Kui käitate mudelivastenduse andmeallika **JourLines** poole pöördumiseks, käivitatakse järgmine SQL-avaldis.</span><span class="sxs-lookup"><span data-stu-id="bf692-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="bf692-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="bf692-126">Additional resources</span></span>

[<span data-ttu-id="bf692-127">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="bf692-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]