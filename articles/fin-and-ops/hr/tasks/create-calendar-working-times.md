---
title: Kalendri ja tööaegade loomine
description: Kalendrid kirjeldavad operatsiooniressursside võimsust ja tööaegu.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba4bd51d2102b3036307f34ab46f94f83df4f461
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "856987"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="12166-103">Kalendri ja tööaegade loomine</span><span class="sxs-lookup"><span data-stu-id="12166-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12166-104">Kalendrid kirjeldavad operatsiooniressursside võimsust ja tööaegu.</span><span class="sxs-lookup"><span data-stu-id="12166-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="12166-105">Selle protseduuri abil saate määratleda töökalendri tööajamalli põhjal.</span><span class="sxs-lookup"><span data-stu-id="12166-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="12166-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="12166-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="12166-107">Avage Kõik tööruumid > Ressursi elutsükli haldus.</span><span class="sxs-lookup"><span data-stu-id="12166-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="12166-108">Klõpsake valikut Kalendrid.</span><span class="sxs-lookup"><span data-stu-id="12166-108">Click Calendars.</span></span>
3. <span data-ttu-id="12166-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="12166-109">Click New.</span></span>
4. <span data-ttu-id="12166-110">Sisestage väärtus väljale Kalender.</span><span class="sxs-lookup"><span data-stu-id="12166-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="12166-111">See on selle kalendri ID, mida kasutatakse viitena kalendrite määramisel näiteks operatsiooniressursile või ressursigrupile.</span><span class="sxs-lookup"><span data-stu-id="12166-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="12166-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12166-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="12166-113">Sisestage number väljale Standardne tööpäev tundides.</span><span class="sxs-lookup"><span data-stu-id="12166-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="12166-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="12166-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="12166-115">Klõpsake valikut Tööajad.</span><span class="sxs-lookup"><span data-stu-id="12166-115">Click Working times.</span></span>
9. <span data-ttu-id="12166-116">Klõpsake valikut Koosta tööajad.</span><span class="sxs-lookup"><span data-stu-id="12166-116">Click Compose working times.</span></span>
    * <span data-ttu-id="12166-117">Looge töötunnid iga päeva kohta perioodil, millal on vaja tööd plaanida.</span><span class="sxs-lookup"><span data-stu-id="12166-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="12166-118">Aja möödudes saate luua tööaegu täiendavatele perioodidele.</span><span class="sxs-lookup"><span data-stu-id="12166-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="12166-119">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="12166-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="12166-120">See on esimene päev, millal see kalender peab olema avatud.</span><span class="sxs-lookup"><span data-stu-id="12166-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="12166-121">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="12166-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="12166-122">See on viimane päev, millal see kalender avatud on.</span><span class="sxs-lookup"><span data-stu-id="12166-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="12166-123">Valige või sisestage väärtus väljal Tööajamall.</span><span class="sxs-lookup"><span data-stu-id="12166-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="12166-124">Tööajamall määratleb iga nädalapäeva töötunnid.</span><span class="sxs-lookup"><span data-stu-id="12166-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="12166-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12166-125">Click OK.</span></span>
14. <span data-ttu-id="12166-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="12166-126">Close the page.</span></span>

