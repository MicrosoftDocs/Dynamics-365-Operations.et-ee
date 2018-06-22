---
title: "Sissetulevate dokumentide sõelumine Microsoft Excelis"
description: "Selles teemas selgitatakse elektroonilise aruandluse vormingute kujundamist sissetulevates Microsoft Exceli failides oleva sisu sõelumiseks."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 001e287590b9f43ed38de803bcace3a25a6f6637
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2018

---

# <a name="parse-incoming-microsoft-excel-files"></a><span data-ttu-id="32aa8-103">Sissetulevate Microsoft Exceli failide sõelumine</span><span class="sxs-lookup"><span data-stu-id="32aa8-103">Parse incoming Microsoft Excel files</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="32aa8-104">Saate kujundada elektroonilise aruandluse vormingud sõeluma sissetulevaid Microsoft Exceli faile, mis esitavad andmeid Microsoft Exceli töövihikutes (XLSX-vormingus failid).</span><span class="sxs-lookup"><span data-stu-id="32aa8-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="32aa8-105">Seejärel saate neist failidest pärit sisu kasutada rakenduse andmete värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="32aa8-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="32aa8-106">See on kasulik järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="32aa8-106">This is useful if you:</span></span>

-   <span data-ttu-id="32aa8-107">Uue mudeli ja vormingu kujundamine, testides neid käitusajal.</span><span class="sxs-lookup"><span data-stu-id="32aa8-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="32aa8-108">Sellisel juhul simuleerib Excel tegelikke rakenduse andmeid.</span><span class="sxs-lookup"><span data-stu-id="32aa8-108">In this case, Excel will simulate the actual application data.</span></span>
-   <span data-ttu-id="32aa8-109">Lisaks rakenduse Exceli andmete haldamiseks ja soovite importida kindla aruande andmed.</span><span class="sxs-lookup"><span data-stu-id="32aa8-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="32aa8-110">Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusejuhiseid **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist (1. osa: vormingu kujundamine)** ja **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist (2. osa: andmete importimine)** (osad äriprotsessist 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)).</span><span class="sxs-lookup"><span data-stu-id="32aa8-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="32aa8-111">Need tegevusejuhised selgitavad, kuidas saab sissetulevat Exceli faili elektroonilise aruandluse vormingu abil sõeluda, et importida teavet sissetulevatest dokumentidest ja värskendada rakenduse andmeid.</span><span class="sxs-lookup"><span data-stu-id="32aa8-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="32aa8-112">Saate tegevusejuhise failid alla laadida [Microsofti allalaadimiskeskusse](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="32aa8-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="32aa8-113">Eespool nimetatud tegevusejuhiste lõpuleviimiseks laadige alla järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="32aa8-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="32aa8-114">Sisu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="32aa8-114">Content description</span></span>                        | <span data-ttu-id="32aa8-115">Fail</span><span class="sxs-lookup"><span data-stu-id="32aa8-115">File</span></span>                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="32aa8-116">Sissetulev fail XLSX-vormingus – mall</span><span class="sxs-lookup"><span data-stu-id="32aa8-116">Incoming file in .XLSX format - template</span></span>   | [<span data-ttu-id="32aa8-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="32aa8-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)  |
| <span data-ttu-id="32aa8-118">Sissetulev fail XLSX-vormingus – näidisandmed</span><span class="sxs-lookup"><span data-stu-id="32aa8-118">Incoming file in .XLSX format - sample data</span></span>| [<span data-ttu-id="32aa8-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="32aa8-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="32aa8-120">Kui te pole järgmist tegevusejuhist, [Elektrooniline aruandlus: nõutud konfiguratsioonide loomine andmete importimiseks välisest failist](./tasks/er-required-configurations-import-data.md), praeguses rakenduses Dynamics 365 for Finance and Operation veel vaadanud, laadige alla järgmine fail.</span><span class="sxs-lookup"><span data-stu-id="32aa8-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="32aa8-121">Sisu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="32aa8-121">Content description</span></span>                        | <span data-ttu-id="32aa8-122">Fail</span><span class="sxs-lookup"><span data-stu-id="32aa8-122">File</span></span>                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="32aa8-123">Elektroonilise aruandluse mudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="32aa8-123">ER model configuration</span></span>                     | [<span data-ttu-id="32aa8-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="32aa8-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)            |


