---
title: Soodustuskõlblikkuse töötlemine
description: See protseduur näitab, kuidas soodustuskõlblikkuse protsess töötab.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 57e3e1dde4b4c8038b151dabf17af0f911f2ba07
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008771"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="e7096-103">Soodustuskõlblikkuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="e7096-103">Benefit eligibility process</span></span>

<span data-ttu-id="e7096-104">See protseduur näitab, kuidas soodustuskõlblikkuse protsess töötab.</span><span class="sxs-lookup"><span data-stu-id="e7096-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="e7096-105">Kui protsess on lõpule viidud, saab tulemusi vaadata.</span><span class="sxs-lookup"><span data-stu-id="e7096-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="e7096-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e7096-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="e7096-107">Avage Personaliarvestus > Soodustused > Soodustused.</span><span class="sxs-lookup"><span data-stu-id="e7096-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="e7096-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e7096-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e7096-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e7096-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e7096-110">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="e7096-110">Click Edit.</span></span>
5. <span data-ttu-id="e7096-111">Valige väljal Sobivus väärtus Reegli põhjal.</span><span class="sxs-lookup"><span data-stu-id="e7096-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="e7096-112">Valige väljal Reegli tüüp soodustuse poliitika reegel, mida soovite soodustusele rakendada.</span><span class="sxs-lookup"><span data-stu-id="e7096-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="e7096-113">Klõpsake toimingupaanil suvandit Soodustus.</span><span class="sxs-lookup"><span data-stu-id="e7096-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="e7096-114">Klõpsake valikut Kõlblikkuse sündmuse loomine, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="e7096-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="e7096-115">Tippige väärtus väljale Sündmus.</span><span class="sxs-lookup"><span data-stu-id="e7096-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="e7096-116">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e7096-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="e7096-117">Tehke väljal Sündmuse tüüp valik Registreerimise avamine.</span><span class="sxs-lookup"><span data-stu-id="e7096-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="e7096-118">Sisestage kuupäev ja kellaaeg väljale Kehtivuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="e7096-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="e7096-119">Sisestage kuupäev ja kellaaeg väljale Registreerimisperiood.</span><span class="sxs-lookup"><span data-stu-id="e7096-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="e7096-120">Sisestage number väljale Registreerimispäevad.</span><span class="sxs-lookup"><span data-stu-id="e7096-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="e7096-121">Klõpsake valikut Loo sündmus.</span><span class="sxs-lookup"><span data-stu-id="e7096-121">Click Create event.</span></span>
16. <span data-ttu-id="e7096-122">Klõpsake käsku Lisa töötajate kiirkaardile.</span><span class="sxs-lookup"><span data-stu-id="e7096-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="e7096-123">Tehke väljal Tüübi alusel kuvamine valik Töötajad.</span><span class="sxs-lookup"><span data-stu-id="e7096-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="e7096-124">Tehke väljal Juriidilise isiku alusel kuvamine valik Praegune juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="e7096-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="e7096-125">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="e7096-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="e7096-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e7096-126">Click OK.</span></span>
21. <span data-ttu-id="e7096-127">Klõpsake suvandit Töötle.</span><span class="sxs-lookup"><span data-stu-id="e7096-127">Click Process.</span></span>
22. <span data-ttu-id="e7096-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e7096-128">Click OK.</span></span>
23. <span data-ttu-id="e7096-129">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="e7096-129">Refresh the page.</span></span>
24. <span data-ttu-id="e7096-130">Klõpsake käsku Kuva tulemused.</span><span class="sxs-lookup"><span data-stu-id="e7096-130">Click Show results.</span></span>
25. <span data-ttu-id="e7096-131">Avage oleku veeru filter.</span><span class="sxs-lookup"><span data-stu-id="e7096-131">Open Status column filter.</span></span>
26. <span data-ttu-id="e7096-132">Sordi A-st Z-ni</span><span class="sxs-lookup"><span data-stu-id="e7096-132">Sort A to Z</span></span>
