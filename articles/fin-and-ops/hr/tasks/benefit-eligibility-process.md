--- 
title: "Soodustuskõlblikkuse töötlemine"
description: "See protseduur näitab, kuidas soodustuskõlblikkuse protsess töötab."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e98d48fc31a9dfd4959e88f31e00317afbfeb8c1
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="5fba6-103">Soodustuskõlblikkuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="5fba6-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5fba6-104">See protseduur näitab, kuidas soodustuskõlblikkuse protsess töötab.</span><span class="sxs-lookup"><span data-stu-id="5fba6-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="5fba6-105">Kui protsess on lõpule viidud, saab tulemusi vaadata.</span><span class="sxs-lookup"><span data-stu-id="5fba6-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="5fba6-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="5fba6-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5fba6-107">Avage Personaliarvestus > Soodustused > Soodustused.</span><span class="sxs-lookup"><span data-stu-id="5fba6-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="5fba6-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5fba6-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5fba6-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5fba6-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5fba6-110">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5fba6-110">Click Edit.</span></span>
5. <span data-ttu-id="5fba6-111">Valige väljal Sobivus väärtus Reegli põhjal.</span><span class="sxs-lookup"><span data-stu-id="5fba6-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="5fba6-112">Valige väljal Reegli tüüp soodustuse poliitika reegel, mida soovite soodustusele rakendada.</span><span class="sxs-lookup"><span data-stu-id="5fba6-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="5fba6-113">Klõpsake toimingupaanil suvandit Soodustus.</span><span class="sxs-lookup"><span data-stu-id="5fba6-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="5fba6-114">Klõpsake valikut Kõlblikkuse sündmuse loomine, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="5fba6-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="5fba6-115">Tippige väärtus väljale Sündmus.</span><span class="sxs-lookup"><span data-stu-id="5fba6-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="5fba6-116">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="5fba6-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="5fba6-117">Tehke väljal Sündmuse tüüp valik Registreerimise avamine.</span><span class="sxs-lookup"><span data-stu-id="5fba6-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="5fba6-118">Sisestage kuupäev ja kellaaeg väljale Kehtivuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="5fba6-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="5fba6-119">Sisestage kuupäev ja kellaaeg väljale Registreerimisperiood.</span><span class="sxs-lookup"><span data-stu-id="5fba6-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="5fba6-120">Sisestage number väljale Registreerimispäevad.</span><span class="sxs-lookup"><span data-stu-id="5fba6-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="5fba6-121">Klõpsake valikut Loo sündmus.</span><span class="sxs-lookup"><span data-stu-id="5fba6-121">Click Create event.</span></span>
16. <span data-ttu-id="5fba6-122">Klõpsake käsku Lisa töötajate kiirkaardile.</span><span class="sxs-lookup"><span data-stu-id="5fba6-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="5fba6-123">Tehke väljal Tüübi alusel kuvamine valik Töötajad.</span><span class="sxs-lookup"><span data-stu-id="5fba6-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="5fba6-124">Tehke väljal Juriidilise isiku alusel kuvamine valik Praegune juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="5fba6-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="5fba6-125">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="5fba6-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="5fba6-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5fba6-126">Click OK.</span></span>
21. <span data-ttu-id="5fba6-127">Klõpsake suvandit Töötle.</span><span class="sxs-lookup"><span data-stu-id="5fba6-127">Click Process.</span></span>
22. <span data-ttu-id="5fba6-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5fba6-128">Click OK.</span></span>
23. <span data-ttu-id="5fba6-129">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="5fba6-129">Refresh the page.</span></span>
24. <span data-ttu-id="5fba6-130">Klõpsake käsku Kuva tulemused.</span><span class="sxs-lookup"><span data-stu-id="5fba6-130">Click Show results.</span></span>
25. <span data-ttu-id="5fba6-131">Avage oleku veeru filter.</span><span class="sxs-lookup"><span data-stu-id="5fba6-131">Open Status column filter.</span></span>
26. <span data-ttu-id="5fba6-132">Sordi A-st Z-ni</span><span class="sxs-lookup"><span data-stu-id="5fba6-132">Sort A to Z</span></span>


