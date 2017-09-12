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
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 05ca41dd5d660e9f0ef72ee5bd49d800645081a5
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="b8dde-103">Vahemikuga intressikoodi loomine</span><span class="sxs-lookup"><span data-stu-id="b8dde-103">Create an interest code with a range</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8dde-104">Viivisekoodid saab seadistada nii, et arvutatakse erinevad viivisesummad väärtuste vahemiku põhjal.</span><span class="sxs-lookup"><span data-stu-id="b8dde-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="b8dde-105">See protseduur näitab, kuidas viivisekoodi ja sellele vahemikku lisada.</span><span class="sxs-lookup"><span data-stu-id="b8dde-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="b8dde-106">Avage Krediit ja sissenõuded > Intress > Intressikoodide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="b8dde-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="b8dde-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b8dde-107">Click New.</span></span>
3. <span data-ttu-id="b8dde-108">Sisestage väljale Viivisekood viivisekoodi nimi.</span><span class="sxs-lookup"><span data-stu-id="b8dde-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="b8dde-109">Sisestage väljale Kirjeldus viivisekoodi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b8dde-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="b8dde-110">Valige kuu.</span><span class="sxs-lookup"><span data-stu-id="b8dde-110">Select Month.</span></span>
6. <span data-ttu-id="b8dde-111">Laiendage jaotist Tulud.</span><span class="sxs-lookup"><span data-stu-id="b8dde-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="b8dde-112">Laiendage jaotist Tulud valuuta jaotisega.</span><span class="sxs-lookup"><span data-stu-id="b8dde-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="b8dde-113">Määrake väljal Pearaamatu sisestuskonto soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="b8dde-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="b8dde-114">Tehke väljal Intress vahemiku järgi valik Kuud.</span><span class="sxs-lookup"><span data-stu-id="b8dde-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="b8dde-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b8dde-115">Click Add.</span></span>
11. <span data-ttu-id="b8dde-116">Sisestage väljale Kirjeldus selle valuuta ja vahemiku kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b8dde-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="b8dde-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b8dde-117">Click Save.</span></span>
13. <span data-ttu-id="b8dde-118">Klõpsake valikut Vahemikud.</span><span class="sxs-lookup"><span data-stu-id="b8dde-118">Click Ranges.</span></span>
14. <span data-ttu-id="b8dde-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b8dde-119">Click New.</span></span>
15. <span data-ttu-id="b8dde-120">Sisestage algväärtuseks 0 ja seejärel viiviseprotsent kuus, mida viivise arvutamiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="b8dde-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="b8dde-121">Meie näites on see 1,5.</span><span class="sxs-lookup"><span data-stu-id="b8dde-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="b8dde-122">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="b8dde-122">Click New.</span></span>
17. <span data-ttu-id="b8dde-123">Sisestage järgmiseks algväärtuseks 4, mis on esimene kuu, millest alates uut viivisesummat arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="b8dde-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="b8dde-124">Sisestage viiviseprotsent kuus, mida kasutatakse viivise arvutamiseks alates 4. kuust.</span><span class="sxs-lookup"><span data-stu-id="b8dde-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="b8dde-125">Selles näites on viiviseprotsent 2,0.</span><span class="sxs-lookup"><span data-stu-id="b8dde-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="b8dde-126">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="b8dde-126">Click New.</span></span>
20. <span data-ttu-id="b8dde-127">Sisestage järgmiseks algväärtuseks 7, mis on järgmine kuu, millest alates uut viivisesummat arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="b8dde-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="b8dde-128">Sisestage viiviseprotsent kuus, mida kasutatakse viivise arvutamiseks alates 7. kuust.</span><span class="sxs-lookup"><span data-stu-id="b8dde-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="b8dde-129">Selles näites on viiviseprotsent 2,5.</span><span class="sxs-lookup"><span data-stu-id="b8dde-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="b8dde-130">Seadistuse lõpuleviimiseks klõpsake nuppu Sule.</span><span class="sxs-lookup"><span data-stu-id="b8dde-130">Click Close to complete the setup.</span></span>


