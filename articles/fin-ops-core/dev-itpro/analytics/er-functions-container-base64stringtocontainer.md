---
title: ER-i funktsioon Base64StringToContainer
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni Base64StringToContainer.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739071"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="996db-103">ER-i funktsioon Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="996db-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="996db-104">[Funktsioon](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` teisendab tüübi *String* määratud sisendi tüübi *[Konteiner](er-functions-category-container.md)* andmeüksuseks.</span><span class="sxs-lookup"><span data-stu-id="996db-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="996db-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="996db-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="996db-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="996db-106">Arguments</span></span>

<span data-ttu-id="996db-107">`input`: *string*</span><span class="sxs-lookup"><span data-stu-id="996db-107">`input`: *String*</span></span>

<span data-ttu-id="996db-108">Tüübi *String* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="996db-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="996db-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="996db-109">Return values</span></span>

<span data-ttu-id="996db-110">*Konteiner*</span><span class="sxs-lookup"><span data-stu-id="996db-110">*Container*</span></span>

<span data-ttu-id="996db-111">Tulemuseks saadav kahendväärtus on binaarses suure objekti (BLOB) vormingus.</span><span class="sxs-lookup"><span data-stu-id="996db-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="996db-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="996db-112">Usage notes</span></span>

<span data-ttu-id="996db-113">Kui sisendstring ei esita õiget binaarsest tekstiks kodeerimisskeemi Base64 gruppi, tehakse erand „Parameeter on kehtetu”.</span><span class="sxs-lookup"><span data-stu-id="996db-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="996db-114">Näide</span><span class="sxs-lookup"><span data-stu-id="996db-114">Example</span></span>

<span data-ttu-id="996db-115">Määratlege oma mudelivastenduses järgmised andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="996db-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="996db-116">Andmeallika **DocuTypeGroupEnum** juur tüübil *Dynamics 365 for Operations / loetellu*, mis viitab rakenduse loetelule **DocuTypeGroup**</span><span class="sxs-lookup"><span data-stu-id="996db-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="996db-117">Andmeallika **Klient** juur tüübil *Dynamics 365 for Operations / tabelikirjed*, mis viitab rakenduse tabelile **CustTable**</span><span class="sxs-lookup"><span data-stu-id="996db-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="996db-118">Andmeallikas **\#Meedium** tüübil *Arvutatud väli*, mis on konfigureeritud järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="996db-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="996db-119">See on lisatud andmeallikale **Klient** alamandmeallikana.</span><span class="sxs-lookup"><span data-stu-id="996db-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="996db-120">See sisaldab avaldist `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="996db-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="996db-121">Andmeallikas **\#MediaAsBase64String** tüübil *Arvutatud väli*, mis on konfigureeritud järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="996db-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="996db-122">See on lisatud andmeallikale **Klient.'\#Meedium'** alamandmeallikana.</span><span class="sxs-lookup"><span data-stu-id="996db-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="996db-123">See sisaldab avaldist `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="996db-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="996db-124">Andmeallikas **\#BlobFomBase64** tüübil *Arvutatud väli*, mis on konfigureeritud järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="996db-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="996db-125">See on lisatud andmeallikale **Klient.'\#Meedium'** alamandmeallikana.</span><span class="sxs-lookup"><span data-stu-id="996db-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="996db-126">See sisaldab avaldist `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="996db-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="996db-127">Selles näites kodeerib andmeallikas **\#MediaAsBase64String** praeguse meediumi manuse binaarse sisu tekstina, mis tähistab binaarsest tekstiks kodeerimisskeemi Base64 gruppi.</span><span class="sxs-lookup"><span data-stu-id="996db-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="996db-128">Andmeallikas **\#BlobFomBase64** dekodeerib Base64 stringi ja tagastab binaarse väärtuse BLOB-vormingus.</span><span class="sxs-lookup"><span data-stu-id="996db-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Näidis andmeallikad ER-i mudeli vastenduse koostaja lehel](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="996db-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="996db-130">Additional resources</span></span>

[<span data-ttu-id="996db-131">Konteineri funktsioonid</span><span class="sxs-lookup"><span data-stu-id="996db-131">Container functions</span></span>](er-functions-category-container.md)