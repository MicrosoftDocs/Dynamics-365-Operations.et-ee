---
title: Sissetulevate dokumentide sõelumine JSON-vormingus
description: Selles teemas selgitatakse, kuidas seadistada elektroonilise aruandluse vorminguid, et sõeluda sissetulevad dokumente vormingus JavaScript Object Notation (JSON).
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703917"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="42f82-103">Sissetulevate dokumentide sõelumine JSON-vormingus</span><span class="sxs-lookup"><span data-stu-id="42f82-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="42f82-104">Saate kujundada elektroonilise aruandluse vormingud sõeluma sissetulevaid elektroonilisi dokumente, mis esitavad andmeid JavaScriptil põhinevas tekstivormingus (teisisõnu failid vormingus JavaScript Object Notation \[JSON\]).</span><span class="sxs-lookup"><span data-stu-id="42f82-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="42f82-105">Selle funktsiooni kohta lisateabe saamiseks laadige alla järgmises tabelis olevad failid ja seejärel esitage elektroonilise aruandluse vormingu konfiguratsiooni loomise importimiseks välisest JSON-failist tegevuse juhised.</span><span class="sxs-lookup"><span data-stu-id="42f82-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="42f82-106">Selles tegevuse juhises näidatakse, kuidas elektroonilise aruandluse vormingut saab kasutada sissetuleva JSON-faili sõelumiseks rakenduse andmete värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="42f82-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="42f82-107">Tiitel</span><span class="sxs-lookup"><span data-stu-id="42f82-107">Title</span></span>                                  | <span data-ttu-id="42f82-108">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="42f82-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="42f82-109">Elektroonilise aruandluse vormingu konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="42f82-109">ER format configuration</span></span>                | [<span data-ttu-id="42f82-110">Hankija kannete importimise vorming_JSON.xml</span><span class="sxs-lookup"><span data-stu-id="42f82-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="42f82-111">CSV-vormingus sissetuleva faili näidis</span><span class="sxs-lookup"><span data-stu-id="42f82-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="42f82-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="42f82-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="42f82-113">Nõuded</span><span class="sxs-lookup"><span data-stu-id="42f82-113">Requirements</span></span>

<span data-ttu-id="42f82-114">Enne elektroonilise aruandluse vormingu konfiguratsiooni loomise importimiseks välisest JSON-failist tegevuse juhiste lõpetamist peavad olema täidetud järgmised nõuded.</span><span class="sxs-lookup"><span data-stu-id="42f82-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="42f82-115">JSON-faili ülem-elemendid võivad olla ainult objekti elemendid.</span><span class="sxs-lookup"><span data-stu-id="42f82-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="42f82-116">Objekti pesastatud elemendid peaksid olema atribuudi elemendid, et luuakse kehtiv JSON-i struktuur.</span><span class="sxs-lookup"><span data-stu-id="42f82-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="42f82-117">JSON-massiivid võivad olla ainult objekti atribuudi elementide pesastatud elemendid.</span><span class="sxs-lookup"><span data-stu-id="42f82-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="42f82-118">JSON-massiivid võivad sisaldada ainult JSON-objekte.</span><span class="sxs-lookup"><span data-stu-id="42f82-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="42f82-119">Need ei saa sisaldada otseseid stringi/numbrilisi väärtusi ega pesastatud massiive.</span><span class="sxs-lookup"><span data-stu-id="42f82-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="42f82-120">Nende massiivide elemente sõelutakse järjekorras, nagu need on vormingus määratud.</span><span class="sxs-lookup"><span data-stu-id="42f82-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="42f82-121">Iga JSON-objekti puhul kaalutakse kordsuse sätteid.</span><span class="sxs-lookup"><span data-stu-id="42f82-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="42f82-122">Lisaks peate läbima tegevuse juhise [Vajalike konfiguratsioonide loomine välisest failist andmete importimiseks elektroonilise aruandluse jaoks](tasks/er-required-configurations-import-data.md), kui te pole seda veel läbinud..</span><span class="sxs-lookup"><span data-stu-id="42f82-122">Additionally, you must complete the [ER Create required configurations to import data from an external file for electronic reporting](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="42f82-123">Tegevuse juhise lõpuleviimiseks laadige alla järgmine fail.</span><span class="sxs-lookup"><span data-stu-id="42f82-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="42f82-124">Tiitel</span><span class="sxs-lookup"><span data-stu-id="42f82-124">Title</span></span>                  | <span data-ttu-id="42f82-125">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="42f82-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="42f82-126">Elektroonilise aruandluse mudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="42f82-126">ER model configuration</span></span> | [<span data-ttu-id="42f82-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="42f82-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
