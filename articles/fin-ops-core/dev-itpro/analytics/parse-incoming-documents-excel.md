---
title: Sissetulevate dokumentide sõelumine Excelis vormingus
description: Selles teemas selgitatakse elektroonilise aruandluse vormingute kujundamist sissetulevates Microsoft Exceli failides oleva sisu sõelumiseks.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
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
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3f83271327df186d407516ff1a197800ffc8c78c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249352"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="fa7d1-103">Sissetulevate dokumentide sõelumine Exceli vormingus</span><span class="sxs-lookup"><span data-stu-id="fa7d1-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fa7d1-104">Saate kujundada elektroonilise aruandluse vormingud sõeluma sissetulevaid Microsoft Exceli faile, mis esitavad andmeid Microsoft Exceli töövihikutes (XLSX-vormingus failid).</span><span class="sxs-lookup"><span data-stu-id="fa7d1-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="fa7d1-105">Seejärel saate neist failidest pärit sisu kasutada rakenduse andmete värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="fa7d1-106">See on kasulik järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-106">This is useful if you:</span></span>

- <span data-ttu-id="fa7d1-107">Uue mudeli ja vormingu kujundamine, testides neid käitusajal.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="fa7d1-108">Sellisel juhul simuleerib Excel tegelikke rakenduse andmeid.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="fa7d1-109">Lisaks rakenduse Exceli andmete haldamiseks ja soovite importida kindla aruande andmed.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="fa7d1-110">Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusjuhiseid **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist (1. osa: vormingu kujundamine)** ja **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist (2. osa: andmete importimine)** (osad äriprotsessist 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)).</span><span class="sxs-lookup"><span data-stu-id="fa7d1-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="fa7d1-111">Need tegevusejuhised selgitavad, kuidas saab sissetulevat Exceli faili elektroonilise aruandluse vormingu abil sõeluda, et importida teavet sissetulevatest dokumentidest ja värskendada rakenduse andmeid.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="fa7d1-112">Saate tegevusejuhise failid alla laadida [Microsofti allalaadimiskeskusse](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="fa7d1-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="fa7d1-113">Eespool nimetatud tegevusejuhiste lõpuleviimiseks laadige alla järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="fa7d1-114">Sisu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fa7d1-114">Content description</span></span>                         | <span data-ttu-id="fa7d1-115">Fail</span><span class="sxs-lookup"><span data-stu-id="fa7d1-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="fa7d1-116">Sissetulev fail XLSX-vormingus – mall</span><span class="sxs-lookup"><span data-stu-id="fa7d1-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="fa7d1-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="fa7d1-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="fa7d1-118">Sissetulev fail XLSX-vormingus – näidisandmed</span><span class="sxs-lookup"><span data-stu-id="fa7d1-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="fa7d1-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="fa7d1-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="fa7d1-120">Kui te pole järgmist tegevusejuhist, [Elektrooniline aruandlus: nõutud konfiguratsioonide loomine andmete importimiseks välisest failist](./tasks/er-required-configurations-import-data.md), praeguses rakenduses Finance and Operation veel vaadanud, laadige alla järgmine fail.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="fa7d1-121">Sisu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fa7d1-121">Content description</span></span>    | <span data-ttu-id="fa7d1-122">Fail</span><span class="sxs-lookup"><span data-stu-id="fa7d1-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="fa7d1-123">Elektroonilise aruandluse mudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="fa7d1-123">ER model configuration</span></span> | [<span data-ttu-id="fa7d1-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="fa7d1-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |