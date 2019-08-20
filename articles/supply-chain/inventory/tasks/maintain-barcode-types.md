---
title: Vöötkoodi tüüpide haldamine
description: See protseduur selgitab, kuidas seadistada uut vöötkoodi määratlust, mida saab seejärel kasutada komplekteerimislehe aruande osana.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0551784ff55f5dc05fbe92ee354316eb04d755cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845434"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="852a6-103">Vöötkoodi tüüpide haldamine</span><span class="sxs-lookup"><span data-stu-id="852a6-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="852a6-104">See protseduur selgitab, kuidas seadistada uut vöötkoodi määratlust, mida saab seejärel kasutada komplekteerimislehe aruande osana.</span><span class="sxs-lookup"><span data-stu-id="852a6-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="852a6-105">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="852a6-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="852a6-106">USMF-i kasutamisel saate kasutada kuvatavaid näidisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="852a6-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="852a6-107">Neid ülesandeid täidab üldjuhul laohaldur.</span><span class="sxs-lookup"><span data-stu-id="852a6-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="852a6-108">Mine vöötkoodide juurde.</span><span class="sxs-lookup"><span data-stu-id="852a6-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="852a6-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="852a6-109">Click New.</span></span>
3. <span data-ttu-id="852a6-110">Tippige väärtus väljale Vöötkoodide häälestus.</span><span class="sxs-lookup"><span data-stu-id="852a6-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="852a6-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="852a6-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="852a6-112">Valige suvand väljalt Vöötkoodi tüüp.</span><span class="sxs-lookup"><span data-stu-id="852a6-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="852a6-113">USMF-i kasutamisel saate valida suvandi Kood 39.</span><span class="sxs-lookup"><span data-stu-id="852a6-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="852a6-114">Sisestage number väljale Suurus.</span><span class="sxs-lookup"><span data-stu-id="852a6-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="852a6-115">Sisestage number väljale Maksimaalne pikkus.</span><span class="sxs-lookup"><span data-stu-id="852a6-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="852a6-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="852a6-116">Click Save.</span></span>
9. <span data-ttu-id="852a6-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="852a6-117">Close the page.</span></span>
10. <span data-ttu-id="852a6-118">Minge jaotisse Varude ja laohalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="852a6-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="852a6-119">Valige või sisestage väärtus väljal Vöötkoodi häälestus.</span><span class="sxs-lookup"><span data-stu-id="852a6-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="852a6-120">Valige varem loodud vöötkoodiseadistus, kuid arvestage, et vöötkoodi vorming peab ühtima protsessis kasutatud kirjetüübi ainuidentifikaatori vorminguga.</span><span class="sxs-lookup"><span data-stu-id="852a6-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="852a6-121">Näiteks peab komplekteerimisprotsesside puhul vöötkoodi vorming ühtima komplekteerimisprotsessi viite vorminguga, mis on tavaliselt numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="852a6-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="852a6-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="852a6-122">Click Save.</span></span>
13. <span data-ttu-id="852a6-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="852a6-123">Close the page.</span></span>

