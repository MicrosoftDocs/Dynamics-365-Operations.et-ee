---
title: Kalendrite loomine ja tööaegade genereerimine
description: Kalendrid kirjeldavad operatsiooniressursside võimsust ja tööaegu. Selles artiklis selgitatakse, kuidas määratleda tööajamalli põhjal töökalendrit.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
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
ms.openlocfilehash: 38c0482c62e86e3e12e4bdd67f6d8f090ddfbfeb
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008729"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="8acda-104">Kalendrite loomine ja tööaegade genereerimine</span><span class="sxs-lookup"><span data-stu-id="8acda-104">Create calendars and generate working times</span></span>



<span data-ttu-id="8acda-105">Kalendrid kirjeldavad operatsiooniressursside võimsust ja tööaegu.</span><span class="sxs-lookup"><span data-stu-id="8acda-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="8acda-106">Selles artiklis selgitatakse, kuidas määratleda tööajamalli põhjal töökalendrit.</span><span class="sxs-lookup"><span data-stu-id="8acda-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="8acda-107">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="8acda-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="8acda-108">Valige kodulehel **Ressursi elutsükli haldus**.</span><span class="sxs-lookup"><span data-stu-id="8acda-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="8acda-109">Valige **Kalendrid**.</span><span class="sxs-lookup"><span data-stu-id="8acda-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="8acda-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8acda-110">Select **New**.</span></span>
4. <span data-ttu-id="8acda-111">Väljal **Kalender** liigitage oma kalender.</span><span class="sxs-lookup"><span data-stu-id="8acda-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="8acda-112">See on selle kalendri ID, mida kasutatakse viitena kalendrite määramisel näiteks operatsiooniressursile või ressursigrupile.</span><span class="sxs-lookup"><span data-stu-id="8acda-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="8acda-113">Väljal **Nimi** liigitage oma kalender.</span><span class="sxs-lookup"><span data-stu-id="8acda-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="8acda-114">Sisestage number väljale **Standardne tööpäev tundides**.</span><span class="sxs-lookup"><span data-stu-id="8acda-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="8acda-115">Veenduge, et rida on valitud, seejärel valige toimingupaanilt **Tööajad**.</span><span class="sxs-lookup"><span data-stu-id="8acda-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="8acda-116">Valige **Koosta tööajad**.</span><span class="sxs-lookup"><span data-stu-id="8acda-116">Select **Compose working times**.</span></span> <span data-ttu-id="8acda-117">Looge töötunnid iga päeva kohta perioodil, millal on vaja tööd plaanida.</span><span class="sxs-lookup"><span data-stu-id="8acda-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="8acda-118">Aja möödudes saate luua tööaegu täiendavatele perioodidele.</span><span class="sxs-lookup"><span data-stu-id="8acda-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="8acda-119">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="8acda-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="8acda-120">See on esimene päev, millal see kalender peab olema avatud.</span><span class="sxs-lookup"><span data-stu-id="8acda-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="8acda-121">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="8acda-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="8acda-122">See on viimane päev, millal see kalender avatud on.</span><span class="sxs-lookup"><span data-stu-id="8acda-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="8acda-123">Valige või sisestage väärtus väljal **Tööajamall**.</span><span class="sxs-lookup"><span data-stu-id="8acda-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="8acda-124">Tööajamall määratleb iga nädalapäeva töötunnid.</span><span class="sxs-lookup"><span data-stu-id="8acda-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="8acda-125">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8acda-125">Select **OK**.</span></span>
13. <span data-ttu-id="8acda-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8acda-126">Close the page.</span></span>

