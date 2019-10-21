---
title: Hulgivärbamisprojekti loomine
description: See protseduur annab ülevaate hulgivärbamisprojekti seadistamise protsessist.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea0f4638a968d2aecf4e3bb27acbd19e6455a8b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190622"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="120e5-103">Hulgivärbamisprojekti loomine</span><span class="sxs-lookup"><span data-stu-id="120e5-103">Create a mass hire project</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="120e5-104">See protseduur annab ülevaate hulgivärbamisprojekti seadistamise protsessist.</span><span class="sxs-lookup"><span data-stu-id="120e5-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="120e5-105">Värbaja saab hulgivärbamisprojekte kasutada hõlpsalt mitme ametikoha loomiseks ja nendele ametikohtadele töötajate värbamiseks.</span><span class="sxs-lookup"><span data-stu-id="120e5-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="120e5-106">Selle protseduuri alustamiseks avage Inimressursid > Värbamine > Hulgivärbamisprojektid.</span><span class="sxs-lookup"><span data-stu-id="120e5-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="120e5-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="120e5-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="120e5-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="120e5-108">Click New.</span></span>
2. <span data-ttu-id="120e5-109">Sisestage väärtus väljale Hulgivärbamisprojekt.</span><span class="sxs-lookup"><span data-stu-id="120e5-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="120e5-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="120e5-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="120e5-111">Sisestage kuupäev väljale Projekti algus.</span><span class="sxs-lookup"><span data-stu-id="120e5-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="120e5-112">Sisestage kuupäev väljale Projekti lõpp.</span><span class="sxs-lookup"><span data-stu-id="120e5-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="120e5-113">Klõpsake suvandit Ava projekt.</span><span class="sxs-lookup"><span data-stu-id="120e5-113">Click Open project.</span></span>
7. <span data-ttu-id="120e5-114">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="120e5-114">Click Yes.</span></span>
8. <span data-ttu-id="120e5-115">Klõpsake suvandit Ametikohtade loomine.</span><span class="sxs-lookup"><span data-stu-id="120e5-115">Click Create positions.</span></span>
9. <span data-ttu-id="120e5-116">Sisestage väljale Kogus ametikohtade arv, mida soovite luua.</span><span class="sxs-lookup"><span data-stu-id="120e5-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="120e5-117">Alguskuupäev muutub uute töötajate palkamise kuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="120e5-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="120e5-118">Lõppkuupäev muutub uute töötajate töösuhte lõppemise kuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="120e5-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="120e5-119">Määrake, kas uued töötajad on Töötajad või Töövõtjad.</span><span class="sxs-lookup"><span data-stu-id="120e5-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="120e5-120">Klõpsake väljal Töö ripploendi nuppu, et valida töö, mille puhul ametikohti luua.</span><span class="sxs-lookup"><span data-stu-id="120e5-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="120e5-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="120e5-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="120e5-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="120e5-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="120e5-123">Täistööaja vaikeväärtus tuleneb valitud tööst.</span><span class="sxs-lookup"><span data-stu-id="120e5-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="120e5-124">Saate seda vajaduse korral muuta.</span><span class="sxs-lookup"><span data-stu-id="120e5-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="120e5-125">Lisaks saate valida uute ametikohtade osakonna.</span><span class="sxs-lookup"><span data-stu-id="120e5-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="120e5-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="120e5-126">Click OK.</span></span>

