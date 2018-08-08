---
title: "Vöötkooditüüpide haldamine"
description: "See protseduur selgitab, kuidas seadistada uut vöötkoodi määratlust, mida saab seejärel kasutada komplekteerimislehe aruande osana."
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: bcaba4b56f665acb97a74982053dfd14d241344d
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="maintain-bar-code-types"></a><span data-ttu-id="8dd01-103">Vöötkooditüüpide haldamine</span><span class="sxs-lookup"><span data-stu-id="8dd01-103">Maintain bar code types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8dd01-104">See protseduur selgitab, kuidas seadistada uut vöötkoodi määratlust, mida saab seejärel kasutada komplekteerimislehe aruande osana.</span><span class="sxs-lookup"><span data-stu-id="8dd01-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="8dd01-105">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="8dd01-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="8dd01-106">USMF-i kasutamisel saate kasutada kuvatavaid näidisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="8dd01-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="8dd01-107">Neid ülesandeid täidab üldjuhul laohaldur.</span><span class="sxs-lookup"><span data-stu-id="8dd01-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="8dd01-108">Mine vöötkoodide juurde.</span><span class="sxs-lookup"><span data-stu-id="8dd01-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="8dd01-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8dd01-109">Click New.</span></span>
3. <span data-ttu-id="8dd01-110">Tippige väärtus väljale Vöötkoodide häälestus.</span><span class="sxs-lookup"><span data-stu-id="8dd01-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="8dd01-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="8dd01-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8dd01-112">Valige suvand väljalt Vöötkoodi tüüp.</span><span class="sxs-lookup"><span data-stu-id="8dd01-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="8dd01-113">USMF-i kasutamisel saate valida suvandi Kood 39.</span><span class="sxs-lookup"><span data-stu-id="8dd01-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="8dd01-114">Sisestage number väljale Suurus.</span><span class="sxs-lookup"><span data-stu-id="8dd01-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="8dd01-115">Sisestage number väljale Maksimaalne pikkus.</span><span class="sxs-lookup"><span data-stu-id="8dd01-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="8dd01-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="8dd01-116">Click Save.</span></span>
9. <span data-ttu-id="8dd01-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8dd01-117">Close the page.</span></span>
10. <span data-ttu-id="8dd01-118">Minge jaotisse Varude ja laohalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="8dd01-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="8dd01-119">Valige või sisestage väärtus väljal Vöötkoodi häälestus.</span><span class="sxs-lookup"><span data-stu-id="8dd01-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="8dd01-120">Valige varem loodud vöötkoodiseadistus, kuid arvestage, et vöötkoodi vorming peab ühtima protsessis kasutatud kirjetüübi ainuidentifikaatori vorminguga.</span><span class="sxs-lookup"><span data-stu-id="8dd01-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="8dd01-121">Näiteks peab komplekteerimisprotsesside puhul vöötkoodi vorming ühtima komplekteerimisprotsessi viite vorminguga, mis on tavaliselt numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="8dd01-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="8dd01-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="8dd01-122">Click Save.</span></span>
13. <span data-ttu-id="8dd01-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8dd01-123">Close the page.</span></span>

