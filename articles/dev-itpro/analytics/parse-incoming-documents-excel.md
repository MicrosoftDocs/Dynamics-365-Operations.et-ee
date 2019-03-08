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
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "367474"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="f6347-103">Sissetulevate dokumentide sõelumine Exceli vormingus</span><span class="sxs-lookup"><span data-stu-id="f6347-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f6347-104">Saate kujundada elektroonilise aruandluse vormingud sõeluma sissetulevaid Microsoft Exceli faile, mis esitavad andmeid Microsoft Exceli töövihikutes (XLSX-vormingus failid).</span><span class="sxs-lookup"><span data-stu-id="f6347-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="f6347-105">Seejärel saate neist failidest pärit sisu kasutada rakenduse andmete värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="f6347-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="f6347-106">See on kasulik järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="f6347-106">This is useful if you:</span></span>

- <span data-ttu-id="f6347-107">Uue mudeli ja vormingu kujundamine, testides neid käitusajal.</span><span class="sxs-lookup"><span data-stu-id="f6347-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="f6347-108">Sellisel juhul simuleerib Excel tegelikke rakenduse andmeid.</span><span class="sxs-lookup"><span data-stu-id="f6347-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="f6347-109">Lisaks rakenduse Exceli andmete haldamiseks ja soovite importida kindla aruande andmed.</span><span class="sxs-lookup"><span data-stu-id="f6347-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="f6347-110">Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusjuhiseid **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist (1. osa: vormingu kujundamine)** ja **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist (2. osa: andmete importimine)** (osad äriprotsessist 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)).</span><span class="sxs-lookup"><span data-stu-id="f6347-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="f6347-111">Need tegevusejuhised selgitavad, kuidas saab sissetulevat Exceli faili elektroonilise aruandluse vormingu abil sõeluda, et importida teavet sissetulevatest dokumentidest ja värskendada rakenduse andmeid.</span><span class="sxs-lookup"><span data-stu-id="f6347-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="f6347-112">Saate tegevusejuhise failid alla laadida [Microsofti allalaadimiskeskusse](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="f6347-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="f6347-113">Eespool nimetatud tegevusejuhiste lõpuleviimiseks laadige alla järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="f6347-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="f6347-114">Sisu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f6347-114">Content description</span></span>                         | <span data-ttu-id="f6347-115">Fail</span><span class="sxs-lookup"><span data-stu-id="f6347-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="f6347-116">Sissetulev fail XLSX-vormingus – mall</span><span class="sxs-lookup"><span data-stu-id="f6347-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="f6347-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="f6347-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="f6347-118">Sissetulev fail XLSX-vormingus – näidisandmed</span><span class="sxs-lookup"><span data-stu-id="f6347-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="f6347-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="f6347-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="f6347-120">Kui te pole järgmist tegevusejuhist, [Elektrooniline aruandlus: nõutud konfiguratsioonide loomine andmete importimiseks välisest failist](./tasks/er-required-configurations-import-data.md), praeguses rakenduses Dynamics 365 for Finance and Operation veel vaadanud, laadige alla järgmine fail.</span><span class="sxs-lookup"><span data-stu-id="f6347-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="f6347-121">Sisu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f6347-121">Content description</span></span>    | <span data-ttu-id="f6347-122">Fail</span><span class="sxs-lookup"><span data-stu-id="f6347-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f6347-123">Elektroonilise aruandluse mudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="f6347-123">ER model configuration</span></span> | [<span data-ttu-id="f6347-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="f6347-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
