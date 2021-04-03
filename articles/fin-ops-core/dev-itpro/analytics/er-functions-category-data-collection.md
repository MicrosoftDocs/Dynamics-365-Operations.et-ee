---
title: ER-i funktsioonide loend andmete kogumise kategoorias
description: See teema annab teavet andmete kogumise funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba3a1f031a4a98592081b04a4128450aeb8218ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561730"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="77efb-103">ER-i funktsioonide loend andmete kogumise kategoorias</span><span class="sxs-lookup"><span data-stu-id="77efb-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77efb-104">Elektroonilise aruandluse (ER) andmete kogumise funktsioone kasutatakse, et loendada ja liita käitatav ER-vorming, mis põhineb juba **teksti** või **XML-i** vormingus loodud väljundi andmetel.</span><span class="sxs-lookup"><span data-stu-id="77efb-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="77efb-105">Seda varianti kasutatakse käitatud ER-vormingu jõudluse parandamiseks, loodud dokumentides jooksvate kogusummade väärtuste sisestamiseks ja muuks otstarbeks.</span><span class="sxs-lookup"><span data-stu-id="77efb-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="77efb-106">See teema sisaldab järgmiste funktsioonide kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="77efb-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="77efb-107">Toetatud funktsioonide loend</span><span class="sxs-lookup"><span data-stu-id="77efb-107">List of supported functions</span></span>

| <span data-ttu-id="77efb-108">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="77efb-108">Function</span></span> | <span data-ttu-id="77efb-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77efb-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="77efb-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="77efb-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="77efb-111">See funktsioon tagastab *kirjete loendi* väärtuse, mis sisaldab nende väärtuste loendit, mis on tagastatud vorminguelementide atribuudi **Kogutud andmete võtme väärtus** poolt ja kogutud, kui vorminguelemente kasutati väljamineva dokumendi loomisel vormingu käitamise ajal, ja mis vastab määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="77efb-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="77efb-112">Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="77efb-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="77efb-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="77efb-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="77efb-114">See funktsioon tagastab *täisarvu* väärtuse, mis tähistab vorminguelementide arvu, mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="77efb-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="77efb-115">See tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="77efb-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="77efb-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="77efb-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="77efb-117">See funktsioon tagastab *täisarvu* väärtuse, mis tähistab vorminguelementide arvu, mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="77efb-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="77efb-118">Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="77efb-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="77efb-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="77efb-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="77efb-120">See funktsioon tagastab *stringi* väärtuse, mis tähistab praeguse ER-vormingu elemendi nime.</span><span class="sxs-lookup"><span data-stu-id="77efb-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="77efb-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="77efb-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="77efb-122">See funktsioon tagastab *tegeliku* väärtuse, mis tähistab vorminguelementide sidumiste tagastatud väärtuste summat ja mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="77efb-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="77efb-123">See tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="77efb-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="77efb-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="77efb-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="77efb-125">See funktsioon tagastab *tegeliku* väärtuse, mis tähistab vorminguelementide sidumiste tagastatud väärtuste summat ja mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="77efb-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="77efb-126">Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest.</span><span class="sxs-lookup"><span data-stu-id="77efb-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="77efb-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="77efb-127">Additional resources</span></span>

[<span data-ttu-id="77efb-128">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="77efb-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="77efb-129">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="77efb-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="77efb-130">Elektroonilise aruandluse valemi keel</span><span class="sxs-lookup"><span data-stu-id="77efb-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]