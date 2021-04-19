---
title: Vöötkoodi tüüpide haldamine
description: See protseduur selgitab, kuidas seadistada uut vöötkoodi määratlust, mida saab seejärel kasutada komplekteerimislehe aruande osana.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 937384f14d88dafd537888d862ee1e363ea20626
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809514"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="39066-103">Vöötkoodi tüüpide haldamine</span><span class="sxs-lookup"><span data-stu-id="39066-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39066-104">See protseduur selgitab, kuidas seadistada uut vöötkoodi määratlust, mida saab seejärel kasutada komplekteerimislehe aruande osana.</span><span class="sxs-lookup"><span data-stu-id="39066-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="39066-105">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="39066-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="39066-106">USMF-i kasutamisel saate kasutada kuvatavaid näidisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="39066-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="39066-107">Neid ülesandeid täidab üldjuhul laohaldur.</span><span class="sxs-lookup"><span data-stu-id="39066-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="39066-108">Mine vöötkoodide juurde.</span><span class="sxs-lookup"><span data-stu-id="39066-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="39066-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="39066-109">Click New.</span></span>
3. <span data-ttu-id="39066-110">Tippige väärtus väljale Vöötkoodide häälestus.</span><span class="sxs-lookup"><span data-stu-id="39066-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="39066-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="39066-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="39066-112">Valige suvand väljalt Vöötkoodi tüüp.</span><span class="sxs-lookup"><span data-stu-id="39066-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="39066-113">USMF-i kasutamisel saate valida suvandi Kood 39.</span><span class="sxs-lookup"><span data-stu-id="39066-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="39066-114">Sisestage number väljale Suurus.</span><span class="sxs-lookup"><span data-stu-id="39066-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="39066-115">Sisestage number väljale Maksimaalne pikkus.</span><span class="sxs-lookup"><span data-stu-id="39066-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="39066-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="39066-116">Click Save.</span></span>
9. <span data-ttu-id="39066-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="39066-117">Close the page.</span></span>
10. <span data-ttu-id="39066-118">Minge jaotisse Varude ja laohalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="39066-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="39066-119">Valige või sisestage väärtus väljal Vöötkoodi häälestus.</span><span class="sxs-lookup"><span data-stu-id="39066-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="39066-120">Valige varem loodud vöötkoodiseadistus, kuid arvestage, et vöötkoodi vorming peab ühtima protsessis kasutatud kirjetüübi ainuidentifikaatori vorminguga.</span><span class="sxs-lookup"><span data-stu-id="39066-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="39066-121">Näiteks peab komplekteerimisprotsesside puhul vöötkoodi vorming ühtima komplekteerimisprotsessi viite vorminguga, mis on tavaliselt numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="39066-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="39066-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="39066-122">Click Save.</span></span>
13. <span data-ttu-id="39066-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="39066-123">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]