--- 
title: Vahemikuga intressikoodi loomine
description: "Viivisekoodid saab seadistada nii, et arvutatakse erinevad viivisesummad väärtuste vahemiku põhjal."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e7b6cbc70058c9b9a8edaf3c3303fa7ba0e9da44
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="2c12d-103">Vahemikuga intressikoodi loomine</span><span class="sxs-lookup"><span data-stu-id="2c12d-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c12d-104">Viivisekoodid saab seadistada nii, et arvutatakse erinevad viivisesummad väärtuste vahemiku põhjal.</span><span class="sxs-lookup"><span data-stu-id="2c12d-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="2c12d-105">See protseduur näitab, kuidas viivisekoodi ja sellele vahemikku lisada.</span><span class="sxs-lookup"><span data-stu-id="2c12d-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="2c12d-106">Avage Krediit ja sissenõuded > Intress > Intressikoodide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="2c12d-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="2c12d-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2c12d-107">Click New.</span></span>
3. <span data-ttu-id="2c12d-108">Sisestage väljale Viivisekood viivisekoodi nimi.</span><span class="sxs-lookup"><span data-stu-id="2c12d-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="2c12d-109">Sisestage väljale Kirjeldus viivisekoodi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="2c12d-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="2c12d-110">Valige kuu.</span><span class="sxs-lookup"><span data-stu-id="2c12d-110">Select Month.</span></span>
6. <span data-ttu-id="2c12d-111">Laiendage jaotist Tulud.</span><span class="sxs-lookup"><span data-stu-id="2c12d-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="2c12d-112">Laiendage jaotist Tulud valuuta jaotisega.</span><span class="sxs-lookup"><span data-stu-id="2c12d-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="2c12d-113">Määrake väljal Pearaamatu sisestuskonto soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="2c12d-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="2c12d-114">Tehke väljal Intress vahemiku järgi valik Kuud.</span><span class="sxs-lookup"><span data-stu-id="2c12d-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="2c12d-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="2c12d-115">Click Add.</span></span>
11. <span data-ttu-id="2c12d-116">Sisestage väljale Kirjeldus selle valuuta ja vahemiku kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="2c12d-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="2c12d-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2c12d-117">Click Save.</span></span>
13. <span data-ttu-id="2c12d-118">Klõpsake valikut Vahemikud.</span><span class="sxs-lookup"><span data-stu-id="2c12d-118">Click Ranges.</span></span>
14. <span data-ttu-id="2c12d-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2c12d-119">Click New.</span></span>
15. <span data-ttu-id="2c12d-120">Sisestage algväärtuseks 0 ja seejärel viiviseprotsent kuus, mida viivise arvutamiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="2c12d-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="2c12d-121">Meie näites on see 1,5.</span><span class="sxs-lookup"><span data-stu-id="2c12d-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="2c12d-122">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="2c12d-122">Click New.</span></span>
17. <span data-ttu-id="2c12d-123">Sisestage järgmiseks algväärtuseks 4, mis on esimene kuu, millest alates uut viivisesummat arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="2c12d-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="2c12d-124">Sisestage viiviseprotsent kuus, mida kasutatakse viivise arvutamiseks alates 4. kuust.</span><span class="sxs-lookup"><span data-stu-id="2c12d-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="2c12d-125">Selles näites on viiviseprotsent 2,0.</span><span class="sxs-lookup"><span data-stu-id="2c12d-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="2c12d-126">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="2c12d-126">Click New.</span></span>
20. <span data-ttu-id="2c12d-127">Sisestage järgmiseks algväärtuseks 7, mis on järgmine kuu, millest alates uut viivisesummat arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="2c12d-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="2c12d-128">Sisestage viiviseprotsent kuus, mida kasutatakse viivise arvutamiseks alates 7. kuust.</span><span class="sxs-lookup"><span data-stu-id="2c12d-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="2c12d-129">Selles näites on viiviseprotsent 2,5.</span><span class="sxs-lookup"><span data-stu-id="2c12d-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="2c12d-130">Seadistuse lõpuleviimiseks klõpsake nuppu Sule.</span><span class="sxs-lookup"><span data-stu-id="2c12d-130">Click Close to complete the setup.</span></span>


