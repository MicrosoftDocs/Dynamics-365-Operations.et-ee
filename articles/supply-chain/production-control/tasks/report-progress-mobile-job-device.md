---
title: Edenemisteabe esitamine töö mobiilses seadmes
description: See protseduur näitab, kuidas käivitada tootmistööd ja edastada andmeid selle edenemise kohta tööseadme registreerimisvormil.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm, JmgRegistrationTouchReportProgress, JmgFeedbackWizard, JmgJobBundleProdFeedback
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c08822dc3960ba5fc85399ca236a31aaf2c38f1f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010943"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="0e3cb-103">Edenemisteabe esitamine töö mobiilses seadmes</span><span class="sxs-lookup"><span data-stu-id="0e3cb-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e3cb-104">See protseduur näitab, kuidas käivitada tootmistööd ja edastada andmeid selle edenemise kohta tööseadme registreerimisvormil.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="0e3cb-105">Selle protseduuri kasutamiseks peab teil olema kasutajakontoga seotud süsteemiadministraatori või masinaoperaatori roll.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="0e3cb-106">Avage Tootmise juhtimine > Tootmise käivitamine > Töökaardi vahend.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="0e3cb-107">Sisestage väljale WorkerTextField töötaja pääse.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="0e3cb-108">Tippige demoettevõtte USMF andmetes 123 – Christina Portra ...</span><span class="sxs-lookup"><span data-stu-id="0e3cb-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="0e3cb-109">Klõpsake valikut Sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-109">Click Log in.</span></span>
4. <span data-ttu-id="0e3cb-110">Klõpsake nuppu Filter.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-110">Click the Filter button.</span></span>
5. <span data-ttu-id="0e3cb-111">Märkige või tühjendage ruut Rakenda konfiguratsioonifilter.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="0e3cb-112">Filtri määramisel saate kasutada USMF-i puhul tootmisüksust 110.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="0e3cb-113">Valige väljalt Tootmisüksus ressursigrupp, mille tootmistöödega töötaja saab töötada.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="0e3cb-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0e3cb-115">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-115">Click OK.</span></span>
9. <span data-ttu-id="0e3cb-116">Klõpsake nuppu Alusta tööd.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-116">Click the Start job button.</span></span>
10. <span data-ttu-id="0e3cb-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-117">Click OK.</span></span>
11. <span data-ttu-id="0e3cb-118">Klõpsake nuppu Edenemisest teadaandmine.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="0e3cb-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-119">Click OK.</span></span>
13. <span data-ttu-id="0e3cb-120">Klõpsake nuppu Järgmine töö.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-120">Click the Next job button.</span></span>
14. <span data-ttu-id="0e3cb-121">Klõpsake nuppu Määratud, et näha kõigi tootmistööde ülevaadet.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="0e3cb-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-122">Close the page.</span></span>
16. <span data-ttu-id="0e3cb-123">Klõpsake nuppu Vaheaeg.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-123">Click the Break button.</span></span>
17. <span data-ttu-id="0e3cb-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="0e3cb-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-125">Click OK.</span></span>
19. <span data-ttu-id="0e3cb-126">Klõpsake nuppu Lahkumas.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="0e3cb-127">Valige väljalogimiseks.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-127">Select to log out.</span></span>
21. <span data-ttu-id="0e3cb-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-128">Click OK.</span></span>
22. <span data-ttu-id="0e3cb-129">Logige väljal WorkerTextField uuesti sisse.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="0e3cb-130">Demoettevõtte USMF-i andmetes võite valida töötaja 123.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="0e3cb-131">Klõpsake valikut Sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-131">Click Log in.</span></span>
24. <span data-ttu-id="0e3cb-132">Klõpsake valikut Lõpeta vaheaeg.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-132">Click Stop break.</span></span>
25. <span data-ttu-id="0e3cb-133">Klõpsake nuppu Tegevus.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-133">Click the Activity button.</span></span>
26. <span data-ttu-id="0e3cb-134">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-134">Click Cancel.</span></span>
27. <span data-ttu-id="0e3cb-135">Klõpsake nuppu Lahkumas.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="0e3cb-136">Valige väljaregistreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-136">Select to clock out.</span></span>
29. <span data-ttu-id="0e3cb-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-137">Click OK.</span></span>
30. <span data-ttu-id="0e3cb-138">Valige põhjus, miks te varem välja registreerite.</span><span class="sxs-lookup"><span data-stu-id="0e3cb-138">Select a reason why you are clocking out early.</span></span>

