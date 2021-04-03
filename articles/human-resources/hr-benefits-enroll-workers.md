---
title: Töötajate soodustuste registreerimine ja eemaldamine
description: See protseduur näitab, kuidas ühe töötaja saab registreerida vähemalt ühe soodustuse saajaks ning kuidas mitu töötajat saab soodustuse saajaks registreerida.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cb56d11cb3acd1e8e39765284269234fc632f17f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465098"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="ffe42-103">Töötajate soodustuste registreerimine ja eemaldamine</span><span class="sxs-lookup"><span data-stu-id="ffe42-103">Enroll and remove benefits from workers</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="ffe42-104">See protseduur näitab, kuidas ühe töötaja saab registreerida vähemalt ühe soodustuse saajaks ning kuidas mitu töötajat saab soodustuse saajaks registreerida.</span><span class="sxs-lookup"><span data-stu-id="ffe42-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="ffe42-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ffe42-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="ffe42-106">Ühe töötaja registreerimine soodustustes</span><span class="sxs-lookup"><span data-stu-id="ffe42-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="ffe42-107">Avage Personaliarvestus > Töötajad > Töötajad</span><span class="sxs-lookup"><span data-stu-id="ffe42-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="ffe42-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ffe42-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ffe42-109">Klõpsake suvandit Soodustused.</span><span class="sxs-lookup"><span data-stu-id="ffe42-109">Click Benefits.</span></span>
4. <span data-ttu-id="ffe42-110">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="ffe42-110">Click New.</span></span>
5. <span data-ttu-id="ffe42-111">Valige või sisestage väärtus väljal Soodustus.</span><span class="sxs-lookup"><span data-stu-id="ffe42-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="ffe42-112">Sisestage kuupäev ja kellaaeg väljale Kehtivuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="ffe42-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="ffe42-113">Sisestage kuupäev ja kellaaeg väljale Kehtivuse lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="ffe42-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="ffe42-114">Laiendage jaotist Kasusaajad, kui soodustusele on vaja kasusaajaid lisada.</span><span class="sxs-lookup"><span data-stu-id="ffe42-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="ffe42-115">Saate lisada sellel lehel ka sõltuvaid üksusi, kui seda on soodustuse puhul vaja.</span><span class="sxs-lookup"><span data-stu-id="ffe42-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="ffe42-116">Samuti saab sellel lehel redigeerida soodustuse saamiseks registreerimise üksikasju või kustutada registreerimise.</span><span class="sxs-lookup"><span data-stu-id="ffe42-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="ffe42-117">Kui olete soodustuse registreerimise muudatuste tegemise lõpetanud, sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ffe42-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="ffe42-118">Mitme töötaja registreerimine soodustuses</span><span class="sxs-lookup"><span data-stu-id="ffe42-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="ffe42-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ffe42-119">Close the page.</span></span>
2. <span data-ttu-id="ffe42-120">Avage Personaliarvestus > Töötajad > Töötajad</span><span class="sxs-lookup"><span data-stu-id="ffe42-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="ffe42-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ffe42-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ffe42-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ffe42-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ffe42-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ffe42-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ffe42-124">Klõpsake valikut Soodustuste registreerimine.</span><span class="sxs-lookup"><span data-stu-id="ffe42-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="ffe42-125">Valige või sisestage väärtus väljal Soodustus.</span><span class="sxs-lookup"><span data-stu-id="ffe42-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="ffe42-126">Sisestage kuupäev ja kellaaeg väljale Kehtivuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="ffe42-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="ffe42-127">Sisestage kuupäev ja kellaaeg väljale Kehtivuse lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="ffe42-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="ffe42-128">Klõpsake valikut Registreeri.</span><span class="sxs-lookup"><span data-stu-id="ffe42-128">Click Enroll.</span></span>
11. <span data-ttu-id="ffe42-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ffe42-129">Close the page.</span></span>
12. <span data-ttu-id="ffe42-130">Avage Personaliarvestus > Soodustused > Registreerimine > Soodustuse registreerimise tulemused</span><span class="sxs-lookup"><span data-stu-id="ffe42-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="ffe42-131">Otsige üles vajalik soodustuse tulemuste kirje.</span><span class="sxs-lookup"><span data-stu-id="ffe42-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="ffe42-132">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ffe42-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="ffe42-133">Sellel lehel saate vaadata, millised töötajad on soodustuse saamiseks registreeritud ja millised mitte.</span><span class="sxs-lookup"><span data-stu-id="ffe42-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]